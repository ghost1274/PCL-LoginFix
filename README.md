# PCL 正版登录修复版

这是第三方基于 PCL 独立修改的版本，版本号为 2.99.0.0。
原作者：龙腾猫跃。原作者赞助链接：https://meloong.com/afd/a/LTCat 。保留原始 LICENCE。

修复 Microsoft 网页授权后启动器没有显示正版账号的问题：独立轮询线程错误地触发了取消判断，使登录流程在 5% 提前结束。本版保存并传递原始登录线程，在两处取消检查中正确区分正常轮询、用户取消和登录重启。

## 下载与使用

请到 [Releases](https://github.com/ghost1274/PCL-LoginFix/releases/latest) 下载 `PCL-LoginFix-2.99.0.0-AccountDisplayFix.zip`。它包含已编译的 Windows 主程序、配置文件、完整源码、许可证和验证记录。

1. 完整解压 ZIP。
2. 在 Windows 上运行 `PCL-LoginFix.exe`，需要 .NET Framework 4.8。
3. 点击“正版登录”中的“登录”，完成 Microsoft 网页授权，再返回启动器等待 Minecraft 账号验证完成。

GitHub 自动生成的 Source code 压缩包不是可运行发行包；请下载上述命名 ZIP。完整项目源码位于发行包的 `source` 目录，编译说明及差异补丁也在包内。

## 验证

完整 WPF/VB/C# 编译和实际 EXE 检查通过，12 项登录线程回归检查通过；旧判断可复现提前取消。发行包保留正版持有和玩家档案检查，未绕过账号授权。

尚未使用真实用户账号完成在线授权全链路测试。微软网页授权完成后，仍需要 Xbox 和 Minecraft 服务验证成功，才能显示账号。
