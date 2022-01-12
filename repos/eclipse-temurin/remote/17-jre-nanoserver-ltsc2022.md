## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:82370e0f1ee06cf00fd04c78ea94961534395503b886578b25592fa33fc46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.469; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.469; amd64

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
