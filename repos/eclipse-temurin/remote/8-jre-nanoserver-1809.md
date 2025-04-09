## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:40037b6fe25c991685dd6ccb01d0c459b768808b4f5297b6e913354171c375ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:61f3070fd56bf158b737040cdc588887e311c1492f75cb313b6a47db59164b49
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147662883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a35d7e6f7b995e8b70497ac262a43f82f0193ada04a9a7d343339476b012ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:19:08 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:19:10 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:19:10 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:19:11 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:19:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:19:15 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:19:18 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:19:21 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398d448212f0816fcb06e4f18911add90720bbfa83316a65ae552a1c7bea19c6`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef449908e6fa3eb93bb965edb2cf903652fc96c80640d3f48c1c07cd36a076e8`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d57bc13b8b6e124ea04d708e83c8e90c09f344102e1ba794132c70ab7a38d4`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e46ba24267c851d0963acb2a246a7af0c61bb3f2f662ce8feee801e17b0810`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582cd8187dba4c726e2e8958abfa89b6da0c0d8720fbe36e14c92a40443db7bc`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 72.1 KB (72086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d464f29d6ee8a7dd4851c4fb7ac1760c2239d61ef03e8f50f2c4c0166c3368`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff853a9fd09101ac5980002ca3a5a5f68c822b712c746b9ecfc9f5c910985be`  
		Last Modified: Wed, 09 Apr 2025 01:19:28 GMT  
		Size: 40.6 MB (40552552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fec1765babc25b84c4fa850af47854acbe52b3e9e954fe25ea3ef5f43e4296`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 110.5 KB (110452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
