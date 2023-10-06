# Linux basic commands

## Installation

Install .deb
```
sudo dpkg -i file_name
```

Install .tar.gz

```
tar xzf file.tar.gz
```

Install tar.xz 

```
tar -xf file.tar.xz 
```


## Restart print service in Unbutu
```
sudo service cups restart
```

##Matar el proceso que tiene en uso el puerto
sudo kill `sudo lsof -t -i:8080`

Forced:
sudo kill -9 `sudo lsof -t -i:8080`
 (9 is SIGKILL). See the documentation for kill for more info and How to kill a process in Ubuntu.