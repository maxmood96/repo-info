## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:167d8c75e1aef6dcebd21c90ab5012c70fcdb9402fdec185190638defc72f10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:45f216aa7a551f8ee0693fc34bd7794473ee89533cf74f1131eeb61599611e19
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345233039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aece579d91320c5f30d3f5deb38b290a6f5826ebbd11a39a983403e62b9225c2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Wed, 09 Oct 2024 23:37:31 GMT
SHELL [cmd /s /c]
# Wed, 09 Oct 2024 23:52:38 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 09 Oct 2024 23:52:38 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Oct 2024 23:52:39 GMT
USER ContainerAdministrator
# Wed, 09 Oct 2024 23:52:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Oct 2024 23:52:49 GMT
USER ContainerUser
# Wed, 09 Oct 2024 23:53:01 GMT
COPY dir:11f935f87b5561ba9de5a02e585d9b073f4114e9ab1765209f28e6005e01c91d in C:\openjdk-17 
# Wed, 09 Oct 2024 23:53:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Oct 2024 23:53:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6adfd98d9a05d48859cfa5f6e1dc162be56797c9e86e7647518192a16af3d27`  
		Last Modified: Thu, 10 Oct 2024 00:20:41 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd5871594ea0edb1cbe05e7b9044e155182eaf5c9ff9fa5e5003755aaf045d3`  
		Last Modified: Thu, 10 Oct 2024 00:26:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b34251fd4c18da8ae9561441a25ac8a0daa460833af4ed83b4241ebcb6dab21`  
		Last Modified: Thu, 10 Oct 2024 00:26:35 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9aa5d601461ab6ddd6030a5b48aa92a7f868c149bae892010555b52b3faa863`  
		Last Modified: Thu, 10 Oct 2024 00:26:34 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce71e9d146261dcf74a7ede1fc033cc346be0af1c36fc62864c309bf46621b17`  
		Last Modified: Thu, 10 Oct 2024 00:26:32 GMT  
		Size: 68.2 KB (68222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d66c591d22da5ec7ed481cc918f39f364764653592e3d3dc7eaf3086bd2078f`  
		Last Modified: Thu, 10 Oct 2024 00:26:32 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28edfd82e8e4a6901bcb9cf3ed4e81263b384103d523f1f6f4229b43b3ec1169`  
		Last Modified: Thu, 10 Oct 2024 00:26:49 GMT  
		Size: 186.5 MB (186459346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90a712c32649f7b52c7ffcb592f75e46a00cf8f2641ab372b6e55c1d10811eb`  
		Last Modified: Thu, 10 Oct 2024 00:26:33 GMT  
		Size: 3.6 MB (3604991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01d9b7fbb2cd28af7fe3fafd9124d2fbb58c5a9f2bb6380ca1e6a808d6f75a6`  
		Last Modified: Thu, 10 Oct 2024 00:26:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
