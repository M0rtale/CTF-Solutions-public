#Legit App Not Ransomware

## The Binary

The Binary contains numerous .NET Environment strings when opened in ida, i.e. "System Exception". Indicating a packed Visual Studio .NET program compile

## Exeinfope

Loading Binary into Exeinfope confirms my suspicion and it identifies as a .NET runtime. Stripping the exe of executables shows rip.exe

## DnSpy

Loading rip.exe into DnSpy, it was able to identify it as a valid .NET executable. Locate the main function, notice the flag is encoded by local variable d, u, c, t, f. Concat all the strings together and decode using base64 gives the flag

`DUCTF{d1d_y0u_pan1c_0r_c00l_as_cucumb3r}`
