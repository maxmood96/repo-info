## `openjdk:18-ea-33-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:e89ae104bfdc373aa69146d34cca382d2c3a36ec9c724d163b3acd78cc60edc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:18-ea-33-jdk-nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:39d3326c7aa02bb90f2c4ec7072daed00ca9a9a3b120d6f4deb40f98afde908f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290656334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb12404fdfc110bcad134986ff5e170e77fa0d65e8efe5f94b0de21e5a37d352`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:28:51 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 19 Jan 2022 22:28:52 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:29:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:29:07 GMT
USER ContainerUser
# Tue, 01 Feb 2022 03:31:27 GMT
ENV JAVA_VERSION=18-ea+33
# Tue, 01 Feb 2022 03:31:59 GMT
COPY dir:95c41d3bc60229e94a7850a91bc82381530c979d9ad441198fb641b53f80c2a3 in C:\openjdk-18 
# Tue, 01 Feb 2022 03:32:18 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 01 Feb 2022 03:32:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a1b3e13bb7b3d4b61b5f49a91d6eb9bfcf5539ab89c3687d608f17713c2409b5`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848f0583ef29156642246562456f8e070e665d934ee5b5eca5da3a549c83b769`  
		Last Modified: Thu, 20 Jan 2022 02:26:27 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408e60a5374b05b851d28c9154c5da23c66b31ff9344a9d4aa29e471f89a90f`  
		Last Modified: Thu, 20 Jan 2022 02:26:27 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fd9cc1e1a14cc04328a97d502fe56af7c5256437bad3c9c13e77832c28f28e`  
		Last Modified: Thu, 20 Jan 2022 02:26:27 GMT  
		Size: 68.6 KB (68587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cd88d42425b3a9d8b74a22ca8c7ca9daaa1903b0a06ee4fd2194cd5acf6362`  
		Last Modified: Thu, 20 Jan 2022 02:26:25 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99dcd6855668441cbc2f985729bbaf7b98622a8bcc5972a99daf8be3acacff31`  
		Last Modified: Tue, 01 Feb 2022 03:46:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb2bb14da9381f0d4a9a9fe389f007c58daa8393b4e2af27f3926cce2895bad`  
		Last Modified: Tue, 01 Feb 2022 03:47:11 GMT  
		Size: 184.0 MB (183987051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6848e93831c78634082198234b26270b5c67ae868db40c799ff7e1ee864497f`  
		Last Modified: Tue, 01 Feb 2022 03:46:51 GMT  
		Size: 3.5 MB (3547277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4556ffdb2ee3201b1dec5e50ab2f27a84d6093f7cec15f4df643941d9cfd8b3a`  
		Last Modified: Tue, 01 Feb 2022 03:46:50 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
