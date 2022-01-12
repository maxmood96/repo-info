## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4c04d6c8d86e7254f5f42d61f0d39db2544f51add920e279dc10754cd973e36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull eclipse-temurin@sha256:8a95e000d12f0ac1f02b11f30f6922aca5c6406627ac33cc6cc698a7153ea036
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295111504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732dd0be8e7f9d71d0e6457c4a01624b4536aaf482a94ec4e71b591032c2bcd9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 22:25:06 GMT
RUN Apply image 1809-amd64
# Wed, 12 Jan 2022 05:19:56 GMT
SHELL [cmd /s /c]
# Wed, 12 Jan 2022 15:41:41 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Wed, 12 Jan 2022 15:41:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Jan 2022 15:41:43 GMT
USER ContainerAdministrator
# Wed, 12 Jan 2022 15:41:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jan 2022 15:41:56 GMT
USER ContainerUser
# Wed, 12 Jan 2022 15:42:26 GMT
COPY dir:7549fd743977f7762910679960e9adfeab116385590a40bc0f1570100fce1af1 in C:\openjdk-11 
# Wed, 12 Jan 2022 15:42:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jan 2022 15:42:42 GMT
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
	-	`sha256:ae4ea70b005e41ddc4a95fc7fb15951e348a19152d6b73a3b12bfb999fc6a257`  
		Last Modified: Wed, 12 Jan 2022 16:13:15 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dca5a57808ce387df1ce94bb982a29da2a12df8e756f6c08841cd2c50514a5a`  
		Last Modified: Wed, 12 Jan 2022 16:13:15 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7a5ceb0434da477def40e4519d41218e841f10f8fd2590d8c3a67c9eb34e5a`  
		Last Modified: Wed, 12 Jan 2022 16:13:14 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8739b602e8fca551fcf4512abe5c66b4fe03a2086bf109b24193c8cd919169ff`  
		Last Modified: Wed, 12 Jan 2022 16:13:12 GMT  
		Size: 71.7 KB (71701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc86a69fcf0830120bf56c69b5a19bb167b7193783c3d071858b50aef785aec5`  
		Last Modified: Wed, 12 Jan 2022 16:13:12 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3d15b667502ab1849ea818f83f3178bd45d715cfbd787e79813079bedbf608`  
		Last Modified: Wed, 12 Jan 2022 16:13:31 GMT  
		Size: 191.9 MB (191943499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e610303cd010c1f3e52059bcbc86d016296a3b20bc7171572be04fc19c6bdd`  
		Last Modified: Wed, 12 Jan 2022 16:13:12 GMT  
		Size: 58.3 KB (58266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fef56b14c7ab5275c55c77a2f5e77c54c95d9e47ed04e50f836573b0b42def`  
		Last Modified: Wed, 12 Jan 2022 16:13:12 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
