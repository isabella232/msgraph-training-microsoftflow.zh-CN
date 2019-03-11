<!-- markdownlint-disable MD002 MD041 -->

在本练习中, 将创建一个新的 Azure Active Directory 应用程序, 该应用程序将用于为自定义连接器提供委派权限。

打开浏览器并导航到[Azure Active Directory 管理中心](https://aad.portal.azure.com)。 在左侧导航菜单中选择 " **Azure Active Directory** " 链接, 然后在**Azure active directory**边栏的 "**管理**" 部分中选择 "**应用注册**" 条目。

![azure active directory 中的 azure active directory 刀片的屏幕截图管理中心](./images/app-reg1.png)

选择 "**应用**注册" 边栏选项卡顶部的 "**新建应用程序注册**" 菜单项。

![Azure Active Directory 管理中心中的应用程序注册刀片的屏幕截图](./images/app-reg2.png)

在`MS Graph Batch App` "**名称**" 字段中输入`https://localhost.com/$batch` , 并在 "**登录 URL** " 字段中输入, 然后选择 "**创建**"。

![Azure Active Directory 管理中心中的新应用注册的创建表单的屏幕截图](./images/app-reg3.png)

在 " **MS Graph 批处理应用**程序" 页上, 复制应用程序的**应用程序 ID** 。 在下一个练习中, 你将需要此操作。

![已注册的应用程序页的屏幕截图](./images/app-reg4.png)

在 "应用程序名称" 下选择 "**设置**" 齿轮, 然后选择 "设置" 边栏选项卡中的 "**所需权限**" 菜单项。 选择 "**所需权限**" 边栏顶部的 "**添加**"。

![所需权限刀片的屏幕截图](./images/app-perms1.png)

在 "**添加 api 访问**" 边栏中选择 "**选择 api** " 选项, 然后选择 " **Microsoft Graph** " 项目, 然后在 "刀片式服务器" 底部选择 "**选择**"。

![选择 API 刀片的屏幕截图](./images/app-perms2.png)

在 "**启用访问**" 边栏中, 向下滚动到 "**委派权限**" 部分。 选择 "**读取和写入所有组**委派权限", 然后选择刀片式服务器底部的 "**选择**"。 在 "**添加 API 访问**" 边栏底部选择 "**完成**"。

 ![启用 Access 边栏的屏幕截图](./images/app-perms3.png)

选择 "**设置**" 边栏选项卡上的 "**密钥**" 菜单项。 在`forever` "**键说明**" 中输入, 然后从 "**持续时间**" 下拉菜单中选择 "**从不过期**"。 在 "**密钥**" 边栏顶部选择 "**保存**"。 复制新项的键值。 在下一个练习中, 你将需要此操作。

![键刀片的屏幕截图](./images/app-key1.png)

> [!IMPORTANT]
> 此步骤非常关键, 因为关闭此边栏后将无法访问密钥。 将此项保存到文本编辑器中, 以便在即将进行的练习中使用。

若要启用对通过 Microsoft Graph (包括团队属性) 访问的其他服务的管理, 需要选择其他更合适的范围以启用管理特定服务。 例如, 若要扩展我们的解决方案以启用创建 OneNote 笔记本或 Planner 计划、存储桶和任务, 需要为相关 api 添加所需的权限范围。