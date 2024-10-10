@echo off
echo Downloading Visual Studio Code installer...
powershell -Command "Start-BitsTransfer -Source https://update.code.visualstudio.com/latest/win32-x64-user/stable -Destination %temp%\VSCodeSetup.exe"

echo Installing Visual Studio Code...
start /wait %temp%\VSCodeSetup.exe /silent /mergetasks=!runcode

echo Installation completed!
pause
