---
title: "Linux系统中新磁盘的分区与格式化"
slug: initial-new-disk
date: 2024-10-16T14:33:27+08:00
lastmod: 2024-10-16T14:33:27+08:00
math: true
draft: false
hidden: false
comments: true
readingTime: true
image:
categories:
tags:
toc: true
---

## 磁盘分区与格式化
使用 parted 工具为新硬盘创建GPT分区表。在 parted 交互式界面中，执行以下命令：

```
sudo parted /dev/sda
```
- 在 parted 交互式界面中，执行以下命令：
  - 创建GPT分区表：
    `mklabel gpt`
    创建新分区
    `mkpart primary ext4 0% 100%`
    
  - 退出`parted`
  
    `quit`
  
- 格式化分区
```bash
sudo mkfs.ext4 /dev/sdb1
```
## 磁盘挂载

编辑`/etc/fstab`

```
/dev/sdb1 /mnt/large0 ext4 defaults 0 2
/dev/sda1 /mnt/large1 ext4 defaults 0 2
```

查看已经挂载的硬盘
`df -h`

## 共享硬盘

- 在挂载目录下创建用户目录并修改用户和用户组

```
sudo mkdir /mnt/large0/user
sudo chown group:user /mnt/large0/user
```

- 为当前项目创建文件夹，并创建软连接

```bash
mkdir /mnt/large0/user/project
ln -s /mnt/large0/user/project data/large
```

至此，可以在`data/large`目录中使用新硬盘

## 远程连接

开启smb服务，创建的账号名为`smb_user`，可以凭此账号通过445端口连接smb远程文件夹。

```bash
sudo apt install samba
sudo vi /etc/samba/smb.conf
sudo smbpasswd -a smb_user
sudo systemctl restart smbd
```

```conf
[shared_1]
path = /mnt/large1/user
available = yes
valid users = smb_user
read only = no
browsable = yes
public = yes
writable = yes
```

需要注意权限，smb_user只给user使用，因为smb_user账号可以修改目录`/mnt/large1/user`下所有文件。

路径`//10.70.181.65/shared_1`可以连接上用户`/mnt/large1/user`文件夹，
