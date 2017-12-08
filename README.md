# BootstrapAngularAdmin
基于angular、bootstrap的管理系统

### 原生插件存在的bug
ui-bootstrap-tpls.js 分页器当前分页通过 $location.search()方法查询时始终跳转第一页问题解决办法

      $scope.$watch('totalPages', function(value) {
        setNumPages($scope.$parent, value); // Readonly variable
        if ( $scope.page > value ) {
          $scope.selectPage(value);
        } else {
          ngModelCtrl.$render();
        }
      });
      
      改为：
      
      $scope.$watch('totalPages', function(value) {
        setNumPages($scope.$parent, value); // Readonly variable
        // if ( $scope.page > value ) {
        //   $scope.selectPage(value);
        // } else {
          ngModelCtrl.$render();
        // }
      });
