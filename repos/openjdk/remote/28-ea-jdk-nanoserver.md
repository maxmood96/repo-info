## `openjdk:28-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:4d19240aa297e53091b22cb7de14fb172d81b0892c7be817cf9c8b279c9c1323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-jdk-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:8731f50cdf6a48f57045a1f196d37d940e023f9480868632d7c1bade691bed11
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.4 MB (420388739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fd98774d6a61a93984b9065ccf6c0d279c9358845510bc17b0d40e4ce6b746`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Wed, 17 Jun 2026 00:09:12 GMT
SHELL [cmd /s /c]
# Wed, 17 Jun 2026 00:09:13 GMT
ENV JAVA_HOME=C:\openjdk-28
# Wed, 17 Jun 2026 00:09:13 GMT
USER ContainerAdministrator
# Wed, 17 Jun 2026 00:09:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 17 Jun 2026 00:09:27 GMT
USER ContainerUser
# Wed, 17 Jun 2026 00:09:27 GMT
ENV JAVA_VERSION=28-ea+2
# Wed, 17 Jun 2026 00:10:39 GMT
COPY dir:7a688c2845332d8c78625013fb7ea6948a575814777db81fbce8268792efb42f in C:\openjdk-28 
# Wed, 17 Jun 2026 00:10:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 17 Jun 2026 00:10:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7d6978bd46ae56ac57f6491b5ed1f5845547872fa521657a482b4c0a5cc827`  
		Last Modified: Wed, 17 Jun 2026 00:10:56 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e05d1aa1daa761aa54240ffd6f04aea71110533d8c259fcc3600bd51114b23d`  
		Last Modified: Wed, 17 Jun 2026 00:10:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849fad7e56eca49b7f4ee07cc8cfed0568dc7809207143a89f0b0675fc29e0c`  
		Last Modified: Wed, 17 Jun 2026 00:10:56 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a18edefbf43699e3a354e9e54bbf5b92f912e20909dc94beb691f7e9a8688a1`  
		Last Modified: Wed, 17 Jun 2026 00:10:56 GMT  
		Size: 76.9 KB (76869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bfedf8240fd7a67f616c57af5e11d2a5dd43592f2a323e91953e586aca73c0`  
		Last Modified: Wed, 17 Jun 2026 00:10:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0952289155ef8081afb66cd26841900b7a44af147a258990d8ec6fa3193f89c2`  
		Last Modified: Wed, 17 Jun 2026 00:10:54 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bec86125ad5e793bbe78bdb23a53bb13c87aa784927e8aa068202c9c08757d0`  
		Last Modified: Wed, 17 Jun 2026 00:11:10 GMT  
		Size: 223.5 MB (223539992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c59cf6273d3c85d434eed3d3dc7507d229f8327617ce5755c8e7b61d375137`  
		Last Modified: Wed, 17 Jun 2026 00:10:54 GMT  
		Size: 97.6 KB (97562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bdf1cfa17d93bfef665608742b72eb674fdbc1a3d31367d0ad7d3902e20dc`  
		Last Modified: Wed, 17 Jun 2026 00:10:54 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:28-ea-jdk-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:ddb764e335bbf9a77a53ada5bb492d57d80b5a9916279bcbe632c858b0216f8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347712195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56d373f3117cc7f85b78d8e3000c9bf4cbb12da498162a0f6845ad12ba2663d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Wed, 17 Jun 2026 00:09:00 GMT
SHELL [cmd /s /c]
# Wed, 17 Jun 2026 00:09:01 GMT
ENV JAVA_HOME=C:\openjdk-28
# Wed, 17 Jun 2026 00:09:01 GMT
USER ContainerAdministrator
# Wed, 17 Jun 2026 00:09:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 17 Jun 2026 00:09:08 GMT
USER ContainerUser
# Wed, 17 Jun 2026 00:09:08 GMT
ENV JAVA_VERSION=28-ea+2
# Wed, 17 Jun 2026 00:10:16 GMT
COPY dir:7a688c2845332d8c78625013fb7ea6948a575814777db81fbce8268792efb42f in C:\openjdk-28 
# Wed, 17 Jun 2026 00:10:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 17 Jun 2026 00:10:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de52ab6f0e221eac4e1abafbec1f68338a9808610258ab1e6e431e69fafa10c`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302dadb9e7ef94ce348919c42c603fda54b2e80c3c10f7d0e9bd14107ce6d4c0`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60c92665861d170653a4e8ec25482a238176fafef13374ee27ff7d5dbf75fc`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb20b392a3fd0cdbb215bd54c8dd7da0ab9336f18016a7a8dd7709c6798916c`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 71.1 KB (71107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6ffb76840896de26bff9bba9647aac85530b9b1d3601fb23bb811d1adae3f6`  
		Last Modified: Wed, 17 Jun 2026 00:10:34 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95e685be809a94b88666879b9bd908610eeb70597c3812acfbd8e7f53cb9a91`  
		Last Modified: Wed, 17 Jun 2026 00:10:34 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c886ce20a58ca115b9acad0732f3dd049f19616ca34fe581f38ce82209aa6d`  
		Last Modified: Wed, 17 Jun 2026 00:10:50 GMT  
		Size: 223.5 MB (223540094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bab90ba1d53ebb57d0e7b1f78f920ca1427ddd06452ca834755ee4e87c0bf4`  
		Last Modified: Wed, 17 Jun 2026 00:10:34 GMT  
		Size: 97.1 KB (97089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3897877382c39c0cdb39af8846ffbdb41caaf925d30fd87a4c949cbba6818b24`  
		Last Modified: Wed, 17 Jun 2026 00:10:34 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
