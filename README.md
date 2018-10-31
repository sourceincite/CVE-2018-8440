# CVE-2018-8440

Since I noticed that metasploit is using the [dll](https://github.com/rapid7/metasploit-framework/blob/master/modules/exploits/windows/local/alpc_taskscheduler.rb#L86) lib provided by SandboxEscaper and only has a target for [x64](https://github.com/rapid7/metasploit-framework/blob/master/modules/exploits/windows/local/alpc_taskscheduler.rb#L48), I decided to share my poc to the community. Of course there are much better vectors than targeting the print spooler, but I'll leave that as an exercise for the reader.

This is a standalone poc executable that was tested on x86 (I needed it for a client). AFAIK, this should also run on x64, but this environment as been untested at this time.

## Getting Started

* Run the Release poc.exe I dare you.

Just kidding.

### Prerequisites

* You might want to relink the resource file since `C:\Users\researcher\source\repos\lpe\Release\payload.dll` probably doesn't exist on your system.

### Installing

* Install Visual Studio 2017 (v141)
* Install Windows SDK 10.0.17134.0
* Relink the resource file in the poc project to a dll of choice
* Compile each project separately
* Run the built poc.exe

## Environment

This was tested on Windows 10 x86 Version 10.0.10240 with the latest patches at the time of development.

## Built With

* [Visual Studio 2017 (v141)](https://visualstudio.microsoft.com/downloads/) - IDE

## Authors

* **SandboxEscaper** - *Initial work* - [PoCLPE.rar](https://github.com/SandboxEscaper/randomrepo/blob/master/PoCLPE.rar)
* **mr_me** - this repo

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* SandboxEscaper for the killer zeroday bug drop
* James Foreshaw for the CommonUtils project

