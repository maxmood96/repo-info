## `openjdk:19-ea-30-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:1991469585ec3baf79f018d42a6c389fe7cb9eeb59934a2615bf74861d3e7994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:19-ea-30-jdk-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:29292b162f0a83d713356292cdba8307327f0dfebbfe50194227d08ee5e9cafb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298130818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b2e3b28c6bc3e485b97f0576462c06a0e827e135659027806993a71e2f5357`
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
# Tue, 12 Jul 2022 01:22:23 GMT
ENV JAVA_VERSION=19-ea+30
# Tue, 12 Jul 2022 01:22:39 GMT
COPY dir:41fe7a1669df299f55773d5104c868166917acabbcf0f619552a43deab65a538 in C:\openjdk-19 
# Tue, 12 Jul 2022 01:22:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 12 Jul 2022 01:22:58 GMT
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
	-	`sha256:2bf56375e8908475f9ab59ecebd1d710ca45b63ab793d865ddde3250f98690ee`  
		Last Modified: Tue, 12 Jul 2022 03:23:47 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7624adf4668746c1d74a465f4db54ff7cd8b2d73161b7e08c0908a9781dac5d`  
		Last Modified: Tue, 12 Jul 2022 03:24:07 GMT  
		Size: 191.2 MB (191186891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aba509751a50ced7ebeedde5a591cea99832fc6ca4f626e3ae07000d893ae0`  
		Last Modified: Tue, 12 Jul 2022 03:23:47 GMT  
		Size: 3.7 MB (3714836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e429c9ebd30128a3d4f03c110ea33a2ea6a109871d20d3b1dc2d9d9216530dd0`  
		Last Modified: Tue, 12 Jul 2022 03:23:46 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
