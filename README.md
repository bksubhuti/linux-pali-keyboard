# linux-pali-keyboard
Pali Keyboard for Linux/Ubuntu

This file was created to help in making ubuntu keyboard setup easier.
originally taken from https://ubuntuforums.org/showthread.php?t=646207


# Instructions
sudo apt install ibus ibus-gtk ibus-m17n ibus-table

>sudo wget https://raw.githubusercontent.com/bksubhuti/linux-pali-keyboard/main/hi-itrans.mim -P  /usr/share/m17n/hi-itrans.mim

Type this to hold back changes
>echo "libm17n-0 hold" | sudo dpkg --set-selections

Type this to make Velthuis
>sudo wget https://raw.githubusercontent.com/bksubhuti/linux-pali-keyboard/main/sa-translit.mim -P /usr/share/m17n/sa-translit.mim


Edit this file to add the new files
>sudo gedit /usr/share/m17n/mdb.dir

change the following lines
>(input-method * "*.mim")
>;;; </ul>

to read
>(input-method * "*.mim")
>(input-method t sa-translit "sa-translit.mim")
>;;; </ul>







