
# bat2exe-tools



## Description

bat2exe-tools is a collection of tools for converting BAT (Batch) files to EXE (executable) files. These tools aim to simplify the process of converting and packaging batch scripts into standalone executable files, making it easier to distribute and run them on various Windows systems.

## Tools Included

- **BAT to EXE Converter**: This tool converts BAT files to EXE format while preserving the functionality of the original script. It supports various options for customization, such as setting custom icons, adding version information, specifying administrator privileges, and more.

- **Encryption and Obfuscation Tool**: This tool enhances the security of your converted EXE files by encrypting and obfuscating the code. It helps protect your batch script from unauthorized access and tampering, making it more difficult for malicious actors to analyze or modify your script.

- **Resource Embedder**: This utility allows you to embed additional resources, such as images, icons, or data files, into the converted EXE file. You can include any required resources that your batch script relies on, ensuring that everything is contained within a single executable file for easy distribution.

- **Command-line Interface (CLI)**: The repository also provides a command-line interface for automating the conversion process. This CLI tool allows you to convert BAT files to EXE files in batch mode, enabling you to convert multiple scripts simultaneously or integrate the conversion process into your build pipeline.

## Usage

Please refer to the individual tool's documentation for instructions on how to use them effectively. You can find detailed usage instructions and examples in their respective directories.

## Contributions

Contributions are welcome! If you have any ideas, enhancements, bug fixes, or new tools that you'd like to contribute, please feel free to submit a pull request. Make sure to follow the existing coding style and add appropriate tests for any new functionality.

## Instructions

1. Open a text editor (e.g., Notepad) on your Windows computer.

2. In the text editor, type the following code:

```bat
;@echo off
;Title Converting batch scripts to file.exe with iexpress
;Mode 75,3 & color 0A
;echo(
;if "%~1" equ "" (
    ;echo  Usage : Drag and Drop your batch file over this script:"%~nx0"  
    ;Timeout /T 5 /nobreak>nul & Exit
;)
;set "target.exe=%__cd__%%~n1.exe"
;set "batch_file=%~f1"
;set "bat_name=%~nx1"
;set "bat_dir=%~dp1"
;Set "sed=%temp%\2exe.sed"
;echo              Please  wait a while ...  Creating "%~n1.exe" ...
;copy /y "%~f0" "%sed%" >nul
;(
    ;(echo()
    ;(echo(AppLaunched=cmd /c "%bat_name%")
    ;(echo(TargetName=%target.exe%)
    ;(echo(FILE0="%bat_name%")
    ;(echo([SourceFiles])
    ;(echo(SourceFiles0=%bat_dir%)
    ;(echo([SourceFiles0])
    ;(echo(%%FILE0%%=)
;)>>"%sed%"

;iexpress /n /q /m %sed%
;del /q /f "%sed%"
;exit /b 0

[Version]
Class=IEXPRESS
SEDVersion=3
[Options]
PackagePurpose=InstallApp
ShowInstallProgramWindow=0
HideExtractAnimation=1
UseLongFileName=1
InsideCompressed=0
CAB_FixedSize=0
CAB_ResvCodeSigning=0
RebootMode=N
InstallPrompt=%InstallPrompt%
DisplayLicense=%DisplayLicense%
FinishMessage=%FinishMessage%
TargetName=%TargetName%
FriendlyName=%FriendlyName%
AppLaunched=%AppLaunched%
PostInstallCmd=%PostInstallCmd%
AdminQuietInstCmd=%AdminQuietInstCmd%
UserQuietInstCmd=%UserQuietInstCmd%
SourceFiles=SourceFiles

[Strings]
InstallPrompt=
DisplayLicense=
FinishMessage=
FriendlyName=-
PostInstallCmd=<None>
AdminQuietInstCmd=

```


---
### Create Tools to convert BAT file to EXE file ( @Frex-IQ )

<a href="https://youtu.be/iq0W7G3QrtU"><img src="https://i.ibb.co/vPSFp25/pngtree-watch-now-button-website-media-png-image-4711007-removebg-preview.png" alt="Watch the video" width="200" height="60"></a>

---
Feel free to customize the README.md file based on your specific needs and preferences.

<img src="bat2exe-tools Screenshot.png" >
