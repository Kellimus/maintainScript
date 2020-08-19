# Maintain — A BASH Script running Aptitude (and apt-get for cleaning files) for step-by-step maintenance, or automated maintenance

**Maintain** — Calls various maintenance commands using aptitude. Aptitude must be installed in order for this script to properly work.
Install aptitude if necessary: ``apt-get install aptitude``

**usage: maintain option option option**  
First option can be either y or n. This tells the script to either update (y/Y) the repositories, or not to update (n/N) them.  
Second option can be either y or n. This tells the script to either do a safe-upgrade (y/Y), or not to safe-upgrade (n/N).  
Third option can be either f/F or any key. This tells the script to either do a full-upgrade (f/F), or to not full-upgrade (any character).  
__*All three options must be called if you want to full-upgrade, and the third option must be a f/F in order to full-upgrade.*__

Examples:  
Maintain | Doesn't call any options and walks the user through questions relating to update and upgrade  
Maintain n | Calls the script and tells it to not update the respositories, and then asks questions pertinent to upgrade  
Maintain y y * | Calls the script and tells it to update the repositories, and to safe-upgrade; third option can be anything, doesn't run because of safe-upgrade  
Maintain n n f | Calls the script and tells it not to update, not to safe-upgrade, and to full-upgrade  
Maintain y n f | Calls the script and tells it to update and to full-upgrade  
Maintain n y * | Calls the script and tells it to not update and to safe-upgrade; third option can be anything, doesn't run because of safe-upgrade  
Maintain n n n | Calls the script for cleaning only. Does not update or upgrade  
Maintain -h/-help/--h/--help | Four options to call this help file  

_Author: Kelly Christus (C) 2019-2020 The Nation-State of Alkemia_  
__Licensed for free use and alteration under The Nation-State of Alkemia's Open Software License__
