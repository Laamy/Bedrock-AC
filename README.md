# Notes
do NOT join a public server with the anticheat active else you will get immedately banned <br/>
feel free to join a local world with this anticheat active and try bypass it

# How to install
put the winhttp.dll module next to bedrock_server.exe (to secure your server)
or next to Minecraft.Windows.exe to secure the client

only secured clients can connect to secured servers

# TODO
A worker service that runs on the side with the anticheat to check for hypervisors loaded by drivers & DSE for people patching it before win11 24h2<br/>
also want to include icon signatures MEMORY.FIRST checks in temp and a few others for cheat engine and other misc tools like process inform<br/>
I plan to tell clients if they should send secured packets so you can play normal servers with this (later)

# Goal
goal is to move as many hyperion (roblox) checks recreated & hopefully better to minecraft bedrock <br/>
im probably gonna host a PVP server using this anticheat plus some more custom serverside checks

# Main Features
While giving minimal information on what these actually include here is a quick rundown of the highlights<br/>

Anti debugging
- there are several antidebugging methods used in BEAC including but not limited to
  - IsDebuggerPresent (with integrity checks)
  - TEB
  - DebugBreak traps
  - OutputDebugString traps
  - memory traps (including modified memory permissions & int3's scattered around)
  - all of these are inlined and used in several places while being as small as possible to basically crap on debugging without a hypervisor like BDVM

Basic AntiVM<br/>

Integrity checks
- Integrity checks on vital mc functions used by several clients
  - All nitr0 hooks
  - several flarial & order client hooks
  - common functions used by mc clients
- Seperate BASIC Integrity checks on windows functions used by BEAC
- Anticheat integrity checks for code section

Hooks on functions like LoadLibraryA, LoadLibraryW that validates windows certificates to stop basic injectors that use CRT</br>

Memory whitelist to stop manual mapping (to avoid injection using poolparty vuln and kernel mmappers)</br>

Secure packets that go over raknet with info about the client so you cant just unload the anticheat</br>

Anticheat encryption & security on ALL important functions to stop IDA xref & Loads more
