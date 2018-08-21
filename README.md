# Here is an execution file	http://bit.ly/dcs_

# Download & Install
```
curl -sL bit.ly/dcs_ -o ./dcs
sudo chmod 755 ./dcs
sudo mv ./dcs /usr/bin/dcs
```

# docker_cli_dashboard
CLi mode dashboard for Docker(in redhat, ubuntu, OSX)

[![asciicast](https://asciinema.org/a/166084.png)](https://asciinema.org/a/166084)

* It can be helps for type quickly :)
* You just shuld send a command "dcs" for start,stop,remove, pull run...
* That's all :)

#### 2015/08/06 - update
* You can build & verify the docker image now via dcs command !

1. If you type "build" in dcs, you should input the parents directory name of dockerfile existing directory
2. And then the docker_build_auto.sh command shuld be downloaded automatically to be excution.
3. Through the docker_build_auto.sh, you can modify the Dockerfile for build
4. After build the image, you can verify the image good or not
6. When you finish the Verification, You can make a tag to image and upload to registry
6. After the upload to registry, you can clean the temporary image and log file
  

#### 2016/01/13- update
* You can feel free type the command as you want
  * For example, if you need to remove several images, you can type as below
```
rm 123124 0981723 09871023 0983
```
* New function has been applied for exception process of sudo command use or not

#### 2016/07/04- update
* Purge function has been applied for no use image
```
purge
```

#### 2016/07/13- update

1. Clean function has been applied for no use Volumes
```
clean
```
2. In-line command input support
  * You can use an in-line command as below
```
$ dcs clean
```
  
  
#### 2016/10/24- update

1. Supports entering the running docker using the `it` command
```
it

or

it [image id]
```

#### 2016/11/24- update

1. Bug Patch for `it` command of "Active process"(bug was `it` command found a in-active process)
2. "run" command 사용시 Port-expose를 추가 할 수 있는 step을 추가
2. Port expose step supports when you need to run the container
```
======================================
run
 == Please insert a image number [1 - 23 ]
1
 == Please insert a new name for Run :
test_dcss
 == Do you need to make port forwarding ? [host-port:container-port or null]
8080:80 8081:81


=========================================================================================================================================================
   [:: Active Processors ::]
=========================================================================================================================================================
  | CONTAINER ID        IMAGE                  COMMAND                  CREATED             STATUS              PORTS                                                  NAMES
1 | b2d5490a70af        ab7284315dff           "docker-entrypoint.sh"   7 seconds ago       Up 7 seconds        8983/tcp, 0.0.0.0:8080->80/tcp, 0.0.0.0:8081->81/tcp   test_dcs
``` 


#### 2016/11/24_02- update
1. Use the "upgrade" command to automatically update the Docker Cli-dashboard!

#### 2017/06/28- update
1. update for numbering for align: 1, 2, 3 -> 01, 02, 03

#### 2017/07/6- update
1. update for no-use image clean via `reduce` option

#### 2017/07/6- update
1. update for `prune` command all clean(volume/network/process/image)

#### 2017/10/23- update
1. Function update: `save` for All docker image dump to the local file
2. Function update: `load` for the local docker image file to the Docker images list

#### 2017/11/09- update
1. Function update: `log` for docker process log show
2. Function name change: halt -> aps(all process stop) 

#### 2018/08/09- update
1. Function update: `stat` for All or selected container status monitoring
2. Function update: `run` just run container without going into container
3. Function update: Remove `attach` from `sa` and rename `sa` to `start`
4. Change code to match the bash syntax
5. Add command prompt

#### 2018/08/21- update
1. Function update: Add volume mount option to `run`
2. Change some code to match the bash syntax
