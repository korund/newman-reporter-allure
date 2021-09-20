This is a fork of https://github.com/ervirendersingh/newman-reporter-allure

# newman-reporter-allure
A newman reporter for generating nice and clean report using Allure-js framework

## Installation
```console
$ npm install -g @danvargas46/newman-reporter-allure
```

## Added Functionality
This fork includes more information in the results, such as the request and response headers, cookies, etc. Additionally, cleaned up the formatting a bit when displaying JSON entities.

## Usage
To generate Allure results, specify `allure` in Newman's `-r` or `--reporters` option.

```console
$ newman run <Collection> -e <Environment> -r allure
$ newman run <Collection> -e <Environment> -r allure --reporter-allure-export <allure-results-out-dir>
```

## Generating and Serving Allure report

Allure results will be generated under folder "allure-results" in the root location.
Use allure-commandline to serve the report locally.
  ```console
  $ allure serve
  ```
Generate the static report web-application folder using allure-commandline 
 ```console
  $ allure generate --clean
  ```
  Report will be generated under folder "allure-report" in the root location.


![Screenshot1](screenshot1.jpg)
![Screenshot2](screenshot2.jpg)
![Screenshot3](screenshot3.jpg)
![Screenshot4](screenshot4.jpg)