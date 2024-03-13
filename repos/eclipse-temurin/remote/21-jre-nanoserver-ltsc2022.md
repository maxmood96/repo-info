## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:bb2d488cac7867f7bb2949f7c483205d8d002710a5b4f40d34517b1e38b5d0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull eclipse-temurin@sha256:a6ab8f374df920169b45d012902f6f4e00806a23933607bd5153a7a8d3154f3c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169595682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53821e40a51af119721fac2b843e6b4673fa34dcb0338e5b3c11e6468487a631`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:20:55 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 01:24:40 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 13 Mar 2024 01:24:41 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 13 Mar 2024 01:24:41 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:24:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 01:24:50 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:25:32 GMT
COPY dir:a5c64f66204a1ce40e58093b44657f9abbd9eecac263988d919d778d3cf84131 in C:\openjdk-21 
# Wed, 13 Mar 2024 01:25:44 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e98336f720b829e374bd1d59306210d3700861b11d3df51506afbc0b50d039`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83efc8de11af0e25519b85abf96148f2475793f094309066eac652639fbca18`  
		Last Modified: Wed, 13 Mar 2024 01:42:43 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9995cb7c9edca2bb5c3e11f694a46b8b73631df18c0a526ea0cd8f842ac0a86`  
		Last Modified: Wed, 13 Mar 2024 01:42:43 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6539a489b4b129670fb26d05666ef23f4e16d1f2f6beb79f115c8f147b072c`  
		Last Modified: Wed, 13 Mar 2024 01:42:42 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed259747ed5cfe2c11b088f085eb60f2fb1971d82dc0262948b077f1d7abe4a`  
		Last Modified: Wed, 13 Mar 2024 01:42:41 GMT  
		Size: 76.6 KB (76611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4f3340acaf5e2a8813f189f6a862a5718c405303b59a3940e85592a45c6bd4`  
		Last Modified: Wed, 13 Mar 2024 01:42:40 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976e2eb6345caad46805e1a84cd8117fa5dd18858f10636db00d8919e1944a0c`  
		Last Modified: Wed, 13 Mar 2024 01:43:19 GMT  
		Size: 48.7 MB (48749835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45b3f25a342ee1335ba920574e2025f873c804a61136ff03e5235120fca1b84`  
		Last Modified: Wed, 13 Mar 2024 01:43:10 GMT  
		Size: 61.1 KB (61108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
