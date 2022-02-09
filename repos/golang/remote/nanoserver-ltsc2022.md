## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:82e1b49da3594d1b27e37ddd30c6f881569f4282e8abb9636466d7e2fd6cbf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull golang@sha256:5107e6435698c4d97c4bce4421a460e2ed759513638e3f4fdff3df6be0696f8c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262696442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70945021806e8da2f428961895d7eaa9dd2dd60173b87e9dbe9844b5631e910d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 01 Feb 2022 02:25:40 GMT
RUN Apply image ltsc2022-amd64
# Wed, 09 Feb 2022 13:48:34 GMT
SHELL [cmd /S /C]
# Wed, 09 Feb 2022 13:48:35 GMT
ENV GOPATH=C:\go
# Wed, 09 Feb 2022 13:48:36 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 13:49:22 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Feb 2022 13:49:22 GMT
USER ContainerUser
# Wed, 09 Feb 2022 14:04:34 GMT
ENV GOLANG_VERSION=1.17.6
# Wed, 09 Feb 2022 14:07:00 GMT
COPY dir:7d325dd3c7e81bd29326c5fb7b320ff307098f97c2703658681dad899622f617 in C:\Program Files\Go 
# Wed, 09 Feb 2022 14:07:51 GMT
RUN go version
# Wed, 09 Feb 2022 14:07:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3ab33c1d9cc1eaef56d5617b87373ead45d8a4ff7ab7da384afe612ba569a524`  
		Size: 117.5 MB (117457656 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d52811c4b439c00c93423790e004fc266374135015625d93ffb80def500d7b64`  
		Last Modified: Wed, 09 Feb 2022 14:34:32 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263041b42d7aee90b2defa92fc60f7db99cbbb4686f589864f236b46225ac2a3`  
		Last Modified: Wed, 09 Feb 2022 14:34:31 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0167ac52d6f1254de3c047db124eaa082939ef069a8951247813c10025676d6b`  
		Last Modified: Wed, 09 Feb 2022 14:34:31 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95619fbd5e91dcd251f92bd790e401d548ac0352fc1c7ec9b7a17fd0e46cfdf3`  
		Last Modified: Wed, 09 Feb 2022 14:34:32 GMT  
		Size: 87.2 KB (87240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c044d79e4b1aeb1f8dfdb389f38af55837434f7ff54f3b66176470da6c2c8c`  
		Last Modified: Wed, 09 Feb 2022 14:34:29 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec33e49583534f8de106c8930b8621ea95150e7d5cb227ad216f7b4e6b189cf`  
		Last Modified: Wed, 09 Feb 2022 14:46:29 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38740887ab45281a3dc07f69fe5165b54fde8c4f9551b26ff10b9f4ffcf5a09a`  
		Last Modified: Wed, 09 Feb 2022 14:49:01 GMT  
		Size: 145.1 MB (145096694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7e3e2f4a382cb048643f62f327db3194db6bf179b9ca54b9d5dd9ef0d9f04c`  
		Last Modified: Wed, 09 Feb 2022 14:46:29 GMT  
		Size: 47.7 KB (47714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddddc294528b9f75d305a1180a4c6bd97cf315128e111e1d4459fd5ab78827b`  
		Last Modified: Wed, 09 Feb 2022 14:46:29 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
