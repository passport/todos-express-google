# todos-express-google-oauth2

This app illustrates how to use [Passport](https://www.passportjs.org/) with
[Express](https://expressjs.com/) to sign users in with [Google](https://www.google.com/).
Use this example as a starting point for your own web applications.

## Quick Start

To run this app, clone the repository and install dependencies:

```bash
$ git clone https://github.com/passport/todos-express-google-oauth2.git
$ cd todos-express-google-oauth2
$ npm install
```

This app requires OAuth 2.0 credentials from Google, which can be obtained by
[setting up](https://developers.google.com/identity/protocols/oauth2/openid-connect#appsetup)
a project in [Google API console](https://console.developers.google.com/apis/).
The redirect URI of the OAuth client should be set to `'http://localhost:3000/oauth2/redirect/accounts.google.com'`.

Once credentials have been obtained, create a `.env` file and add the following
environment variables:

```
GOOGLE_CLIENT_ID={{INSERT_CLIENT_ID_HERE}}
GOOGLE_CLIENT_SECRET={{INSERT_CLIENT_SECRET_HERE}}
```

Start the server.

```bash
$ npm start
```

Navigate to [`http://localhost:3000`](http://localhost:3000).

## Overview

This example illustrates how to use Passport and the [`passport-google-oauth20`](https://www.passportjs.org/packages/passport-google-oauth20/)
strategy within an Express application to sign users in with [Google](https://www.google.com)
via OAuth 2.0.

This app implements the features of a typical [TodoMVC](https://todomvc.com/)
app, and adds sign in functionality.  This app is a traditional web application,
in which all application logic and data persistence is handled on the server.

User interaction is performed via HTML pages and forms, which are rendered via
[EJS](https://ejs.co/) templates and styled with vanilla CSS.  Data is stored in
and queried from a [SQLite](https://www.sqlite.org/) database.

After users sign in, a login session is established and maintained between the
server and the browser with a cookie.  As authenticated users interact with the
app, creating and editing todo items, the login state is restored by
authenticating the session.

## License

[The Unlicense](https://opensource.org/licenses/unlicense)

## Credit

Created by [Jared Hanson](https://www.jaredhanson.me/)
