       Microsoft Windows XP Service Pack 2 (SP2)，RTM
                         Deploy.cab 
                          自述文档
                     2004 年 6 月 25 日

本文档中的信息（包括引用的 URL 和其他 Internet 网站）仅供参考，如有变动，
恕不另行通知。因使用本文档而造成的所有风险及后果由用户承担，
Microsoft Corporation 不作任何明示或暗示的担保。除非另行说明，本文档示例
中涉及的公司、组织、产品、人物和事件均属虚构，与任何真实的公司、组织、产
品、人物和事件无关，如有雷同，纯属巧合。遵守所有适用的版权法是用户的责任。
在不限制版权许可权利的前提下，未经 Microsoft Corporation 明确书面许可，
本文档的任何部分均不得复制、存储或引进检索系统，或者以任何形式、任何方式
（电子、机械、复印、录音或其他）或为任何目的进行传播。
  
本文档可能涉及 Microsoft 的专利、专利申请、商标、版权或其他知识产权。除非
得到 Microsoft 的明确书面许可协议，否则，本文档不授予使用这些专利、商标、
版权或其他知识产权的任何许可。

(c) 2004 Microsoft Corporation。保留所有权利。

Microsoft、MS-DOS、Windows 和 Windows NT 是 Microsoft Corporation 在美国
和/或其他国家（地区）的注册商标或商标。

本文档所提及的真实公司和产品的名称可能是其各自所有者的商标。

==============
如何使用本文档
==============

要在 Microsoft Windows 记事本中查看此自述文件，请最大化记事本窗口，并在
“格式”菜单上，单击“自动换行”。

要打印此自述文件，请在记事本或其他字处理器中打开该文件，然后使用“文件”
菜单上的“打印”命令。

====
目录
====

1. 简介

2. Windows PE 的可用性

3. 从以前版本的工具升级

4. 升级现有配置集

5. 已知问题

-------
 
1. 简介
-------

本文档提供有关适用于 Microsoft Windows XP Service Pack 2 (SP2) 和
Windows Server 2003 家族的 Deploy.cab 文件所含工具的最新信息。

注意：Deploy.cab 中包含的安装管理器工具 (Setupmgr.exe) 仅供企业管理员使
      用。对于系统制造商来说，应安装 OEM 预安装工具包 (OPK) 光盘中的工具
      和文档。OPK 光盘包含在 OEM 分销商按照 Microsoft OEM 系统制造商许可
      协议分发给如下人员的每个 Windows 软件包中：原始计算机制造商、组装
      者、重新组装者和/或计算机硬件的软件预安装人员。

安装管理器不再包含上下文相关帮助。有关安装管理器的各页的详细信息，请参阅
“Microsoft Windows 企业部署工具用户指南”(Deploy.chm) 中的“安装管理器
设置”主题。

----------------------

2. Windows PE 的可用性
----------------------

Windows 预安装环境 (Windows PE) 授权给原始设备制造商 (OEM)，供他们在新的
计算机上预安装 Windows 时使用。Windows PE 针对企业用户提供。有关详细信息，
请与您的帐户管理员联系。

-----------------------

3. 从以前版本的工具升级
-----------------------

可以使用 Windows XP SP2 OPK 预安装下列 Windows 版本：

    * Windows XP 金版发布
    * Windows XP SP1 和 Windows XP SP2
    * Windows Server 2003 家族

要预安装基于 Windows Server 2003 Itanium 的客户端，请使用基于
Windows Server 2003 SP1 Itanium 的工具。

不要使用 Windows XP 金版发布企业部署工具来预安装 Windows Server 2003 家族。

如果以前安装了 Windows XP 金版发布企业部署工具或 Windows XP SP1 企业部署
工具，则必须将这些工具升级到 Windows XP SP2 企业部署。Windows XP 金版发
布企业部署工具或 Windows XP SP1 企业部署工具不能与 Windows XP SP2 企业部
署工具共存于技术人员计算机中。

不要将 Windows Server 2003 企业部署工具的安装升级到
Windows Server 2003 SP1 试用版。

如果使用 Windows XP 金版发布企业部署工具或 Windows XP SP1 企业部署工具设
置分布共享，将启用来宾帐户。

如果使用 Windows XP SP2 企业部署工具设置新的分布共享，则不会自动启用来宾
帐户。此外，将 Windows XP 企业部署工具升级到 Windows XP SP2 不会改变现有
分布共享的属性。

-----------------

4. 升级现有配置集
-----------------

升级到 Windows XP SP2 企业部署工具不会改变位于 \Cfgsets 文件夹中的任何现
有配置集，也不会改变位于 \Lang 文件夹中的任何可用的 Windows 产品文件。

必须使用安装管理器中的“产品”页来加载 Windows 更新版本（如
Windows XP SP2 或 Windows Server 2003 家族成员）的 Windows 产品文件。

