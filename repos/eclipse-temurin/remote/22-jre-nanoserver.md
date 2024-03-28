## `eclipse-temurin:22-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7d9e01a0e1092cd3b24316e81230637dd01d8d0b17e8c629188e5e5414e3508d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:22-jre-nanoserver` - windows version 10.0.20348.2340; amd64

```console
$ docker pull eclipse-temurin@sha256:adcf0f4d6389b3371beb915c446602ba947cf36a8cf1bc3e04cd30c5f405eb03
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169328185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7746b90fbc6b228d145ffea42023f0280fe1b4407784a5fde76bfb569bc47878`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:20:55 GMT
SHELL [cmd /s /c]
# Thu, 28 Mar 2024 01:33:01 GMT
ENV JAVA_VERSION=jdk-22+36
# Thu, 28 Mar 2024 01:33:01 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 28 Mar 2024 01:33:02 GMT
USER ContainerAdministrator
# Thu, 28 Mar 2024 01:33:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Mar 2024 01:33:25 GMT
USER ContainerUser
# Thu, 28 Mar 2024 01:34:11 GMT
COPY dir:205bc28a2cfde808c3c902b087992a6d179f1f6b12b6c0fffa64f09e3dab56d1 in C:\openjdk-22 
# Thu, 28 Mar 2024 01:34:23 GMT
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
	-	`sha256:2cae91a355f117e36f8601eb8bbecd3204be41a74eb3c060e221d3473c7fc480`  
		Last Modified: Thu, 28 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701197661d7d6b1888ca71f6fdbe3a8dba48b4a4520819924d7a2ac894746350`  
		Last Modified: Thu, 28 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eec842d09161a6d90b7bfecb4bd349fd3e5786ad48ffce9234936523fc3f46`  
		Last Modified: Thu, 28 Mar 2024 01:40:26 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef885139e5bbccead0be23fca4419f1cf65a5779b37207ce1767e6ff73821e4a`  
		Last Modified: Thu, 28 Mar 2024 01:40:24 GMT  
		Size: 78.3 KB (78256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747f96e45555c2291908aea8e63c4e52c087a3e6862a8152ca3f63664fc70909`  
		Last Modified: Thu, 28 Mar 2024 01:40:24 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ae5d456f9749d35e8e3ef763df9d94d6db974de7bd24203f301e503713ff99`  
		Last Modified: Thu, 28 Mar 2024 01:41:04 GMT  
		Size: 48.5 MB (48479946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3513cbedd658f7f5f1275636796913d3b4b2eb9a9589d7f3cfa741431299abd6`  
		Last Modified: Thu, 28 Mar 2024 01:40:55 GMT  
		Size: 61.5 KB (61510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:fdd5114036ab79907bacedc33da33b6a38fbdcfd90121631795b9fa85c86539a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156564164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb00eb65ef0dfa746adf872b8cb8461d1c9f7e98a3609a0b23053dfb23dc4d3a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 00:41:38 GMT
SHELL [cmd /s /c]
# Thu, 28 Mar 2024 01:25:00 GMT
ENV JAVA_VERSION=jdk-22+36
# Thu, 28 Mar 2024 01:25:01 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 28 Mar 2024 01:25:01 GMT
USER ContainerAdministrator
# Thu, 28 Mar 2024 01:25:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Mar 2024 01:25:21 GMT
USER ContainerUser
# Thu, 28 Mar 2024 01:30:53 GMT
COPY dir:205bc28a2cfde808c3c902b087992a6d179f1f6b12b6c0fffa64f09e3dab56d1 in C:\openjdk-22 
# Thu, 28 Mar 2024 01:31:03 GMT
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
	-	`sha256:57cb9c24ea67642372d52c48fd29ea184f577c493da96e7582cb21988f552c86`  
		Last Modified: Thu, 28 Mar 2024 01:38:49 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9c0feed8d9a7949e6c0a11940c910c82470fee50ac0f29eef348b61f48b260`  
		Last Modified: Thu, 28 Mar 2024 01:38:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c45826021dd09b48f82f606aacc2162cda51c6c39996b3af9982654d63888a6`  
		Last Modified: Thu, 28 Mar 2024 01:38:48 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3277bafd8f072d26debee2e8da6934103c9058785ea67a0a27363fd519cb1f7`  
		Last Modified: Thu, 28 Mar 2024 01:38:47 GMT  
		Size: 67.8 KB (67769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65288dd7c5e5daed3e41f2428a4d2b9a964f365e3c0ec0ebd0615e95ad3141e5`  
		Last Modified: Thu, 28 Mar 2024 01:38:46 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e4abce25a96b6f0a21125413f7cede2870ee81e3eea15e6bcc373d611d6f5c`  
		Last Modified: Thu, 28 Mar 2024 01:40:08 GMT  
		Size: 48.5 MB (48476650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfc69468f880948010e0355c951eddddc27f2e3c36b50c465f7f7bd25f3f9ce`  
		Last Modified: Thu, 28 Mar 2024 01:39:59 GMT  
		Size: 3.4 MB (3393814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
