## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:07334bda7dacaef3ab0686c519ee01cd1ffacfa995f8c0f020989b203a55ed9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:952e30695b95afff16a5afad598765d413892c204ee55ed6d541a5f10883f43f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209532851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6745856c183982f9f16aaa17ca1ca79f240eff626b05a78a9c31ba3d3a7988`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:17:04 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:05 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:17:06 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:17:07 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:10 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:17:17 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:17:21 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4a9cf2fc7af908b726e9ebe0ef9df28c4fe20326597b3ba269fdc98b858625`  
		Last Modified: Wed, 09 Apr 2025 01:17:25 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149d27841e1abbbbaa820d10d6543425c4c83558346120934de52632fbb7b494`  
		Last Modified: Wed, 09 Apr 2025 01:17:25 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ed874f3a5edb38d19a33a6ff360388a7953b8ee1d064bea592b4f00a5039ec`  
		Last Modified: Wed, 09 Apr 2025 01:17:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25df916e9c16032a143304f10f185fd2eabcd6261125e0f0f56591db8d3c28c1`  
		Last Modified: Wed, 09 Apr 2025 01:17:24 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc4146513325951684e20a940e2c9f04d64bededd8cc01f4c4e10ac5a88779f`  
		Last Modified: Wed, 09 Apr 2025 01:17:24 GMT  
		Size: 71.9 KB (71943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7abc1fff11455d5351c0ea445beddc1976b10b5948d7991a9e711ab366840d3`  
		Last Modified: Wed, 09 Apr 2025 01:17:23 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881a36420c941eccb94e2ec17f566162f1742852fcfd2640e5d0973a5eb1f5ca`  
		Last Modified: Wed, 09 Apr 2025 01:17:30 GMT  
		Size: 102.4 MB (102433306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b3272a80b37d1ab4680c99a01ae4cbb982eb4b923b7a87c7cca62fa434d5a0`  
		Last Modified: Wed, 09 Apr 2025 01:17:23 GMT  
		Size: 99.9 KB (99930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
