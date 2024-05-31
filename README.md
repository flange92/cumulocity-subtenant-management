# Cumulocity Subtenant Management
Tool for managing subtenants from a c8y management or enterprise tenant

## Capabilities of this tool

This tool allows to access subtenants from a Cumulocity enterprise or management tenant.
To do so, it performs priviledge escalation through a dummy microservice, which is created on management/enterprise tenant and subscribed to the desired subtenants.
The microservices credentials are then used to access the subtenants.

The following actions can be performed on the subtenants:
- User
  - creation
  - suspend/reactivation
  - edit
  - delete
  - trigger password reset mail
- Devices
  - list
  - trigger operations (e.g. restart, firmware update or configuration update)
- Device registration requests
  - list
  - create bulk device registration request
  - cancel/accept
- Firmware update history (see failing/successfull firmware updates)
- **Provisioning**
  - **Alarm transformations**
  - **Analytics Builder**
  - **Applications** (Lists the available applications, microservices, packages available in the tenant along with the list of active tenants having the app. Subscribe / un-subscribe from the specific tenant option is available.  )
  - EPL Rules
  - Firmware (Lists the firmware available in the tenant. Provision/Re-provision options are available for all selected sub-tenants.)
  - Global roles (Lists global rules available in the tenant, incl. permissions and applications. Existing global roles can be re-provisioned for sub-tenants)
  - Retention rules (Lists the retention rules from all the sub-tenants. New retention rule can be created, sub-tenants can be selected while doing so. Update and delete of retention rule is available.)
  - Smart Groups
  - SmartREST templates (Lists the SmartREST templates available in the tenant. Existing SmartREST templates can be re-provisioned to the sub-tenants. )
  - Tenant options (Lists the tenant options available in the tenant. New tenant options can be created . Tenant options can be re-provisioned to the sub-tenants.)
- Statistics
  - Firmware (Diagramm to check which firmware version is installed on which amount of devices for a specific sub-tenant.)
  - Inventory (Lists the count of inventory objects matching the query respective to each sub-tenant . Query can be entered in the right top corner field. )
  - Storage (Sub-tenants list is displayed, to cleanup reports of 14 days older option is available. )
 
These capabilities could be in general extended further. For any requirements raise an issue or contribute by creating a PR.

## Installation

1. Download the [latest release of the Subtenant Management App](https://github.com/SoftwareAG/cumulocity-subtenant-management/releases/latest)
2. Open the Administration app of your enterprise or management tenant
3. Navigate to "Applications" -> "Own applications"
4. Click the "Add application" button in the upper right corner
5. Select "Upload web application" in the dialog and upload the zip file you've downloaded in the first step
6. After a reload of the page, the Subtenant Management App should be available in your app switcher


------------------------------

These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.

## 

## This application does not support the following features yet:
- Pagination during subtenant selection
- preview whether any assets have been deployed or provisioned on the target tenant