## `eclipse-temurin:26-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a7eb70bb09a8b10d942c6424fea699ac65300cc70db68bc327dfc6e5f5f94a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:26-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

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
