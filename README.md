iTunesMonitor
=============

An AppleScript and a LaunchDaemon config to monitor iTunes open connections.

Background
With the launch of AppleTV3 problems arose with Home Sharing connectivity. Some long threads:"https://discussions.apple.com/thread/3870357?start=45&tstart=0" on Apple's support forums found that iTunes creates huge numbers of open connections, which ultimately renders it unreachable. Since Apple hasn't come up with a solution and also the latest iTunes update (10.7) didn't fix it, dcarr178:"https://discussions.apple.com/people/dcarr178" came up with a simple AppleScript that monitors iTunes's open connections and restarts it, if it exceeds a number of 60 connections. 

Setup
=====

Copy iTunesMonitor.scpt to your user's bin directory (Users/<USERNAME>/bin). User the AppleScript-Editor to edit it and fill in the variables in the first three lines.
Copy iTunesMonitor.plist to your user's LaunchDaemons directory (Users/<USERNAME>/Library/LaunchDaemons). Edit it and update your username.
Add it to your permanent launch deamons:
launchctl load -w /Users/<USERNAME>/Library/LaunchDaemons/iTunesMonitor.plist


