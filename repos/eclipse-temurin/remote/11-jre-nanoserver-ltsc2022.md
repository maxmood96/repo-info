## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:87b36e7d1623997e4ebf7a51ae92721ff8dc9b1d12196efaa4f7ad6f9ddb10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull eclipse-temurin@sha256:0ded52ca9a04d28cfec17b18c3e0b549abd233404ab80a9d1b25a6855ebbe21d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163962029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decfc5cbe364ab67d1a3a03e0415edc22d06011bc0dc897d3ac74e5be77b8760`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 Aug 2024 19:28:00 GMT
RUN Apply image 10.0.20348.2655
# Tue, 13 Aug 2024 20:19:48 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 20:20:46 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 20:20:47 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Aug 2024 20:20:48 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 20:20:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 20:20:55 GMT
USER ContainerUser
# Tue, 13 Aug 2024 20:21:36 GMT
COPY dir:d312cd25f7717f1c23a729ceda7f0a5b69cc56184795f5759819b3fb155af4e0 in C:\openjdk-11 
# Tue, 13 Aug 2024 20:21:45 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:695cae91f2de8dadf81c8b3a95f4942533ef064a72ad8fa7843cca84a839bfba`  
		Last Modified: Tue, 13 Aug 2024 20:02:51 GMT  
		Size: 120.6 MB (120554921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8146ec246b230c09f8b628d688c831ad1269b9cef24c5c95a8d1eb2f76b89bdc`  
		Last Modified: Tue, 13 Aug 2024 20:40:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4d702d09964f58a74605ef70f3bbac3f639bce491371021adcb4d2b4431a18`  
		Last Modified: Tue, 13 Aug 2024 20:40:42 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98cfd66c50a25e90135d888df9f5e21b476aa1da805b29d0921ed4a07ce1bef`  
		Last Modified: Tue, 13 Aug 2024 20:40:42 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183fbd712a963e52e7d253d6f5a82c3839adf9587bdfdc2de59a66b9e0a7612f`  
		Last Modified: Tue, 13 Aug 2024 20:40:42 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab1922c39f4c578f7dd56e6ecfbd28b0d148e6de4f7d04f37b8230cd28c101e`  
		Last Modified: Tue, 13 Aug 2024 20:40:40 GMT  
		Size: 77.3 KB (77277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624139632c148578ac7f39ac34ca86fc98cf280b210ba99f2df91bdcb1c565f8`  
		Last Modified: Tue, 13 Aug 2024 20:40:40 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a3030283928c404941c52e6d6a3a3fd4c443680e84e60ad1189fb5e5a5a26e`  
		Last Modified: Tue, 13 Aug 2024 20:41:09 GMT  
		Size: 43.3 MB (43263238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbbb5ff9a6356ba901caaaec030dbcf7ab25d8cc31b0b5124b7fa8b5cea13e2`  
		Last Modified: Tue, 13 Aug 2024 20:41:04 GMT  
		Size: 61.0 KB (61001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