升级到 Windows XP SP2 企业部署工具将更新安装管理器在创建新的配置集时使用
的模板文件。用 Windows XP SP2 安装管理器新建的所有配置集都将使用从这些新
模板文件中获取的默认值。

* 迁移 Windows XP 或 Windows XP SP1 的配置集，以便预安装 Windows XP SP2

1. 在安装管理器中打开配置集。

2. 在“产品”页，选择新产品“Windows XP SP2”。

3. 保存此配置集。

-----------

5. 已知问题
-----------

* Unattend.txt 和 Sysprep.inf 的 [RegionalSettings] 节中的 InputLocale
项仅能用于指定最多 7 种输入法区域设置和键盘布局组合。

解决方法：

请参阅知识库文章 325856，获得有关如何在完成最小化安装后指定区域设置的信息。

* 如果通过在 Unattend.txt 中设置 AutomaticUpdates = On 或使用“欢迎使用
Windows”中的“帮助保护您的计算机”页打开“自动更新”，然后运行
Sysprep -reseal，自动更新将始终保持打开状态。

* 如果在运行 Windows Server 2003 的计算机上安装企业部署工具，可能需要在
创建分布共享时完成一个额外的步骤。在运行 Windows Server 2003 的计算机上，
共享文件夹会将 Everyone 组的默认权限设置为只读。如果要允许 Everyone 通过
网络向此分布共享执行写操作，必须添加额外的权限。

解决方法：为需要向分布共享执行远程写入操作的用户添加读取-写入权限。

* 如果在工厂模式下运行 Sysprep (Sysprep -factory) 的过程中预安装多语言用
户界面 (MUI) 程序包，并重新启动计算机进入最小化安装，则最小化安装的所有
页面均会被截断。

解决方法：将默认的 MUI 用户界面设置为英语。

* 无法在工厂模式下运行 Sysprey 时手动更改 Windows 安装。

解决方法：在运行 Sysprep -factory 时使用 Winbom.ini 来修改 Windows 安装。

- 或者 -

如果需要手动修改 Windows 安装，请使用 Sysprep -audit 命令。

* 如果将企业部署工具安装到本地化目录中，而将用户区域设置更改为另一种语言，
则无法打开企业部署帮助文件。

解决方法：更改用户区域设置，使之与本地化目录的语言相匹配。

* 可以使用 Sysprep 来安装测试证书，以便在操作系统映像上对那些经过 Windows
硬件质量实验室 (WHQL) 测试签名的驱动程序启用测试，即使已对映像运行了
Sysprep，也可以执行此操作。有关详细信息，请参阅 KB321559。

* 不能在 I386 目录内运行 Update.exe 将 Windows XP 安装升级到
Windows XP SP2。必须对 Windows 光盘的所有内容运行 Update.exe。如果
Windows 光盘的所有内容未出现在安装共享中，Update.exe 将不能完成安装过程。

* 不能对已使用 Update.exe 升级到 Windows XP SP2 的 Windows XP SP1 安装运
行 Sysprep.exe。只能对集成（“整合”）的 Windows 安装运行 Sysprep。

* 正确更新 Windows XP I386 目录

1. 下载 Windows XP Service Pack 2。

2. 在命令提示符下，转到存放已下载的 XPSP2.exe 文件的文件夹，然后键入以下
   命令：

   xpsp2.exe -x

3. 出现提示信息时，键入要从中展开此 Service Pack 的路径。例如，请键入：

   C:\XPSP2

4. 在系统中创建一个临时目录，然后将 Windows XP 产品光盘中的所有内容复制到
   该目录中。例如，请键入：

   MD C:\INTSP2 XCopy CDROM Drive Letter:\*.* C:\INTSP2 /e

5. 在执行完上一步骤后，转到包含 Windows XP SP2 文件的目录。例如，请键入：

   CD C:\xpsp2\update

6. 要更新 Windows XP 文件以便包含 SP2，请键入：

   update.exe -s c:\INTSP2

上述过程结束后，I386 目录会更新为 Windows XP SP2。

* 在 OEM 预安装参考 (Ref.chm) 中，Unattend.txt 应答文件中
[TerminalServices] 节的 AllowConnections 项的功能已改变。如果指定：

[TerminalServices]
AllowConnections = 1

在无人参与安装过程中将启用远程桌面。但是，远程桌面不会添加到 Windows
防火墙例外列表中。Unattend.txt 应答文件中至少应具备以下项，才能在无
人参与安装过程中启用远程桌面，并将其添加到 Windows 防火墙例外列表中：

[WindowsFirewall]
Profiles = Standard（指定一个用户定义的配置文件名）

[WindowsFirewall.Standard]
Services = RemoteDesktop（指定一个用户定义的服务名）

[WindowsFirewall.RemoteDesktop]
Type = 2

[TerminalServices]
AllowConnections = 1

有关 Windows 防火墙设置的详细信息，请参阅 OEM 预安装参考 (Ref.chm) 的
Unattend.txt 一章的 [WindowsFirewall] 各节和项。
