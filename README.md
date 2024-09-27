# moonlight-qt-loongarch64

在`loongarch64`上编译安装`moonlight`。

## 环境

![image-20240927104350194](https://raw.githubusercontent.com/XiWeiGu/typora/main/image-20240927104350194.png)

## 编译

### 下载源码

```shell
git clone https://github.com/moonlight-stream/moonlight-qt.git
```

### 安装依赖

```shell
sudo apt install ffmpeg gcc
```



```shell
sudo apt install libegl1-mesa-dev libgl1-mesa-dev libopus-dev libsdl2-dev libsdl2-ttf-dev libssl-dev libavcodec-dev libavformat-dev libswscale-dev libva-dev libvdpau-dev libxkbcommon-dev wayland-protocols libdrm-dev
```

```shell
sudo apt install qt6-base-dev qt6-declarative-dev libqt6svg6-dev qml6-module-qtquick-controls qml6-module-qtquick-templates qml6-module-qtquick-layouts qml6-module-qtqml-workerscript qml6-module-qtquick-window qml6-module-qtquick
```

### 构建

```shell
qmake6 moonlight-qt.pro
```

### 编译

```shell
make release
```

## 测试

启动`Moonlight`

```shell
./app/moonlight
```

![11](https://raw.githubusercontent.com/XiWeiGu/typora/main/11.png)

通过测试可以正常连接`Sunshine`，客户端硬件解码也可以开启，暂时未发现明显的问题。

## `TODO`

1. 未在`loongnix`等其它系统上验证；
2. 制作安装包？


