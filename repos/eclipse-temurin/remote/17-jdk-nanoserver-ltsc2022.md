## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:46ab7ded0251d20606f3c4c92060bc6506b3722892125c4405698213af3eb5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:e7ff0d7086bd96ec4d5625a14b5ea1b628974c445062bd5d7dbeb4f9b1dc1d13
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310265389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3de39ebd37b9675de88cc195abbcf58fec55777ab7a5f3cdce25e922e684f8f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:19:28 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:28 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 10 Sep 2025 22:19:28 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Sep 2025 22:19:28 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:30 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:19:39 GMT
COPY dir:75620c5ae31b24727a476334c04df62052433150d79cd2f45de8191a02ae0b2f in C:\openjdk-17 
# Wed, 10 Sep 2025 22:19:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Sep 2025 22:19:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a17097280a912afb9e913f64e693d77bd1894f2056c1a8328975d3a62759b`  
		Last Modified: Wed, 10 Sep 2025 22:20:44 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccdbe87c7270edd50fd0f95c0645d3dd723596bdcda3592508f45a9df545b1c`  
		Last Modified: Wed, 10 Sep 2025 22:20:44 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf613abd7cff930bf6318ee0ce67986f399fd4a5dff7dca9bb76ad36f19e824`  
		Last Modified: Wed, 10 Sep 2025 22:20:44 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c302a5a47a2eacbd0ec02bf1fce80d7e7ee7d2d27fa3a5c705ec9b97a750418d`  
		Last Modified: Wed, 10 Sep 2025 22:20:44 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f094c46e388c7e4536eea73f6b7a24f62777b5d412942f6dd84e38e840ab729`  
		Last Modified: Wed, 10 Sep 2025 22:20:44 GMT  
		Size: 77.5 KB (77473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a00705d8c40716515bec2b251b7b85170f3739e627ec78c1044844d322bf639`  
		Last Modified: Wed, 10 Sep 2025 22:20:44 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9276a6be77a8da34c53cb42532c1e875a973e0e36900285c3a51a80b22e3af8`  
		Last Modified: Thu, 11 Sep 2025 00:14:48 GMT  
		Size: 187.4 MB (187353379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbac8afb4937240c05244c6bb1b94d8440f29faaf258b8c435301fe707773c54`  
		Last Modified: Wed, 10 Sep 2025 22:20:44 GMT  
		Size: 108.2 KB (108247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dd16c01d7f57baeb1631cb2d501516b634a2f607c00cb11441cfe5a6e25104`  
		Last Modified: Wed, 10 Sep 2025 22:20:44 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
