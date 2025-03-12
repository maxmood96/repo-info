## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8f46ca1d769047870f640bad6e71c470427309c298a333df78a662a27cb6500e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:cf786852a4fb8a460bd464142e7ecca21573f39942880c1f7dd3bf28d5dec936
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (247028987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab785a5ba63fed0c978a5a7ef635eb02ecda87e097c4b17f16c6649e06b56685`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:00 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:02 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:17:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:17:04 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:09 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:12 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:17:16 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce2e201d1af7f5d86f70a6900c84ca210055bf152501e719e8eb24c2fd72074`  
		Last Modified: Wed, 12 Mar 2025 19:17:20 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd3b289e647fd123b2c4abe25c49d368fc0cc10331fe0f6285a41eb2469e597`  
		Last Modified: Wed, 12 Mar 2025 19:17:20 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731e3f3f1781cf224fe90dbbbd6b50224eba26e3d748c682ad976f4d3139a6ba`  
		Last Modified: Wed, 12 Mar 2025 19:17:20 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aaefc3ddcc9a41fda2ded2eda32d1dd78d5892b08223a91ba2dff9b1dee33a`  
		Last Modified: Wed, 12 Mar 2025 19:17:19 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2e7ff0fb1f1b72fb355ba5d05ae37bb462e3e0b29cbf9b649f96d9948510ba`  
		Last Modified: Wed, 12 Mar 2025 19:17:19 GMT  
		Size: 76.2 KB (76209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20963f84985eb7bcb59a93fd4dca9b6d94c26f0d820e6641ab526f61ed8229e`  
		Last Modified: Wed, 12 Mar 2025 19:17:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ab6269633770e7cabcdb5625a49d30fb222843c0966c6d2dd84c824e0b2af`  
		Last Modified: Wed, 12 Mar 2025 19:17:23 GMT  
		Size: 40.6 MB (40552456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7a12f7e402a747df77c1d028f09b45bd55b78344c36cc53ef7d1b231c4ea04`  
		Last Modified: Wed, 12 Mar 2025 19:17:19 GMT  
		Size: 92.8 KB (92761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:58c49e8b09b5d4c8b9f40b76317b4dd65a411ffe610878d9aa57470dd959d7d4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161436651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac63d75b3c9b496d2b96f334c8522f7342592db70101beca9cfd7e489c0d22d2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:26:23 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:26:24 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:26:25 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:26:25 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:26:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:26:28 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:26:32 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:26:36 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae632334bf112f435189793d6894283d928c18f1a290fc77842c2ed6d3048a2b`  
		Last Modified: Wed, 12 Mar 2025 19:26:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c906bcd06f0137cab4722e2d20cd2895877059bc83ee5065fc5a55c2a983e96c`  
		Last Modified: Wed, 12 Mar 2025 19:26:39 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6816c07da7288f774c3b8c6eef67da40a7c9ae3f484fb348eb3759f7d6c37d`  
		Last Modified: Wed, 12 Mar 2025 19:26:39 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914e31054b061396dc27c834532798a49a4f565b45c7e485731e67226c5e39b0`  
		Last Modified: Wed, 12 Mar 2025 19:26:38 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0cdc83d30946b1e7ae564d1da0ee66c5661239ea3992863ad2c9c17e5aeffd`  
		Last Modified: Wed, 12 Mar 2025 19:26:38 GMT  
		Size: 76.8 KB (76750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac1085568eeb3c4bfaa4053fce18def95d70ab6eda479c229d57b85d76b8f73`  
		Last Modified: Wed, 12 Mar 2025 19:26:38 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bc5c4ba731749d0a057a410a6e11aed288c80a3129b1a99e67c2e89e9b8d32`  
		Last Modified: Wed, 12 Mar 2025 19:26:42 GMT  
		Size: 40.6 MB (40552261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ace66d996afeb53b4f34816caf69302eeed7b1e70036e5d71a1055b6e9cd4c`  
		Last Modified: Wed, 12 Mar 2025 19:26:38 GMT  
		Size: 106.9 KB (106948 bytes)  
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
