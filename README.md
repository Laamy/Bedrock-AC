# Notes
do NOT join a public server with the anticheat active else you will get immedately banned <br/>
feel free to join a local world with this anticheat active and try bypass it

Also this is less of an anticheat and more of an antitamper so normal methods to bypass client-server anticheats will not work with it</br>
I will now refer to it as BEAC (**BE**drock **A**nti**C**heat/Antitamper)

# Servers
You will be **KICKED** from these servers unless the required **BEAC module** version is installed and running

147.185.221.27:48834 (AU) (**Latest BEAC/v1.21.120**) Test server (Feel free to try cheat, INSTALL THE RELEASE <-- REQUIRED)

List of people who have bypassed: (msg me on discord yeemi.2 to get added) </br>
No one

# How to install
put the winhttp.dll module next to bedrock_server.exe (to secure your server)
or next to Minecraft.Windows.exe to secure the client</br>
Or if your lazy you can install it on the client via the [installer](https://github.com/Laamy/Bedrock-AC/releases/download/v1.21.120-3/TamperModule.exe)

only secured clients can connect to secured servers

# TODO
NOTE: A worker service is no longer required as of v1.21.120 because of GDK Platform letting me access everything i need</br>
I plan to tell clients if they should send secured packets so you can play normal servers with this (later)</br>
apply beac packet encryption to all packets & improve it massively

# Goal
Goal is to make an antitamper similar to robloxes hyperion to Minecraft Bedrock Edition <br/>
im probably gonna host a PVP server using this antitamper plus some more custom serverside checks

# Main Features
While giving minimal information on what these actually include here is a quick rundown of the highlights (Check back a few commits to see a larger list)<br/>
NOTE: I decided to only list these 3 so you know what your getting into without me exposing to much

[Memory whitelist](https://github.com/Laamy/MemoryWhitelist) to stop manual mapping (Open source feel free to look at this)</br>

Integrity checks
- Integrity checks on vital mc functions used by several clients
  - All nitr0 hooks
  - several flarial & order client hooks
  - common functions used by mc clients
- Seperate BASIC Integrity checks on windows functions used by BEAC
- Complete validation of BEAC module on the server side
- BEAC integrity checks for code section

Hooks on functions like LoadLibraryA, LoadLibraryW that validates windows certificates to stop basic injectors that use CRT</br>
