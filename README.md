# PinUtil
PinUtil : Pin To TaskBar And StartMenu Utility

Usage1: PinUtil (TaskBar|StartMenu) File ["File 2" "File 9"]

Ex1: PinUtil TaskBar %windir%\System32\calc.exe"
Ex2: PinUtil StartMenu "C:\Windows\System32\notepad.exe" "%windir%\System32\calc.exe"


Usage2: PinUtil Config ConfigFile [Section (Default=PinUtil)]

Ex: PinUtil Config %windir%\System32\PintUtil.ini

PinUtil.ini Limited To 9 Elements For TaskBar And StartMenu:
[PinUtil]
StartMenu1=%AllPrograms%\Accessories\Paint.lnk
StartMenu0=%WinDir%\Explorer.exe
TaskBar0=%SystemRoot%\System32\cmd.exe
TaskBar9=%SystemRoot%\Explorer.exe


Usage3: Pecmd ConfigFile [SubSection (Default=PinUtil)]   (_SUB SubSection)

Ex: PinUtil Pecmd %windir%\System32\Pecmd.ini PinUtil 

Pecmd.ini
_SUB PinUtil
PINT %AllPrograms%\Accessories\Paint.lnk,StartMenu
PINT %WinDir%\Explorer.exe,StartMenu
PINT %SystemRoot%\System32\cmd.exe,TaskBar
PINT %SystemRoot%\Explorer.exe,TaskBar


Environment Variables are Available As Well As:
%StartMenu% ($Start_Menu), %Programs%, %ALLPrograms%, %Desktop% ($Desktop), %QuickLaunch% ($Quick_Launch)

Support StartIsback, Start10, Start8, Open-Shell, Classic Shell, Explorer7ForWin8, Windows 7 StartMenu

You Cannot Pin Applications from a Removable Media...
