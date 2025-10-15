## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8a8a07b4308724e2204c6bd36d06eccd08f7a2ec36971bfd20b2335b145dc31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:90c3e11374467809e0d2b6350342143fc6750efb3282dc148b8b354d1de46a3d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.8 MB (388829150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97299616241440ce9bc0ae2a9f48ea49510799a91c0ef8e17995f5a88c02cf0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 21:13:22 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:23 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 14 Oct 2025 21:13:23 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 14 Oct 2025 21:13:24 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:29 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:36 GMT
COPY dir:210c213d7567f4ae9108259b6c16f9783779d8f224bc53a31a49e53f33738954 in C:\openjdk-11 
# Tue, 14 Oct 2025 21:13:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Oct 2025 21:13:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf58f2091e1f5f98c259bfbfb77f31f2a9af5d2eeb54b448ec0c972e5a891b2`  
		Last Modified: Tue, 14 Oct 2025 21:14:29 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795a2004c991bd1d65d798d6555d50590fa5f1ec1da2016fe0281dbd9b4703af`  
		Last Modified: Tue, 14 Oct 2025 21:14:29 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d904d151b40b515b8ff4684eb053607f68b3e4e2ecc524144ea1a3e5e80d1b1c`  
		Last Modified: Tue, 14 Oct 2025 21:14:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43cda84125de1f8150f8dfcad87f4993da458ed77d358b6722036aa0b9a8251`  
		Last Modified: Tue, 14 Oct 2025 21:14:29 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171a837662a90f6015c2cb883cdc8ead03616c3968994ba7bc1e9d5632efcf9b`  
		Last Modified: Tue, 14 Oct 2025 21:14:28 GMT  
		Size: 71.9 KB (71866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4996ee0de3df2d840bf952fc2786dd629b3a8fc7b2a8b6d5a08cfd1955020d19`  
		Last Modified: Tue, 14 Oct 2025 21:14:29 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cfa7e37efc40dfc8c02d0239e17eaefa94bee108449e2952bc96f4d7f849d`  
		Last Modified: Wed, 15 Oct 2025 00:13:02 GMT  
		Size: 194.6 MB (194620422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b24503251e7a60b3a15215d8850943f52c1ed29a6fac9fb21403c0d8da5bf15`  
		Last Modified: Tue, 14 Oct 2025 21:14:29 GMT  
		Size: 103.7 KB (103677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db519873ccc39677b9eab1e0be4e6cf53fd9e2d8abf196dae94c57eccd96f45a`  
		Last Modified: Tue, 14 Oct 2025 21:14:29 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:ad1ddf7cedccb2e0b7f4fa034ad6be261cbd2b9285888ac116b26ae26862f72a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317492522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430ab9f71d5d9f2e17dac1ab49b08c7fdac0ceadc4303c02e019e39b9b1b79bd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:12:39 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:12:39 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 14 Oct 2025 21:12:39 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 14 Oct 2025 21:12:40 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:12:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:12:43 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:12:50 GMT
COPY dir:210c213d7567f4ae9108259b6c16f9783779d8f224bc53a31a49e53f33738954 in C:\openjdk-11 
# Tue, 14 Oct 2025 21:12:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Oct 2025 21:12:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd747c07589c6a814c4f7a7c3abfb6aa666808466241c2d588fd8a9597b7367`  
		Last Modified: Tue, 14 Oct 2025 21:13:19 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb098dbc3042fdda15aea6da185980b6f11a5b234d18ecdb168bba90b1068fb`  
		Last Modified: Tue, 14 Oct 2025 21:13:19 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a5cdf2e92adead47a6a6548b9c3f99c73164e2b6e54b0a17a955f839a28a28`  
		Last Modified: Tue, 14 Oct 2025 21:13:19 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299d610d2333559c7f354cc45c915b4d6588ddd9ef5196f23955820d9dbe07b8`  
		Last Modified: Tue, 14 Oct 2025 21:13:19 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8d02374bf84b0ed9696d627327510cb685b107373d57e85ad07935a6fffc3d`  
		Last Modified: Tue, 14 Oct 2025 21:13:19 GMT  
		Size: 80.2 KB (80240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4879241149903949b2662b698c71223ec14cc3f141fb2a9413529dc261117ba`  
		Last Modified: Tue, 14 Oct 2025 21:13:19 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebbfb65b70be519d7aa2c269e5e47707ca7f61dd35f526a79ef8a7a59a33afa`  
		Last Modified: Wed, 15 Oct 2025 00:13:07 GMT  
		Size: 194.6 MB (194620432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e499dae160a4bc98b0b3aa2c1bea34bda3456af939e19836a1fee949e502c47b`  
		Last Modified: Tue, 14 Oct 2025 21:13:19 GMT  
		Size: 96.6 KB (96558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11baad135e98a0ca7a4cc8ec2a7f6c55d5828c0a350352f0e2bd2200dfdfdc96`  
		Last Modified: Tue, 14 Oct 2025 21:13:19 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
