<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="436c0-101">在本练习中，将创建一个新的自定义连接器，该连接器可在流中或在 Azure 逻辑应用中使用。</span><span class="sxs-lookup"><span data-stu-id="436c0-101">In this exercise, you will create a new custom connector which can be used in Flow or in Azure Logic Apps.</span></span> <span data-ttu-id="436c0-102">将使用 Microsoft Graph `$batch`终结点的正确路径预建 Open API 定义文件，并使用其他设置来启用简单导入。</span><span class="sxs-lookup"><span data-stu-id="436c0-102">The Open API definition file is prebuilt with the correct path for the Microsoft Graph `$batch` endpoint and additional settings to enable simple import.</span></span>

<span data-ttu-id="436c0-103">使用文本编辑器，创建一个名为`MSGraph-Delegate-Batch.swagger.json`的新的空文件，并添加以下代码。</span><span class="sxs-lookup"><span data-stu-id="436c0-103">Using a text editor, create a new empty file named `MSGraph-Delegate-Batch.swagger.json` and add the following code.</span></span>

[!code-json[](../LabFiles/MSGraph-Delegate-Batch.swagger.json)]

<span data-ttu-id="436c0-104">打开浏览器并导航到[Microsoft Flow](https://flow.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="436c0-104">Open a browser and navigate to [Microsoft Flow](https://flow.microsoft.com).</span></span> <span data-ttu-id="436c0-105">使用 Office 365 租户管理员帐户登录。</span><span class="sxs-lookup"><span data-stu-id="436c0-105">Sign in with your Office 365 tenant administrator account.</span></span> <span data-ttu-id="436c0-106">在左侧菜单中，展开 "**数据**"，然后选择 "**自定义连接器**"。</span><span class="sxs-lookup"><span data-stu-id="436c0-106">In the left-hand menu, expand **Data** and choose **Custom connectors**.</span></span>

![Microsoft Flow 中自定义连接器菜单项的屏幕截图](./images/flow-conn1.png)

<span data-ttu-id="436c0-108">在 "**自定义连接器**" 页上，选择右上方的**新自定义连接线**链接，然后在下拉菜单中选择 "**导入 OpenAPI 文件**" 项。</span><span class="sxs-lookup"><span data-stu-id="436c0-108">On the **Custom connectors** page choose the **New custom connector** link in the top right, then select the **Import an OpenAPI file** item in the drop-down menu.</span></span> <span data-ttu-id="436c0-109">在`MS Graph Batch Connector` "**连接器名称**" 文本框中输入。</span><span class="sxs-lookup"><span data-stu-id="436c0-109">Enter `MS Graph Batch Connector` in the **Connector name** text box.</span></span> <span data-ttu-id="436c0-110">选择 "**导入**" 按钮以上载打开的 API 文件。</span><span class="sxs-lookup"><span data-stu-id="436c0-110">Choose **Import** button to upload the Open API file.</span></span> <span data-ttu-id="436c0-111">浏览到您`MSGraph-Delegate-Batch.swagger.json`创建的文件。</span><span class="sxs-lookup"><span data-stu-id="436c0-111">Browse to the `MSGraph-Delegate-Batch.swagger.json` file you created.</span></span> <span data-ttu-id="436c0-112">选择 "**继续**" 上传 OpenAPI 文件。</span><span class="sxs-lookup"><span data-stu-id="436c0-112">Choose **Continue** to upload the OpenAPI file.</span></span>

 !["创建自定义连接器" 对话框的屏幕截图](./images/flow-conn3.png)

<span data-ttu-id="436c0-114">在 "连接器配置" 页上，选择 "导航" 菜单中的 "**安全**" 链接。</span><span class="sxs-lookup"><span data-stu-id="436c0-114">On the connector configuration page, choose the **Security** link in the navigation menu.</span></span> <span data-ttu-id="436c0-115">按如下所示填写字段。</span><span class="sxs-lookup"><span data-stu-id="436c0-115">Fill in the fields as follows.</span></span>

- <span data-ttu-id="436c0-116">**选择您的 API 实现的身份验证**：`OAuth 2.0`</span><span class="sxs-lookup"><span data-stu-id="436c0-116">**Choose what authentication is implemented by your API**: `OAuth 2.0`</span></span>
- <span data-ttu-id="436c0-117">**标识提供程序**：`Azure Active Directory`</span><span class="sxs-lookup"><span data-stu-id="436c0-117">**Identity Provider**: `Azure Active Directory`</span></span>
- <span data-ttu-id="436c0-118">**客户端 id**：在上一练习中创建的应用程序 id</span><span class="sxs-lookup"><span data-stu-id="436c0-118">**Client id**: the application ID you created in the previous exercise</span></span>
- <span data-ttu-id="436c0-119">**客户端密码**：在上一练习中创建的密钥</span><span class="sxs-lookup"><span data-stu-id="436c0-119">**Client secret**: the key you created in the previous exercise</span></span>
- <span data-ttu-id="436c0-120">**登录 url**：`https://login.windows.net`</span><span class="sxs-lookup"><span data-stu-id="436c0-120">**Login url**: `https://login.windows.net`</span></span>
- <span data-ttu-id="436c0-121">**租户 ID**：`common`</span><span class="sxs-lookup"><span data-stu-id="436c0-121">**Tenant ID**: `common`</span></span>
- <span data-ttu-id="436c0-122">**资源 URL**： `https://graph.microsoft.com` （无尾随/）</span><span class="sxs-lookup"><span data-stu-id="436c0-122">**Resource URL**: `https://graph.microsoft.com` (no trailing /)</span></span>
- <span data-ttu-id="436c0-123">**范围**：保留为空</span><span class="sxs-lookup"><span data-stu-id="436c0-123">**Scope**: Leave blank</span></span>

<span data-ttu-id="436c0-124">选择右上方的 "**创建连接器**"</span><span class="sxs-lookup"><span data-stu-id="436c0-124">Choose **Create Connector** on the top-right</span></span>

![连接器配置中的 "安全" 选项卡的屏幕截图](./images/flow-conn4.png)

<span data-ttu-id="436c0-126">创建连接器后，复制生成的**重定向 URL**。</span><span class="sxs-lookup"><span data-stu-id="436c0-126">After the connector has been created, copy the generated **Redirect URL**.</span></span>

![生成的重定向 URL 的屏幕截图](./images/flow-conn5.png)

<span data-ttu-id="436c0-128">返回到在上一练习中创建的[Azure 门户](https://aad.portal.azure.com)中已注册的应用程序。</span><span class="sxs-lookup"><span data-stu-id="436c0-128">Go back to the registered application in the [Azure Portal](https://aad.portal.azure.com) you created in the previous exercise.</span></span> <span data-ttu-id="436c0-129">选择**MS Graph 批处理应用**边栏上的**概述**，然后选择 "**添加重定向 URI**"。</span><span class="sxs-lookup"><span data-stu-id="436c0-129">Select **Overview** on the **MS Graph Batch App** blade, then select **Add a Redirect URI**.</span></span> <span data-ttu-id="436c0-130">在 "**重定向 URI** " 字段中添加已复制的**重定向 URL** ，然后选择 "**保存**"。</span><span class="sxs-lookup"><span data-stu-id="436c0-130">Add the **Redirect URL** you copied in the **Redirect URI** field and choose **Save**.</span></span>

![Azure 门户中答复 Url 刀片的屏幕截图](./images/flow-conn-preview6.png)
