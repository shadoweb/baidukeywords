# baidukeywords
百度关键词排名批量查询

##20201207更新
百度更新了html代码
$preg='/<div\s+class=\"f13\"><a\s+target=\"_blank\"\s+href=\"[^>]+\">[\s\S]*?<\/a><\/div>/i';
原正则修改一下就行.
$preg='/<div\s+class=\"f13[\s\S]*?\"><a\s+target=\"_blank\"\s+href=\"[^>]+\">[\s\S]*?<\/a><\/div>/i';
不过对于百家号的形式,目前没匹配.开始的时候匹配过,后没想好怎么合并.
凑合用吧.
QQ925474725
网址:www.menglei.net/2799/
github的是最新的.网址中是原始的
##20191115更新
多线程版本 indexs.php
单线程版本 index.php

测试说明
在phpstudy2018中,Apache环境可以正常使用
php-5.4.45+Apache
php-7.2.10-nts+Apache 速度快一些.

在phpstudy8.0中,有问题,不知原因.


默认搜索前10页的排名情况
可以自行修改
indexs.php中
第9行for($p = 1;$p <=10;$p++){ 修改数字10

index.php中
if($page > 10){
        $res .= '<tr><td>'.$keyword.'</td><td>0</td><td>5页之外</td></tr>';
        
修改这两行中的数字5即可

因为是通过即时查询百度结果,大概每页要1s左右的时长,具体视服务器性能和带宽影响

所以查询的时候要注意关键词的数量

例如要查询前5页的排名情况

每个词要查5页,每页1s

每个词大概要5s,如果服务器性能好,每词可以大概到1s的时长,具体可以自行测试.



网址中可以填写网址或者是网站绑定的百家号(商家号)名称,视自己的情况决定

因简单的实现功能,未做更多优化.

如用于商业环境,建议自行优化.


分享仅作学习交流,请勿恶意评论和用于非人道主义行为.

且行且珍惜
