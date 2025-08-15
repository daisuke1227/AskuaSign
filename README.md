# AskuaSign
IPA Signing API using zsign

# Setup (Linux)
## Natively
1. Install NodeJS and NPM
    ```console
    apt install nodejs -y
    apt install npm -y
    ```

2. Update NodeJS
    ```console
    npm install -g n
    n latest
    ```
    Reconnect to SSH

3. Install MongoDB
    ```console
    apt-get install gnupg curl
    curl -fsSL https://pgp.mongodb.com/server-7.0.asc | \gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg \--dearmor
    echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list
    apt-get update
    apt-get install -y mongodb-org

    Debian swap line 3 with
    echo "deb [ signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] http://repo.mongodb.org/apt/debian bullseye/mongodb-org/7.0 main" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list
    ```

4. Install Modules
    ```console
    npm install
    ```
    
5. Modify .env

6. make zsign executeable
```console
chmod +x files/zsign/zsign
```
6. Run
    ```console
    node .
    ```

## Setup (Windows)
1. Install NodeJS/NPM https://nodejs.org/en/download

2. Install MonogoDB https://www.mongodb.com/try/download/community

3. open up cmd cd into AsukaSign and run
```
npm install
```
4. modify the env >~<

5. your all done now just run
```console
npm .
```

## Docker
1. clone repo
   ```console
   git clone --depth=1 https://github.com/Athenua/AskuaSign
   ```
2. open up `docker-compose.yml` and change `DOMAIN` on line 9 (should be able to use `http://127.0.0.1:3000` if you're only hosting locally)
3. `docker compose up -d`
4. askuasign is now running locally on http://127.0.0.1:3000 !

I love you! >:3
