## `eclipse-temurin:24-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fb894d76cd3719990b520992e2dba61711e5b3c5043c0a19a7d15c4bf6b70a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:73946402591f7372659275da35f99baf21d4d8efac121f97932fde24b6ec137f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178618869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70d9dd1adbd612368d5d9e7c1a7a7654ce531aed1b5540bbe33eac59eb7bfee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 02:50:07 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:50:08 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 02:50:09 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 02:50:10 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:50:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:50:13 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:50:18 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Wed, 09 Apr 2025 02:50:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7046fc683ccd86445d4e043fb4ba343a805bfe1823ff459eee09746fe3c9e2a`  
		Last Modified: Wed, 09 Apr 2025 02:50:29 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a260370f04911ce9c35f1b1ca7fb41baa2c643b3ad44e78274aa101611a023c1`  
		Last Modified: Wed, 09 Apr 2025 02:50:29 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b2233b7618cf177f59c57973fae207bceea0f8eb82e8394f1e334dad671e75`  
		Last Modified: Wed, 09 Apr 2025 02:50:29 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742d0bdbe1a4a8c752c8524f07863fc33060d036241fadf0772c6edcacd56885`  
		Last Modified: Wed, 09 Apr 2025 02:50:27 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa4956c880c914872efd0624ec34dfe1305bd9f0c605f1aa6af378f5834cd23`  
		Last Modified: Wed, 09 Apr 2025 02:50:27 GMT  
		Size: 77.4 KB (77442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa47692eafbd37a055808a85c4b596a1650da511678088aaa39f08d1f54d80d`  
		Last Modified: Wed, 09 Apr 2025 02:50:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff1f4361d839e73ada5ef21d2858191e25d9409e361b0248310a565f7a1477a`  
		Last Modified: Wed, 09 Apr 2025 02:50:35 GMT  
		Size: 57.7 MB (57701947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072045a721eee9e50ffbba4cc7448444e0b635345abd665f525ca185e1b782d`  
		Last Modified: Wed, 09 Apr 2025 02:50:27 GMT  
		Size: 98.0 KB (97965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
