# 小工具合集
## 1 去除桌面快捷方式小箭头
### 1.1 使用方式
以管理员身份运行.bat文件

### 1.2 实现方法
去除桌面快捷方式小箭头.txt
```
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Icons" /v 29 /d "%systemroot%\system32\imageres.dll,197" /t reg_sz /f
taskkill /f /im explorer.exe
attrib -s -r -h "%userprofile%\AppData\Local\iconcache.db"
del "%userprofile%\AppData\Local\iconcache.db" /f /q
start explorer
pause
```
修改.txt为.bat

### 1.3 参考资料
参考[卡饭网](https://www.kafan.cn/A/jv4z90go3r.html)
