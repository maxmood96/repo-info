## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:d427cb842a46e07e8a026f57ff5f4cc04fdc889e1508af7c9f990c5c28e58066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `mongo:nanoserver` - windows version 10.0.20348.3566; amd64

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
		Last Modified: Thu, 01 May 2025 23:10:25 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f183967f938ab5b1db9dfa5e10398db3987055e2053342abb754ede4232365`  
		Last Modified: Thu, 01 May 2025 23:10:25 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb8f45e532aa875a51415d35ff16d04f61e9121c9f6dbb1fd1f77935f817951`  
		Last Modified: Thu, 01 May 2025 23:10:24 GMT  
		Size: 71.9 KB (71921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa98c9166e4602f833fcf40008389852838f9c92f0d96c593319ac27a165ddd`  
		Last Modified: Thu, 01 May 2025 23:10:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe43f10c15659b88463fadc6aed0e8791181fd606af08b65e04b4fa31e8cd0d9`  
		Last Modified: Thu, 01 May 2025 23:10:24 GMT  
		Size: 275.2 KB (275173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884eaaa12e2e5c83feecb979ad61c70ff24d480c861174cc02373dc87f23f70f`  
		Last Modified: Thu, 01 May 2025 23:10:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ab15605aca3bdc2e29c0f20e3d0b61bf53cdc40a5757b8c59f8d635c78cb4`  
		Last Modified: Thu, 01 May 2025 23:11:24 GMT  
		Size: 772.4 MB (772366357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe18f17371dc9e7353cc1bbaaf018e71f300757c75dafae2b5d0f2c18b57ca7`  
		Last Modified: Thu, 01 May 2025 23:10:23 GMT  
		Size: 83.3 KB (83281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505b09c49cf911df6ceabe3145c4c86eaaf8c6ee5399869df378acd257ba6621`  
		Last Modified: Thu, 01 May 2025 23:10:23 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59e74d29d61aafe99781861abc5dad7996b685cac818c20e95158321f253855`  
		Last Modified: Thu, 01 May 2025 23:10:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd424af4a7cbd2e6e71cc709c1b374cf6d66d73fe2c0cc56c44054d626e6be54`  
		Last Modified: Thu, 01 May 2025 23:10:23 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:2eed87560e55be2ef06724209cf3eebe40f5d0eb2bc25a893c9bfbee2bd306f3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **881.5 MB (881536379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27257933f4281590fb9923fdd18dc6085445465d84d84268fd67de362fb07ee4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Thu, 01 May 2025 23:09:38 GMT
SHELL [cmd /S /C]
# Thu, 01 May 2025 23:09:40 GMT
USER ContainerAdministrator
# Thu, 01 May 2025 23:09:56 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 01 May 2025 23:09:56 GMT
USER ContainerUser
# Thu, 01 May 2025 23:09:58 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 01 May 2025 23:09:59 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 23:10:48 GMT
COPY dir:2013d81808dfe3aedec29f0fe3f5cee2f3dde8ce99732a408b9c6918c9a5780a in C:\mongodb 
# Thu, 01 May 2025 23:11:00 GMT
RUN mongod --version
# Thu, 01 May 2025 23:11:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 01 May 2025 23:11:01 GMT
EXPOSE 27017
# Thu, 01 May 2025 23:11:02 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c088050258572ba3368f7c965f601239a38adea2b66c45bb62ef4095030b95`  
		Last Modified: Thu, 01 May 2025 23:11:06 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce10dde42931e2c453b6f72cefbb6f067dc89959972540b1dafa51bc3296f823`  
		Last Modified: Thu, 01 May 2025 23:11:06 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0537d561b3542b9ca5acf148a330307fa8e989c2f1463d75dca834ca3a9638`  
		Last Modified: Thu, 01 May 2025 23:11:05 GMT  
		Size: 67.9 KB (67913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8b3b064065ed32c59c210107312aa6a7e91c3fb2f7760377d0d85c59cf240f`  
		Last Modified: Thu, 01 May 2025 23:11:05 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8145362e11fd6829bc597ba71efd5a68d63df395ba755164b845500db75bb09e`  
		Last Modified: Thu, 01 May 2025 23:11:05 GMT  
		Size: 275.1 KB (275149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef06cfe233c34b0d0523f093395dbc16e63b563dec2ce5302fef0a3aaa761f26`  
		Last Modified: Thu, 01 May 2025 23:11:05 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06d1316ba194acce1d026d104c632b3aae1c728954c203b4d3a1d64be723f02`  
		Last Modified: Thu, 01 May 2025 23:12:06 GMT  
		Size: 772.4 MB (772366160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7122cba359a85ea7dea36877369b7807b519f074aae3ae80aea408e23c53c7`  
		Last Modified: Thu, 01 May 2025 23:11:04 GMT  
		Size: 67.6 KB (67634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd315805e343847795e286dd8c02f2e5e16bc33b68e193623cb94c0aba597e61`  
		Last Modified: Thu, 01 May 2025 23:11:04 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a87923c34a7cff2a60f6b3780fecc34c8200a4799e75f605a8d78a223696c3f`  
		Last Modified: Thu, 01 May 2025 23:11:04 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba904ea6154a46b26ed84eaf4f83806f382730e631bb55cb6cfd5869d8607712`  
		Last Modified: Thu, 01 May 2025 23:11:04 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
