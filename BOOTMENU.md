# Boot Menu

1. `bcdedit /store .\BCD /set {bootmgr} displaybootmenu on`

2. `bcdedit /store .\BCD /set {bootmgr} timeout 10`

3. `bcdedit /store .\BCD /deletevalue {bootmgr} customactions`

4. `bcdedit /store .\BCD /deletevalue {bootmgr} custom:54000001`

5. `bcdedit /store .\BCD /deletevalue {bootmgr} custom:54000002`

6. `bcdedit /store .\BCD /displayorder {default}`
