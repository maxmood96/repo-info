## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9ffff06a26b537c9ea6c21aef0f4f2d535d3d6f4780f8c09d25e77ee4d6cefb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:5374be1f7363b37fb35afd3b9e7f94fc8c603680b8cab2689c159224297905a7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218695020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba2879e24fa12149d244e88586658955f1306b5519770d469cb5196e6a6af5d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Jul 2022 17:25:17 GMT
RUN Apply image 10.0.20348.825
# Wed, 13 Jul 2022 15:22:06 GMT
SHELL [cmd /s /c]
# Tue, 02 Aug 2022 18:36:21 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Tue, 02 Aug 2022 18:36:22 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 02 Aug 2022 18:36:23 GMT
USER ContainerAdministrator
# Tue, 02 Aug 2022 18:36:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 02 Aug 2022 18:36:39 GMT
USER ContainerUser
# Tue, 02 Aug 2022 18:36:50 GMT
COPY dir:770d4c58725f903fa5cc3374e6a3f654e24baf27258320561cb0479514743464 in C:\openjdk-8 
# Tue, 02 Aug 2022 18:37:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3719b23d309b17276277110a008a58133c9fc92465d2519f2f32c9961c39887d`  
		Size: 118.0 MB (118046090 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:569505cbc9e1bcad1fbbdd7edca170e5a914864bcad2f53e1fc5d5816ecc8aa5`  
		Last Modified: Wed, 20 Jul 2022 12:54:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589515435cc74b16ecdcca85063c8c5a3e52b45ffebb06f73aacf7c70fc999e`  
		Last Modified: Tue, 02 Aug 2022 18:47:12 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098a92f594e84ecbbb8cd69a3dbfbabe32eac918acd2a16692ac4e13cab38b32`  
		Last Modified: Tue, 02 Aug 2022 18:47:11 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0cded47c0b33befaa67a297688be13eadaac8604b6562999d34f4bafc9eefd`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f52bbe4c2d6aa576880dfc7f24542be14e2379fa604502078a17de5c963ada`  
		Last Modified: Tue, 02 Aug 2022 18:47:10 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5ff650044ea148647cc2fc894105075f8dda748117560fb3bfd2457ff9663`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bee07b4ffeaf3e7993d85d4f5e28a1110a47a0f03e184abcb89fa83bce6d15`  
		Last Modified: Tue, 02 Aug 2022 18:47:21 GMT  
		Size: 100.5 MB (100475567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b3643c9d5b3c829d2e5f2f487e118c72aa592496f11dc25d32fb8f060c84f`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 68.7 KB (68725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:345d2b3e4abf72b6575eaf91aa0f5aeaeea2315b62da53b7d343955ea9ad9bd5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203800336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154534d54cca635a2d440e43931636b5c040f371cc79cc2b50b88e5991c7578f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Tue, 02 Aug 2022 18:20:58 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Tue, 02 Aug 2022 18:20:58 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 02 Aug 2022 18:20:59 GMT
USER ContainerAdministrator
# Tue, 02 Aug 2022 18:21:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 02 Aug 2022 18:21:11 GMT
USER ContainerUser
# Tue, 02 Aug 2022 18:21:22 GMT
COPY dir:770d4c58725f903fa5cc3374e6a3f654e24baf27258320561cb0479514743464 in C:\openjdk-8 
# Tue, 02 Aug 2022 18:21:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afb618c90b77419f2ba1f5cc9462e79727701df91db5fdad3b5471d61e915ab`  
		Last Modified: Tue, 02 Aug 2022 18:42:47 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b2c1dc8371357afa7f2bffb8953ce48eb6ce7fb4d9dff32cf29f491555f4c5`  
		Last Modified: Tue, 02 Aug 2022 18:42:47 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc03726463a40a0e346109623370ceedc85a9fdc7f3af42480b612bde6fdc87`  
		Last Modified: Tue, 02 Aug 2022 18:42:45 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8884b11b9d50972244fc935a95dfa3e795447d8ef888a4ab21bcefc91d35134`  
		Last Modified: Tue, 02 Aug 2022 18:42:45 GMT  
		Size: 68.1 KB (68138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1922d55220d13d511321a93f55ca92f4b464d239af9b51f68056e8b014474a16`  
		Last Modified: Tue, 02 Aug 2022 18:42:45 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d138b2f72292f139bd20992551a78e3f5d162e3ff97b6643930c20897479c5e0`  
		Last Modified: Tue, 02 Aug 2022 18:42:57 GMT  
		Size: 100.5 MB (100473842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf530b4f08dd5d2b6b12cfa45b344620978672ce7692cf97393037ffd244208f`  
		Last Modified: Tue, 02 Aug 2022 18:42:47 GMT  
		Size: 97.7 KB (97660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
