# apigee-gcp-azure-auth-example
This repo shows a sample proxy that can vaildate both Google &amp; Azure AD JWT tokens using Apigee flow conditions.

The default endpoint preflow decodes the JWT token and writes all claims to variables.  Then two VerifyJWT polices with conditions to check the issuer claim of the token decide to either verify a Google or Azure AD JWT token.  

This can be useful in multi-cloud scenarios, where both Google Cloud and Azure tokens should be allowed to be used to call APIs.

## Deploy
To deploy, either zip and import manually into Apigee, or use one of the CLI tools such as [apigeecli](https://github.com/srinandan/apigeecli) or [Sackmesser](https://github.com/apigee/devrel/tree/main/tools/apigee-sackmesser).
