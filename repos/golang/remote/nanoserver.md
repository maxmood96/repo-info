## `golang:nanoserver`

```console
$ docker pull golang@sha256:8c0985fbb63a8ec4992cd0b46b4d4e4b64a04337341b58c0ecac59e117bc8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `golang:nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull golang@sha256:9ccd7501fd24c6d5c6c935d196deb310fe6932db69cac44bee31302281caaefb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273497754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40f739ef2d915ae8575b3003ba1bd539daaa5767fd160d9ec1f6f5b2848ebc0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:11 GMT
SHELL [cmd /S /C]
# Wed, 14 May 2025 21:14:12 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 21:14:13 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:15 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 May 2025 21:14:16 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:17 GMT
ENV GOLANG_VERSION=1.24.3
# Wed, 14 May 2025 21:15:20 GMT
COPY dir:11c24136d74cfff65bad471f7cd999b92a92062aeed3b3acc0519a1823e1187a in C:\Program Files\Go 
# Wed, 14 May 2025 21:15:23 GMT
RUN go version
# Wed, 14 May 2025 21:15:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20a59e1970814df9234ccab3e3042a288705465b09e0c1a6da98da26016edf5`  
		Last Modified: Sat, 17 May 2025 16:46:21 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8595cba111c13eaa7d9fc2289472241dc3e2d47c9217371dd7d4f46e204a23`  
		Last Modified: Sat, 17 May 2025 16:46:21 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec2824be3c42d15d0661bcb1f1be5ebdbabe10e507ba49121375864aea9053e`  
		Last Modified: Sat, 17 May 2025 16:46:21 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d30965497f94ac3e97f9b6d26392628c27294fafa6ad593c0731e496ed2bf4`  
		Last Modified: Sat, 17 May 2025 16:46:21 GMT  
		Size: 76.0 KB (75967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a14114cd125e4c07f6317dadc36c08ce3fe73e676e3875344de874385a9b649`  
		Last Modified: Sat, 17 May 2025 16:46:22 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8cd6f02d4f80a6ce7948a2446e960bcf97acb518dfcbdaf33fe77012d81f8`  
		Last Modified: Sat, 17 May 2025 16:46:22 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f37c5c3e341d4264b21232fd876f5d0fa635a2b5cb356c9cc549bd21abc479d`  
		Last Modified: Sat, 17 May 2025 16:46:30 GMT  
		Size: 81.9 MB (81915515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aa8d9ccff1344b7d9a44e8a1e4c80b0c20bea015f4d75b6d45ab7a3d8837ce`  
		Last Modified: Sat, 17 May 2025 16:46:22 GMT  
		Size: 87.7 KB (87695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9524759fda7b5bd89fe0f1d62a3b671ad9f21e56b83240685cb58b2e5c0cb177`  
		Last Modified: Sat, 17 May 2025 16:46:22 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.3692; amd64

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
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed08c7b51b42d9725bc664ceaa7c63ffd2a5a9ee4632c4d799b87c1f8074e18`  
		Last Modified: Sat, 17 May 2025 05:14:13 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c5e1292fc6e0d94d931ee1322a90cac2ca5a870653c0ab2463ffa839ef7bc0`  
		Last Modified: Sat, 17 May 2025 05:14:13 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f2b978a6fbac6fbdbfddef03bbd8dd4581b0070c8f3da3c93e3e8670644ffd`  
		Last Modified: Sat, 17 May 2025 05:14:13 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48883f2a8de666240ea8ca7af19e2c37f1281a71af4909bc4bcd999c313d4f03`  
		Last Modified: Sat, 17 May 2025 05:14:13 GMT  
		Size: 76.9 KB (76933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc7d79d46b44509df4bd2fef08c0a6cff2a9bb326d0a11ba120a23c37c73e6`  
		Last Modified: Sat, 17 May 2025 05:14:13 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77074d74745b5e60413a56c0c00b90a197ef99c2ee16fbe60b085f335275e7e5`  
		Last Modified: Sat, 17 May 2025 05:14:13 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2c6be00fd1a606df6780fdbf4cc7d3e348b4950b1d8c1eb76685375b8599de`  
		Last Modified: Sat, 17 May 2025 05:14:18 GMT  
		Size: 81.9 MB (81879877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba3c351fc57de91b40ad2d40df85cb863a8be09f60dfb9967e62c542a779f5`  
		Last Modified: Sat, 17 May 2025 05:14:14 GMT  
		Size: 82.0 KB (81996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97f03b4c556b5eeb69f7b5d71c95040bd75b542362d0bf29d56a5fe1d53a995`  
		Last Modified: Sat, 17 May 2025 05:14:14 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
