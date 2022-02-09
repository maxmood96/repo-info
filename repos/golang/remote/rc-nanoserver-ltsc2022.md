## `golang:rc-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:5b577ce1455a804f07b330903f1d6ead7848cafeae86a787322266b24bf46a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `golang:rc-nanoserver-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull golang@sha256:9245c2ead1a11439aae05f999a1338ae9bdf2048c99435e0385f3e7291019e51
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269639452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7ca2b2c7cde13b2fe89ee99f557cd7fd30bae4c58f450fcd983e76edadd748`
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
# Wed, 09 Feb 2022 13:49:23 GMT
ENV GOLANG_VERSION=1.18beta2
# Wed, 09 Feb 2022 13:52:13 GMT
COPY dir:71b79cea25a0f7926c53d5d3ecfe583efc6c6e6b413ed2254acd66bf37c90389 in C:\Program Files\Go 
# Wed, 09 Feb 2022 13:53:03 GMT
RUN go version
# Wed, 09 Feb 2022 13:53:05 GMT
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
	-	`sha256:0e8925464a42791d5ffd6920625f7e40ea8e78a95483c3a4b3e8bd674c4444f3`  
		Last Modified: Wed, 09 Feb 2022 14:34:29 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7754301e5312dc9c34d5394b695a3c393af12facb2d2bec78a4f4adf08f5f342`  
		Last Modified: Wed, 09 Feb 2022 14:37:18 GMT  
		Size: 152.0 MB (152039241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26137810b0657186284e0b52713bdb059686a23cb9f2353d978703e5247b30cf`  
		Last Modified: Wed, 09 Feb 2022 14:34:30 GMT  
		Size: 48.2 KB (48195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480f94e6586f81893aa3d409895bffd5553f79027f9292c5bed552ef40fcd9b4`  
		Last Modified: Wed, 09 Feb 2022 14:34:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
