## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:d424f4743b69b0b37da9824016776b3e8c987f91eb4192809d8f626286572f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:0cd54604a240799d6c8376ab7377ae95cb9b76900b4d362adfa8568404e73be2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321467568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea5d6730c7145f1cfb95216576963f4b76e51f42bcbe78a9f1d17188e47da57`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 19 Oct 2024 02:16:00 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:16:00 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Sat, 19 Oct 2024 02:16:01 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 19 Oct 2024 02:16:02 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:16:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:16:04 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:16:11 GMT
COPY dir:21acee06f7f20f6df9d2b0d45ba60360b710f331f6da7fc795fe21536879ea4b in C:\openjdk-21 
# Sat, 19 Oct 2024 02:16:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Oct 2024 02:16:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d205b4816bf52788196e48da4bf366b0433798a9b3fe51ab32fc2042151aaa8c`  
		Last Modified: Sat, 19 Oct 2024 02:16:21 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f7543bccecb04cf4b808e268c68cef3b54ade6772805955dfb2f39b6d7dcc6`  
		Last Modified: Sat, 19 Oct 2024 02:16:21 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b05789b59dcbb5d1affa62024cb32826ad4f48b965e08e8d5b585e1e64e7689`  
		Last Modified: Sat, 19 Oct 2024 02:16:21 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8a132e012f86c53524074d721829b2e5d87cd2f9c172d8507e5d5999dc123`  
		Last Modified: Sat, 19 Oct 2024 02:16:20 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8544a3c9df1dd5ea487aa7fb5a1e1bdbfc42acec175e92c72bcc2a9c60316`  
		Last Modified: Sat, 19 Oct 2024 02:16:19 GMT  
		Size: 78.3 KB (78339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacaa86c7d542e336fac665074154d78446b5c46153a76b53a7a740bd963dd4f`  
		Last Modified: Sat, 19 Oct 2024 02:16:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89172a6a5fd2d9670e645c65ecc66d92f8d10416d12330de463f9a740e81112`  
		Last Modified: Sat, 19 Oct 2024 02:16:30 GMT  
		Size: 200.8 MB (200753890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a52c6b98011fc1be00c9be38119f8416691a38d32386e5d6da3e2ebb95d3cf`  
		Last Modified: Sat, 19 Oct 2024 02:16:20 GMT  
		Size: 118.1 KB (118121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf82f6e9e3778596347ae1a4bd11bf47e779222812990020c5f45f1cb629b3`  
		Last Modified: Sat, 19 Oct 2024 02:16:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:2a2077e084243b104a6431cf7676e5e5763272007f3605e090012f90de96a70e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359775909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07c6498c2b308626cafe71f5a0b4c3ab8a6b6a57aaf09e7200e45d4645d44a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 19 Oct 2024 02:07:53 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:07:55 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Sat, 19 Oct 2024 02:07:56 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 19 Oct 2024 02:07:57 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:08:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:08:16 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:08:24 GMT
COPY dir:21acee06f7f20f6df9d2b0d45ba60360b710f331f6da7fc795fe21536879ea4b in C:\openjdk-21 
# Sat, 19 Oct 2024 02:08:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Oct 2024 02:08:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3c96c8c99661b7b781dc9ea8f232450962049c0731f5d58d3f0a7db31538b`  
		Last Modified: Sat, 19 Oct 2024 02:08:40 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab370e33e60801313403ae169448fc41ba398f3cded0926013d12a156592bb77`  
		Last Modified: Sat, 19 Oct 2024 02:08:39 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e33202abb54b59c5b446912c2beff6581d65500f4badbfe1abbda1bcaeb36e9`  
		Last Modified: Sat, 19 Oct 2024 02:08:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce531a773538cfe012c78db8c189dee2252eb9f46ba7809cd6cfa5b902e84528`  
		Last Modified: Sat, 19 Oct 2024 02:08:39 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd20cd5f10902fcc94f62816a87e22e224308ccbf7bdc6965f5914ac8e3a2434`  
		Last Modified: Sat, 19 Oct 2024 02:08:38 GMT  
		Size: 67.3 KB (67314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ea4fbb18ebb931aae9da92de511facd446def34a08afbe3d87247337064ee`  
		Last Modified: Sat, 19 Oct 2024 02:08:38 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e908754f696c39a4a1fa8f6bfb018e68e3871bdf49f0e59e6ec1475c04569562`  
		Last Modified: Sat, 19 Oct 2024 02:08:49 GMT  
		Size: 200.8 MB (200752060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe9b6d34ec960dd1b7a8a69d15478a27070947b3d0eed7661d216fafc118df0`  
		Last Modified: Sat, 19 Oct 2024 02:08:38 GMT  
		Size: 3.9 MB (3856768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfe32a4983b4eb4dded452ca3ad990ba6ac330be941ed94e2bad38aaa7148c3`  
		Last Modified: Sat, 19 Oct 2024 02:08:38 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
