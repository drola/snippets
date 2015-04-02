Angular 1.x snippets
====================

jsonIo directive
----------------
Load and save JSON to DOM element. JSON is loaded on initialization and saved back when `json-save` event is emmited. If element has `extend` attribute, existing object in scope is extended instead of being overwritten.

    "use strict";
    angular.module("jsonIo", []).directive("jsonIo", function() {
        return {
            scope: {
              target: '='
            },
            restrict: "EA",
            link: function(scope, elem, attrs, modelCtrl) {
                var data = JSON.parse(elem.html());
                if(elem.is('[extend]')) {
                    $.extend(scope.target, data);
                } else {
                    scope.target = data;
                }
                scope.$on('json-save', function(){
                    elem.text(angular.toJson(scope.target));
                });
            }
        };
    });

