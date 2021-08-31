# Android SELinux Tools

## How to Use

- Run the binary
```shell
adb root
adb shell setenforce 0
adb push rockchip_selinux_tools /data/local/tmp/
adb shell
(in)shell$ /data/local/tmp/rockchip_selinux_tools
```
- Add the result to `genfs_contexts` in `get_build_var BOARD_SEPOLICY_DIRS`

## Sample output
```log
/sys/devices/platform/fdd40000.i2c/i2c-0/0-0020/rk805-pwrkey/wakeup	u:object_r:sysfs_wakeup:s0
/sys/devices/platform/fdd40000.i2c/i2c-0/0-0020/rk808-rtc/wakeup	u:object_r:sysfs_wakeup:s0
...
/sys/devices/platform/fdd40000.i2c/i2c-0/0-0020/wakeup	u:object_r:sysfs_wakeup:s0
```
