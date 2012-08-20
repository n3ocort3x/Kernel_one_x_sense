--Please follow below command to download the official android toolchain: (arm-eabi-4.4.3)
        
                git clone https://android.googlesource.com/platform/prebuilt

                NOTE: the tool ¡¥git¡¦ will need to be installed first; for example, on Ubuntu, the installation command would be: apt-get install git

--Modify the .bashrc to add the toolchain path, like bellowing example:

								PATH=/usr/local/share/toolchain-eabi-4.4.3/bin:$PATH 

--Start 
$ make ARCH=arm CROSS_COMPILE=$TOP/prebuilt/linux-x86/toolchain/arm-eabi-4.4.3/bin/arm-eabi- endeavoru_android_defconfig -j8 
$ make ARCH=arm CROSS_COMPILE=$TOP/prebuilt/linux-x86/toolchain/arm-eabi-4.4.3/bin/arm-eabi- -j8 
# $TOP is an absolute path to android code


--Clean
								$make clean

--Files path
arch/arm/boot/zImage
drivers/*/*.ko																
