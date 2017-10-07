Azure PowerShell 4.3.1 安装程序：[链接](https://github.com/Azure/azure-powershell/releases/download/v4.3.1-August2017/azure-powershell.4.3.1.msi)

ARM Cmdlet 的库模块：[链接](https://www.powershellgallery.com/packages/AzureRM/4.3.1)

适用于服务管理 (RDFE) 的旧 Cmdlet 的库模块：[链接](https://www.powershellgallery.com/packages/Azure/4.3.1)

## <a name="changes-in-431"></a>4.3.1 中的更改

- 修复某些程序集无法签名导致导入模块时出现 `could not load file or assembly` 错误的问题

## <a name="changes-in-430"></a>4.3.0 中的更改

* AnalysisServices
    * 修复了 Set-AzureRmAnalysisServciesServer 中的 bug
        - 如果未提供管理员，将删除该管理员。
    * New-AzureRmAnalysisServicesServer 和 Set-AzureRmAnalysisServicesServer 中添加了 BackupBlobContainerUri
        - 启用可设置/禁用用于备份/还原 Azure Analysis Services 服务器的备份 blob 容器
    * 更新了 New-AzureRmAnalysisServicesServer 和 Set-AzureRmAnalysisServicesServer 中的 SKU 查找
        - 将硬编码 SKU 改为动态查找。
    * Add-AzureAnalysisServicesAccount 支持通过服务主体登录
* 自动化
    * 对 AutomationDSC* cmdlet 进行了修改，可拉取超过 100 条记录
    * 解决了调用某些自动化 cmdlet（如 Get-AzureRmAutomationVariable、Get-AzureRmAutomationJob）之后，详细流停止工作的问题。
    * StartAzureAutomationDscCompilationJob 和 ImportAzureAutomationDscNodeConfiguration 中添加了对 NodeConfiguration 生成版本控制的支持。
    * 针对现有问题进行了 bug 修复 - 修复了 #3775 别名问题、 runOn 别名以及对 HybridWorkers 的支持。
* 计算
    * Set-AzureRmVMAEMExtension：添加对新高级磁盘大小的支持
    * Set-AzureRmVMAEMExtension：添加对 M 系列的支持
    * 向 Add-AzureRmVmssExtension 添加 ForceUpdateTag 参数
    * 向 New-AzureRmVmssIpConfig 添加 Primary 参数
    * 向 Add-AzureRmVmssNetworkInterfaceConfig 添加 EnableAcceleratedNetworking 参数
    * 向 Set-AzureRmVmss 添加 InstanceId
    * 向 Get-AzureRmVM -Status 输出公开 MaintenanceRedeployStatus
    * 向 Get-AzureRmComputeResourceSku 的表格格式公开限制和功能
* DataLakeStore
    * 问题修复：https://github.com/Azure/azure-powershell/issues/4323
* EventHub
    * 向 NamespaceAttributes 添加了 ResourceGroup 属性
        - “ResourceGroup”获取命名空间所在资源组的名称
    * commandlet 已使用新参数和参数别名更新
        - 以下 cmdlet 已使用 Namespace 的 Parameterset 和 AuthorizationRule 操作的 EventHub 更新
        - New-AzureRmEventHubAuthorizationRule
            + 向现有 NameSpace 或 EventHub 添加新的 AuthorizationRule 。
        - Get-AzureRmEventHubAuthorizationRule
            + 获取现有 NameSpace 或 EventHub 的 AuthorizationRule 或 AuthorizationRule 列表。
        - Set-AzureRmEventHubAuthorizationRule
            + 更新 EventHub NameSpace 的现有 AuthorizationRule 属性。
        - Remove-AzureRmEventHubAuthorizationRule
            + 删除现有 NameSpace 或 EventHub 的现有 AuthorizationRule。
        - New-AzureRmEventHubKey
            + 为现有 NameSpace 或 EventHub 的 AuthorizationRule 生成新的主密钥或辅助密钥。
        - Get-AzureRmEventHubKey
            + 获取现有 NameSpace 或 EventHub 的 AuthorizationRule 主密钥或辅助密钥。
* 网络
    * New-AzureRmExpressRouteCircuitPeeringConfig：添加了 IPv6 支持。 添加了新的可选参数
        - PeerAddressType
    * Set-AzureRmExpressRouteCircuitPeeringConfig：添加了 IPv6 支持。 添加了新的可选参数
        - PeerAddressType
    * Remove-AzureRmExpressRouteCircuitPeeringConfig：添加了 IPv6 支持。 添加了新的可选参数
        - PeerAddressType
    * 参数 -ProbeEnabled 标记为“已过时”
        - Add-AzureRmApplicationGatewayBackendHttpSettings
        - New-AzureRmApplicationGatewayBackendHttpSettings
        - Set-AzureRmApplicationGatewayBackendHttpSettings
* 配置文件
    * 数据收集在默认情况下处于启用状态。 Microsoft 收集使用情况数据以改进用户体验。 数据是匿名的，不会包括命令行参数值。
        - 使用 Disable-AzureRmDataCollection cmdlet 可关闭此功能
        - 使用 Enable-AzureRmDataCollection cmdlet 可打开此功能
* 资源
    * 支持将请求发送到 ARM 之前对以下 roledefinition 和 roleassignment commandlet 范围进行验证
        - Get-AzureRMRoleAssignment
        - New-AzureRMRoleAssignment
        - Remove-AzureRMRoleAssignment
        - Get-AzureRMRoleDefinition
        - New-AzureRMRoleDefinition
        - Remove-AzureRMRoleDefinition
        - Set-AzureRMRoleDefinition
* ServiceBus
    * 为 NameSpace、 Queue 和 Topic 的 AuthorizationRule 添加了以下新 commandlet。 根据参数集执行授权规则操作。
     - New-AzureRmServiceBusAuthorizationRule
       - 向现有 ServiceBus NameSpace/Queue/Topic 添加新的 AuthorizationRule 。
     - Get-AzureRmServiceBusAuthorizationRule
       - 获取现有 ServiceBus NameSpace/Queue/Topic 的 AuthorizationRule 或 AuthorizationRule 列表。
     - Set-AzureRmServiceBusAuthorizationRule
       - 更新 Servicebus NameSpace/Queue/Topic 的现有 AuthorizationRule 属性。
     - New-AzureRmServiceBusKey
       - 为现有 ServiceBus NameSpace/Queue/Topic 的 AuthorizationRule 生成新的主密钥或辅助密钥。
     - Get-AzureRmServiceBusKey
       - 获取现有 ServiceBus NameSpace/Queue/Topic 的 AuthorizationRule 主密钥或辅助密钥。
     - Remove-AzureRmServiceBusNamespaceAuthorizationRule
       - 删除 ServiceBus NameSpace/Queue/Topic 的现有 AuthorizationRule 属性。
    * 向 NamespceAttributes 添加了 Resource Group 属性
* Sql
    * 更新 Set-AzureRmSqlServerTransparentDataEncryptionProtector，如果加密保护程序类型设置为 AzureKeyVault，则会显示警告并要求确认
    * 为审核设置添加新的已更新 cmdlet
        - 添加 Get-AzureRmSqlDatabaseAuditing cmdlet，它可获取 Azure SQL 数据库的审核设置。
        - 添加 Get-AzureRmSqlServerAuditing cmdlet，它可获取 Azure SQL Server 的审核设置。
        - 添加 Set-AzureRmSqlDatabaseAuditing cmdlet，它可更改 Azure SQL 数据库的审核设置。
        - 添加 Set-AzureRmSqlServerAuditing cmdlet，它可更改 Azure SQL Server 的审核设置。
    * 弃用现有审核策略 cmdlet
        - 弃用 Get-AzureRmSqlDatabaseAuditingPolicy
        - 弃用 Get-AzureRmSqlServerAuditingPolicy
        - 弃用 Set-AzureRmSqlDatabaseAuditingPolicy
        - 弃用 Set-AzureRmSqlServerAuditingPolicy
        - 弃用 Use-AzureRmSqlServerAuditingPolicy
        - 弃用 Remove-AzureRmSqlDatabaseAuditing
        - 弃用 Remove-AzureRmSqlServerAuditing
    * Update-AzureRmSqlSyncGroup 的架构文件分析现可区分大小写。
* 存储
    * 向资源模式存储帐户 cmdlet 添加 NeworkRule 支持
        - New-AzureRmStorageAccount
        - Set-AzureRmStorageAccount
        - Get-AzureRmStorageAccountNetworkRuleSet
        - Update-AzureRmStorageAccountNetworkRuleSet
        - Add-AzureRmStorageAccountNetworkRule
        - Remove-AzureRmStorageAccountNetworkRule

查看[自上次发布以来的更改](https://github.com/Azure/azure-powershell/compare/v4.2.1-July2017...v4.3.1-August2017)
