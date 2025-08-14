## `eclipse-temurin:8u462-b08-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0421d510fc9ac8b1367da587ceccf7ab05c27dbc29ca226c42cb8eb56873e976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:8u462-b08-jdk-nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:e9eb105ee43bd2135be6af7110576e55be20b05cf8633c6147dfe6072ce016cd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296098383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdc7221d81235943c70dfab998f62815be071a15da0d26a619419ac88f3e43f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:49:56 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:49:57 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 12 Aug 2025 20:49:57 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 12 Aug 2025 20:49:57 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:49:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:49:59 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:03 GMT
COPY dir:8f60928811eb34a4f9439f9096d4a66f726650730b831f7d5ea7bcab71861e91 in C:\openjdk-8 
# Tue, 12 Aug 2025 20:50:06 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4045f7f0f08b1351cceece699b7e02f12fd3df9c3c559ca6422d203b2119e66e`  
		Last Modified: Tue, 12 Aug 2025 20:50:58 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd31d8eae5603c40c538b27ca8fd4e9a2dd8cc5499634465df650144e835551`  
		Last Modified: Tue, 12 Aug 2025 20:50:57 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572856f066cbfea9b4357a7571c4fe768319ca8e969ce8833fad6110fd8c5034`  
		Last Modified: Tue, 12 Aug 2025 20:50:58 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36258e7ffdbaa55c56bcfe07ff6631e815fde38e06b91f5d7a6a2ac6576fb51`  
		Last Modified: Tue, 12 Aug 2025 20:50:58 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687ffc9a12f167627cfcb125aae1803ac7236df2e85130e6e9cc2ebd3353b60c`  
		Last Modified: Tue, 12 Aug 2025 20:50:58 GMT  
		Size: 75.4 KB (75449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622917a22c8756c45019aa405d361ccd8b7d0dbb4cb8c55c1337ba90ac37ef2e`  
		Last Modified: Tue, 12 Aug 2025 20:50:57 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3460a405890f1233642f156ca730d721c6bd7b1732ac241745daca3e3f195f`  
		Last Modified: Tue, 12 Aug 2025 21:19:44 GMT  
		Size: 102.4 MB (102434913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6650d488167cd9151a8bb73d59494c5f27aa1d5e58304562f84d575dc8dd039`  
		Last Modified: Tue, 12 Aug 2025 20:50:47 GMT  
		Size: 113.2 KB (113170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u462-b08-jdk-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:ebaa6b955b5278efb48d459d0af253f6592c725a501c92d019092195ea46fdd9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225283946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9273849692806dbb1604ffd60973b9da5c908d930e637d89ff8d3aecf9595012`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:50:23 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:24 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 12 Aug 2025 20:50:25 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 12 Aug 2025 20:50:27 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:31 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:38 GMT
COPY dir:8f60928811eb34a4f9439f9096d4a66f726650730b831f7d5ea7bcab71861e91 in C:\openjdk-8 
# Tue, 12 Aug 2025 20:50:44 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbcb3de280f9b7eb0e365b3cc8c9807000764a85f3b676e1e3183c2d608475e`  
		Last Modified: Tue, 12 Aug 2025 20:51:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9717117c15fec13529567eba37f47960081ee0ccefc7e4628dbba545d1da4b01`  
		Last Modified: Tue, 12 Aug 2025 20:51:38 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c627020787dcaf346bdb70e66babdaf0cc7e6be7ee88c8a094e56f7485ea26c`  
		Last Modified: Tue, 12 Aug 2025 20:51:39 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74843625d781d8b0bcad037b67a7a73366a4008280b5fe6944f4412865ebed2d`  
		Last Modified: Tue, 12 Aug 2025 20:51:38 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b53385b301446b663bb4a6e3ecf952d9d5379da21f9931599067bd7642e5e5`  
		Last Modified: Tue, 12 Aug 2025 20:51:39 GMT  
		Size: 78.5 KB (78498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def9c79292ac78fff38178d9414496f353b448f74d9c1f14ca2b24b492647501`  
		Last Modified: Tue, 12 Aug 2025 20:51:38 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b11e18552887006625e8ea06bb78224ae37d55798cc8f9ddbd13a8323722ed`  
		Last Modified: Tue, 12 Aug 2025 20:52:01 GMT  
		Size: 102.4 MB (102432972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992f41ecfcf151f4e9b037238540d02ed3fe62e9f37f9c2e1cd93fbb49aae04`  
		Last Modified: Tue, 12 Aug 2025 20:51:39 GMT  
		Size: 107.0 KB (106959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
