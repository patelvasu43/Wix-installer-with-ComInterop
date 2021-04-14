# Wix-installer-with-ComInterop
Wix installer , Com Interop, C++, C#


1. Wix Installer
    you can download Wix Toolset build tools and Visual Studio Extension
    Download Link : https://wixtoolset.org/releases
    Build Tools : https://wixtoolset.org/releases/v3.11.2/stable
    Visual Studio Extension : https://marketplace.visualstudio.com/items?itemName=WixToolset.WixToolsetVisualStudio2019Extension
2. Project Detail
  Demo5.Lib
  it is class library which we are registring as com interop
  it is also register in GAC
3. Demo5.Wix
   it is installer ,which register dll as com interop and GAC.
   it generated automated information which required to register com component.
   
   After installer finish below location,you can verify dll
   1. C:\ProgramData\ProPlayAIWindowsSDK
      if this folder not exist please create
   2. C:\Program Files (x86)\Demo5.Wix
   C:\Windows\Microsoft.NET\assembly\GAC_MSIL\Demo5.Lib
   
   You may also required to generated license
   for generate license please use below project
   Solution >Licensing >App >ActivationTool
   
   Add your computer name and generate license.
   
   Save license with file name : license5.lic
   Save license location at : C:\ProgramData\ProPlayAIWindowsSDK
   
   Aslo  add your dependent dll at below location so that C# console app should resolve runtime assembly reference.
   e.g. System.Security.Cryptography.Xml
   location : C:\\ProgramData\\OtherAssembly
   
   
   
   
   
      
