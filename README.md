#Webuploader For Amazeui  
---  

Webuploader For Amazeui 基于百度webuploader的AMUI上传组件。

- [Webuploader文档](http://fex.baidu.com/webuploader/doc/index.html)

**使用说明：**

1. 获取 Webuploader For Amazeui 


2. 页面先引入Amaze UI的样式和JS文件还有jQuery文件：

3. 最后依次引入webuploader.js和webuploader.css还有AMUIwebuploader.js（`dist` 目录下的 js和css）：

  ```html
  <link rel="stylesheet" href="../dist/amazeui/assets/css/amazeui.min.css"/>
  <script src="../dist/js/webuploader.js"></script>
  <script src="../dist/js/AMUIwebuploader.js"></script>
  ```

4. 在页面任意位置输入示例div则可以快速声明上传组件:

  ```html
  <div data-am-webuploader-simple="{id:'demo', name:'thumb', pick:{id:'#demo'}}"></div>
  ```  
  
**部署事项：**  
组件本身提供快速修改后端参数的选项，考虑到日后的使用建议对文件进行硬写入修改。  
  
打开AMUIwebuploader.js文件（`dist`目录下的js),将文件中server和swf修改为您可以调用的地址。  
  ```js
    // 自行修改为您可以调用的地址。
    server: '../server/fileupload.php',
    // 自行修改为您可以调用的地址
    swf: '../docs/js/Uploader.swf',
  ```
  此外，组件默认提供的上传库不具备用于正式的生产环境中！！
  