## `openjdk:26-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:bd24fb4210c3c22cc529e3152883ad169324227394ed1ab5c424dc8a1df50949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `openjdk:26-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:c6238a69442570834374763d8a1781b39c15d1928df5ba5fa536b8c9a70cc6b7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.4 MB (415383544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450b5c3ff33a2ae9175d31901a5d971f680e627eefc5098f761d55b33c0165b4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:20:51 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:22:24 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 24 Oct 2025 19:22:24 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:22:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 24 Oct 2025 19:22:26 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:22:26 GMT
ENV JAVA_VERSION=26-ea+20
# Fri, 24 Oct 2025 19:22:38 GMT
COPY dir:6bffdfd50160c82e6869fd0a690d084eedfe2bd58671ef19a440f7d2cd9a5727 in C:\openjdk-26 
# Fri, 24 Oct 2025 19:22:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 24 Oct 2025 19:22:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8407703267a708f1e861d96ba7297b491ec4181f89a12fcf487a7b283523fd8a`  
		Last Modified: Fri, 24 Oct 2025 19:21:56 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d049885f1168820d10689dd2a9b31272ab9b90fd4afe0e42ac7d201fc2634562`  
		Last Modified: Fri, 24 Oct 2025 19:23:17 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae075814f368a1aa2b03f2b072513d1a6ebb97b81c8ae08dffaaf673cee2e17f`  
		Last Modified: Fri, 24 Oct 2025 19:23:18 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf71f4e56980b0dfb80e1853c73eca005f0a2e5f2a1279427e6c3c37e9de53cf`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 72.1 KB (72108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e598fd04f697b70b20b173383d3399c6279de834e511631457c0c257fc0f95`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0900502dd016e7205278d4b7f5c0866bfbaf45e2d3b8423a56f3c5309c0c6213`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910e63b9d4989aeb9fb9ec1e8b1927705af0d813f518e3b8b5137fa984754f35`  
		Last Modified: Fri, 24 Oct 2025 21:24:39 GMT  
		Size: 221.2 MB (221151933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6be36a899281814aea046b135690305be2396eda7af2cd78585a20439bf551`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 123.6 KB (123637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8c4bc730d1794f83b9eaf05395a6ded49f06aa10cc319aaab9220782472100`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
