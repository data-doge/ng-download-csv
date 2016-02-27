# ng-download-csv

angular service for downloading text/csv content as file from a server, using code from [this stackoverflow post](http://stackoverflow.com/a/20904398)

## install

`npm install --save ng-download-csv`

## usage

```javascript
require('angular')
require('ng-download-csv')

var exampleApp = angular.module('exampleApp', ['ngDownloadCsv'])

exampleApp.controller('exampleController', ['$scope', 'DownloadCSV', function ($scope, DownloadCSV) {

  // downloads a csv with filename 'a-good-title.csv'
  DownloadCSV({
    url: 'http://example.com/api/resource.csv',
    filename: 'a-good-title'
  }).success(function (data, status, headers, config) {
    // on download success ...
  }).error(function (data, status, headers, config) {
    // on download error ...
  })

}])
```
