#

```
var klib = {
    BOM: {
        location: {
            search: {
                _parseToObject: function () {
                    var obj_search = {};
                    var arr_mapList = location.search.split('').splice(1).join('').split('&');
                    for (var i = 0; i < arr_mapList.length; i++) {
                        obj_search[arr_mapList[i].split('=')[0]] = arr_mapList[i].split('=')[1];
                    }
                    return obj_search;
                },
                origin        : window.location.search,
                obj           : this._parseToObject()
            }
        }
    }
};

console.log(klib.BOM.location.search.obj);
```








> Created by kang on 2016/3/3.