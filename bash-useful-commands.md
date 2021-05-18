# Useful Bash tips

## Bash and Zsh Shortcuts

`CTRL + A`	Move to the beginning of the line
`CTRL + E`	Move to the end of the line
`CTRL + [left arrow]`	Move one word backward (on some systems this is ALT + B)
`CTRL + [right arrow]`	Move one word forward (on some systems this is ALT + F)
`CTRL + U (bash)`	Clear the characters on the line before the current cursor position
`CTRL + U (zsh)`	If you're using the zsh, this will clear the entire line
`CTRL + K`	Clear the characters on the line after the current cursor position
`ESC + [backspace]`	Delete the word in front of the cursor
`CTRL + W`	Delete the word in front of the cursor
`ALT + D `       Delete the word after the cursor
`CTRL + R`	Search history
`CTRL + G`	Escape from search mode
`CTRL + _`	Undo the last change
`CTRL + L`	Clear screen
`CTRL + S`	Stop output to screen
`CTRL + Q`	Re-enable screen output
`CTRL + C`	Terminate/kill current foreground process
`CTRL + Z`	Suspend/stop current foreground process
Command	Action
`!!`	Execute last command in history
`!abc`	Execute last command in history beginning with abc
`!abc:p`	Print last command in history beginning with abc

## Pacman

### Reset pacman lock file

This can happen when something goes wrong when installing a package. The pacman lock file remains stuck. To unlock remove the lock file.

```
  sudo rm /var/lib/pacman/db.lck
```

## Grep

### Recursive search through folder

```
grep -rni "string" *
```

where,

r = recursive i.e, search subdirectories within the current directory
n = to print the line numbers to stdout
i = case insensitive search 

## ImageMagick

### Convert `.jpeg` to `.png` and vice verse

```
magick convert rose.jpg rose.png
```

### Compress .jpeg file

```
magick "input.jpg" -strip -interlace Plane -gaussian-blur 0.05 -quality 85% "output.jpg"
```

### Compress every .jpg file in directory

```
for file in ./*              
	do
		magick "$file" -strip -interlace Plane -gaussian-blur 0.05 -quality 85% "$file"
		count=$(( $count + 1 ))
		echo "Compressed $file, total compressed $count files"
	done
```
