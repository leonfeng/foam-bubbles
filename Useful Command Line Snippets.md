# Useful Command Line Snippets

## Mount a USB drive in WSL:

```zsh
sudo mount -t drvfs e: /mnt/e
```

## Batch partial rename in zsh:

```zsh
zmv '(*)x264(*)' '$1av1$2'
```

## Reorganize MDX blog entries:

```zsh
for f in blog/*.mdx; do mkdir ${f:r} && mv "$f" ${f:r}/index.mdx; done
```

## Generate video previews:

```zsh
for f in *.mkv; do vcsi "$f" -t -w 850 -g 4x4 --background-color 000000 --metadata-font-color ffffff --end-delay-percent 20 --metadata-font /usr/share/fonts/TTF/DejaVuSans-Bold.ttf; done
```

## Install git with parameters on Windows 10 using Chocolatey:

```posh
choco install git -y --params "/GitAndUnixToolsOnPath /NoAutoCrlf /WindowsTerminal /DefaultBranchName:main /Editor:nvim"
```

## Download a YouTube video with subtitles

```shell
yt-dlp --write-auto-sub --sub-lang zh-Hans,en --convert-subs=srt ${url}
```

## Securely wipe an Android phone’s free space in Termux

-   [ ] TODO: test on a device

```shell
# Generate a large file that fills up the free space
fallocate -l 2T big_file
# Overwrite the file with random data and delete it
shred -n7 -uv big_file
```

## Add sequential tasks in zsh

```zsh
for i in {17..60}; do task add pro:普通话考试短文 pri:M 录制第`echo $i`篇短文; done
```

## Print $PATH, one segment per line

```shell
echo $PATH | tr ':' '\n' | sort
```

## Save SSH key passphrase on demand

```shell
eval $(keychain --eval --quiet id_ed25519 ~/.ssh/id_ed25519)
```

## Add tasks from a list of items

```zsh
#!/bin/zsh
# File: readfile.zsh
# Usage: chmod +x readfile.zsh
# 		./readfile.zsh myfile.txt

if [ -z "$1" ]; then
	echo "Please specify a text file to read."
	exit 1
fi

if [ ! -f "$1" ]; then
	echo "File '$1' not found."
	exit 1
fi

while read -r line; do
	task add pro:clean-apt pri:L due:eow recur:weekly +home "Clean the `echo "$line"`"
done < "$1"
```
