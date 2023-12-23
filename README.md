# golang-1.20-go for trusty

### install
```
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:trzsz/golang
sudo apt update
sudo apt install golang-1.20-go
```

### publish
```
wget https://go.dev/dl/go1.20.12.src.tar.gz
tar -xzf go1.20.12.src.tar.gz

cd go
debuild -d -S -k$DEBSIGN_KEYID | tee /tmp/debuild.log 2>&1

cd ..
dput ppa:trzsz/golang golang-1.20-go_1.20.12_source.changes
```
