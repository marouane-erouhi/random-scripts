## Convert all flac files to mp3 in current directory (with metadata)
```powershell
Get-ChildItem -file "*.flac" | Foreach-Object { ffmpeg -i $_.Name -ab 320k -map_metadata 0 -id3v2_version 3 "$($_.BaseName).mp3" }
```