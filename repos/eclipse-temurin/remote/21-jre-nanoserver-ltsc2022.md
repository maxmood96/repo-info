## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fddae123acb4821a15b62115dbd2174bae8b76630ff192b2a285b8a1ae292177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:8c1193a93892b633523dd36f4e6f44124d027464ae53037d965a0617616dd353
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176229516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8abd0b62bf60c0ebce893cb9701213ee4f6d825f7ee64c43558a3abcfd31c2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Fri, 08 May 2026 01:19:10 GMT
SHELL [cmd /s /c]
# Fri, 08 May 2026 01:20:17 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 01:20:17 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 08 May 2026 01:20:18 GMT
USER ContainerAdministrator
# Fri, 08 May 2026 01:20:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 08 May 2026 01:20:19 GMT
USER ContainerUser
# Fri, 08 May 2026 01:20:35 GMT
COPY dir:4940aac187beb0c950977243d0b1d703fc0231f7cabe77dd307cf1e9c831ffc7 in C:\openjdk-21 
# Fri, 08 May 2026 01:20:37 GMT
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
	-	`sha256:716882ca7cefc1d98c654278642b1df6f601dea95208d8c95a7ccd26e8acdaad`  
		Last Modified: Fri, 08 May 2026 01:20:43 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da186c2f7e08d95885a9a7b9ccfb2bd41db1e60cfec47fee6dc4a29ee7d759b2`  
		Last Modified: Fri, 08 May 2026 01:20:43 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7e46792a37fd42d1c2d34ff0d496ffd4c0a0327afbd8923398a6b4eb9a6d33`  
		Last Modified: Fri, 08 May 2026 01:20:41 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59dd16fa8dd3ddc76094f7aa32d38ac7f1c71fe524e30a3ebe02acedf3d2a2c`  
		Last Modified: Fri, 08 May 2026 01:20:41 GMT  
		Size: 77.1 KB (77134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a7a69584e03f1df652f442420a4650362138ca787b61df6bb091f291800759`  
		Last Modified: Fri, 08 May 2026 01:20:41 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981c755bf7e838241d28d9af9b878b02304588c73936dfd94ae02808af4bff7b`  
		Last Modified: Fri, 08 May 2026 01:20:48 GMT  
		Size: 49.1 MB (49082878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bcce1b0ccefded7d2fc2a5fa0d4afc1e54e27c41761713211ce1b58f7f62f3`  
		Last Modified: Fri, 08 May 2026 01:20:42 GMT  
		Size: 108.2 KB (108199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
