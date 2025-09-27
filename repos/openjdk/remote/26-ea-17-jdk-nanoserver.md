## `openjdk:26-ea-17-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:68560ce73ee1a24fb7888796c52699ffcf088dca5478aa2ce64d4b8e06bd4a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-17-jdk-nanoserver` - windows version 10.0.26100.6584; amd64

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

### `openjdk:26-ea-17-jdk-nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:eb9da50056a5c0f2f2faf3a62ac52b3aeb6a23977946420b7d63ccdecbc83dfc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.1 MB (344058230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993fcbccbd5b8a3b474214b7bbaf91ac08fe645f3365d7c7c3e3bcdcfce08bcb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 22:47:03 GMT
SHELL [cmd /s /c]
# Fri, 26 Sep 2025 22:47:04 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 26 Sep 2025 22:47:05 GMT
USER ContainerAdministrator
# Fri, 26 Sep 2025 22:47:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 26 Sep 2025 22:47:17 GMT
USER ContainerUser
# Fri, 26 Sep 2025 22:47:18 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 22:48:14 GMT
COPY dir:00243416b2d1eb1675fd4c082ccd61e2c80377000367c1dfb1f71202ed6aabd5 in C:\openjdk-26 
# Fri, 26 Sep 2025 22:48:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 Sep 2025 22:48:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46340b8979f289bcaf285ece02bed3ec2854bfa7c2ed4832db6c4aa2305f9ed0`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c129981d58881324998b0e4847cee578c3bd437b03960324b76ff46f24e7f3`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cab07eed729b42d1000ca66b8393917c8a57182dda802c628ed7423f191d21`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c935ed3274972357166c602592471dd8551c916e641baa7b95d17fdaa17bd6e7`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 82.9 KB (82875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafb8cf92d35cfd6d65a646ab0c3bdbc458e2a5fd0b7b2ddc395ca04cd5911fe`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23edf0f483301e5359c2758a43a7900f5d075941f50eae4678814bdd3b905a`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019399d7d29937e73b72c0dee877fbac772669d5b10ec4b79af9ab8415ac822b`  
		Last Modified: Sat, 27 Sep 2025 00:24:12 GMT  
		Size: 221.1 MB (221123424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90b2b14d405a3fdb5c9b33abb8b82326fec747a4196d0bcad23bc705f60740`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 125.7 KB (125705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ea98e12ff56769b07c025fbaac2ce83e072bf845c23c9290db67c0eb14e27`  
		Last Modified: Fri, 26 Sep 2025 22:48:55 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
