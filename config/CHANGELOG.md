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
