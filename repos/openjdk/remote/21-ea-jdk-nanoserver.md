## `openjdk:21-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:f68aabd581023619378428bda1a4a034d839a041ab48d0873cbf210c5c2f7a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `openjdk:21-ea-jdk-nanoserver` - windows version 10.0.17763.4010; amd64

```console
$ docker pull openjdk@sha256:7e83606c49d253c9e729ee23936ed1816ebd2bae7ab7aa9a827558d17e04a583
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304756392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74fb555dfa8d14607c57392fc8d523105793d28fd1912c59f9193b8235ea872f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Wed, 15 Feb 2023 22:46:15 GMT
SHELL [cmd /s /c]
# Thu, 16 Feb 2023 02:20:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Feb 2023 02:20:17 GMT
USER ContainerAdministrator
# Thu, 16 Feb 2023 02:20:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Feb 2023 02:20:27 GMT
USER ContainerUser
# Sat, 18 Feb 2023 00:09:21 GMT
ENV JAVA_VERSION=21-ea+10
# Sat, 18 Feb 2023 00:09:43 GMT
COPY dir:94ce8f5ec957413da5d3698117f4a8ec518bb11298cd8980de0ef34fe7bcfaf6 in C:\openjdk-21 
# Sat, 18 Feb 2023 00:10:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 18 Feb 2023 00:10:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0185f49bd9e9c2d18b1dcf8f1f67123b4146383e07a158cb4623d96fb2d18c05`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b040b2f53926e6a02088ae0173e36f1f01b75c581f435607dd2f86dfe095f4a`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0134c2e5e080e208ed0917cd948446b60048729433bf731850e4165e426977c`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf352af9ffad203bc10ae043af50fee20ca5c0e02a370dcc2b040c702c9d48f`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 67.9 KB (67900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58adc24996cad294b1ceeed12449ee5750c4442dfcc5e3135984239942ba8503`  
		Last Modified: Thu, 16 Feb 2023 02:29:13 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1320ddf20fbcf695b97020d497e1890efc3ce72fe5303d174a2ab28e7f51f01d`  
		Last Modified: Sat, 18 Feb 2023 00:13:59 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63602c7fb78602ff2e7b9961bb8cbe44ab7b63da1f147f7e80cfff9af325eef8`  
		Last Modified: Sat, 18 Feb 2023 00:14:26 GMT  
		Size: 194.2 MB (194216320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff149f6c7cd8f4f6e3f9eb9b91ce2279d2c4e55207f572218f751d3eb21d11b`  
		Last Modified: Sat, 18 Feb 2023 00:14:01 GMT  
		Size: 3.8 MB (3790353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4541057b52dba25c5bedf5356b392422152f12d9955e382d4703685fa9b18264`  
		Last Modified: Sat, 18 Feb 2023 00:13:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
