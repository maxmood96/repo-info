## `eclipse-temurin:25-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8be457694eced903dc6c9f2694fd2335026cfcc264edb27352ce9af100ba7f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:25-jdk-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:ddc90e742829f6a09a27b7b3cbccda8f6264df95f477648759b451e92bc55240
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.2 MB (332183481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0defa6f3b069c9746efe29e5e0cc23355e4f2c04493e8278e8af36b3a63a05`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:19:14 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:19:14 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 19:19:15 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 08 Nov 2025 19:19:16 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:19:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:19:21 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:19:32 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Sat, 08 Nov 2025 19:19:37 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 08 Nov 2025 19:19:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3951beddd0c036c165f339869dab951299b53cf4f438eddd55b5e2b052fdbde4`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5d7f9a8b981ff980132e2156290054354c4d2a91a7d88c17e1592c4c4aa95`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4047690f7787dd3fc91c1981bc70dc2bb9c487ced3247436c157e9107353083a`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890835a7dccc965ed75636c925c94e7745ef856656e35f89e85fbf134f7a3560`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4f187879fa93e43326132627e37a7d95190d96ea74ad0461325e0c39e63956`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 69.3 KB (69319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fb06392818817993f818c9b988827d54081c9a15efb5c0d56d39683d4ae37c`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002006204fc4d4e28a75cc4b95e2486e57f3762739f55bc4f04ac0aa39832d51`  
		Last Modified: Sat, 08 Nov 2025 22:21:15 GMT  
		Size: 138.0 MB (137952154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe5d2f7a5dbfb35d47595d1cd2c7c9b0657e635308b39d5ea22bcf73684cdc6`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 126.1 KB (126123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8433ef188efc6f2c42d7ab1e6fee64d21bf2b3b21c462ee77725ff648861c1ae`  
		Last Modified: Sat, 08 Nov 2025 19:20:01 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25-jdk-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:1607c95e61f476cacf7c87b713278ddde62721abc4ae532018edf2b28c62f3b6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260819002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3d96c84b699fc117bb575c85aa74539fa31732faf6f84878a15294ba59eec9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 19:19:21 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:19:22 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 19:19:22 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 08 Nov 2025 19:19:23 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:19:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:19:28 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:19:54 GMT
COPY dir:889642903e29f32ff0f0b6da5f64cf6a40ecfa6d85d0926e4981ccbc885ac0c0 in C:\openjdk-25 
# Sat, 08 Nov 2025 19:19:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 08 Nov 2025 19:19:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8fcfa9b99eebc75a84c6511c7f2eafdc1efb8bf36c0e11e8f201e3c74228a1`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e2a586b5ce3ab60bceddb7feeb354bd72cc3d0f747557469877c8ceeef3930`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a51664d673a4eb59a615e60c29522d287380ac8d27b675d8e6bc83688b1032`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b610d8d00411bb798a1c16e348cc88ce1eab2db9ff09c1e523ec498c7cc766d`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2112b51a6ca48a93091da92b640b7ee5a1acad34173def1ee4192aa96971df4c`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 69.7 KB (69676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f3225cb271eed5a2e33d38d06ef9994f1e0a8cc69d385a129bd3f172e8c36`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52f8673f166de15864b6f76f8b7f5a30b58dfb28a8c7d11b1daa8419aec6e87`  
		Last Modified: Sat, 08 Nov 2025 22:21:07 GMT  
		Size: 138.0 MB (137951938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2246427734f43dd4b2d737117b2eea717b9a9c28a521a0c2dae8bc773983d6fc`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 106.9 KB (106949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d6880c1ac529c0da77ebd866071b114b8704bece571c74fddbf5a9c29f0262`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
