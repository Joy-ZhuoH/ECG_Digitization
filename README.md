# ECG Digitization Project

## Update conclusion
v1.0 Basic function of ECG Digitization.

## Set up environment
### Backend
install requirements.txt
```shell
python3 -m venv env 
source env/bin/activate
pip install -r requirements.txt
```
### Frontend
1. Install nvm

    `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`
    
    Close and reopen your terminal to start using nvm

2. Install node, npm 
`nvm install 16`

## Run!
### Start Backend
```shell
python ECG_web/manage.py runserver
```

remote: 
```shell
sudo ufw allow 8147
nohup python ECG_web/manage.py runserver http://... &
```
Remember! Change the `apiUrl` in src/globalData.js
This apiUrl should be the same as in backend, e.g.: `let apiUrl = "http://127.0.0.1:8000";`

### Start Frontend
```shell
cd ECG_Digitization
npm i
npm run start
```

## Shut down
Kill port
`sudo fuser -k 8147/tcp`

## Reference
[1] https://github.com/nvm-sh/nvm#installing-and-updating

