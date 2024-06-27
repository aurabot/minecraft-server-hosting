# minecraft-server-hosting, dont skid plz
this will allow you to host a feather server with mods! (IF YOU DO NOT UNDERSTAND, WATCH THE VIDEO FOR VISUAL)
FIRST STEP:
Download feather - https://feathermc.com/
Open feather -> servers (4th on the left dashboard) -> + sign (name and proxy hostname whatever you want) Choose Template - Custom
Java Version - 17
Ram and Slots however much you want (recommended no more then 50% of pc ram) to check go to ctrl + shift + esc (task mgr) -> Performance -> Memory and check how much you have.
Make the server and press accept on EULA,
open folder of this server, press the settings button on the top left of the server that you made and press open folder and next put the thing you download on the next step there.

SECOND STEP:
Download for example 1.20.1 (use any version you want) server jar: https://files.minecraftforge.net/net/minecraftforge/forge/index_1.20.1.html (better to use recommended version)
After you open the installer press on the install server option and the 3 dots (...) click that and put the directory of where the feather server is, in the first step we have shown you where.
You can download server file from curseforge too.
use whichever one you want, really, this solution works on any server with a run batch file (run.bat and could have a different name) on windows, or a shell file for linux (run.sh), if you are using linux.

THIRD STEP:
install IntelliJ IDEA: https://www.jetbrains.com/idea/download/?section=windows
My IntelliJ will look different because I have an old version, in the new version there is a 3 lined dashbar that opens the tabs like File, Build, that would be neccesary for this guide.
open up your IntelliJ IDEA (you can use a diferent project builder if you are advanced enough to do so)
make a project file -> new -> project
name it server, use jdk 17. if you dont have it, download it: https://www.oracle.com/java/technologies/downloads/#jdk17-windows (windows link)
press create. open in this window.
After you have made the project, on src folder, right click and new -> java class -> server
now press enter, and it should be made inside the src. go into the server.java now 
and paste whatever is in the txt in this repository, server.txt
in this server.txt will be a "ur directory here" and you will have to change wherever you have the feather server, and in that server the directory where you opened the run.bat file and it generated the necessary server files, you need to exactly
give the correct directory, and this has to be in the server folder that you made in feather.
to give an example, for me it would be:
C:\Users\boilerjohn\AppData\Roaming\.feather\player-server\servers\eea8dcd2-d767-4bf5-b53b-0a4440041ba5\run.bat (for linux it would be run.sh for example)
so this goes in 

        ProcessBuilder pb = new ProcessBuilder("ur directory here"); // so it would change to 
        
        ProcessBuilder pb = new ProcessBuilder("C:\Users\boilerjohn\AppData\Roaming\.feather\player-server\servers\eea8dcd2-d767-4bf5-b53b-0a4440041ba5\run.bat");


and now, in IntelliJ go to file -> Project Structure -> in project settings go to Artifacts press + in Artifacts, JAR -> From modules with dependencies -> the Module, if you did all steps correctly should be server, the Main Class server as well. now, press OK, then press Apply and then OK again now press Build -> Build Artifacts... Now a popup will appear and press Build. Now it will be wherever you made your project, /out/artifacts/server_jar and it will be named server.jar
now what you have to do, is put this server.jar where the feather server is, so 
C:\Users\boilerjohn\AppData\Roaming\.feather\player-server\servers\eea8dcd2-d767-4bf5-b53b-0a4440041ba5\    
for me, it would be different for you.
now once server.jar is placed in the correct directory, and everything is done correctly, open feather client go to servers, open the server. (Start Server), the button.
if you want to  add mods, go to the server directory, open mods folder and add whatever you want for the version you made.
Keep in mind, you have to use the same mods for the client 

FOURTH STEP:
ENJOY!!!!!!!!!!!!!!!!!!!!!!!!




