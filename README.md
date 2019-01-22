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

  <package id="Microsoft.IdentityModel.Logging" version="5.3.0" targetFramework="net461" />
  <package id="Microsoft.IdentityModel.Protocols" version="5.3.0" targetFramework="net461" />
  <package id="Microsoft.IdentityModel.Protocols.WsFederation" version="5.3.0" targetFramework="net461" />
  <package id="Microsoft.IdentityModel.Tokens" version="5.3.0" targetFramework="net461" />
  <package id="Microsoft.IdentityModel.Tokens.Saml" version="5.3.0" targetFramework="net461" />
  <package id="Microsoft.IdentityModel.Xml" version="5.3.0" targetFramework="net461" />
  <package id="Microsoft.Owin" version="4.0.0" targetFramework="net461" />
  <package id="Microsoft.Owin.Host.SystemWeb" version="4.0.0" targetFramework="net461" />
  <package id="Microsoft.Owin.Security" version="4.0.0" targetFramework="net461" />
  <package id="Microsoft.Owin.Security.ActiveDirectory" version="4.0.0" targetFramework="net461" />
  <package id="Microsoft.Owin.Security.Jwt" version="4.0.0" targetFramework="net461" />
  <package id="Microsoft.Owin.Security.OAuth" version="4.0.0" targetFramework="net461" />
  <package id="System.IdentityModel.Tokens.Jwt" version="5.2.1" targetFramework="net461" />
   <package id="Owin" version="1.0" targetFramework="net461" />
   
  <h1> Authorisation </h1>
  
  Then apply the [authorize] tag wherever you need to restrict usage as shown in the ValuesController.
  
  <h1> Things to Note </h1>
  
  <ul>
  <li> The valid token audiences must match in the calling service when getting the access token, in the Startup.Auth.cs file and
       in Azure Authentication for it to be successful.
  </li>
  </ul>

