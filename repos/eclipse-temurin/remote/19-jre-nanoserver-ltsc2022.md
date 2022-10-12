## `eclipse-temurin:19-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:38152eb7920cd081ada58a656c05205daf422e9372fd9cbd053f420854f07eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:19-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:3c60a70aa960f917040c65f0b6d653e8f44d37c6e9ade1fe3792272495efee3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163458892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278abc3cb8ccdfa827954f1ebff7cbdc0b324cb4f842fd044d22a91970bdbd30`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 15:54:21 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:58:19 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 12 Oct 2022 15:58:20 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 12 Oct 2022 15:58:21 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:58:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:58:31 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:59:19 GMT
COPY dir:941cb8f5f97f3f5d2a48807df827e977e3ea22f3a1de758e43d87dd2ec67a41d in C:\openjdk-19 
# Wed, 12 Oct 2022 15:59:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:38fa349577729651ac1fc3ec785f908719a8100da5f5ba9bd3f549411061f583`  
		Size: 118.2 MB (118202895 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0ed0041e3584df1952980c3f73fd2b6e154328c7a0165f37dbe92ef94ae8a95`  
		Last Modified: Wed, 12 Oct 2022 16:12:53 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6600c5961e588d1043da5291c8ff4ae24eb763a46b37646c7eed3595563cb7`  
		Last Modified: Wed, 12 Oct 2022 16:15:13 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aea4aed78ddd1a041967cfed00e5d1b62a44f502cdefc523c6f065215e984df`  
		Last Modified: Wed, 12 Oct 2022 16:15:13 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c75b72fa9bce3569f8c2c8b26da3d331bebf435a9dea945d5bee6c78731c256`  
		Last Modified: Wed, 12 Oct 2022 16:15:13 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2381ef0d8a47f6f87b637d450f7053ce3f57cf77ae3109708410d404cce34c01`  
		Last Modified: Wed, 12 Oct 2022 16:15:10 GMT  
		Size: 85.1 KB (85058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291d1068cddc207235531c946aa2b96927e6fb63cd4f124d88e26ab4d83e0eb`  
		Last Modified: Wed, 12 Oct 2022 16:15:10 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538ecef9d63a923220b9c50f231d56588b2c0f7b90f5f0642348e2c72177667`  
		Last Modified: Wed, 12 Oct 2022 16:15:54 GMT  
		Size: 45.1 MB (45103420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9f4cbb135e54f437f2dbbd98e5caeb89a868e657f1d8ae65dc3d57ee74c68c`  
		Last Modified: Wed, 12 Oct 2022 16:15:45 GMT  
		Size: 61.8 KB (61805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
