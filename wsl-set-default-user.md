The current Microsoft recommended way of setting the username in an instance is to create a /etc/wsl.conf in the instance with the following setting:

```
[user]
default=username
```

Changing, of course, username to be your default username.

Exit your distro/instance, then issue a 
```
wsl --terminate <distroname> 
```
from PowerShell or CMD. When you restart, the default user should be set.

This is safer and less error-prone than the registry-based methods.