## `eclipse-temurin:8u382-b05-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8c88c8352f5a3623a19299fdbc1987ee4ec09a8c6291ea6b0d378cbe48e4c950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:8u382-b05-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:90d04043a0d380c059d7f4cde0d904d8a244bf6b4ba48c6f5eaadf5a039a9197
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222133005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368cc3353812ec1cc7278504c9ecc2166376d10d18903ed8723e938e43750aee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:11:36 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Thu, 10 Aug 2023 00:11:37 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 10 Aug 2023 00:11:37 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:11:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:11:51 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:12:02 GMT
COPY dir:809f08e9d949f52aad6441d5338932efbf6208a06192d58db41d3e3c11ba3f9f in C:\openjdk-8 
# Thu, 10 Aug 2023 00:12:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3572ac06c9147f0946a40530f2197bb0101b82dd45b1defe04a8904a1c81a18`  
		Last Modified: Thu, 10 Aug 2023 00:30:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e89764c10b44510903b32c7edd36c21e79b25d8b06469e52cc62eda35374a86`  
		Last Modified: Thu, 10 Aug 2023 00:30:45 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceecc9a97f51e72739327b08e944e807b59412c3371154cd1517a1076f0ff13`  
		Last Modified: Thu, 10 Aug 2023 00:30:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6af468f1994e77d29a4fd32c9af35ed9cbc560bc299dae24b1be570c72bdc3`  
		Last Modified: Thu, 10 Aug 2023 00:30:43 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccc203e63ce253cf5087832aef09390ce453c9142f45b40e6c69d58bd390157`  
		Last Modified: Thu, 10 Aug 2023 00:30:43 GMT  
		Size: 81.8 KB (81786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f95e202c688c9a7e7c6f0f9bf6b76f2160d7aa79897363a9d892edd174453`  
		Last Modified: Thu, 10 Aug 2023 00:30:43 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887cf0cd4cb99c29ac1b12412a8139f04c0eaa6e588f91686bdb450e4ee998c7`  
		Last Modified: Thu, 10 Aug 2023 00:30:56 GMT  
		Size: 101.5 MB (101482958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa737a9920f31dc482f0b642360b685e52600f01b58740afd24afa78e77d100`  
		Last Modified: Thu, 10 Aug 2023 00:30:43 GMT  
		Size: 62.3 KB (62301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
