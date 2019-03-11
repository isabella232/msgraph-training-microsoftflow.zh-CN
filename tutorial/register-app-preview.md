<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="b0b5d-101">在本练习中, 将创建一个新的 Azure Active Directory 应用程序, 该应用程序将用于为自定义连接器提供委派权限。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-101">In this exercise, you will create a new Azure Active Directory Application which will be used to provide the delegated permissions for the custom connector.</span></span>

<span data-ttu-id="b0b5d-102">打开浏览器并导航到[Azure Active Directory 管理中心](https://aad.portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-102">Open a browser and navigate to [Azure Active Directory admin center](https://aad.portal.azure.com).</span></span> <span data-ttu-id="b0b5d-103">在左侧导航菜单中选择 " **Azure Active Directory** " 链接, 然后在**Azure active directory**边栏的 "**管理**" 部分中选择 "**应用注册 (预览)** " 条目。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-103">Choose the **Azure Active Directory** link in the left navigation menu, then choose the **App registrations (Preview)** entry in the **Manage** section of the **Azure Active Directory** blade.</span></span>

![azure active directory 中的 azure active directory 刀片的屏幕截图管理中心](./images/app-reg-preview1.png)

<span data-ttu-id="b0b5d-105">选择 "**应用注册" (预览)** 刀片顶部的 "**新建注册**" 菜单项。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-105">Choose the **New registration** menu item at the top of the **App Registrations (Preview)** blade.</span></span>

![Azure Active Directory 管理中心中的应用程序注册刀片的屏幕截图](./images/app-reg-preview2.png)

<span data-ttu-id="b0b5d-107">在`MS Graph Batch App` "**名称**" 字段中输入。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-107">Enter `MS Graph Batch App` in the **Name** field.</span></span> <span data-ttu-id="b0b5d-108">在 "**支持的帐户类型**" 部分, 选择**任意组织目录中的 "帐户"**。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-108">In the **Supported account types** section, select **Accounts in any organizational directory**.</span></span> <span data-ttu-id="b0b5d-109">将 "**重定向 URI** " 部分留空, 然后选择 "**注册**"。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-109">Leave the **Redirect URI** section blank and choose **Register**.</span></span>

![在 Azure Active Directory 管理中心中注册应用程序边栏的屏幕截图](./images/app-reg-preview3.png)

<span data-ttu-id="b0b5d-111">在**MS Graph 批处理应用**边栏上, 复制**应用程序 (客户端) ID**。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-111">On the **MS Graph Batch App** blade, copy the **Application (client) ID**.</span></span> <span data-ttu-id="b0b5d-112">在下一个练习中, 你将需要此操作。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-112">You'll need this in the next exercise.</span></span>

![已注册的应用程序页的屏幕截图](./images/app-reg-preview4.png)

<span data-ttu-id="b0b5d-114">在**MS Graph 批处理应用**边栏的 "**管理**" 部分中选择 " **API 权限**" 条目。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-114">Choose the **API permissions** entry in the **Manage** section of the **MS Graph Batch App** blade.</span></span> <span data-ttu-id="b0b5d-115">选择 " **API 权限**" 下**的 "添加权限**"。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-115">Choose **Add a permission** under **API permissions**.</span></span>

![API 权限刀片的屏幕截图](./images/app-perms-preview1.png)

<span data-ttu-id="b0b5d-117">在 "**请求 API 权限**" 边栏中, 选择 " **Microsoft Graph**", 然后选择 "**委派权限**"。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-117">In the **Request API permissions** blade, choose the **Microsoft Graph**, then choose **Delegated permissions**.</span></span> <span data-ttu-id="b0b5d-118">搜索`group`, 然后选择 "**读取和写入所有组**" 委派权限。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-118">Search for `group`, then select the **Read and write all groups** delegated permission.</span></span> <span data-ttu-id="b0b5d-119">选择刀片式服务器底部的 "**添加权限**"。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-119">Choose **Add permissions** at the bottom of the blade.</span></span>

 ![请求 API 权限刀片的屏幕截图](./images/app-perms-preview2.png)

<span data-ttu-id="b0b5d-121">在**MS Graph 批处理应用**边栏的 "**管理**" 部分中选择 "**证书和密码**" 条目, 然后选择 "**新建客户端密码**"。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-121">Choose the **Certificates and secrets** entry in the **Manage** section of the **MS Graph Batch App** blade, then choose **New client secret**.</span></span> <span data-ttu-id="b0b5d-122">在`forever` **说明**中输入, 然后选择 "**永不\*\*\*\*过期**"。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-122">Enter `forever` in the **Description** and select **Never** under **Expires**.</span></span> <span data-ttu-id="b0b5d-123">选择“添加”\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-123">Choose **Add**.</span></span>

![证书和密码刀片的屏幕截图](./images/app-key-preview1.png)

<span data-ttu-id="b0b5d-125">复制新项的键值。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-125">Copy the key value for the new key.</span></span> <span data-ttu-id="b0b5d-126">在下一个练习中, 你将需要此操作。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-126">You'll need this in the next exercise.</span></span>

![新客户端密码的屏幕截图](./images/app-key-preview2.png)

> [!IMPORTANT]
> <span data-ttu-id="b0b5d-128">此步骤非常关键, 因为关闭此边栏后将无法访问密钥。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-128">This step is critical as the key will not be accessible once you close this blade.</span></span> <span data-ttu-id="b0b5d-129">将此项保存到文本编辑器中, 以便在即将进行的练习中使用。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-129">Save this key to a text editor for use in upcoming exercises.</span></span>

<span data-ttu-id="b0b5d-130">若要启用对通过 Microsoft Graph (包括团队属性) 访问的其他服务的管理, 需要选择其他更合适的范围以启用管理特定服务。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-130">To enable management of additional services accessible via the Microsoft Graph, including Teams properties, you would need to select additional, appropriate scopes to enable managing specific services.</span></span> <span data-ttu-id="b0b5d-131">例如, 若要扩展我们的解决方案以启用创建 OneNote 笔记本或 Planner 计划、存储桶和任务, 需要为相关 api 添加所需的权限范围。</span><span class="sxs-lookup"><span data-stu-id="b0b5d-131">For example, to extend our solution to enable creating OneNote Notebooks or Planner plans, buckets and tasks you would need to add the required permission scopes for the relevant APIs.</span></span>