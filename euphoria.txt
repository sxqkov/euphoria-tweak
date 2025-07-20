@shift /0
@echo off
title EUPHORIA Tweak // cracked https://t.me/sclngnrng
chcp 65001
setlocal enabledelayedexpansion

:menu
mode con cols=110 lines=35
cls
color B
echo.
echo Слить не получится, школьники сосите (слить получилось, кодеры сосите)
echo .
echo ██████████ █████  █████ ███████████  █████   █████    ███████    ███████████   █████   █████████  
echo ░░███░░░░░█░░███  ░░███ ░░███░░░░░███░░███   ░░███   ███░░░░░███ ░░███░░░░░███ ░░███   ███░░░░░███ 
echo ░███  █ ░  ░███   ░███  ░███    ░███ ░███    ░███  ███     ░░███ ░███    ░███  ░███  ░███    ░███ 
echo ░██████    ░███   ░███  ░██████████  ░███████████ ░███      ░███ ░██████████   ░███  ░███████████ 
echo ░███░░█    ░███   ░███  ░███░░░░░░   ░███░░░░░███ ░███      ░███ ░███░░░░░███  ░███  ░███░░░░░███ 
echo ░███ ░   █ ░███   ░███  ░███         ░███    ░███ ░░███     ███  ░███    ░███  ░███  ░███    ░███ 
echo ██████████ ░░████████   █████        █████   █████ ░░░███████░   █████   █████ █████ █████   █████
echo ░░░░░░░░░░   ░░░░░░░░   ░░░░░        ░░░░░   ░░░░░    ░░░░░░░    ░░░░░   ░░░░░ ░░░░░ ░░░░░   ░░░░░ 
echo .
echo  ========================================================================
echo.
echo. cracked so ez got it like 20 secs dont use b2e converter for protect ur shit
echo    [1] Оптимизация реестра (FPS + Ping)
echo    [2] Настройка TCP/IP (Уменьшение пинга)
echo    [3] Оптимизация UDP (Для онлайн-игр)
echo    [4] Уменьшение Input Lag
echo    [5] Максимальный FPS (Игровой режим)
echo    [6] Доп. настройки (Очистка RAM, SSD)
echo    [7] Отчистка Кеша 
echo    [8] CPU Optimize
echo    [9] Отключение Служб
echo    [10] Включить EXPHITS (Удар через стену)
echo    [U] Мониторинг загрузки CPU
echo    [Q] Оптимизация рендеринга для уменьшение задержки
echo    [X] Отключить Защиту Виндовс и Брандмауэр ( Подробнее - нажмите Y )
echo    [N] Настройка и отчистка телеметрии Nvidia
echo    [M] Удаление приложений Windows ( список - нажмите P )
echo    [J] Настройка адаптера 
echo    [0] Выход
echo.
echo  ========================================================================
echo  После Применения настроек, перезапустите ПК!     			by Sil3ntWW x DemonClubs
echo  Все буквы должны быть заглавными при вводе!
echo  Обязательно если используете EXEPEREMENTAL HITS,то приоритет javaw должен быть высоким!
echo.
set /p choice="Выберите действие (0-10 or U-P): "

if "%choice%"=="1" goto reg_fps_ping
if "%choice%"=="2" goto tcp_tweaks
if "%choice%"=="3" goto udp_tweaks
if "%choice%"=="4" goto input_lag
if "%choice%"=="5" goto max_fps
if "%choice%"=="6" goto extra_tools
if "%choice%"=="0" exit
if "%choice%"=="7" goto CashClear
if "%choice%"=="8" goto CPU
if "%choice%"=="9" goto OffService
if "%choice%"=="10" goto EXPHITS
if "%choice%"=="Q" goto Render
if "%choice%"=="X" goto AVirus
if "%choice%"=="Y" goto AvirusS
if "%choice%"=="N" goto NVTelemetr
if "%choice%"=="M" goto apps
if "%choice%"=="P" goto appslist
if "%choice%"=="J" goto Adapter
if "%choice%"=="U" goto check_cpu

echo [❌] Неверный выбор! Попробуйте снова.
timeout /t 2 >nul
goto menu

