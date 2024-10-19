## `eclipse-temurin:21-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:215ea40ede33af1e83ff95f84f265ae5c2e03a57b1bb594841a186fad434b435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:2a2077e084243b104a6431cf7676e5e5763272007f3605e090012f90de96a70e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359775909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07c6498c2b308626cafe71f5a0b4c3ab8a6b6a57aaf09e7200e45d4645d44a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 19 Oct 2024 02:07:53 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:07:55 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Sat, 19 Oct 2024 02:07:56 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 19 Oct 2024 02:07:57 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:08:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:08:16 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:08:24 GMT
COPY dir:21acee06f7f20f6df9d2b0d45ba60360b710f331f6da7fc795fe21536879ea4b in C:\openjdk-21 
# Sat, 19 Oct 2024 02:08:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Oct 2024 02:08:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3c96c8c99661b7b781dc9ea8f232450962049c0731f5d58d3f0a7db31538b`  
		Last Modified: Sat, 19 Oct 2024 02:08:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab370e33e60801313403ae169448fc41ba398f3cded0926013d12a156592bb77`  
		Last Modified: Sat, 19 Oct 2024 02:08:39 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e33202abb54b59c5b446912c2beff6581d65500f4badbfe1abbda1bcaeb36e9`  
		Last Modified: Sat, 19 Oct 2024 02:08:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce531a773538cfe012c78db8c189dee2252eb9f46ba7809cd6cfa5b902e84528`  
		Last Modified: Sat, 19 Oct 2024 02:08:39 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20cd5f10902fcc94f62816a87e22e224308ccbf7bdc6965f5914ac8e3a2434`  
		Last Modified: Sat, 19 Oct 2024 02:08:38 GMT  
		Size: 67.3 KB (67314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ea4fbb18ebb931aae9da92de511facd446def34a08afbe3d87247337064ee`  
		Last Modified: Sat, 19 Oct 2024 02:08:38 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e908754f696c39a4a1fa8f6bfb018e68e3871bdf49f0e59e6ec1475c04569562`  
		Last Modified: Sat, 19 Oct 2024 02:08:49 GMT  
		Size: 200.8 MB (200752060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe9b6d34ec960dd1b7a8a69d15478a27070947b3d0eed7661d216fafc118df0`  
		Last Modified: Sat, 19 Oct 2024 02:08:38 GMT  
		Size: 3.9 MB (3856768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfe32a4983b4eb4dded452ca3ad990ba6ac330be941ed94e2bad38aaa7148c3`  
		Last Modified: Sat, 19 Oct 2024 02:08:38 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
