# win10获得管理员权限

清理电脑文件时，删除文件或者文件夹时会提示：需要管理员权限；

但是网上教程各种各样，而且大多并不能成功获得管理员权限；

在这里教大家一种获得Win10管理员权限的一个简单可行的方法；

## 第一步

需要运行一个注册表文件（以.reg为后缀的文件)，放在桌面直接双击即可。

两种方法获得这个文件

法一：直接去我网盘下载：<https://pan.baidu.com/s/1dG5QOXN> 密码：3ohp

法二：把以下代码写进 .txt的文件里，然后更改为 .reg即可

右键添加管理员权限

```
Windows Registry Editor Version 5.00
[HKEY_CLASSES_ROOT\*\shell\runas]
@="获取管理员所有权"
"NoWorkingDirectory"=""
[HKEY_CLASSES_ROOT\*\shell\runas\command]
@="cmd.exe /c takeown /f \"%1\" && icacls \"%1\" /grant administrators:F"
"IsolatedCommand"="cmd.exe /c takeown /f \"%1\" && icacls \"%1\" /grant administrators:F"
[HKEY_CLASSES_ROOT\exefile\shell\runas2]
@="获取管理员所有权"
"NoWorkingDirectory"=""
[HKEY_CLASSES_ROOT\exefile\shell\runas2\command]
@="cmd.exe /c takeown /f \"%1\" && icacls \"%1\" /grant administrators:F"
"IsolatedCommand"="cmd.exe /c takeown /f \"%1\" && icacls \"%1\" /grant administrators:F"
[HKEY_CLASSES_ROOT\Directory\shell\runas]
@="获取管理员所有权"
"NoWorkingDirectory"=""
[HKEY_CLASSES_ROOT\Directory\shell\runas\command]
@="cmd.exe /c takeown /f \"%1\" /r /d y && icacls \"%1\" /grant administrators:F /t"
"IsolatedCommand"="cmd.exe /c takeown /f \"%1\" /r /d y && icacls \"%1\" /grant administrators:F /t"
```

右键取消管理员权限

```
Windows Registry Editor Version 5.00  
[-HKEY_CLASSES_ROOT\*\shell\runas]  
[-HKEY_CLASSES_ROOT\exefile\shell\runas2]  
[-HKEY_CLASSES_ROOT\Directory\shell\runas]
```

## 第二部

在双击运行 .reg 文件后，右键要删除的文件或文件夹，

点击获取管理员权限（在没有运行.reg文件之前，右键没有这个选项）即可；

### 然后就可对此文件或文件夹进行删除或其他需要管理员权限的操作了