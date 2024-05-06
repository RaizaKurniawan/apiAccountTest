## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Run the test](#run-the-test)

## General info
Referral Code API Test by MochaJS.
	
## Technologies
Project is created with:
* MochaJS: latest version
* Chai: latest version
* Axios: latest version
	
## Setup
To run this project, install it locally using npm:

```
$ cd /~yourfoldername
$ npm install --save-dev mocha chai axios path properties-reader
$ npm install --save-dev mochawesome
```

```
Create config folder 
Create env.properties file
Add this code to the env file
    devURI = https://your-api-devurl/
    stagURI = https://your-api-stagurl/
    uatURI = https://your-api-uaturl/
    prodURI = https://your-api-produrl/

Create tokens.js file in config folder
Adding token in that file
module.exports = {
    token1: 's0dfdasfsdfdsfdsfds',
    token2: 'sfskjdfksdjflkdsfsflkj'
};

Create headers.js 
Add this code to the file
// config/headers.js

const tokens = require('./tokens');

const getHeaders = () => {
  return {
    'Content-Type': 'application/json',
    'Authorization': `Bearer ${tokens.token1}`
    // Tambahkan header lainnya jika diperlukan
  };
};

module.exports = {
  getHeaders
};
```


## Run the test
To run the test:

```
npx mocha ./test/**/*.js

// run with report
npx mocha ./test/**/*.js --timeout=30000 --reporter mochawesome

```
