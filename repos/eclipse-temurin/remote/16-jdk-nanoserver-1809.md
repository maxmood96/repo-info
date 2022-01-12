## `eclipse-temurin:16-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:820585f4258348a7533c1e82c623def555e69d4590a3f964b7192cc2318dc8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `eclipse-temurin:16-jdk-nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull eclipse-temurin@sha256:ca31c7afbbe2a1ba797d9f57d2cad8772e4dbbf3446a6787e358866c993baa0b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305559646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231f80580b25a45d4762bcdc7a55d70f38d1a0ad52e8331ea1612400324573b5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 05:19:56 GMT
SHELL [cmd /s /c]
# Wed, 12 Jan 2022 15:49:33 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Wed, 12 Jan 2022 15:49:34 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 12 Jan 2022 15:49:35 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 15:49:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jan 2022 15:49:45 GMT
USER ContainerUser
# Wed, 12 Jan 2022 15:50:18 GMT
COPY dir:9a7ef5975d9ba9576c4744dc049616bbcb218f14c3c0bd967851cd46479d6134 in C:\openjdk-16 
# Wed, 12 Jan 2022 15:50:31 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jan 2022 15:50:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a78847ea829208edc2d7b320b7e602b9d12e47689499d5180a9cc7790dec4d7`  
		Size: 103.0 MB (103031066 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:71dcb756adb8534a87210067788d6aa4a5a366b72d022b7af035e5263a3e54a0`  
		Last Modified: Wed, 12 Jan 2022 16:05:17 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1c51a7deefc19dbbc404b59fee99e247bd3c4ff9e94cd8150b3421feffedb5`  
		Last Modified: Wed, 12 Jan 2022 16:15:11 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b24d92c3163385b1826a1e016b65f6a3faf511842bf165ccee1030de1d082c3`  
		Last Modified: Wed, 12 Jan 2022 16:15:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abc4d4bb0c74be9e18729e504e778ad4bbc2cce0e694f00ee291b98d39f75af`  
		Last Modified: Wed, 12 Jan 2022 16:15:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1357415974ff8928dc5d3d515d6c2e2452218346f76a616b1b77641b843acede`  
		Last Modified: Wed, 12 Jan 2022 16:15:08 GMT  
		Size: 71.9 KB (71858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff511c7926df4b01ee2dcda47aac8272918868bfcddc5ffea6da4117e54270bf`  
		Last Modified: Wed, 12 Jan 2022 16:15:08 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5ef821c0f13f0441a4c4664815ef9ed916dfbb76400a5747d938e868eed43e`  
		Last Modified: Wed, 12 Jan 2022 16:18:41 GMT  
		Size: 198.8 MB (198765810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af489397513ece64c23243a476315ad4202c8ff806986f9306a45e68a700a1e7`  
		Last Modified: Wed, 12 Jan 2022 16:15:09 GMT  
		Size: 3.7 MB (3684047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342d97e2750995f1f603a695fed031e1276eabae155900c7c763b7542c887356`  
		Last Modified: Wed, 12 Jan 2022 16:15:08 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
