## `eclipse-temurin:8-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:4e617d880b1d6529fbf27dc83c3faab1ed7ca8ffe777685b748669a69f9c3047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:d66b63281f10de7f5d650dc71efc3c2af7b36fa9df83d56e97359cb9e765ec04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292791854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a6d86dfa37817d0778d323ad4604b5e515c319d9eb7338f514826bc0bc9ab8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Mon, 28 Apr 2025 20:56:28 GMT
SHELL [cmd /s /c]
# Mon, 28 Apr 2025 20:56:29 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 28 Apr 2025 20:56:31 GMT
ENV JAVA_HOME=C:\openjdk-8
# Mon, 28 Apr 2025 20:56:32 GMT
USER ContainerAdministrator
# Mon, 28 Apr 2025 20:56:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Mon, 28 Apr 2025 20:56:37 GMT
USER ContainerUser
# Mon, 28 Apr 2025 20:56:43 GMT
COPY dir:5c4bbf817a67c787f7f2d8809dee99be16882c3512e063f4e47205ca5ccbd190 in C:\openjdk-8 
# Mon, 28 Apr 2025 20:56:51 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2331b51d4cf0bd4bcd777f499d0d3f3e26d70eb373da9eb1c785a7c2b16abe99`  
		Last Modified: Mon, 28 Apr 2025 20:56:56 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf9a66582bb8b87e162b6e3604c93ce035c331285502b84d2d3cbdfa6bc522`  
		Last Modified: Mon, 28 Apr 2025 20:56:56 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76c5623953aab73da6e8bbafc9a080b2142145fe053193f14c0d2efc0c27902`  
		Last Modified: Mon, 28 Apr 2025 20:56:56 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633251a6dbc2b31d93a4143ada1f6ddb637745d0765359f5f5e9a0da6e1b046b`  
		Last Modified: Mon, 28 Apr 2025 20:56:55 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2ea0a345065777e06434cd62dd31d80dcfa5e11a75e737c4385bfacbf153e`  
		Last Modified: Mon, 28 Apr 2025 20:56:55 GMT  
		Size: 77.3 KB (77258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2196e2dbf7924a8c9b53bcd29414ab50b5feb0c8a7335d8ce315e890eaf5b0c6`  
		Last Modified: Mon, 28 Apr 2025 20:56:55 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5ff764e448224ae172c593dc5abf3217834f29b03260e261934a4edf5fc820`  
		Last Modified: Mon, 28 Apr 2025 20:57:02 GMT  
		Size: 102.4 MB (102440598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a862e8e7a3ea8c6cbe3c35ca7b04336faf495ad5b64a38990852058e3140e726`  
		Last Modified: Mon, 28 Apr 2025 20:56:55 GMT  
		Size: 126.4 KB (126443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
