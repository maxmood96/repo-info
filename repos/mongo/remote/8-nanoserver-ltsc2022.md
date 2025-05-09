## `mongo:8-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:bf6364c03fe8f6bb5fd866d14af5854e6141c744e842fc9826448753a7891d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `mongo:8-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull mongo@sha256:7ff7d3db44ab75230e2d55e10f6f976147d624f8f9204b577db00beadb2247ce
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **895.3 MB (895343113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee83659e11a8528446b65c2fdcf4819c3fbfecd2da8b94ccc8bfbb14dce6606`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Thu, 01 May 2025 23:08:54 GMT
SHELL [cmd /S /C]
# Thu, 01 May 2025 23:08:55 GMT
USER ContainerAdministrator
# Thu, 01 May 2025 23:09:15 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 01 May 2025 23:09:15 GMT
USER ContainerUser
# Thu, 01 May 2025 23:09:19 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 01 May 2025 23:09:20 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 23:09:47 GMT
COPY dir:2013d81808dfe3aedec29f0fe3f5cee2f3dde8ce99732a408b9c6918c9a5780a in C:\mongodb 
# Thu, 01 May 2025 23:10:18 GMT
RUN mongod --version
# Thu, 01 May 2025 23:10:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 01 May 2025 23:10:20 GMT
EXPOSE 27017
# Thu, 01 May 2025 23:10:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a686134911e07edf2fda63d3d64d15cac30488d79f753fa257b234c629a10a7`  
		Last Modified: Fri, 09 May 2025 12:27:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f183967f938ab5b1db9dfa5e10398db3987055e2053342abb754ede4232365`  
		Last Modified: Fri, 09 May 2025 12:27:46 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb8f45e532aa875a51415d35ff16d04f61e9121c9f6dbb1fd1f77935f817951`  
		Last Modified: Fri, 09 May 2025 12:27:46 GMT  
		Size: 71.9 KB (71921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa98c9166e4602f833fcf40008389852838f9c92f0d96c593319ac27a165ddd`  
		Last Modified: Fri, 09 May 2025 12:27:46 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe43f10c15659b88463fadc6aed0e8791181fd606af08b65e04b4fa31e8cd0d9`  
		Last Modified: Fri, 09 May 2025 12:27:47 GMT  
		Size: 275.2 KB (275173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884eaaa12e2e5c83feecb979ad61c70ff24d480c861174cc02373dc87f23f70f`  
		Last Modified: Fri, 09 May 2025 12:27:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ab15605aca3bdc2e29c0f20e3d0b61bf53cdc40a5757b8c59f8d635c78cb4`  
		Last Modified: Thu, 01 May 2025 23:11:24 GMT  
		Size: 772.4 MB (772366357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe18f17371dc9e7353cc1bbaaf018e71f300757c75dafae2b5d0f2c18b57ca7`  
		Last Modified: Fri, 09 May 2025 12:27:47 GMT  
		Size: 83.3 KB (83281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505b09c49cf911df6ceabe3145c4c86eaaf8c6ee5399869df378acd257ba6621`  
		Last Modified: Fri, 09 May 2025 12:27:47 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59e74d29d61aafe99781861abc5dad7996b685cac818c20e95158321f253855`  
		Last Modified: Fri, 09 May 2025 12:27:46 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd424af4a7cbd2e6e71cc709c1b374cf6d66d73fe2c0cc56c44054d626e6be54`  
		Last Modified: Fri, 09 May 2025 12:27:46 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
