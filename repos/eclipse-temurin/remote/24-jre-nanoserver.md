## `eclipse-temurin:24-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:045bb1163758579248056c626d9f97fca206cfc700cd8d37467c32d308d3092f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

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

### `eclipse-temurin:24-jre-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:18287b19009c453389840241bbe676a5c0a074c9a9933e37208f04b31a14d809
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168584110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e61d42e037db37dac87b24caf2d5dd5300d226841c9e3e74eb5bacfbab08b35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 25 Mar 2025 23:18:27 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:18:29 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:18:30 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:18:30 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:18:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:18:34 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:18:39 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:18:42 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42a0811c09bb7f0cc287a9b055a55a251e1639a924bcd1217ff35bcb1fa77a3`  
		Last Modified: Tue, 25 Mar 2025 23:18:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162977662480aec0e59d689b90cd91db862f5459e0e2fedab921c8e143c07040`  
		Last Modified: Tue, 25 Mar 2025 23:18:46 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30aefc727fb4e9f6733e0b4ed73dbbcef05d3edbcddd469f8dde64450c1f2c5c`  
		Last Modified: Tue, 25 Mar 2025 23:18:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc45bc7581625cb5c1227ed95e921ec5f8181e3ac6dc0eedff82aa06068014`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf563a55f51833614596eb35bfa0b6f0f6a8947d72ccc1fecd5c1cb11af1841`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 70.3 KB (70285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc65f99a24cf7764374e24ec5911536994f58f83c9f3922b741522a7d94b4a85`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b359a30bd1d01353d142067fb8e72dce94ac44cb58eb2e800d47417b117bf1`  
		Last Modified: Tue, 25 Mar 2025 23:18:52 GMT  
		Size: 57.7 MB (57700848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60ea89829296b5810e00af267a460d679d88530377780e1542a455eab8f9aaa`  
		Last Modified: Tue, 25 Mar 2025 23:18:45 GMT  
		Size: 3.9 MB (3899992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