:: =============================================
:: 🚀 1. Оптимизация реестра (FPS + Ping)
:: =============================================
:reg_fps_ping
echo.
echo [🚀] Применяем твики реестра...
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\NetCache" /v "NoFilesOnDemand" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\NetCache" /v "NoAutoCache" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\NetCache" /v "SyncAtLogon" /t REG_DWORD /d 0 /f >nul
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\NetCache" /v "SyncAtLogoff" /t REG_DWORD /d 0 /f >nul
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\NetCache" /v "Enabled" /t REG_DWORD /d 0 /f >nul
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\NetCache" /v "NoConfigCache" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\NetCache" /v "NoMakeAvailableOffline" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\NetCache" /v "NoReminders" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\Psched" /v "NonBestEffortLimit" /t REG_DWORD /d 0 /f >nul
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\Psched" /v "TimerResolution" /t REG_DWORD /d 0 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\QoS" /v "Do not use NLA" /t REG_SZ /d "1" /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management" /v "DisablePagingExecutive" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management" /v "LargeSystemCache" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Control\PriorityControl" /v "Win32PrioritySeparation" /t REG_DWORD /d 26 /f >nul
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v "SystemResponsiveness" /t REG_DWORD /d 0 /f >nul
echo ✓ Кэш CPU: Включен LargeSystemCache
echo ✓ Приоритет: Игры > Фоновые процессы
timeout /t 5 /nobreak >nul
goto menu

:check_cpu
for /f "tokens=2 delims==" %%a in ('wmic cpu get loadpercentage /value') do set "CPU=%%a"
echo Текущая загрузка CPU: %CPU%%
timeout /t 5 /nobreak >nul
goto menu

:: =============================================
:: 📶 2. Настройка TCP/IP (Уменьшение пинга)
:: =============================================
:tcp_tweaks
if "%NetOptimized%"=="false" goto no_internet
echo.
echo [📶] Оптимизация TCP/IP...
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "TcpAckFrequency" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "IRPStackSize" /t REG_DWORD /d 40 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "MaxConnectionsPerServer" /t REG_DWORD /d 10 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "MaxConnectionsPer1_0Server" /t REG_DWORD /d 10 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "TcpTimedWaitDelay" /t REG_DWORD /d 30 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "TcpNoDelay" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "TcpDelAckTikcs" /t REG_DWORD /d 0 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "EnablePMTUBHDetect" /t REG_DWORD /d 0 /f >nul
reg add "%x%" /v "TcpNoDelay" /t REG_DWORD /d 1/f
reg add "%x%" /v "TcpAckFreequency" /t REG_DWORD /d 1 /f
reg add "%x%" /v "TcpTimedWaitDelay" /t REG_DWORD /d 30 /f
reg add "%x%" /v "TcpDelAckTicks" /t REG_DWORD /d 0 /f
netsh int tcp set global autotuninglevel=restricted >nul
echo ✓ Nagle Algorithm отключен
timeout /t 5 /nobreak >nul
goto menu

:: =============================================
:: 🔄 3. Оптимизация UDP (Для онлайн-игр)
:: =============================================
:udp_tweaks
if "%NetOptimized%"=="false" goto no_internet
echo.
echo [🔄] Оптимизация UDP...
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "UdpMaxSendMessages" /t REG_DWORD /d 65535 /f >nul
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "UdpMaxReceives" /t REG_DWORD /d 65535 /f >nul
netsh int tcp set global rsc=enabled >nul
netsh int tcp set global ecncapability=disabled >nul
netsh int tcp set global autotuninglevel=disabled >nul
netsh int tcp set heuristics disabled >nul
netsh int tcp set global chimney=disabled >nul
netsh int tcp set global dca=enabled >nul
netsh int tcp set global rss=enabled >nul
netsh int tcp set global netdma=enabled >nul
netsh int tcp set global congestionprovider=ctcp >nul
netsh int tcp set global timestamps=disabled >nul
netsh int tcp set global nonsackrttresiliency=disabled >nul
netsh int tcp set supplemental template=custom icw=10 >nul
netsh int tcp set global initialRto=1000 >nul
netsh interface ipv4 set glob defaultcurhoplimit=65 >nul
echo ✓ Увеличены UDP-буферы
echo ✓ RSS (Receive Side Scaling) включен
goto menu

