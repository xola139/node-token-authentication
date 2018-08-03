# Node Token Authentication
This repo is a fork of [node-token-authentication](https://github.com/scotch-io/node-token-authentication) and was fodified for my use personal.


This repo uses JSON Web Tokens and the [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken) package to implement token based authentication on a simple Node.js API.

This is a starting point to demonstrate the method of authentication by verifying a token using Express route middleware.

## Requirements

- node and npm

## Usage

1. Clone the repo: `git clone git@github.com:scotch-io/node-token-authentication`
2. Install dependencies: `npm install`
3. Change SECRET in `config.js`l
4. Add your own MongoDB database to `config.js`
5. Start the server: `node server.js`
6. Create sample user by visiting: http://localhost:8080/setup


Once everything is set up, we can begin to use our app by creating and verifying tokens.

### Getting a Token



Send a `POST` request to `http://localhost:8080/api/authenticate` with test user parameters as `x-www-form-urlencoded`. 

```
  {
    name: 'usuario',
    password: 'password'
  }
```

### Verifying a Token and Listing Users

- Can use verify with `GET` request to `http://localhost:8080/api/check?token=your_token` with a header parameter of `x-access-token` and the token.

- Send a  `GET` request to get all the register users `http://localhost:8080/api/users` with a header parameter of `x-access-token` and the token .

- You can also update data user with `POST`  `http://localhost:8080/api/user` assign variables in body and parameter of `token`


