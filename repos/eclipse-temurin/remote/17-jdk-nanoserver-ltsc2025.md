## `eclipse-temurin:17-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:4c47bd1530534e1b186cdcd27c5a58405fcc1ed5990d3f1f9290a5d6f6e7216d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

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
		Last Modified: Fri, 09 May 2025 07:42:27 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09db4e36827584552e2beae9691e8cfa45aee9300bf64944e84d9c8f6360a60a`  
		Last Modified: Fri, 09 May 2025 07:42:27 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff90573fb088cb7c7cccdec36676a073b776ed9485f5b7c2b53b5d1dc1c2bad`  
		Last Modified: Fri, 09 May 2025 07:42:27 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852deb019ed1ac5b15fe743a0acaeaaca7c4ce3e106fac9940821a21d8b7e2da`  
		Last Modified: Fri, 09 May 2025 07:42:27 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d712dcf32355b5074e96511dee93a54064ee966240ddbd82213321b86f274e`  
		Last Modified: Fri, 09 May 2025 07:42:27 GMT  
		Size: 76.6 KB (76564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62707bf14299873ece848adde37a7c2bcd68a38df9693e650b56c7aa94b27267`  
		Last Modified: Fri, 09 May 2025 07:42:27 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b797ad1510fcaf4d11b1fa1dbd10260a725cad4bea00f21ec42379f979faed47`  
		Last Modified: Wed, 23 Apr 2025 17:17:05 GMT  
		Size: 187.3 MB (187310890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5994212efa201d154de71324e03bcfe540be2a6cd1434a94d2dbc0ee1db488e6`  
		Last Modified: Fri, 09 May 2025 07:42:27 GMT  
		Size: 115.0 KB (115012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee6b89d5d126d87f72c9d1d1a2db7f24a1e1a36f9bfa243bc5e2460d67f4956`  
		Last Modified: Fri, 09 May 2025 07:42:27 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
