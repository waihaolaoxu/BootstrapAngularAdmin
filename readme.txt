1：请将文件放在服务器或本地主机上预览。

例如：把“src”文件在本地的“src”文件夹


看起来像：
"src/css"
"src/fonts"
"src/img"
"src/js"
"src/tpl"
"src/l10n"
"src/index.html"

预览:  http://localhost/src/index.html

2: Documents locate "tpl/docs.html" or "http://localhost/src/index.html#/app/docs"
online: http://flatfull.com/themes/angulr/#/app/docs

3: Use Grunt and Bower

install node.js
go to the app root

>npm install -g grunt-cli
>npm install
>grunt bower-install
>grunt build:dev
>grunt build:dist
>npm start