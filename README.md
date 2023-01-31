# PinUtil : Pin To TaskBar And StartMenu Utility

## Usage 1 :
PinUtil (TaskBar|StartMenu) File ["File 2" "File 9"]<br>

```
Ex1: PinUtil TaskBar %windir%\System32\calc.exe
Ex2: PinUtil StartMenu "C:\Windows\System32\notepad.exe" "%windir%\System32\calc.exe"
```

## Usage 2 :
PinUtil Config ConfigFile [Section (Default=PinUtil)]<br>

```
Ex: PinUtil Config %windir%\System32\PintUtil.ini
```
PinUtil.ini (Limited To 9 Elements For TaskBar And StartMenu):<br>

```
[PinUtil]
StartMenu1=%AllPrograms%\Accessories\Paint.lnk
StartMenu0=%WinDir%\Explorer.exe
TaskBar0=%SystemRoot%\System32\cmd.exe
TaskBar9=%SystemRoot%\Explorer.exe
```

## Usage 3 :
Pecmd ConfigFile [SubSection (Default=PinUtil)]   (_SUB SubSection)<br>
Pecmd is a command interpreter commonly used in WinPE (Windows PE)<br>

```
Ex: PinUtil Pecmd %windir%\System32\Pecmd.ini PinUtil
```
Pecmd.ini:<br>
```
_SUB PinUtil<br>
  PINT %AllPrograms%\Accessories\Paint.lnk,StartMenu
  PINT %WinDir%\Explorer.exe,StartMenu
  PINT %SystemRoot%\System32\cmd.exe,TaskBar
  PINT %SystemRoot%\Explorer.exe,TaskBar
```

<br>

**Environment Variables are Available As Well As:**<br>
%StartMenu%, %Programs%, %ALLPrograms%, %Desktop%, %QuickLaunch%<br>
<br>
**Support** StartAllBack, StartIsback++, Start10, StartIsback, Start8, Classic Shell, Open-Shell, Explorer7ForWin8, Windows 7 StartMenu<br>
Windows 10 and 11 Start Screen are not Supported<br>
<br>
You Cannot Pin Applications from a Removable Media...