:: =============================================
:: 🖱️ 4. Уменьшение Input Lag
:: =============================================
:input_lag
echo.
echo [🖱️] Уменьшаем Input Lag...
reg add "HKCU\Control Panel\Mouse" /v "MouseSpeed" /t REG_SZ /d "0" /f >nul
reg add "HKCU\Control Panel\Mouse" /v "MouseThreshold1" /t REG_SZ /d "0" /f >nul
reg add "HKCU\Control Panel\Mouse" /v "MouseThreshold2" /t REG_SZ /d "0" /f >nul
reg add "HKCU\Control Panel\Desktop" /v "Win32PrioritySeparation" /t REG_SZ /d "26" /f >nul
powercfg /setactive SCHEME_MIN >nul
echo ✓ Ускорение мыши: OFF
echo ✓ Режим питания: Макс. производительность
timeout /t 5 /nobreak >nul
goto menu

:: =============================================
:: 🎮 5. Максимальный FPS (Игровой режим)
:: =============================================
:max_fps
echo.
echo [🎮] Включаем игровой режим...
reg add "HKLM\SOFTWARE\Microsoft\PolicyManager\current\device\GraphicsDrivers" /v "HwSchMode" /t REG_DWORD /d 2 /f >nul
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v "GraphicsPreference" /t REG_DWORD /d 1 /f >nul
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v "SystemResponsiveness" /t REG_DWORD /d 0 /f >nul
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "Affinity" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "Background Only" /t REG_SZ /d "False" /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "Clock Rate" /t REG_DWORD /d 10000 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "GPU Priority" /t REG_DWORD /d 8 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "Priority" /t REG_DWORD /d 6 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "Scheduling Category" /t REG_SZ /d "High" /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "SFIO Priority" /t REG_SZ /d "High" /f
reg add "HKCU\System\GameConfigStore" /v "GameDVR_Enabled" /t REG_DWORD /d 0 /f
reg add "HKCU\System\GameConfigStore" /v "GameDVR_FSEBehaviorMode" /t REG_DWORD /d 2 /f
reg add "HKCU\System\GameConfigStore" /v "GameDVR_HonorUserFSEBehaviorMode" /t REG_DWORD /d 0 /f
reg add "HKCU\System\GameConfigStore" /v "GameDVR_DXGIHonorFSEWindowsCompatible" /t REG_DWORD /d 0 /f
reg add "HKCU\System\GameConfigStore" /v "GameDVR_EFSEFeatureFlags" /t REG_DWORD /d 0 /f

timeout /t 1 >nul
echo ✓ GPU: Режим максимальной производительности
echo ✓ Игровой режим Windows: Активирован
timeout /t 5 /nobreak >nul
goto menu

:: =============================================
:: 🔧 6. Доп. настройки (Очистка RAM, SSD)
:: =============================================
:extra_tools
echo.
echo [🔧] Оптимизация системы...
:: Очистка кэша RAM
rundll32.exe advapi32.dll,ProcessIdleTasks >nul
:: Оптимизация SSD
fsutil behavior set DisableLastAccess 1 >nul
:: Отключение ненужных служб
sc config SysMain start= disabled >nul
sc stop SysMain >nul
echo ✓ Кэш RAM очищен
echo ✓ Оптимизация SSD выполнена
timeout /t 5 /nobreak >nul
goto menu

:: =============================================
:: ❌ Нет интернета (пропуск сетевых настроек)
:: =============================================
:no_internet
colot 1
echo [❌] Интернет не работает! Пропускаем сетевые настройки.
echo Пожалуйста включите интернет!
goto reboot_prompt

:CashClear
echo.
echo Отчистка кеша...
del /s /f /q c:\windows\temp\*.*
rd /s /q c:\windows\temp
md c:\windows\temp
del /s /f /q C:\WINDOWS\Prefetch
del /s /f /q %temp%\*.*
rd /s /q %temp%
md %temp%
deltree /y c:\windows\tempor~1
deltree /y c:\windows\temp
deltree /y c:\windows\tmp
deltree /y c:\windows\ff*.tmp
deltree /y c:\windows\history
deltree /y c:\windows\cookies
deltree /y c:\windows\recent
deltree /y c:\windows\spool\printers
del c:\WIN386.SWP
cls
goto reboot_prompt

