FGLRX_DIRECTORY=$SOURCE_DIRECTORY/working &&

#dry run
./ati-installer.sh $INNER_VERSION --install &&

# We build the kernel BEFORE actually calling prepare install
# so it doesn't remove a working driver incase the kernel module
# fails to compile  

KVER=`uname -r` &&

cd install/lib/modules/fglrx/build_mod/ &&
sh make.sh &&
cd 2.6.x && make clean &&

cd $BUILD_DIRECTORY/$FGLRX_DIRECTORY &&

prepare_install &&

install -m0644 -D -t /usr/share/doc/ati install/usr/share/doc/ati/LICENSE.TXT &&
install -m0644 -D -t /usr/share/doc/ati/user-manual install/usr/share/doc/ati/user-manual/AMD_Linux_Driver_Specification.pdf &&
install -m0644 -D -t /usr/share/doc/ati/user-manual install/usr/share/doc/ati/user-manual/index.html &&
install -m0755 -D -t /usr/share/doc/ati/examples/etc/init.d install/usr/share/doc/ati/examples/etc/init.d/atieventsd.sh &&
install -m0644 -D -t /usr/share/doc/ati/examples/etc/acpi/events install/usr/share/doc/ati/examples/etc/acpi/events/a-lid-aticonfig &&
install -m0644 -D -t /usr/share/doc/ati/examples/etc/acpi/events install/usr/share/doc/ati/examples/etc/acpi/events/a-ac-aticonfig &&
install -m0755 -D -t /usr/share/doc/ati/examples/etc/acpi install/usr/share/doc/ati/examples/etc/acpi/ati-powermode.sh &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/1gbhang.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4461.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4462.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4463.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4464.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4469.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4470.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4475.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4478.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4479.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4480.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4481.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4482.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4483.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4484.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/4485.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/corruptstereo.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/corruptvtswitch.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/devshm.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/dga3dhang.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/doom3corrupt.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/dualheadvideo.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/laptopsuspend.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/missingdrmheaders.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/mousecursorhang.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/no3d-aiw8500dv.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/no3d-kt400.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/nomembercount.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/pcie3dmemoryleak.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/r420blankdisplay.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/rv280dviblankdisplay.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/rv350springdale.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/secondheadcorruption.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/xf86_enodev.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/xrestartpcie.html &&
install -m0644 -D -t /usr/share/doc/ati/articles install/usr/share/doc/ati/articles/xvsatshift.html &&
install -m0644 -D -t /usr/share/doc/ati install/usr/share/doc/ati/configure.html &&
install -m0644 -D -t /usr/share/doc/ati install/usr/share/doc/ati/driverfaq.html &&
install -m0644 -D -t /usr/share/doc/ati install/usr/share/doc/ati/index.html &&
install -m0644 -D -t /usr/share/doc/ati install/usr/share/doc/ati/installer.html &&
install -m0644 -D -t /usr/share/doc/ati install/usr/share/doc/ati/issues.html &&
install -m0644 -D -t /usr/share/doc/ati install/usr/share/doc/ati/linuxfaq.html &&
install -m0644 -D -t /usr/share/doc/ati install/usr/share/doc/ati/tips-linux.html &&
install -m0644 -D -t /usr/share/man/man8 install/usr/share/man/man8/atieventsd.8 &&
install -m0644 -D -t /usr/lib/xorg/modules/linux install/usr/lib/xorg/modules/linux/libfglrxdrm.so &&
install -m0644 -D -t /usr/lib/xorg/modules/drivers install/usr/lib/xorg/modules/drivers/fglrx_drv.so &&
install -m0644 -D -t /usr/lib/xorg/modules install/usr/lib/xorg/modules/glesx.so &&
install -m0644 -D -t /usr/lib/xorg/modules install/usr/lib/xorg/modules/amdxmm.so &&
install -m0755 -D -t /usr/lib/fglrx install/usr/lib/fglrx/switchlibGL &&
install -m0755 -D -t /usr/lib/fglrx install/usr/lib/fglrx/switchlibglx &&
install -m0644 -D -t /usr/lib/xorg/modules/extensions/fglrx install/usr/lib/xorg/modules/extensions/fglrx/fglrx-libglx.so &&
install -m0644 -D -t /usr/lib install/usr/lib/libamdhsasc32.so &&
install -m0644 -D -t /usr/lib install/usr/lib/libamdocl32.so &&
install -m0644 -D -t /usr/lib install/usr/lib/libAMDXvBA.cap &&
install -m0644 -D -t /usr/lib install/usr/lib/libAMDXvBA.so.1.0 &&
install -m0644 -D -t /usr/lib install/usr/lib/libatiadlxx.so &&
install -m0644 -D -t /usr/lib install/usr/lib/libaticalcl.so &&
install -m0644 -D -t /usr/lib install/usr/lib/libaticaldd.so &&
install -m0644 -D -t /usr/lib install/usr/lib/libaticalrt.so &&
install -m0644 -D -t /usr/lib install/usr/lib/libatiuki.so.1.0 &&
install -m0644 -D -t /usr/lib install/usr/lib/libfglrx_dm.a &&
install -m0644 -D -t /usr/lib install/usr/lib/libfglrx_dm.so.1.0 &&
install -m0644 -D -t /usr/lib install/usr/lib/libOpenCL.so.1 &&
install -m0644 -D -t /usr/lib install/usr/lib/libXvBAW.so.1.0 &&
install -m0644 -D -t /usr/lib/fglrx install/usr/lib/fglrx/fglrx-libGL.so.1.2 &&
install -m0644 -D -t /usr/lib/dri install/usr/lib/dri/fglrx_dri.so &&
install -m0644 -D -t /usr/include/GL install/usr/include/GL/glATI.h &&
install -m0644 -D -t /usr/include/GL install/usr/include/GL/glxATI.h &&
install -m0644 -D -t /usr/include/ATI/GL install/usr/include/ATI/GL/glxext.h &&
install -m0644 -D -t /usr/include/ATI/GL install/usr/include/ATI/GL/glx.h &&
install -m0755 -D -t /usr/bin install/usr/bin/fgl_glxgears &&
install -m0755 -D -t /usr/bin install/usr/bin/fglrxinfo &&
install -m0755 -D -t /usr/bin install/usr/bin/aticonfig &&
install -m0755 -D -t /usr/bin install/usr/bin/atiodcli &&
install -m0755 -D -t /usr/bin install/usr/bin/atiode &&
install -m0755 -D -t /usr/bin install/usr/bin/amd-console-helper &&
install -m0755 -D -t /usr/bin install/usr/bin/clinfo &&
install -m0644 -D -t /usr/src/ati install/usr/src/ati/fglrx_sample_source.tgz &&
install -m0755 -D -t /usr/sbin install/usr/sbin/amdnotifyui &&
install -m0755 -D -t /usr/sbin install/usr/sbin/atieventsd &&
install -m0755 -D -t /usr/sbin install/usr/sbin/atigetsysteminfo.sh &&
install -m0644 -D -t /etc/ati install/etc/ati/amdpcsdb.default &&
install -m0644 -D -t /etc/ati install/etc/ati/atiapfxx &&
install -m0644 -D -t /etc/ati install/etc/ati/atiapfxx.blb &&
install -m0644 -D -t /etc/ati install/etc/ati/atiapfxx.log &&
install -m0755 -D -t /etc/ati install/etc/ati/authatieventsd.sh &&
install -m0644 -D -t /etc/ati install/etc/ati/control &&
install -m0644 -D -t /etc/ati install/etc/ati/logo_mask.xbm.example &&
install -m0644 -D -t /etc/ati install/etc/ati/logo.xbm.example &&
install -m0644 -D -t /etc/ati install/etc/ati/signature &&
install -m0644 -D -t /etc/OpenCL/vendors install/etc/OpenCL/vendors/amdocl32.icd &&
install -m0755 -D -t /usr/bin install/usr/bin/amdconfig &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/libfglrx_ip.a &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_acpi.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_debug.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_ioctl.c &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_ioctl.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_wait.c &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_agp.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_str.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_config.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/drmP.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/fglrxko_pci_ids.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/firegl_public.c &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl.c &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_wait.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_io.c &&
install -m0644 -D -t /lib/modules/fglrx/build_mod/2.6.x install/lib/modules/fglrx/build_mod/2.6.x/Makefile &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/firegl_public.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_iommu.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/drm_compat.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/drm_proc.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/drm_os_linux.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_debug.c &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/drm.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_pci.c &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_pci.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_type.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_iommu.c &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_agp.c &&
install -m0755 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/make.sh &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_io.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_str.c &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_osconfig.h &&
install -m0644 -D -t /lib/modules/fglrx/build_mod install/lib/modules/fglrx/build_mod/kcl_acpi.c &&
install -m0755 -D -t /lib/modules/fglrx install/lib/modules/fglrx/make_install.sh &&
install -m0644 -D -t /etc/modprobe.d install/etc/modprobe.d/blacklist-fglrx.conf &&
install -m0644 -D -t /usr/share/applications install/usr/share/applications/amdcccle.desktop &&
install -m0644 -D -t /usr/share/applications install/usr/share/applications/amdccclesu.desktop &&
install -m0644 -D -t /usr/share/icons install/usr/share/icons/ccc_large.xpm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_cs.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_da_DK.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_de.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_el_GR.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_es_ES.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_fi_FI.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_fr_FR.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_hu_HU.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_it_IT.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_ja.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_ko_KR.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_nl_NL.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_no.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_pl.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_pt_BR.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_ru_RU.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_sv_SE.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_th.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_tr_TR.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_zh_CN.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/amdcccle_zh_TW.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_cs.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_da.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_de.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_es.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_fr.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_hu.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_ja_JP.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_ja.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_ko.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_pl.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_pt.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_ru.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_sv.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_zh_CN.qm &&
install -m0644 -D -t /usr/share/ati/amdcccle install/usr/share/ati/amdcccle/qt_zh_TW.qm &&
install -m0755 -D -t /usr/bin install/usr/bin/amdcccle &&
install -m0755 -D -t /usr/bin install/usr/bin/amdxdg-su &&
install -m0755 -D -t /usr/bin install/usr/bin/amdupdaterandrconfig &&
install -m0644 -D -t /usr/share/doc/ati install/usr/share/doc/ati/ccc_copyrights.txt &&
install -m0644 -D -t /etc/security/console.apps install/etc/security/console.apps/amdcccle-su &&
install -m0644 -D -t /usr/share/ati/lib install/usr/share/ati/lib/libQtCore.so.4 &&
install -m0644 -D -t /usr/share/ati/lib install/usr/share/ati/lib/libQtGui.so.4 &&

touch /etc/ati/atiapfuser.blb &&
chmod a+w /etc/ati/atiapfuser.blb &&
chmod a+s /usr/bin/amd-console-helper

ln -sf /usr/lib/fglrx/fglrx-libGL.so.1.2 /usr/lib/libGL.so.1.2 &&
ln -sf /usr/lib/libGL.so.1.2 /usr/lib/libGL.so.1 &&
ln -sf /usr/lib/libGL.so.1 /usr/lib/libGL.so &&
ln -sf /usr/lib/xorg/modules/extensions/fglrx/fglrx-libglx.so /usr/lib/xorg/modules/extensions/libglx.so &&
ln -sf /usr/lib/libXvBAW.so.1.0 /usr/lib/dri/fglrx_drv_video.so &&

ln -sf /etc/pam.d/su /etc/pam.d/amdcccle-su &&

mkdir -p /lib/modules/${KVER}/kernel/drivers/char/drm &&
cp -af install/lib/modules/fglrx/fglrx.$KVER.ko \
	/lib/modules/${KVER}/kernel/drivers/char/drm/fglrx.ko

