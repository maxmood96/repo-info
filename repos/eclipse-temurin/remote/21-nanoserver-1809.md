## `eclipse-temurin:21-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:8965bb8c52cd5113b620dd0d8b5a8ed3e05a4ec85421f107b0dba381521d9b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:8721eb85d611934668ca5d59a3a403c482732f9866e78381669087c42785e562
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.6 MB (361576278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2153acceb8d0c781b754009a8475f537d3ffb7c8363856de2e02fa466f7b1945`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 24 Oct 2024 01:52:35 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:36 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 24 Oct 2024 01:52:36 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 24 Oct 2024 01:52:37 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:52:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:52:41 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:52:49 GMT
COPY dir:cc909cc6d9328a16dd1468618a073abc368d41e200a32534756819e3433a0b04 in C:\openjdk-21 
# Thu, 24 Oct 2024 01:52:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 24 Oct 2024 01:52:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2190a6629a3e57540bb9716a3018337c533e24db94b6cc7d1f5831eb00db25c0`  
		Last Modified: Thu, 24 Oct 2024 01:53:01 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37d2077d40c9705db8bfeedf2e86586dc69834ac2ed8babc6714a664d58957d`  
		Last Modified: Thu, 24 Oct 2024 01:53:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451f81f509d104b482dbd66c66b42d3d8bf327f318dc4b4a12fe2bfb29daea65`  
		Last Modified: Thu, 24 Oct 2024 01:53:00 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb3a909036c414db92ff367a3489707ba9901803984fd42e515cdf938b5867`  
		Last Modified: Thu, 24 Oct 2024 01:53:00 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5d70a4da69007ea8b4afcf9add0f69fa64353286100161e0357e75c5d7ba3b`  
		Last Modified: Thu, 24 Oct 2024 01:52:58 GMT  
		Size: 68.1 KB (68101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81c44045815e56fceffabc49a9e299c3f823b75fc9b4b473a48a9677de0b6d8`  
		Last Modified: Thu, 24 Oct 2024 01:52:58 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac0532a62cb0387265ed2562be0852d31ce7a8b792b4ef233b0698e7236785`  
		Last Modified: Thu, 24 Oct 2024 01:53:09 GMT  
		Size: 202.6 MB (202575987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d492242f06115e2ab98f88c362ed7239d573cfbcf7211c72589b26bd5aa684be`  
		Last Modified: Thu, 24 Oct 2024 01:52:59 GMT  
		Size: 3.8 MB (3832102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45964be9b4ff60145f0d03a9698f2727876fa3bf3c5df2547b9b993b08a5582d`  
		Last Modified: Thu, 24 Oct 2024 01:52:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
