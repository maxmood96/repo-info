## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:61bc2136015d6576f139b51ab66961b5327241fd6cb9b3597241348a72474410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull eclipse-temurin@sha256:e3268dc2ac51cf26be947edb54d22ba100408e1d9fa91109d8e3215d8688d0ca
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145886351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2bf700f210b2a123c3e27b34e230ce9ab4848410b9aadc1bf5217f0262afed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 12 Jan 2022 15:45:58 GMT
COPY dir:6031cfac1e4bd8de6c5533bea0aabc25715779d854db7f41b8aea3e1449ff0bf in C:\openjdk-11 
# Wed, 12 Jan 2022 15:46:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:ed9c850d0df5b835f82a653188a80bf74427a8e5a29bfaebbdb2776780c2a434`  
		Last Modified: Wed, 12 Jan 2022 16:14:14 GMT  
		Size: 42.7 MB (42728393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676987ef5191f314774b94c0b618bfcad3866e0889d0b85d9c2f2c9065a77834`  
		Last Modified: Wed, 12 Jan 2022 16:14:06 GMT  
		Size: 49.4 KB (49397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
