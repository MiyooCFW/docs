
## How to run remote debugging on miyoo device using VS code and gdbserver

1. Install the [Native Debug](https://github.com/WebFreak001/code-debug) extension for VS Code
2. Add below launch configuration to Run configurations in VS Code (Run->Add Configuration..)
```
{
    "version": "0.2.0",
    "configurations": [
    
        {
            "type": "gdb",
            "request": "attach",
            "name": "Attach to gdbserver",
            "executable": "<path to binary relative to workspace root>",
            "target": "192.168.137.1:9999",
            "remote": true,
            "cwd": "${workspaceRoot}", 
            "gdbpath": "/opt/arm-miyoo-linux-uclibcgnueabi_sdk-buildroot/bin/arm-linux-gdb"
        }
    ]
}
```
3. On miyoo device start gdbserver with application
```
gdbserver 192.168.137.1:9999 ./<application>
```
4. Start debugging in VS code (Run->Start Debugging)

[![image](https://github.com/user-attachments/assets/f86e0869-414f-46b2-836f-7c1dc13e8ba7)](https://github.com/user-attachments/assets/f86e0869-414f-46b2-836f-7c1dc13e8ba7)

