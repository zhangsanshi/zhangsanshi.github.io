title: "ubuntu下安装wordpress"
date: 2015-03-08 23:24:04
tags: ubuntu
---
##注意点
  教程中绝大多数提及wordpress都是放在var/www下面，很少有说到是放在 var/www/html下面，
  我在安装过程中，一开始是放在var/www下面，发现不成功，后查找发现目录默认是var/www/html，
  当然这个目录是可以改的，在 etc/apache2/sites-enabled下面的文件夹里可以修改
  
{% asset_img apache2-config.png %}  
