## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b0262e8ead486bd9e28d3414751c32c2e9a9f8404c16b408ed16d0de6ac2e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.825; amd64

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

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:2e24561ae6f748ace319a9d4a0ec9610527cf82ec0c997dee6e579d92f839c90
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292220996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa36e48ae8dddf4031672117faf6a4f748c54bc647a82501f6332172956d2b1a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Thu, 28 Jul 2022 16:31:34 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:31:35 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 28 Jul 2022 16:31:35 GMT
USER ContainerAdministrator
# Thu, 28 Jul 2022 16:31:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Jul 2022 16:31:46 GMT
USER ContainerUser
# Thu, 28 Jul 2022 16:31:59 GMT
COPY dir:be8ac85d984fd6d07ec942e6824366b313a501643dad7e29e6805d4aab47b44c in C:\openjdk-17 
# Thu, 28 Jul 2022 16:32:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 16:32:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2895487da2db86c62dbe5e78ed3eb9e82b82dcefd45f0920c1ebddce351b5e8d`  
		Last Modified: Thu, 28 Jul 2022 16:47:35 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb602783895d59eb3c367f6c49e797b6f531b4cc7bf2c8597a6302667302f3`  
		Last Modified: Thu, 28 Jul 2022 16:47:35 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0923366291c2355a7c25e03826245ce90a9c13dbc2c90c7b7502d2ca0707a1d`  
		Last Modified: Thu, 28 Jul 2022 16:47:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4f433194296f27434a06ca64d7359f939b637250531b3cbd3b12f33918b4c3`  
		Last Modified: Thu, 28 Jul 2022 16:47:33 GMT  
		Size: 73.4 KB (73365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601a9a7e1b55f3a24e32cb3e026b678483367ad999bb97c68db71f983aa96d69`  
		Last Modified: Thu, 28 Jul 2022 16:47:33 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9d5c531bf43951a01bc359455a13ab909c330822643e1440ed3c38a930a422`  
		Last Modified: Thu, 28 Jul 2022 16:47:53 GMT  
		Size: 185.3 MB (185342113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c752ea4024d0440e3b9983dbfef3dcce5c95e1e35efe798b766c88973cb2488e`  
		Last Modified: Thu, 28 Jul 2022 16:47:33 GMT  
		Size: 3.6 MB (3643617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c768edba6b966cb72b613845d96ab468d162a69269e7cf627c068367fc318b`  
		Last Modified: Thu, 28 Jul 2022 16:47:32 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
