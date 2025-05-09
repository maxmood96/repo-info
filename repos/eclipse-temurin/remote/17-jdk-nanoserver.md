## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e2cd486783533ad14ec7a6b425ab5446a4e6918ab8a1a0894d696037d32d78cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:8b9e4b81f2a596414214de82fcc07fd1af8ea9308ee8d5530ac2659a65c2d70c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.7 MB (377651034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6018d1b31c5f26bcdd7f1204e5af0bedc3dae7e4301826e342cb5081a292d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Wed, 23 Apr 2025 17:16:29 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:16:30 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 17:16:31 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 23 Apr 2025 17:16:33 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:16:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:16:37 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:16:44 GMT
COPY dir:642284f27aa03ba1e21a689edd99e2d493ba3e3290e848ff1bdf623fc783a5e1 in C:\openjdk-17 
# Wed, 23 Apr 2025 17:16:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 23 Apr 2025 17:16:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e492d2efb0ccf6d4bb5b95326e3438c42256766ad4ef7bd2c4c83349a16ce6`  
		Last Modified: Wed, 23 Apr 2025 17:16:56 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09db4e36827584552e2beae9691e8cfa45aee9300bf64944e84d9c8f6360a60a`  
		Last Modified: Wed, 23 Apr 2025 17:16:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff90573fb088cb7c7cccdec36676a073b776ed9485f5b7c2b53b5d1dc1c2bad`  
		Last Modified: Wed, 23 Apr 2025 17:16:56 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852deb019ed1ac5b15fe743a0acaeaaca7c4ce3e106fac9940821a21d8b7e2da`  
		Last Modified: Wed, 23 Apr 2025 17:16:56 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d712dcf32355b5074e96511dee93a54064ee966240ddbd82213321b86f274e`  
		Last Modified: Wed, 23 Apr 2025 17:16:55 GMT  
		Size: 76.6 KB (76564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62707bf14299873ece848adde37a7c2bcd68a38df9693e650b56c7aa94b27267`  
		Last Modified: Wed, 23 Apr 2025 17:16:55 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b797ad1510fcaf4d11b1fa1dbd10260a725cad4bea00f21ec42379f979faed47`  
		Last Modified: Wed, 23 Apr 2025 17:17:05 GMT  
		Size: 187.3 MB (187310890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5994212efa201d154de71324e03bcfe540be2a6cd1434a94d2dbc0ee1db488e6`  
		Last Modified: Wed, 23 Apr 2025 17:16:55 GMT  
		Size: 115.0 KB (115012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee6b89d5d126d87f72c9d1d1a2db7f24a1e1a36f9bfa243bc5e2460d67f4956`  
		Last Modified: Wed, 23 Apr 2025 17:16:55 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:15c541b91b249049df2179c267fd27e49369c5169dfdcf36dc6b9e9343faa3fe
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (310026471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f651dbc604d50268b39f203a21abe88fbceccaae477eb93d586effa13f1b609a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Wed, 23 Apr 2025 17:13:57 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:13:58 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 17:13:59 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 23 Apr 2025 17:14:00 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:14:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:14:07 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:14:14 GMT
COPY dir:642284f27aa03ba1e21a689edd99e2d493ba3e3290e848ff1bdf623fc783a5e1 in C:\openjdk-17 
# Wed, 23 Apr 2025 17:14:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 23 Apr 2025 17:14:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78ce9d306720ddd26a2b05036f059e1721b777b68208ecdb5aba3925a93956a`  
		Last Modified: Thu, 08 May 2025 23:37:36 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c813c96db31c71ccc051b8501e093bbbae9bfe3c6429ba7229e1e597b6e07a1`  
		Last Modified: Thu, 08 May 2025 23:37:36 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc970e146571387f437c074e8a9986c19a909ce7b87435cf0f3bb2bab9df6c7`  
		Last Modified: Thu, 08 May 2025 23:37:36 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a3f8ee7bec665b3cb98fcc14822e03d952ffa4a48a20c474666ab908c4ecc1`  
		Last Modified: Thu, 08 May 2025 23:37:37 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c905276405d0281414aa38d4aea04da0ba4a98014d1900b9fddfe34203a68c`  
		Last Modified: Thu, 08 May 2025 23:37:37 GMT  
		Size: 72.8 KB (72764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247bc36e8f84863f7e08fa114d31154215f83becbc0168f819e8a927762649c1`  
		Last Modified: Thu, 08 May 2025 23:37:37 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fa4e9ddd67fd5af83fa5be9db4639d5e06845b2c9945b762780a648f591bd2`  
		Last Modified: Thu, 08 May 2025 23:37:46 GMT  
		Size: 187.3 MB (187308640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f09f9aea927374c39a5682a5dc2d1153b068301fdb151ae42d2ef28a4f3c7a5`  
		Last Modified: Thu, 08 May 2025 23:37:37 GMT  
		Size: 99.8 KB (99806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2070e4ba58ce99d2682ed31137488be9d14cb6d8e331df7e1ba7bb6ee56a7d`  
		Last Modified: Thu, 08 May 2025 23:37:37 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
