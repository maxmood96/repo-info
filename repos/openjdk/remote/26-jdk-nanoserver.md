## `openjdk:26-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:2692062b557e78f86de1eea8d44b1e34fa21779eb86e4cc0c123c09e7a507cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-jdk-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:0b3e4e2e450859ef53b9c4a8cf898a80d13c847d5818a5963cca6003b74951be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410706389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2861bc6801a5bcbf364f65df1a640adf7017b88440a445e5fc5482d26a20490a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Mon, 30 Jun 2025 18:15:34 GMT
SHELL [cmd /s /c]
# Mon, 30 Jun 2025 18:15:35 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 30 Jun 2025 18:15:36 GMT
USER ContainerAdministrator
# Mon, 30 Jun 2025 18:15:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 30 Jun 2025 18:15:41 GMT
USER ContainerUser
# Mon, 30 Jun 2025 18:15:42 GMT
ENV JAVA_VERSION=26-ea+4
# Mon, 30 Jun 2025 18:15:50 GMT
COPY dir:9343c399342bfceaf41d41506cae5b04cc1bd9723c9bec54f094b2ab7e5f9176 in C:\openjdk-26 
# Mon, 30 Jun 2025 18:15:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Jun 2025 18:15:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fafcaf18cdaf69d3d8c820bd56c5a3d2c1d478ecc4b8bab53207a3fd48ffe5`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c23d1d89e4979f2e09e503f3765929b22fe03aa00e816ff7fec070228d08b8`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d8286f53a882d9bb52b1c7709e7b32149b7454ec23728884f9cde797fe39a`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec84a1c830bfccec928388db1bafa6cf3b5ee6a0ddb9bf6cf66a0b1e257848c9`  
		Last Modified: Mon, 30 Jun 2025 18:16:28 GMT  
		Size: 75.4 KB (75398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353873f9e92f12402a217afda63c1ad8bc4e0cd58b08273262d9b7cf327820c4`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2940a6cce1d4ac75088aa476005742ba1a48b71eaabc72a4656879d72582846d`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ddce15f3a3d8f23fb1e46569c2f2f8089b3fa01ec5d7167cf6e92c3144b0c1`  
		Last Modified: Mon, 30 Jun 2025 21:24:26 GMT  
		Size: 218.4 MB (218427850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42c71ed066dfe97158c83d30917e29416a15655a70afdb21b39a591f0fcd46d`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 114.3 KB (114297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108fea4f867f60c3289f7d2078aa07e82abd425b3f3d0463a74166245c3cd183`  
		Last Modified: Mon, 30 Jun 2025 18:16:29 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:af7b64a2e1f14616d65e12134bb7856bbea0e13edba373ecba92a9893d81e637
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341150212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e02fc59b2dc8856226d5509422ba95c9f4c0c3ed3fa8ab34881b729723f93e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Mon, 30 Jun 2025 17:37:24 GMT
SHELL [cmd /s /c]
# Mon, 30 Jun 2025 17:37:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 30 Jun 2025 17:37:26 GMT
USER ContainerAdministrator
# Mon, 30 Jun 2025 17:37:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 30 Jun 2025 17:37:45 GMT
USER ContainerUser
# Mon, 30 Jun 2025 17:37:48 GMT
ENV JAVA_VERSION=26-ea+4
# Mon, 30 Jun 2025 17:37:57 GMT
COPY dir:9343c399342bfceaf41d41506cae5b04cc1bd9723c9bec54f094b2ab7e5f9176 in C:\openjdk-26 
# Mon, 30 Jun 2025 17:38:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Jun 2025 17:38:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b84c257aad3c87c87574250644ebeb6a4e0dd68c54124231deef71e0ceca0c6`  
		Last Modified: Mon, 30 Jun 2025 17:39:27 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93336ba9c8e9d71ba4d99c242cd5fa3b995c09b1cb598e1ca82b380127c119bc`  
		Last Modified: Mon, 30 Jun 2025 17:39:27 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4b7ae9158a36d4f446e079649c94511da5156a873f2010c303f12d82cb0bed`  
		Last Modified: Mon, 30 Jun 2025 17:39:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e483d86111d08d9f7d4df89d0aa4361fa0857ef76aa62c13056f2e8d0d02f736`  
		Last Modified: Mon, 30 Jun 2025 17:39:27 GMT  
		Size: 71.7 KB (71740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20828b51dd7c784aec274a0221be986e022a3f7c9e8f34078ec8480bdb832a9`  
		Last Modified: Mon, 30 Jun 2025 17:39:27 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b4c677fc49e02cd9eb1f53cba5fedf3ccf3009d3ce049e716420cc763d4bcd`  
		Last Modified: Mon, 30 Jun 2025 17:39:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353a228a0326f042e0e59ea5c6add009c0cbceba96fd5c76f05eaa21642e5bdb`  
		Last Modified: Mon, 30 Jun 2025 18:26:14 GMT  
		Size: 218.4 MB (218422939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3070c8e6e0a2c36268c05079f2386f5bc16c5610ad9c4c9d3a7c6f1cc67973e`  
		Last Modified: Mon, 30 Jun 2025 17:39:28 GMT  
		Size: 108.8 KB (108819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15af065451e54f7db72641fd9ad2b7cee9c1cf84dc1ad48603a7d7bab7b2a62b`  
		Last Modified: Mon, 30 Jun 2025 17:39:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
