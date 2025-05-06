## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:0984d7e17969d7173419cb8105d7fef537ae4ddd99600adeaef885976887194c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

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
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
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
