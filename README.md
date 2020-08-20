# Maintain - A BASH script using aptitude to handle the update of repositories and either a safe-upgrade or full-upgrade, then cleanup

__<u>Maintain</u>__ - Calls various maintenance commands using aptitude. Aptitude must be installed in order for this script to work properly.
*Install aptitude if necessary:* `apt-get install aptitude`

__<u>usage: maintain option option option__</u><br />
First option can be either y or n. This tells the script to either update (y/Y) the repositories, or not to update (n/N) them.<br />
Second option can be either y or n. This tells the script to either do a safe-upgrade (y/Y), or not to safe-upgrade (n/N).<br />
Third option can be either f/F or any character. This tells the script to either do a full-upgrade (f/F), or to not full-upgrade (any character).<br />
*All three options must be called if you want to full-upgrade, and the third option must be a f/F in order to full-upgrade.*<br /><br />

Examples:<br />
Maintain ; Doesn't call any options and walks the user through questions relating to update and upgrade.<br />
Maintain n ; Calls the script and tells it to not update the repositories, and then asks questions pertinent to upgrade.<br />
Maintain y y * ; Calls the script and tells it to update the repositories and to safe-upgrade - third option can be anything, doesn't run because of safe-upgrade.<br />
Maintain n n f ; Calls the script and tells it to not update, not to safe-upgrade, and to full-upgrade.<br />
Maintain y n f ; Calls the script and tells it to update and to full-upgrade.<br />
Maintain n y * ; Calls the script and tells it to not update and to safe-upgrade - third option can be anything, doesn't run because of safe-upgrade.<br />
Maintain n n n ; Calls the script for cleaning only. Skips update and upgrade.<br />
Maintain -h/-help/--h/--help ; Four options to call this help file.

*__Author:__ Kelly Christus (C) 2019-2020 The Nation-State of Alkemia*<br />
__Licensed for free use and alteration under The Nation-State of Alkemia's Open Software License__
