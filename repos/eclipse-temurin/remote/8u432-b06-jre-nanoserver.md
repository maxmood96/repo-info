## `eclipse-temurin:8u432-b06-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e7c669e90ff6263a77a377a3bf688b9af8c3b78c67fee8c1ea597b066813690d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:8u432-b06-jre-nanoserver` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:e10099610a103b2721942f6e967837c4f600a325b61b8aa0934d26f2e8827743
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161848805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c456c2206a3157967972bd2488e928e88e98d03f554d7a5b9c47860e657b4d6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:18:38 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:18:39 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 21:18:39 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 14 Nov 2024 21:18:40 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:18:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:18:43 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:18:45 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Thu, 14 Nov 2024 21:18:48 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f5c135be763e5ed04d4cd012b052a154fef9032ee0e338132c1b702287efcc`  
		Last Modified: Thu, 14 Nov 2024 21:18:54 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b38ba156726859099e63b3cd2abfdaa8128b2c6337c5cb1c315a22042db522`  
		Last Modified: Thu, 14 Nov 2024 21:18:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3e747f0b190de91f60614cdb2ad982f45ffd18ed104c05be85b124e2dede9b`  
		Last Modified: Thu, 14 Nov 2024 21:18:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d01d2a46372e643d92d1a62fb1efcdf8ae43cdf387f749dc1aefd2148e58b98`  
		Last Modified: Thu, 14 Nov 2024 21:18:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1148e5e149f399879f1cc996c5d0c0785583d4c2d7166129168abee497b73b5d`  
		Last Modified: Thu, 14 Nov 2024 21:18:52 GMT  
		Size: 76.7 KB (76661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d99f31f1f561edde797d6ffaae4f4de0bd2491e4370b616be54cecc4822812b`  
		Last Modified: Thu, 14 Nov 2024 21:18:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77322e160804f61856645a43718fdf1f2c5eaa9a239a7cd312bd143c274a54e7`  
		Last Modified: Thu, 14 Nov 2024 21:18:55 GMT  
		Size: 41.1 MB (41061137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb17ec6aa2b01b2e523b85baa4c176cf5119a159917e69b9cb7bf1dfaaf09d2`  
		Last Modified: Thu, 14 Nov 2024 21:18:52 GMT  
		Size: 100.9 KB (100904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u432-b06-jre-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:3f2d49cc433bfc45c3de80a3f8b30c922184b930273e427b99e94997f380d5e0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196475261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9c3d4378e95a18cd4c7592f582a344cb9ffd313fc95015a29b5dae75fcb056`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:17:49 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:17:50 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 21:17:51 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 14 Nov 2024 21:17:51 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:17:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:17:54 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:17:57 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Thu, 14 Nov 2024 21:18:00 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e884f914e6a1dac4bcdeb6517ff1a7c8e46ee86ac10c5c8391a9e78a8cf17a15`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5c1abd153b18fd459debdc48a3cad23d5be49d1e20319a6f22d6afa401c40a`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c45070a577c61fbdd171b8e6fd28210128eb6026d1cc4fc5b22338440a5ffa`  
		Last Modified: Thu, 14 Nov 2024 21:18:05 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d82da8a53ff1f9c8a41c5a7b5da5c5e096293b54efe31446f9761f2ebe31b3`  
		Last Modified: Thu, 14 Nov 2024 21:18:03 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01109611fec62f04c008426298eff9fb8e06091021e1ea3ed151e414e1a0ddf3`  
		Last Modified: Thu, 14 Nov 2024 21:18:04 GMT  
		Size: 84.2 KB (84238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fc0e0d2708dd0d6af3ec7bd641acba3a2166e44d08226e5732e8ba9c711500`  
		Last Modified: Thu, 14 Nov 2024 21:18:03 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f13593041c29509f2a62d2acf273486c715b28e19a760c0f182251d6623af`  
		Last Modified: Thu, 14 Nov 2024 21:18:07 GMT  
		Size: 41.1 MB (41061240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c3ccf40945c0866eb9f2cbcd45ff5e750463686812187a115e95986fc0024a`  
		Last Modified: Thu, 14 Nov 2024 21:18:04 GMT  
		Size: 110.4 KB (110386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
