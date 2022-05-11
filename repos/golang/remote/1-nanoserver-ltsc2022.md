## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:90c454662e6096b944ea69ba0e35eacf9aa43560c7336f03dfe9a3e6c8e3e3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull golang@sha256:7d1d3d90dacd6ad20d2ada43d9561d8dd17387a027f7b8633fb8d09260cb1aac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.0 MB (267032422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a504f93cd886f6ad55c92ac460c8f1adf6aaae806c41ca7b3820748e2438114f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 May 2022 02:37:33 GMT
RUN Apply image 10.0.20348.707
# Tue, 10 May 2022 22:28:05 GMT
SHELL [cmd /S /C]
# Tue, 10 May 2022 22:28:06 GMT
ENV GOPATH=C:\go
# Tue, 10 May 2022 22:28:07 GMT
USER ContainerAdministrator
# Tue, 10 May 2022 22:28:55 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 May 2022 22:28:56 GMT
USER ContainerUser
# Tue, 10 May 2022 22:28:57 GMT
ENV GOLANG_VERSION=1.18.2
# Tue, 10 May 2022 22:31:13 GMT
COPY dir:67f7fab8d1a7f065771db4253ddaacaab4ff63abff61135cad8768defff592fc in C:\Program Files\Go 
# Tue, 10 May 2022 22:32:08 GMT
RUN go version
# Tue, 10 May 2022 22:32:09 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2c74f0842c5a8e9b80b9e2cf64e1ab10a6fa67951f28cff5fee060b88128564c`  
		Size: 117.7 MB (117687017 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:617bb7e935bb4ca0ff934490b4a9f19a0bdedc2df4476ebd2784b3e63f7ec0eb`  
		Last Modified: Tue, 10 May 2022 22:56:44 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d185904f43d3a2981edaed48af0694ad47290902c2db8fc338def1f6d21a700`  
		Last Modified: Tue, 10 May 2022 22:56:44 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd0b6a3dc76d11dbe60ada4f477170f4156f5e8d0a1e13555d3b4c266f9258`  
		Last Modified: Tue, 10 May 2022 22:56:44 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892e1a707cb554fd1d08cd68714e3e78217f10d1c9d93a6120ea840590f89ff`  
		Last Modified: Tue, 10 May 2022 22:56:44 GMT  
		Size: 98.4 KB (98390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b0fb4392e920dc3d82438940caa8c09546cce8a9d054013225a0c792a6d5bb`  
		Last Modified: Tue, 10 May 2022 22:56:41 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b4727c585b49bd8149db7caa4b202692f092dd8b8f77e049b36b5c8bca00a4`  
		Last Modified: Tue, 10 May 2022 22:56:41 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f6af98a9eb6f86af11e834998c9bbda6bed227bb65867318cff85cb87ee601`  
		Last Modified: Tue, 10 May 2022 22:59:17 GMT  
		Size: 149.2 MB (149175785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4859e776aa707f42d0dc88b7ef206ae4e15259db82d6ef4cc5c02dd4fac512b6`  
		Last Modified: Tue, 10 May 2022 22:56:41 GMT  
		Size: 64.1 KB (64080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e06f248b072e0f931c360154415b235150eb0884bf7a10d97e1cc29244402`  
		Last Modified: Tue, 10 May 2022 22:56:41 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
