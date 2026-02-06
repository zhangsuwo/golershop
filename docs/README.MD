1、开源版下载地址: a: https://github.com/shsuishang/golershop   b: https://gitee.com/suisung/golershop
2、开源版 和  企业版核心区别有两个：企业版功能更多、性能更高
在线文档： https://docs.shopsuite.cn/
安装部署SQL下载地址：https://www.shopsuite.cn/uploads/sql/shopsuite-001.sql

http://106.14.156.6:8080/admin/#/login
后台默认账号:admin
后台默认密码:shopsuite.cn
接口文档：http://106.14.156.6:8080/swagger

Golang 版本演示站：
移动端： https://demo.golershop.cn/h5
PC端： https://demo.golershop.cn/
后台：https://demo.golershop.cn/admin

<!-- 运行 -->
go mod tidy
go run main.go
<!-- 后端打包 -->
cd server && echo "y" | gf build
<!-- 赋权限 -->
chmod +x goleshop
<!-- 配置文件 -->
mkdir manifest/config
mkdir resource/public
<!-- 后台执行 -->
nohup ./goleshop &
<!-- 验证8080端口 -->
netstat -tuln | grep 8080
后端访问http://106.14.156.6:8080/admin
<!-- 编译linux错误 -->
先查看编译报错的地方
gf build --debug
升级报错的包
go list -m github.com/go-pay/gopay
go get -u github.com/go-pay/gopay
升级gf
gf up -a