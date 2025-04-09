## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6cb8827e1c07448cac30098e260b4baca652b68ee093c7900ce9182fe4a85898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:b8b955c93ddccaa17bf55a2570b6ca502a5f9e45c04aa9faca5b9e2200e5f1b8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230839639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ba40aff19fa6452b5e8fe13016c290d4bf309495f9555e5065cfecefeb5b62`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:17:36 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:37 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:17:38 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:17:39 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:42 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:17:45 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:17:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d359084aa46c27da8504967579b6c10642ef236971754e03da5fb98f14265d`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e9bb659181740fce4f82e4bc60cd345de47de8967bd7204ee1719a6627565a`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac118af9931455b122b05c02e048e17c5f4fee342c9735d172e21c971cef1abe`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0787a7b73ed50be70ec8e8d3d0f387b11ce693f20a573689aa7cd062b4c9cb98`  
		Last Modified: Wed, 09 Apr 2025 01:17:53 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8872db4b3fb1b456db3f5d9401f41b189aae998c43c6f7c4bb222278e2fe87a`  
		Last Modified: Wed, 09 Apr 2025 01:17:53 GMT  
		Size: 76.1 KB (76092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c02796add8739739d9900f160ff233d3c8136f181d310e3b435a3b47318516`  
		Last Modified: Wed, 09 Apr 2025 01:17:52 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ac9154a569806eb7563faf95f76008dd6b5127ec9ad5f7c7a28a9afb618b26`  
		Last Modified: Wed, 09 Apr 2025 01:17:56 GMT  
		Size: 40.6 MB (40552519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47924eca07819d04efa9450504795e68b49324d416546b05dd3011c706296080`  
		Last Modified: Wed, 09 Apr 2025 01:17:53 GMT  
		Size: 92.6 KB (92612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:10e8989ea0c04030fa33368740d7d0df982d271cbfa902003601eb0637dc8b26
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161469517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd705e070a844d39bc95b23c2eac961ef715e6d947b5efc1bcacd5a4fce4d93`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:54:13 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:54:14 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:54:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:54:15 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:54:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:54:18 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:54:21 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:54:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cd5e09260c9524dadea97e28f87b14aa5d1b3a9ac02bf3e635fc2a23df7530`  
		Last Modified: Wed, 09 Apr 2025 01:54:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f08195c64d704602fd2c8bfdad632facbf35210b54c3ec5431220ed0ae73c`  
		Last Modified: Wed, 09 Apr 2025 01:54:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55da8f6efa226ebad73eb66aa55c8258c3b78656d0311cec416ab70de90e9f`  
		Last Modified: Wed, 09 Apr 2025 01:54:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9aa83f4f7622154c7573bd5f261d45f0b8622cef16eaad426ac90c70b40492`  
		Last Modified: Wed, 09 Apr 2025 01:54:27 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d579eea466efaab9fbde60edd8d7dbef8ebc8ddde7b36a01414bc69f541e50`  
		Last Modified: Wed, 09 Apr 2025 01:54:28 GMT  
		Size: 76.9 KB (76895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f902e5f73347c2f03e8c6cd73c3b3d9729b7ae93bdd59b65f3f049eea1702b`  
		Last Modified: Wed, 09 Apr 2025 01:54:27 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd6d803a131832e9d4b22065277aeb76c475b2bb3b5cf609050275c3ae9c44`  
		Last Modified: Wed, 09 Apr 2025 01:54:31 GMT  
		Size: 40.6 MB (40552174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1f51f449f8cdf70a9ae13d296330ed31151fa9f3af301e1c6920eec5229462`  
		Last Modified: Wed, 09 Apr 2025 01:54:27 GMT  
		Size: 99.0 KB (98992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:531030d58a11f6d6f2b316e1d96cd8fed8e94afc32952486f27a2e264a942544
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147650264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581c56bd093cdc6ad4c3a05dd669728585a728d4202f593497a2227e64ab98c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:14:04 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:14:05 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:14:06 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:14:06 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:14:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:14:09 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:14:12 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:14:15 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9948c6d4a8081bafb3e44259f9e3fce5ef86e361a0955afcfdfa0b7cdd6ccc`  
		Last Modified: Wed, 12 Mar 2025 19:14:21 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab9c6eb823887093207600e822b957d420615820f710822064d689464857ad`  
		Last Modified: Wed, 12 Mar 2025 19:14:21 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e89d9dc06cb725e9e0b07869ed1b5c7d68fdfdbd04b7fe446b6214193c7c303`  
		Last Modified: Wed, 12 Mar 2025 19:14:21 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4ae3decb161cf6ebd1c8316c43d9da1da905b300c3bf224c52ebbed32995e`  
		Last Modified: Wed, 12 Mar 2025 19:14:19 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bbaea4c6bfc079dd808efa140d8a0dceb309967016eeffd5135a12d5896272`  
		Last Modified: Wed, 12 Mar 2025 19:14:19 GMT  
		Size: 73.2 KB (73150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a009101e50ff6bfa5540b557b72aa4b9f7b8240ba6f324b337152f08e9a4af`  
		Last Modified: Wed, 12 Mar 2025 19:14:19 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3579eb782a10a212f5dd9f4a1baebf49fab2df96eabae9eb2345fec92763fb6`  
		Last Modified: Wed, 12 Mar 2025 19:14:23 GMT  
		Size: 40.6 MB (40552702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a27a4d65fc81d85d9efdc6fffcd1681c51fa922c690f22b09c6c4aceeb401`  
		Last Modified: Wed, 12 Mar 2025 19:14:19 GMT  
		Size: 111.2 KB (111181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
