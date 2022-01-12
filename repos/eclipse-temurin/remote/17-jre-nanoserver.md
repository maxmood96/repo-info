## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0099f11dd187504f85f03f98cfe7d4b30a794eee9f6b1bb0504e6df6599f8a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64

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

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull eclipse-temurin@sha256:86fd7a7714b68e26cad5a1a2794c7ced7f4762e9ac76591feedeb6810dfee69f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149198873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a825f23b233a718a633d2685f1923c418fead056d80f0100a2ce6288d5b406`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 12 Jan 2022 15:58:25 GMT
COPY dir:38eebe4e3a4da98e178f49482de333d171d427f5886e68b2b67715641b9694d5 in C:\openjdk-17 
# Wed, 12 Jan 2022 15:58:35 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:f6e1e5f9514947d07d5344ca9153980a5b4eed5bb78caee486e2e40b5a332457`  
		Last Modified: Wed, 12 Jan 2022 16:23:46 GMT  
		Size: 43.1 MB (43074148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbc15fd8dffcd670a83a4a7cf0f9f7c3b3e046ae74547005d842cafe939b2b5`  
		Last Modified: Wed, 12 Jan 2022 16:23:39 GMT  
		Size: 3.0 MB (3020296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
