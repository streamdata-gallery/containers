swagger: "2.0"
x-collection-name: Azure Data Lake Analytics
x-complete: 1
info:
  title: DataLakeAnalyticsJobManagementClient
  description: creates-an-azure-data-lake-analytics-job-client-
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DataLakeAnalytics/accounts/{accountName}/StorageAccounts/{storageAccountName}/Containers/{containerName}
  : get:
      summary: Storage Accounts Get Storage Container
      description: Gets the specified Azure Storage container associated with the
        given Data Lake Analytics and Azure Storage accounts.
      operationId: StorageAccounts_GetStorageContainer
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-datalakeanalyticsaccountsaccountnamestorageaccountsstorageaccountnamecontainerscontainername-get
      parameters:
      - in: path
        name: accountName
        description: The name of the Data Lake Analytics account for which to retrieve
          blob container
      - in: path
        name: containerName
        description: The name of the Azure storage container to retrieve
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the Azure resource group that contains the Data Lake
          Analytics account
      - in: path
        name: storageAccountName
        description: The name of the Azure storage account from which to retrieve
          the blob container
      responses:
        200:
          description: OK
      tags:
      - Containers