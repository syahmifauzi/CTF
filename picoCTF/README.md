# picoCTF{flag-here}

## Steps
1. `$ wget <url>`
2. `$ file <filename>` 
3. `$ tldr grep`
4. `$ curl cht.sh/<tool>/<anything>`

## Forensics Tools
1. strings
2. hexeditor
3. [Steganography Online](https://stylesuxx.github.io/steganography/)
4. wireshark
5. tshark
6. tcpflow
7. [CyberChef](https://gchq.github.io/CyberChef/)
8. pngcheck

## To Look Back Later

### tshark batch mode
- `$ for stream in 'tshark -r follow_tcp.pcap -R "ip.addr eq 127.0.0.1 and tcp.port eq 5678" -T fields -e tcp.stream | sort -n -u'; do echo Stream: $stream; tshark -r follow_tcp.pcap -q -z follow,tcp,ascii,$stream; done`
> source: [Maybe use tcpflow](https://osqa-ask.wireshark.org/questions/14811/follow-tcp-stream-with-tshark-still-can-not-in-batch-mode)

### wireshark filters 
- `tcp or frame contains '{'`
- `tcp or frame contains pico`

### tshark commands
- `$ tshark -r capture.pcap -Y "frame contains '{'"`
- `$ tshark -r capture.pcap -Y 'frame contains pico'`
- `$ tshark -r capture.pcap -z follow,udp,ascii,10.0.0.2:5000,10.0.0.13:8888`

### tcpflow commands
- `$ tcpflow -a -r filename.pcap -o outdir`

### vim search
- `ga` # view character code
- `:%s/\%x20/0/g`
- `:%s/\%x20/1/g`
- `:%s/foo/bar/g` # replace all foo with bar
