# gitee图床

#### 一、安装 **node**

- [`node`](https://nodejs.org/zh-cn/) 下载安装

#### 二、安装 **PicgGo-Core**

![20211025105338](https://gitee.com/dikesk/dikesk-tu/raw/master/img/20211025123923.png)

#### 三、安装 **gitee-uploader**及**super-prefix** 插件

- win+R 打开运行命令

- 输入 cmd 回车

```shell
##进入以下目录
cd C:\Users\dikesk\AppData\Roaming\Typora\picgo\win64

##安装gitee插件
.\picgo.exe install gitee-uploader

##自动命名插件
.\picgo.exe install super-prefix
```

#### 四、设置 **gitee-uploader** 插件

```shell
cd C:\Users\dikesk\AppData\Roaming\Typora\picgo\win64

##设置插件
picgo set uploader
```

```yaml
{
  "picBed": {
    "current": "gitee", // 代表当前的上传图床
    "gitee": {
      "repo": "dikesk/dikesk-tu", // 仓库名，格式是 username/reponame 必填
      "branch": "master", // 分支名，默认是 master
      "token": "", // gitee 私人令牌 必填
      "path": "img/", // 自定义存储路径，比如 img/ 建议填
      "customPath": "default",
      "customUrl": ""// 自定义域名（没有自己的域名的话，可以默认为空就行），注意要加http://或者https://
    },
    "uploader": "gitee",
    "transformer": "path"
  },
  "picgoPlugins": {
    "picgo-plugin-gitee-uploader": true,
    "picgo-plugin-super-prefix": true
  },
  "picgo-plugin-gitee-uploader": {
    "lastSync": "2021-10-25 12:39:24"
  },
  "picgo-plugin-super-prefix": {
    "fileFormat": "YYYYMMDDHHmmss"//super-prefix插件配置
  }
}
```
#### 五、设备 **super-prefix** 插件按时间命名

![微信截图_20211025124208](https://gitee.com/dikesk/dikesk-tu/raw/master/img/20211025124334.png)

```yaml
  "picgo-plugin-super-prefix": {
    "fileFormat": "YYYYMMDDHHmmss"//super-prefix插件配置
  }
```

#### 六、设 **gitee-uploader** 插件为启动

```shell
cd C:\Users\dikesk\AppData\Roaming\Typora\picgo\win64

##设为使用
picgo use uploader
```

#### 七、设置 **Typora 图像命令** 参数

![20211025105409](https://gitee.com/dikesk/dikesk-tu/raw/master/img/20211025123600.png)

```shell
C:\Users\dikesk\AppData\Roaming\Typora\picgo\win64\picgo upload
```

