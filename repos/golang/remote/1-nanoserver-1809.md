## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:cd193ec95a99f83fa3941a6a981506ff940a6cb62417b9f9dd0e1ccf66634118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull golang@sha256:7cdb3b4a2520e6c4e00c320ce8a7a2ff0ba95d86e21bc6e2e281aee5fafec4f1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213167645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012edac894df197212cfd7246b02fbb10137d3694f2a05ba9825e7c6c681333f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 01:31:05 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 01:31:06 GMT
ENV GOPATH=C:\go
# Wed, 10 May 2023 01:31:06 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 01:31:15 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 May 2023 01:31:15 GMT
USER ContainerUser
# Tue, 06 Jun 2023 20:23:47 GMT
ENV GOLANG_VERSION=1.20.5
# Tue, 06 Jun 2023 20:25:28 GMT
COPY dir:2b56775b246889ea39ed6a295f7604dfecd0a015e0fc1352d091198ccc0b1678 in C:\Program Files\Go 
# Tue, 06 Jun 2023 20:25:47 GMT
RUN go version
# Tue, 06 Jun 2023 20:25:48 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ddac9d33b62fa0bb37c6743a1992a622e53b5bb070758474e92416b5f031ba`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a155cedba06fb5098abf51cdebd14a436bafaa6b6331cdf23c15a1b88aa9a6`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd8f19817a4336375d9d4706a35ee835a3391a94309471d2d0465cc38b3f181`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b17eb34d866264b66ab9e30b51834fef645f02261a5382f9d80bf1e377340`  
		Last Modified: Wed, 10 May 2023 01:48:38 GMT  
		Size: 65.5 KB (65474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7b0290c09d5f21a749be38c92ce5c06bd83dde4983d6e7c543189c6611324b`  
		Last Modified: Wed, 10 May 2023 01:48:36 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c241f48bfa324c20b89434a1299d8fe0c177159ccb6e01d6eddeb17abb35e48a`  
		Last Modified: Tue, 06 Jun 2023 20:40:34 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c503099658c92972c09e90bec6307e44f4fc98d41c5c085dff979a3b0bf092`  
		Last Modified: Tue, 06 Jun 2023 20:40:55 GMT  
		Size: 108.6 MB (108637571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea13326f72b4ce21425cc3edcc1b31f50690c91ff13832e0ed1be5e465c1b0e`  
		Last Modified: Tue, 06 Jun 2023 20:40:34 GMT  
		Size: 73.4 KB (73391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f39274ed50dc71b567065072a85ec7ff8be964e2efe59f7455485698440039e`  
		Last Modified: Tue, 06 Jun 2023 20:40:34 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
