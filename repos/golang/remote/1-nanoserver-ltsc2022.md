## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:b16e42871442e497ec45853bce51e280042823bc2e78aa52e28e821915a0cdf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull golang@sha256:3370e2f27d1e5c6040b087315b4cbb00c081c551e592d70fda0863ea0a875309
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202689972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f86edd934a2045e85b02bd135c4fd655b3a75589bb4b13d61f0cb66694ccc94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Thu, 13 Mar 2025 19:29:42 GMT
SHELL [cmd /S /C]
# Thu, 13 Mar 2025 19:29:43 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 19:29:43 GMT
USER ContainerAdministrator
# Thu, 13 Mar 2025 19:29:46 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 13 Mar 2025 19:29:46 GMT
USER ContainerUser
# Thu, 13 Mar 2025 19:29:47 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 19:32:20 GMT
COPY dir:1c8a5df65fcdbd0ad306edfb20884d0712989c03ff01d990889cdc983af886a3 in C:\Program Files\Go 
# Thu, 13 Mar 2025 19:32:23 GMT
RUN go version
# Thu, 13 Mar 2025 19:32:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac539fba92aabef6aa1334ed741c2cc76305fe7983c59d2e2813b7bce114424`  
		Last Modified: Thu, 13 Mar 2025 19:32:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d945086758e16255f96063e49f8f91f133a7222f341550b0bf9d13f5232654`  
		Last Modified: Thu, 13 Mar 2025 19:32:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca0d57e4a2c8eeaec6aabc75ecb3232cac1570fb6c9059dc00a046ad5e004d`  
		Last Modified: Thu, 13 Mar 2025 19:32:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0588951a65608595261db6b4578dabd6b4a07d69ebe23ceefbc58784e641fa`  
		Last Modified: Thu, 13 Mar 2025 19:32:28 GMT  
		Size: 75.9 KB (75869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa957882855fd355c7a985e33f8a8e7275880c00588697c1e77d952515418fe`  
		Last Modified: Thu, 13 Mar 2025 19:32:27 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be729eeb2eb0e195c51ca405401488d5038098498b1c09d01a6237b17e863839`  
		Last Modified: Thu, 13 Mar 2025 19:32:27 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820b61b699842a4c1d9e210737a8fabe061cc281d9db0a882774071df5510343`  
		Last Modified: Thu, 13 Mar 2025 19:32:39 GMT  
		Size: 81.8 MB (81819720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465c68cdaecc0f0e78f4286825c35dff934e8bec91f81034d4c06e3dee9a1f33`  
		Last Modified: Thu, 13 Mar 2025 19:32:27 GMT  
		Size: 92.5 KB (92455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778ed1d6cfb0059a4af9fe5aaef622b1e5ea3b97e5d2b34e456ac81861831779`  
		Last Modified: Thu, 13 Mar 2025 19:32:27 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