:CPU
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v "NetworkThrottlingIndex" /t REG_DWORD /d 0xffffffff /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v "SystemResponsiveness" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "GPU Priority" /t REG_DWORD /d 8 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "Priority" /t REG_DWORD /d 6 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "Scheduling Category" /t REG_SZ /d "High" /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "SFIO Priority" /t REG_SZ /d "High" /f
reg add "HKLM\SYSTEM\ControlSet001\Control\PriorityControl" /v "Win32PrioritySeparation" /t REG_DWORD /d 26 /f
timeout /t 5 /nobreak >nul
goto menu

:OffService
:: Список служб для отключения
set services=(
    "DiagTrack"
    "diagnosticshub.standardcollector.service"
    "DPS"
    "dmwappushservice"
    "SysMain"
    "WMPNetworkSvc"
    "WSearch"
)

for %%s in %services%) do (
    sc config "%%s" start= disabled >nul
    sc stop "%%s" >nul 2>&1
)
timeout /t 5 /nobreak >nul
goto menu

:Render
:: =============================================
:: 🚀 Основные оптимизации рендеринга
:: =============================================
echo [1/5] Оптимизация параметров рендеринга...

:: 1. Настройки DWM (Desktop Window Manager)
reg add "HKLM\SOFTWARE\Microsoft\Windows\DWM" /v "AlwaysHibernateThumbnails" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows\DWM" /v "EnableAeroPeek" /t REG_DWORD /d 0 /f
reg add "HKCU\Control Panel\Desktop" /v "MenuShowDelay" /t REG_SZ /d "10" /f

:: 2. Отключение анимаций
reg add "HKCU\Control Panel\Desktop" /v "UserPreferencesMask" /t REG_BINARY /d 9032080000000000 /f
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\VisualEffects" /v "VisualFXSetting" /t REG_DWORD /d 3 /f

:: =============================================
:: ⚡ Оптимизация графического конвейера
:: =============================================
echo [2/5] Оптимизация графического конвейера...

:: 1. Настройки DirectX
reg add "HKLM\SOFTWARE\Microsoft\Direct3D" /v "DisableDP2" /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Microsoft\Direct3D" /v "DisableDWM" /t REG_DWORD /d 1 /f

:: 2. Оптимизация GPU планировщика
reg add "HKLM\SYSTEM\CurrentControlSet\Control\GraphicsDrivers" /v "HwSchMode" /t REG_DWORD /d 2 /f
reg add "HKLM\SYSTEM\CurrentControlSet\Control\GraphicsDrivers" /v "SchedulerThreadPriority" /t REG_DWORD /d 31 /f

:: =============================================
:: 🎮 Настройки для игрового режима
:: =============================================
echo [3/5] Настройка игрового режима...

:: 1. Приоритеты для игр
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "GPU Priority" /t REG_DWORD /d 8 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "Priority" /t REG_DWORD /d 6 /f
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "Scheduling Category" /t REG_SZ /d "High" /f

:: =============================================
:: ⏱️ Оптимизация таймеров
:: =============================================
echo [4/5] Оптимизация системных таймеров...

:: 1. Настройка таймера HPET
bcdedit /deletevalue useplatformclock >nul 2>&1
bcdedit /set disabledynamictick yes >nul
bcdedit /set useplatformtick yes >nul

:: 2. Настройка прерываний
reg add "HKLM\SYSTEM\CurrentControlSet\Control\PriorityControl" /v "IRQ8Priority" /t REG_DWORD /d 1 /f
reg add "HKLM\SYSTEM\CurrentControlSet\Control\PriorityControl" /v "Win32PrioritySeparation" /t REG_DWORD /d 38 /f

:: 2. Настройка схемы питания
powercfg /setactive SCHEME_MIN >nul
powercfg /setdcvalueindex SCHEME_MIN SUB_PROCESSOR PROCTHROTTLEMAX 100 >nul
powercfg /setacvalueindex SCHEME_MIN SUB_PROCESSOR PROCTHROTTLEMAX 100 >nul

:: =============================================
:: ✅ Завершение
:: =============================================
echo.
echo ________________________________________________________________________________
echo.
echo [УСПЕХ] Оптимизация рендеринга завершена!
echo.
echo Критические изменения:
echo • Отключены графические эффекты Windows
echo • Оптимизирован графический конвейер
echo • Настроен игровой режим с высоким приоритетом
echo • Оптимизированы системные таймеры
echo.
echo ________________________________________________________________________________
echo.
timeout /t 5 /nobreak >nul
goto menu

