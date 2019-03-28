# Docker Command

#### * _update: 2019.03.28_

<br>
<br>

### ■ 컨테이너 목록 확인
> : docker ps
 - **실행중인** 컨테이너 목록을 보여준다. detached mode로 실행중인 컨테이너들이 보인다.
 - 어떤 이미지를 기반으로 만들었는지 어떤 포트와 연결이 되어있는지 등 간단한 내용을 보여준다.
> : docker ps -a
 - 모든 컨테이너 목록을 보여준다.
 - 종료된 컨테이너도 보여준다. (컨테이너는 종료되어도 삭제되지 않고 남아있다.)
 - 종료된 건 다시 시작할 수 있고 컨테이너의 읽기/쓰기 레이어는 그대로 존재한다.



<br>


### ■ docker run
> : docker run OOOOO
 - run 명령어를 사용하면 사용할 이미지가 저장되어 있는지 확인하고 없다면 다운로드(pull)를 한 후 컨테이너를 생성(create)하고 시작(start)한다.

> : docker run -p 2181:2181 --name zookeeper01 -d zookeeper
 - [-p] : 포트번호 설정
 - [--name] : 이름 설정
 - [-d] : 데몬


<br>


### ■ 컨테이너 중지 (stop)
> : docker stop (컨테이너 ID)
 - 도커 ID의 전체 길이는 64자리이다.
 - 하지만 명령어의 인자로 전달할 때는 전부 입력하지 않아도 된다. 예를 들어 ID가 abcdefgh... 라면 abcd만 입력해도 된다. 앞부분이 겹치지 않는다면 1~2자만 입력해도 된다.
> : docker stop 컨테이너ID 컨테이너ID 컨테이너ID ...
 - 동시에 여러개의 컨테이너를 stop 하려면 컨테이너ID를 여러개 쓰면 된다.
 - 컨테이너ID는 명령어의 인자로 전달할 때 전부 입력하지 않아도 된다. (겹치지만 않는다면)


<br>


### ■ 이미지 목록 확인 (images)
> : docker images


<br>


### ■ 이미지 다운로드하기 (pull)
> : docker pull 이미지명
 - (ex) docker pull ubuntu:14.04
 - (ex) docker pull zookeeper


<br>


### ■ 이미지 삭제하기 (rmi)
> : docker rmi 이미지ID
 - 컨테이너가 실행중인 이미지는 삭제되지 않는다.


<br>






● 



● 