## 1. 首先绑定爱快云

## 2. 进入爱快云平台添加docker插件，爱快云链接：[https://yun.ikuai8.com/#/login?redirect=%](https://yun.ikuai8.com/#/login?redirect=%2F)
## 3. 点击【插件应用】-【安装】
<img width="1338" height="357" alt="image" src="https://github.com/user-attachments/assets/8ebc63f5-1c3e-46ca-95a2-351986c6835d" />


## 4. 选择部署好的爱快路由系统，点击【 > 】，再点击【确认】
<img width="864" height="636" alt="image" src="https://github.com/user-attachments/assets/1b5c5923-fa27-4125-857f-3fae8314afe1" />

## 5. 接着回到爱快路由系统界面，刷新页面，就能看到docker功能已经安装成功了，但是进入到这个功能的时候，会发现没有部署存储空间，这时候需要点击【前往设置】
<img width="870" height="555" alt="image" src="https://github.com/user-attachments/assets/6d5b52bb-aaaa-4e14-9c36-97cb0ae4d94c" />
<img width="972" height="435" alt="image" src="https://github.com/user-attachments/assets/4532b096-a34f-49c6-a223-3de83a5c36c5" />

## 6.这里需要注意，建议给docker至少5GB的存储空间，如果你的存储空间允许，就一次性给个20GB也不错
<img width="1355" height="273" alt="image" src="https://github.com/user-attachments/assets/67c563b5-d672-4312-ba88-f2ec1d0281a0" />

## 7. 随意分一下区，但至少是2个分区（因为一个要用来存储系统日志），点击【保存】之后会提示路由重启，点击【重启】就是了

<img width="1308" height="642" alt="image" src="https://github.com/user-attachments/assets/82998065-297d-4ee1-9044-8debdd78f90f" />

## 8.这里绑定业务选择【普通存储】，挂载路径需要是英文的（不能有中文），我这里输入了【docker】，然后点击【确定】
<img width="1332" height="366" alt="image" src="https://github.com/user-attachments/assets/175c81ae-9849-49dd-a39e-894e3337f936" />

## 9. 回到插件管理打开docker把docker服务打开
<img width="1338" height="450" alt="image" src="https://github.com/user-attachments/assets/8e716074-f29a-47f9-b087-f541bec74db7" />


## 10. 点击点击【接口管理】-【添加】
### 如下添加
### 接口名称需要用英文的（不要用中文哦！）
### IPv4地址为172.17.0.0/24
### IPv4网关为172.17.0.1
<img width="648" height="192" alt="image" src="https://github.com/user-attachments/assets/03c92f15-27b8-4f87-a732-db8409af213d" />
<img width="1254" height="537" alt="image" src="https://github.com/user-attachments/assets/5f0e64c7-da0c-4095-89ca-6977504b30ed" />

## 11. 在镜像管理里面点几添加-镜像库下载搜素（ginuerzh/gost）然后下载
<img width="2505" height="957" alt="image" src="https://github.com/user-attachments/assets/e9c5f5c8-d950-46e2-b09a-31fba385bf13" />

## 12.回到docker服务页面，在容器列表点击添加
<img width="2538" height="825" alt="image" src="https://github.com/user-attachments/assets/ad934de2-96c6-4753-8a9f-eee2022b940b" />
容器名称：自定义
内存占用：64
镜像文件：ginuerzh/gost:latest
网络接口：选择接口管理里面创建的接口
IPv4地址：留空
IPv6地址：留空
开机自启动：打勾

### A高级设置内
### A启动命令为`-L=socks5://ddvpn:dd123@:1080?udp=true`
### A注：dvpn:dd123是用户名密码，1080是服务端口，可自行做修改
```
function test() {
  console.log("This code will have a copy button to the right of it");
}
```



