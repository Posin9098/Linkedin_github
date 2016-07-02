# HelpBaseify REST API

Here we create a REST api for report a bug or add new bug from third party to Lean Testing site.

For add a new bug you just create an url (explain below) with parameters and hit that url and it return with a json. 

For this we want various parameter (List is below)

1. Project_id (as '**project_id**') : Id of project in which we want to add bug
2. Token (as '**token**'): Authentication toke

Rest of all lean parameters are below.
We need all required parameter and rest of all are optional.

Note: We can pass either **project_version** or **project_version_id** 

Request parameters

Name | type | Description | Required
------------ | ------------- | ------------- | -------------
title | string | Bug title | Required
status_id | integer || Required
status_id | integer || Required
project_version | string |The project version where the bug occurred. e.g. v1.1 or beta | Required
project_version_id | integer | The project version ID where the bug occurred. This parameter has precedence over project_version. | Required
project_section_id | integer || Optional
type_id | integer || Optional
reproducibility_id | integer || Optional
priority_id | integer || Optional
assigned_user_id | integer | The user ID that will be assigned to this bug | Optional
description | string || Optional
expected_results | string || Optional
steps | array | A list with the steps to reproduce the bu | Optional
platform | object | The platform details were the bug occurred (with the options shown below). | Optional
| **Show child parameters**
device_model | string | e.g. iPhone | Optional
device_model_id | integer | Has precedence over device_model. | Optional
os | string | e.g. iOS | Optional
os_version | string | e.g. 8.1 | Optional
os_version_id | integer |Has precedence over os_version | Optional
browser_version_id | integer |  | Optional


**Here is the example of rest api url**

URL:

**Main url** : http://a.posintechnologies.com/helpbaseify.php?
**Required parameters** : project_id=15646&token=aemV7Olm9syJGdZ59RnCF86RDJg6Ap2MG6NK7XsI&title=Bugwithapi&status_id=1&severity_id=2&project_version_id=19756
**Optional parameters** : 
assigned_user_id=20154&reproducibility_id=1&type_id=1&priority_id=1&description=itsjustatest&expected_results=getresult&project_section_id=47219&device_type_id=3&device_model_id=3597&browser_version_id=43&os_version_id=6

**So the url with only required fields is**:
required parameters url
all parameters api

