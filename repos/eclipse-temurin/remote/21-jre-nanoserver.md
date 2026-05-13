## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fa58a9acf742f797bd9f52ade227d5d2d720c2caaeb2e2ed3eb839a9bf575fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:45a20b2c4f9e4440154dfe247cc01c2c6aa721d6356a37b09e699cfaa7a56cf3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (249012731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f80f2d96589c7458e56cc43eb34452e988bc8404563460fd4375e5eee2eaf72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:28:28 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:28:29 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 13 May 2026 00:28:29 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 13 May 2026 00:28:30 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:28:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:28:32 GMT
USER ContainerUser
# Wed, 13 May 2026 00:28:36 GMT
COPY dir:4940aac187beb0c950977243d0b1d703fc0231f7cabe77dd307cf1e9c831ffc7 in C:\openjdk-21 
# Wed, 13 May 2026 00:28:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4e820697cfc28931885e71a00ffe65b17be434d4aab29ceafd4f0234fe78f9`  
		Last Modified: Wed, 13 May 2026 00:28:46 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe234518ee55e5e83c2a6e3c4f72182a0c2abe249d37695c8eace7e39ea68dc`  
		Last Modified: Wed, 13 May 2026 00:28:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efc80a81c080086ec2359e677ca4878e6a71fc2f3951480d26c37ffb9f1d16b`  
		Last Modified: Wed, 13 May 2026 00:28:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c489a365b761642d688f54e15d1956fceedd705d470e9fedfdc568c4f508f59`  
		Last Modified: Wed, 13 May 2026 00:28:44 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee59943c102034ca7561b72b820ea8f7e285b4df78415935846c357040ec05d`  
		Last Modified: Wed, 13 May 2026 00:28:44 GMT  
		Size: 72.1 KB (72056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96af92263dbcd5093b59e9135ba884aa1c939a3d8bcf057f486dcbaef53ce448`  
		Last Modified: Wed, 13 May 2026 00:28:44 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d533562dfe398d6d1d7ad5de6eabc9c10eedede005a7545d61c6dc2368cf67a`  
		Last Modified: Wed, 13 May 2026 00:28:51 GMT  
		Size: 49.1 MB (49082935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddf41d701776d893ea67f3891c1251c974981d86e1c7c7fb5c1ce3ed2a6441c`  
		Last Modified: Wed, 13 May 2026 00:28:44 GMT  
		Size: 113.4 KB (113417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:619787146ea1831fdd59ef7d92211e9e3d1187514471f976786acb750f5875fe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176294383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188f0c73faa16ce327014c1c9ece2e2a462231bbfab8b9a1e280573e5292c7f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:53 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:24:50 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 13 May 2026 00:24:50 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 13 May 2026 00:24:51 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:24:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:24:53 GMT
USER ContainerUser
# Wed, 13 May 2026 00:24:57 GMT
COPY dir:4940aac187beb0c950977243d0b1d703fc0231f7cabe77dd307cf1e9c831ffc7 in C:\openjdk-21 
# Wed, 13 May 2026 00:24:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268beb93bae0a3fcb4f27b79193145978fd732af03aac83a53212232ff073dca`  
		Last Modified: Wed, 13 May 2026 00:24:15 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13d65ceb24ff16599f9d592a65fef42baa391bd8966c0f2b448622e71610375`  
		Last Modified: Wed, 13 May 2026 00:25:05 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74457710738f4d22d72b47d58d1b01f2c04d7f86591e1b526ecf2dd95d73dc2`  
		Last Modified: Wed, 13 May 2026 00:25:05 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b42f1f60e71fa552a4a209d6246fd6f8e59aafdbdee52b77eb35d509dde04b9`  
		Last Modified: Wed, 13 May 2026 00:25:03 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcefd5e7a3898290bb3fb99ba3eb902f16523589f65024239d09ad32d29e4068`  
		Last Modified: Wed, 13 May 2026 00:25:03 GMT  
		Size: 77.0 KB (77012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79b6648d1ef5dfea3779a699fbfa2331ae885f0e9d9b09d64a9e563b34dae12`  
		Last Modified: Wed, 13 May 2026 00:25:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa92faf3680c2e5e2a49eecc508c1ffc578896fca8c1d44bff13727a54066306`  
		Last Modified: Wed, 13 May 2026 00:25:10 GMT  
		Size: 49.1 MB (49082849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd19f5b692d76fb852758b9aebf3c6e999a2a647b67cdd4d1aa8cbca8bb1209`  
		Last Modified: Wed, 13 May 2026 00:25:03 GMT  
		Size: 90.4 KB (90351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
