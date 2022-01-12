## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a699ccc7db0687250702e440b354b5d56544d48eea7f8d2c48a8b1ebd27ae714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2451; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.469; amd64

```console
$ docker pull eclipse-temurin@sha256:243c038c544ef6439cf736d24fbcb71c6d05669d50272b58160b1edd9c16ee71
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160555623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935b96c684a88845f448329527967307e596ad8ec69bee1053ab86a522e0d7f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Jan 2022 03:34:42 GMT
RUN Apply image ltsc2022-amd64
# Tue, 11 Jan 2022 22:29:41 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 22:33:10 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Tue, 11 Jan 2022 22:33:11 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 11 Jan 2022 22:33:12 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 22:33:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 22:33:24 GMT
USER ContainerUser
# Tue, 11 Jan 2022 22:34:33 GMT
COPY dir:38eebe4e3a4da98e178f49482de333d171d427f5886e68b2b67715641b9694d5 in C:\openjdk-17 
# Tue, 11 Jan 2022 22:34:47 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b2bb136f79c12b0a42720d7bb83469bce3f7bf2ca5c8bc68a36228796311fc6b`  
		Size: 117.3 MB (117334348 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d7943d6864d35f22a1b2c416194fc3658b93c41ce26a946ba9e15f3671a482a`  
		Last Modified: Tue, 11 Jan 2022 23:15:45 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02decf96be3c4b72bcf51bd63f61322637eb5bacfa54cec6fa22cd2b2675923`  
		Last Modified: Tue, 11 Jan 2022 23:18:56 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff99d2735cf0b4ad92e04373e1627f3646b2abe93c426f6ee83e714af29c7a`  
		Last Modified: Tue, 11 Jan 2022 23:18:56 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab1e19667cf0c201fef594c6e6eae2c3183deae7061fcbcb45a920cd9b711ef`  
		Last Modified: Tue, 11 Jan 2022 23:18:56 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b7c1f5f36b1a8d40e87fc92e5f09026116f80cff75a474b2b7475d45042b44`  
		Last Modified: Tue, 11 Jan 2022 23:18:54 GMT  
		Size: 80.0 KB (80027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be8f9c99776667d4701e33c1dd78073e01daceedf8308832c33d43797e26cd2`  
		Last Modified: Tue, 11 Jan 2022 23:18:53 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeaa4b4890dd68e27b06f23e24fdae74acd27afb1fa1577a85cfdbcae119342`  
		Last Modified: Tue, 11 Jan 2022 23:19:35 GMT  
		Size: 43.1 MB (43075016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4e6247dc871f7381662dcbba9e3e59e056abf73236c80568d31d513d4cf8bd`  
		Last Modified: Tue, 11 Jan 2022 23:19:27 GMT  
		Size: 60.6 KB (60559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.2451; amd64

```console
$ docker pull eclipse-temurin@sha256:af3ab5de4fab94c76a183ee3ac6b19f71a2b1e41b3c04f67dc49283fc002b703
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149188242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb09114b9198e1684bed8386dc7918107ec956623f2defcc5e428247f27c64e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:33:30 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 22:16:07 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Tue, 11 Jan 2022 22:16:08 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 11 Jan 2022 22:16:08 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 22:16:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 22:16:26 GMT
USER ContainerUser
# Tue, 11 Jan 2022 22:25:36 GMT
COPY dir:38eebe4e3a4da98e178f49482de333d171d427f5886e68b2b67715641b9694d5 in C:\openjdk-17 
# Tue, 11 Jan 2022 22:25:49 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6cc5785ab09c66739c3205c3a26410f1cf4bf85c377fa81b240e754cf0659c58`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7bafbaafb473c19a780298470b47c981eb427487ec11fec6a0513803ed1e8d`  
		Last Modified: Tue, 11 Jan 2022 23:11:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146d7ba2e72925e70b8cb5cccc9fb11d30eb5c1e63c658821294917083d8a6eb`  
		Last Modified: Tue, 11 Jan 2022 23:11:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca136dfbf1765c8e4fdc8d38a93bff7f7dc87cc920ff3f7861d65b4a8f77f7d`  
		Last Modified: Tue, 11 Jan 2022 23:11:19 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6347e4c3ded29f3f1dca92bf17130fbc95b9b38853681437e1cc0998f7d659ce`  
		Last Modified: Tue, 11 Jan 2022 23:11:17 GMT  
		Size: 70.6 KB (70561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024e3cc8e0edecdaa83890b60538167cdd56c94f6a5021f6281fcb90f0d6268c`  
		Last Modified: Tue, 11 Jan 2022 23:11:17 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6244f1b8d5d4bbdb57c954a7f1d9e9fd6b92ee79c5c82c2b0d1cfc906cd17815`  
		Last Modified: Tue, 11 Jan 2022 23:15:11 GMT  
		Size: 43.1 MB (43075477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db86c428f268f47cdd5c131f7f93699c34e58193b6c8dc3ebdff1c442ff73034`  
		Last Modified: Tue, 11 Jan 2022 23:14:25 GMT  
		Size: 3.0 MB (3021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
