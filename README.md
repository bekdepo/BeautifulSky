# BeautifulSky

It is a W32/W64 cross-platform x86/x64 code base for (my) proof-of-concept self-replicators.

# What's new in BeautifulSky

– uses the same code to run in both x86/x64 modes, single execution path
– fully x86/x64 compatible encoding
– no self-modifying code to achieve compatibility
– position independent-code and compatible with Address Space Layout Randomization
– uses Process Environment Block (PEB) to get kernel32/ntdll directly on both platforms
– stdcall/x64 calling convention compatible
– own GetProcAddress() that supports PE32/PE32+
– uses CRC32 instead of name strings
– uses Vectored Exception Handler for common exception handling on both platforms

BeautifulSky searches the current directory for any file. To open and map files for infection it uses an adapted and more efficient version of a technique used by W32.Cabanas virus by Jacky Qwerty in 1998.

For a more detailed description, read SKYBEA2.TXT.

# Compilation

Compile with masm32:

ml /c /coff /Cp "beautifulsky32.asm"
link /SUBSYSTEM:CONSOLE /SECTION:.text,erw /OUT:"beautifulsky32.asm" "beautifulsky32.obj"

Both sources are written in x86/x64 code.
When executed, BeautifulSky64 generates a standard PE32+ file (SkyBeautiful64.exe) with its code inside so that you can run it in 64-bit mode.

# Contact

Contact me for comments, permission to use the sources in your project, or bug reports to: com.gmail@fsendjinn