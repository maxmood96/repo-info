## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:148efe6826398b35408b448a9a9888c8f25e33027e2015eb7f47941c757d358d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull golang@sha256:968889e1d0d4d831e7f712f1520312304c9bb20a97c8161db030e3d7d9ecf9aa
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202542860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0311aeea617c89548ee401fe2adda66af811c43967814d083932d447f90d260c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:15:39 GMT
SHELL [cmd /S /C]
# Thu, 13 Feb 2025 01:15:40 GMT
ENV GOPATH=C:\go
# Thu, 13 Feb 2025 01:15:40 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:15:43 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 13 Feb 2025 01:15:43 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:15:44 GMT
ENV GOLANG_VERSION=1.24.0
# Thu, 13 Feb 2025 01:16:59 GMT
COPY dir:c62b8dc6e9060a1c90492bd4af0627f1fb2ef88d5b0c6bad980916fff57ef6a8 in C:\Program Files\Go 
# Thu, 13 Feb 2025 01:17:03 GMT
RUN go version
# Thu, 13 Feb 2025 01:17:03 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59eb2722f77c8713adf7be2c05f44d2460db6bfcf80f092f33e5ca449250ff7`  
		Last Modified: Thu, 13 Feb 2025 03:22:39 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e23c1993c7510cd045322d199167b83d4ac1eaeac419478b585771a51431ac`  
		Last Modified: Thu, 13 Feb 2025 03:22:39 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f18faa83485b31148513cde38befb60086d12bd606819ad5a65ee9879cc5661`  
		Last Modified: Thu, 13 Feb 2025 03:22:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a8c5a2e42b030b8d3c0a12467407cfabce0c656c6d6d770d537b11f86893d3`  
		Last Modified: Thu, 13 Feb 2025 03:22:39 GMT  
		Size: 77.1 KB (77110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0049027d55cfbb5a58f34d21572e5756e39fe6cb0357d3d11f0ae88391b9b5`  
		Last Modified: Thu, 13 Feb 2025 03:22:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd43cc35fab9745317a02defdfb1ef97dfa88a6f83c6436632ba40d28bef7c7d`  
		Last Modified: Thu, 13 Feb 2025 03:22:39 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db8fd970058a868210f55d7c46ef4fdde2f3b67d29acc901cc74bf80e279d50`  
		Last Modified: Thu, 13 Feb 2025 03:22:45 GMT  
		Size: 81.7 MB (81688095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61dd719085566f38a465d90bf42b0ad0034b0a63a639e41b65d651d0fa5fc90`  
		Last Modified: Thu, 13 Feb 2025 03:22:39 GMT  
		Size: 104.7 KB (104651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e02c8ab44b2445de37ae0dd9bc4805a5f2406b21c9a457eafa7c4ecdb325cf`  
		Last Modified: Thu, 13 Feb 2025 03:22:39 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
