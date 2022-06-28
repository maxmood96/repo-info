## `openjdk:19-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:b92e6c49061f01d649c1e9c173fc7abef224a3eb15dc3dbc34419c4021094afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:19-jdk-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:a20cd6eca1e29eb713beec7823d26ec3a198f55af99bb71e8837d5b458b175ed
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298140289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2610f34d56514af7784f3a0381f8fbef19d215f3488104142bbe610243e9625d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 19:36:19 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 15 Jun 2022 19:36:20 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 19:36:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Jun 2022 19:36:31 GMT
USER ContainerUser
# Tue, 28 Jun 2022 00:22:09 GMT
ENV JAVA_VERSION=19-ea+28
# Tue, 28 Jun 2022 00:22:25 GMT
COPY dir:3766f791fd88d8608da5dc772c67a94e6f491dd7c8f269568cfa01c24a250cc8 in C:\openjdk-19 
# Tue, 28 Jun 2022 00:22:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 28 Jun 2022 00:22:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b58c89b4b822d0d5d5f1bc8225f7a37f7dc8a316f92594090c400a34a1a51ff`  
		Last Modified: Wed, 15 Jun 2022 20:10:09 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2fbbb0972907c5181cdfabed7833e7b033a86dcac9a55e84b1e6dc2861652`  
		Last Modified: Wed, 15 Jun 2022 20:10:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28327af37fa2c35b8687ad7e3ec93de3a24924e9504e2eaadb1ef6cd98728065`  
		Last Modified: Wed, 15 Jun 2022 20:10:09 GMT  
		Size: 68.9 KB (68857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266bdb7d76259c486b3300ec15922ed2162301ab3c50cfd1c9f8b1ed4ca95b1f`  
		Last Modified: Wed, 15 Jun 2022 20:10:06 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6fe5efc42d640ed1437774808681cdf49a32f4c50527ff8cb4e025b4a2cd1b`  
		Last Modified: Tue, 28 Jun 2022 02:33:28 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d09b7c625c68974f54104e4fd67f50bfb75bab37f9e71770bd875146e65d666`  
		Last Modified: Tue, 28 Jun 2022 02:36:56 GMT  
		Size: 191.2 MB (191175470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad816abf4723fd6ac585616aa6e8f686ee79044ec8464b9a91d21fae30199dc`  
		Last Modified: Tue, 28 Jun 2022 02:33:32 GMT  
		Size: 3.7 MB (3735688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d6e97ce10b2bf0e1b3f91eb3d9ee508c5070c6e4c80a4e4d4e2004fbb4cc0e`  
		Last Modified: Tue, 28 Jun 2022 02:33:28 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
