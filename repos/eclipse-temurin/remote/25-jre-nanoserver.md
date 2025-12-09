## `eclipse-temurin:25-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0c28e02d2c42fedf6b9479a7f20b3a7cc19b3f78262d1abf3ca9639c5979bc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:3fbb97b7eae600e19826163cf7fa5e7054fa218be2ae2b58a0901704368f7bf6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257608776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ad57aca25dccebf03ffd6ef8dbb7211a7a89eee2b760e43f2301131fb5c07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:13:13 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:15:41 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 09 Dec 2025 21:15:41 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Dec 2025 21:15:41 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:15:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:15:43 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:15:50 GMT
COPY dir:38f2d146da8b2d45f6309f76e3864fba66a43ff9541e6e5522e91b15798552e5 in C:\openjdk-25 
# Tue, 09 Dec 2025 21:15:52 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c3e9ac772555dbb907a48e4dcac3181c5961b789f6ef74dc9cf30cd0cc60ba`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba7c0682ce878ac891c94eeebe01b6e2300c031df45955f0cf50ddbc4a07285`  
		Last Modified: Tue, 09 Dec 2025 21:16:12 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7893ce86cfc2ff62239630ce918ae6959fb88e66e67f43482cd38b2144195707`  
		Last Modified: Tue, 09 Dec 2025 21:16:12 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e03606b21f2efd75accf58269c96250c65af030b777f4db949bbd716757f55`  
		Last Modified: Tue, 09 Dec 2025 21:16:12 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e345799079c0a51f7980b5ee0275be362bd8fa46b07f52e72da96a00448e38ff`  
		Last Modified: Tue, 09 Dec 2025 21:16:12 GMT  
		Size: 72.1 KB (72127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e366448333ec30f315d1e586a4d8ac849c9ac4d7b4053dbf112d651de71cbf2c`  
		Last Modified: Tue, 09 Dec 2025 21:16:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69e91b24f6f3a8b1be9c7c3407d32cf20f2e6b3e8e2bee72f91ba8df6ef76b`  
		Last Modified: Tue, 09 Dec 2025 21:16:25 GMT  
		Size: 58.6 MB (58564030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caba31bf5a674f9c589c16bdf38080164e0242c16ce96cfe979aca150c24a8a0`  
		Last Modified: Tue, 09 Dec 2025 21:16:12 GMT  
		Size: 93.3 KB (93347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:edaa81fa03c331d2d62f1906abfca878179a11ce791dacfdaa5b9428d3aa3ec0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185107086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b2c581db6bc16e57d4dbc6d417d3df23658a07356668e1e3d50af22c85c430`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:41 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:13:30 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Tue, 09 Dec 2025 21:13:30 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Dec 2025 21:13:31 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:13:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:13:33 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:13:47 GMT
COPY dir:38f2d146da8b2d45f6309f76e3864fba66a43ff9541e6e5522e91b15798552e5 in C:\openjdk-25 
# Tue, 09 Dec 2025 21:13:50 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95361dc1d7d66c6d1cca1411b68c4130a2416a2274c8b466e22d712d4f5999bc`  
		Last Modified: Tue, 09 Dec 2025 21:13:24 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a58a11c6c6aa0a759bf83b7f3c43336060934b15ced31376fdbe0121536170`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52caa5d2ddd90ed3c6ebb136a27a7cc9c4ab543d9b6863b97e06ee95e6bd54ac`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7deaa71b27c6c7577c1a26dab200b96d773f0e4406bf7eef0b2533d4b9f28c`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c48adfc7a1bd84a6e4049d8b9f073d6fac85cbe68994fe273b145d1291f047`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 77.0 KB (76958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a0eec0acbe45ffbf16f3b5169eb86ba8979cb07e501221422320779b97a455`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0ed9a47c4ceac099b073d6385c60e731bd11e866069c421f9a7ac0a6f4541c`  
		Last Modified: Tue, 09 Dec 2025 21:14:16 GMT  
		Size: 58.6 MB (58563820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb01136fee988d334bf4a2128b3749948e7149adb8afe9b12f152a7128dbac7`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 102.7 KB (102684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
