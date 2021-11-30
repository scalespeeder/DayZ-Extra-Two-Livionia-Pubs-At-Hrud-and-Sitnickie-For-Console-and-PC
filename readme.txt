DayZ Livonia Pubs At Hrud & Sitnickie For Console and PC xml json Mod Instructions & Terms Of Use

Limited Testing on PC Livonia Local Server DAYZ Version 1.15 Nov 2021.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

Many Thanks To Inclement Dab for his amazing DayZ Editor that makes this all possible: https://steamcommunity.com/sharedfiles/filedetails/?id=2250764298

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "livonia-hrud-pub.json" and "livonia-sitnickie-pub.json" from the extracted files to inside the "custom" folder of the mission directory on your server. This file places the structures on your map.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "objectSpawnersArr" line.

This file tells your server to access your custom file.

Edit it to look like this: 

	"objectSpawnersArr": ["custom/livonia-hrud-pub.json","custom/livonia-sitnickie-pub.json"]
	
If you already are calling custom jsons to spawn items, seperate the files like this:

	"objectSpawnersArr": ["custom/livonia-hrud-pub.json","custom/livonia-sitnickie-pub.json","custom/differentfile.json"]
	
Save your changes & upload if you need to.
	
Next we add loot to the structures by adding the following code snippet to the top of your mapgrouppos.xml file, after <map> 

	<!--hrud pub-->
	<group name="Land_Village_Pub" pos="6517.459961 209.470993 9050.370117" rpy="-0.500000 0.000000 68.933006" a="21.067"/>
	<group name="Land_Misc_Toilet_Dry" pos="6521.247559 206.143250 9077.831055" rpy="-0.000000 -0.000000 -14.221914" a="104.222"/>
	<group name="Land_Lunapark_Carousel_Small" pos="6510.723633 206.882690 9065.986328" rpy="-0.000000 -0.000000 0.000000" a="90"/>
	<group name="Land_Misc_Greenhouse" pos="6525.589844 206.199997 9071.309570" rpy="0.000000 0.500000 -25.000000" a="115"/>
	<!--sitnickie pub-->
	<group name="Land_Misc_Greenhouse" pos="11550.827148 174.720276 10258.075195" rpy="-0.000000 -0.000000 -46.529625" a="136.53"/>
	<group name="Land_Village_Pub" pos="11533.267578 177.741714 10238.087891" rpy="-0.000000 -0.000000 -44.839867" a="134.84"/>
	<group name="Land_Shed_W5" pos="11546.403320 175.074020 10244.411133" rpy="-0.000000 -0.000000 136.918640" a="-46.9186"/>
	<group name="Land_Misc_Toilet_Dry" pos="11542.571289 175.002792 10246.038086" rpy="-0.000000 -0.000000 49.659687" a="40.3403"/>
	<group name="Land_Misc_Toilet_Dry" pos="11540.601563 174.957642 10247.932617" rpy="-0.000000 -0.000000 45.951176" a="44.0488"/>
	<group name="Land_misc_chickenCoop" pos="11544.223633 173.908264 10249.691406" rpy="-0.000000 -0.000000 -131.005020" a="-138.995"/>
	<group name="Land_Misc_Greenhouse" pos="11555.016602 174.805725 10254.382813" rpy="-0.000000 -0.000000 -46.529625" a="136.53"/>
	
Save your changes & upload if you need to.

Restart your server and the new structures will appear immediatly, and then they will slowly stock with loot.

Thanks, Rob.
