# RaspberryService
Trying to run asp.net core on Raspberry Pi 3 running Windows 10 Iot

I am trying to run asp.net core app on Raspberry pi 3 which runs Windows10 IoT .What I have done so far is:

 1. Created a simple Web Api application in Asp.net core in local Windows 10 machine using visual studio. 
 2. removed `type:platform` from project.json file  (for self contained deployment)
 3. built and published the application using `dotnet publish -c release -r win10-arm`  
 4. copied the published files to UNC share folder in path  
 5. opened the port 5000 in pi powershell session  `netsh advfirewall firewall add rule name="DNX Web Server port" dir=in action=allow protocol=TCP localport=5000` 
 6. typed `'C:\PROGRAMS\dnxpi\RasberryService.exe'` in powershell session to pi

But it errors

    Program 'RasberryService.exe' failed to run: The operation completed successfully.
    + CategoryInfo          : ResourceUnavailable: (:) [], ApplicationFailedException
    + FullyQualifiedErrorId : NativeCommandFailed

Thanks in Advance!!

