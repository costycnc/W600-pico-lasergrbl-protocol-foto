You can use this terminal for write(comunicate) with w600-pico https://bipes.net.br/aroca/web-serial-terminal/ 

Paste in terminal with ctrl+A+V
        
    import easyw600
    easyw600.createap(ssid="W600_softAP")        
    import w600
    w600.run_ftpserver(port=21,username="user",password="12345678")
    
        
after send these four lines if not have a ftp you can use dos command prompt >> ftp 192.168.43.1

will see 
        
        Connected to 192.168.43.1.
        220-= welcome on W600 FTP server =-
        220
        
        or...
        
install https://filezilla-project.org/download.php?type=client

        and connect at 192.168.43.1 user 12345678
        and will see all files and folders from w600-pico
        Keep in mind ... is a local connection ... so need to discconect from router and connect to "W600_softAP" station