## `openjdk:28-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:edef1c2d087e01ecd448c5b385024ef61b5391f4d08005bae6476fdd74c6a283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:28-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

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
