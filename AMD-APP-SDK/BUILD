ARCH_FULL=`uname -m`

prepare_install &&

if ! module_installed fglrx; then
	echo "No fglrx installed, copy runtime files..."
	VENDORS_DIR="/etc/OpenCL/vendors"

	mkdir -p $VENDORS_DIR &&
	echo "libamdocl$ARCH_M.so" > "$VENDORS_DIR/amdocl$ARCH_M.icd" &&

	install -m755 "bin/$ARCH_FULL/clinfo" /usr/bin/ &&
	install -m644 "lib/$ARCH_FULL/libamdocl12$ARCH_M.so" /usr/lib/ &&

	install -m644 "lib/$ARCH_FULL/libamdocl$ARCH_M.so" /usr/lib/ &&
	install -m644 "lib/$ARCH_FULL/libOpenCL.so.1" /usr/lib/
fi

ln -rs /usr/lib/libOpenCL.so.1 /usr/lib/libOpenCL.so
cp -af "lib/$ARCH_FULL/libhsail.a" /usr/lib

if [ ! -e "/usr/lib/libGLEW.so" ]; then
	install -m644 "lib/$ARCH_FULL/libGLEW.so" /usr/lib/
fi

if [ ! -e "/usr/lib/libglut.so" ]; then
	install -m644 "lib/$ARCH_FULL/libglut.so" /usr/lib/
fi

cp -rf include/{CL,SDKUtil} /usr/include/

if [ ! -e "/usr/include/GL/" ]; then
	cp -rf include/GL /usr/include/
fi
