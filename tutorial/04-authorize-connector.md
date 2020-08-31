<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="875d5-101">确保连接器可供使用的最后一个配置步骤是授权和测试自定义连接器以创建缓存的连接。</span><span class="sxs-lookup"><span data-stu-id="875d5-101">The final configuration step to ensure the connector is ready for use is to authorize and test the custom connector to create a cached connection.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="875d5-102">以下步骤要求您使用管理员权限登录。</span><span class="sxs-lookup"><span data-stu-id="875d5-102">The following steps requires that you are logged in with administrator privileges.</span></span>

<span data-ttu-id="875d5-103">在 [Microsoft 电力自动化](https://flow.microsoft.com)中，转到左侧的 " **数据** " 菜单项，然后选择 " **连接** " 页。</span><span class="sxs-lookup"><span data-stu-id="875d5-103">In [Microsoft Power Automate](https://flow.microsoft.com), go to the **Data** menu item on the left and choose the **Connections** page.</span></span> <span data-ttu-id="875d5-104">选择 " **新建连接** " 链接。</span><span class="sxs-lookup"><span data-stu-id="875d5-104">Choose the **New Connection** link.</span></span>

!["新建连接" 按钮的屏幕截图](./images/new-connection.png)

<span data-ttu-id="875d5-106">通过单击加号按钮找到您的自定义连接器并完成连接。</span><span class="sxs-lookup"><span data-stu-id="875d5-106">Find your custom connector and complete the connection by clicking the plus button.</span></span> <span data-ttu-id="875d5-107">使用 Office 365 租户管理员的 Azure Active Directory 帐户登录。</span><span class="sxs-lookup"><span data-stu-id="875d5-107">Sign in with your Office 365 tenant administrator's Azure Active Directory account.</span></span>

!["连接" 列表的屏幕截图](./images/connection-sign-in.png)

<span data-ttu-id="875d5-109">当系统提示您输入请求的权限时，请选中 " **代表您的组织同意"** ，然后选择 " **接受** " 以授权权限。</span><span class="sxs-lookup"><span data-stu-id="875d5-109">When prompted for the requested permissions, check **Consent on behalf of your organization** and then choose **Accept** to authorize permissions.</span></span>

![同意提示的屏幕截图](./images/consent-prompt.png)

<span data-ttu-id="875d5-111">授权权限后，会在 "自动使用电源" 中创建连接。</span><span class="sxs-lookup"><span data-stu-id="875d5-111">After you authorize the permissions, a connection is created in Power Automate.</span></span>

<span data-ttu-id="875d5-112">现在已配置并启用自定义连接器。</span><span class="sxs-lookup"><span data-stu-id="875d5-112">The custom connector is now configured and enabled.</span></span> <span data-ttu-id="875d5-113">可能在应用权限中存在延迟且可用，但现在已配置连接器。</span><span class="sxs-lookup"><span data-stu-id="875d5-113">There may be a delay in permissions being applied and available, but the connector is now configured.</span></span>
