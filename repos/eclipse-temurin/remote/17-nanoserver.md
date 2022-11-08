## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1fbbe793a23ba8470b8d8d61d4182d6068187076a58019641cf57c5590c3a4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:07c3d14d4ed425ac71f56a51bdb09f48902ba0d55b197c622902086335daecd3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307694359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ce38a96b2a0af2ee44840f69c9e78d1f332d3ec99668d0792383fd7a4b3158`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Tue, 08 Nov 2022 19:27:23 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:31:41 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Tue, 08 Nov 2022 19:31:42 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 08 Nov 2022 19:31:43 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:31:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:32:00 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:32:18 GMT
COPY dir:a12ba5a18c812bc88dc6c1e12f0d0bdbacab70db88697cd6bad273d4570ac4fb in C:\openjdk-17 
# Tue, 08 Nov 2022 19:32:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 19:32:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd83067a7e6c6d9dab3ac0265a21919de95a0bf4e737e647fbf3e43c9874b0`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9fbea36ffc078ae0e4b51819bb0a036f7e4ed68b0ab258a75a21d3cff70968`  
		Last Modified: Tue, 08 Nov 2022 19:59:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bb56c987d6ccea4c4faf4e59e21868ba4b671a45348326f2f3a0635d36e7b6`  
		Last Modified: Tue, 08 Nov 2022 19:59:28 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2826d5cbecf5e352a40c64be93a8435927f58594941d3700c3b66bd1a4ea5a12`  
		Last Modified: Tue, 08 Nov 2022 19:59:27 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c698d6626dffc79e30d4b30ee1b35f3196235422377db691449c4479ecf335`  
		Last Modified: Tue, 08 Nov 2022 19:59:25 GMT  
		Size: 81.4 KB (81405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e989e10d6bdbb37e4d9ae67fff479d4652dc06b485f73ae4607bbd93cfcdb14e`  
		Last Modified: Tue, 08 Nov 2022 19:59:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6725da78579eafc2a9ad8c1b02254528195968c0072793fd01b40a9392c2a997`  
		Last Modified: Tue, 08 Nov 2022 19:59:46 GMT  
		Size: 185.4 MB (185422397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd4caaa25490d73540786fdba0d6199d74089e75749de9c1cfaaaf5af2dacd8`  
		Last Modified: Tue, 08 Nov 2022 19:59:25 GMT  
		Size: 91.5 KB (91504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dee44b889dde55fd1fcdbbefc3e3f0904870acdbeebd0c672932fa715b24e9`  
		Last Modified: Tue, 08 Nov 2022 19:59:25 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:84da831330ec6ec917140a87878b984edab01d10807223a3207d7031c20abd3c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295893361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1dde02cb612ae9e8fca4681b293a4d8512e9cd74362ad714bc2800313526d9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:05:04 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Tue, 08 Nov 2022 19:05:05 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 08 Nov 2022 19:05:06 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:05:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:05:19 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:05:36 GMT
COPY dir:a12ba5a18c812bc88dc6c1e12f0d0bdbacab70db88697cd6bad273d4570ac4fb in C:\openjdk-17 
# Tue, 08 Nov 2022 19:06:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 19:06:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728b19a01e1b46a120b42a3b2a7535421722e52ce56376a673ad470d61c74f6d`  
		Last Modified: Tue, 08 Nov 2022 19:52:25 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ec0e424a6fac75aa67218f7a281c11d03d0d64b9f50922427f6441d2b82c95`  
		Last Modified: Tue, 08 Nov 2022 19:52:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed85d131d2f653cf456952c38b38099abd8089e91bebc9bb827f08e2cdba1c9`  
		Last Modified: Tue, 08 Nov 2022 19:52:25 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e76cd29e9e7987d476226ff8e87682ec0bc20ac4ec608747c2f45705846a94c`  
		Last Modified: Tue, 08 Nov 2022 19:52:22 GMT  
		Size: 70.2 KB (70186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fe828122921910e65a8a25576dcd55c815908b58dea415dc13bc738c8a0523`  
		Last Modified: Tue, 08 Nov 2022 19:52:22 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7693e5e63a2d8c8efc49e9941ed4fc3a3187a8e73712a85b58586e9e7c2b102b`  
		Last Modified: Tue, 08 Nov 2022 19:52:44 GMT  
		Size: 185.4 MB (185427863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d39917ef6a3f4586f0507b905f3d4f482327ed469defe39544927149e272927`  
		Last Modified: Tue, 08 Nov 2022 19:52:23 GMT  
		Size: 3.7 MB (3664936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afd4aec47b01ac7c25db8fb9fe7a6e1010c905bc2f4999ea8d7f783a43201ed`  
		Last Modified: Tue, 08 Nov 2022 19:52:22 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
