## `eclipse-temurin:8-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:8d994eb04b5dc88dc55488a8116081652c2be2be22cc2ba44f11b0d0e82e322e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:8-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:3ea5b84ff082b53c5cac9b6a19c78499bd37011fc4f6c23390c1c398f2b3add6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294050246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d9b5342027183d348513ae8266bdfbadebb78d95dab743420a9d09208e437`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:13:32 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:13:33 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 14 May 2025 21:13:34 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 May 2025 21:13:35 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:13:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:13:38 GMT
USER ContainerUser
# Wed, 14 May 2025 21:13:44 GMT
COPY dir:5c4bbf817a67c787f7f2d8809dee99be16882c3512e063f4e47205ca5ccbd190 in C:\openjdk-8 
# Wed, 14 May 2025 21:13:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e1405d2ec9c939314d66718f4cba33b4b2cfa76a0a8fd6217d283097d5075b`  
		Last Modified: Sun, 18 May 2025 21:00:20 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97489cf01087bcbd67d2064064f039bc61d4413b4cfd8023ec8e00dec4cae6c`  
		Last Modified: Sun, 18 May 2025 21:00:20 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e251d66041ad6d8d407be833b6e008b9607e2c02dc7ea4946bdce4cded963a`  
		Last Modified: Sun, 18 May 2025 21:00:20 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1154d408e65aa4d55c6c51cd44d600ccf36b513170bbb74f3bc0a16302e1aefb`  
		Last Modified: Sun, 18 May 2025 21:00:20 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa43340d41fb5d27c2e126700d5fa34ee9c362dcfd1bc403149d3f57015bf723`  
		Last Modified: Sun, 18 May 2025 21:00:21 GMT  
		Size: 76.1 KB (76071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1d5329d84729d5bd136522763866220cfde02cece0150156641977dd15e10c`  
		Last Modified: Sun, 18 May 2025 21:00:21 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894473a5504bd4f4a5e9a3c25b70974550dd45720f880ec7b13a62c25f79fa5d`  
		Last Modified: Sun, 18 May 2025 21:00:33 GMT  
		Size: 102.4 MB (102440585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bd50097138d097e2fb380e6738bc6b7bc7c23be56de5159efc8380706e3d8b`  
		Last Modified: Sun, 18 May 2025 21:00:21 GMT  
		Size: 116.3 KB (116291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
