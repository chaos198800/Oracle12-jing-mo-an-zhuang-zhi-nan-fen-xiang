# Oracle 12 静默安装指南

本仓库提供了一个资源文件，用于在CentOS和麒麟系统上进行Oracle 12的静默安装。该安装方法无需任何用户干预，直接按默认设置进行安装，适用于自动化部署和批量安装场景。

## 资源文件内容

- **Oracle 12 安装包**：包含Oracle 12的安装文件，适用于CentOS和麒麟系统。
- **依赖包**：包含安装过程中所需的依赖包，确保安装顺利进行。
- **配置文件**：提供静默安装所需的配置文件，简化安装步骤。

## 安装步骤

1. **安装准备**：
   - 关闭防火墙和SELinux。
   - 安装必要的依赖包。

2. **创建用户和组**：
   - 创建oinstall和dba组。
   - 创建oracle用户并设置密码。

3. **修改内核参数**：
   - 编辑`/etc/sysctl.conf`文件，添加必要的内核参数。

4. **修改用户限制**：
   - 编辑`/etc/security/limits.conf`文件，设置oracle用户的资源限制。

5. **创建安装目录**：
   - 创建Oracle安装目录，并设置权限。

6. **配置Oracle用户环境变量**：
   - 编辑`~/.bash_profile`文件，设置Oracle环境变量。

7. **上传并解压安装文件**：
   - 上传Oracle安装文件到指定目录并解压。

8. **复制配置文件并修改权限**：
   - 复制配置文件到指定目录，并修改文件权限。

9. **执行静默安装**：
   - 使用`runInstaller`命令进行静默安装。

10. **执行数据库脚本**：
    - 切换到root用户，执行数据库安装脚本。

11. **配置监听程序**：
    - 使用`netca`命令配置监听程序。

12. **启动监听**：
    - 使用`lsnrctl start`命令启动监听。

13. **静默建库**：
    - 使用`dbca`命令进行静默建库。

## 注意事项

- 安装过程中可能会遇到一些报错，请参考[CSDN博客文章](https://blog.csdn.net/qq_42578459/article/details/126171535)中的解决方案。
- 确保系统满足Oracle 12的硬件和软件要求。

## 贡献

欢迎提交问题和改进建议，帮助完善本仓库的内容。

## 许可证

本仓库内容遵循[CC 4.0 BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)许可证。

## 下载链接

[Oracle12静默安装指南分享](https://pan.quark.cn/s/b9b4cd0aff65)