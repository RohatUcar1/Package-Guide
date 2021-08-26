
## Azure Active Directory Package


| Nodes                                     | Description             |
|-------------------------------------------|----------------------|
| `Add User To Group`                              | `This node adds user to a specific group` |
| `Connect`               | `This is first node and provide access for directory` |
| `Create Group`                     | `This node creates a group` |
| `Create User`                              | `This node creates a user` |
| `Delete Group`                     | `This node deletes a group` |
| `Delete User`                     | `This node deletes a user` |
| `Delete User From Group`  | `This node deletes a user from a group` |
| `Get Group` | `This node retrieves info about specific group` |
| `Get User`                              | `This node retrieves info about specific user`    |
| `List Group Members`                         | `This node lists members of a specific group`    |
| `Show All Groups`                         | `This node shows all groups in directory`    |
| `Show All Users`                         | `This node shows all users in directory`    |
| `Update Group`                         | `This node updates group properties`    |
| `Update User`                         | `This node updates user properties`    |



## Add User To Group

Input

  Name  | Key | Required | Type | Description
- Group Object Id | GroupObjectId | True | string | Id of a group.
- User Id | UserId | True  | string | Id of a user.

Output

Name  | Key | Required | Type | Description
- Result | result | True | object | Response message for request.

Options

Errors
Code  |  Description
- Robomotion.ActiveDirectory.AddUserToGroup.InvalidGroupObjectId | Group Id is empty.
- Robomotion.ActiveDirectory.AddUserToGroup.InvalidUserId | User Id is empty.
## Connect

Input

Name  | Key | Required | Type | Description
- Tenant Id | TenantId | True | string | Id of tenant.
- Client(Application) Id | ClientId | True  | string | Id of application.
- Client Secret | ClientSecret | True  | string | Secret value.

Output

- Name  | Key | Required | Type | Description
- Access Token | accesstoken | True | object | Access token for application.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.Connect.InvalidClientId | Client Id is empty.
- Robomotion.ActiveDirectory.Connect.InvalidClientSecret | Client Secret is empty.
- Robomotion.ActiveDirectory.Connect.InvalidTenantId | Tenant Id is empty.
## Create Group

Input

Name  | Key | Required | Type | Description
- Access Token | accesstoken | True | object | Access token for application.
- Editor | - | True  | - | Group properties.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.AddUserToGroup.InvalidGroupObjectId | Group Id is empty.
- Robomotion.ActiveDirectory.AddUserToGroup.InvalidUserId | User Id is empty.
## Create User

Input

Name  | Key | Required | Type | Description
- Access Token | accesstoken | True | object | Access token for application.
- Editor | - | True  | - | User properties.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

## Delete Group

Input

Name  | Key | Required | Type | Description
- Group Object Id | GroupObjectId | True | string | Id of a group.
- Access Token | accesstoken | True | object | Access token for application.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.DeleteGroup.InvalidGroupObjectId | Group Id is empty.

## Delete User

Input

Name  | Key | Required | Type | Description
- User Id | UserId | True | string | Id of a User.
- Access Token | accesstoken | True | object | Access token for application.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.DeleteUser.InvalidGroupObjectId, User Id is empty.

## Delete User From Group

Input

Name  | Key | Required | Type | Description
- User Id | UserId | True | string | Id of a User.
- Group Object Id | GroupObjectId | True | string | Id of a group.
- Access Token | accesstoken | True | object | Access token for application.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.DeleteUserFromGroup.InvalidGroupObjectId | Group Id is empty.
- Robomotion.ActiveDirectory.DeleteUserFromGroup.InvalidUserId | User Id is empty.

## Get Group

Input

Name  | Key | Required | Type | Description
- Group Object Id | GroupObjectId | True | string | Id of a group.
- Access Token | accesstoken | True | object | Access token for application.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.GetGroup.InvalidGroupObjectId | Group Id is empty.

## Get User

Input

Name  | Key | Required | Type | Description
- User Id | UserId | True | string | Id of a User.
- Access Token | accesstoken | True | object | Access token for application.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.GetGroup.InvalidUserId | User Id is empty.

## List Group Members

Input

Name  | Key | Required | Type | Description
- Group Object Id | GroupObjectId | True | string | Id of a group.
- Access Token | accesstoken | True | object | Access token for application.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.ListGroupMembers.InvalidGroupObjectId | Group Id is empty.

## Show All Groups

Input

Name  | Key | Required | Type | Description
- Access Token | accesstoken | True | object | Access token for application.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

## Show All Users

Input

Name  | Key | Required | Type | Description
- Access Token | accesstoken | True | object | Access token for application.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

## Update Group

Input

Name  | Key | Required | Type | Description
- Group Object Id | GroupObjectId | True | string | Id of a group.
- Access Token | accesstoken | True | object | Access token for application.
- Editor | - | True  | - | User properties.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.UpdateGroup.InvalidGroupObjectId | Group Id is empty.

## Update User

Input

Name  | Key | Required | Type | Description
- User Id | UserId | True | string | Id of a group.
- Access Token | accesstoken | True | object | Access token for application.
- Editor | - | True  | - | User properties.


Output

Name  | Key | Required | Type | Description
- Result | result | True  | object | Response message for request.

Options

Errors

Code  |  Description
- Robomotion.ActiveDirectory.UpdateUser.InvalidGroupObjectId | User Id is empty.



```bash
go get -u github.com/iancoleman/strcase
```


