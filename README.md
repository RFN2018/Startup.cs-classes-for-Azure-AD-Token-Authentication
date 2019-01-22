# Startup.cs-classes-for-Azure-AD-Token-Authentication
Startup classes for Azure AD Token Authentication

The code in the file demonstrates how to retrospectively add the authentication files into an MVC project in order to validate access 
tokens for an Azure web application

<h1>Classes to Add</h1>
<ul>
   <li>Startup.cs</li>
   <li>Startup.Auth.cs</li>
</ul>

<h1>Dependacies Required</h1>

Refer to the packages.config file for the full list, I've highlighted some in particular below especially the 
'Microsoft.Owin.Host.SystemWeb' package as that isn't explicitely referenced in any of the the files but is neccessary for the 
authorisation process.

<ul>
  <li>"Microsoft.IdentityModel.Logging"</li>
  <li>"Microsoft.IdentityModel.Protocols"</li>
  <li>"Microsoft.IdentityModel.Protocols.WsFederation"</li>
  <li>"Microsoft.IdentityModel.Tokens"</li>
  <li>"Microsoft.IdentityModel.Tokens.Saml"</li>
  <li>"Microsoft.IdentityModel.Xml"</li>
  <li>"Microsoft.Owin" </li>
  <li>"Microsoft.Owin.Host.SystemWeb"</li>
  <li>"Microsoft.Owin.Security"</li>
  <li>"Microsoft.Owin.Security.ActiveDirectory"</li>
  <li>"Microsoft.Owin.Security.Jwt"</li>
  <li>"Microsoft.Owin.Security.OAuth"</li>
  <li>"System.IdentityModel.Tokens.Jwt"</li>
  <li>"Owin"</li>
</ul>
   
  <h1> Authorisation </h1>
  
  Then apply the [authorize] tag wherever you need to restrict usage as shown in the ValuesController.
  
  <h1> Things to Note </h1>
  
  <ul>
  <li> The valid token audiences must match in the calling service when getting the access token, in the Startup.Auth.cs file and
       in Azure Authentication for it to be successful.
  </li>
  </ul>

