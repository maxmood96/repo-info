## `golang:nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:3ea9e429d6fd721680a942604a980c9a2972708630004222a4cda2a14d31d581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `golang:nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull golang@sha256:26762fda78c698bbebf337aa3fdc0e8a59b82cc49ee72829b61100c193f9016d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256096728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a94fa53abc2225312132d5b1912e5ea84beac5a5a395f83b639b3c5652f714`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:20:09 GMT
SHELL [cmd /S /C]
# Fri, 24 Oct 2025 19:20:10 GMT
ENV GOPATH=C:\go
# Fri, 24 Oct 2025 19:20:10 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:20:12 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Fri, 24 Oct 2025 19:20:13 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:20:13 GMT
ENV GOLANG_VERSION=1.25.3
# Fri, 24 Oct 2025 19:21:22 GMT
COPY dir:6b7560915a38431967d90704d11f1201c2d1cdc45bff8fe429921d03a21c4716 in C:\Program Files\Go 
# Fri, 24 Oct 2025 19:21:24 GMT
RUN go version
# Fri, 24 Oct 2025 19:21:25 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a244e6de142417d0d9154d9af67a51a7b3ea6c100c94d27b30a0d974ef28ad`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0230660c57b44321ca929af81a9396a238af0360a878b16e2640d2f4902088d3`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d636c8f3e1886415378990aa509f86fcc4811d2b4612d1e1634f6b5ffa3b5361`  
		Last Modified: Fri, 24 Oct 2025 19:21:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cff9d259af9c29b7e7367e2ec66d0a6c142ac05b8cd0f08cc924f241985bb4`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 72.1 KB (72075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3538cecf353d75cce131d262d199bc6160e002021cda477e02db9f5dd87b8057`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7254d1080dfeff8c203c6d5fa913feaa97f47ba9b5cb7693e8deaf9205d12bda`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71682384a6b34b18ab59b080d6a3471e9548cf4738b9caf1d141e5807f64a4e9`  
		Last Modified: Fri, 24 Oct 2025 19:22:00 GMT  
		Size: 61.9 MB (61906627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25296b327c17f7968b5429c7bf02642b5cc59d86c057b8c8499b735203a21b83`  
		Last Modified: Fri, 24 Oct 2025 19:21:57 GMT  
		Size: 82.0 KB (82047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e474c80731578b829a0d50c4bbd8caa34c48f41ab0388be734d739c52211cb2`  
		Last Modified: Fri, 24 Oct 2025 19:21:57 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
