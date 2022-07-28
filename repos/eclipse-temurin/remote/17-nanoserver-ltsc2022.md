## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ead11dc70582b8f736e262c9918f8699832557d8574c67fc5a6a1631db66177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:23afe5e243e868b6c6ec9f102b519950fe85fd5bef50d2d7feb0957e3358db2a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303539514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe939d186408632761a69bfae3d885825e3f803b9b420219b1779f53e782d43`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Jul 2022 17:25:17 GMT
RUN Apply image 10.0.20348.825
# Wed, 13 Jul 2022 15:22:06 GMT
SHELL [cmd /s /c]
# Thu, 28 Jul 2022 16:39:26 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:39:27 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 28 Jul 2022 16:39:28 GMT
USER ContainerAdministrator
# Thu, 28 Jul 2022 16:39:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Jul 2022 16:39:38 GMT
USER ContainerUser
# Thu, 28 Jul 2022 16:39:52 GMT
COPY dir:be8ac85d984fd6d07ec942e6824366b313a501643dad7e29e6805d4aab47b44c in C:\openjdk-17 
# Thu, 28 Jul 2022 16:40:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:40:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3719b23d309b17276277110a008a58133c9fc92465d2519f2f32c9961c39887d`  
		Size: 118.0 MB (118046090 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:569505cbc9e1bcad1fbbdd7edca170e5a914864bcad2f53e1fc5d5816ecc8aa5`  
		Last Modified: Wed, 20 Jul 2022 12:54:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab7ca482672c31ad41ca49077521306112cd79da1eff76d3af35188546cfb3c`  
		Last Modified: Thu, 28 Jul 2022 16:50:09 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6011b5ff8abfe38519ce8a359ee00893ef676de7b71efe7a58441a703b8d6c6e`  
		Last Modified: Thu, 28 Jul 2022 16:50:09 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc23f59b24abc2c5ef80b5785b63c9064f955766257caf8d9c80c4502ccd87`  
		Last Modified: Thu, 28 Jul 2022 16:50:09 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8792acac6dffa02bf3cc323d8cbfb3f66c0707eca875414f3013b00d7e0f44f3`  
		Last Modified: Thu, 28 Jul 2022 16:50:07 GMT  
		Size: 87.1 KB (87070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c369c947b981a1aa61f4b27ffa5562be1000f7cc7202af35e223339563abfdd3`  
		Last Modified: Thu, 28 Jul 2022 16:50:06 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545ab9c96082ecf25a45fb79fae0dafa5d9894bc70eccd228c7444d7f48ba66c`  
		Last Modified: Thu, 28 Jul 2022 16:50:25 GMT  
		Size: 185.3 MB (185342245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc59b3be52ca6e84cc863f3d5a548332fc31281cfbcacd941443af5aa574227`  
		Last Modified: Thu, 28 Jul 2022 16:50:07 GMT  
		Size: 57.2 KB (57151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2874b4ff58828d0007b7bfed2d81c2b2b71e27e9d54dd777f2f72d1c2f7d9856`  
		Last Modified: Thu, 28 Jul 2022 16:50:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
