## `eclipse-temurin:8u372-b07-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:81227fbab89c88a7e11067f44b7c546bac1f9d6298ce7ca944d77d003f806f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:8u372-b07-jre-nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:1d1aae9742e8fff072fd84161263ed7ddb77bb151898329d4cff7f837756c543
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144537737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76085169d938af871ddd8401f894fe5ad0c944206ad2506d01e3ac827b235f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 21:36:33 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 13 Jul 2023 21:36:33 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 13 Jul 2023 21:36:34 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 21:36:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 21:36:44 GMT
USER ContainerUser
# Thu, 13 Jul 2023 21:41:10 GMT
COPY dir:8a6c7975745f12f5841a11f3a56ce128ecca26850fc38f023ad9679c09b008c3 in C:\openjdk-8 
# Thu, 13 Jul 2023 21:41:22 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b30eda955daff9169341fdb80582892899af8281f4a212720442538e2423fe7`  
		Last Modified: Thu, 13 Jul 2023 22:19:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81b7fe9ecdd110abd7fdedec4f78d1c2618bbd040bdaff607352462b87e69e2`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c488c573b312bf1ff8965a90b400d1c0e504c43a3ef81be737fc6a2b6a1685b8`  
		Last Modified: Thu, 13 Jul 2023 22:19:04 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce833e9d67aa99c3f24c4581dab3878c0005cfaca0340e8ac34e310ed4eedb4`  
		Last Modified: Thu, 13 Jul 2023 22:19:05 GMT  
		Size: 77.7 KB (77728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de2e484bb71b98cc30d2c993a6a3478b5686b6e41e6a711d21c54aac53170cf`  
		Last Modified: Thu, 13 Jul 2023 22:19:04 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141559ac6f1bdbf8391cefe42425abf40ef3b8455686a0bc707569194cfad974`  
		Last Modified: Thu, 13 Jul 2023 22:20:08 GMT  
		Size: 40.0 MB (39958474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ede0d7cf7aa8f091ab0e11e872ff37221185e5b73f24ed6cd69a5cd7503568`  
		Last Modified: Thu, 13 Jul 2023 22:20:02 GMT  
		Size: 88.0 KB (87969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