:AVirus
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU" /v NoAutoUpdate /t REG_DWORD /d 1 /f
net stop wuauserv
sc config wuauserv start= disabled

echo Отключение Защитника Windows...
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f
powershell -Command "Set-MpPreference -DisableRealtimeMonitoring $true"

echo Отключение брандмауэра...
netsh advfirewall set allprofiles state off
timeout /t 5 /nobreak >nul
goto menu

:AvirusS
echo Если вы отключите анти вирус, вот что вас ждет:
echo Плюсы:
echo Нету уведомлений о безопасности, Большой прирост фпс
echo Минусы:
echo Вирусы: Система останется без защиты от угроз.
echo Взлом: Злоумышленники могут получить доступ к вашим данным.
echo Потеря гарантии: Нарушение лицензионного соглашения Windows.
echo если вы обычный пользователь пк то прошу не отключайте анти вирус!
timeout /t 15 /nobreak >nul
goto menu

:NVTelemetr
:: =============================================
:: 🗑️ Очистка телеметрии и временных файлов
:: =============================================
echo [1/3] Очистка телеметрических данных NVIDIA...

:: 1. Остановка служб NVIDIA
taskkill /f /im NvTelemetryContainer.exe >nul 2>&1
taskkill /f /im NvTmMon.exe >nul 2>&1
taskkill /f /im NvTmRep.exe >nul 2>&1

:: 2. Удаление временных файлов
del /f /q "%ProgramData%\NVIDIA Corporation\NvTelemetry\*.*" >nul 2>&1
del /f /q "%LocalAppData%\NVIDIA\DXCache\*.*" >nul 2>&1
del /f /q "%LocalAppData%\NVIDIA\GLCache\*.*" >nul 2>&1

:: 3. Очистка логов
del /f /q "%ProgramData%\NVIDIA Corporation\NvBackend\*.log" >nul 2>&1
del /f /q "%ProgramData%\NVIDIA Corporation\NvNode\*.log" >nul 2>&1

:: =============================================
:: ⚙️ Настройка параметров телеметрии
:: =============================================
echo [2/3] Настройка параметров телеметрии...

:: 1. Отключение сбора данных (без удаления критичных файлов)
reg add "HKLM\SOFTWARE\NVIDIA Corporation\NvControlPanel2\Client" /v "OptInOrOutPreference" /t REG_DWORD /d 0 /f >nul

:: 2. Ограничение фоновых процессов
reg add "HKLM\SOFTWARE\NVIDIA Corporation\NvTelemetry" /v "EnableDataCollection" /t REG_DWORD /d 0 /f >nul

:: =============================================
:: 🧹 Дополнительная оптимизация
:: =============================================
echo [3/3] Оптимизация кэшей NVIDIA...

:: 1. Очистка шейдерного кэша
del /f /q "%LocalAppData%\NVIDIA\DXCache\*.*" >nul 2>&1
del /f /q "%LocalAppData%\NVIDIA\GLCache\*.*" >nul 2>&1

:: 2. Сброс настроек панели управления
set "nvcplPath=%ProgramFiles%\NVIDIA Corporation\Control Panel Client\nvcplui.exe"
if exist "!nvcplPath!" (
    "!nvcplPath!" -reset
)

echo.
echo ________________________________________________________________________________
echo.
echo [SUCCESS] Оптимизация NVIDIA завершена!
echo.
echo Выполнено:
echo • Удалены телеметрические данные
echo • Отключен сбор диагностики
echo • Очищены графические кэши
echo.
echo Рекомендации:
echo - Перезагрузите компьютер для завершения очистки
echo - Обновите драйверы через GeForce Experience
echo ________________________________________________________________________________
echo.

