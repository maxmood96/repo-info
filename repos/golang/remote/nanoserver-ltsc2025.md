## `golang:nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:4210c668f111b14beb0b169047f0286f577d664dac3c9477b85647b894c2f1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `golang:nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull golang@sha256:88f6e61d95039b06d29cdd505675c21a5533d851d78fa1efe887016b22287b0f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272231152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8819688e3150fc56db0ec2676157a17856d7284f1bb8fb19c67cc9585023a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Tue, 06 May 2025 20:14:53 GMT
SHELL [cmd /S /C]
# Tue, 06 May 2025 20:14:54 GMT
ENV GOPATH=C:\go
# Tue, 06 May 2025 20:14:55 GMT
USER ContainerAdministrator
# Tue, 06 May 2025 20:14:58 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 06 May 2025 20:14:59 GMT
USER ContainerUser
# Tue, 06 May 2025 20:15:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 20:16:13 GMT
COPY dir:11c24136d74cfff65bad471f7cd999b92a92062aeed3b3acc0519a1823e1187a in C:\Program Files\Go 
# Tue, 06 May 2025 20:16:15 GMT
RUN go version
# Tue, 06 May 2025 20:16:16 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881d24be1f0f0767fa1fd23016064cfdc9e0d8cdead320b446b1d62f91dc0141`  
		Last Modified: Tue, 06 May 2025 20:16:20 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0986d48d0922c1706cb85086f426c1a493aa360fb9da9ed5fced67257f6bae`  
		Last Modified: Tue, 06 May 2025 20:16:20 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ec46f4a202682e4e2953287cd08c4e97ddc9e37dd6e594c82521261a367720`  
		Last Modified: Tue, 06 May 2025 20:16:20 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1726c2ee485233e9dda9dabe778396d94725a225dbc57cf2ceea1426029bb5c`  
		Last Modified: Tue, 06 May 2025 20:16:20 GMT  
		Size: 76.7 KB (76728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fa836da8150f483a80e505eaaeadbd75839c36e85f55ee2bc5c18b13b288ac`  
		Last Modified: Tue, 06 May 2025 20:16:19 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949916d8ea5e7f5c18aeb8ddbb75f00308df605d471247e02da5724fdd35a443`  
		Last Modified: Tue, 06 May 2025 20:16:19 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f9f0e0339202486912cfe5e2f8fa644e16c4bd27b11f7a9bf2191748cb0b52`  
		Last Modified: Tue, 06 May 2025 20:16:31 GMT  
		Size: 81.9 MB (81916926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a55f2ad0b27ae2dbd7fb0218045955595c14ac05f12b34402b15a31e2e186c`  
		Last Modified: Tue, 06 May 2025 20:16:19 GMT  
		Size: 88.9 KB (88902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd75a5c2764a25ffb2c8fc8d1234945dc23662a93dcb8dd854a3ad1420ae59`  
		Last Modified: Tue, 06 May 2025 20:16:19 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
