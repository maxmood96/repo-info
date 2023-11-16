## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fcf59cc75574fdd66f22d1f9c95088d7615ee1a385fe166d332dde02a83893b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:cf9567175018fcb58f06c46d3c3b78925a5051543732f43d88c1dd9065968fe2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164300423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2308b14d79f2ebca5cd020e9a967ff4e3408fb22e46b82b8c8c3f747648d643`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 06:09:19 GMT
RUN Apply image 10.0.20348.2113
# Thu, 16 Nov 2023 02:17:18 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 02:20:00 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Thu, 16 Nov 2023 02:20:01 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 16 Nov 2023 02:20:01 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 02:20:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 02:20:12 GMT
USER ContainerUser
# Thu, 16 Nov 2023 02:21:10 GMT
COPY dir:d3f692ac99669197443250e31cbc5c2f5282787fd78589cc9b6c2e91236738f4 in C:\openjdk-17 
# Thu, 16 Nov 2023 02:21:21 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:a6af13a0bdacebb67b2c2de5f087a7c9a54fd1ddc20291a3e0113601f6fc0358`  
		Last Modified: Thu, 16 Nov 2023 02:39:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933b6deb6421eea26b734f3c395e896c14f03c96cf94415a9b9d155d3dc40aba`  
		Last Modified: Thu, 16 Nov 2023 02:39:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905a570baca945dfb2069746c271640bee4b949a7f068d15dabfddc23623105`  
		Last Modified: Thu, 16 Nov 2023 02:39:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cba15fe50e81fd8c7e1ece2183869b0eb961268ba23bc1f1cd246b54d46616`  
		Last Modified: Thu, 16 Nov 2023 02:39:25 GMT  
		Size: 79.2 KB (79166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7d503f34fb8c292cc2bbcaff06c5e71f57109209f99917719b53097b237821`  
		Last Modified: Thu, 16 Nov 2023 02:39:24 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee290e0c3b16ce7f71bbee09586154f2f11fdf225d615356c7f82d01dcc1b7b`  
		Last Modified: Thu, 16 Nov 2023 02:40:03 GMT  
		Size: 43.4 MB (43387807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0327836e683c39f37a024679ce7b7038243224b79e21a4b7b89c9a0ca2dc43`  
		Last Modified: Thu, 16 Nov 2023 02:39:54 GMT  
		Size: 74.3 KB (74341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
