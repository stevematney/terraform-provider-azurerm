## 2.51.0 (Unreleased)

FEATURES:

* **New Resource:** `azurerm_purview_account` [GH-10395]
* **New Resource:** `azurerm_data_factory_dataset_parquet` [GH-10852]
* **New Resource:** `azurerm_security_center_server_vulnerability_assessment` [GH-10030]
* **New Resource:** `azurerm_security_center_assessment` [GH-10694]
* **New Resource:** `azurerm_security_center_assessment_policy` [GH-10694]
* **New Resource:** `azurerm_sentinel_data_connector_azure_advanced_threat_protection` [GH-10666]
* **New Resource:** `azurerm_sentinel_data_connector_azure_security_center` [GH-10667]
* **New Resource:** `azurerm_sentinel_data_connector_microsoft_cloud_app_security` [GH-10668]

ENHANCEMENTS:

* dependencies: updating to v52.3.0 of `github.com/Azure/azure-sdk-for-go` [GH-10829]
* `azurerm_role_assignment` - support enrollment ids in `scope` argument [GH-10890]
* `azurerm_kubernetes_cluster` - support `None` for the `private_dns_zone_id` property [GH-10774]
* `azurerm_kubernetes_cluster` - support for `expander` in the `auto_scaler_profile` block [GH-10777]
* `azurerm_linux_virtual_machine` - support for configuring `platform_fault_domain` [GH-10803]
* `azurerm_linux_virtual_machine_scale_set` - will no longer recreate the resource when `rolling_upgrade_policy` or `health_probe_id` is updated [GH-10856]
* `azurerm_windows_virtual_machine` - support for configuring `platform_fault_domain` [GH-10803]
* `azurerm_windows_virtual_machine_scale_set` - will no longer recreate the resource when `rolling_upgrade_policy` or `health_probe_id` is updated [GH-10856]

BUG FIXES:

* Data Source: `azurerm_function_app_host_keys` - retrying reading the keys to work around a broken API [GH-10894]
* Data Source: `azurerm_log_analytics_workspace` - ensure the `id` is returned with the correct casing [GH-10892]
* Data Source: `azurerm_monitor_action_group` - add support for `aad_auth` attribute [GH-10876]
* `azurerm_api_management_custom_domain` - prevent a perpetual diff [GH-10636]
* `azurerm_eventhub_consumer_group` - detecting as removed when deleted in Azure [GH-10900]
* `azurerm_key_vault_access_policy` - Fix destroy where permissions casing on service does not match config / state [GH-10931]
* `azurerm_key_vault_secret` - setting the value of the secret after recovering it [GH-10920]
* `azurerm_kusto_eventhub_data_connection` - make `table_name` and `data_format` optional [GH-10913]
* `azurerm_mssql_virtual_machine` - workaround for inconsistent API value for `log_backup_frequency_in_minutes` in the `manual_schedule` block [GH-10899]
* `azurerm_postgres_server` - support for replicaset scaling [GH-10754]
* `azurerm_postgresql_aad_administrator` - prevent invalid usernames for the `login` property [GH-10757]

---

## 2.50.0 (March 05, 2021)

FEATURES:

