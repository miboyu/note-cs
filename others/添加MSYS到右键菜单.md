# 添加MSYS到右键菜单

1. 在Run中运行regedit，打开注册表；
2. 找到HKEY_CURRENT_USER\Software\Classes\Directory\Background\shell;
3. 右键shell->New->Key，命名为MSYS2；
4. 右键MSYS2->New->Key，命名为command；
5. MSYS2下的Value：

| Name      | Type   | Data             | Note                         |
| :-------- | :----- | :--------------- | :--------------------------- |
| (Default) | REG_SZ | MSYS2 Here       | #右键菜单中显示的名称，自由设定 |
| Icon      | REG_SZ | %MSYS%\msys2.ico | #右键菜单中显示的图标，自由设定 |

6. command下的Value：

| Name       | Type      | Data                                       |
| :--------- | :-------- | :----------------------------------------- |
| (Default)	 | REG_SZ	 | "%MSYS%\usr\bin\mintty.exe" "-i/msys2.ico" |

*注意双引号，前部分为 mintty 命令所在位置，后面部分指定打开后的窗口图标，注意 -i 后无空格* 