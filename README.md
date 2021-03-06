Password authentication and authorization
=========================================

Simple implementation of a custom password-based auth for web applications.

Can be used with of without server-side sessions.

Uses `sha256` hash by default, different hash function (`bcrypt` etc) may be plugged in.

See direct usage example: [test](https://github.com/wilton-iot/pwdauth/blob/master/test.js), and
a full "server + client" example: [auth](https://github.com/wilton-iot/examples/tree/wilton/auth).

License information
-------------------

This project is released under the [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0).

API
---
1. Client side:
   - createPasswordHash = function(password: String, userId: String)

   - createRequest = function(path: String, userId: String, passwordHash: String, timestamp: String)

2. Server side:
   - authorize = function(loadUser: Function, token: String)

   - authenticate = function(loadUser: Function, createRequest: Function, createToken: Function, request: Object) 

Changelog
---------

**2018-03-04**

 * initial public version
