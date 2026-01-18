# windows-library-file-reverse-shell
exploiting windows .library-ms to deliver malicious payload ( Social Engineering Attack ) 

Create WebDAV server either by using python3's wsgidav

```python
/home/kali/.local/bin/wsgidav --host=0.0.0.0 --port=80 --auth=anonymous --root /home/kali/webdav/
```

or any other desired way, then paste the malicious .lnk file in that webDAV root folder

deliver the library-ms file through social engineering vector, once the victim double clicks the library-ms file , the malicious library pointing to attacker controlled webdav will be pinned with "pictures" icon, if a user clicks on the .lnk file in this webdav server contents of which will be displayed as any other benign folder in explorer.exe, reverse shell paylaod will be triggered

PS: AV might detect the malicious shortcut file, make sure you use obfuscation to avoid getting detected.
