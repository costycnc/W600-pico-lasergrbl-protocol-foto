You can use https://bipes.net.br/aroca/web-serial-terminal/ terminal for write(comunicate) with w600-pico  

another serial terminal https://www.settorezero.com/wordpress/software/zeroterm/

Copy lines from bellow
        
    import easyw600
    easyw600.createap(ssid="W600_softAP")        
    import w600
    w600.run_ftpserver(port=21,username="user",password="user")
    
and paste in terminal with ctrl+A+V    
    
<img src="https://raw.githubusercontent.com/costycnc/W600-pico-lasergrbl-protocol-foto/main/foto/connect.jpg">        


after send these four lines ...

download https://github.com/costycnc/W600-pico-lasergrbl-protocol-foto and unzip

open wifi tab windows and connect with w600 module 

<img src="https://raw.githubusercontent.com/costycnc/W600-pico-lasergrbl-protocol-foto/main/foto/wifi.jpg"> 

open folder (that saved first) W600-pico-lasergrbl-protocol-foto-main\W600-pico-lasergrbl-protocol-foto-main\empty w600-pico

write "cmd" in adress bar folder...

<img src="https://raw.githubusercontent.com/costycnc/W600-pico-lasergrbl-protocol-foto/main/foto/connect1.jpg">      


it will open dos command prompt


and type >> ftp 192.168.43.1

will see 
        
        Connected to 192.168.43.1.
        220-= welcome on W600 FTP server =-
        220
        
insert user "user" and password "user"    

<img src="https://raw.githubusercontent.com/costycnc/W600-pico-lasergrbl-protocol-foto/main/foto/connect2.jpg">

if is correct conected with module when send "dir" will see list of all files and folders of w600 ...

<img src="https://raw.githubusercontent.com/costycnc/W600-pico-lasergrbl-protocol-foto/main/foto/connect3.jpg">

now the module accept all ftp standard commands
        
if want use mozilla ftp client ...install https://filezilla-project.org/download.php?type=client    

<img src="https://raw.githubusercontent.com/costycnc/W600-pico-lasergrbl-protocol-foto/main/foto/filezilla.jpg">
<img src="https://raw.githubusercontent.com/costycnc/W600-pico-lasergrbl-protocol-foto/main/foto/filezilla1.jpg">
<img src="https://raw.githubusercontent.com/costycnc/W600-pico-lasergrbl-protocol-foto/main/foto/filezilla2.jpg">



Keep in mind ... is a local connection (the wifi module is connected directly with your pc)... so need to discconect from router and connect to "W600_softAP" station when want upload file to w600 module

and disconnect from w600 module and connect with your wifi modem when need to navigated on internet.


If want create automatically an access point (connect directly with w600) when restart w600 ... ulpoad boot.py from ap folder

If want connect automatically w600 with your router when restart w600 ... upload boot.py from router folder

       ...
       wlan.active(True)                      
       wlan.connect("name", "psw")#insert name and password of your router
       for i in range(16):
       ...
       
change "name" and "password" with your home router name and password       

        
### Costycnc foam cutter        
        
 [<img src="https://raw.githubusercontent.com/costycnc/W600-pico-lasergrbl-protocol-foto/main/foto/costycnc.jpg">](https://youtu.be/_HhSQFuQPcA)       