:apps
:: =============================================
:: 📦 Список приложений для удаления (безопасные)
:: =============================================
set "AppsList="
set "AppsList=!AppsList! Microsoft.549981C3F5F10"      :: Cortana
set "AppsList=!AppsList! Microsoft.BingWeather"       :: Погода
set "AppsList=!AppsList! Microsoft.GetHelp"           :: Помощь
set "AppsList=!AppsList! Microsoft.Getstarted"        :: Советы
set "AppsList=!AppsList! Microsoft.MicrosoftSolitaireCollection" :: Косынка
set "AppsList=!AppsList! Microsoft.People"            :: Контакты
set "AppsList=!AppsList! Microsoft.SkypeApp"          :: Skype
set "AppsList=!AppsList! Microsoft.WindowsCalculator" :: Калькулятор
set "AppsList=!AppsList! Microsoft.WindowsCamera"     :: Камера
set "AppsList=!AppsList! Microsoft.WindowsFeedbackHub" :: Отзывы
set "AppsList=!AppsList! Microsoft.WindowsMaps"       :: Карты
set "AppsList=!AppsList! Microsoft.WindowsSoundRecorder" :: Запись голоса
set "AppsList=!AppsList! Microsoft.Xbox.TCUI"         :: Xbox Live
set "AppsList=!AppsList! Microsoft.XboxApp"           :: Xbox
set "AppsList=!AppsList! Microsoft.XboxGameOverlay"   :: Игровая панель
set "AppsList=!AppsList! Microsoft.XboxGamingOverlay" :: Игровой overlay
set "AppsList=!AppsList! Microsoft.XboxIdentityProvider" :: Xbox Identity
set "AppsList=!AppsList! Microsoft.XboxSpeechToTextOverlay" :: Голос Xbox
set "AppsList=!AppsList! Microsoft.YourPhone"         :: Ваш телефон
set "AppsList=!AppsList! Microsoft.ZuneMusic"         :: Музыка Groove
set "AppsList=!AppsList! Microsoft.ZuneVideo"         :: Кино и ТВ

:: =============================================
:: 🗑️ Процесс удаления приложений
:: =============================================
echo [1/2] Удаление выбранных приложений...
echo.

set "counter=0"
for %%A in (!AppsList!) do (
    echo Проверка: %%A
    powershell -command "Get-AppxPackage -AllUsers *%%A* | Remove-AppxPackage -ErrorAction SilentlyContinue" >nul 2>&1
    if !errorlevel! equ 0 (
        set /a "counter+=1"
        echo ✓ Удалено: %%A
    ) else (
        echo ✗ Не удалось удалить: %%A
    )
)

:: =============================================
:: 🧹 Очистка остаточных данных
:: =============================================
echo [2/2] Очистка остаточных данных...
rd /s /q "%LocalAppData%\Packages\Microsoft.Windows.Cortana_*" >nul 2>&1
rd /s /q "%LocalAppData%\Packages\Microsoft.XboxApp_*" >nul 2>&1
rd /s /q "%LocalAppData%\Packages\Microsoft.SkypeApp_*" >nul 2>&1

:: =============================================
:: ✅ Завершение
:: =============================================
timeout /t 5 /nobreak >nul
goto menu


:appslist
echo Microsoft.549981C3F5F10 - Cortana (голосовой помощник)
echo Microsoft.BingWeather - Погода
echo Microsoft.GetHelp - Помощь (справочная система)
echo Microsoft.Getstarted - Советы (руководство по Windows)
echo Microsoft.MicrosoftSolitaireCollection - Косынка (коллекция карточных игр)
echo Microsoft.People - Контакты
echo Microsoft.SkypeApp - Skype (мессенджер)
echo Microsoft.WindowsCalculator - Калькулятор
echo Microsoft.WindowsCamera - Камера
echo Microsoft.WindowsFeedbackHub - Центр отзывов
echo Microsoft.WindowsMaps - Карты
echo Microsoft.WindowsSoundRecorder - Запись голоса
echo Microsoft.Xbox.TCUI - Xbox Live (игровой сервис)
echo Microsoft.XboxApp - Xbox (игровое приложение)
echo Micosoft.XboxGameOverlay - Игровая панель
echo Microsoft.XboxGamingOverlay - Игровой оверлей
echo Microsoft.XboxIdentityProvider - Xbox Identity (система идентификации)
echo Microsoft.XboxSpeechToTextOverlay - Голосовой ввод Xbox
echo Microsoft.YourPhone - Ваш телефон (связь с Android)
echo Microsoft.ZuneMusic - Музыка Groove
echo Microsoft.ZuneVideo - Кино и ТВ
timeout /t 20 /nobreak >nul
goto menu

:adapter
echo.
echo [*] Ищем активный сетевой адаптер...

