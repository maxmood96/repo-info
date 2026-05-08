## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:6e11234743e3f9645394d23c607b20334e41281d7bc02c4216b59004a97e395f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:8d3e43fd7ccd874d2ec284696d1d003b4909dc2c5c51f058f7f6d92eeaa9b40e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170977588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8847dd37a0dddb1478457cb9dec9c5e7659f39de9a4e58d5e04dadc4d407ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Fri, 08 May 2026 01:19:10 GMT
SHELL [cmd /s /c]
# Fri, 08 May 2026 01:19:11 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 01:19:11 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 08 May 2026 01:19:12 GMT
USER ContainerAdministrator
# Fri, 08 May 2026 01:19:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 08 May 2026 01:19:23 GMT
USER ContainerUser
# Fri, 08 May 2026 01:19:41 GMT
COPY dir:2f70d7e82fbe25185baf6a6b1e05b870cb38c3ad05aac5b5932c695a93320f91 in C:\openjdk-17 
# Fri, 08 May 2026 01:19:45 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb3ed8bc3f412b5e0d41967f56ec38a3784867fe97418c4e81f14bc8a0fc390`  
		Last Modified: Fri, 08 May 2026 01:19:51 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8904d54487912731d9121615bdbf728c267341e8aeccf40e44ec1c41a470b2f0`  
		Last Modified: Fri, 08 May 2026 01:19:51 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe94fd9df9e854d5e75119aa2e946b6d3802cd67992d8ab31da37ecb3846f1c`  
		Last Modified: Fri, 08 May 2026 01:19:51 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9b562fbbca564cbbd69112baa6faa819d7326004fdf7a15887abbb85a192ad`  
		Last Modified: Fri, 08 May 2026 01:19:49 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e5c9f598c173cff694a4e07103789d91214a9aa24ac0d6f5ccfce7805f0dbc`  
		Last Modified: Fri, 08 May 2026 01:19:49 GMT  
		Size: 73.2 KB (73195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b12ef0ed4f6506a20b66bec29dbc960e5b47bd77546bd40a91ef15dc87a5c3`  
		Last Modified: Fri, 08 May 2026 01:19:49 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5b2c3e9a32e37a0a9bf38233f848f4b80b95b1044c5f279600621f4830a40e`  
		Last Modified: Fri, 08 May 2026 01:19:55 GMT  
		Size: 43.8 MB (43833718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01b00b4ea0177491c944aba430ca4696c28e49ae9f3fee3358209aa9a589d06`  
		Last Modified: Fri, 08 May 2026 01:19:49 GMT  
		Size: 109.4 KB (109382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
