# VehicleCustomsPinRekeyFix

There is an issue with the default exile code where you need one additional poptab before you can change a vehicle's pin. So, currently if the dialogue box says 10,000, you would need 10,001 for the "reset pin" button to light up and allow you to click to change pin.

This very simple fix sorts out that problem so you only need to have what it tells you to have on your player.

1) Add the file ExileClient_gui_vehicleRekeyDialog_event_onDropDownSelectionChanged.sqf to your fixes folder

2) In your mission file config.cpp find the block the starts with class CfgExileCustomCode and add the following for the override:
    	//Fix For Vehicle Customs needing extra PT for Pin Change
	ExileClient_gui_vehicleRekeyDialog_event_onDropDownSelectionChanged = "fixes\ExileClient_gui_vehicleRekeyDialog_event_onDropDownSelectionChanged.sqf";
  
3) Repack and upload your mission.pbo
