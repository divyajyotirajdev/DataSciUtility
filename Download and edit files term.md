## Download and edit files from term
Citations: multiple stack overflow posts 

1. download 
```
wget -r -A 'samplepattern*.zip' 'link to download from'
```
2. unzip (in current dir)
```
unzip \*.zip
```
3. Remove first line from say all csv or txt
```
sed -i .bak -e 1d file.csv
rm *.bak
```
use `2d` to remove first data line

4. concatenate all to 1 file
```
cat ./*.csv >> filename.csv
```

5. Move
```
mv sourcepath/filename.txt destfolder
```
