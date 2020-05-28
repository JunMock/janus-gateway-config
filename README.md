# janus-gateway-config

## janus WebRTC Server Ubuntu 18.04 환경 설정

[janus 깃허브](https://github.com/meetecho/janus-gateway)

## 1. 전체 설치

aws ec2 (ubunto 18.04) 인스턴스 생성 후  
원하는 디렉토리에서 시작.

```text
sudo apt-get update
git clone https://github.com/JunMock/janus-gateway-config.git
cd janus-gateway-config
bash install_dependencies.sh
bash install_libnice.sh
bash install_libsrtp.sh
bash install_usrsctp.sh
bash install_libwebsockets.sh
```

선택 사항입니다.  
필요에따라 설치해주세요

```text
bash install_mqtt.sh
sudo apt-get update
sudo apt-get install libnanomsg-dev
bash install_rabbitmqc.sh
```

```text
git clone https://github.com/meetecho/janus-gateway.git
cd janus-gateway
sh autogen.sh
./configure --prefix=/opt/janus
make
make install
make configs
/opt/janus/bin/janus --help
```

## 2. shell script 설명

### 2-1. 의존성 설치

Janus를 소스에서 컴파일하여 Ubuntu 18.04 배포판에 설치하려면 시스템에 다음과 같은 종속성이 설치되어 있어야합니다.  
(install_dependencies.sh)

- git
- libmicrohttpd-dev
- libjansson-dev
- libssl-dev
- libsrtp-dev
- libsofia-sip-ua-dev
- libglib2.0-dev
- libopus-dev
- libogg-dev
- libcurl4-openssl-dev
- liblua5.3-dev
- libconfig-dev
- pkg-config
- gengetopt
- libtool
- automake
- gtk-doc-tools
- cmake

### 2-2 libnice 다운로드 및 컴파일

### 2-3 libsrtp 설치

### 2-4 usrsctp 설치

### 2-5 libwebsockets 설치

### 2-6 MQTT 설치 (선택 사항)

### 2-7 NanoMSG 설치 (선택 사항)

### 2-8 RabbitMQ C AMQP 설치 (선택 사항)

## 3. janus-gateway

### 3-1. janus-gateway 컴파일

### 3-2. janus test