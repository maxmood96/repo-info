## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:da4b0d6bd7349c9314580b8a9488b42be55777026673e4dd015351d7fb803ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:dd8d715bf0fb47337e555e4eb8c8d5910762d93b131be1e1fcce628eaf52ec09
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222202173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7238cdbfb6996443995cf0e71fa7eb818e4885f8f58ca0b2d09501733901e7b0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 19 Oct 2024 02:07:53 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:07:53 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sat, 19 Oct 2024 02:07:54 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 19 Oct 2024 02:07:54 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:08:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:08:10 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:08:16 GMT
COPY dir:1819e9728b8ce1656dc0a20e5dd4c40c4149d50cae5eed15e03f81dabbaba653 in C:\openjdk-8 
# Sat, 19 Oct 2024 02:08:20 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3508672e006fde82e46b4462cd188ba5c16f2013b271397dbcc0221f9ddcefa6`  
		Last Modified: Sat, 19 Oct 2024 02:08:23 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07272c862057fd6cdb359a6beba8a0a591df15ba4fb7e98a2797a458fed94d36`  
		Last Modified: Sat, 19 Oct 2024 02:08:23 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968772eda9799c0da0dc1cf8f0c60237071f77c1d24bc754ef6e9f954edef043`  
		Last Modified: Sat, 19 Oct 2024 02:08:23 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6e00305ef7943e2d3e007497440d80be8bc65a687926a8034370a527dfc0f7`  
		Last Modified: Sat, 19 Oct 2024 02:08:22 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a8418b6b4dc1bd4ea908a96957e7c73efe4f8edcbc02f7e0d859d4f380df79`  
		Last Modified: Sat, 19 Oct 2024 02:08:23 GMT  
		Size: 74.6 KB (74558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327cfce559860f3ba151d5224adcc9638b8ccf7a897310c94659b5560e09527`  
		Last Modified: Sat, 19 Oct 2024 02:08:22 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d99fe74e7ea0943f49ce04845b6759b41d273dd1413e471bf7294c5014c27a7`  
		Last Modified: Sat, 19 Oct 2024 02:08:29 GMT  
		Size: 101.5 MB (101518864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb505cef711129b3d8feb4c47839eb8ec2dbe0392cdef7f0cd8ea2cc074655e`  
		Last Modified: Sat, 19 Oct 2024 02:08:22 GMT  
		Size: 92.6 KB (92597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
