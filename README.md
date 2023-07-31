# Rootless-deb-tool
A cross-platform `Jailbreak` deb packaging tool includes `Fugu15` `rootless` deb，for linux_aarch64、linux_x86_64、macosx_x86_64、macosx_arm64.

## Usage
### You just need to put your demo.dylib in the same folder as pack_cross_deb.sh

<img src="https://github.com/MustangYM/Rootless-deb-tool/assets/21478687/24250cb1-f913-4378-ae2a-2d9b613db370" width="300px"/>

### Config
Config your deb in pack_cross_deb.sh
```
DEB_NAME="YourDebName"
DEB_VERSION="1.0.0"
DEB_AUTHOR="MustangYM"
DEB_DES="Be a hero"
DEB_ARCHITECTURE="iphoneos-arm"
TARGET_PROCESS="YourProcessName" 
TARGET_BUNDLE=("YourProcessId")
```

### permission
```
chmod +x pack_cross_deb.sh
```

### Fire
Will automatically iterate through dylib in the current directory and then determine your platform to call the matching ldid to sign.
```
./pack_cross_deb.sh
```
### Success
```
mustangym@MustangYMdeMacBook-Pro Rootless-deb-tool % /Users/mustangym/Rootless-deb-tool/pack_cross_deb.sh

  A cross-platform deb packaging tool includes rootless deb
#     #                                          #     # #     #
##   ## #    #  ####  #####   ##   #    #  ####   #   #  ##   ##
# # # # #    # #        #    #  #  ##   # #    #   # #   # # # #
#  #  # #    #  ####    #   #    # # #  # #         #    #  #  #
#     # #    #      #   #   ###### #  # # #  ###    #    #     #
#     # #    # #    #   #   #    # #   ## #    #    #    #     #
#     #  ####   ####    #   #    # #    #  ####     #    #     #

Processing libPineappleDylib.dylib
dpkg-deb: 正在 'ThemePro_1.1.9_iphoneos-arm.deb' 中构建软件包 'themepro'。
🍻: Change permissions for ldid_macosx_arm64
🍻: Change permissions for /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.UlbSrt0T/DEBIAN/*
🍻: Change permissions for /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.UlbSrt0T/DEBIAN/control
🍻: Replace iphoneos-arm with iphoneos-arm64
/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/install_name_tool: warning: changes being made to the file will invalidate the code signature in: /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.Dt0gaxSY/var/jb/usr/lib/TweakInject/libPineappleDylib.dylib
/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/install_name_tool: warning: changes being made to the file will invalidate the code signature in: /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.Dt0gaxSY/var/jb/usr/lib/TweakInject/libPineappleDylib.dylib
/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/install_name_tool: warning: changes being made to the file will invalidate the code signature in: /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.Dt0gaxSY/var/jb/usr/lib/TweakInject/libPineappleDylib.dylib
/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/install_name_tool: warning: changes being made to the file will invalidate the code signature in: /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.Dt0gaxSY/var/jb/usr/lib/TweakInject/libPineappleDylib.dylib
/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/install_name_tool: warning: changes being made to the file will invalidate the code signature in: /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.Dt0gaxSY/var/jb/usr/lib/TweakInject/libPineappleDylib.dylib
/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/install_name_tool: warning: changes being made to the file will invalidate the code signature in: /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.Dt0gaxSY/var/jb/usr/lib/TweakInject/libPineappleDylib.dylib
/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/install_name_tool: warning: changes being made to the file will invalidate the code signature in: /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.Dt0gaxSY/var/jb/usr/lib/TweakInject/libPineappleDylib.dylib
/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/install_name_tool: warning: changes being made to the file will invalidate the code signature in: /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.Dt0gaxSY/var/jb/usr/lib/TweakInject/libPineappleDylib.dylib
🍻: Sign /var/folders/2b/y1cj1s594q74p_qf_8n0v9hw0000gn/T/tmp.Dt0gaxSY/var/jb/usr/lib/TweakInject/libPineappleDylib.dylib with ldid
dpkg-deb: 正在 '/Users/mustangym/Rootless-deb-tool/ThemePro_1.1.9_iphoneos-arm64_rootless.deb' 中构建软件包 'themepro'。
🍻: 🍻🍻🍻🍻🍻🍻Success🍻🍻🍻🍻🍻🍻
```
### Product
<img src="https://github.com/MustangYM/Rootless-deb-tool/assets/21478687/30c835c4-d269-47cd-86aa-dd3255d2cc18" width="600px"/>

### Base on
[v2.1.5-procursus7](https://github.com/ProcursusTeam/ldid/releases/tag/v2.1.5-procursus7)
