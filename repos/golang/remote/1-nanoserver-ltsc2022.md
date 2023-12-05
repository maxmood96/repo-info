## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:4a6bc1c595464b6cc4f916024390f88768481e17209425cd7fe2bace2fa429dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull golang@sha256:ed86402246e16e5d39fe0c2dfba9b4fce54c1a6521a3e7ac41dae6558205c375
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189959984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c156dacdfa2c78d04c5bb27e8629e3e1e2ae6f3da9aa7c2e1995466192d746`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Nov 2023 06:09:19 GMT
RUN Apply image 10.0.20348.2113
# Thu, 16 Nov 2023 02:53:08 GMT
SHELL [cmd /S /C]
# Thu, 16 Nov 2023 02:53:08 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:53:09 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:53:22 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 16 Nov 2023 02:53:23 GMT
USER ContainerUser
# Tue, 05 Dec 2023 20:21:34 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:23:24 GMT
COPY dir:fa545352f3e55e017c681e7849ee55f85e57ced6c9433ce00d83edb22e7b50e6 in C:\Program Files\Go 
# Tue, 05 Dec 2023 20:23:52 GMT
RUN go version
# Tue, 05 Dec 2023 20:23:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1ca4fbe907f22e883670decfa8d7f4490a79a995bb83a6c286248c21d61a62f5`  
		Last Modified: Tue, 14 Nov 2023 21:13:36 GMT  
		Size: 120.8 MB (120753560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc13ac2d02de25aafaa5c365411a34535ba58cc30cea6c804138bd620ee8c2ce`  
		Last Modified: Thu, 16 Nov 2023 03:12:33 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6786fe7e9f978f507ccf4813f375f0d544334cb2a3030c7c0b2f291c32d468b8`  
		Last Modified: Thu, 16 Nov 2023 03:12:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f24692d87e465149126eea39ee22582304c41fcd0e2affbddbe532567e15b3`  
		Last Modified: Thu, 16 Nov 2023 03:12:33 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9006c9206a76d59091068379f9331e643ac23d99a6f61bc30513cf6b4142a34e`  
		Last Modified: Thu, 16 Nov 2023 03:12:33 GMT  
		Size: 77.7 KB (77741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc2acac700a0916f870d88e4952d9629c176708d793825d3895089622b79594`  
		Last Modified: Thu, 16 Nov 2023 03:12:31 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcadea1044be3c01941c0ba8bde9dacad7da7d1e31988a1cefe65702b44c812`  
		Last Modified: Tue, 05 Dec 2023 20:39:56 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440059ad22598bd355a43cf8b0b5b8932653c112efdbd2e821133c731be7d2c3`  
		Last Modified: Tue, 05 Dec 2023 20:40:16 GMT  
		Size: 69.1 MB (69069049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9c25ec0ad0dd3e7dd5422338f05d60a0a2ad9e9933bf65c91fc05f4d4e84b3`  
		Last Modified: Tue, 05 Dec 2023 20:39:56 GMT  
		Size: 52.5 KB (52461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7364c592c4c6201425304ae2f31dd644565cdd481638b1a8d2d18c16f59f887d`  
		Last Modified: Tue, 05 Dec 2023 20:39:56 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
