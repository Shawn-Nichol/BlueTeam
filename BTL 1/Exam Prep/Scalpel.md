# Move scapel
Copy scapel config over to working directory and change the ownership of the file
```
sudo cp /etc/scalpel/scalpel.conf ./myscalpel.conf
sudo chown ubuntu myscalpel.conf
```


# Edit the file
Open the copy config file and and remove the # for file types you want to search
![image](https://github.com/Shawn-Nichol/BlueTeam/assets/30714313/5d4af420-620a-4ea5-a722-14fa55b13b7a)

Make a directory to save the results to
```
mkdir output
```


# Run scalpel
```
scalpel -c myscaplel.conf fileOfInterest.img -o outout
```
