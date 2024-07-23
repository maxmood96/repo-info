## `openjdk:23-ea-33-nanoserver`

```console
$ docker pull openjdk@sha256:1398db20832822d9dd1b828a6be0672427f15921c92f2ca9d59f4f397e0cae28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-ea-33-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:fbeea2e315eb822f3241c704b17745a960b7a9de56783e7373ad1d18aecca1c9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365284415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0d92931801826870602286eef76304bdabbb7b69882aea0ac61d0dd06f16f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Mon, 22 Jul 2024 22:09:31 GMT
SHELL [cmd /s /c]
# Mon, 22 Jul 2024 22:09:34 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 22 Jul 2024 22:09:35 GMT
USER ContainerAdministrator
# Mon, 22 Jul 2024 22:09:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Jul 2024 22:09:53 GMT
USER ContainerUser
# Mon, 22 Jul 2024 22:09:54 GMT
ENV JAVA_VERSION=23-ea+33
# Mon, 22 Jul 2024 22:10:03 GMT
COPY dir:11d94a9651e56b9be859aa9994f1c5c26c8bd38c50017badc2fde294e2cf8b08 in C:\openjdk-23 
# Mon, 22 Jul 2024 22:10:09 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Jul 2024 22:10:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f629f046746c3bce5a5b91a37ec61992072230a24440bdfec6be9d85be0b43e`  
		Last Modified: Mon, 22 Jul 2024 22:10:17 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad029c2733002223b458bd733b9598146cc466aba2eacc3ec663ba585769f95d`  
		Last Modified: Mon, 22 Jul 2024 22:10:16 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67a447a9b83b36f1c64663e25041eadf721e6281b00ba8decbc68c08052b0cd`  
		Last Modified: Mon, 22 Jul 2024 22:10:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5d54fd268fe96c45b33d51f625c491d8281466ffd895ca11827b9478491d09`  
		Last Modified: Mon, 22 Jul 2024 22:10:16 GMT  
		Size: 67.5 KB (67535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b7838f986c09936c94f51f95354890d161cf9b30b90225d0e411d2e4022ed0`  
		Last Modified: Mon, 22 Jul 2024 22:10:14 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f750cd66cea5dc04a26f65e8f9fdfd34c69c52bd85932a7ca56e632405188f`  
		Last Modified: Mon, 22 Jul 2024 22:10:14 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44897e6459bc74fba7083ec93eb090e63608512f54c77017685d89101d1349f0`  
		Last Modified: Mon, 22 Jul 2024 22:10:25 GMT  
		Size: 206.0 MB (206049170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e0f7d3e21a7aa7d77db2e43bc323c0892e3e0343869cc161e39e57e2e1cf8`  
		Last Modified: Mon, 22 Jul 2024 22:10:15 GMT  
		Size: 4.1 MB (4079736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5827bbd293630b0b7c8ca483cecce3a02f3e14eacf0e764a4b22a44bb79f3923`  
		Last Modified: Mon, 22 Jul 2024 22:10:14 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
