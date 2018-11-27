# GTASuperESC
一键结束进程或断网，支持多人联机一人按键一起结束进程或断网，做游戏挑战用的，比如GTA5的犯罪之神(首脑)挑战，要求不能死，但有人死后全队迅速关游戏，在上传数据之前关掉游戏，挑战进度就不会清空！用本软件就可以实现其中一人按键四人一起关游戏，不局限于GTA5，其他游戏或软件也可以使用。  
可修改快捷键，按键后操作可以选择结束进程(可设置进程名,支持多进程)、禁用网卡与进程断网，多种网络连接方式，操作简单，一键创建房间(服务器)就能联机！  
This software also supports English, but it is translated by Google, and the translation quality may be poor.  
  
# 官网：https://gtasuperesc.gtxcn.com  
  
软件引用了以下模块：  
精易模块 (源码：http://ec.125.la)  
WebSocketClient (源码：https://bbs.125.la/thread-14039123-1-1.html)  
UPnP模块 (源码：http://www.pudn.com/Download/item/id/2523129.html)  
CryptAPI (源码：https://bbs.125.la/thread-14033539-1-1.html)
若以上地址打不开或不能下载可从这里下载模块及模块源码：https://pan.baidu.com/s/1BF9sCpZbrJ6gpP9eia81Kw  
  
传输封包=```文本_加密c(<body><hash>时间!随机数</hash>传输内容</body><md5>body标签内(包含标签)的MD5</md5>)```  
自动/手动创建房间，使用UDP或TCP传输时都是直接发送传输封包，加密后是字节集类型，不需要转换  
WebSocket是使用workerman-chat聊天室，发送内容就像这样：  
```{"type":"say","to_client_id":"all","to_client_name":"所有人","content":"Base64编码(传输封包)"}```  
一键创建房间的房间号:```?昵称!密码```,普通(手动创建)房间号:```地址:端口!密码```,自动创建房间号:```#混淆并Base64编码后的普通房间号```  
  
The main function of this software is that after multiple people open the software and connect online, one of them presses the hot key, and multiple people perform the end process (close the game) or disable the network card (disconnected).  
GTA Online has a Criminal Mastermind challenge, you can get 10 million after passing!  
Criminal Mastermind: Only professional need apply. This is the ultimate challenge. Complete all 5 Heists in full on hard difficulte, in order, with the same team and with out losing a single life.  
The whole process can't die, which makes this challenge difficult, but if you use this software, when someone dies, press the button quickly, and the person who opens the software will close the game together! As long as four people turn off the game before saving the data, the progress of the challenge will not be reset!  
The software can also be used elsewhere, and the name of the process to be terminated can be modified.  
  
## How to use to do Criminal Mastermind:  
- Open the software and click on "Auto create"  
- (If create fails, please try to get teammates to click "Auto create", if he also fails, please click "Use free server")  
- Copy the given number and send it to your teammates  
- Let teammates open the software, enter the number and connect  
- Done! At this point, any person presses the hotkey and multiple people will quickly close the game together.  
- When someone dies, immediately press the shortcut key, then re-open the game to continue to do the Criminal Mastermind  
  
  
This software has multiple online methods. If one of the teams is a public network IPv4 address, you can use the automatic creation server. The software will automatically establish port mapping through NAT-PMP or UPnP and automatically test whether it is really valid, and then give a number. Others can easily connect by entering this number. The data is transmitted by TCP+UDP or by TCP or UDP.  
If no one has a public network IPv4 address, you can use the free server I provided. When you click the button, it will automatically connect and give a number. Other people can directly connect to this number and connect directly. The data is transmitted through WebSocket. (TCP), the latency may be slightly higher than for an automatically created server because the server is in Japan.  
Network transmissions do simple encryption and anti-replay, and heartbeat packets ensure connection reliability.  
  
In addition, this software can also be used to implement Private Public Lobby with one-click Windows Firewall rules, supporting multiple IP whitelists.  
(But if you run the software without administrator privileges, you will use the pause game process for 10 seconds to implement Private Public Lobby)  
  
This software is open source using the GPL protocol, written in easy language(易语言), and does not reference any closed source libraries.  
But because easy language is not the mainstream programming language, and some people use him to make a lot of malware or game plug-ins because he is very simple.  
Because software files made using easy language are very similar, some anti-virus software incorrectly reports it as malware.
But now I will submit it to Microsoft before it is released, so Windows Defender will not report it as malware.  
  
My English is very poor, even the software code is written in Chinese, so most of the English language of the software is translated by Google, and the translation may be very bad.  
Welcome to provide translation improvement feedback.  
Since this software is non-Unicode software, Chinese characters will be garbled on a computer with a Unicode locale other than Chinese. 
If the software displays garbled characters after opening the software, please set the language of the software to English.  
If the software save settings fail or cannot obtain the network card name. Please put the software in the file path of pure English. 
