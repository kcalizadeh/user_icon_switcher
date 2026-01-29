### User Icon Switcher

This script takes icons from a user-designated folder, selects one randomly, and places it in the relevant system folder. The result is a randomized change to the user profile icon. This can then be set to run automatically so you get a new icon with every session.

To use:
- Create a folder to store the selection of random profile pictures in. Script defaults to ~/home/<user>/Pictures/user_icons. Modify the SOURCE_DIR variable with the appropriate path.
- Identity your system's icon folder. The script defaults to /var/lib/AccountsService/icons which is appropriate for the KDE Plasma Login Manager. Will need to be adjusted if using SDDM or another login manager. Modify the DEST_DIR variable with the appropriate path.
- Modify the USERNAME variable with your username. 

You can then run the script manually or set it up to run at system boot or shutdown, for example by adding to the exec-once section of your hyprland config. 

Notes:
- Icons typically must be in png. 
- Plasma looks for an icon named '<user>' in the relevant folder; other tools prefer names like 'face' or 'face.icon'. You may need to change the renaming section of the script accordingly.
- Plasma will automatically crop your icon to a circle, centered on the center of the image.

