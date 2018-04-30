##<?php
header("Access-Control-Allow-Origin: *");
header("Content-Type: application/json");

$cnx = new mysqli("servername","sername","password","db_name");

$result = $cnx->query("SELECT * FROM Skillz");

while($rs = $result->fetch_array(MYSQLI_ASSOC)) {
  $rows[]=$rs;
  }
$outp = '{"obj":'.json_encode($rows).'}';
$cnx->close();
  
echo($outp);
##?>


# Ag6

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.7.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
