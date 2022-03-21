# BloodyAv
> BloodyAv is Custom Shell Code loader to Bypass Av and Edr.

```
 ▄▄▄▄       ██▓        ▒█████      ▒█████     ▓█████▄    ▓██   ██▓    ▄▄▄          ██▒   █▓
▓█████▄    ▓██▒       ▒██▒  ██▒   ▒██▒  ██▒   ▒██▀ ██▌    ▒██  ██▒   ▒████▄       ▓██░   █▒
▒██▒ ▄██   ▒██░       ▒██░  ██▒   ▒██░  ██▒   ░██   █▌     ▒██ ██░   ▒██  ▀█▄      ▓██  █▒░
▒██░ █▀    ▒██░       ▒██   ██░   ▒██   ██░   ░▓█▄   ▌     ░ ▐██▓░   ░██▄▄▄▄██      ▒██ █░░
░▓█  ▀█▓   ░██████▒   ░ ████▓▒░   ░ ████▓▒░   ░▒████▓      ░ ██▒▓░    ▓█   ▓██▒      ▒▀█░  
░▒▓███▀▒   ░ ▒░▓  ░   ░ ▒░▒░▒░    ░ ▒░▒░▒░     ▒▒▓  ▒      ░██▒▒▒     ▒▒   ▓▒█░      ░ ▐░  
▒░▒   ░    ░ ░ ▒  ░   ░ ░ ▒ ▒░    ░ ░ ▒ ▒░     ░ ▒  ▒     ▓██ ░▒░      ▒   ▒▒ ░      ░ ░░  
 ░    ░      ░ ░  ░   ░ ░ ░ ▒     ░ ░ ░ ▒      ░ ░  ░     ▒ ▒ ░░       ░   ▒  ░        ░░  
 ░             ░  ░       ░ ░         ░ ░        ░  ░     ░ ░          ░   ░  ░         ░  
 ░                                      ░        ░  ░                         ░         ░




usage: BloodyAV.py [-h] [-p explorer.exe] [-m QueueUserAPC] [-nr] [-v] [-d] [-o output.exe] file

Mr.N1K0'S CUSTOM SHELLCODE LOADER FOR WINDOWS DEFAULT PROCESS

positional arguments:
  file                  File that containing raw shellcode

options:
  -h, --help            show this help message and exit
  -p explorer.exe, --process explorer.exe
                        Process to inject into
  -m QueueUserAPC, --method QueueUserAPC
                        Method for shellcode execution ( Method: QueueUserAPC, RemoteThreadContext, CurrentThread) (Recommended:QueueUserAPC)
  -nr, --no-randomize   Disable syscall name randomization
  -v, --verbose         Enable debugging messages upon execution and show more Info
  -d, --dll-sandbox     Use DLL based sandbox checks instead of the standard ones
  -o output.exe, --outfile output.exe
                        Name of output file
```


## Features

1. It has many loading modes. There are 13 loading modes in 32 bits and 12 loading modes in 64 bits.
2. Support development. If a new attack means is found, you can develop template according to the specified method.
3. Shellcode is automatically encrypted.The md5 of loaders that come from the same shellcode are different,because the generator uses time as seed to randomly generate 128-bit keys for encryption.
4. XOR Encryption with Dynamic Key Generation
5. Sandbox Evasion via Loaded DLL Enumeration
6. Sandbox Evasion via Checking Processors, Memory, and Time
7. You Can Also Add Your Own SystemCall in SystemCall.h File For Some Kind Of Customization.


## installation

```
git clone https://github.com/MRNIKO1/BloodyAv.git

sudo apt install mingw-w64 python3

cd BloodyAv

python3 BloodyAV.py -h 
```


## Note

1. For SandBox Evasion When you Run your Exe It will Take Some Time To Call Back To Your C2.
3. -P Flag Will Only Work With Default PE Of Windows And For Running Process Like (explorer.exe, calc.exe, notepad.exe, etc)


## Ref

- [Antisandbox](https://0xpat.github.io/Malware_development_part_2/)
- [RC4 Crypt](https://www.52pojie.cn/thread-800115-1-1.html)
- [CreateThreadpoolWait Load](https://www.ired.team/offensive-security/code-injection-process-injection/shellcode-execution-via-createthreadpoolwait)
- [Fiber Load](https://www.ired.team/offensive-security/code-injection-process-injection/executing-shellcode-with-createfiber)
- [NtTestAlert Load](https://www.ired.team/offensive-security/code-injection-process-injection/shellcode-execution-in-a-local-process-with-queueuserapc-and-nttestalert)
- [SEH except Load](https://idiotc4t.com/code-and-dll-process-injection/seh-code-execute)
- [TLS callback Load](https://idiotc4t.com/code-and-dll-process-injection/tls-code-execute)
- [syscall Load](https://modexp.wordpress.com/2020/06/01/syscalls-disassembler/)
- [APC Inject Load](https://www.ired.team/offensive-security/code-injection-process-injection/apc-queue-code-injection)
- [Early Bird APC Inject Load](https://www.ired.team/offensive-security/code-injection-process-injection/early-bird-apc-queue-code-injection)
- [Early Brid APC Inject](https://www.ired.team/offensive-security/code-injection-process-injection/early-bird-apc-queue-code-injection)
- [NtCreateSection Inject Load](https://www.ired.team/offensive-security/code-injection-process-injection/ntcreatesection-+-ntmapviewofsection-code-injection)
- [OEP Hiijack Hiijack Inject Load](https://www.ired.team/offensive-security/code-injection-process-injection/addressofentrypoint-code-injection-without-virtualallocex-rwx)
- [Thread Hiijack Inject Load](https://idiotc4t.com/code-and-dll-process-injection/setcontext-hijack-thread)
