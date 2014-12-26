ARCH_FULL=`uname -m`

prepare_install &&

if ! module_installed fglrx; then
	VENDORS_DIR="/etc/OpenCL/vendors"

	mkdir -p $VENDORS_DIR &&
	echo "libamdocl$ARCH_M.so" > "$VENDORS_DIR/amdocl$ARCH_M.icd" &&

	install -m755 "bin/$ARCH_FULL/clinfo" /usr/bin/ &&
	install -m644 "lib/$ARCH_FULL/libamdocl$ARCH_M.so" /usr/lib/ &&
	install -m644 "lib/$ARCH_FULL/libOpenCL.so.1" /usr/lib/
fi

cp -af "lib/$ARCH_FULL/libOpenCL.so" /usr/lib &&
install -m644 "lib/$ARCH_FULL/libamdoclcl$ARCH_M.so" /usr/lib/ &&
install -m644 "lib/$ARCH_FULL/libaparapi_$ARCH_FULL.so" /usr/lib/ && 

cp -rf include/{CL,SDKUtil} /usr/include/
