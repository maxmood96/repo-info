## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:ec526dd724502b3221cd796a0175070fed8b51b0c9d07d985ada2fd93c946d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull golang@sha256:d1a3fa70f6bc6544e3e3a58cf5ff3a1a4f6da979223ac722d11dc0231e673b19
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204621798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4fd9d5bc16ff7407d9c21d1bf09fc52d259576bff2a7d05b6cecbcf119700b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:20:35 GMT
SHELL [cmd /S /C]
# Wed, 14 May 2025 21:20:35 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 21:20:36 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:20:38 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 May 2025 21:20:39 GMT
USER ContainerUser
# Wed, 14 May 2025 21:20:39 GMT
ENV GOLANG_VERSION=1.24.3
# Wed, 14 May 2025 21:22:56 GMT
COPY dir:11c24136d74cfff65bad471f7cd999b92a92062aeed3b3acc0519a1823e1187a in C:\Program Files\Go 
# Wed, 14 May 2025 21:23:00 GMT
RUN go version
# Wed, 14 May 2025 21:23:00 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Tue, 13 May 2025 19:42:18 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed08c7b51b42d9725bc664ceaa7c63ffd2a5a9ee4632c4d799b87c1f8074e18`  
		Last Modified: Wed, 14 May 2025 21:23:04 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c5e1292fc6e0d94d931ee1322a90cac2ca5a870653c0ab2463ffa839ef7bc0`  
		Last Modified: Wed, 14 May 2025 21:23:04 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2b978a6fbac6fbdbfddef03bbd8dd4581b0070c8f3da3c93e3e8670644ffd`  
		Last Modified: Wed, 14 May 2025 21:23:04 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48883f2a8de666240ea8ca7af19e2c37f1281a71af4909bc4bcd999c313d4f03`  
		Last Modified: Wed, 14 May 2025 21:23:04 GMT  
		Size: 76.9 KB (76933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc7d79d46b44509df4bd2fef08c0a6cff2a9bb326d0a11ba120a23c37c73e6`  
		Last Modified: Wed, 14 May 2025 21:23:03 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77074d74745b5e60413a56c0c00b90a197ef99c2ee16fbe60b085f335275e7e5`  
		Last Modified: Wed, 14 May 2025 21:23:03 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2c6be00fd1a606df6780fdbf4cc7d3e348b4950b1d8c1eb76685375b8599de`  
		Last Modified: Wed, 14 May 2025 21:23:15 GMT  
		Size: 81.9 MB (81879877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba3c351fc57de91b40ad2d40df85cb863a8be09f60dfb9967e62c542a779f5`  
		Last Modified: Wed, 14 May 2025 21:23:03 GMT  
		Size: 82.0 KB (81996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97f03b4c556b5eeb69f7b5d71c95040bd75b542362d0bf29d56a5fe1d53a995`  
		Last Modified: Wed, 14 May 2025 21:23:03 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
