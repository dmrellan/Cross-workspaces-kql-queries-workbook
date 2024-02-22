# Cross-workspaces-kql-queries-workbook

Have you ever needed to run a Kusto Query Language (KQL) query against **multiple** (or all) of your Log Analytics workspaces?

If so, you probably know this can be achieved through [**cross-workspace queries**](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/cross-workspace-query). These queries can be executed directly using the appropriate KQL syntax or modifying the query scope from the Azure portal. Although both solutions are valid and effective, they are, not always, the most efficient way. For example, if the number of workspaces is high, selecting them one by one can be impractical. However, a third option will save us time: **using Azure Workbooks**.

In this article, I want to share a simple but very useful Azure Workbook to save time if you need to run KQL queries on multiple Log Analytics workspaces. As you can see below, the workbook consists of four parameters: subscriptions, workspaces, time range, and a **KQL query**. By writing the query and clicking outside the parameter, a cross-query will be run against all the selected Log Analytics workspaces, unifying the results in a table. In this way, you can quickly consult or export the results.

![image](https://github.com/dmrellan/Cross-workspaces-kql-queries-workbook/assets/35997289/a090b9df-5086-4234-b8b4-d2c7b83105b1)


You can find the workbook code in the **materials** folder of this article. Enjoy it! But remember, the maximum limit of workspaces for a cross-query is 100 in each execution. Therefore, if you have [over 100 workspaces](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/cross-workspace-query#limitations), you must perform several executions.

Any comments or suggestions are welcome.

