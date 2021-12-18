## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:89e1e9da1003370ef2ab679d11e43bce7bad09fb52db8ff6fc2a3db7c1a890a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull eclipse-temurin@sha256:e152acc78a102c0a989bf50173ee2f5abbc5870b4c4359ed3bb03ee4cc16b1c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145777499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940f58b14b8b69d3e0d3edc8e0dbc94c5891741879eb69f026cc3cebc5c0fec7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 05:18:44 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 05:35:01 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Sat, 18 Dec 2021 05:35:02 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 18 Dec 2021 05:35:02 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 05:35:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 05:35:15 GMT
USER ContainerUser
# Sat, 18 Dec 2021 05:43:32 GMT
COPY dir:6031cfac1e4bd8de6c5533bea0aabc25715779d854db7f41b8aea3e1449ff0bf in C:\openjdk-11 
# Sat, 18 Dec 2021 05:43:47 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4c557aac927613dd487d7c04b01a8eeb8ad174693f61b14c8f4285f1db6afdd2`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fa60c368d5bb9faa3ad271daca3b9a6fe74a9b5e70d653bc6d67ad3450f552`  
		Last Modified: Sat, 18 Dec 2021 06:16:33 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9255e05ef5fec9b6cd7ad18f075a54f693830ba74909a117138108f53defa97d`  
		Last Modified: Sat, 18 Dec 2021 06:16:33 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf074477c9367c74d409e04f2b827675a3880bb0ef74271edad2042c0c749e`  
		Last Modified: Sat, 18 Dec 2021 06:16:33 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee8be34dd79508052db04b5a53af01efbafe32cb6a4d8abe7994b6a70e79481`  
		Last Modified: Sat, 18 Dec 2021 06:16:31 GMT  
		Size: 68.8 KB (68848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488890323943c28acb7a2561bcac21b1d1073598007b7205947af2336ce64d77`  
		Last Modified: Sat, 18 Dec 2021 06:16:31 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a8a726427d62a6eedc2e8a18177fd6386358c0de345da59b687d385f3368f7`  
		Last Modified: Sat, 18 Dec 2021 06:28:56 GMT  
		Size: 42.7 MB (42717437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a635172337876bc9d7da1279cb7bc7049ac08af8c37a0dcf86c78c315f4b66`  
		Last Modified: Sat, 18 Dec 2021 06:28:48 GMT  
		Size: 81.4 KB (81412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
