## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:bb857ebd2539bad4e0a59a31d60712dda8b0ee1fea3b3c86e041847675c91236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull golang@sha256:fd912214164771dc979d4a232f7a771a2284e23df73c95c56691982b79338cc1
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192550340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22673f83d473c21663c5002f9ca42fa1cebb1bca4c85460b2bbbc3322537c6cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Tue, 14 May 2024 23:57:42 GMT
SHELL [cmd /S /C]
# Tue, 14 May 2024 23:57:43 GMT
ENV GOPATH=C:\go
# Tue, 14 May 2024 23:57:43 GMT
USER ContainerAdministrator
# Tue, 14 May 2024 23:58:03 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 14 May 2024 23:58:04 GMT
USER ContainerUser
# Tue, 14 May 2024 23:58:04 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 00:00:05 GMT
COPY dir:4d079461b01f7018cdefcf75d79e42082e4956562e5247e8be7d5083d6b6044d in C:\Program Files\Go 
# Wed, 15 May 2024 00:00:09 GMT
RUN go version
# Wed, 15 May 2024 00:00:10 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6232bca68c5e4faf7d9f262e100e36f916802bc4032b74395febec9e74d3c3`  
		Last Modified: Wed, 15 May 2024 00:00:16 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405fb04a4782998c0f787f1d43d0a48dbc5c6cdb6d12623450fd3b3cfba4c1a8`  
		Last Modified: Wed, 15 May 2024 00:00:15 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e6faefb2586cde7ee60c057bd076641787a6d78d7c8da440a2beffbd54766c`  
		Last Modified: Wed, 15 May 2024 00:00:14 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f494bca74fd1249edcd68deef4cfea7720031c4150c0562558852ddee1da35`  
		Last Modified: Wed, 15 May 2024 00:00:14 GMT  
		Size: 107.3 KB (107288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c7ff51f9c0597b07a83f28adc412fc7cd05381078e7892d4862b4ff6723cb7`  
		Last Modified: Wed, 15 May 2024 00:00:13 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a59c831fc54e91cf6eb2752faee84ba2e35179115ab6b8903cd4722b2a77f58`  
		Last Modified: Wed, 15 May 2024 00:00:13 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e610674107625b4fc84104b64ba420c7eb735cb37a0dfd3f4893a786813bcf`  
		Last Modified: Wed, 15 May 2024 00:00:25 GMT  
		Size: 71.4 MB (71353640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f05568d9a41d1ce23662b76ba450cb02d712339b5ccf9147a6a0df664ec9bd`  
		Last Modified: Wed, 15 May 2024 00:00:14 GMT  
		Size: 89.2 KB (89166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f6650f536904520ed29def5f2fbda4343df87156f63f9d27261a8399463582`  
		Last Modified: Wed, 15 May 2024 00:00:14 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
