## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:699c159b5cb441dd8fc06e9f6ac9a7978a6b1f8eab50c1ccf7f5c0b2f59b3d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:afd4b3fb04d65e005c258e180c6967ce76850d8d4f0cf434c6d3170eff4f2205
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314725741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e171a62ad9d383be15f04ca42f3e9b3a1d799aa883e6865e437aae506b68ba`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:27:44 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:29:03 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 12 Jun 2024 18:29:03 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Jun 2024 18:29:04 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:29:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:29:14 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:29:30 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 12 Jun 2024 18:29:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 18:29:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ae17666c85b2b00f8e5aa24951a59f0b01a1eb41704faa32e1282e0f0ef217`  
		Last Modified: Wed, 12 Jun 2024 18:52:48 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea358a99b6c4175aaf5f9486194d911138c450ffa13f45e102f1539fee9f32c6`  
		Last Modified: Wed, 12 Jun 2024 18:53:35 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67291aac9e33e31baf9decee3bafa55569a24608299e634f094e24c14a6501d3`  
		Last Modified: Wed, 12 Jun 2024 18:53:34 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f72be97270f7c9d1e5761550ec67b54b386652154067cb5f920effc045628a`  
		Last Modified: Wed, 12 Jun 2024 18:53:35 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2170e5dc67eeac86b745b8f0a1d529d966be5d40259deec56be5837417802d`  
		Last Modified: Wed, 12 Jun 2024 18:53:33 GMT  
		Size: 83.2 KB (83159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc3e14751faa5de8a8ab0d5a22999319b3b998004c05eb7df57a4e72476cb14`  
		Last Modified: Wed, 12 Jun 2024 18:53:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1aeefe150599136c59a3cf28c3bd75b84738727b6d50a395235cbd96f4ab4ce`  
		Last Modified: Wed, 12 Jun 2024 18:53:50 GMT  
		Size: 194.1 MB (194084563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e79aeb435a54adf59957f3ff57e998dd5c51b416249dfbb5ff4be82f8476c41`  
		Last Modified: Wed, 12 Jun 2024 18:53:33 GMT  
		Size: 62.1 KB (62103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59b7a837a6731fe01a3909820c7a19987b1ee0b565878cde098402d5f1d6712`  
		Last Modified: Wed, 12 Jun 2024 18:53:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:4a9eba0b99feca20972aeda410248c5790320e97f5b62bbdb1e9de6e6e9b0ea4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349255212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3d37b6caf4369e6e0f0053a40a73275046aefc512b0217a68c7cc22844d9e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 17:51:03 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 12 Jun 2024 17:51:04 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Jun 2024 17:51:04 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 17:51:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 17:51:13 GMT
USER ContainerUser
# Wed, 12 Jun 2024 17:51:28 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 12 Jun 2024 17:51:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 17:51:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77f119d6104e3c8342435b5ecf20e3d87fd794b0b9d432c754d791dda070c15`  
		Last Modified: Wed, 12 Jun 2024 18:43:26 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb3afe9e4bf592bc5953d90b42d691e67c1bd6e2e85f763440a46e9af8a279`  
		Last Modified: Wed, 12 Jun 2024 18:43:26 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06259e7480cb7dc7229ee508752a310efbcc003e7cce59426c878fe97b66322`  
		Last Modified: Wed, 12 Jun 2024 18:43:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8b43aaa845da9fc8d7216df2a9485bc92264455f05123c47b9c198f5359e67`  
		Last Modified: Wed, 12 Jun 2024 18:43:23 GMT  
		Size: 71.6 KB (71646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d564193114d887c543c571d7eccefb26d886f1092038aaac0050df32e66ad2ff`  
		Last Modified: Wed, 12 Jun 2024 18:43:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a0ef37d7f1b173e65444b9fa2ff4266efebca26c93d7d8fb78a378418f9f39`  
		Last Modified: Wed, 12 Jun 2024 18:43:41 GMT  
		Size: 194.1 MB (194084597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7fce39f8d007e5cf4fdbae852fd0136a0d5406c7824fc4d3badf9275a078b0`  
		Last Modified: Wed, 12 Jun 2024 18:43:23 GMT  
		Size: 58.8 KB (58760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e389ba1178e24086751d64b9e3bd4b17dd96d66252bc240b1a8e06fd325893`  
		Last Modified: Wed, 12 Jun 2024 18:43:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
