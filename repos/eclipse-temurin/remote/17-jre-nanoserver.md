## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9ae1b77ae3c168d57a5927d8d09842b2645826100375d778b3b8c060d152f6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:ceb8eaea0a4428dd1f1397843a41e78dff99bfc45abfe0ac0911620a11ba718a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165148338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88387b39e5384c38898714e29f8ac4349f0e34dbd6ded26431e75b4f40c31cd3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:23:44 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:23:44 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 14 Nov 2024 21:23:45 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 14 Nov 2024 21:23:46 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:23:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:23:48 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:23:53 GMT
COPY dir:4c6d77ca6f58a330005c5f34389fe1882335ea3db28c021259e868cb18ddb756 in C:\openjdk-17 
# Thu, 14 Nov 2024 21:23:58 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0497842a20ee8180d6b14890933e227a9b3c359dd51e251d026498d5b3faedd`  
		Last Modified: Thu, 14 Nov 2024 21:24:03 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c61539307f308067e8887bc4d1500c9612b332a4d80f15d183d3f5dc3e6db1`  
		Last Modified: Thu, 14 Nov 2024 21:24:03 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc71dae54c793ef76d04aeb850a610c700d866eef446a6eb0d67ab9f238680c5`  
		Last Modified: Thu, 14 Nov 2024 21:24:03 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e5c8a50e92c9fe6161709fe429bdf8c2123ed4278bca339b29a0e01f855e49`  
		Last Modified: Thu, 14 Nov 2024 21:24:02 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b74c0f09c3d236eccbfe5faae4f5b5263b309c6e6ffb0fef56b1b4ba047dd0`  
		Last Modified: Thu, 14 Nov 2024 21:24:02 GMT  
		Size: 77.2 KB (77242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a7062f05c8bdbeb724bb771713e66b65a504c9470bd26efaa40741ab892fb`  
		Last Modified: Thu, 14 Nov 2024 21:24:02 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a6823ce116e60f123a8ba3d1e3b4f3dd7d7700a33c009a8790ca0bda0d966`  
		Last Modified: Thu, 14 Nov 2024 21:24:07 GMT  
		Size: 44.4 MB (44359945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3e02f52d0f59f34d123f16bd25d4ea7058e73142bf1de29549d390a234b168`  
		Last Modified: Thu, 14 Nov 2024 21:24:02 GMT  
		Size: 100.9 KB (100853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:f4e3e26b36cd55e6c005ceb64bc1a9d0adcbfcab89365a84abb9d628ed1c79aa
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202666464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20105cbdb627c01c444f922fcc621cdc67458922eafb9ed9b6e1754425120d6e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:16:07 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:16:08 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 14 Nov 2024 21:16:09 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 14 Nov 2024 21:16:09 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:16:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:16:13 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:16:16 GMT
COPY dir:4c6d77ca6f58a330005c5f34389fe1882335ea3db28c021259e868cb18ddb756 in C:\openjdk-17 
# Thu, 14 Nov 2024 21:16:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c412d22cf2c63983086eb172c4e120252e7dbfee3fec0075ded27d995170418`  
		Last Modified: Thu, 14 Nov 2024 21:16:27 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f826f446dd6945aa221ab3e7da12a9a8d45d5e15f725e9d0f2ce5cff5bc61a`  
		Last Modified: Thu, 14 Nov 2024 21:16:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b8d17a4f2ee97d1a6073c97c519a61c451592212974c2689df78e10803db71`  
		Last Modified: Thu, 14 Nov 2024 21:16:26 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f766ef12122de5feb187f00bb877f8f29534179abd42a6971d80bd78588cfaa`  
		Last Modified: Thu, 14 Nov 2024 21:16:24 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386cc7f2311fb7b197c78f12ed0b8e3f32e16ae9c7aae9a992e2c6243acba690`  
		Last Modified: Thu, 14 Nov 2024 21:16:24 GMT  
		Size: 84.4 KB (84443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b872d83fd799a9b29e7f06cda935b15ca8f2da8e1cf33650acb97da5d5444e`  
		Last Modified: Thu, 14 Nov 2024 21:16:24 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4ce1513876c811300cb7d1fbd3fc22be9ca9bf23d8282f6a5e38ae62acfe6d`  
		Last Modified: Thu, 14 Nov 2024 21:16:29 GMT  
		Size: 44.4 MB (44361008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cf79fb288fe2d98e5807519fb8179907786bbbc7eb34be201e57279d78034b`  
		Last Modified: Thu, 14 Nov 2024 21:16:25 GMT  
		Size: 3.0 MB (3001254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
