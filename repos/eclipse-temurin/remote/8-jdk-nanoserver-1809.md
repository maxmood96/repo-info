## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:00c5111ba9e03f8fefe9aa8fbbba74ad0cc597583306545447860b31bdd62e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.3165; amd64

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
