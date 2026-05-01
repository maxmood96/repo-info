## `eclipse-temurin:25-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:186827dad540a82a1e2708c986969850996158a3854481ef3f7b99186c78c538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:14f0560bcde4c28a040c456b6732f20f8c2707a14860c5c0b4dd52fab2634f5e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185749505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120554629150c1f08a0ec84bf7c736c487c37abc5de0e4b72a3a2707b3f099ca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Fri, 01 May 2026 00:08:25 GMT
SHELL [cmd /s /c]
# Fri, 01 May 2026 00:08:26 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 01 May 2026 00:08:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 01 May 2026 00:08:27 GMT
USER ContainerAdministrator
# Fri, 01 May 2026 00:08:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 01 May 2026 00:08:41 GMT
USER ContainerUser
# Fri, 01 May 2026 00:10:14 GMT
COPY dir:fd8baea77fa86bd13952f69621f69e815eb87406af0c0441c94fb1b8a78482df in C:\openjdk-25 
# Fri, 01 May 2026 00:10:19 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9eab84a9e1f2e6d55c6504872f175d8eb9e7ce2b40a70765eba12d7dff1eae`  
		Last Modified: Fri, 01 May 2026 00:09:25 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00648df02311ed062e14cd4679883a1f828a6e40efa81216c31767e64ab6e09a`  
		Last Modified: Fri, 01 May 2026 00:09:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94162ce0ea68d89d2ac717b7a993645b5e45a37a7f6b9a8e671328376b946e2a`  
		Last Modified: Fri, 01 May 2026 00:09:25 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc82f87b45ffe572d4dde69caef3286d14872d85ff8c9e4d3bff9767858c2830`  
		Last Modified: Fri, 01 May 2026 00:09:25 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033ab7e00536aa3a31ece781986436b095d5e9cde8ea957c89f4b85c05be13e`  
		Last Modified: Fri, 01 May 2026 00:09:24 GMT  
		Size: 65.6 KB (65626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058de18e0b125bed9756ff6cbbf10da262f97109e07a83651eda128f385d551d`  
		Last Modified: Fri, 01 May 2026 00:09:23 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a9315a66648f19e9fbef163d31150dc24c7ee3ab7ee8283f918cf70256757c`  
		Last Modified: Fri, 01 May 2026 00:10:31 GMT  
		Size: 58.6 MB (58620117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d29bd3d2d667fe77f0c18bb3249ec0c3dca4974496d2bed7e372f66c5fbf86`  
		Last Modified: Fri, 01 May 2026 00:10:23 GMT  
		Size: 102.4 KB (102448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
