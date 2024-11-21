# Enable-All-Tokens
This branch is add simple input command support.

Enable-All-Tokens is a Go-based project designed to adjust and enable a list of specified privileges for the current process token on a Windows operating system. This project can be particularly useful for developers and system administrators who need to programmatically enable various system privileges for their applications.

## Description

The `Enable-All-Tokens` project provides a simple command-line tool that adjusts and enables a predefined set of Windows privileges. This tool leverages the `golang.org/x/sys/windows` package to interact with Windows APIs, enabling privileges such as `SeDebugPrivilege`, `SeBackupPrivilege`, `SeRestorePrivilege`, and many others.


## Prerequisites

Before running the `Enable-All-Tokens` tool, ensure that you have:

- Go installed on your system.
- The `golang.org/x/sys/windows` package installed. You can install this package using the following command:
```sh
go get golang.org/x/sys/windows
```

## Build it if in linux

```
sudo apt-get install gcc-multilib
sudo apt-get install gcc-mingw-w64

touch go.mod
go mod edit -module=example.com/mod
go get golang.org/x/sys/windows

GOOS=windows GOARCH=amd64 CGO_ENABLED=1 CXX=x86_64-w64-mingw32-g++ CC=x86_64-w64-mingw32-gcc go build
```

## Usage

```
.\mod.exe cmd.exe "/c whoami /priv"
```

- Contributions are welcome! Please feel free to submit a pull request or open an issue if you have any suggestions or improvements.
- Made by evilbytecode aka codepulze.
- Mod by [manesec](https://github.com/manesec/).

# 1st : Elevated + Enable All Tokens
![image](https://github.com/EvilBytecode/Enable-All-Tokens/assets/151552809/55927734-e09b-446a-9c19-bc882880cdf6)

# 2nd : Elevated Normal Process + Not Enabled All Tokens
![image](https://github.com/EvilBytecode/Enable-All-Tokens/assets/151552809/d7378f48-226a-4b2b-885b-7d0a61e3f8b5)
