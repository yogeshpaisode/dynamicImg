<!DOCTYPE html>
<!--
To change this license header, choose License Headers in Project Properties.
To change this template file, choose Tools | Templates
and open the template in the editor.
-->
<html>
    <head>
        <title>TODO supply a title</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <script src="https://code.jquery.com/jquery-2.2.4.min.js"></script>
        <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.6/angular.min.js"></script>

    </head>
    <body ng-app="myGIIS" ng-controller="indexCtr">

        <div>
            Color: <input type="text" value="" ng-model="form.color"/>
            <br>
            Hex: <input type="text" value="" ng-model="form.hex"/>
            <br>
            <div ng-repeat="img in form.images">
                {{img}}
            </div>
            <input type="file" file-model="myFile" multiple=""/>
            <button ng-click="addImg();">Add Img</button>
            <br><br>
            <button ng-click="add();">Add</button>
        </div>
        <br><br>

        <div ng-repeat="f in formList">
            Color: <input type="text" value="{{f.color}}" ng-model="f.color"/>
            <br>
            Hex: <input type="text" value="{{f.hex}}" ng-model="f.hex"/>
            <br>
            {{f.images}}
        </div>


        <script>
                    angular.module("myGIIS", [])
                            .directive('fileModel', ['$parse', function ($parse) {
                                    return {
                                        restrict: 'A',
                                        link: function (scope, element, attrs) {
                                            var model = $parse(attrs.fileModel);
                                            var modelSetter = model.assign;

                                            element.bind('change', function () {
                                                scope.$apply(function () {
                                                    modelSetter(scope, element[0].files[0]);
                                                });
                                            });
                                        }
                                    };
                                }])
                            .controller("indexCtr", ["$scope", "$http", function ($scope, $http) {
                                    $scope.formList = [];
                                    $scope.form = {};
                                    var imgIndex = 0;
                                    $scope.form.images = [];

                                    $scope.add = function () {
                                        $scope.formList.push($scope.form);
                                        $scope.form = {};
                                        imgIndex = 0;
                                        $scope.form.images = [];
                                    }
                                    $scope.addImg = function () {
                                        imgIndex++;
                                        var obj = {name: $scope.myFile.name, uploadStatus: "Preparing.."};
                                        var fileObj = $scope.myFile;
                                        $scope.form.images.push(obj);
                                        uploadFile(obj, fileObj);
                                    }
                                    var uploadFile = function (obj, fileObj) {
                                        obj.uploadStatus = "Uploading..." + imgIndex;
                                        var fd = new FormData();
                                        fd.append('image', fileObj);
                                        
                                        $http({
                                            method: 'POST',
                                            url: "http://upchar.esy.es/upload.php",
                                            headers: {'Content-Type': undefined},
                                            data: fd
                                        }).then(function successCallback(response) {
                                            obj.uploadStatus = "Uploaded Successfully..." + imgIndex;
                                        }, function errorCallback(response) {
                                            obj.uploadStatus = "Error while Uploading..." + imgIndex;
                                        });
                                    }
                                }]);
        </script>


    </body>
</html>
