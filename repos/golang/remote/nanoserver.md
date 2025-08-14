## `golang:nanoserver`

```console
$ docker pull golang@sha256:3f1b131a7566387583f0c65255d07d09a1e8dd262b44ced292f28debf8859d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `golang:nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull golang@sha256:5efaa52e8e05d25e784e508fc6709cb2b1738a03ac3a740984757fc870e7c1d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255535033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ec6b9a0b1a9a59873730982e6eb6b49a93393872c9f479e840edeb2192ade2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Wed, 13 Aug 2025 18:31:25 GMT
SHELL [cmd /S /C]
# Wed, 13 Aug 2025 18:31:25 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:31:25 GMT
USER ContainerAdministrator
# Wed, 13 Aug 2025 18:31:27 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 Aug 2025 18:31:27 GMT
USER ContainerUser
# Wed, 13 Aug 2025 18:31:28 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:32:23 GMT
COPY dir:e0136877c8d65248ebfafffe24a0c4cb6a2bc1ae83d2b9a9ec6dc66367830ec0 in C:\Program Files\Go 
# Wed, 13 Aug 2025 18:32:25 GMT
RUN go version
# Wed, 13 Aug 2025 18:32:26 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299e43242fb82ff27891288b4a061e9d17748168298e9bbdee65fda814273918`  
		Last Modified: Wed, 13 Aug 2025 18:36:28 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4127e58f15947f30d6f585dc6ce73e0f0b38cc4ec78e92b723ad3e677a045c59`  
		Last Modified: Wed, 13 Aug 2025 18:36:32 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8514458441a6e926fa21ff1de2c1c217b582aac138321944e009ffb91c94b982`  
		Last Modified: Wed, 13 Aug 2025 18:36:35 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125c969354a4a0f1bf4df4bc4761a3582e7a74141a11dc06ff4b5a24de491fa2`  
		Last Modified: Wed, 13 Aug 2025 18:36:39 GMT  
		Size: 75.6 KB (75553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230caa614465afefe9250bc9c6fc6934ee826897f80da63d579de2a2fddeb131`  
		Last Modified: Wed, 13 Aug 2025 18:36:43 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f229c073f192cd45c522181f2d87e68ece5b09d3ee78e7d92a6da428e52872a`  
		Last Modified: Wed, 13 Aug 2025 18:33:31 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd7f13e18dcda31249e149450d709f1f64cd20a10c81897e913c48064d3996d`  
		Last Modified: Wed, 13 Aug 2025 18:33:44 GMT  
		Size: 61.9 MB (61895996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ba3d45be52b2f1d8609d8d284c91d11e311d03eb2c0a974f5ca0a34b8c41c`  
		Last Modified: Wed, 13 Aug 2025 18:33:31 GMT  
		Size: 87.5 KB (87532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b9c7b54a661f9a47721d5dd4c0f6793199ff732256d5e1e7bf9cacc331d0cd`  
		Last Modified: Wed, 13 Aug 2025 18:33:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull golang@sha256:919cc84df8522a2c84b7fae464d85cbf8686007a27ec70332204e26bc83d6208
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184691487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cb4f566fa3da199838cb3ff0b3e2d91c2afd118e983799b916472de9c9352c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 13 Aug 2025 18:31:00 GMT
SHELL [cmd /S /C]
# Wed, 13 Aug 2025 18:31:01 GMT
ENV GOPATH=C:\go
# Wed, 13 Aug 2025 18:31:02 GMT
USER ContainerAdministrator
# Wed, 13 Aug 2025 18:31:05 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 Aug 2025 18:31:05 GMT
USER ContainerUser
# Wed, 13 Aug 2025 18:31:06 GMT
ENV GOLANG_VERSION=1.25.0
# Wed, 13 Aug 2025 18:32:39 GMT
COPY dir:e0136877c8d65248ebfafffe24a0c4cb6a2bc1ae83d2b9a9ec6dc66367830ec0 in C:\Program Files\Go 
# Wed, 13 Aug 2025 18:32:43 GMT
RUN go version
# Wed, 13 Aug 2025 18:32:44 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bdcc753aa2a8762b55b26c86dbe7bcaebb96f6502f5f9075eb95faf029d5ea`  
		Last Modified: Wed, 13 Aug 2025 18:33:40 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3069709bfa9400f235979fbd1725bea958b632e6a7b4a377d90220ba98aba5cf`  
		Last Modified: Wed, 13 Aug 2025 18:33:41 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c0e24a4c0d293244b2d9bece4e0e706b822878062146405e1ffe7d1984b513`  
		Last Modified: Wed, 13 Aug 2025 18:33:41 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab18feb696ccff3a2a24f54825d15137abda3b974bd34948235bf162e227503`  
		Last Modified: Wed, 13 Aug 2025 18:33:41 GMT  
		Size: 76.5 KB (76534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc6cf4e0e9fc8fe1ae75e3022dd8dd4ab386f9be480dc8f223b35f8ff27233c`  
		Last Modified: Wed, 13 Aug 2025 18:33:41 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97863e01494ae7668da2711a78df3c3cc64e092fbf231bdd60403d4f2a8a7808`  
		Last Modified: Wed, 13 Aug 2025 18:33:41 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25e48070241bb76ff7a4a8ce6215c0f10c3c9bed8fe9036ba5c662148951ec6`  
		Last Modified: Wed, 13 Aug 2025 18:34:06 GMT  
		Size: 61.9 MB (61865068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a59c8d6c4100e886af7eaebc0de5aa363c40f2d0deb970bc081c88e94d9d20`  
		Last Modified: Wed, 13 Aug 2025 18:33:42 GMT  
		Size: 83.1 KB (83149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04410456ca9f126928a1511218fbbd2aa3414f5f364e3260d29985ba634f76f9`  
		Last Modified: Wed, 13 Aug 2025 18:33:42 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
