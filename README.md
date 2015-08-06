Here is an execution file	http://bit.do/dcs_

# docker_cli_dashboard
CLi mode dashboard for Docker(in redhat, ubuntu, OSX)

![](https://trello-attachments.s3.amazonaws.com/55825a38d0e8e46411fb808c/1138x736/d5da1142d30aac9dba2ed4adc286297c/docker_cli_dashboard.png)

* It can be helps for type quickly :)
* You just shuld send a command "dcs" for start,stop,remove, pull run...
* That's all :)

2015/08/06 - update
* Docker Cli Dashboard를 통해서 자동으로 이미지 build 및 Verification 할 수 있는 command를 추가 하였습니다. :) 

1. "build" command 입력 시, Build에 사용 될 Dockerfile이 위치한 상위 디렉토리를 입력 받습니다.
2. docker_build_auto.sh command를 해당 경로에 download 받고 해당 명령을 실행 합니다.
3. 해당 경로에 속한 Dockerfile을 수정 후 build를 진행 합니다.

 * Image verification을 위한 명령어를 CheckCommand= 변수에 지정 해 주시면 이미지가 생성 된 후 확인을 진행 합니다.

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/goody80/docker_cli_dashboard/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

