## `eclipse-temurin:24-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0deda52b84b550eaac6db100489a920ab194d70f6a758ccd7a6734caf53c1af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:24-jre-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:5f06dafae2ccf2ab3129abf6914e1cdab4f57fcb6d100f81edc364f6357d56b6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (248003261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549b967169787b5ffbe80d7448f1086c802ee3acbbc814d492feed008e8c0ab0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 02:48:04 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:48:05 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 02:48:06 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 02:48:07 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:48:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:48:11 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:48:16 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Wed, 09 Apr 2025 02:48:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58e57df9cb0b3f9be5ca25da624c3bfbd98f77156d2e9d88c9f498753c406ec`  
		Last Modified: Wed, 09 Apr 2025 02:48:23 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cada0c0871286fc4dfadbb67a58dffa2960997f6f1027bd35915c72c80cefd`  
		Last Modified: Wed, 09 Apr 2025 02:48:23 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c28a41271797d54ab8b6f4f7b275e599ddc4d9a18c0bc8783bfaf43b8f0b781`  
		Last Modified: Wed, 09 Apr 2025 02:48:23 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ac4fba4dfedcb7094afa90dc3f499e04e9ce4f2dc8ed57c7678264c67f2dda`  
		Last Modified: Wed, 09 Apr 2025 02:48:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1c287073d6b3764d780015abb0100c9896dc62e8598d9e8ddd5006b0bd32c`  
		Last Modified: Wed, 09 Apr 2025 02:48:22 GMT  
		Size: 77.0 KB (76968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6bfb57f26db7d389e21b23cfe2db6766f3181270685b5c79c1943dfd4db86a`  
		Last Modified: Wed, 09 Apr 2025 02:48:22 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7ed762f03d913d914780c9474309af2681b1dea41e1b7366899f4fa8af2c4e`  
		Last Modified: Wed, 09 Apr 2025 02:48:29 GMT  
		Size: 57.7 MB (57702457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed98c4266dd8c12973d02ad3dbffff4332afe6ad611551f214e686ba6b2c5469`  
		Last Modified: Wed, 09 Apr 2025 02:48:22 GMT  
		Size: 105.3 KB (105349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jre-nanoserver` - windows version 10.0.20348.3453; amd64

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

### `eclipse-temurin:24-jre-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:a5e7154c2d9bf90be50d707d60b976e634f5811cb88bddc608d00255a5beceec
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168603554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30cd24cfbfec888640e6152106ca42953b29498a6b4c77cf9292d92b67dc350`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:20:41 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:20:44 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 01:20:45 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 01:20:45 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:20:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:20:49 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:20:55 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Wed, 09 Apr 2025 01:21:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcc6759b25e1ff0cb6cb4f455e94ecd27b2c8777349a97d384ceef85d3362cf`  
		Last Modified: Wed, 09 Apr 2025 01:21:06 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9b6e6f038ad2b7ee9870fda7633c9268a6022e6108093e8b7e6a5aa9946014`  
		Last Modified: Wed, 09 Apr 2025 01:21:06 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8a71b21b417161467f59de1278a51e6fb01e9cd2aa44b09fadcd2e130f441a`  
		Last Modified: Wed, 09 Apr 2025 01:21:06 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd80c339caa441f724ad6fc0408fa3275abb5cff18a6f765a08ab3f02642876`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf7324b467845202a6772835ad25f62a7c29932561abdb49fde4211d08c7e90`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 69.4 KB (69412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167003c646c376dd536f1a0210b6c431a6dd765e7ae3a21569ca1174e868ef8e`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e52164e67e137d88a1d63df22df6b0dc47f0fc5f33c252aa64443afa366b1b`  
		Last Modified: Wed, 09 Apr 2025 01:21:12 GMT  
		Size: 57.7 MB (57701210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d207b5570d306038823001e29275ec993d4f9efa056cd57411513539b6f43270`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 3.9 MB (3905050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
