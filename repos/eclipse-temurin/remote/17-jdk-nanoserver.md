## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f56ab78368dfd967292878d80edfffff12496f230a8631e7feb7f6c01850b4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.469; amd64

```console
$ docker pull eclipse-temurin@sha256:6ddbbeadcec2e269c57431776c984e9de863a0a7eec02596e57cf522138b7fc7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302418139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd28fbe78f79517e4fe72a18ba22c5556403ae5d7db8f0e5d18eb41f729a0a8`
-	Default Command: `["jshell"]`
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
# Tue, 11 Jan 2022 22:33:58 GMT
COPY dir:75727e79a870c9066772bd3811959a8f3c491ac4b54ae3b2c145d1638b6bc93f in C:\openjdk-17 
# Tue, 11 Jan 2022 22:34:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Jan 2022 22:34:13 GMT
CMD ["jshell"]
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
	-	`sha256:2850fdbb4173bd1c595ebfedb92f9ebb1f5f0f6d69e0ad6c6329bd9e0c3aa32c`  
		Last Modified: Tue, 11 Jan 2022 23:19:14 GMT  
		Size: 184.9 MB (184936317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770bd89ac8523f8dfacd92d01f0a271d3de22d06d894835305e15d74a8617962`  
		Last Modified: Tue, 11 Jan 2022 23:18:54 GMT  
		Size: 60.6 KB (60620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137e6f01d5bf1fbaeb19026aeccf7ac3324b1a89c021afcf201890fd10204583`  
		Last Modified: Tue, 11 Jan 2022 23:18:54 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull eclipse-temurin@sha256:cc99ea8a2daa2d0ede662520729f9920d5c211da130a30bd6cd5fd1745d963e6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291700537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbed0262d5ca1da193ec803d9a928b08511d4bc274202d86789fffb2b6c9b79e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 05:19:56 GMT
SHELL [cmd /s /c]
# Wed, 12 Jan 2022 15:54:25 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Wed, 12 Jan 2022 15:54:25 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Jan 2022 15:54:26 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 15:54:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jan 2022 15:54:38 GMT
USER ContainerUser
# Wed, 12 Jan 2022 15:55:11 GMT
COPY dir:75727e79a870c9066772bd3811959a8f3c491ac4b54ae3b2c145d1638b6bc93f in C:\openjdk-17 
# Wed, 12 Jan 2022 15:55:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jan 2022 15:55:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:71dcb756adb8534a87210067788d6aa4a5a366b72d022b7af035e5263a3e54a0`  
		Last Modified: Wed, 12 Jan 2022 16:05:17 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1983a294203bf82e538d4fb4e5d589dc853a2d3feb3745942848770b644afd`  
		Last Modified: Wed, 12 Jan 2022 16:19:44 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a01630196a0c77fd4703967461934b575d4a89aaa51d39f64b34808273647fc`  
		Last Modified: Wed, 12 Jan 2022 16:19:43 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df7dcaf2f2a0734109ef31fc277229d7648d07695d0f48a24e3b9922523130e`  
		Last Modified: Wed, 12 Jan 2022 16:19:43 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef38329dc0f6e0bf7c4050b72f27d4fec8e31edd53f67a8c6fdd64b2441a1d1c`  
		Last Modified: Wed, 12 Jan 2022 16:19:41 GMT  
		Size: 67.6 KB (67595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe606976eb75c39f730f1cb89faba294bd48c06f6245f22001ef1081efa5705`  
		Last Modified: Wed, 12 Jan 2022 16:19:41 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7d968a4bd8dbbd88df53cdba365ff38527da10bb5be0dd99bf69111f3f6c6d`  
		Last Modified: Wed, 12 Jan 2022 16:22:59 GMT  
		Size: 185.0 MB (184950060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63e5d159aa752fc2741246120dcec7e895f44ba61422af897d2552a6a7f357`  
		Last Modified: Wed, 12 Jan 2022 16:19:42 GMT  
		Size: 3.6 MB (3644887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efe30c358a5058f345fd24ef4fa997479ea6102fc4d2e2a841f291f83322881`  
		Last Modified: Wed, 12 Jan 2022 16:19:41 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
