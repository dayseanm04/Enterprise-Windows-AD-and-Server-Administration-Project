# Configure File and Folder Auditing

## Overview
Turning on Object Access auditing at the GPO level doesn't log anything by itself — it just tells Windows to *pay attention* to file activity. To actually get events in the log, I still have to tell Windows which folder to watch and what actions on it count as worth logging. I'm setting this up on the Finance-Folder, since that's the folder I want to track changes on.
