## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:668bb6bd79c6682f45d673dacf16848e10c12e8d713332f8fb3ab54dabcb29a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:438f4ba58f04e0220089b281d311bc2b50f9199e7ae928e190177a1affcb84e0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223281047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80c005a6500f9f98ea98d47c10c31d312606f8e0a779680d128d35d24c5f5f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:02 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:03 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 02:11:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 31 Jan 2025 02:11:04 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:09 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:11:14 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Fri, 31 Jan 2025 02:11:18 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f199657438eb77d59b38021b80b14f2ba6015665359c6a0afa05c2e205bed57`  
		Last Modified: Fri, 31 Jan 2025 02:11:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ea1a55f99aefad6f39abb828497624366e3433865d9f23c9dbc72c326e5ec5`  
		Last Modified: Fri, 31 Jan 2025 02:11:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907a90a47bc784357b6b98b0758b9b7d5e76ed5b286421afb35472d697e51d70`  
		Last Modified: Fri, 31 Jan 2025 02:11:23 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f03657d108ee9d764cae4730ba77e610878f96af0f352512c8863afcb7cfa5c`  
		Last Modified: Fri, 31 Jan 2025 02:11:22 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fec1f9ed5adb9cdbcc25c921412c89c57d3ad3e144125957a83169e0c1e384`  
		Last Modified: Fri, 31 Jan 2025 02:11:22 GMT  
		Size: 73.9 KB (73866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4ca3b437598b503811c258714e84a98506222eab0b9857f57d9b1e56e2cd1f`  
		Last Modified: Fri, 31 Jan 2025 02:11:22 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d8df7341554e72cee8cb1ea3dd0eabe94546ed4d6b05999eb2ca849b4e4b4f`  
		Last Modified: Fri, 31 Jan 2025 02:11:28 GMT  
		Size: 102.4 MB (102431296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b590648c85ada435b0bc54e291b110cc840685700d3703b212a5fe3102cb4b32`  
		Last Modified: Fri, 31 Jan 2025 02:11:22 GMT  
		Size: 109.2 KB (109181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

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
