## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:fe81520b483203f06a19295f7b0be01dbba77a8cac4a122db532e8ab2223b23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:6dc7e9969cc5ca60eaace5022d87fc1707405fc93b85f7bea3a80dcd3c2b7175
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153720074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05be022baedbcc1f78dd208d83132167cb292b16cafaa86ce5d7a0fcc7ddba24`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:17:00 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 09 Apr 2025 01:17:03 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Apr 2025 01:17:03 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:07 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:17:11 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Wed, 09 Apr 2025 01:17:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dc514fefbf2d0cfc7984b3a58ae947f59a63a9314118a77c01af4e5dab65ac`  
		Last Modified: Wed, 09 Apr 2025 01:17:19 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f42753104e204304bc7ff86ec5db339a81af1fe5fa4fb2dad7ca78d2ff03fd`  
		Last Modified: Wed, 09 Apr 2025 01:17:19 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1713f59e5f0f196b7df5ee248f889b416f3f36372da2a539241286a4462293`  
		Last Modified: Wed, 09 Apr 2025 01:17:19 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a5f811168e67fdc05c94ffc17dad4ff51fd79dd3c3365a1a8efe0f7361b4f7`  
		Last Modified: Wed, 09 Apr 2025 01:17:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6647f1764f769fb166bfeb8a6ceb21acac502bdbc2a26bbd91c1582da4f3b94a`  
		Last Modified: Wed, 09 Apr 2025 01:17:18 GMT  
		Size: 70.7 KB (70700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e2e19566a976e5bd865319568e52bbca156ee516b3558881bd41c85c88c7f7`  
		Last Modified: Wed, 09 Apr 2025 01:17:18 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5138965f2f6a5875324d759dfd93f984deb8a8e7e79f1508840302a7aef97c`  
		Last Modified: Wed, 09 Apr 2025 01:17:23 GMT  
		Size: 43.7 MB (43728614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bfec6f6b85768e75f0c22e93566d4dfdcf8b03874106e089c71d295db43997`  
		Last Modified: Wed, 09 Apr 2025 01:17:18 GMT  
		Size: 3.0 MB (2993105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
