# Deprecation notice 

Thanks for your interest in the Project Tango Plugin for Unreal Engine 4. This repository is no longer maintained. Please see https://developers.google.com/ar/ for the latest information on Google AR capabilities for UE4.

# Tango 4 Unreal Plug-In

The Tango 4 Unreal Plug-In enables the use of Project Tango tablet devices sensors within Unreal 4
Android deployments.

## Getting Started

* Create a "Plugins" folder inside you Unreal 4 project, if it doesn't already exist.
* Clone this repository into the Plugins folder:
* `git clone https://github.com/opaquemultimedia/ProjectTangoPlugin.git`
* Alternatively, if your project is already a git repository:
* `git submodule add https://github.com/opaquemultimedia/ProjectTangoPlugin.git`
* Refer to the [Git Book](https://git-scm.com/book/en/v2/Git-Tools-Submodules) for more
information about git submodules
* Go to your plug-in settings, browse the to "Google" category, enable the plug-in, then restart
the Unreal Editor.

## Using the plug-in
Currently, the most stable implementation is the "Tango Motion" component. This retrieves
the device's positional tracking data and presents functions to access it.

### In a new blueprint pawn

* Add a "Tango Motion" component to the pawn.

### Then in the default variables list of the component:

* Under the Tango|Motion category, change:
* "Position Offset" to: `X 0.0 | Y 0.0 | Z 175.0`

### In the Event Graph:

* Place a reference to the component in.
* From the component reference, add a "Set Is Sending Motion to Pawn" function node, check the
boolean to true.
* Connect an execution link from the BeginPlay event to the function.

### Back in your level:

* Setup the pawn to be the default pawn spawned for the level's game mode, then launch the project
on your device.
* Have fun!
