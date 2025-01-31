## `eclipse-temurin:23-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:bc060b60e585abfdc61a0b857d9be0d4541ac4da8f7caa1f8131dc4d5973e743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:23-jdk-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:64c4acc3746dd534941920a48770712cfc18bc94fae7578d8bf3775dd8c0a1ed
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.5 MB (368453162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33d9d5b0451f5bf7ccface2223ef8109c13a00fa8e8c7acf5715caa960fbc5c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 02:12:04 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:12:06 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 02:12:06 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 31 Jan 2025 02:12:07 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:12:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:12:32 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:46 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Fri, 31 Jan 2025 02:12:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e737ac5508e866496944da08191b6b2d78b987fca5bad30c5d4aa6f1b7bc26`  
		Last Modified: Fri, 31 Jan 2025 02:12:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a4ad27d258480dc73df4856594aa1a5cb488ded66223552cf150e2e7211864`  
		Last Modified: Fri, 31 Jan 2025 02:12:57 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94dd882b3de0c33394a25589360480863907bde7774dbf0c365837fedf725be0`  
		Last Modified: Fri, 31 Jan 2025 02:12:57 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6263f90d047fd028a87c9001a04418143cbf22b1b1956fb8ef32c05a5df619b3`  
		Last Modified: Fri, 31 Jan 2025 02:12:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34282ab5585e4c156d8a08a145f2fe02660b8c9088da22ac8abd79ec47621e98`  
		Last Modified: Fri, 31 Jan 2025 02:12:56 GMT  
		Size: 67.1 KB (67146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e524b335755bda8421873eec0fd42191a29b740c12a61e1223b81ddf3157e6ac`  
		Last Modified: Fri, 31 Jan 2025 02:12:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d16831d7390cabd4085ed02383f87109a04fbdc80afc8d344e9ecbe7f46dd2`  
		Last Modified: Fri, 31 Jan 2025 02:13:08 GMT  
		Size: 209.0 MB (209028178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bfd7645ac1d37b3ee701893ab1245de5b7556ab479c4a0dc3fd66aed83088d`  
		Last Modified: Fri, 31 Jan 2025 02:12:57 GMT  
		Size: 4.1 MB (4084025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c58fcd6d489f87b5f6ff7afe2224e9f0f610a2a707d0942434f1b551ef4d530`  
		Last Modified: Fri, 31 Jan 2025 02:12:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
