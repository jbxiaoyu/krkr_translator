#### 准备工具:
 
### 1.解压工具---GARbro和KrkrExtract
### 2.文本编辑器-emeditor
### 3.打包工具---krkrrel



1.解包data.xp3
2.将解包后目录里,所有*.tjs和*.ks文件,用emeditor打开(shift-jis或utf8,utf16),请确保看到的不是乱码,才能转码保存(注意,有些游戏脚本和剧本,有多种编码,例如tjs是shift-jis,而ks是utf编码,这样的需要注意),然后全部转换成utf16LE有签名,emeditor-->文件-->指定编码全部保存
3.机翻工具翻译剧本文件,机翻工具-->浏览-->选择需要翻译的剧本文件*.ks
4.翻译完成后替换掉原始的剧本文件*.ks
5.打包data,打包的所有文件名不能包含"・",如果文件名含有"・",请将"・"全部换成"-",然后,所有脚本tjs或ks中查找含有"・"的文件名的字串,找到后将"・"替换成"-"即可
6.打包好data.xp3后替换原来的data.xp3,进游戏进行测试机翻汉化...快进......
