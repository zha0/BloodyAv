# BloodyAv
BloodyAv is Custom Shell Code loader to Bypass Av and Edr.

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

Mr.N1K0'S CUSTOM SHELLCODE LOADER FOR WINDOWS DEFAULT

positional arguments:
  file                  File that containing raw shellcode

options:
  -h, --help            show this help message and exit
  -p explorer.exe, --process explorer.exe
                        Process to inject into
  -m QueueUserAPC, --method QueueUserAPC
                        Method for shellcode execution (Options: ProcessHollow, QueueUserAPC, RemoteThreadContext,
                        RemoteThreadSuspended, CurrentThread) (Recommended:QueueUserAPC)
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


- The tool has been confirmed to successfully load Meterpreter and a Cobalt Strike beacon on fully updated systems with Windows Defender enabled. The project itself is still in a PoC/WIP state, as it currently doesn't work with all payloads.



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
- 《加密与解密4》
