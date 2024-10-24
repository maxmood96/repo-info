## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9ce5ffd422cae34d72ea9eaffb455b00605c5d75d22d706a591a9cdf4b25ad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:af6fcb322380fc8557dc8cd915ca97abe04b214b18147848ff29b82fcb7fef68
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323255097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bc099b2820ea3000d57f2119a016a048de3dcc447064ffb38ec8b48051e05d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:52:51 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:51 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 24 Oct 2024 01:52:52 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 24 Oct 2024 01:52:53 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:06 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:14 GMT
COPY dir:cc909cc6d9328a16dd1468618a073abc368d41e200a32534756819e3433a0b04 in C:\openjdk-21 
# Thu, 24 Oct 2024 01:53:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 24 Oct 2024 01:53:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab6983d85d5ea82e0f3f95a6fb89ec05dcea3e0480946795c60f76949024b9d`  
		Last Modified: Thu, 24 Oct 2024 01:53:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20830494b10e35d7612dcdd0657cf0b3cc03d5d57e256964268e2ba92f64fa67`  
		Last Modified: Thu, 24 Oct 2024 01:53:26 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1c79963351d8d886970a5c50bd7a19243fbe34198fdbb321751bf837473050`  
		Last Modified: Thu, 24 Oct 2024 01:53:26 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174534683c421f0dfbd426778dae85f094a9d20eff07f5c059fc3845a5aa72f8`  
		Last Modified: Thu, 24 Oct 2024 01:53:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f8c84a2ab49bec260ca6f0b60ef60f5113b61abddcecf55570db7c08beca40`  
		Last Modified: Thu, 24 Oct 2024 01:53:24 GMT  
		Size: 73.1 KB (73124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7fab5dee104872c358c88a56736cd301b03ff4241b2413ad8acc820faab63d`  
		Last Modified: Thu, 24 Oct 2024 01:53:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836530ca906d0804aefa42da4e3123e592b85eb0fb12a777dd5166469f0f0857`  
		Last Modified: Thu, 24 Oct 2024 01:53:35 GMT  
		Size: 202.6 MB (202576126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2438b34b7bff2a34faeed61604914e761824e255c9478849b7ced60f61779de1`  
		Last Modified: Thu, 24 Oct 2024 01:53:24 GMT  
		Size: 88.5 KB (88513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42179192d764910b44acf271742f54c8ad65a63e965b3c9df3ebb988b51d8d7b`  
		Last Modified: Thu, 24 Oct 2024 01:53:24 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.17763.6414; amd64

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
