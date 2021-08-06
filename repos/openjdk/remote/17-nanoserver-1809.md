## `openjdk:17-nanoserver-1809`

```console
$ docker pull openjdk@sha256:d9b2f21333a5a8274441987fb93174b2363b34e7f34145c4bd1568483a55a388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:17-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:59b802a705bc3820b22a905cb934ccc204e8ce0f2ce2ddfe102dd0040be79979
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288514591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc9422775099ab98c8ff1bdfce84dcb3729f5e640422f7ee479f6bb8f1faa2f`
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
# Fri, 06 Aug 2021 22:19:48 GMT
ENV JAVA_VERSION=17
# Fri, 06 Aug 2021 22:20:09 GMT
COPY dir:16139fd5761a261a0505c9fb2561cbcbf9614d8d2403d5d2b56478bd7a396d2c in C:\openjdk-17 
# Fri, 06 Aug 2021 22:20:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 06 Aug 2021 22:20:41 GMT
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
	-	`sha256:abb7172621c3ac9ab0fd8fadc09ff7fcd7576960cf7123bf15f6afb2a079420b`  
		Last Modified: Fri, 06 Aug 2021 22:32:01 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1151c5b60ecd9fee650125fb8b6771d5cb474a71820451f4adcd16b358cc560b`  
		Last Modified: Fri, 06 Aug 2021 22:32:18 GMT  
		Size: 182.1 MB (182079127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe0b5ba5b0a52123dbc99bb2b49ea2832a7103c5034db6c5e13ab333d6cf4c6`  
		Last Modified: Fri, 06 Aug 2021 22:32:02 GMT  
		Size: 3.6 MB (3636108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c29b0125ac713a42d6a6d6f87b894ed9fe65015a0ed35a23b1e60677da292b1`  
		Last Modified: Fri, 06 Aug 2021 22:32:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