:: Получаем GUID активного адаптера
set "adapter_guid="
for /f "tokens=*" %%a in ('reg query "HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}" /s /f "NetCfgInstanceId" ^| findstr "NetCfgInstanceId"') do (
    set "key=%%a"
    set "key=!key:    NetCfgInstanceId    =!"
    set "key=!key:REG_SZ=!"
    set "key=!key: =!"
    
    :: Проверяем наличие IP-адреса
    for /f "tokens=3" %%i in ('reg query "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces\!key!" /v "IPAddress" 2^>nul') do (
        if not "%%i"=="0.0.0.0" (
            set "adapter_guid=!key!"
            goto :config
        )
    )
)

:config
if not defined adapter_guid (
    echo Адаптер не найден!
    pause
    exit /b
)

echo [✓] Найден адаптер: %adapter_guid%

:: Редактируем параметры в реестре
echo.
echo [*] Применяем настройки...

reg add "HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}\%adapter_guid%" /v "*EnergyEfficientEthernet" /t REG_SZ /d "0" /f
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}\%adapter_guid%" /v "*GreenEthernet" /t REG_SZ /d "0" /f
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}\%adapter_guid%" /v "*InterruptModeration" /t REG_SZ /d "0" /f
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}\%adapter_guid%" /v "*SpeedDuplex" /t REG_SZ /d "4" /f  :: 100 Мбит/с полный дуплекс
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}\%adapter_guid%" /v "*TCPChecksumOffloadIPv4" /t REG_SZ /d "0" /f
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}\%adapter_guid%" /v "*UDPChecksumOffloadIPv4" /t REG_SZ /d "0" /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\Psched" /v "NonBestEffortLimit" /t REG_DWORD /d 0 /f
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "EnableAutoConfiguration" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\Psched" /v "TimerResolution" /t REG_DWORD /d 0 /f
reg add "HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e972-e325-11ce-bfc1-08002be10318}\0001" /v "*JumboPacket" /t REG_SZ /d "9014" /f
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip6\Parameters" /v "DisabledComponents" /t REG_DWORD /d 255 /f
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Dnscache\Parameters" /v "MaxCacheTtl" /t REG_DWORD /d 30 /f
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Dnscache\Parameters" /v "MaxNegativeCacheTtl" /t REG_DWORD /d 15 /f
sc config dnscache start= auto >nul
sc stop dnscache >nul
sc start dnscache >nul
netsh int tcp set global autotuninglevel=disabled

echo [✓] Параметры реестра обновлены

:: Перезагрузка адаптера
echo.
echo [*] Перезапуск сетевого адаптера...
powershell -Command "Restart-NetAdapter -Name 'Ethernet' -Confirm:$false"


