# Linux Meta data commands
```
ls -lsap <file>
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/068582c4-74d6-4da0-8afa-17f52649781c)

```
stat <file>
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/3ce99528-d361-4fbf-9ca9-19f36cb2b446)

```
exifTool <file>
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/9ebfcdb3-02ff-41d0-a536-686691985caa)

how to install exifTool
```
sudo apt-get install exiftool
```

# Move scalpel
Copy the scalpel config over to the working directory and change the file ownership.
```
sudo cp /etc/scalpel/scalpel.conf ./myscalpel.conf
sudo chown ubuntu myscalpel.conf
```


# Edit the file
Open the copy config file and remove the # for file types you want to search
```
nano myscalpel.conf
```
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/5d4af420-620a-4ea5-a722-14fa55b13b7a)

Make a directory to save the results to
```
mkdir output
```


# Run scalpel
```
scalpel -c myscaplel.conf fileOfInterest.img -o output
```
