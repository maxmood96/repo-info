## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:1daa3eec38902a08f7968b0bda6a09369e7f333e0f050b1bc9ede7575cf2ef14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.32522; amd64

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

### `golang:1-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull golang@sha256:70ce96ba4eaa6120781caf027f9d8458b99a16e5d2ffd22d96bef08bc8dd288b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195982239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cdc41151b2102f7c9f38a9c58b0e7ab44e33195a7ce57ce63a7edc437d78e3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:38:12 GMT
SHELL [cmd /S /C]
# Tue, 10 Mar 2026 22:38:12 GMT
ENV GOPATH=C:\go
# Tue, 10 Mar 2026 22:38:13 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:38:15 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 10 Mar 2026 22:38:15 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:38:16 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 10 Mar 2026 22:39:20 GMT
COPY dir:075c372929040b7949c230fc01c695c61ff90e3e4ea8f5872f2353ec5724269a in C:\Program Files\Go 
# Tue, 10 Mar 2026 22:39:22 GMT
RUN go version
# Tue, 10 Mar 2026 22:39:23 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963fca4fcbbfcd350dddf47d5e69e9fc8513d978be4d53b2df8be5adcfe8df9a`  
		Last Modified: Tue, 10 Mar 2026 22:39:29 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef28e312eabeeb83e576c8a821f26cfa557fed5bc5849a5b3d27f63eaac5c8fc`  
		Last Modified: Tue, 10 Mar 2026 22:39:29 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4257810d3e37a2472a8402586160568a73f87371812f77ee8ff602de4e9f8b`  
		Last Modified: Tue, 10 Mar 2026 22:39:29 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2f2795c27ff5bca95202e329e03c1c649a93fa1bd31683776292f12f46779f`  
		Last Modified: Tue, 10 Mar 2026 22:39:29 GMT  
		Size: 78.0 KB (78005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858fa85d1752feb4773aea3fb6d451b21520971f93f434774547d7577eda4226`  
		Last Modified: Tue, 10 Mar 2026 22:39:27 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411da51ab6ba5b5f7739ae7d538612b5fa88d1a544704f161642f490bb7d2c54`  
		Last Modified: Tue, 10 Mar 2026 22:39:27 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfc0ea1ba0966046e354c4282a7b7d3af19b57011a9f7fad2b203c59c04be5c`  
		Last Modified: Tue, 10 Mar 2026 22:39:39 GMT  
		Size: 69.2 MB (69162000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b5d419039f45baef84ef50ff170a772dcb4da12ee1ae979c0fc817e6f00ecc`  
		Last Modified: Tue, 10 Mar 2026 22:39:27 GMT  
		Size: 85.1 KB (85127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dc79caec089daefc72be093cc8ebbe21ea8eaf663dc2932786c8c778d8ddc0`  
		Last Modified: Tue, 10 Mar 2026 22:39:27 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
