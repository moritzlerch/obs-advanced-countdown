# obs-advanced-countdown

This is a script for OBS Studio that sets a text source as a timer with advanced options. You also have the option to switch to a scene, if the timer ends. 

## Modes
**Note:** Don't forget to start the countdown with the button below. ;-)
- ``Countdown`` (countdown from specified amount of seconds)  
- ``Countup`` (starts a stopwatch timer)  
- ``Specific time`` (starts to countdown to a specific time, such as countdown to 12:00 am)  
- ``Specific date & time`` (starts to countdown to a date and time)  
- ``Streaming timer`` (starts timer when streaming starts)  
- ``Recording timer`` (starts timer when recording start)

**Modes special in advanced-timer-godi.lua** (this is mainly for sunday services)
- ``Normale GoDi`` [--> normal services] (You can just select the time when the service is starting and the countdown will get set automatically, e.g. 9:30, 10:30) 

## Settings
**Mode:**
- See **[Modes](#Modes)**

**General:**
- **"Text Source"** --> Use the drop-down menu to choose the text-source to be replaced by the timer.
- **"Next Scene"** --> Provide a scene via the drop-down if you want the script to transition to another scene, when the countdown ends.
- **"Countdown Final Text"** --> Input some text that should be displayed, if the countdown has ended. (Note that the final text is not displayed if you choosed a scene! For this to work, you have to select the empty placeholder at the top of the scenes.)
- **[Formatting](#Formatting)** of the coundown text is possible.
- **"Countup when done"** Option to countup when the countdown is finished (requires some kind of countdown mode selected)

**Activation Modes:**
- Global (the timer is always active)  
- Start timer on activation (starts timer when source is activated, such as when switching to a scene with that source or turning the visibility of the source to on)  

## Formatting 
- The default format is: ``%hh:%mm:%ss (00:00:00)``
- The infinity option is useful for leaving out the next bigger unit and including it in the smaller unit. (e.g. for leaving out hours and including the remaining hours as minutes in minutes | ``1h01min --> 61min``)


```
%d - days
%hh - hours with leading zero (00..23)
%h - hours (0..23)
%HH - hours with leading zero (00..infinity)
%H - hours (0..infinity)
%mm - minutes with leading zero (00..59)
%m - minutes (0..59)
%MM - minutes with leading zero (00..infinity)
%M - minutes (0..infinity) 
%ss - seconds with leading zero (00..59)
%s - seconds (0..59)
%SS - seconds with leading zero (00..infinity)
%S - seconds (0..infinity)
%t - tenths
%2t - hundredths
%3t - thousandths
```


## Hotkeys
Hotkeys can be set for starting/stopping and to the reset timer. --> `obs-settings/hotkeys`