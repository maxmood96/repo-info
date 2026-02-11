## `eclipse-temurin:11-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:fdb483042637656862683ba484df29aba79c7c905962ea35122a9ec54990dca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:137c0b63efc6f41bd219871cdf816ab2a602f5fc6ef72df1e13c40793b5ca0b9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.2 MB (394164552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ed3ffabb39c8f7af1764ed1e657b7ab7d1d7de9cf4d2693675489f23195f7f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:36:33 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:36:33 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 10 Feb 2026 23:36:34 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 10 Feb 2026 23:36:34 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:36:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:36:39 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:36:49 GMT
COPY dir:7dbbb550790b7446baaa5767cc14c2e1895a96b2462584273935c311b414f284 in C:\openjdk-11 
# Tue, 10 Feb 2026 23:36:54 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Feb 2026 23:36:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ee029b14f013ec4b8c026aa2261c04a1fbb3f25373d8d88ab30292a6f287c6`  
		Last Modified: Tue, 10 Feb 2026 23:37:01 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacd1011c944621c7da62041567d8b47f818f4bf0c4c069ed737bec40b130544`  
		Last Modified: Tue, 10 Feb 2026 23:37:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71d1ecd6a9a43b49e2eccbd086f7e86952ebc26f88bea35f97af3f29cfd632b`  
		Last Modified: Tue, 10 Feb 2026 23:37:01 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205d4b199b7f768e79127e29cd037aa76d22c820486b4ba9fbfe1084e2b47c6b`  
		Last Modified: Tue, 10 Feb 2026 23:37:01 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6982e32ab700cb309682a97913dfa22c9fd0b08b096f54d50ae58fe30e9ebf66`  
		Last Modified: Tue, 10 Feb 2026 23:36:59 GMT  
		Size: 71.7 KB (71696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ee59228d7e43578d00e005bbcadbbda531161ee3a21703908ed4b1c230875c`  
		Last Modified: Tue, 10 Feb 2026 23:36:59 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be951097588b219fdc027826be8fea5ba9f69c04d289c0167dc605c2bacf643c`  
		Last Modified: Tue, 10 Feb 2026 23:37:13 GMT  
		Size: 194.7 MB (194722414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2268f65233c35f0c242c2d14beef8373596f48f8256516904fa393154e2035b4`  
		Last Modified: Tue, 10 Feb 2026 23:36:59 GMT  
		Size: 112.4 KB (112436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8f918f78db2e227385bff437a54c85d4e8c124537c731a01b69f55bd3fb82f`  
		Last Modified: Tue, 10 Feb 2026 23:36:59 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
