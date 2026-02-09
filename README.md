## Treeland Automate

Usage: ./treeland-automate [test-name]

Automate testing for Treeland using ydotool.

Requirements:
- Run as root
- ydotool installed
- 1920x1080 screen resolution

Available environment variables:
- INPUT_DELAY: Delay between each input event, default to 0.3
- LOCK_DELAY: Delay after locking the screen, default to 1
- UNLOCK_DELAY: Delay after unlocking the screen, default to 4
- CHECK_LOG_DELAY: Delay before checking the log, default to 0.5
- USER1: Username of the first user (the second last user in the user list)
- PASSWORD1: Password of the first user
- USER2: Username of the second user (the last user in the user list)
- PASSWORD2: Password of the second user

Available tests:
- login: Test login, logout, lock, unlock and switch user
- open-terminal: Stress test, Open 20 terminals then kill them until Treeland crashes.

### Event Record Guide

The following is how to record desired mouse input event the developer herself, for referrence only.

1. Get a Mac
2. Install [UTM](https://mac.getutm.app/) and create a Linux virtual machine with Apple Virtualization backend. Edit the VM and _disable Retina_ inside the Device -> Display settings.
3. Install deepin & Treeland develop environment
4. Start the VM, adjust the size of the window of the virtual display to 1920x1080, or any resolution you want to test on.
5. Install [PixelSnap](https://pixelsnap.com/) (Subscribe from [SetApp](https://setapp.com/apps/358?utm_medium=vendor_program&utm_source=PixelSnap) is a good choice)
6. Start the Treeland, measure the screen with PixelSnap and get the coordinate you want

![Example measurement using PixelSnap](./pixelsnap.png)

### Acknowledgements

Thanks to [ydotool](https://github.com/ReimuNotMoe/ydotool), which
provides the critical infrastructure for the automation.

### License

[GNU AGPL v3](./LICENSE), same with [ydotool](https://github.com/ReimuNotMoe/ydotool/blob/master/LICENSE)

## Treeland 自动化测试

用法: ./treeland-automate [测试名称]

使用 ydotool 自动化测试 Treeland。

要求:
- 以 root 身份运行
- ydotool 已安装
- 屏幕分辨率为 1920x1080

可用环境变量:
- INPUT_DELAY: 每个输入事件之间的延迟，默认为 0.3
- LOCK_DELAY: 锁屏后的延迟，默认为 1
- UNLOCK_DELAY: 解锁后的延迟，默认为 4
- CHECK_LOG_DELAY: 检查日志前的延迟，默认为 0.5
- USER1: 第一个用户的用户名（用户列表中倒数第二个用户）
- PASSWORD1: 第一个用户的密码
- USER2: 第二个用户的用户名（用户列表中最后一个用户）
- PASSWORD2: 第二个用户的密码

可用测试:
- login: 测试登录、注销、锁屏、解锁和切换用户
- open-terminal: 压力测试，打开20个终端然后杀掉它们直到 Treeland 崩溃。

### 事件录入指南

以下是开发者本人录入鼠标输入事件的方法，仅供参考。

1. 准备一台 Mac
2. 安装 [UTM 虚拟机软件](https://mac.getutm.app/)并创建一个使用 Apple Virtualization 后端的 Linux 虚拟机。编辑虚拟机，在显示器设置中_禁用 Retina_
3. 安装 deepin 操作系统和 Treeland 开发环境
4. 启动虚拟机，将虚拟屏幕窗口的大小调整至 1920x1080 （或者其它你想录入的分辨率）
5. 安装 [PixelSnap](https://pixelsnap.com/zh) （通过 [SetApp](https://setapp.com/apps/358?utm_medium=vendor_program&utm_source=PixelSnap) 订阅是一个比较优惠的渠道）
6. 启动 Treeland ，使用 PixelSnap 测量并获取屏幕坐标信息

![PixelSnap 操作示例](./pixelsnap.png)

### 致谢

感谢 [ydotool](https://github.com/ReimuNotMoe/ydotool) 为自动化测试提供了至关重要的基础设施。

### 开源协议

[GNU AGPL v3](./LICENSE), 与 [ydotool](https://github.com/ReimuNotMoe/ydotool/blob/master/LICENSE) 相同。
