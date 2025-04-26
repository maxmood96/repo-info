## `openjdk:25-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:b4742e2c19ee6a0e68728c6bc3a5acefb99587c353ed012997805c1058db27e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:b20ab4a597f7b08e791a6d7fa55ad618a28986f79528107566436987828b5609
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (398040733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99728cd51c65c618edef6e9f46192ea40a72f6bf46206035abba983c50147d2c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 25 Apr 2025 22:14:47 GMT
SHELL [cmd /s /c]
# Fri, 25 Apr 2025 22:14:48 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 22:14:49 GMT
USER ContainerAdministrator
# Fri, 25 Apr 2025 22:14:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 25 Apr 2025 22:14:54 GMT
USER ContainerUser
# Fri, 25 Apr 2025 22:14:56 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 22:15:04 GMT
COPY dir:68bac63248f06b5a3c6e48fd170d3fc54c730eec81f70554d15d79ed34fe2288 in C:\openjdk-25 
# Fri, 25 Apr 2025 22:15:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 25 Apr 2025 22:15:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409753cc488778a144ea889ab925b5f1dff516978e08fbe9c52d81982582d6d`  
		Last Modified: Fri, 25 Apr 2025 22:15:16 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0f99f9f47d40ea27110b026a8d73e0f1430f52d1d4434cb962039d03da16f9`  
		Last Modified: Fri, 25 Apr 2025 22:15:16 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead629dd28e5e2f8ddeaf6ae93b77d89b654633e389c29ce8b89bc7ab70a9b2f`  
		Last Modified: Fri, 25 Apr 2025 22:15:16 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9addc5c1eb495649cc807749c979bd6aaff2c92c06018bde9242cc11f9039`  
		Last Modified: Fri, 25 Apr 2025 22:15:16 GMT  
		Size: 76.5 KB (76458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cd81e099bdc16f2b5929df8cab02ce0e664658e3b8e7a64cd6aeb39e7c842e`  
		Last Modified: Fri, 25 Apr 2025 22:15:15 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f2aa70ed50683ef643947a4548209b9cee999c8dc764bd7c8a1561253bea8e`  
		Last Modified: Fri, 25 Apr 2025 22:15:15 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155e71e7f9e46ec99067356184c56b796230bc429a09d6a19fbf76c863f83d6d`  
		Last Modified: Fri, 25 Apr 2025 22:15:26 GMT  
		Size: 207.7 MB (207700888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4486d3da245c08502bb741757a4e7e1f7569f2336b933eec5e1bc726b7f072`  
		Last Modified: Fri, 25 Apr 2025 22:15:15 GMT  
		Size: 115.0 KB (115016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2854f7f82e74fb6da9c502068f8ed90419e2f48232870fa4f4c05b793ed449`  
		Last Modified: Fri, 25 Apr 2025 22:15:15 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
