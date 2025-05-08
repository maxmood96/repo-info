## `golang:nanoserver`

```console
$ docker pull golang@sha256:a23829d4b5e5877e60ae3785cb5fcc1f56e7aa8b07ec2ef7ea674470c135541f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `golang:nanoserver` - windows version 10.0.26100.3781; amd64

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

### `golang:nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull golang@sha256:27b4f122f884484250496add210b77a090a5dc1712e64064058eb665e9609ae4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204572385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66289b9ba17e72230159d8f1edfa44b99f01a35ce0c75e34b76e0243ecf8e310`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Tue, 06 May 2025 20:10:32 GMT
SHELL [cmd /S /C]
# Tue, 06 May 2025 20:10:33 GMT
ENV GOPATH=C:\go
# Tue, 06 May 2025 20:10:34 GMT
USER ContainerAdministrator
# Tue, 06 May 2025 20:10:57 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 06 May 2025 20:10:58 GMT
USER ContainerUser
# Tue, 06 May 2025 20:10:59 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 20:12:23 GMT
COPY dir:11c24136d74cfff65bad471f7cd999b92a92062aeed3b3acc0519a1823e1187a in C:\Program Files\Go 
# Tue, 06 May 2025 20:12:26 GMT
RUN go version
# Tue, 06 May 2025 20:12:27 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c16daf77c97b66da61f8651d1999f198c065d9e1ceadd8aae441cd40b2e888`  
		Last Modified: Tue, 06 May 2025 20:12:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645dabaad02b943229767c2858b6d556bf706350b142c351f5ee50c7d64895fe`  
		Last Modified: Tue, 06 May 2025 20:12:30 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe0553c58bef7f6088c4146734816656043ca9e88109efcc25f1b36ae0a3ba6`  
		Last Modified: Tue, 06 May 2025 20:12:30 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba147ca6d7824b1f353dde04a5bb73b214b893993801420c524c3e78eef2a37`  
		Last Modified: Tue, 06 May 2025 20:12:30 GMT  
		Size: 75.2 KB (75218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc160423170b98a4d15eb559dc23d71b5bdea390f95526954412552b946b24e`  
		Last Modified: Tue, 06 May 2025 20:12:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5927a9d1b0c07e03892f4e02ccd6152561143b1914df259fbf255340f06ea154`  
		Last Modified: Tue, 06 May 2025 20:12:29 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98e5876fa421e51204210ac3dd2d23d4e6a7a02578e5d3a5e33efcfba766621`  
		Last Modified: Tue, 06 May 2025 20:12:41 GMT  
		Size: 81.9 MB (81874521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3473e3989157c6f03ed65a88e5795c239e6d75716372f4e4526f7abcec5545f`  
		Last Modified: Tue, 06 May 2025 20:12:30 GMT  
		Size: 77.2 KB (77164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4229a40ee41c7913340f92bea20961ce4adf0a0e6e3c78d97daef83e5a9cee4`  
		Last Modified: Tue, 06 May 2025 20:12:29 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull golang@sha256:efd2ec4ff375bbca309be4c3fb048d62cd9464b8fdcd5d3a97aa6ea066cb387a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190795672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a866abb51c02a13ad0ec8187c3968c6f105717321effe105251d2a4e3ae01f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Tue, 06 May 2025 20:09:01 GMT
SHELL [cmd /S /C]
# Tue, 06 May 2025 20:09:03 GMT
ENV GOPATH=C:\go
# Tue, 06 May 2025 20:09:04 GMT
USER ContainerAdministrator
# Tue, 06 May 2025 20:09:15 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 06 May 2025 20:09:16 GMT
USER ContainerUser
# Tue, 06 May 2025 20:09:16 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 20:10:23 GMT
COPY dir:11c24136d74cfff65bad471f7cd999b92a92062aeed3b3acc0519a1823e1187a in C:\Program Files\Go 
# Tue, 06 May 2025 20:10:26 GMT
RUN go version
# Tue, 06 May 2025 20:10:27 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2232fc3c0bcf33dd48680722abc9ac920ab2a0ba03e73f060d26f2910415276`  
		Last Modified: Tue, 06 May 2025 20:10:35 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fdd5b43587885d9235dc574b999eebeaf45da5138f420d1ec22cdc2a74ea54`  
		Last Modified: Tue, 06 May 2025 20:10:34 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd70a7a9891adfbbe505beccf8354a96640d5e25fb07a20d645430935218803`  
		Last Modified: Tue, 06 May 2025 20:10:34 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eae49bc0c5771f0b3d00bdf62b0c55b79a56288b7e0712999baa44f31355a12`  
		Last Modified: Tue, 06 May 2025 20:10:33 GMT  
		Size: 66.7 KB (66738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4911d34220cc17791ba0cf3340610d58e0a5f78b2a96363867cdece0e924cc2`  
		Last Modified: Tue, 06 May 2025 20:10:31 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529e0bf976318af0247145796aef2810f178aa5597a010404420808c2d00d746`  
		Last Modified: Tue, 06 May 2025 20:10:33 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdae9489add78ac47c9ee955368dcda968642ce5151eaab3eea828d9bd098c79`  
		Last Modified: Tue, 06 May 2025 20:10:44 GMT  
		Size: 81.9 MB (81902521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e80b3fb2b1d5c301fdb1c80fbd0572ce3ea74ee5f44c8288392a6008877870`  
		Last Modified: Tue, 06 May 2025 20:10:31 GMT  
		Size: 67.7 KB (67660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee7daa6965a6fc45050b0d4795d6200eb30107c408d691dbc3eaff31ca754a7`  
		Last Modified: Tue, 06 May 2025 20:10:31 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
