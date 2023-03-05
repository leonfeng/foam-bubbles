# Inbox

-   Here you can write disorganised notes to be categorised later
-   Bullet points are useful, but it could be free form text as well
-   Sometimes it's better to just get things off your mind quickly, rather than stop to think where it belongs
-   But don't let this list get too long
-   Move information to more specific documents and link to them.
    -   This helps you navigate between documents quickly
    -   For example, you can `Cmd`+`Click` (`Ctrl`+`Click` in Windows) this: [[todo]]
-   Some notes don't end up making sense the next day
-   That's ok, you can just delete them!
    -   You can always find them in your git history, if you really need it!

<hr>

## Useful Windows Utilities

-   [0patch](https://0patch.com/): micropatches for security vulnerabilities
-   7zip-zstd
-   [chocolatey](https://chocolatey.org/)
-   [CompactGUI](https://github.com/IridiumIO/CompactGUI): transparently compresses your games and programs
-   [Cryptomator](https://cryptomator.org/): pre-Internet encryption for the cloud
-   [DNS Benchmark](https://www.grc.com/dns/benchmark.htm)
-   dnscrypt-proxy
-   [FastCopy](https://fastcopy.jp/): the Fastest Copy/Backup Software on Windows
-   [InControl](https://www.grc.com/incontrol.htm): prevents Microsoft from force upgrading your Windows
-   lsd
-   oh-my-posh
-   [PowerToys](https://learn.microsoft.com/en-us/windows/powertoys/): utilities to customize Windows
-   [Sandboxie Plus](https://sandboxie-plus.com/): sandbox-based isolation software
-   [shutup10](https://www.oo-software.com/en/shutup10): free antispy tool for Windows 10 and 11
-   [SpeedFan](https://www.almico.com/speedfan.php): access temperature sensor in your computer
-   [Syncthing](https://syncthing.net/): a continuous file synchronization program
-   [Sysinternals Suite](https://learn.microsoft.com/en-us/sysinternals/): advanced system utilities
-   tldr-plusplus
-   which
-   [wsldl](https://github.com/yuk7/wsldl): advanced WSL launcher / installer

## Useful Command Line Snippets

### Mount a USB drive in WSL:

```zsh
sudo mount -t drvfs e: /mnt/e
```

### Batch partial rename in zsh:

```zsh
zmv '(*)x264(*)' '$1av1$2'
```

### Reorganize MDX blog entries:

```zsh
for f in blog/*.mdx; do mkdir ${f:r} && mv "$f" ${f:r}/index.mdx; done
```

### Generate video previews:

```zsh
for f in *.mkv; do vcsi "$f" -t -w 850 -g 4x4 --background-color 000000 --metadata-font-color ffffff --end-delay-percent 20 --metadata-font /usr/share/fonts/TTF/DejaVuSans-Bold.ttf; done
```

### Install git with parameters on Windows 10 using Chocolatey:

```posh
choco install git -y --params "/GitAndUnixToolsOnPath /NoAutoCrlf /WindowsTerminal /DefaultBranchName:main /Editor:nvim"
```

### 字幕文件带时间戳

```shell
yt-dlp --write-auto-sub --sub-lang zh-Hans,en --convert-subs=srt ${url}
```

## WSL Troubleshooting

### WSL2 and WireGuard : WireGuard

Clipped from: https://www.reddit.com/r/WireGuard/comments/rp48lr/wsl2_and_wireguard/

> Maybe dns problem, try vpn and change the dns setting in wsl in /etc/resolv.conf, add nameserver 8.8.8.8 to the end. This change is not persist though. Change /etc/wsl.conf or creat that file, fill with in the end

```ini
[network]
generateResolvConf = false
```

## Useful JavaScript Snippets

### Complete an entire section in a Udemy course

```javascript
const section = document.querySelector('div[data-purpose="section-panel-16"]');
const checkboxes = section.querySelectorAll(
	'input[type="checkbox"]:not(:checked)'
);
for (let cb of checkboxes) {
	cb.click();
}
```

### Clear Twitter interests

```javascript
const intervalID = setInterval(() => {
	const cb = document.querySelector('input[type="checkbox"]:checked');
	if (!cb) {
		clearInterval(intervalID);
		return;
	}
	cb?.click();
}, 500);
```

### Clear Twitter topic suggestions

```javascript
const intervalID = setInterval(() => {
	const btn = document.querySelector('div[aria-label*="Dismiss"]');
	if (!btn) {
		clearInterval(intervalID);
		return;
	}
	btn?.click();
}, 500);
```
