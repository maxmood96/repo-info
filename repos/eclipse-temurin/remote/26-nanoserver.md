## `eclipse-temurin:26-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:88f7985d01a8c015480083ce782395d16b74423c6a2e11d701fe0b26200df680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:26-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:adec4ecfd718d53931f91d247ced26d0581cdf9879b832fe2ab737c70b259856
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 MB (338132185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12d314ed1e72f862f4b46cb70e9a352cb85753568f44a3c4cb443a3948812c9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:18:08 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:21:12 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 09 Jun 2026 23:21:12 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 09 Jun 2026 23:21:12 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:21:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:21:14 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:21:23 GMT
COPY dir:254440c2db85c674475ced33fb249e9ba634466f55592d23f645db2e3bf929d7 in C:\openjdk-26 
# Tue, 09 Jun 2026 23:21:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Jun 2026 23:21:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee5a15e6c0ae33d8458f16b5e982a3e6eb3be95d54d8918eb8862671f3dd652`  
		Last Modified: Tue, 09 Jun 2026 23:18:35 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f6c8d40bc1b4c99d683a5865f0ee3c615d346bd0a838e70f7d4ac40841f4f5`  
		Last Modified: Tue, 09 Jun 2026 23:21:33 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c112e459709bdd025a3635ccd4c19aae142eac7ca1ae8a43c4f19ac6946667`  
		Last Modified: Tue, 09 Jun 2026 23:21:33 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed99145c1df4aa2063eb9e14aa140ab10902d5d282441c1a8a466540f79a1fa2`  
		Last Modified: Tue, 09 Jun 2026 23:21:33 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb88dd0f011fbda065441ebe6e0f1d6f2fdbacde5eb9044240a685a574d61d2`  
		Last Modified: Tue, 09 Jun 2026 23:21:32 GMT  
		Size: 72.1 KB (72059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c5580b125d87fe585fd46e856e00235fa3b4c69ed81e2b7f163b563ae2db67`  
		Last Modified: Tue, 09 Jun 2026 23:21:31 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6f1dc4e881d14f0622d9f1c48f0910750154b44401259bc46656ab60663b41`  
		Last Modified: Tue, 09 Jun 2026 23:21:44 GMT  
		Size: 141.3 MB (141273196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cef1abb44e4defbd37373182f7d957d305c42c9cd536cc6e23910f301baa99c`  
		Last Modified: Tue, 09 Jun 2026 23:21:31 GMT  
		Size: 112.6 KB (112589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88924e1fd3183726b1d91d4149ec82b1ad58fa1fc09daa4bd4f14a41b813aea8`  
		Last Modified: Tue, 09 Jun 2026 23:21:31 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:26-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:a5f67589e7c78e72d0d2f755234060db39414a3c82096c1fcc31c994062586c1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265464066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c21e2d21bc37527d6f17348b7458edcd5366432fd4edc5c965eea38cc0c7a9b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:21:48 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:22:54 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 09 Jun 2026 23:22:55 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 09 Jun 2026 23:22:55 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:22:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:22:58 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:23:09 GMT
COPY dir:254440c2db85c674475ced33fb249e9ba634466f55592d23f645db2e3bf929d7 in C:\openjdk-26 
# Tue, 09 Jun 2026 23:23:14 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Jun 2026 23:23:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eebc83110026c1787f0a5411743bbd7e3cd34a1b101ec31d0e6f1d601324f59`  
		Last Modified: Tue, 09 Jun 2026 23:22:14 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c220602a8d4ce44bc412730f6a80c35820c5d429c1ce01e320a45dddcc71d5`  
		Last Modified: Tue, 09 Jun 2026 23:23:21 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ceede5da30922339b711c8a95203682c2c5f3e987b05fd24bd5f0a461bb33c`  
		Last Modified: Tue, 09 Jun 2026 23:23:21 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4464a6792108d696db3a8e66dba1a5ea0e67b900078c25e518b1bf1e56a098d2`  
		Last Modified: Tue, 09 Jun 2026 23:23:20 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1291e49f626dc0a3adf23b48d1baaa1bcbc3ff356cb94b8879150c386376035`  
		Last Modified: Tue, 09 Jun 2026 23:23:19 GMT  
		Size: 78.2 KB (78234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b3705cb091320b3e590cef6a8d92f0326fb2302212778636f28e221e7bc64b`  
		Last Modified: Tue, 09 Jun 2026 23:23:19 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720af1dd5e1defd9d4e419779a331866eccfd8d352e9f0ee06b2aa595aae0571`  
		Last Modified: Tue, 09 Jun 2026 23:23:30 GMT  
		Size: 141.3 MB (141273346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf36f1c6ce28be80caf834141e4c72f0c17155e4e65c933c927dd87f3c9f5e0`  
		Last Modified: Tue, 09 Jun 2026 23:23:19 GMT  
		Size: 108.6 KB (108629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19847369a543b7faed88675eddc3fe0ff52b89852f31c3af14ec317b09b746a`  
		Last Modified: Tue, 09 Jun 2026 23:23:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
