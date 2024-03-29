# 原型图
<https://org.modao.cc/app/578a54a90fbedcfcb3c12d3f06092a01>
# E-R图
![E-R图](https://github.com/yao123983/PMReader/blob/master/e-r%E5%9B%BE.png)
# 用例图
![用例图](https://github.com/yao123983/PMReader/blob/master/%E7%94%A8%E4%BE%8B%E5%9B%BE.png)
# 流程图
## 基本流
![基本流](https://github.com/yao123983/PMReader/blob/master/%E6%B5%81%E7%A8%8B%E5%9B%BE.png)
## 拓展流
### 注册流程
1.显示注册界面  
2.选择手机号或者第三方登录  
3.用户选择手机号注册并输入手机号，系统校验手机号  
3a.用户选择第三方登录,转第三方登录流程  
4.验证成功，系统生成一个4位验证码，发送验证码到用户手机号，提示用户60秒内输入验证码  
4a.手机号已被注册  
4a.1提示手机号被注册，返回3  
4b.手机号格式错误  
4b.1提示手机号格式错误，返回3  
5.用户输入验证码，系统校验验证码  
5a.用户未按时输入验证码  
5a.1提示用户输入验证码超时，返回4  
5b.用户未输入正确验证码  
5b.1提示用户未输入正确验证码，返回4  
6.用户输入密码，系统校验密码  
7.用户重复输入密码，系统校验密码  
8.验证成功，用户提交注册信息  
8a.用户未输入相同密码  
8a.1提示用户未输入相同密码，返回6或7  
10.系统校验注册信息  
11.转登录流程5  
### 注册需求拓展  
邮箱注册，找回密码  
### 登录流程  
1.显示登录界面  
2.用户选择手机登录或者第三方登录  
3.用户选择手机登录并输入手机号，系统校验手机号  
3a.用户选择第三方登录,转第三方登录流程  
4.验证成功，用户输入密码，系统校验密码，用户数据返回客户端  
4a.手机号未被注册  
4a.1提示手机号无效，返回4  
5.登录成功，页面回退到上一页或主页  
6.用户点击我的页面显示相关数据和退出登录按钮  
7.点击退出  
### 登录需求拓展  
修改密码，实名认证插入，邮箱绑定  
### 购买知识流程  
1.显示知识内容界面  
2.用户选择购买并输入支付密码或者第三方支付，系统校验  
3.校验成功  
3a.用户选择第三方支付,转第三方支付流程  
3b.未登录  
3d.支付密码错误  
3c.账户余额不足  
3d.账户达到限额  
3e.未绑定银行卡  
3f.知识资源错误  
4.转查看知识流程  
### 查看知识需求拓展  
从只有pdf，txt资源到加入音频，视频及其它文字类型  
### 创建知识流程  
1.显示创建知识界面  
2.系统校验用户账户  
3.校验成功，用户输入创建表单，系统校验表单  
3a.未登录  
3b.未实名认证  
4.校验成功，返回我的界面  
### 创建知识需求拓展  
从只能上传pdf，txt资源到加入音频，视频及其它文字类型  
### 查看知识列表需求拓展  
PV+UV热度推送，协同过滤，关键词推荐，名称搜索，类型搜索，深度学习模型  
### 实名认证流程  
1.显示实名认证界面  
2.用户输入身份证号，系统校验身份证号  
3.校验成功，上传身份证正反面，系统识别  
3a.身份证号已被注册，提示是否删除原绑定账户  
4.识别成功  
4a.身份证号与输入号不一致  
4b.身份证图片识别失败  
5.退回前一界面  
### API网关需求拓展  
nginx后端节点健康检查  
### service需求拓展  
LVS，CS架构  
### 数据库需求拓展  
分表，分片，客户端缓存，读写分离，主从集群，集群缓存  
### 整体异常  
1xxx 网关验证出错信息  
2xxx 接口的参数验证失败  
3xxx 接口的参数经过数据库验证时非法的  
4xxx 接口的对数据库的操作出现错误  
### 整体需求拓展  
客户端认证授权  
