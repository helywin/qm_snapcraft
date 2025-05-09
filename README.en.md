# Description

[中文](README.zh.md) | [English](README.en.md)

Package the QM state machine UI editing tool via snapcraft using Github Actions, enabling it to run on lower versions of Ubuntu.

## Environment Setup

```bash
sudo snap install snapcraft --classic
sudo snap install lxd
```

Add user to the lxd group

```bash
sudo usermod -a -G lxd $USER
```

Log out and log back in

```bash
lxd init
```

Select the default options for all prompts

## Packaging

```bash
git clone https://github.com/helywin/qm_snapcraft.git
cd qm_snapcraft
snapcraft
```

## Installation

```bash
sudo snap install --classic --dangerous ./qm_7.0.1_amd64.snap
```

> [!CAUTION]
> In my testing, after packaging and installing on my own computer, it worked fine. However, when copying and installing on other computers, it failed with the error `cannot extract the snap-name from change: data entry not found`. The specific reason is unknown.

## References

- [snapcraft](https://snapcraft.io/docs/create-a-new-snap)
