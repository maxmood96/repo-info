## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:4c7aa1ef6a8710f2340b0238a9e5a4a837a040ea72fded3f1b4ae714de96f6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull golang@sha256:d8668064d78a6b9d37ecf48c3d9376d4fa22648c60432a21d9f9b1a8e2ad5986
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 MB (197638679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de22d2403ae344a0c71c54b4d712dfe1cb29e049032a74b1766921456d1e642a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 10 Aug 2024 19:28:00 GMT
RUN Apply image 10.0.20348.2655
# Thu, 05 Sep 2024 23:06:20 GMT
SHELL [cmd /S /C]
# Thu, 05 Sep 2024 23:06:20 GMT
ENV GOPATH=C:\go
# Thu, 05 Sep 2024 23:06:21 GMT
USER ContainerAdministrator
# Thu, 05 Sep 2024 23:06:40 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 05 Sep 2024 23:06:41 GMT
USER ContainerUser
# Thu, 05 Sep 2024 23:06:41 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 23:08:41 GMT
COPY dir:3148b20efd35f18b5a0e13c6e7eabd669161775894572897e562dc60e9ffc1b0 in C:\Program Files\Go 
# Thu, 05 Sep 2024 23:08:47 GMT
RUN go version
# Thu, 05 Sep 2024 23:08:48 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:695cae91f2de8dadf81c8b3a95f4942533ef064a72ad8fa7843cca84a839bfba`  
		Last Modified: Tue, 13 Aug 2024 20:02:51 GMT  
		Size: 120.6 MB (120554921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1086d3f06b8449b0f35afb6bffcd23204c8646dde08444c2498910e759018712`  
		Last Modified: Thu, 05 Sep 2024 23:08:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060567ec1bb5800949b363cc1ae38f7c09ae18899abcde45ab2dc6b24228bc72`  
		Last Modified: Thu, 05 Sep 2024 23:08:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f90975e0b8694b5021db26d2802e39e6f78200837eba1d791e1d5cb80ad5c14`  
		Last Modified: Thu, 05 Sep 2024 23:08:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f332f55a95f539c0010695f6f2c10a07792421874eed7f2941ca803a75aa5e`  
		Last Modified: Thu, 05 Sep 2024 23:08:52 GMT  
		Size: 72.8 KB (72752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc68a7aad5f21523a2149b0048708a285668f77036c20235dd2068bea07049a`  
		Last Modified: Thu, 05 Sep 2024 23:08:51 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d796cb4671983651074d0479aa112619cf6558d7114ffeaa01723d6417b1449f`  
		Last Modified: Thu, 05 Sep 2024 23:08:51 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9c777f3b044fe883289724a855bcc77305e174ea1f2d0b9a22fde713cb6e0`  
		Last Modified: Thu, 05 Sep 2024 23:09:02 GMT  
		Size: 76.9 MB (76925914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cb16b1ae5eb17a04626164ed0e53033b62d7b062b2dd57842afc98569f770e`  
		Last Modified: Thu, 05 Sep 2024 23:08:51 GMT  
		Size: 78.7 KB (78712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99dec5cdf8696d78250b3f6bccaa6af27f29f2fc3c8234ed89b7a2d7839cb15c`  
		Last Modified: Thu, 05 Sep 2024 23:08:51 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
