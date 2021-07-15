## `openjdk:17-ea-30-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:4e63ab849817d92e5fdc68ecc50cf51685be241dcf1f0b773c4bf054422a64b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:17-ea-30-jdk-nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:f6dcccf85b5ba72617e83881cc09c4b4d2110eb498df5f6d2c039e4815108dd5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288549041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584539c1254027f1e1939f2eab2525c31f8c29f522daaf9b63b0fce458bf9e74`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 03:02:56 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Jul 2021 03:02:59 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 03:03:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 03:03:16 GMT
USER ContainerUser
# Wed, 14 Jul 2021 03:03:18 GMT
ENV JAVA_VERSION=17-ea+30
# Wed, 14 Jul 2021 03:03:35 GMT
COPY dir:2f32e93e5269ecf3899583f56f58411c06458255db4abcd1984333bf6e94ca7e in C:\openjdk-17 
# Wed, 14 Jul 2021 03:03:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Jul 2021 03:04:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d058f99ef2d3fe28236834e60b39712d663043177b35defac1c8acfafd3016d5`  
		Last Modified: Wed, 14 Jul 2021 03:47:37 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456549b72e3f1534b7acf6fa76038ed24ce3663d39883813dbe50372eb3986bb`  
		Last Modified: Wed, 14 Jul 2021 03:47:36 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3002766b2def22b4702b5aee99f9816819823d022a6adab4d7e1e1aab42f9a16`  
		Last Modified: Wed, 14 Jul 2021 03:47:36 GMT  
		Size: 66.8 KB (66818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3f23d871bb0957ed5203be3aa3cf5c809b42e159fb728ed9b411dc03f6af15`  
		Last Modified: Wed, 14 Jul 2021 03:47:34 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d55a01fdacd09f46f83d32a6dcfc8e9fdd380be8ddb8cbc5447eccbb406be8a`  
		Last Modified: Wed, 14 Jul 2021 03:47:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018044c68940fea928ad965ffd54677bea3488593b4d4b6e01f9e7edfbde4df8`  
		Last Modified: Wed, 14 Jul 2021 03:47:54 GMT  
		Size: 182.1 MB (182104670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d645e3eb99e77c391ac1db2b596bb3a0358b10207540b30864619a1d144a3d`  
		Last Modified: Wed, 14 Jul 2021 03:47:35 GMT  
		Size: 3.6 MB (3644949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7625957890bded33efe20cc33b40c24a338846ff9e8c1441d2e94d107e813ed8`  
		Last Modified: Wed, 14 Jul 2021 03:47:34 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
