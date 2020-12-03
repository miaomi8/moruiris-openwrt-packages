# luci-app-adguardhome
复杂的AdGuardHome的openwrt的luci界面

 - 可以管理网页端口
 - luci下载/更新核心版本
 - upx 压缩核心
 - dns重定向
 - 自定义执行文件路径（支持tmp，每次重启后自动下载bin）
 - 自定义配置文件路径
 - 自定义工作路径
 - 自定义运行日志路径
 - gfwlist 定义上游dns服务器
 - 修改网页登陆密码
 - 倒序/正序 查看/删除/备份 每3秒更新显示运行日志
 - 手动修改配置文件(支持yaml编辑器)
 - 使用模板快速配置(没有配置文件时)
#### 已知问题：
 - db数据库不支持放在比较特别的文件系统上比如 overlay data-stk-oo，请修改工作目录，本软件如果检测到overlay会自动ln(软连接)到/tmp，将会导致重启丢失dns数据库
 - AdGuardHome 不支持ipset 设置，在使用ipset的情况下，无法替代dnsmasq只能作为dnsmasq上游存在，如果你想要这个功能就去投票吧<br>
 https://github.com/AdguardTeam/AdGuardHome/issues/1191
 
#### 项目已经基本稳定，有bug欢迎主动反馈


Complex openwrt AdGuardHome luci

 - can manage browser port
 - download/update core in luci
 - compress core with upx
 - redirect dns
 - change bin path
 - change config path
 - change work dir(support tmp,auto redownload after reboot)
 - change runtime log path
 - gfwlist query to specific dns server
 - modify browser login passord
 - Positive/reverse order see/del/backup runtime log which update every 3 second
 - modify config manually(support yaml editor)
 - use template to fast config(when no config file)
#### known issues:
 - db database not support some filesystem such as overlay and data-stk-oo,please modify work dir,if overlay is found,will auto ln (soft link)the dbs to /tmp ,will lost dns database after reboot
 - AdGuardhome not support ipset,when we use ipset ,it can`t be the repacement of dnsmasq but the upstream of dnsmasq ,if you want it,vote for it.<br>
 https://github.com/AdguardTeam/AdGuardHome/issues/1191<br>
#### pic
example in zh-cn:<br>
![example1](https://user-images.githubusercontent.com/22387141/69557384-7698b900-0fe1-11ea-96a6-85786fec06ac.png)
![example2](https://user-images.githubusercontent.com/22387141/69949917-59a63d80-152d-11ea-9a90-3602f533200c.png)
![example3](https://user-images.githubusercontent.com/22387141/69854039-09c43e00-12c3-11ea-8827-7725d295a471.png)
