# Windows命令：
### 查看最大支持内存：
wmic memphysical get maxcapacity

---
### 修改WIN10桌面图片清晰度：
1. 注册表路径HKEY_CURRENT_USER\Control Panel\Desktop
2. 新建DWORD(32位)值：JPEGImportQuality
3. 数值数据中输入100

---
### Win10激活后，浏览器被劫持的修复方法：
1. 360急救箱扫描系统并重启
2. 360修复浏览器选项
3. 注册表HKEY_LOCAL_MACHINE\Software\Microsoft\Internet Explorer\Main\,修改Default_Page_URL、First Home Page、Start Page,修改注册表需要先关闭360
4. 重置chrome浏览器设置，重新导入书签

---
### 空白处打开PowerShell
1. Ctrl + R 输入regedit进入注册表
2. 找到[HKEY_CLASSES_ROOT\Directory\Background\shell\cmd\command]
3. 修改数据为C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe -NoExit Set-Location "%V",修改前为cmd.exe /s /k pushd "%V"

---
