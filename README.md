# OSC ACTION

This is a Elgato StreamDeck Plugin to send Command IDs to the DAW Reaper via OSC. It is written in Go.

Demo Video can be found here: https://youtu.be/ycdiO8_sevA

## Building

Building the Plugin is quite easy:

`go build -o com.smyck.oscaction.sdPlugin/oscaction`

## Installation

Smlink the plugin folder to the StreamDeck plugins folder

`ln -s ./com.smyck.oscaction.sdPlugin ~/Library/Application\ Support/com.elgato.StreamDeck/Plugins/`

Restart the StreamDeck app and verify in the Preferences / Plugins tab that
the "OSC Action Plugin" appears.

Then place it on one of the StreamDeck Buttons and add "127.0.0.1" as IO, the
port that was configured in Reaper and a command id of your choice.

## Known Issues

* For some reason the plugin can only send messages on the loopback interface.
  My attempts to send messages to other LAN IPs failed for unknown reasons
