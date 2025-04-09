## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f79b4be851497532ede20824cb86d1cb1ffe750b9bbb51c9dd713db742bf551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:f8281afc2b8df82d7dc2bfb8550354b1374803572f2fd93f8ff84e19878a0f19
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150750512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6b7243fb1d07ccb4ddecd95b66aa6c2f4880c2fbeb3790125ae6603a2e92d1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:18:50 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:18:52 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 01:18:52 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 01:18:53 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:18:55 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:59 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Wed, 09 Apr 2025 01:19:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48285d8ae6d3f9bbbea337ab790eef98fbf84e1bcc7b37d00f156f10d56b6e8`  
		Last Modified: Wed, 09 Apr 2025 01:19:09 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354be8866d061f28d36f8d9be61020fa18db825b787a434e69becee9cb31e1ba`  
		Last Modified: Wed, 09 Apr 2025 01:19:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb226929039229dcea1ff249213910326bc95c4c238c4037abf858d3fab496`  
		Last Modified: Wed, 09 Apr 2025 01:19:09 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b175c2f43d785f4fcc0821cdbd37bdaff12fe0e731e1965708cff469d0ad08d5`  
		Last Modified: Wed, 09 Apr 2025 01:19:07 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9c70600754ee8358a4c26e9d148dd21f2c072a2ea3d7ccba62b72a6316a18f`  
		Last Modified: Wed, 09 Apr 2025 01:19:07 GMT  
		Size: 70.2 KB (70163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0642a4667b22186670fef37fbfe4ba9e3e411529bb2d57100128c78b03eeb23`  
		Last Modified: Wed, 09 Apr 2025 01:19:07 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbce22c8d51642006275130f4571af2fb2aba83cfe11d0f883de2fef3ac423db`  
		Last Modified: Wed, 09 Apr 2025 01:19:13 GMT  
		Size: 43.7 MB (43656154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0ec2661a3d3d980bcdac5c1f7f335f3906a270e96fb464665feb819bee235`  
		Last Modified: Wed, 09 Apr 2025 01:19:07 GMT  
		Size: 96.4 KB (96411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
