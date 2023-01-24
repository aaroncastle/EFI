# EFI
i9 9900K + ASUS PRIME Z390-A

### 说明

> Mac OS Ventura 以下系统可用
>
> Ventura系统未做适配，后期更新

### 已做适配内容：

> 针对ASUS PRIME Z390-A主板做USB定制
>
> 针对ASUS PRIME Z390-A主板做 i9 9900k CPU 集显定制
>
> 已经多次完成安装测试，所以去掉唧唧歪歪模式，开机及加载和正常苹果电脑一样，只显示Logo

### 用法：

> 将下载的EFI文件解压后将EFI文件内的`BOOT` 和`OC`文件夹复制到U盘内的`EFI`文件夹内即可启用U盘引导安装。
>
> 完成安装后用苹果系统自带的分区工具查看硬盘的EFI分区，命令为
>
> 1. 找到硬盘的EFI分区
>    ```shell
>    diskutil list
>    ```
>
>    ![EFI](https://mdrs.oss-cn-hangzhou.aliyuncs.com/EFI.png)
>
>    我的示例EFI分区为`disk0s1`
>
> 2. 挂载硬盘EFI分区
>    ```shell
>    sudo diskutil mount disk0s1
>    ```
>
>    挂载行为需要权限，输入开机密码（密码输入时不会显示*），然后即可在文件管理器folder中看到EFI文件
>
> 3. 以此方法挂载U盘EFI分区，并将U盘中EFI文件夹的内容复制到硬盘EFI中后，开机就不需要使用U盘引导。
>
> 4. 取消掉EFI的挂载。
>    ```shell
>    diskutil unmount disk0s1
>    ```
>
> 5. 对桌面的U盘右键点`推出`,拔掉U盘，安装完成。

