## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:b868b8de9c60c4b9dcdb5499f4a6c50caaa96fe065b61c227924dbb681a3b240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

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
