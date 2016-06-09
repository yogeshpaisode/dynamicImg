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
                <img src="{{img.path}}" style="width: 50px;height: 50px;"/>{{img.uploadStatus}}....<button ng-click="deleteImg($index, form.images);">Delete</button>
            </div>
            <br>
            <input type="file" file-model="myFile" multiple="" id="file"/>
            <button ng-click="addImg(form);">Add Img</button>
            <br><br>
            <button ng-click="add();">Add</button>
        </div>
        <br><br>

        <div ng-repeat="f in formList">
            Color: <input type="text" value="{{f.color}}" ng-model="f.color"/>
            <br>
            Hex: <input type="text" value="{{f.hex}}" ng-model="f.hex"/>
            <br>
            <div ng-repeat="img in f.images">
                <img src="{{img.path}}" style="width: 50px;height: 50px;"/>..<button ng-click="deleteImg($index, f.images);">Delete</button>
            </div>
            <br>
            <button ng-click="triggerFileBox();">select File</button>
            <button ng-click="addImg(f);">Add Img</button>
            <hr>
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
                                    var url = "http://upchar.esy.es/img/";
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
                                    $scope.addImg = function (formObj) {
                                        imgIndex++;
                                        var obj = {name: $scope.myFile.name, uploadStatus: "Preparing..", path: ""};
                                        var fileObj = $scope.myFile;
                                        formObj.images.push(obj);
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
                                            obj.path = url + obj.name;
                                        }, function errorCallback(response) {
                                            obj.uploadStatus = "Error while Uploading..." + imgIndex;
                                        });
                                    }

                                    $scope.deleteImg = function (index, list) {
                                        list.splice(index, 1);
                                    }
                                    
                                    $scope.triggerFileBox=function (){
                                        $("#file").click();
                                    }

                                }]);
        </script>


    </body>
</html>
