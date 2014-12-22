umask 022

TMP_INSTALLATION_DIR=VirtualBox
INSTALLATION_DIR=/opt/VirtualBox

mkdir -p -m 755 $TMP_INSTALLATION_DIR &&
tar xf VirtualBox.tar.bz2  -C $TMP_INSTALLATION_DIR &&

# make module
cd $TMP_INSTALLATION_DIR/src/vboxhost &&
make && 

prepare_install &&

make install && cd ../../../ &&

cp -af $TMP_INSTALLATION_DIR $INSTALLATION_DIR &&

chmod 4511 $INSTALLATION_DIR/VirtualBox &&
chmod 4511 $INSTALLATION_DIR/VBoxSDL &&
chmod 4511 $INSTALLATION_DIR/VBoxHeadless &&
chmod 4511 $INSTALLATION_DIR/VBoxNetDHCP &&
chmod 4511 $INSTALLATION_DIR/VBoxNetNAT &&

ln -sf $INSTALLATION_DIR/VBoxVMM.so $INSTALLATION_DIR/components/VBoxVMM.so &&
ln -sf $INSTALLATION_DIR/VBoxRT.so $INSTALLATION_DIR/components/VBoxRT.so &&
chmod 4511 $INSTALLATION_DIR/VBoxNetAdpCtl &&
chmod 4511 $INSTALLATION_DIR/VBoxVolInfo &&

chmod go-w $INSTALLATION_DIR &&

# Create symlinks to start binaries
ln -sf $INSTALLATION_DIR/VBox.sh /usr/bin/VirtualBox
ln -sf $INSTALLATION_DIR/VBox.sh /usr/bin/VBoxManage
ln -sf $INSTALLATION_DIR/VBox.sh /usr/bin/VBoxSDL
ln -sf $INSTALLATION_DIR/VBox.sh /usr/bin/VBoxVRDP
ln -sf $INSTALLATION_DIR/VBox.sh /usr/bin/VBoxHeadless
ln -sf $INSTALLATION_DIR/VBox.sh /usr/bin/VBoxBalloonCtrl
ln -sf $INSTALLATION_DIR/VBox.sh /usr/bin/VBoxAutostart
ln -sf $INSTALLATION_DIR/VBox.sh /usr/bin/vboxwebsrv
ln -sf $INSTALLATION_DIR/VBox.png /usr/share/pixmaps/VBox.png
# Unity and Nautilus seem to look here for their icons
ln -sf $INSTALLATION_DIR/icons/128x128/virtualbox.png /usr/share/pixmaps/virtualbox.png
ln -sf $INSTALLATION_DIR/virtualbox.desktop /usr/share/applications/virtualbox.desktop
ln -sf $INSTALLATION_DIR/virtualbox.xml /usr/share/mime/packages/virtualbox.xml
ln -sf $INSTALLATION_DIR/rdesktop-vrdp /usr/bin/rdesktop-vrdp
ln -sf $INSTALLATION_DIR/src/vboxhost /usr/src/vboxhost-4.3.20

# Convenience symlinks. The creation fails if the FS is not case sensitive
ln -sf VirtualBox /usr/bin/virtualbox > /dev/null 2>&1
ln -sf VBoxManage /usr/bin/vboxmanage > /dev/null 2>&1
ln -sf VBoxSDL /usr/bin/vboxsdl > /dev/null 2>&1
ln -sf VBoxHeadless /usr/bin/vboxheadless > /dev/null 2>&1

# Icons
cur=`pwd`
cd $INSTALLATION_DIR/icons
for i in *; do
	cd $i
	if [ -d /usr/share/icons/hicolor/$i ]; then
		for j in *; do
			if expr "$j" : "virtualbox\..*" > /dev/null; then
				dst=apps
			else
				dst=mimetypes
			fi
			if [ -d /usr/share/icons/hicolor/$i/$dst ]; then
				ln -s $INSTALLATION_DIR/icons/$i/$j /usr/share/icons/hicolor/$i/$dst/$j
			fi
		done
	fi
	cd -
done
cd $cur

cp -f $SCRIPT_DIRECTORY/rules.d/60-vboxdrv.rules /etc/udev/rules.d/ &&

mkdir -p -m 755 /etc/vbox &&
cp $SCRIPT_DIRECTORY/vbox.cfg /etc/vbox &&

mkdir -p -m 755 /etc/init.d &&
cp -af vboxdrv.sh /etc/init.d/vboxdrv &&
cp -af vboxballoonctrl-service.sh /etc/init.d/vboxballoonctrl-service &&
cp -af vboxautostart-service.sh /etc/init.d/vboxautostart-service &&
cp -af vboxweb-service.sh /etc/init.d/vboxweb-service
