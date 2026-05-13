## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ce597547395cbf2c3ca4747dc9a84fa730a3c46a938a7327f066a8a5ec3cf016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:c0fd1194ccc47b4de0926a6e284ecafdac02aa7023a30c8956a2ce0cf7d8a149
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167209134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65088753802241f9db89326ca7a901e87075d13802bb700453323c0f1f24f0c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:32 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:23:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Wed, 13 May 2026 00:23:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 May 2026 00:23:33 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:23:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:23:34 GMT
USER ContainerUser
# Wed, 13 May 2026 00:23:37 GMT
COPY dir:deea9cd49fa78c2b910137007aed467626dd46389507789da1635093de3df40f in C:\openjdk-8 
# Wed, 13 May 2026 00:23:40 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03cbcd303d3a3d248ab22d617e183ed76d01abedfee5c52cc9fb7f6a87170f0`  
		Last Modified: Wed, 13 May 2026 00:23:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4020417b724f038256992f00d0653eb817c5c2ff378c86fa3fe4be98f6f1fe91`  
		Last Modified: Wed, 13 May 2026 00:23:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c372e048e07ebfd58d41d756111d1aca474cd806c8c2c03b12d84fd752a3be`  
		Last Modified: Wed, 13 May 2026 00:23:45 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2afd2ac20279088abcaaa5fd1abc6ea2ccc40ad1b39a398ea3aa17b3ab09ff5`  
		Last Modified: Wed, 13 May 2026 00:23:44 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b02e47ca82f4366df01b94f395b1e69820f1237d0d044c7178eacf2cb94936`  
		Last Modified: Wed, 13 May 2026 00:23:44 GMT  
		Size: 76.7 KB (76688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e7e09994fa92b3e25c93f8e88e7168fbb9672755ea1ceb67cfb91bcfa5fc07`  
		Last Modified: Wed, 13 May 2026 00:23:44 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f9bab70c8817dfb95dc76e820df1c7e443299cef44facaec09dc95685cde65`  
		Last Modified: Wed, 13 May 2026 00:23:48 GMT  
		Size: 40.0 MB (39988105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfad307f0b72b79f8517124f044fe2492fb8e47eb6a0756ed4a0df015606dd7`  
		Last Modified: Wed, 13 May 2026 00:23:44 GMT  
		Size: 100.2 KB (100240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
