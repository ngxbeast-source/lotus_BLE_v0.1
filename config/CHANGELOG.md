# Figure out why the RGB wont work 
# ERRORs
# /tmp/zmk-config/zmk/app/src/rgb_underglow.c:33:2: error: #error "A zmk,underglow chosen node must be declared" #error "A zmk,underglow chosen node must be declared"
# 
# warning: ZMK_USB (defined at /tmp/zmk-config/zmk/app/Kconfig:121) was assigned the value 'y' but got
# the value 'n'. Check these unsatisfied dependencies: (!ZMK_SPLIT || (ZMK_SPLIT &&
# ZMK_SPLIT_ROLE_CENTRAL)) (=n).
# warning: ZMK_BACKLIGHT_AUTO_OFF_IDLE (defined at /tmp/zmk-config/zmk/app/Kconfig:357) was assigned
# the value 'y' but got the value 'n'. Check these unsatisfied dependencies: ZMK_BACKLIGHT (=n).
# FAILED: CMakeFiles/app.dir/src/rgb_underglow.c.obj 
# error: #error "A zmk,underglow chosen node must be declared"
# rror "A zmk,underglow chosen node must be declared"

# 19FEB 26
# Added lotus boards/shields folder
# Edited .dtsi to include rgb support on the hardware level?(This might've been the cause for error when uploading to github) used the code provided from the zmk documentation for rgb support(https://zmk.dev/docs/development/hardware-integration/lighting/underglow)
# Added     lotus58_position_map {       to the layout.dtsi file
# Removed   #include <dt-bindings/zmk/rgb.h> #include <dt-bindings/zmk/ext_power.h>  from .keymap file. It was unnecessary. instead added #include <dt-bindings/led/led.h> to the .dtsi

# 19FEB 26 
# Undid most changes:
# Removed the lotus and nice nano folders from the board/shield folder. I think it was causing an error w/ ZMK superceeding the other files and prioritizing that one first. Only kept necessary files. like .dtsi and .overlay
# Added            #include <dt-bindings/zmk/rgb.h> #include <dt-bindings/zmk/ext_power.h>      to the .dtsi


# Figure out why the RGB wont work 
# ERRORs
# /tmp/zmk-config/zmk/app/src/rgb_underglow.c:33:2: error: #error "A zmk,underglow chosen node must be declared" #error "A zmk,underglow chosen node must be declared"
# 
# warning: ZMK_USB (defined at /tmp/zmk-config/zmk/app/Kconfig:121) was assigned the value 'y' but got
# the value 'n'. Check these unsatisfied dependencies: (!ZMK_SPLIT || (ZMK_SPLIT &&
# ZMK_SPLIT_ROLE_CENTRAL)) (=n).
# warning: ZMK_BACKLIGHT_AUTO_OFF_IDLE (defined at /tmp/zmk-config/zmk/app/Kconfig:357) was assigned
# the value 'y' but got the value 'n'. Check these unsatisfied dependencies: ZMK_BACKLIGHT (=n).
# FAILED: CMakeFiles/app.dir/src/rgb_underglow.c.obj 
# error: #error "A zmk,underglow chosen node must be declared"
# rror "A zmk,underglow chosen node must be declared"

# 19FEB 26
# Added lotus boards/shields folder
# Edited .dtsi to include rgb support on the hardware level?(This might've been the cause for error when uploading to github) used the code provided from the zmk documentation for rgb support(https://zmk.dev/docs/development/hardware-integration/lighting/underglow)
# Added     lotus58_position_map {       to the layout.dtsi file
# Removed   #include <dt-bindings/zmk/rgb.h> #include <dt-bindings/zmk/ext_power.h>  from .keymap file. It was unnecessary. instead added #include <dt-bindings/led/led.h> to the .dtsi

# 19FEB 26 
# Undid most off today's changes:
# Removed the lotus and nice nano folders from the board/shield folder. I think it was causing an error w/ ZMK superceeding the other files and prioritizing that one first. Only kept necessary files. like .dtsi and .overlay
# Added            #include <dt-bindings/zmk/rgb.h> #include <dt-bindings/zmk/ext_power.h>      to the .dtsi