* **New Data Source:** `azurerm_vmware_private_cloud` ([#9284](https://github.com/terraform-providers/terraform-provider-azurerm/issues/9284))
* **New Resource:** `azurerm_kusto_eventgrid_data_connection` ([#10712](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10712))
* **New Resource:** `azurerm_sentinel_data_connector_aws_cloud_trail` ([#10664](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10664))
* **New Resource:** `azurerm_sentinel_data_connector_azure_active_directory` ([#10665](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10665))
* **New Resource:** `azurerm_sentinel_data_connector_office_365` ([#10671](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10671))
* **New Resource:** `azurerm_sentinel_data_connector_threat_intelligence` ([#10670](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10670))
* **New Resource:** `azurerm_subscription` ([#10718](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10718))
* **New Resource:** `azurerm_vmware_private_cloud` ([#9284](https://github.com/terraform-providers/terraform-provider-azurerm/issues/9284))

ENHANCEMENTS:
* dependencies: updating to `v52.0.0` of `github.com/Azure/azure-sdk-for-go` ([#10787](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10787))
* dependencies: updating `compute` to API version `2020-12-01` ([#10650](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10650))
* Data Source: `azurerm_dns_zone` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_a_record` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_aaaa_record` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_caa_record` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_cname_record` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_mx_record` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_ns_record` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_ptr_record` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_srv_record` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_txt_record` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_dns_zone` - updating to use a consistent Terraform Resource ID to avoid API issues ([#10786](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10786))
* `azurerm_function_app_host_keys` - support for `event_grid_extension_config_key` ([#10823](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10823))
* `azurerm_keyvault_secret` - support for the `versionless_id` property ([#10738](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10738))
* `azurerm_kubernetes_cluster` - support `private_dns_zone_id` when using a `service_principal` ([#10737](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10737))
* `azurerm_kusto_cluster` - supports for the `double_encryption_enabled` property ([#10264](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10264))
* `azurerm_linux_virtual_machine` - support for configuring `license_type` ([#10776](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10776))
* `azurerm_log_analytics_workspace_resource` - support permanent deletion of workspaces with the `permanently_delete_on_destroy` feature flag ([#10235](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10235))
* `azurerm_monitor_action_group` - support for secure webhooks via the `aad_auth` block ([#10509](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10509))
* `azurerm_mssql_database` - support for the `log_monitoring_enabled` property within the `extended_auditing_policy` block ([#10324](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10324))
* `azurerm_mssql_database_extended_auditing_policy ` - support for the `log_monitoring_enabled` property ([#10324](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10324))
* `azurerm_mssql_server` - support for the `log_monitoring_enabled` property within the `extended_auditing_policy` block ([#10324](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10324))
* `azurerm_mssql_server_extended_auditing_policy ` - support for the `log_monitoring_enabled` property [[#10324](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10324)] 
* `azurerm_signalr_service` - support for the `upstream_endpoint` block ([#10459](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10459))
* `azurerm_sql_server` - support for the `log_monitoring_enabled` property within the `extended_auditing_policy` block ([#10324](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10324))
* `azurerm_sql_database` - support for the `log_monitoring_enabled` property within the `extended_auditing_policy` block ([#10324](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10324))
* `azurerm_spring_cloud_java_deployment` - supporting delta updates ([#10729](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10729))
* `azurerm_virtual_network_gateway` - deprecate `peering_address` in favour of `peering_addresses` ([#10381](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10381))

BUG FIXES:

* Data Source: `azurerm_netapp_volume` - fixing a crash when setting `data_protection_replication` ([#10795](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10795))
* `azurerm_api_management` - changing the `sku_name` property no longer forces a new resouce to be created ([#10747](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10747))
* `azurerm_api_management` - the field `tenant_access` can only be configured when not using a Consumption SKU ([#10766](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10766))
* `azurerum_frontdoor` - removed the MaxItems validation from the Backend Pools ([#10828](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10828))
* `azurerm_kubernetes_cluster_resource` - allow windows passwords as short as `8` charaters long ([#10816](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10816))
* `azurerm_cosmosdb_mongo_collection` - ignore throughput if Cosmos DB provisioned in 'serverless' capacity mode ([#10389](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10389))
* `azurerm_linux_virtual_machine` - parsing the User Assigned Identity ID case-insensitively to work around an Azure API issue ([#10722](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10722))
* `azurerm_linux_virtual_machine_scale_set` - parsing the User Assigned Identity ID case-insensitively to work around an Azure API issue ([#10722](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10722))
* `azurerm_netapp_volume` - fixing a crash when setting `data_protection_replication` ([#10795](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10795))
* `azurerm_virtual_machine` - parsing the User Assigned Identity ID case-insensitively to work around an Azure API issue ([#10722](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10722))
* `azurerm_virtual_machine_scale_set` - parsing the User Assigned Identity ID case-insensitively to work around an Azure API issue ([#10722](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10722))
* `azurerm_windows_virtual_machine` - parsing the User Assigned Identity ID case-insensitively to work around an Azure API issue ([#10722](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10722))
* `azurerm_windows_virtual_machine_scale_set` - parsing the User Assigned Identity ID case-insensitively to work around an Azure API issue ([#10722](https://github.com/terraform-providers/terraform-provider-azurerm/issues/10722))

---

For information on changes between the v2.49.0 and v2.0.0 releases, please see [the previous v2.x changelog entries](https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/CHANGELOG-v2.md).

For information on changes in version v1.44.0 and prior releases, please see [the v1.x changelog](https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/CHANGELOG-v1.md).
