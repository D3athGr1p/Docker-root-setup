> apt-get update

> apt-get install -y git && apt-get install -y curl && apt-get install -y wget

> apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

> curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

> echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null

> apt-get update

##### IF error (404)
```javascript
sed -i 's/debian/ubuntu/g' /etc/apt/sources.list.d/docker.list
apt update
(https://askubuntu.com/questions/1189679/apt-update-docker-com-release-404-not-found)
```

> apt-get install docker-ce docker-ce-cli containerd.io

> apt-get install systemd

> apt installl nano