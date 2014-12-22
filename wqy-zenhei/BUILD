WQY=/usr/share/fonts/wenquanyi &&

prepare_install &&

if [ ! -d $WQY ] ; then
  mkdir -p $WQY
fi &&

cp -f *.ttc $WQY &&
cp zenheiset /usr/bin &&
chmod 775 /usr/bin/zenheiset &&

mkdir -p /usr/doc/$MODULE &&
cp -a AUTHORS COPYING ChangeLog INSTALL README /usr/doc/$MODULE &&

cp *.conf /etc/fonts/conf.avail/ &&
cd /etc/fonts/conf.d &&
ln -sf ../conf.avail/44-wqy-zenhei.conf &&

cd $WQY &&
mkfontscale &&
mkfontdir
