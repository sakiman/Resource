# SGS.OAD.Resource

![](https://img.shields.io/badge/Tool-Resource-orange)
![](https://img.shields.io/badge/Nginx-111?logo=nginx)
![](https://img.shields.io/badge/Mermaid-555?logo=mermaid)
![](https://img.shields.io/badge/Shields.io-555?logo=shieldsdotio)
![](https://img.shields.io/badge/Markdown-555?logo=markdown)

## 目錄

[Nginx](#一鍵啟用或停用-nginx)  

## 一鍵啟用或停用 nginx

For Windows：
將內容另存成 .bat
```bash
chcp 65001
@echo off
set nginx_path=C:\Users\Sankalp_Chang\Downloads\_Python\__Sankalp__\nginx

:: 切換到 Nginx 目錄
cd /d %nginx_path%

:: 檢查 Nginx 是否正在運行
tasklist | findstr nginx.exe >nul
if %ERRORLEVEL%==0 (
    echo Nginx 已在運行中，正在停止服務...
    nginx -s stop
    echo Nginx 已停止！
) else (
    echo Nginx 未在運行中，正在啟動服務...
    start nginx
    echo Nginx 已啟動！
)

pause
```