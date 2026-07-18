#
# Copyright (C) 2016 MediaTek Inc.
#
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 2 as
# published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
# See http://www.gnu.org/licenses/gpl-2.0.html for more details.


# Mediatek external kernel modules

> [!NOTE]
> Imported from `xiaomi camellian-t-oss`
>
> Supported platform: `MT6833` & `MT6853`

> [!WARNING]
> This driver is intended only for 4.14.x. Not for 4.9.x and below or 4.19.x and above.

# Mediatek required configurations
**Make sure to enable this in your kernel defconfig!**
```
CONFIG_MTK_COMBO_BT=y
CONFIG_MTK_COMBO_WIFI=y
CONFIG_MTK_COMBO_GPS=y
CONFIG_MTK_GPS_SUPPORT=y
CONFIG_MTK_FMRADIO=y
```

# Build configurations
```
CONFIG_DRV_BUILD_IN=y
```
# Bootloop issue
Bootloops can be caused by the drivers in `/vendor/lib/modules/*.ko` conflicting with drivers inline. Removing `/vendor/lib/modules/` can solve it.
