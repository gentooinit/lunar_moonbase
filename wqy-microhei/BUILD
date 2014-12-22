WQY=/usr/share/fonts/wenquanyi &&

prepare_install &&

if [ ! -d $WQY ] ; then
  mkdir -p $WQY
fi &&

cp -f *.ttc $WQY &&

mkdir -p /usr/doc/$MODULE &&
cp -a AUTHORS.txt ChangeLog.txt INSTALL.txt README.txt LICENSE_Apache2.txt LICENSE_GPLv3.txt /usr/doc/$MODULE &&

cd $WQY &&
mkfontscale &&
mkfontdir
