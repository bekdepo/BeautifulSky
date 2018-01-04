# BeautifulSky

It is a W32/W64 cross-platform x86/x64 code base for (my) proof-of-concept self-replicators.
For a detailed description, read SKYBEA2.TXT.

# Compilation

Compile with masm32:

ml /c /coff /Cp "beautifulsky32.asm"
link /SUBSYSTEM:CONSOLE /SECTION:.text,erw /OUT:"beautifulsky32.asm" "beautifulsky32.obj"

Both sources are written in x86/x64 code.
When executed, BeautifulSky64 generates a standard PE32+ file (SkyBeautiful64.exe) with its code inside so that you can run it in 64-bit mode.

# Contact

Contact me for comments, permission to use the sources in your project, or bug reports to: com.gmail@fsendjinn