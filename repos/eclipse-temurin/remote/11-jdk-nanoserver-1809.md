## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:bbb2ffe2917c063949fcdda52beb821afb853f13a0e14a431676832c9d647b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:0e26019d47dc795ecf0c4b9a4047eb6037e334d7ac20ffa6be2de07e72627144
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298776861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373baf7fa11e51c2e3fe0c4ce4a6c6e0770001b210945f5eaaf17fdb8e30e590`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 00:41:38 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 00:52:28 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 13 Mar 2024 00:52:29 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Mar 2024 00:52:30 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 00:52:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 00:52:38 GMT
USER ContainerUser
# Wed, 13 Mar 2024 00:52:53 GMT
COPY dir:06bb700052ae5de12c7654c6d453b954bdaac52e59d87856592b85cdd3ce67e9 in C:\openjdk-11 
# Wed, 13 Mar 2024 00:53:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Mar 2024 00:53:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569a24b1d9b596a48436098ac5fe49c52e3153cd3bd147e365a80a4059570fd`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98a837dde21151ab3509cdfd80924b9e996169a8a5851cce1dc58e4989d462`  
		Last Modified: Wed, 13 Mar 2024 01:33:44 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58a9ec66ff17b3e6012f0432252313a936da84c374fe41322ef18de51dcda5`  
		Last Modified: Wed, 13 Mar 2024 01:33:44 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed3edccd5a17e03e7ea5e1dc3a1aadab2d89c7d3e49f548e4483e0e97c71d3c`  
		Last Modified: Wed, 13 Mar 2024 01:33:44 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6eb9505e98dc9a51920898f4f0cfb81accc9dfed9beedd771a55d28735daf9`  
		Last Modified: Wed, 13 Mar 2024 01:33:42 GMT  
		Size: 75.6 KB (75598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851f50bb9dfa9730a5189e62054b2103c052c0c5d52c5fddd41a94b66d7d36b`  
		Last Modified: Wed, 13 Mar 2024 01:33:42 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a7fe34cce1801665e158ac56587fa3fa2e907f6fb13ec61743b26f22e24718`  
		Last Modified: Wed, 13 Mar 2024 01:34:00 GMT  
		Size: 194.0 MB (193980897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a1d572813885311673e822398095b1cac5725aab2958e44afa47de00ad5ca7`  
		Last Modified: Wed, 13 Mar 2024 01:33:42 GMT  
		Size: 93.7 KB (93716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee5500bded28884bdbb95c0592279b9080b9e21b03d7ec97be6b36e59eadf9`  
		Last Modified: Wed, 13 Mar 2024 01:33:42 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
