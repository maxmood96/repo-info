## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:afdf65b8a9678307898c8762e31ab2ceb3ec023761544cdee4e9dcf368282acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull golang@sha256:abd2ff423b6cab9ba824904827850786201036edaf7a6cccaa573607fd2c5aba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197782527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0f8f969f49d36d27c4059f99ea799852131e3f38eb86cb17a7553b78625286`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Thu, 16 Jan 2025 22:56:45 GMT
SHELL [cmd /S /C]
# Thu, 16 Jan 2025 22:56:46 GMT
ENV GOPATH=C:\go
# Thu, 16 Jan 2025 22:56:46 GMT
USER ContainerAdministrator
# Thu, 16 Jan 2025 22:56:48 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 16 Jan 2025 22:56:49 GMT
USER ContainerUser
# Thu, 16 Jan 2025 22:56:50 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 22:58:54 GMT
COPY dir:686423f35bba4280be244c38d9d939799b38be8e943dabfe1a129b187496242a in C:\Program Files\Go 
# Thu, 16 Jan 2025 22:58:57 GMT
RUN go version
# Thu, 16 Jan 2025 22:58:58 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a74ff023c34672bc6342d9a966e984a037cd0ce1c5685fcb949eb067e7e201`  
		Last Modified: Thu, 16 Jan 2025 22:59:04 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0c2f0693957324ea78289b63acf0c296a57524c788d3d2e3411346cf08e129`  
		Last Modified: Thu, 16 Jan 2025 22:59:04 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991c43c51ce7a881e54c74bb6d249075c2757904c585ff1bfdb40699f14708d5`  
		Last Modified: Thu, 16 Jan 2025 22:59:04 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c533d930dd50f36824c5c08269e0646d5d36cbb655a9593b17b7197edf9f66af`  
		Last Modified: Thu, 16 Jan 2025 22:59:04 GMT  
		Size: 77.3 KB (77311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea82bda638fa607f137d1cb6d9662b41aa492105c6658eb60e0a931577f3340b`  
		Last Modified: Thu, 16 Jan 2025 22:59:02 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c55ec2070dff390df3fc65fb9ec22b639bd982693f28ca362cb36c5bfca977`  
		Last Modified: Thu, 16 Jan 2025 22:59:02 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e724dfb3c501f4565bf97ad56d9af43db99472e70f5089e8d3a95a7326eedc4`  
		Last Modified: Thu, 16 Jan 2025 22:59:14 GMT  
		Size: 77.0 MB (76951270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468df26272102c6f9c541ff36441c37d8fc8f6c20cedd854cfe56c05693ee27f`  
		Last Modified: Thu, 16 Jan 2025 22:59:02 GMT  
		Size: 86.0 KB (86006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02f2f82d6d41bfa154523d613bb7e66dabceee24c0d25d76568b6c87cdb42b`  
		Last Modified: Thu, 16 Jan 2025 22:59:02 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
