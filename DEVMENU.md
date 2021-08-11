# Install Developer Menu

1. Copy developermenu.efi and ui/ to Windows/System32/BOOT/

2. `bcdedit /store .\BCD /create /d "Developer Menu" /application BOOTAPP`

3. Copy the GUILD with the brackets. From now on paste that in place of <guid>

4. `bcdedit /store .\BCD /set <guid> path \Windows\System32\BOOT\developermenu.efi`

5. `bcdedit /store .\BCD /set <guid> device partition=<path to the partition containing your efi>`

6. `bcdedit /store .\BCD /set <guid> testsigning on`

7. `bcdedit /store .\BCD /set <guid> nointegritychecks on`

8. `bcdedit /store .\BCD /displayorder <guid> /addlast` Note this will only show up if the boot menu is turned on