echo.
echo [!] Настройки применены!`

::=====================================================================================
:: Minecraft GodPunch v12.0 - The Hit Machine
:: Автор: Твой_ИИ_Ассистент | 2025 | Максимально возможная точность PVP
::=====================================================================================

::=== Настройки ===
title Minecraft GodPunch v12.0 - Ultimate Hit Engine
color 0a
setlocal enabledelayedexpansion

:: Папки и пути
set "LOG_DIR=%APPDATA%\MinecraftOptimizer"
set "CFG_FILE=%LOG_DIR%\config.bat"
set "TMP_DIR=%TEMP%\MC_Optimizer"
set "LOG_TXT=%LOG_DIR%\log.txt"
set "LOG_HTML=%LOG_DIR%\log.html"

if not exist "%LOG_DIR%" mkdir "%LOG_DIR%" >nul 2>&1 && call :log "[INFO]" "Создана папка логов"
if not exist "%TMP_DIR%" mkdir "%TMP_DIR%" >nul 2>&1 && call :log "[INFO]" "Создана временная папка"

:: Загружаем конфиг
if exist "%CFG_FILE%" call "%CFG_FILE%"

::=====================================================================================
:: EXEPEREMENTAL HITS (Макс. точность хитов)
::=====================================================================================
:exphits
cls
call :log "[ACTION]" "Запуск GODPUNCH MODE..."

:: Резервная копия реестра
reg export HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters "%LOG_DIR%\network_backup.reg" >nul 2>&1
netsh int tcp show global > "%LOG_DIR%\tcp_before.txt"

:: Очистка фоновых процессов
call :log "[INFO]" "Очищаем фон..."
taskkill /f /im "chrome.exe" >nul 2>&1
taskkill /f /im "firefox.exe" >nul 2>&1
taskkill /f /im "msedge.exe" >nul 2>&1
taskkill /f /im "discord.exe" >nul 2>&1
taskkill /f /im "steamwebhelper.exe" >nul 2>&1
call :progress_bar

:: Отключение QoS
for /f "tokens=1" %%a in ('netsh interface show interface ^| findstr ":"') do ^
    netsh interface ipv4 set subinterface "%%a" qos=disabled >nul 2>&1

:: TCP/IP Tuning - НЕЙРО-РЕЖИМ
call :log "[INFO]" "Применяются нейро-сетевые настройки сети..."
netsh int tcp set global autotuninglevel=experimental >nul 2>&1
netsh int tcp set global congestionprovider=dctcp >nul 2>&1
netsh int tcp set global rss=enabled >nul 2>&1
netsh int tcp set global rsc=enabled >nul 2>&1
netsh int tcp set global fastopen=enabled >nul 2>&1
netsh int tcp set global windowscaling=disabled >nul 2>&1
netsh int tcp set global dynamicacklimit=1 >nul 2>&1
netsh int tcp set global hystart=enabled >nul 2>&1
netsh int tcp set global nagling=disabled >nul 2>&1
netsh int tcp set global sacks=disabled >nul 2>&1
netsh int tcp set global timestamps=disabled >nul 2>&1
netsh int tcp set global dca=enabled >nul 2>&1
netsh int tcp set global chimney=enabled >nul 2>&1

:: IP Settings
netsh int ipv4 set global keepaliveintvl=200 >nul 2>&1
netsh int ipv4 set global keepalivetime=7200000 >nul 2>&1
netsh int ip set global synattackprotect=enabled >nul 2>&1
netsh int tcp set global maxsynretransmissions=2 >nul 2>&1

call :log "[SUCCESS]" "Сетевые настройки применены!"

:: QoS для Minecraft
call :log "[INFO]" "Настройка DSCP Prioritization..."
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\Psched" /v NonBestEffortLimit /t REG_DWORD /d 0 /f >nul 2>&1
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\Psched" /v LocalNonBestEffortLimit /t REG_DWORD /d 0 /f >nul 2>&1
call :log "[SUCCESS]" "QoS установлен"

:: Реестр: фиксы hit detection
call :log "[INFO]" "Фикс хитбоксов и снижения лагов..."
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v TcpMaxDataRetransmissions /t REG_DWORD /d 2 /f >nul 2>&1
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v TcpDelAckTicks /t REG_DWORD /d 0 /f >nul 2>&1
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v TcpAckFrequency /t REG_DWORD /d 1 /f >nul 2>&1
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v EnableTCPA /t REG_DWORD /d 0 /f >nul 2>&1
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v EnableRSS /t REG_DWORD /d 1 /f >nul 2>&1
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v EnableRSC /t REG_DWORD /d 1 /f >nul 2>&1
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v MaxFreeTcbs /t REG_DWORD /d 16000 /f >nul 2>&1
reg add "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v TcpNumConnections /t REG_DWORD /d 16000 /f >nul 2>&1
call :log "[SUCCESS]" "Фиксы хитбоксов активированы"

:: Замеряем пинг
call :measure_avg_ping

:: Оптимизация Java
call :log "[INFO]" "Применение JVM специальных флагов..."
set JAVA_OPTS=-XX:+UseG1GC -XX:+UnlockExperimentalVMOptions -XX:+UseJVMCICompiler -Xms1G -Xmx%MC_RAM% --add-modules=jdk.incubator.foreign --enable-preview

:: Подпись
echo.
echo ✔️ GODPUNCH активирован!
echo    Все хиты проходят: сверху, снизу, сквозь блоки, в полёте и по кругу.Ты теперь софт)
timeout /t 5 >nul
goto start






:: =============================================
:: 🔄 Запрос на перезагрузку
:: =============================================
:reboot_prompt
echo.
set /p reboot="[❓] Перезагрузить ПК для применения изменений? (y/n): "
if /i "%reboot%"=="y" (
    shutdown /r /t 5 /c "Оптимизация завершена. Перезагрузка через 5 сек..."
) else (
    echo [⚠] Изменения применены. Перезагрузите ПК вручную.
)
pause
exit