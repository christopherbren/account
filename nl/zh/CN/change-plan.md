---



copyright:

  years: 2017, 2018
lastupdated: "2018-02-07"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 更改套餐
{: #changing}

您可以在 {{site.data.keyword.Bluemix}} 的服务实例仪表板中更改服务套餐，前提是该服务支持套餐更改。
{: shortdesc}

如果您在查找有关升级帐户类型的详细信息，请参阅[如何升级或更改帐户类型？](/docs/account/account_faq.html#changeacct)。
{: tip}

只有特定服务才提供更改服务套餐的功能。如果服务支持套餐更改，那么服务实例仪表板的导航中会显示**套餐**选项。每个服务在套餐更改后都有一组不同的后续步骤要执行。

1. 要更改套餐，请在服务实例仪表板中单击**套餐**。通常，可以升级套餐或降级套餐。
2. 更改套餐后，必须完成一组后续步骤。步骤根据套餐更改和服务的类型而有所不同。例如，如果降级了套餐，那么可能需要重新编译打包应用程序。或者，如果升级了套餐，那么可能需要重新编译打包应用程序并执行其他操作。<br/><br/>要重新编译打包应用程序，请转至 {{site.data.keyword.Bluemix_notm}}“仪表板”，然后找到与服务绑定的应用程序。在应用程序菜单中，选择**重新启动应用程序**。<br/><br/>其他后续步骤操作取决于服务。请参阅下表以了解具体的操作。

|服务|	信息|
|--------|-------------|
|Presence Insights|如果您拥有轻量套餐，但已超过免费限额，那么会显示或记录 403 消息，指示您不再有权使用，且您的服务实例已禁用。此外，还会拒绝 POST REST API 调用，并返回 403 响应。<br/><br/>如果由于超过免费限额而禁用了服务，那么可以从轻量套餐升级到付费套餐。服务将在 2 小时内重新启用。<br/><br/>如果您拥有付费套餐，那么可以将套餐降级到轻量套餐，只要您的使用量未超出事件和总存储量的轻量套餐限额即可。<br/><br/>升级或降级套餐后，都无需重新编译打包或重新启动应用程序。|
{:caption="表 1. 更改套餐的后续步骤" caption-side="top"}

## 通过命令行界面更改套餐
{: #changing_command_line}

（可选）您可以在命令行界面输入以下命令来更改服务套餐：
```
cf update-service <service_name> [-p <new_plan>]
```