# commented the RGB codes, again, when I have a better meal I'll look over it again.
# ERRRO CODE:
# FAILED: CMakeFiles/app.dir/src/rgb_underglow.c.obj 
# ccache /opt/zephyr-sdk-0.16.9/arm-zephyr-eabi/bin/arm-zephyr-eabi-gcc -DKERNEL -DLV_CONF_INCLUDE_SIMPLE=1 -DLV_CONF_PATH=/tmp/zmk-config/zephyr/modules/lvgl/include/lv_conf.h -DNRF52840_XXAA -DPB_MAX_REQUIRED_FIELDS=64 -DPB_NO_ENCODE_SIZE_CHECK -DPB_NO_ERRMSG -DPB_WITHOUT_64BIT -DPICOLIBC_INTEGER_PRINTF_SCANF -D_FORTIFY_SOURCE=1 -D_POSIX_C_SOURCE=200809 -D__LINUX_ERRNO_EXTENSIONS__ -D__PROGRAM_START -D__ZEPHYR__=1 -I/tmp/zmk-config/zmk/app/include -I/tmp/tmp.a0cih6WJQ6 -I/tmp/zmk-config/zephyr/include -I/tmp/tmp.a0cih6WJQ6/zephyr/include/generated -I/tmp/zmk-config/zephyr/soc/arm/nordic_nrf/nrf52 -I/tmp/zmk-config/zephyr/soc/arm/nordic_nrf/common/. -I/tmp/zmk-config/zephyr/subsys/usb/device -I/tmp/zmk-config/zephyr/subsys/bluetooth/controller/ll_sw/nordic/hal/nrf5/nrfx_glue -I/tmp/zmk-config/zephyr/subsys/bluetooth -I/tmp/zmk-config/zephyr/subsys/settings/include -I/tmp/zmk-config/modules/lib/nanopb -I/tmp/zmk-config/modules/hal/cmsis/CMSIS/Core/Include -I/tmp/zmk-config/zephyr/modules/cmsis/. -I/tmp/zmk-config/modules/hal/nordic/nrfx -I/tmp/zmk-config/modules/hal/nordic/nrfx/drivers/include -I/tmp/zmk-config/modules/hal/nordic/nrfx/mdk -I/tmp/zmk-config/zephyr/modules/hal_nordic/nrfx/. -I/tmp/zmk-config/modules/lib/gui/lvgl/src -I/tmp/zmk-config/zephyr/modules/lvgl/include -I/tmp/zmk-config/modules/crypto/tinycrypt/lib/include -I/tmp/zmk-config/zmk/app/module/include -I/tmp/zmk-config/zmk/app/module/drivers/sensor/battery/. -I/tmp/zmk-config/zmk/app/module/drivers/sensor/ec11/. -fno-strict-aliasing -Os -imacros /tmp/tmp.a0cih6WJQ6/zephyr/include/generated/autoconf.h -fno-printf-return-value -fno-common -g -gdwarf-4 -fdiagnostics-color=always -mcpu=cortex-m4 -mthumb -mabi=aapcs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mfp16-format=ieee --sysroot=/opt/zephyr-sdk-0.16.9/arm-zephyr-eabi/arm-zephyr-eabi -imacros /tmp/zmk-config/zephyr/include/zephyr/toolchain/zephyr_stdint.h -Wall -Wformat -Wformat-security -Wno-format-zero-length -Wno-pointer-sign -Wpointer-arith -Wexpansion-to-defined -Wno-unused-but-set-variable -Werror=implicit-int -fno-pic -fno-pie -fno-asynchronous-unwind-tables -ftls-model=local-exec -fno-reorder-functions --param=min-pagesize=0 -fno-defer-pop -fmacro-prefix-map=/tmp/zmk-config/zmk/app=CMAKE_SOURCE_DIR -fmacro-prefix-map=/tmp/zmk-config/zephyr=ZEPHYR_BASE -fmacro-prefix-map=/tmp/zmk-config=WEST_TOPDIR -ffunction-sections -fdata-sections --specs=picolibc.specs -std=c99 -Wfatal-errors -MD -MT CMakeFiles/app.dir/src/rgb_underglow.c.obj -MF CMakeFiles/app.dir/src/rgb_underglow.c.obj.d -o CMakeFiles/app.dir/src/rgb_underglow.c.obj -c /tmp/zmk-config/zmk/app/src/rgb_underglow.c
# /tmp/zmk-config/zmk/app/src/rgb_underglow.c:33:2: error: #error "A zmk,underglow chosen node must be declared"
# #error "A zmk,underglow chosen node must be declared"
    |  ^~~~~
