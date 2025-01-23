## `eclipse-temurin:23-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ca747166774701272f7245f876788026b24814e5fc04d0ff51097fa9f8b97bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:23-jre-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:e974ab85a679121a9eb9c4712d7d9f0d7ccdde8e2b78140440fd9d152ee8a7cd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248839334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9122fc66e1b89a77587192b633c1af0e3c9844f6c1afe536a047fc2ea3339b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:25 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:26 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 19:34:26 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 22 Jan 2025 19:34:27 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:30 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:34:34 GMT
COPY dir:d9adc234ed2c06cd6b72c0beb8933c6d824941dbd1cece41e4fd2578b0632fbd in C:\openjdk-23 
# Wed, 22 Jan 2025 19:34:38 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691363b06a63dfdbb94538495c5dff1e2fef112f83b9280823fdac3abf083694`  
		Last Modified: Wed, 22 Jan 2025 19:34:41 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b085e7a6dd16cff73f3d727ab281ac125e6a10ebc724f3e883cd98239feb9145`  
		Last Modified: Wed, 22 Jan 2025 19:34:41 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839484f2f05ec41b836cede83edf1b1c4ffae39de4f1d7b3d5ffe19cf8f0148`  
		Last Modified: Wed, 22 Jan 2025 19:34:41 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8672a33634dc3f423627b217fc5bffacf501ae43944efb51fb2dfb36cf6a138`  
		Last Modified: Wed, 22 Jan 2025 19:34:40 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d7b2e908f22fd8a06119479da864d525b9850dc47016d2d3e7eeac33440d04`  
		Last Modified: Wed, 22 Jan 2025 19:34:40 GMT  
		Size: 76.2 KB (76182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63a82bcb424d37efdb8c5aae180101655c54da6ddeccebfaa7199d9dc442d30`  
		Last Modified: Wed, 22 Jan 2025 19:34:40 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fa3708cfbdd6be8f25b2d7c24d35f79f92c26dee92de8af3e5a9937be861f6`  
		Last Modified: Wed, 22 Jan 2025 19:34:46 GMT  
		Size: 49.6 MB (49611142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b14f12e27c4f9bf02bbfe82acd51f0360bdf3b1836a13d3982acc17e897ee5d`  
		Last Modified: Wed, 22 Jan 2025 19:34:40 GMT  
		Size: 92.3 KB (92252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
