<!-- markdownlint-disable MD002 MD041 -->

Microsoft 流有230个以上的盒外连接器。 许多这些连接器使用 microsoft graph 与 microsoft 产品的特定终结点进行通信, 但没有与 microsoft graph 直接通信的连接器来覆盖整个 API。 但是, 在某些情况下, 可能需要直接从使用服务的基本构造块的流中调用 Microsoft Graph。

除了解决直接调用 Microsoft graph 的方案之外, 许多 Microsoft Graph API 终结点仅支持[委派权限](https://docs.microsoft.com/graph/permissions-reference)。 Microsoft Flow 中的 HTTP 连接器实现了非常灵活的集成, 包括调用 Microsoft Graph。 但是, HTTP 连接器缺少缓存用户凭据以启用特定委派权限方案的功能。 在这些情况下, 可以创建自定义连接器, 以提供围绕 Microsoft Graph API 的包装, 并启用使用委派权限的 api。

此实验室涵盖了上述两个难题。 首先, 将创建自定义连接器, 以启用与需要[委派权限](https://docs.microsoft.com/graph/permissions-reference)的 Microsoft Graph 的集成。 其次, 您将使用[$batch 请求终结点](https://docs.microsoft.com/graph/json-batching), 以便在使用要求应用程序具有 "登录" 用户的委派权限时提供对 Microsoft Graph 的完整功能的访问权限。

> [!NOTE]
> 本教程介绍了如何创建自定义连接器以在 Microsoft Flow 和 Azure LogicApps 中使用。 本教程假定您已阅读[自定义连接器概述](https://docs.microsoft.com/connectors/custom-connectors/)以了解该过程。

## <a name="prerequisites"></a>先决条件

若要在此文章中完成此练习, 您将需要以下各项:

- 对 Office 365 租赁的管理员访问权限。 如果没有, 请访问[Office 365 开发人员计划](https://developer.microsoft.com/office/dev-program)以注册免费的开发人员租户。
- 对[Microsoft 流](https://flow.microsoft.com/)的访问权限。

## <a name="feedback"></a>反馈

请在[GitHub 存储库](https://github.com/microsoftgraph/msgraph-training-microsoftflow)中提供有关本教程的任何反馈。