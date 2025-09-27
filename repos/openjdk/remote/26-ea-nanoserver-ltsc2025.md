## `openjdk:26-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:4f2488752a41acad3972b779811ddb1f1f5a7e29e30491c0f6b1db368c880aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-ea-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:9da73a6c267bd7cb0f0e14c33070858598428b9e3c85572e2d17767050dc596f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414853749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7177ebde232486eaf7672d913e1468bb3a8ef24d2d9ba7c8fc420c3b658855`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Fri, 26 Sep 2025 22:47:00 GMT
SHELL [cmd /s /c]
# Fri, 26 Sep 2025 22:47:01 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 26 Sep 2025 22:47:01 GMT
USER ContainerAdministrator
# Fri, 26 Sep 2025 22:47:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 26 Sep 2025 22:47:06 GMT
USER ContainerUser
# Fri, 26 Sep 2025 22:47:07 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 22:47:49 GMT
COPY dir:00243416b2d1eb1675fd4c082ccd61e2c80377000367c1dfb1f71202ed6aabd5 in C:\openjdk-26 
# Fri, 26 Sep 2025 22:47:55 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 Sep 2025 22:47:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b741f584780373c0131b04e26a481ecf7bdc5cf0b492bda8404c4cef838d7932`  
		Last Modified: Fri, 26 Sep 2025 22:48:23 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b212c396b1eddfd482e03d706b17ea388120ebb2ebdf7e677682fc59b1ec49a`  
		Last Modified: Fri, 26 Sep 2025 22:48:23 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77e5219201e08e5dc81c896d6197f89e0d4016cb0ceb7220992d461fecacbe4`  
		Last Modified: Fri, 26 Sep 2025 22:48:23 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cbd186d5c5bf5b1dbb6effacc272720b080ad6d08304e8c438d1c79763dda7`  
		Last Modified: Fri, 26 Sep 2025 22:48:23 GMT  
		Size: 70.2 KB (70160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8fe0f68c7311d2e8b4b182dc44150560c06abaec298720ecb2406dcfe59ca3`  
		Last Modified: Fri, 26 Sep 2025 22:48:23 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acbd549cd256f0f04765308c836961a9c95316594e3e509a5e1233c0bcb2816`  
		Last Modified: Fri, 26 Sep 2025 22:48:23 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413ca55b1d2458c93f2710143b3d1af9b8e1ce4633a91fec191b3c1b0fb82722`  
		Last Modified: Sat, 27 Sep 2025 00:24:20 GMT  
		Size: 221.1 MB (221123578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d61762c1f1f6d378093c3b5ca29605e85acadbcf8bfebbe1d526f8e04294a7b`  
		Last Modified: Fri, 26 Sep 2025 22:48:23 GMT  
		Size: 102.8 KB (102807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211bbe534e417ea31d320d0eee60034a310bdc37e3f011d288bf28d7972afd41`  
		Last Modified: Fri, 26 Sep 2025 22:48:23 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
