ssh 설정을 하다 권한을 잘못 건드려서 서버 접근이 불가능해졌다. 해결법으로 서버의 ssh 파일 설정을 변경하라고 하지만 이미 접근이 불가능한 상태라 새로 서버를 만들기로 했다.

- 시작

```bash
sudo apt-get update
```

- nvm 설치

⇒ ubuntu18에서는 node 18버전이 에러가 난다. 16이나 17을 설치하자

```bash
nvm install 17
nvm use 17
```

- nginx 설치

```bash
sudo npm install nginx
```

문제 발생시

nginx/sites-available 에서 “listen [::]:80 default_server;”파트를 삭제해야한다.

여러 말에 의하면 IPv6를 활성화에서 문제가 생긴다고 한다.

그 후 nginx 파일을 작성하고 https 설정을 완료한다.

- pm2 설치

설치 이후 ecosystem.config.js 설정.

다 했으면 pm2 start eco~ 실행

```bash
module.exports = {
    apps: [
        {
            name: 'backend',
            script: 'dist/main.js',
            instances: 0,
            exec_mode: 'cluster',
        },
    ],
};
```

- github actions

자동화하기위해서 deploy.sh파일 생성

```bash
cd ./web11-BOOSTPRESS
git pull
export NVM_DIR=~/.nvm
source ~/.nvm/nvm.sh
npm install
npm run build
```