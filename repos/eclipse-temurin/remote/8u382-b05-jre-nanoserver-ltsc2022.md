## `eclipse-temurin:8u382-b05-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4f45cfccd6334ab5ac052bfab64da8081d84116d70dd62947c96db800f4836f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:8u382-b05-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:134e79556068470fb178f07d94009c8e890d40617a55d76055da3c5ed65b0d84
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160631153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd7943b88f1d3c5803006fe0fcabac76337d21be42336a6df2d87a24fbca695`
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
# Thu, 10 Aug 2023 00:12:25 GMT
COPY dir:f24575d0fd9e2979f5a8010c202ec6d963a3eb3cd788517e3ab1d758c8e6ad81 in C:\openjdk-8 
# Thu, 10 Aug 2023 00:12:36 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:60bbe066c65c91bff5723f12a782298ad14fd0e4d3afa17e3c625f32737905c5`  
		Last Modified: Thu, 10 Aug 2023 00:31:25 GMT  
		Size: 40.0 MB (39981094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251cebcfabc8ebdf0f77e50189fdc648be1cd94aeece3bfb4c3aa9d5f987279`  
		Last Modified: Thu, 10 Aug 2023 00:31:19 GMT  
		Size: 62.3 KB (62313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
