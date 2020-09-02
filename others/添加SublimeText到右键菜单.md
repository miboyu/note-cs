# 添加SublimeText到右键菜单

1. 在Run中运行regedit，打开注册表；

### 为文件添加右键菜单
2. 找到HKEY_CLASSES_ROOT\\*\shell；
3. 右键shell->New->Key，命名为SublimeText3；
4. 右键SublimeText3->New->Key，命名为command；
5. SublimeText3下的Value：

| Name      | Type   | Data                              | Note                         |
| :-------- | :----- | :-------------------------------- | :--------------------------- |
| (Default) | REG_SZ | Edit with Sublime Text 3          | #右键菜单中显示的名称，自由设定 |
| Icon      | REG_SZ | %SublimeText3%\sublime_text.exe,0 | #右键菜单中显示的图标，自由设定 |

6. command下的Value：

| Name       | Type   | Data                                 | Note                            |
| :--------- | :----- | :----------------------------------- | :------------------------------ |
| (Default)	 | REG_SZ | %SublimeText3%\sublime_text.exe "%1" | #注意加引号，防止文件名中的空格问题 |

### 为文件夹添加右键菜单
7. 找到HKEY_CLASSES_ROOT\Directory\shell；
8. 右键shell->New->Key，命名为SublimeText3；
9. 右键SublimeText3->New->Key，命名为command；
10. SublimeText3下的Value：

| Name      | Type   | Data                              | Note                         |
| :-------- | :----- | :-------------------------------- | :--------------------------- |
| (Default) | REG_SZ | Open with Sublime Text 3          | #右键菜单中显示的名称，自由设定 |
| Icon      | REG_SZ | %SublimeText3%\sublime_text.exe,0 | #右键菜单中显示的图标，自由设定 |

11. command下的Value：

| Name       | Type   | Data                                 | Note                            |
| :--------- | :----- | :----------------------------------- | :------------------------------ |
| (Default)	 | REG_SZ | %SublimeText3%\sublime_text.exe "%1" | #注意加引号，防止文件名中的空格问题 |

### 为背景添加右键菜单
12. 找到HKEY_CLASSES_ROOT\Directory\Background\shell；
13. 右键shell->New->Key，命名为SublimeText3；
14. 右键SublimeText3->New->Key，命名为command；
15. SublimeText3下的Value：

| Name      | Type   | Data                              | Note                         |
| :-------- | :----- | :-------------------------------- | :--------------------------- |
| (Default) | REG_SZ | Open in Sublime Text 3            | #右键菜单中显示的名称，自由设定 |
| Icon      | REG_SZ | %SublimeText3%\sublime_text.exe,0 | #右键菜单中显示的图标，自由设定 |

16. command下的Value：

| Name       | Type   | Data                                 | Note                            |
| :--------- | :----- | :----------------------------------- | :------------------------------ |
| (Default)	 | REG_SZ | %SublimeText3%\sublime_text.exe "%1" | #注意加引号，防止文件名中的空格问题 |