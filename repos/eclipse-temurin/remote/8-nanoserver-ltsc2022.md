## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7b59d2e5ceeebd7cf3ca3a2b88a91b4904c0d00927d57a08ba8a43ee8a24a96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:c443930b6b91d2e8e4e58394b43a0798b53f9588724458aeef48dde51489e9a6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225215570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9400649b3e3f70514af1f4deb446900b5eac3439679a86b591ab6ca384b83a90`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 22:24:27 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 22:24:28 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 14 May 2025 22:24:29 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 May 2025 22:24:29 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 22:24:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 22:24:33 GMT
USER ContainerUser
# Wed, 14 May 2025 22:24:39 GMT
COPY dir:5c4bbf817a67c787f7f2d8809dee99be16882c3512e063f4e47205ca5ccbd190 in C:\openjdk-8 
# Wed, 14 May 2025 22:24:43 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdddafbb8c83403994c987810dff76f6ea56acfdb12187e0aa8d124d54bc3f1b`  
		Last Modified: Wed, 14 May 2025 22:24:47 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a67a056b84bf770a43f1f6a155bcdbab8a1a6d94f78cf57ee5f0ace3ce9445a`  
		Last Modified: Wed, 14 May 2025 22:24:47 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fa67632e276e18cf60a6bf18fac1c3b008deb2cab8827f2713a29a84652abd`  
		Last Modified: Wed, 14 May 2025 22:24:47 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c11cb3a5f9e6f04f7a854eab2b5208aadd010ee9160809c91b4904c48da37f`  
		Last Modified: Wed, 14 May 2025 22:24:46 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f46030fc4e7c3cf61cd6be77940cf49e1d25388c2b9c21ed0138986cb33333`  
		Last Modified: Wed, 14 May 2025 22:24:46 GMT  
		Size: 76.6 KB (76576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726984b6e9a74772c5a87ce38d33254769b57482196ac107f9cad88d098b1ea6`  
		Last Modified: Wed, 14 May 2025 22:24:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb0239d426c37e657182c4b5ccd242d89f0648b1c897db2c3edf7cb4b27bacf`  
		Last Modified: Wed, 14 May 2025 22:24:52 GMT  
		Size: 102.4 MB (102438990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0196b4db63919e8e20b1eec9a7118aec03a56f2807cb497491e68b4d35abcc`  
		Last Modified: Wed, 14 May 2025 22:24:46 GMT  
		Size: 118.1 KB (118121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
