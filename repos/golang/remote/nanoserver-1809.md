## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:3bead2d1129bfb65398ec368bdf06808b04e3971df0c9c9beb94132a7fb2964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull golang@sha256:33ca3c1ebce7f615fcfd2b07a67f2614dc57aef0ae77c101fa856393c58c3e5e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252460337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b94953ca544c2896b314edcf71b075bacc27c4a3a19a68b6da52841d2e05317`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Tue, 10 May 2022 22:32:24 GMT
SHELL [cmd /S /C]
# Tue, 10 May 2022 22:32:24 GMT
ENV GOPATH=C:\go
# Tue, 10 May 2022 22:32:25 GMT
USER ContainerAdministrator
# Tue, 10 May 2022 22:32:50 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 May 2022 22:32:51 GMT
USER ContainerUser
# Tue, 10 May 2022 22:32:52 GMT
ENV GOLANG_VERSION=1.18.2
# Tue, 10 May 2022 22:35:17 GMT
COPY dir:67f7fab8d1a7f065771db4253ddaacaab4ff63abff61135cad8768defff592fc in C:\Program Files\Go 
# Tue, 10 May 2022 22:36:01 GMT
RUN go version
# Tue, 10 May 2022 22:36:02 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d7d4dec608f59eb9166ff96f59e4f4fcbda08a55e78d630ba39e558b23b3e475`  
		Last Modified: Tue, 10 May 2022 22:59:35 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4735e17fcd180a1d905a22c771ac994a1a249e57bfdde77ef41ccf51a0e29a3`  
		Last Modified: Tue, 10 May 2022 22:59:35 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833e97847abafba5e024c2c960a8b406785b7f11a1a3dd574f40993a068c19e4`  
		Last Modified: Tue, 10 May 2022 22:59:35 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd374e2694dcb43adcc3181c4f72a6fd7b1432b49478e67616949e2efe9aafd`  
		Last Modified: Tue, 10 May 2022 22:59:35 GMT  
		Size: 68.8 KB (68805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d279dc1f42008981f8d43d3f502139a3b21c0f5ca5d86ac0b9862c424b4477e`  
		Last Modified: Tue, 10 May 2022 22:59:33 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8c4e6731e822aee673a0928fee4d1e3c4d3ba667c3e634c1e85b48cd195e62`  
		Last Modified: Tue, 10 May 2022 22:59:33 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a4ca8bbd0fa265cfeae622fbdf0af0b4599f5ef7f9a057312ae25fdc89017e`  
		Last Modified: Tue, 10 May 2022 23:02:08 GMT  
		Size: 149.2 MB (149176688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb9166d77351b76c37aad97dec39bdf3826d3e1afeb022f48505df7a46f96c7`  
		Last Modified: Tue, 10 May 2022 22:59:33 GMT  
		Size: 73.8 KB (73827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914f5adf56559778f3abe7f029709c4de66cac06f3e74f11f1a832e7a3b35a9`  
		Last Modified: Tue, 10 May 2022 22:59:33 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
