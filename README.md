# Azure Active Directory Package



<img src="https://1tr1r26cy6v2ytmxw6y5occe-wpengine.netdna-ssl.com/wp-content/uploads/2021/05/cropped-robomotion-logo.png" height="100" align="right">


<!-- [START usecases] -->

###### About Package

Azure Active Directory (Azure AD) is Microsoft's cloud-based identity and access management service. For an organization, Azure AD helps employees sign up to multiple services and access them anywhere over the cloud with a single set of login credentials.


<!-- [END usecases] -->


### Setup
Before starting build flows you must complete this steps:

- [App Registration](https://docs.microsoft.com/en-us/graph/auth-register-app-v2) 
- [API Permissions](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-permissions-and-consent)
- Getting Client Secret

Each node of Azure Active Directory Package may need different permissions. For example [Create User](https://docs.microsoft.com/en-us/graph/api/user-post-users?view=graph-rest-1.0&tabs=http). See also [here](https://docs.microsoft.com/en-us/graph/auth/auth-concepts#microsoft-graph-permissions) for more information about permissions.
<!-- [START getstarted] -->
### Build Your Simple Flow


![image](https://user-images.githubusercontent.com/74293190/130731015-34248e2e-7fb7-4694-8d2a-06ba7f585f53.png)


To use Azure Active Directory Packages in your flow, you need Connect node and three input parameters (TenantID, ClientId, ClientSecret):

You can find your TenantId and ClientId on your registered application's main page.

To get your client secret you have to follow this steps:

 1. Sign in to [Azure Portal](https://portal.azure.com/).

 2. Go to Azure Active Directory.

 3. From app registrations in Azure AD, select your application.

 4. Select Certificates & secrets.

 5. Select Client secrets -> New client secret.

Provide a description of the secret, and a duration. When done, select Add.

After saving the client secret, the value of the client secret is displayed. Copy this value because you won't be able to retrieve the key later.


![image](https://user-images.githubusercontent.com/74293190/130729871-0b4b9586-1036-4fe8-955b-73005d579266.png)


Here is editor content of Create User node:

```
{
  "accountEnabled": true,
  "displayName": "Robomotion Test",
  "mailNickname": "Robomotion",
  "userPrincipalName": "test@robomotionio.onmicrosoft.com",
  "passwordProfile" : {
    "forceChangePasswordNextSignIn": true,
    "password": "xWwvJ]6NMw+bWH-d"
  }
}
```

![image](https://user-images.githubusercontent.com/74293190/130733041-ef10a7a0-1843-45aa-824c-06a0fcb9d2a3.png)


Note: The application that used in this flow has enough permissions for Create User, see [here](https://docs.microsoft.com/en-us/graph/api/overview?view=graph-rest-1.0) for required permissions for each operation.




<!-- [END faq] -->
