### exclude denial of service and proof of concept
```
searchsploit <term> --exclude"(POC)|/dos"
```

### use nmap XML result, print EDB-ID, exclude ssh
```
searchsploit --nmap <file.xml> --id --exclude="ssh" -e
```

### copie an exploit to the current directory
```
searchsploit -m EDB-ID <term>
```

### example: import module to metasploit
```
cd ~/.msf4/modules
mkdir -p exploits/windows/browser
cp dobe_flash_pixel_bender_bof.rb ~/.msf4/modules/exploits/windows/browser
```

