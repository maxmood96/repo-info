## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e775aaea0ecf60f908403e3789f958ee5adb72fb402f640beb67de54a381bee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2340; amd64

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

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:a493a78c4938c920c64cde5785d126efc140b0d382015f371864e7eb5ee9cebb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156810702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc175d50d2d70842507eeae015adbb2b09b7cfcc95303128d2460132cd3657c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 00:41:38 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 01:15:13 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 13 Mar 2024 01:15:14 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 13 Mar 2024 01:15:14 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:15:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 01:15:24 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:20:37 GMT
COPY dir:a5c64f66204a1ce40e58093b44657f9abbd9eecac263988d919d778d3cf84131 in C:\openjdk-21 
# Wed, 13 Mar 2024 01:20:47 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569a24b1d9b596a48436098ac5fe49c52e3153cd3bd147e365a80a4059570fd`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2a4287941008944a771e7303adc0fe34dae600d04a88a2a4801f943368b788`  
		Last Modified: Wed, 13 Mar 2024 01:38:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd3c4943c07a2ce8dda98e2064fc5250e5cfb00be821232c623fefe881666b`  
		Last Modified: Wed, 13 Mar 2024 01:38:58 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3d5e15f5a67bec2b3837fbdd9d9b53e3c559507352db87b240dd9a18519e6a`  
		Last Modified: Wed, 13 Mar 2024 01:38:58 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ae2b43cfa06f4f8dee3385edeccfbad111ee4ef72cb34375433628a971ee8e`  
		Last Modified: Wed, 13 Mar 2024 01:38:56 GMT  
		Size: 68.8 KB (68831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8baa61a5bbf475bcc2bd6199af0dd2cfcbeed38ec7e3ab81b205b860e125d2`  
		Last Modified: Wed, 13 Mar 2024 01:38:56 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a5ea3ccedcb419a3b9ce0539af7367badf4471626a578dd7ac1951b07891ef`  
		Last Modified: Wed, 13 Mar 2024 01:40:16 GMT  
		Size: 48.7 MB (48749872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7bbe4cbe853ab25bfe1423f99fe2a9b8fd9845953d0ec974a7e32d68fc7e69`  
		Last Modified: Wed, 13 Mar 2024 01:40:08 GMT  
		Size: 3.4 MB (3366163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
