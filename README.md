# export-search

This simple script do search an address of an export in DLL. It can be useful in writting shellcode.

To use this script, you need the followings:
- Python 2.7 (https://www.python.org/download/releases/2.7/)
- pefile (https://github.com/erocarrera/pefile)

C:\Users\Lab\Documents\GitHub\export-search>python main.py -h
usage: Export search [-h] [-d DLL_PATH] [-e EXPORT]

Searching an export in a DLL

optional arguments:
  -h, --help   show this help message and exit
  -d DLL_PATH  Specify a dll path
  -e EXPORT    Specify a disired export
  
For example:
We want to find the address of NtOpenKey in ntdll.dll:
C:\Users\Lab\Documents\GitHub\export-search>python main.py -d dll/ntdll.dll -e NtOpenKey

Result:
The Export NtOpenKey is located at 0x77f05870 in dll/ntdll.dll
