## `golang:nanoserver`

```console
$ docker pull golang@sha256:08fd9b7279e7e202bd5fc6230af558f7952532a0f584fefd4cda8e4ccbde3dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `golang:nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull golang@sha256:6ecf946083daa0968aa21d2d1422783b471a29caf9c0f916e3138790e06f5872
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202704960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2892e8ec948d12385ca4d3ae79622418993d810baa00f73eb161e3333901e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Tue, 01 Apr 2025 17:14:39 GMT
SHELL [cmd /S /C]
# Tue, 01 Apr 2025 17:14:39 GMT
ENV GOPATH=C:\go
# Tue, 01 Apr 2025 17:14:40 GMT
USER ContainerAdministrator
# Tue, 01 Apr 2025 17:14:58 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 01 Apr 2025 17:14:58 GMT
USER ContainerUser
# Tue, 01 Apr 2025 17:14:59 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 17:16:48 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Tue, 01 Apr 2025 17:16:52 GMT
RUN go version
# Tue, 01 Apr 2025 17:16:53 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9e1a9e0cfadc73edce1fbd6652e859782a85e3c67b5b5a939b525a011b4652`  
		Last Modified: Tue, 01 Apr 2025 17:16:59 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3830e27f493b7c7dff151f0fcbf5d88525482d37d2e5fa5ea8c9a854b5533ec7`  
		Last Modified: Tue, 01 Apr 2025 17:16:59 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4344d14c99d7628531e27a2012c59f5dae825c5dc080d62009b91a5ccce71f`  
		Last Modified: Tue, 01 Apr 2025 17:16:59 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79227729ab0e11bee223b193ede9c3570c9852bca6c4c3374a33057c6f342adb`  
		Last Modified: Tue, 01 Apr 2025 17:16:59 GMT  
		Size: 87.5 KB (87542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2e5d847d2c805293223b3b883d161f3f77cf5f1e0a7a46da6ea6c6853ec0dd`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858264577e30842a5a588ca96e7cf5e0a6e1047c18f960d41b854ca78c116f95`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc32d95fd52b6dd74572e196298c5d576412dacd136fec2b8136fc87233fcf38`  
		Last Modified: Tue, 01 Apr 2025 17:17:09 GMT  
		Size: 81.8 MB (81827347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655d003504403ed2dc9982685e20fa7ffbcb4b4623c41a754d47d49a21dd56b7`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 88.1 KB (88135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058e828215208947cbe67d9a9ab17815983814c161cf0d98c8463601d97dc132`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
