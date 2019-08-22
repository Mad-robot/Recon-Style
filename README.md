
# Recon Style :heart_eyes: :smiling_imp:

1. Subdomain emulation and Screenshot
2. Masscan and nmap
3. Cms scan
4. Dirsearch and Wfuzz
5. GitHub
6. Webarchvie
7. Js files emulation

#### 1. Subdomain emulation and Screenshot :sleepy:
Tools Used-
 > [Aquatone](https://github.com/michenriksen/aquatone)

 - aquatone-discover -d domain

 - aquatone-scan -d domain

 - aquatone-takeover -d domain

 - aquatone-gather -d domain

> [Sublist3r](https://github.com/aboul3la/Sublist3r)

 - python3 Sublister.py -u domain
 
#### 2. Masscan and nmap :astonished:
> [Masscan](https://github.com/robertdavidgraham/masscan)

-  masscan -p1-65535 10.1.1.149/32 --rate=10000

out put of masscan is taken to nmap to get details of open ports

> [Nmap](https://nmap.org/)

- nmap -v -O -A -sV -sC -p22,3128 -oN 10.1.1.149_nmap.txt 10.1.1.149

#### 3. Cms scan :fire:
> [Cmseek](https://github.com/Tuhinshubhra/CMSeeK)

```
for line in `cat /path-to-url`;
do 
python3 cmseek.py -u $line --no-redirect
done
```

#### 4. Dirsearch :boom:
> [Dirsearch](https://github.com/maurosoria/dirsearch)

- Python3 dirsearch -L /path-to-urls -e * -b --plain-text-report=output.txt

> [Wfuzz](https://github.com/xmendez/wfuzz)

- wfuzz -c -z file,/usr/share/dirbuster/wordlists/directory-list-2.3-small.txt --hc 404 http://domain/FUZZ

#### 5. GitHub :wink:
> [Gitrob](https://github.com/michenriksen/gitrob)

- GITROB_ACCESS_TOKEN=60f2675207b6c8c2aa3a2bfaadea1420b7be7021 ./gitrob dxa4481

> [Trufflehog](https://github.com/dxa4481/truffleHog)

- trufflehog git_url

> [GitGot](https://github.com/BishopFox/GitGot)

- ./gitgot.py -q domain.com

#### 6. Webarchvie :alien:
> [waybackMachine](https://github.com/ghostlulzhacks/waybackMachine)

- python waybackMachine.py facebook.com > facebook.txt


#### 7. Js files emulation :yum:
> [Linkfinder](https://github.com/GerbenJavado/LinkFinder)

For single site -

- python linkfinder.py -d domain -o domain.html

For multiple sites -

 ```
for line in `cat /path-to-url`; do python linkfinder.py -d $line -o $line.html
```
