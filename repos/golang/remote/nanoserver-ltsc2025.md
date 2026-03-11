## `golang:nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:c5d81ecc2e7f9f9d6d78a3774f91b5d955f4a0db31395a358f0e942062e156bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `golang:nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull golang@sha256:a39863d93a5e125466bb84c09182a737605d70a74a5ef259a720daefffa5474a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268729289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a631389d5d7fd1c9277777b0e9d70ddbd5c67f79cb0551e682633471967e9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:42:41 GMT
SHELL [cmd /S /C]
# Tue, 10 Mar 2026 22:42:41 GMT
ENV GOPATH=C:\go
# Tue, 10 Mar 2026 22:42:42 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:42:43 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 Mar 2026 22:42:44 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:42:44 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 10 Mar 2026 22:43:51 GMT
COPY dir:075c372929040b7949c230fc01c695c61ff90e3e4ea8f5872f2353ec5724269a in C:\Program Files\Go 
# Tue, 10 Mar 2026 22:43:53 GMT
RUN go version
# Tue, 10 Mar 2026 22:43:54 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d46f06a0523a1a725895d876ca660f26347d90e804bbe48b526b67ba9ed7a9`  
		Last Modified: Tue, 10 Mar 2026 22:43:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4d604b5cb7488b55b9d3f427327176f9b9e4eca0243ffff8795fe928eae2b0`  
		Last Modified: Tue, 10 Mar 2026 22:43:59 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffe0cc69b432b2bf663421539011f9ff6f2cce7fc7cac75836ca0829c7d8bd0`  
		Last Modified: Tue, 10 Mar 2026 22:43:59 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e1cb3c07b6bfe5e778f55183e2324429dd3c566f1bac18926817cd5351a032`  
		Last Modified: Tue, 10 Mar 2026 22:43:59 GMT  
		Size: 72.1 KB (72080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748e06bb429b447718edf2319e81024db835276701aa11fd21e69f18e9ab2a7e`  
		Last Modified: Tue, 10 Mar 2026 22:43:58 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c52ed235d221796f8c27ee9ab16d979aff18fbe0cf8dc445f64e54401a043f`  
		Last Modified: Tue, 10 Mar 2026 22:43:58 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f61f1f5c9bb58fecdd78058ca2907d9844376532c28412d3de1179bf8749f1`  
		Last Modified: Tue, 10 Mar 2026 22:44:09 GMT  
		Size: 69.2 MB (69162439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96121e55d0f54ce8aadebc8dbf842a81b1ff3ac85c5aa57606cb139cda8dc0c`  
		Last Modified: Tue, 10 Mar 2026 22:43:58 GMT  
		Size: 78.9 KB (78867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0098c49800ba9a5b77d28516a3dedba2f5199fc7177cf024447f1fbc1f7e5dab`  
		Last Modified: Tue, 10 Mar 2026 22:43:58 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
