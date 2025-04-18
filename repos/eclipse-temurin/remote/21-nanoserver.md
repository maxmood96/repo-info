## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:45b4453d575fa676d695f6b019eb924cff6cfb9afb8a327b32707671f96f7151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:7150b8a8ae812f87f552252172d51e7f251705b842001748b6e616c287967d8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.8 MB (391815475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d922d3422bc7f013c6abc72ee86e576da32a5e7332a3e987fff0680fc67f5d35`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:58 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:59 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 18 Apr 2025 04:15:00 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 18 Apr 2025 04:15:01 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:15:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:15:05 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:13 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Fri, 18 Apr 2025 04:15:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:15:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b47e80cf06020c6d9c791d19b288bb8dbcc74f3977e609bded147735b06acf`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d72b27313df724a3fd651182f8667cf7ceadc611ce44ccfe37c5084c78fa57e`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8f37013157d75d3577b4bbb5a6d4ff6ca2c05940d17dc13a7343af1cba9fce`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f83b8ab39e73000f236fc570dbaff46bc3de1bdebcec49a751e363d472b91b`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609b3260f014188310ac84c78b1f33bab58710fe28cb243435b9fcd3279cb06f`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 76.4 KB (76416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a6470c1ba45d72a13f28742d6c3a85c2c136b1361dedaa4d4290cfb5273a62`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87aefe6a9e8e06db0e3c3c37f1bdcb835990364170270d99ce44a652cda239ca`  
		Last Modified: Fri, 18 Apr 2025 04:15:35 GMT  
		Size: 201.5 MB (201475986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39922790ce4f9ea5740440487cf355b7ad1225f6e2abb93ef93a2c664313d4fe`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 114.6 KB (114617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d393b2b1ba2f0224012fe01c1281bba7e10633b0e36a9a80107ddeb8e957651a`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:c3b42259866c8c2fa321bb23b954433822f6a25bd4d803cb8770560f051f77f2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324206480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1cccaafad55d20b8d51d5524e229fa6abd0d29bf8904fc42d323b4694ecfb9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:18:26 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:18:27 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 18 Apr 2025 04:18:28 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 18 Apr 2025 04:18:29 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:18:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:18:32 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:18:40 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Fri, 18 Apr 2025 04:18:45 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:18:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f056659c7ba83e0261150d3b401324033b4d4182600dc7514018be52c80ed5`  
		Last Modified: Fri, 18 Apr 2025 04:18:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fb1d474365ca1fd790494efed929da78d3546c2238a359f80322fe3d204f36`  
		Last Modified: Fri, 18 Apr 2025 04:18:51 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436ef6621addb9d04e2ee6d8fc7052b2ab3777795171514abf5aca7729d74fae`  
		Last Modified: Fri, 18 Apr 2025 04:18:51 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ad100f505917ff762884972ac65a58fed8ba8e52c9ea7ebb972aef54ffa338`  
		Last Modified: Fri, 18 Apr 2025 04:18:51 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffef8d88bc09e650e1fc805e5a5766fbaa025c6f7ab9c601198b44536a756976`  
		Last Modified: Fri, 18 Apr 2025 04:18:49 GMT  
		Size: 78.2 KB (78188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137d464b6d2a96ecb9984eb7746b459af1d6f5ff011181fbfb51759fd0e19ffc`  
		Last Modified: Fri, 18 Apr 2025 04:18:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f39f2fc56dc3f11c96baf184f259589033498e987854490e6985bc67cd6a387`  
		Last Modified: Fri, 18 Apr 2025 04:19:01 GMT  
		Size: 201.5 MB (201475700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79150e33baf62d6866b2b97f5bd75f7a44219c92b9fafe4c2b4aa54c4a18917a`  
		Last Modified: Fri, 18 Apr 2025 04:18:49 GMT  
		Size: 107.3 KB (107300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1662a8bdc87c3d77ea09543aefcef36b8e05ca50ce8487ff29d7da5deac86f97`  
		Last Modified: Fri, 18 Apr 2025 04:18:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:e7fb8b7d59b195a464d2f7fe1342dcba855e52c61e114a462a53fc0183ca2f89
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314120051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d23f7d0b0413ac2faf833bf50d70da5d74c5a58bc03a8a5c9220698d03f1dd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:07 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:09 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 18 Apr 2025 04:17:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 18 Apr 2025 04:17:10 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:13 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:20 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Fri, 18 Apr 2025 04:17:25 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:17:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c13df5f4348ca3a97f85905cce89c2cc01f8e249e683767f0a95feb84fef947`  
		Last Modified: Fri, 18 Apr 2025 04:17:30 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8677f67bcc6dc549dc30112f5c61ffc01e3283d66bffcec4d5ba19c9b44d959c`  
		Last Modified: Fri, 18 Apr 2025 04:17:30 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af7ec33d1da800f1d643723547078f8d74a3fcbec8278764eb61c64aeb18e9c`  
		Last Modified: Fri, 18 Apr 2025 04:17:30 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0552b2903fcb5a73827248e9877e24d6be6a675bdd775938df044996ddfc8fe6`  
		Last Modified: Fri, 18 Apr 2025 04:17:29 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22caa57540576dcae253ea93595719606ec13953d79f6a79885ac0578fbe6e13`  
		Last Modified: Fri, 18 Apr 2025 04:17:29 GMT  
		Size: 69.3 KB (69306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478586a536f00e11f3c2aba47eab51a3db812108679fd6d9ecc30198483cbaae`  
		Last Modified: Fri, 18 Apr 2025 04:17:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ced69b6f125cc577e28b96f88b566da184e405e208458901cf179c7a0d9ad1`  
		Last Modified: Fri, 18 Apr 2025 04:17:40 GMT  
		Size: 201.5 MB (201475954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d52126d2b0f7ab2ebff4e192ccfb641d60e1e26030a2dc07c653ba00093bc9d`  
		Last Modified: Fri, 18 Apr 2025 04:17:29 GMT  
		Size: 3.8 MB (3816323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716ef4505b43a8bc5c4f79ce4a179e9e159f0a98b09ca8f56fad87efdebd900`  
		Last Modified: Fri, 18 Apr 2025 04:17:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
