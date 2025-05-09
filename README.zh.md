# 说明

[中文](README.zh.md) | [English](README.en.md)

使用Github Actions通过snapcraft打包QM状态机UI编辑工具，使得能在低版本的Ubuntu下运行

## 环境搭建

```bash
sudo snap install snapcraft --classic
sudo snap install lxd
```

添加用户到lxd组

```bash
sudo usermod -a -G lxd $USER
```

注销后重新登录

```bash
lxd init
```

选项选择默认选项即可

## 打包

```bash
git clone https://github.com/helywin/qm_snapcraft.git
cd qm_snapcraft
snapcraft
```

## 安装

```bash
sudo snap install --classic --dangerous ./qm_7.0.1_amd64.snap
```

> [!CAUTION]
> 本人测试，自己打包后自己安装运行没问题，复制到其他电脑上安装后会失败，打印`cannot extract the snap-name from change: data entry not found`，具体原因不明

## 参考

- [snapcraft](https://snapcraft.io/docs/create-a-new-snap)