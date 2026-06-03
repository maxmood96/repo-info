## `golang:1-nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:fbe15bd1f9baf63dcc4e63cd7547ad1c0fbe759f84c440bcb3845995ed744a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `golang:1-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull golang@sha256:282af527643585e7da341383854c8631647ee5eea598030b6e4a387fdcede14f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269126961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43946803d18c781fe49c6a87bfc7179d0ced18f7d0988d721456d55a95aa8ad1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Tue, 02 Jun 2026 22:31:02 GMT
SHELL [cmd /S /C]
# Tue, 02 Jun 2026 22:31:04 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 22:31:05 GMT
USER ContainerAdministrator
# Tue, 02 Jun 2026 22:31:18 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 02 Jun 2026 22:31:19 GMT
USER ContainerUser
# Tue, 02 Jun 2026 22:31:19 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 22:33:12 GMT
COPY dir:a4d5515d1dbeb183f1060174907c1c319fc78bf773c3b4147ef7f7bec4c9f4ad in C:\Program Files\Go 
# Tue, 02 Jun 2026 22:33:15 GMT
RUN go version
# Tue, 02 Jun 2026 22:33:15 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90230b07e7efae54b522a336544e032456be3725deee01737f332e98f421d9e7`  
		Last Modified: Tue, 02 Jun 2026 22:33:32 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a3e62be6bda3499de4e7ff46bc7da66d66266bbf72e95d95baea6bb9f8ba0a`  
		Last Modified: Tue, 02 Jun 2026 22:33:32 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd58d0fa539d3708170cdc54a4ec9afb7a496bdee64d55d3640e5376d25b33b`  
		Last Modified: Tue, 02 Jun 2026 22:33:32 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aff29360f8d0d1d4b34c85c21d94cb4416a2b421260c00822073562e7445798`  
		Last Modified: Tue, 02 Jun 2026 22:33:32 GMT  
		Size: 71.6 KB (71556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e522d24d3f98c0c333b19a5dbd7871fd2bc8c77ff3008bba79c826719343c`  
		Last Modified: Tue, 02 Jun 2026 22:33:30 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdba7f6015d6b65ec80da169461bd78631cfe0c3f8f5fe0148fc42fa58808f56`  
		Last Modified: Tue, 02 Jun 2026 22:33:30 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe98ae482c3396103c94389fd990e3d584ff5be0207aff55db4f1c71d6439e5c`  
		Last Modified: Tue, 02 Jun 2026 22:33:42 GMT  
		Size: 69.2 MB (69233226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f628315255bd0816266a888cb07150538dc258d0e7adfb9efd9aa42a95dfac1f`  
		Last Modified: Tue, 02 Jun 2026 22:33:30 GMT  
		Size: 76.8 KB (76750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da297ea99ec548c0a35c946c2f8a5a0e0ebf3b4697c814b40399ccd5eac57fd`  
		Last Modified: Tue, 02 Jun 2026 22:33:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
