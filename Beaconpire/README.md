# beaconpire.cna

An Aggressor script used to control Empire listeners and pass sessions between Cobalt Strike and Empire.

## Setup

Load *beaconpire.cna* into Cobalt Strike's Script Manager. 

Configure the Empire server IP, port, and REST token in the *Beaconpire -> Configure Server* attack menu. 


## Adding/Removing Listeners

Listeners can be added/removed in the *Beaconpire -> Configure Empire Listeners* attack menu.

## Sending Beacons to Empire

Beaconpire supports three session passing methods to send Beacons to Empire:

* Within the *Beaconpire -> Send Beacons to Empire* attack menu
* Select one or more Beacons, right click, and select *Send to Empire*
* In a Beacon console, use the command *sendtoempire*

## Puling Empire Agents into Beacon

To pull Empire Agents into Cobalt Strike, use the *Beaconpire -> Pull in Empire Agents*, select Agent(s), and select the Cobalt Strike listener to use for staging. 

*Note: If the Empire server doesn't have a foreign Empire listener for your selected Cobalt Strike server, it will create one.*

## References

For more info and demo GIFs, please see:
[https://bluescreenofjeff.com/2016-11-29-beaconpire-cobalt-strike-and-empire-interoperability-with-aggressor-script](https://bluescreenofjeff.com/2016-11-29-beaconpire-cobalt-strike-and-empire-interoperability-with-aggressor-script)