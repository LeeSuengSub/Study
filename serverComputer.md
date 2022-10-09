## 레이드 세팅

```
Device setting -> sata -> raid -> Controller
-> capable -> Linux -> check all -> arage -> yes
-> virtual Disk -> create(raid1 선택) -> USB(OS 설치) -> 재부팅

raid : 디스크를 나누는 것.
virtual Disk : 디스크를 깨끗하게 하겠다.

순서.
1. raid 세팅
2. virtual Disk 생성
3. virtual Disk에 OS설치

raid1 - 미러링
```

## Linux 설정

```
한국어 -> 소프트웨어 선택 -> 설치대상 -> ROOT암호설정
-> 사용자 생성 -> 설치중 -> 라이센스 동의 체크
```

## Linux ip수정

```
Linux ip 확인

터미널 열기 -> ifconfig 입력


Linux ip 수정

터미널 열기
-> cd /etc/sysconfig/network-scripts
-> vi icfg-em1

IPADDR
NETMASK=255.255.255.0
DNS1
DNS2
GATEWAY=192.168.0.1
BOOTPROTO=NONE
ONBOOT=yes
```

## Linux 단축키

```
init 0 : 시스템 종료
init 6 : 재부팅
```

## VI 명령어

```
vi를 통해 파일 접근

i : input
esc : 나가기
":"(콜론) :w -> 저장
:q -> 나가기
:wq -> 저장하고 나가기

:q! -> 강제 나가기
:wq! -> 강제 저장하고 나가기

vi로 파일에 들어가서 i를 클릭후 내용을 수정한 후 esc클릭
-> (:w, :wq, :q, :q!,:wq!)중 선택
```

## chmod

```
파일 권한변경

u+(r,w,x)

r: 읽기(4)
w: 쓰기(2)
x: 실행(1)

chmod u+x [파일이름]

숫자로 한번에 권한을 수정할 수 있다.

chmod 777 [파일이름]
```

## locale 수정

```
vi /etc/locale.conf
```

## Linux 방화벽 포트

```
sudo 입력

firewall-cmd --zone (개방)
firewall-cmd --reload (재연결)
firewall-cmd --list -ports (확인)
```