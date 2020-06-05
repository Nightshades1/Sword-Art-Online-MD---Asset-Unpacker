# The Official Sword Art Online Memory Defrag Downloader And Asset Unpacker

## Features:
+ Works with all version/region of the game.
+ Download files directly from the CDN and extract all files during the download.
+ Use MD5 Checksum to download only newer or modified files (also redownload damaged files).
+ Ability to see difference(s) between Previous (Actual version) and next version (new patch)
for files added/removed and output it in a log.
+ Ability to decompress all CCZ files automatically at your own request :)
+ Lightweight software and blazing fast Multi-Threaded.

### Quick Install
Get the binaries there:https://github.com/Nightshades1/Sword-Art-Online-MD---Asset-Unpacker/releases
1. Copy "project.manifest" to "files\download" You obtain it from the game (use emulator/rooted device).
1. Do that every new version of the manifest.

### How To Use
1. Download All Assets
Click on "Manifest" -> "Download Files" (it can take a while if files are present) during the download zip files are decompressed.
If you also want to get the assets in their original format (CCZ decompressed) you might want to use "Manifest" -> "Decompress All Files" this will overwrite the corresponding asset in place so you will end with this for my case files\download\images\announcement:<a href="https://imgur.com/buv1eYT"><img src="https://i.imgur.com/buv1eYT.png" title="source: imgur.com" /></a>

### How To Use Asset Database Difference And What's That ?
Asset Database Difference is a simple way based on existing file to see what files has been added or removed
It's very usefull if you are looking for newly added content on a "newer" version of the game or what could've been retired from the game.

### A Real Example Of Asset Database Difference(s)

In this example my manifest version was 1.42.93 english version.
Click on "Manifest" -> "Differ Files" -> "Create Actual Version Database", this will ask you to save a file
by default it is named following this format:Version of the manifest_Asset Database.bin You can also change of name if needed but i do not recommend.

For me this created a "1.42.93_Asset Database.bin" This will be my "actual version" for this Asset Database, next we are going to simulate a new patch, for that i will simply add one dummy file in "files\download\images\announcement" named NewAgent.png

And remove "2018_sale_diamond_2.png" from the folder, finally i'll click again on "Manifest" -> "Differ Files" -> "Create Actual Version Database", this time since we are simulating a new patch, i'll change the version name to something imaginary 99.99.99 the name of the file is "99.99.99_Asset Database.bin"

So we now have 2 file to check the differences, our new patch, and our previous version, Click on "Manifest" -> "Differ Files" -> "Compare New Version with Previous Version Database", from there you will have to Select your actual version (for my case, 99.99.99_Asset Database.bin since it's our imaginary lastest patch/version) then obviously we select the previous version of our asset database which is "1.42.93_Asset Database.bin" for my case.

The results has been generated and the file output has been written, the name of the file will follow this format:
Name of your Current(latest) Asset Database.bin_manifestVersion_day_month_years_hours_minutes.txt for my case:99.99.99_Asset Database.bin_1.42.93_5_6_2020_2h25.txt

The result of the output is:  
[ADDED]  
files\download\images\announcement\NewAgent.png

[REMOVED]  
files\download\images\announcement\2018_sale_diamond_2.png  

# Finally Here's a kiss for you ♥
<a href="https://imgur.com/v7qMPL3"><img src="https://i.imgur.com/v7qMPL3.png" title="source: imgur.com" /></a>
