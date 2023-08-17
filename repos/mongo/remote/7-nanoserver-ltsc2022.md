## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:74fc59ba58f4a2de5790ee94da19a81a4db5a75cb6e6c4be7d5e59202eb2499e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull mongo@sha256:55853da29a309525df1ebdfe84dcca1001166c7f84908928f6ef19f55cd7f1b4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.5 MB (731496735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83b3947c79fd2f4821c72e8cfee77d65db6a7b1db04a4ee81bf9a221acd7be0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:45:25 GMT
SHELL [cmd /S /C]
# Thu, 10 Aug 2023 01:14:21 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 01:14:29 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Aug 2023 01:14:30 GMT
USER ContainerUser
# Thu, 10 Aug 2023 01:14:31 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Thu, 17 Aug 2023 20:22:12 GMT
ENV MONGO_VERSION=7.0.0
# Thu, 17 Aug 2023 20:23:01 GMT
COPY dir:52c2b0def258ae637a0b5523eab235ea2346de3e4d510b59414991e5921a2c6f in C:\mongodb 
# Thu, 17 Aug 2023 20:23:24 GMT
RUN mongod --version
# Thu, 17 Aug 2023 20:23:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 17 Aug 2023 20:23:26 GMT
EXPOSE 27017
# Thu, 17 Aug 2023 20:23:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a528e77cf0bef98e15c3b4194ee340960485498ac4c1bdcbab44307858ecfc4`  
		Last Modified: Thu, 10 Aug 2023 01:03:26 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0247382dbd5864284425d3942427091871bf5f10629f0608efbc6b3303d067`  
		Last Modified: Thu, 10 Aug 2023 01:59:00 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ffaf70bb154004aa4faefa8b8926380d11a591157ac5074e2438ce1696d3ac`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 77.9 KB (77932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54933f30fc7826d81c7a7731e98cb5ea37dd377d70a605f59fda57f3a196506c`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa6daf2a597ffb630f230ca7808bb850f20a800b5ffaf16207e74b4405ba9ff`  
		Last Modified: Thu, 10 Aug 2023 01:58:58 GMT  
		Size: 267.2 KB (267199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de208454f05538e209e91c30edfed61e4afe50c5f4ae68367710f71c54f3d1f0`  
		Last Modified: Thu, 17 Aug 2023 20:31:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748814ae36d78c1e776a804b21b1aade6de3d602abe53973601e8b86647b7651`  
		Last Modified: Thu, 17 Aug 2023 20:33:18 GMT  
		Size: 610.6 MB (610581933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0647be16a19aa87379370b7dbd14a1ff75ad99d23fb0a701eb9027ca264187`  
		Last Modified: Thu, 17 Aug 2023 20:31:43 GMT  
		Size: 60.8 KB (60842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0327a2bc41fdcb286c44fe4019901d0013cf4ab4522f2dbea57c6bd56a7840a`  
		Last Modified: Thu, 17 Aug 2023 20:31:43 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015d8c1382f7d52d2a038bf61c8d007ee748189ea51ef205cceedc75359aba4b`  
		Last Modified: Thu, 17 Aug 2023 20:31:43 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a633df621ac5359eaca789df08b7dbf196e13c49f59a284b63590d1d086e1a7d`  
		Last Modified: Thu, 17 Aug 2023 20:31:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
