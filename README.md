# 2021-7-28 平台更新，目前抓包一次最多活一小时，卒
---
## library-njit
## **中签绝缘体！！**
南京工程学院我去图书馆占座抢座
### 截至2021-3-24 22点06分 测试有效 
---
**仅供个人娱乐和学习交流**

**https://github.com/qmppz/igotolibrary 大佬两年前就有反馈问题，至今仍然未解决**

**本人非计算机相关专业，代码写的烂，变量起名不规范等别说嗷，只是积极使用python 解决生活中所遇到的问题，本次解决不早起自动选固定座位**

**TODO  使用两个ID 预约 - 取消预约 - 预约 实现免签到、防举报占固定座位**

**自用就行了**

---
## 操作步骤 本人备考2022考研，时间有限，有偿帮忙配置
### 浪费别人时间是可耻的，来图书馆找我
 
**1. 抓包**

Ios用户安装stream，按照提示安装证书，然后 ios-通用-关于本机-证书信任设置-信任，操作和视频[ios抓包]里面的一样就行了，提取[wechatSESS\_ID] [SERVERID]

Android用户（我的安卓是MIUI12.5需要获取root权限才可安装CA证书，不好演示，我采用的是电脑上使用Fiddler对手机进行抓包参考视频[安卓抓包]）

**2. 修改参数**

随便用个文本软件打开[index.py] 把刚刚获得的[wechatSESS_ID] [SERVERID]，填入到对应位置[两个引号里边]  

修改你想要的自习室、和座位号[seat_room] [seat_where] [email]等参数  


**3. 接下来部署腾讯云，进行定时任务(选择5min运行一次)**

参考视频[部署腾讯云]，函数名称可以随便起

**4. 保持活跃**

不清楚[SERVERID]的存活时间，第3步设置五分钟一次心跳可以保活不用修改

目前修改一次cookie可以做到连占几天的座位

有新的解决方案我会及时更新，先去复习高数了[狗头]  

---
## 注意

视频太大了，转发给你吧

腾讯云函数中的函数的 index.py 要保持你最新一次的抓包值 

每次在腾讯云中修改完函数的 index.py 内容后 都要重新部署一下--不要忘记部署！

提示微信中打开链接  -重新抓包填入云函数的index.py-部署

腾讯云函数设置5min执行一次

