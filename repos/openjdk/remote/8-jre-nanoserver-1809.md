## `openjdk:8-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:ea8b6a0b3a48b2311233d7fb94bccf0384bfa66f3373ecd2f848e8f0f30bc977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:8-jre-nanoserver-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:547f132c494c796b653a1df754bbd43b77e14bf6312aed8a3a74e8aa5fef34d5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141618512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b61cc44c8d36e99ee64c29fe6c594d96d6c0ef44bb92078f67b93251bad9c2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 19:55:29 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jun 2022 19:55:30 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 19:55:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Jun 2022 19:55:40 GMT
USER ContainerUser
# Wed, 15 Jun 2022 19:55:41 GMT
ENV JAVA_VERSION=8u332
# Wed, 15 Jun 2022 19:58:49 GMT
COPY dir:a69662fb25cadf36484d90c7c9990719015f86fa8a02dabf235af3b8f20f255b in C:\openjdk-8 
# Wed, 15 Jun 2022 19:59:08 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cd545b01222a3eb04f8091b19b0f889a28bfdc13c5fb8f3ca93d64a4f12104`  
		Last Modified: Wed, 15 Jun 2022 20:26:22 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1c9f969ce25e06b9af4b5535d4cdde9a61e95b91f1b45f23098b7d5e5bb386`  
		Last Modified: Wed, 15 Jun 2022 20:26:22 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455853e8a7516ff71a0bea8cb1ba9e5714b59b6d457b79c3e573b7a97400b8d`  
		Last Modified: Wed, 15 Jun 2022 20:26:20 GMT  
		Size: 71.1 KB (71065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae1eb2b55617f949b8f06a2d7702328e41dbe0146194fd91ffb4ff676605547`  
		Last Modified: Wed, 15 Jun 2022 20:26:19 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3408c8159fcf4f878f0051f5f0c31117e509e5b7d13a1d1a27ae06b68a139a`  
		Last Modified: Wed, 15 Jun 2022 20:26:20 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b6651d9c8694935adf1d6c917d646dd5a0c2306231e0dcc77ce9cbdfcb4c1d`  
		Last Modified: Wed, 15 Jun 2022 20:29:16 GMT  
		Size: 38.3 MB (38288942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a6f02adb347a800d5adff849761a374b494c9336b06536212d45791d72ba17`  
		Last Modified: Wed, 15 Jun 2022 20:28:34 GMT  
		Size: 99.4 KB (99419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
