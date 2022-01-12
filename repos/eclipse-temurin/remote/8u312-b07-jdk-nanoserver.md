## `eclipse-temurin:8u312-b07-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8036cecda6fc9d31d0eeee2fbc004688edfb7df021318686ff0e7c30552902d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.469; amd64
	-	windows version 10.0.17763.2452; amd64

### `eclipse-temurin:8u312-b07-jdk-nanoserver` - windows version 10.0.20348.469; amd64

```console
$ docker pull eclipse-temurin@sha256:c2ef7ee699394795664bc4a661fa727441a10d29b43f39776749992d2da97913
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217673713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8f71b0530008717512532207295140b82aced79f6a4ee6b225a4dab6a89ff3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Jan 2022 03:34:42 GMT
RUN Apply image ltsc2022-amd64
# Tue, 11 Jan 2022 22:29:41 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 22:29:42 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Tue, 11 Jan 2022 22:29:43 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 11 Jan 2022 22:29:44 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 22:30:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 22:30:01 GMT
USER ContainerUser
# Tue, 11 Jan 2022 22:30:19 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Tue, 11 Jan 2022 22:30:34 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:b2bb136f79c12b0a42720d7bb83469bce3f7bf2ca5c8bc68a36228796311fc6b`  
		Size: 117.3 MB (117334348 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6d7943d6864d35f22a1b2c416194fc3658b93c41ce26a946ba9e15f3671a482a`  
		Last Modified: Tue, 11 Jan 2022 23:15:45 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c043cffe398f6cd079956176400b13e6685e159354b3471ada29784a214fdb11`  
		Last Modified: Tue, 11 Jan 2022 23:15:44 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8410c2d8d1c245897bf27bf02730b6b991dad90a58c2e77bb35b6cd1be1bab8b`  
		Last Modified: Tue, 11 Jan 2022 23:15:44 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0e41b31760bcf9bd1e63210aee70fb9cce262c80d86717b96e86c7e5ed9f6a`  
		Last Modified: Tue, 11 Jan 2022 23:15:42 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125084f9ebd7cbb813332b1c44800fcf9ce18bc69d9f22296bba5653a386962`  
		Last Modified: Tue, 11 Jan 2022 23:15:42 GMT  
		Size: 87.1 KB (87121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a1852327565da872001ed5000ffb212313c2390b5bf4388f3549218f14681`  
		Last Modified: Tue, 11 Jan 2022 23:15:42 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d25bef88399a8962c5a76f820f694b388589747180349099fbe47af2d32b2a`  
		Last Modified: Tue, 11 Jan 2022 23:17:32 GMT  
		Size: 100.2 MB (100189865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9730b8d506807bf840a1c5ac91b7d0dc28056487a5e2ff5612c6d67ef456e4f0`  
		Last Modified: Tue, 11 Jan 2022 23:15:43 GMT  
		Size: 57.0 KB (57016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u312-b07-jdk-nanoserver` - windows version 10.0.17763.2452; amd64

```console
$ docker pull eclipse-temurin@sha256:45b7bc29e3764b3fc689a2b8cde59f10c7931618f4ab5e362839019af51e842d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203373307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5fe0c9ba09af56a271af90058a25ba2c1b400f1561606ce5734ef2d1d4a38f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 05:19:56 GMT
SHELL [cmd /s /c]
# Wed, 12 Jan 2022 15:34:02 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Wed, 12 Jan 2022 15:34:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Jan 2022 15:34:04 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 15:34:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jan 2022 15:34:19 GMT
USER ContainerUser
# Wed, 12 Jan 2022 15:34:37 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Wed, 12 Jan 2022 15:34:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:71dcb756adb8534a87210067788d6aa4a5a366b72d022b7af035e5263a3e54a0`  
		Last Modified: Wed, 12 Jan 2022 16:05:17 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9688a822af3207c76f479e1dcd24729a872b14ca7b578a5cf939c8da1beea82f`  
		Last Modified: Wed, 12 Jan 2022 16:05:17 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9392e95e3451d5255c7eb6f7082ecb82e722cc977e6a4e482dd4f191928d78e2`  
		Last Modified: Wed, 12 Jan 2022 16:05:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff7ad2a002508b7608d2069eb80fd73536913d79f8a080b2306aaac7967151f`  
		Last Modified: Wed, 12 Jan 2022 16:05:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d3d451d5b86383a9c3ed5b112c411d530439c1306c852d24920a9e3cc74144`  
		Last Modified: Wed, 12 Jan 2022 16:05:15 GMT  
		Size: 69.0 KB (68977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3aacb454a880cd5cf940cca71b6570e6eabd1e99834bba212fef2aab817436`  
		Last Modified: Wed, 12 Jan 2022 16:05:15 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25335eb984553f45fe31b623d29beed47507e001b21742a1ca35d8740ed03ab7`  
		Last Modified: Wed, 12 Jan 2022 16:05:27 GMT  
		Size: 100.2 MB (100186381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5121097c352d366839b63ee98e87cf4c1198effdd73c5d1b5fecacb3ea5526bf`  
		Last Modified: Wed, 12 Jan 2022 16:05:15 GMT  
		Size: 81.1 KB (81073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
