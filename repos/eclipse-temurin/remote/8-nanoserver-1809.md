## `eclipse-temurin:8-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:08639610543f5160ca9764bb62556dcb0277deee19765bcfb28aa5872703cd3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:8-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:c8768dbf6e508fcfad8a0b8baa573ec0e2d1a5f7ec64d02c2c6d85d6e5a796c8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211352484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220f192a24a5869b65e80568c51cd5fba456281c72e41926d55d63b801720905`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:42 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:11:43 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:11:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:11:44 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:11:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:11:47 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:11:52 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:11:56 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6cf7483a3034d01d420b750f53c1e61b7367c83bc60f2c0f1adf4d275841cd`  
		Last Modified: Fri, 18 Apr 2025 04:12:01 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db20f3c6f9805d6fe453f31a2c3cfa5258fb0c4d31d8963aa409bde60f008fda`  
		Last Modified: Fri, 18 Apr 2025 04:12:01 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c35a2b425dd3360dd9baeb7ca5f5878211cd2a2f69405c6a422e7ac7a3d9eb`  
		Last Modified: Fri, 18 Apr 2025 04:12:01 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245f12dbf5406c79a5e2c12d80a95186728f704082ba70cbcd6784a874a069a9`  
		Last Modified: Fri, 18 Apr 2025 04:12:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d78363dc8630ab0c4e9b28ff3c54d7c5e296487593e0b3cabeab0236c19cb1`  
		Last Modified: Fri, 18 Apr 2025 04:11:59 GMT  
		Size: 69.5 KB (69529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0367c778355db17b652bf920a74419bd7c09323d077f52d2445a6fc198a4b188`  
		Last Modified: Fri, 18 Apr 2025 04:12:00 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19be6c2452f194e7f923ba7e9866ede3f2acc07298d1438f9a1a03c63742e2d`  
		Last Modified: Fri, 18 Apr 2025 04:12:06 GMT  
		Size: 102.4 MB (102432706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b3b4cd0abb70fbc1cd2c18261421c3092e09930b6ff93875de8b050002ee91`  
		Last Modified: Fri, 18 Apr 2025 04:12:00 GMT  
		Size: 92.8 KB (92834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
