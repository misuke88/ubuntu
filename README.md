# Server Setting with Ubuntu

## Ubuntu 설치

1. Bootable USB 만들기
	* Download [pendrivelinux](http://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/#button)
	* Download [Ubuntu](http://www.ubuntu.com/download)
	* 다운받은 Ubuntu iso 파일을 pendrivelinux를 사용해서 USB에 설치

2. 서버에 USB 탑재 후 컴퓨터 전원을 키고 해당 화면이 나오면 Install Ubuntu 선택
<img src="/picture/picture1.jpg"  width="70%" height="20%">

3. 다음 화면에서 continue  
<img src="/picture/picture2.jpg"  width="70%" height="40%">
4. Installation type에서 something else를 선택 후 continue  
<img src="/picture/picture3.jpg"  width="70%" height="40%">
5. 만약 새로 추가한 드라이브가 안잡힐 경우 New Partition Table를 선택 
<img src="/picture/picture4.jpg"  width="70%" height="40%">
6. Size가 보이면 Ubuntu OS를 설치하고 싶은 드라이브를 선택 후 + 버튼을 클릭  
<img src="/picture/picture5.jpg"  width="70%" height="40%">
7. 먼저 EFI boot partition에 100MB를 지정해줌  
<img src="/picture/picture6.jpg"  width="70%" height="40%">
8. Swap area에 3200MB 설정  
<img src="/picture/picture7.jpg"  width="70%" height="40%">
9. 남은 용량에 Ext4 journaling file system으로 설정하고 mount point를 다음과 같이 지정해줌
<img src="/picture/picture8.jpg"  width="70%" height="40%">
10. 남은 드라이브들도 Ext4 journaling file system으로 설정하고 원하는 mount point를 지정
<img src="/picture/picture9.jpg"  width="70%" height="40%">
<img src="/picture/picture10.jpg"  width="70%" height="40%">
11. 시간 설정 및 User 설정  
<img src="/picture/picture11.jpg"  width="70%" height="40%">
<img src="/picture/picture12.jpg"  width="70%" height="40%">
12. 설치 완료  
<img src="/picture/picture13.jpg"  width="70%" height="40%">
<img src="/picture/picture14.jpg"  width="70%" height="20%">

## Ubuntu Update

1. 설치 후 제대로 설치되었는지 확인하기 위해 터미널에서 `df -h` 입력
<img src="/picture/picture17.jpg"  width="70%" height="40%">
2. apt-get update: `sudo apt-get update`
3. apt-get upgrade: `sudo apt-get upgrade`("Do you want to continue?[Y/n]: **y**)
4. 설치 후 원격 접속을 가능하게 하기 위해 `sudo apt-get install ssh`
5. local 컴퓨터에서 접속해 보기  
<img src="/picture/picture18.jpg"  width="70%" height="20%">

## 계정 추가 및 관리자 권한 주기

1. 사용자 계정 추가: `sudo adduser <username>` -> 비밀번호 설정
2. 관리자 권한 설정: `sudo adduser <username> sudo`
<img src="/picture/picture19.jpg"  width="70%" height="20%">