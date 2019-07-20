# 文字游戏 翻译君 使用说明 2019-06-25


### 文字游戏 翻译君 QQ群 [38552538](https://shang.qq.com/wpa/qunwpa?idkey=750821134ca5569c2215b66c9593df40851d615fe92aa5633af297a6cba96420) [度盘提取码:bb3b](https://pan.baidu.com/s/1qObSVEx6ZijYcia8QKic3w) 
![image](img/2019-07-19-img-000.png)
![image](img/2019-07-19-img-001.png)
![image](img/2019-07-19-img-002.png)
#### 最新消息
```
2019-07-19
百度翻译api更新,限制了api每秒调用次数,多线程不可用(以前用多线程可是很快的)
```
>#### 软件特性:
```
1.文本文件任意支持的语言(见API支持语言列表)翻译成中文(并不局限于ks或scn文件)
2.翻译好的文件编码为utf16le有签名
3.自动识别编码shift-jis和utf8,utf16,gb2312等(utf16be无签名除外)
4.由正则过滤不需要翻译的行,以及其他不需要翻译的内容,精准提取文本
5.调用有道和百度api翻译,腾讯API接口(腾讯API有每秒5次请求限制,暂时无法使用多线程),由于api额度有限,需用户自行申请
6.scn解文本封文本自动处理
7.翻译完成自动打包xp3(可选项)
8.翻译字数统计(实际略多于api实际翻译字数,误差大概10%以内)只精确到翻译行的字数,行内不需要翻译的字忽略不计
9.人名修改系统,通过正则提取游戏内人物"说话"时的名字,请根据翻译参考或游戏人物参考对照修改
10.采用多线程同时翻译多个文件,目前最大支持32个文件同时翻译,效率是以前的单文件的32倍
11.添加制作人信息,会在每次翻译最开始的文本前插入此信息(xxxx制作)这样的文字,仅插入一次
12.文润系统(后期处理文本用,可以将API返回的常见错误加以修正,例如翻译好的文本中有大量的AAAA,AAAA是api返回的翻译结果,但并不是正确的结果,通过文润系统可以将所有文本中的AAAA,全部换成您设定好的BBBB,文润系统尽量让原始字符多的排在最前面)
13.加入自动激活功能,目前只支持支付宝付款后的自动激活
```

>#### 已知BUG:(请尽量避免以下操作)
```
1.待翻译列表内的文件路径如果不同时,会出错.
2.SCN文件和ks文件同时出现在待翻译列表内,会出错.
3.规则全为空时,翻译scn会出错,但不影响最终结果.
```

>#### 使用说明:
```
1.文字游戏_机翻君-->浏览-->选择需要翻译的剧本文件*.ks或*.txt(一定要确认不是utf16be无签名的)*.scn不用管,一键直翻即可
2.翻译完成后替换掉原始的剧本文件*.ks
3.打包进游戏测试
4.人名系统正则表达式例子 (?<=^\[NAME_[MW] n=\").+(?=\"\]\\$) 匹配下句中的 [NAME_W n="xxxx"]\ xxxx部分
```

>#### 翻译api申请:
```
有道申请方法:有道智云-->自然语言翻译-->翻译实例-->创建实例-->名称XX选文本翻译-->应用管理-->我的应用-->创建-->API方式-->绑定刚刚的翻译实例-->记下应用ID和应用密钥并确认已经绑定翻译实例--有道智云给新用户100元,翻译按字数收费
百度申请方法:百度翻译开放平台-->开通通用翻译API-->每个月200万字符免费,超出按字数收费
```

>#### 更新说明
```
1.修复腾讯api设置不能保存的bug
2.更改原来的翻译方向jp-->zhs,改为auto-->zhs,也就是说可以将任意支持的语言(见API支持语言列表)翻译成中文
3.tools下添加xmoeproject/KrkrExtract4.0.1.4解包打包工具----官网 https://github.com/xmoeproject/KrkrExtract
```

>#### 位置说明:
```
KS,所有翻译好的文本和xp3封包位于翻译文件的目录下的\trans_cn_****\目录下
SCN,所有翻译好的文本位于翻译文件的目录下的\trans_cn_****\目录下,所有翻译后生生成的scn和xp3封包位于\trans_cn_test\OutScript\目录下
```

>#### 其他:

##### 新浪博客--http://blog.sina.com.cn/u/1403364340

##### QQ空间--https://user.qzone.qq.com/27001095

##### Git地址--https://sh2288.github.io/krkr_translator
