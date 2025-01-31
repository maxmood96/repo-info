## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:783cd2bc71968898b9710620d788bb98ba0cb15ac953e74b2b27b3b2e92a8d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:c2aa1e54146390be5d14dd4b0db7e5ae65e90c9320ba4fa01c7bc90efa2d925f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257839859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811fd7a21fc29171a39e498cf7b95742eb0fcebab8a926f2fe39a510cc4e0a7d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 02:11:30 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:32 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 02:11:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 31 Jan 2025 02:11:33 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:51 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:01 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Fri, 31 Jan 2025 02:12:06 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b9a58a8cf552629dd8aa810c3d42dd3471ed852b6befa9e63c63ccafc09710`  
		Last Modified: Fri, 31 Jan 2025 02:12:09 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476c90ef3c29b170d8ad934cb0105cfa3ac84177e3fbf14b9991c3fd036612f`  
		Last Modified: Fri, 31 Jan 2025 02:12:09 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d433e684ac2261aebf4fe0d421f3e8acae67c4d7fc11b210dcb95d5285285447`  
		Last Modified: Fri, 31 Jan 2025 02:12:09 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e2710e87e5d16d733ec4c3b60f3dddb26a745affd7f46305d4c2e85fd29fd9`  
		Last Modified: Fri, 31 Jan 2025 02:12:08 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f7df3b11f321cdc73a3268283dd5123799ca04e58ebaa8f76a84f43076919`  
		Last Modified: Fri, 31 Jan 2025 02:12:08 GMT  
		Size: 67.3 KB (67346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6535b42d207723358b5d0b9be90a30a5f373566ddfa87086d61680e5ed301bde`  
		Last Modified: Fri, 31 Jan 2025 02:12:08 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92b0228baa627e8b230d9f9f03e41d616d68f0ecf526284b7dd77eebe887423`  
		Last Modified: Fri, 31 Jan 2025 02:12:14 GMT  
		Size: 102.4 MB (102431158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff661382cc4920287c73409f5b7c8f9731f20c48414086f65f4d60a35ada3d7`  
		Last Modified: Fri, 31 Jan 2025 02:12:08 GMT  
		Size: 68.6 KB (68601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
