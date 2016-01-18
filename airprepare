#!/bin/sh

# pass in wlan interface or assume name "wlan"
$wlan=${1:-wlan0}

# reset mac address and turn on monitor mode
ifconfig $wlan down
macchanger -r $wlan
iwconfig $wlan mode monitor
ifconfig $wlan up

# check for any software interference
airmon-ng check $wlan
