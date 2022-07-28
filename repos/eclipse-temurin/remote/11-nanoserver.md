## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:82730bdecb109083a7a73d7830d42dbbd7d9426516dd17af50097ed4a119a521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:7bea4329a1152ede3aebe910413c65faf418632f8ec099015356017c671ea1a9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310571121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edb3efb1f45f2b1fa1d1e15a08a63626670c760c979dd9c545e0941ff2e4a04`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Jul 2022 17:25:17 GMT
RUN Apply image 10.0.20348.825
# Wed, 13 Jul 2022 15:22:06 GMT
SHELL [cmd /s /c]
# Thu, 28 Jul 2022 16:37:40 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:37:41 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 28 Jul 2022 16:37:42 GMT
USER ContainerAdministrator
# Thu, 28 Jul 2022 16:38:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Jul 2022 16:38:03 GMT
USER ContainerUser
# Thu, 28 Jul 2022 16:38:18 GMT
COPY dir:311b50e59d3b0be0ca838f3cd712deaf9388198aeb821aea34d4de0537bd9b6e in C:\openjdk-11 
# Thu, 28 Jul 2022 16:38:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:38:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3719b23d309b17276277110a008a58133c9fc92465d2519f2f32c9961c39887d`  
		Size: 118.0 MB (118046090 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:569505cbc9e1bcad1fbbdd7edca170e5a914864bcad2f53e1fc5d5816ecc8aa5`  
		Last Modified: Wed, 20 Jul 2022 12:54:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1252b05e04415b932e0493ebb1c1d9630862699553a73c59de593de5037f231b`  
		Last Modified: Thu, 28 Jul 2022 16:49:16 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685c91e252aaa6220a6877517bdf3c005bd968d17423f3048bde56276159d52a`  
		Last Modified: Thu, 28 Jul 2022 16:49:15 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db05847b29dbb1bab6b2c49599195bffe75394e90dd8b8adf44ff003e6853d5b`  
		Last Modified: Thu, 28 Jul 2022 16:49:15 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ffb9642495dfdf16069f58704735111679b78d9810a36cd142d0b28cd02981`  
		Last Modified: Thu, 28 Jul 2022 16:49:13 GMT  
		Size: 84.6 KB (84552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8f95fa92d264d501d6e5872398e021530227e929f92756d32bab884109acf6`  
		Last Modified: Thu, 28 Jul 2022 16:49:13 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f3eb03f13e7c351814d3a9deca06f26fbbd63fa17ff438a140ad04264e0b09`  
		Last Modified: Thu, 28 Jul 2022 16:49:33 GMT  
		Size: 192.4 MB (192371694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fd33de494d620eddec65f3ab610307e67c6cab126096aa541b0170be5f35a6`  
		Last Modified: Thu, 28 Jul 2022 16:49:13 GMT  
		Size: 61.8 KB (61849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d6b2d65552c088380a74eded59f7d3a7169e1bd759b7c9991ceb720429927`  
		Last Modified: Thu, 28 Jul 2022 16:49:13 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:c3ab52dabd32b73cb4c1996ba170b8371a22cc355bf8eb81ae205a319c322dd2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295685152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eba534d1c2308ec60031a48514a45b2d71ca388a9734375d07e56932ae6a665`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Thu, 28 Jul 2022 16:21:12 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:13 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 28 Jul 2022 16:21:14 GMT
USER ContainerAdministrator
# Thu, 28 Jul 2022 16:21:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Jul 2022 16:21:30 GMT
USER ContainerUser
# Thu, 28 Jul 2022 16:21:45 GMT
COPY dir:311b50e59d3b0be0ca838f3cd712deaf9388198aeb821aea34d4de0537bd9b6e in C:\openjdk-11 
# Thu, 28 Jul 2022 16:22:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:22:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea12bb691aaa5d39e320d6c853d1f72c4f8a5cf6ea617ae2993a322713c92bcc`  
		Last Modified: Thu, 28 Jul 2022 16:44:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb07b488c8049fc65ecfb4ece07bd17ca87edc4bc3a924090d12c38a915a89c`  
		Last Modified: Thu, 28 Jul 2022 16:44:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4af14d5e4431703d40fe5c49f8ddd4cf832f851de381cfc75cd5e101f9d07f0`  
		Last Modified: Thu, 28 Jul 2022 16:44:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c60b48cbcf85422570b793d7032b6f380d04f09aea72ecaf4b378309ccff98e`  
		Last Modified: Thu, 28 Jul 2022 16:44:38 GMT  
		Size: 70.6 KB (70584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6b078b4a6303e9ef5314be0c4dac84047bc0b7226e9591025e14f1e56777b`  
		Last Modified: Thu, 28 Jul 2022 16:44:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74f82cbe26f37c6e0fd1db0bd405ed1cce701a5ba747b252cb8d61a085b6790`  
		Last Modified: Thu, 28 Jul 2022 16:44:57 GMT  
		Size: 192.4 MB (192370323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de33372ff17d6aced764fbc88654b2de0ab2ab91be9181d36c13a871f99fff81`  
		Last Modified: Thu, 28 Jul 2022 16:44:37 GMT  
		Size: 82.3 KB (82340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb658fa172b4ec8498e211f308ddbef34ce0767d0bbbeffa6d52dfeb3efaab0`  
		Last Modified: Thu, 28 Jul 2022 16:44:37 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
