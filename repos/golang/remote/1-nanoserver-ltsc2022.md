## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:a3511c3d945653b5d25e28b27504421f8e3c1038aaacdc982d38fe6b28c44bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull golang@sha256:b044947f062d0a01ff678ac5b250d6afb91a00ebb81ec68a48b49d872cd02b6c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195988422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb92c0bb0f77922cab19fb69d5ec99ba5eb29408f249ae6b793ca16e3e346ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 07 Apr 2026 21:58:43 GMT
SHELL [cmd /S /C]
# Tue, 07 Apr 2026 21:58:44 GMT
ENV GOPATH=C:\go
# Tue, 07 Apr 2026 21:58:45 GMT
USER ContainerAdministrator
# Tue, 07 Apr 2026 21:58:53 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 07 Apr 2026 21:58:54 GMT
USER ContainerUser
# Tue, 07 Apr 2026 21:58:54 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 22:00:45 GMT
COPY dir:67fc335d5ed530085681f1943ca37084f1abf3c9dd644604da00d33121190fa6 in C:\Program Files\Go 
# Tue, 07 Apr 2026 22:00:49 GMT
RUN go version
# Tue, 07 Apr 2026 22:00:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f216241facf4bba1cc03d1ec55fdf125abb561d7f3a568a3ffe678888b92f2`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da6bb8d7c1d4117737148054e412319c7d99fb56863457a6a24f7c69ec72e01`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4529d7130569fb746783a303f6abb4168223c24d7390b990fc29781eea77ef8`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07f386751e503d44d894ca77516fbabd191a6907b6bee6d003087c91f5fa56e`  
		Last Modified: Tue, 07 Apr 2026 22:01:07 GMT  
		Size: 80.8 KB (80775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d628fc173a698b9cecd00506d8d138898e4ab7b1b37ddba0f1750ba8f95a98`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d884941654cb343034a810782e4394437ea9794039cf3a5cb7cdc8b3511c89`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa5fed408a1d0c911eca62d232dc4e6e2716fb04b71038e13c11e38dca71b4b`  
		Last Modified: Tue, 07 Apr 2026 22:01:16 GMT  
		Size: 69.2 MB (69170893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b011e5d0af76eb6651b003c8d6e325ce9ba9569df969beee1add2e2db78b96`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 79.6 KB (79609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa9e347e2d411dd96c9dd9186c97a8836996138ace6c13178b1cc6a29771f2f`  
		Last Modified: Tue, 07 Apr 2026 22:01:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
