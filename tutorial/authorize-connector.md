<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="585f4-101">确保连接器可供使用的最后一个配置步骤是授权和测试自定义连接器以创建缓存的连接。</span><span class="sxs-lookup"><span data-stu-id="585f4-101">The final configuration step to ensure the connector is ready for use is to authorize and test the custom connector to create a cached connection.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="585f4-102">以下步骤要求您使用管理员权限登录。</span><span class="sxs-lookup"><span data-stu-id="585f4-102">The following steps requires that you are logged in with administrator privileges.</span></span>

<span data-ttu-id="585f4-103">在[Microsoft Flow](https://flow.microsoft.com)中, 转到 "连接器配置" 屏幕并在导航菜单中选择 "**测试**" 链接。</span><span class="sxs-lookup"><span data-stu-id="585f4-103">In [Microsoft Flow](https://flow.microsoft.com), go to the Connector configuration screen and choose the **Test** link in the navigation menu.</span></span> <span data-ttu-id="585f4-104">选择 "**新建连接**" 链接。</span><span class="sxs-lookup"><span data-stu-id="585f4-104">Choose the **New Connection** link.</span></span> <span data-ttu-id="585f4-105">使用 Office 365 租户管理员的 Azure Active Directory 帐户登录。</span><span class="sxs-lookup"><span data-stu-id="585f4-105">Sign in with your Office 365 tenant administrator's Azure Active Directory account.</span></span>

<span data-ttu-id="585f4-106">当系统提示您输入请求的权限时, 请选中 "**代表您的组织同意"** , 然后选择 "**接受**" 以授权权限。</span><span class="sxs-lookup"><span data-stu-id="585f4-106">When prompted for the requested permissions, check **Consent on behalf of your organization** and then choose **Accept** to authorize permissions.</span></span>

![权限提示的屏幕截图](./images/flow-conn8.png)

<span data-ttu-id="585f4-108">授权权限后, 将在流中创建连接。</span><span class="sxs-lookup"><span data-stu-id="585f4-108">After you authorize the permissions, a connection is created in Flow.</span></span>

![在 Microsoft Flow 中创建的连接的屏幕截图](./images/flow-conn9.png)

<span data-ttu-id="585f4-110">现在已配置并启用自定义连接器。</span><span class="sxs-lookup"><span data-stu-id="585f4-110">The custom connector is now configured and enabled.</span></span> <span data-ttu-id="585f4-111">可能在应用权限中存在延迟且可用, 但现在已配置连接器。</span><span class="sxs-lookup"><span data-stu-id="585f4-111">There may be a delay in permissions being applied and available, but the connector is now configured.</span></span>