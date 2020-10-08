# Route Redirect and Authentication for React Components
Simple Route Authentication and Redirect for React's Components that adds an extra layer of security on the front-end with JWT Tokens. 
1. RouteAuthentication can be used for authenticating sensitive components (user profile). If the user has a JWT Token, the requested component is rendered, otherwise a redirect to the Homepage is issued.
2. RouteRedirect can be used for redirecting users after a successful action, for example after obtaining a JWT Token from the back-end after signing up or logging in. Here, the logic is reverted. If the user has no JWT Token, the requested page is rendered (signup or login forms), otherwise a redirect to the Homepage is issues (successful login/signup).

### Using this package

This implementation assumes you are using JWT Tokens stored in sessionStorage under the key `secret_token`. This implementation can of course be changed so that this package works for you.

**Route Redirect**
1. Import the package in your component: `import RouteRedirect from "../RouteRedirect";`
2. Export the component like so: `export default RouteRedirect(RegistrationForm);`

**Route Authentication**
1. Import the package in your component: `import RouteAuthentication from "../RouteAuthentication";`
2. Export the component like so: `export default RouteAuthentication(Profile);`

Note: substitute RegistrationForm and Profile with whatever your Class Component is called.
