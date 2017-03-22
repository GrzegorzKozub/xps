# XPS

Dell XPS 13 9360 tweaks

## Disable MaxxAudioPro

This will disable (not remove) all background apps related to Realtek MaxxAudioPro. Your headphones will now be detected automatically without any popup. You will also be able to open MaxxAudioPro manually to adjust your audio settings. Since these apps will no longer run in background you will gain some resources and battery life. 

Run `Disable-MaxxAudioPro.ps1` with PowerShell as admin once. You will likely need to run it again after your audio driver is updated.

The script prevents the following apps from running on startup:

* RtHDVBg_PushButton (scheduled task)
* Realtek Audio Service (service)
* Waves Audio Services (service)
* HD Audio Background Process
* Realtek HD Audio Manager
* Waves MaxxAudio Service Application

You will see the last three apps from the above list disabled in task manager under Startup tab.

The script is not destructive so you will be able to re-enable any scheduled task, service and task manager app it disables.
