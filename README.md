# PinUtil : Pin To TaskBar And StartMenu Utility

**Usage1:** PinUtil (TaskBar|StartMenu) File ["File 2" "File 9"]<br>
<br>
Ex1: PinUtil TaskBar %windir%\System32\calc.exe<br>
Ex2: PinUtil StartMenu "C:\Windows\System32\notepad.exe" "%windir%\System32\calc.exe"<br>
<br>
**Usage2:** PinUtil Config ConfigFile [Section (Default=PinUtil)]<br>
<br>
Ex: PinUtil Config %windir%\System32\PintUtil.ini<br>
<br>
PinUtil.ini (Limited To 9 Elements For TaskBar And StartMenu):<br>
> [PinUtil]<br>
> StartMenu1=%AllPrograms%\Accessories\Paint.lnk<br>
> StartMenu0=%WinDir%\Explorer.exe<br>
> TaskBar0=%SystemRoot%\System32\cmd.exe<br>
> TaskBar9=%SystemRoot%\Explorer.exe<br>
<br>

**Usage3:** Pecmd ConfigFile [SubSection (Default=PinUtil)]   (_SUB SubSection)<br>
Pecmd is a command interpreter commonly used in WinPE (Windows PE)<br>
<br>
Ex: PinUtil Pecmd %windir%\System32\Pecmd.ini PinUtil<br>
<br>
Pecmd.ini:<br>
> _SUB PinUtil<br>
> PINT %AllPrograms%\Accessories\Paint.lnk,StartMenu<br>
> PINT %WinDir%\Explorer.exe,StartMenu<br>
> PINT %SystemRoot%\System32\cmd.exe,TaskBar<br>
> PINT %SystemRoot%\Explorer.exe,TaskBar<br>
<br>

**Environment Variables are Available As Well As:**<br>
%StartMenu%, %Programs%, %ALLPrograms%, %Desktop%, %QuickLaunch%<br>
<br>
**Support** StartAllBack, StartIsback++, Start10, StartIsback, Start8, Classic Shell, Open-Shell, Explorer7ForWin8, Windows 7 StartMenu<br>
Windows 10 and 11 Start Screen are not Supported<br>
<br>
You Cannot Pin Applications from a Removable Media...
