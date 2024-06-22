## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7d532bc5c5b76a61abe14b07dd08c1ddf2026a00979d7aab281febe9a1c627b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.2529; amd64

```console
$ docker pull eclipse-temurin@sha256:e9fe96f874ff3bc78a6f5208fc96b41313fb4c98aa9bab40634940cde447d025
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222353674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f170959e7a97defa92daba9d35e8c0d6a2080acf7e9459774b0af12fce3fff`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 00:50:29 GMT
SHELL [cmd /s /c]
# Sat, 22 Jun 2024 00:50:29 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Sat, 22 Jun 2024 00:50:30 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 22 Jun 2024 00:50:31 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 00:50:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 22 Jun 2024 00:50:43 GMT
USER ContainerUser
# Sat, 22 Jun 2024 00:50:53 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Sat, 22 Jun 2024 00:51:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c04e6fe7f33e5ed7b73641c362d031eb0404b55967c9af2b8fa6f2269d9f92`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b174078aa7a66a8b622abdc2a54e532be01686cada8b14b73b36ea06415eb6cc`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ff4188cf271748f13726e82487fe15353b089142d1af3090ccb2c007885b0c`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ef3ce5545b1eeaa16986a08c1644cfcf0acdb70e03c9613088e7f5a3588271`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8445abea445ef1c0fe004a0b917c558137e71f35550eb457adf5f148f579d83`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 94.8 KB (94840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a8432058d09db20b0fe84efd2d8c3eb4c5371e198e6b9cde3fee1535706bb3`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef92566de8cf5a00a6b42f65e863f4b205cfe6ce170a8293cdc7d55ce8f97e61`  
		Last Modified: Sat, 22 Jun 2024 01:06:36 GMT  
		Size: 101.7 MB (101685011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea66dad1ceb60ba6d2006671a607de85decd165e4d8e5dc95a0e975c6d7fca37`  
		Last Modified: Sat, 22 Jun 2024 01:06:25 GMT  
		Size: 68.5 KB (68468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:213cfc48d6c1162f70bdfbe486c5d53db1de3e412277faafea859d572c6a8890
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256902909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c9a3cf4adedbf6bf61e269180206524d9f0f1c33f58e9d0c84f244a32c2cff`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 17:41:08 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 12 Jun 2024 17:41:09 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Jun 2024 17:41:09 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 17:41:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 17:41:24 GMT
USER ContainerUser
# Wed, 12 Jun 2024 17:41:36 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 12 Jun 2024 17:41:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:e103b0c4319eeff05be4b5cc015670eb122f3727896333159e7321bc10634963`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8d6954eb39f9fd2f578ce496e72392db95feeba4f554191404ad7b6b709d5e`  
		Last Modified: Wed, 12 Jun 2024 18:40:42 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ff02bf0ad42d650e4abb942ee2fbdfb7ed0cf9a7ceae338aaa48c0a6dfc9cd`  
		Last Modified: Wed, 12 Jun 2024 18:40:41 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a84c83bc80d6b9b72ded2a37d4cfd8436c1a3bb6a6dae21c64eacf138db34d5`  
		Last Modified: Wed, 12 Jun 2024 18:40:41 GMT  
		Size: 76.0 KB (75997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f107f1e4d09247900bdf27d9c22c33a029f55e34fef8538899888171bba9a887`  
		Last Modified: Wed, 12 Jun 2024 18:40:41 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d22cfc6909b097347eb6f46d08a1092a9f0df3d2b12292b0e7e681c94b1772`  
		Last Modified: Wed, 12 Jun 2024 18:40:53 GMT  
		Size: 101.7 MB (101699154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c448abd661b393e23cff7543bcd83a1aed436ca6ff1c8e841237a2fddddd89e3`  
		Last Modified: Wed, 12 Jun 2024 18:40:41 GMT  
		Size: 88.8 KB (88759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
