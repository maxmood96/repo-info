## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:90d6a721310cd87122e7b0c6b5db052fa09955820ab7e9aaf2ca48b884cfc9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:543f3f18cb367a4977a6d882f6353c3361383e2a09729dd62d041abbabdd4713
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314868974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce109db4c357923aecaa9514c3d87f7059ca45bf6b0482dbb51b1251b6b0fd9c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 06:09:19 GMT
RUN Apply image 10.0.20348.2113
# Thu, 16 Nov 2023 02:17:18 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:18:40 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Thu, 16 Nov 2023 02:18:40 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 16 Nov 2023 02:18:41 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:18:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:18:51 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:19:06 GMT
COPY dir:3378004dd1c559f9d7d6f4bacd149386aa6ab741f7dba391fbd8a10b1a80b205 in C:\openjdk-11 
# Thu, 16 Nov 2023 02:19:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Nov 2023 02:19:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1ca4fbe907f22e883670decfa8d7f4490a79a995bb83a6c286248c21d61a62f5`  
		Last Modified: Tue, 14 Nov 2023 21:13:36 GMT  
		Size: 120.8 MB (120753560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2f0edb58e1876347bbad88c907697db94e172aa6ff4a38560ccfb68d72aa86`  
		Last Modified: Thu, 16 Nov 2023 02:37:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17da8727ce4c05eb0ac5d2556f4bae44bcfc7182f8b68aa18e0ce3f5d5f4c7a`  
		Last Modified: Thu, 16 Nov 2023 02:38:38 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619db30282dc4b71d71d51df46474e984e03c281012879e44b94c28db05a117f`  
		Last Modified: Thu, 16 Nov 2023 02:38:38 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91d895e42f8926868d20203dd027e55b41e756b6f0e59c38f9707dc3eeb8d2a`  
		Last Modified: Thu, 16 Nov 2023 02:38:38 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e21aaa12f70b8a0296eec04bcf23166115d3ac45cd2966bb5ab2ed8b22b16e7`  
		Last Modified: Thu, 16 Nov 2023 02:38:37 GMT  
		Size: 78.1 KB (78051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b15e9cdc6258c0594edb12985429e990517aebff173af95a0a6d130c4cb4ab`  
		Last Modified: Thu, 16 Nov 2023 02:38:36 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5e8ee9d3f1994d9905eb83bb559b4e35c3a5c3e33fc693028deaec15d7bcd7`  
		Last Modified: Thu, 16 Nov 2023 02:38:55 GMT  
		Size: 194.0 MB (193969649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa898f4a0239d1366e889b05677eb481fafb17eebf3749a60ac0c02372453076`  
		Last Modified: Thu, 16 Nov 2023 02:38:36 GMT  
		Size: 61.0 KB (60971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86eecdd577dd0f9db25f4b45a85c66915637b3c05c70bcb9a2b56223765f389b`  
		Last Modified: Thu, 16 Nov 2023 02:38:36 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:1921186d834725209c3570a820a078b071aaa0b2229e3691eaa85a5339dde7f3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298624406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b7e57f0794560b567cfb92e7855917097c764221e691e632cbbdf51bcb024c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 01:51:25 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Thu, 16 Nov 2023 01:51:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 16 Nov 2023 01:51:26 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 01:51:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 01:51:38 GMT
USER ContainerUser
# Thu, 16 Nov 2023 01:51:54 GMT
COPY dir:3378004dd1c559f9d7d6f4bacd149386aa6ab741f7dba391fbd8a10b1a80b205 in C:\openjdk-11 
# Thu, 16 Nov 2023 01:52:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Nov 2023 01:52:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4310155f8eee56b296d809c0b64c304b9eb3a29e2f1d02624f32c177cea95882`  
		Last Modified: Thu, 16 Nov 2023 02:30:49 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650e34bd545b29edcc2ae1affdae2a78a27f414d2209a19da4dbc369bdcbb686`  
		Last Modified: Thu, 16 Nov 2023 02:30:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99cc8499cc732cad3ae9183c5dbbbfd8108c86124844783a2b2593c0e3e8f6d`  
		Last Modified: Thu, 16 Nov 2023 02:30:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97ecbccad5d7f6feacf54e359e81a90cb90b80773cd9000e04b3ecbc011b51b`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 68.7 KB (68689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af0fcd14761493fc6db7fc3e0ee0a2aa3f69e8c62004c86ffb367b875a276d2`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de83016c33857b55fb7388b994f7294e76ef6b716b09f4bc526a1d87d453d14`  
		Last Modified: Thu, 16 Nov 2023 02:31:04 GMT  
		Size: 194.0 MB (193969933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e31a6befc69cd78ebbd218fe16cb01b1ae73aba0d6be241244ca34c9d3e1108`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 81.5 KB (81469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aa411a77fa77c69cb5db7e8d49341958fcc94d097b60449718832f70518cfb`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
