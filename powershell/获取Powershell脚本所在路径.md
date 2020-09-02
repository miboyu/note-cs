# 获取Powershell脚本所在路径

```powershell
$location = Split-Path -Parent $MyInvocation.MyCommand.Definition
```