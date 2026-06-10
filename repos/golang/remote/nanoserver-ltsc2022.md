## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:0293578b7328c1bc22d34dafbbf90e93104a3e5129cbbafdd4a8e663fc48dec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull golang@sha256:b63791b9e2ff6c892d562f04ea3d9f2270a0a79dfaf434f88b6609f33a109c9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193399414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4479fc6695e07ce0eeec4f4d5a8597187dbcc1b616b02bee1f935fbad99245`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:23:37 GMT
SHELL [cmd /S /C]
# Tue, 09 Jun 2026 23:23:37 GMT
ENV GOPATH=C:\go
# Tue, 09 Jun 2026 23:23:38 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:23:40 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 09 Jun 2026 23:23:41 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:23:41 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 09 Jun 2026 23:25:18 GMT
COPY dir:a4d5515d1dbeb183f1060174907c1c319fc78bf773c3b4147ef7f7bec4c9f4ad in C:\Program Files\Go 
# Tue, 09 Jun 2026 23:25:21 GMT
RUN go version
# Tue, 09 Jun 2026 23:25:22 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66837d0c2d21784c1390a342c8563271f5c2238c265301b0b4204db1ca32ba51`  
		Last Modified: Tue, 09 Jun 2026 23:25:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec7c57fad1c0ff65ffc25afd07fe04202af80ad71a39bf11f5a4960615d97`  
		Last Modified: Tue, 09 Jun 2026 23:25:39 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e160ade6ae99e12abd69dcc9629c9fcd040ddc167714612e93edbbcfaf90ac`  
		Last Modified: Tue, 09 Jun 2026 23:25:38 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8d71cbb06110060694457404ba6ae3e55777127c5e0cd8baff7ff06c2dbc1`  
		Last Modified: Tue, 09 Jun 2026 23:25:38 GMT  
		Size: 75.4 KB (75418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb275b3868a1ae2a368d9e7901be1dd59f5f80aa0445643533985b24e6720eb`  
		Last Modified: Tue, 09 Jun 2026 23:25:37 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baf6658f8cafcaa2e74f8459aee7212174042f6546f6d0458628f58d49b18aa`  
		Last Modified: Tue, 09 Jun 2026 23:25:36 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490a9aeeff9396b30d987e6de481cc0cff6741ddbb23239584441d822f5b1f70`  
		Last Modified: Tue, 09 Jun 2026 23:25:48 GMT  
		Size: 69.2 MB (69233528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182d2826ce6ea32bfbb88a19e9af544a26c0731da00937598ea0398f3b78f04`  
		Last Modified: Tue, 09 Jun 2026 23:25:37 GMT  
		Size: 86.4 KB (86370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee4f066a7a061739f318fdb6674e5ce04ef37ca5ad24d50a017b5a908fcfec4`  
		Last Modified: Tue, 09 Jun 2026 23:25:37 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
