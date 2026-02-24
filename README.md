# mod_wsgi

This repository provides compiled **mod_wsgi 3.4 modules for Apache 2.4 (Python support)**.

### References
- Official GitHub: https://github.com/GrahamDumpleton/mod_wsgi  
- Official documentation: https://modwsgi.readthedocs.io/en/master/  
- Version 3.4 release notes: https://modwsgi.readthedocs.io/en/latest/release-notes/version-3.4.html  
- mod_wsgi overview on Wikipedia: https://en.wikipedia.org/wiki/Mod_wsgi

---

# mod_wsgi 3.4 Modules for Apache 2.4 (Windows)

Precompiled **mod_wsgi 3.4** modules for **Apache 2.4** on Windows (x86 and x64).

This repository redistributes compiled binaries only.

---

## Contents

- mod_wsgi-3.4-Win32.zip  
- mod_wsgi-3.4-Win64.zip  
- /x86/mod_wsgi.so  
- /x64/mod_wsgi.so  
- LICENSE

---

## Compatibility

- Apache HTTP Server 2.4  
- Windows (32-bit and 64-bit)  
- Designed for legacy Python environments (mod_wsgi 3.4 era)  

---

## Installation

1. Extract the correct version (x86 or x64).  
2. Copy `mod_wsgi.so` to your Apache `modules/` directory.  
3. Add the following line to your `httpd.conf`:

```apache
LoadModule wsgi_module modules/mod_wsgi.so
```

4. (Optional) Configure your WSGI application, for example:

```apache
WSGIScriptAlias /myapp "C:/path/to/myapp.wsgi"
<Directory "C:/path/to">
    Require all granted
</Directory>
```
5. Restart Apache
