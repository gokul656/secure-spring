# secure-spring

Spring boot developed to handle Role Based Access Control (RBAC) with In-Memory authentication.

To run: `mvn spring-boot:run`

By default the server runs on port `2001`. It has three endpoints, each requiring different Authorities to access the route. 

Since it's just a demo app it doesn't have any special authentication mechanism like JWT or OAUTH. Just add `X-AUTH-HEADER` with the requests to authenticate.

To verify using curl

**USER** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- `curl localhost:2001/user/ping` <br/>
**ADMIN** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- `curl localhost:2001/admin/ping -H "x-auth-header: admin"` <br/>
**MANGER** &nbsp;&nbsp; - `curl localhost:2001/manager/ping -H "x-auth-header: manager"` <br/>
