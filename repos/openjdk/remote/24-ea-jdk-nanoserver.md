## `openjdk:24-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:0b2bd4bf8e0555a4966933e3a35b301ac2631f6363aff9782cd0714e379c8d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-jdk-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:988edac54a50de51f1920a9e8000d5b4adb93c6c6d61dd54215daa65870e7473
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368154372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a42fa79146014ad2d6bfa7b9d7039857f51edafaf7613489f096561f805331`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Tue, 26 Nov 2024 00:08:30 GMT
SHELL [cmd /s /c]
# Tue, 26 Nov 2024 00:08:32 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 26 Nov 2024 00:08:32 GMT
USER ContainerAdministrator
# Tue, 26 Nov 2024 00:08:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 26 Nov 2024 00:08:47 GMT
USER ContainerUser
# Tue, 26 Nov 2024 00:08:48 GMT
ENV JAVA_VERSION=24-ea+25
# Tue, 26 Nov 2024 00:08:57 GMT
COPY dir:258a72c49d90829f48c37f1943736777958760f35fe9cb07955381917f6524b9 in C:\openjdk-24 
# Tue, 26 Nov 2024 00:09:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 26 Nov 2024 00:09:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35989cc7df9ef9725db16d6be919ecae441fccd0c0ec2df5cb067fc448fe4c75`  
		Last Modified: Tue, 26 Nov 2024 00:09:11 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6169357cb773209d9af00d14661604d390febc3a3a8d40d15ca13bcacdfc980`  
		Last Modified: Tue, 26 Nov 2024 00:09:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c97948b2606eab880b64cbe0f8a4636d21db3f39f85c528403eba47b5bbea8`  
		Last Modified: Tue, 26 Nov 2024 00:09:10 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32828e375acd05679bafc9c734366ee23c193ac705948e7b43bf10d985ee16e`  
		Last Modified: Tue, 26 Nov 2024 00:09:10 GMT  
		Size: 66.6 KB (66588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc6b43df7c782d1b0f8e2c9d16839b592be3d1f896e1c1226fdf4207c87e590`  
		Last Modified: Tue, 26 Nov 2024 00:09:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e18fe3ddfe6f154af1693eeb5d2fc4015354311659651d0c217d4c188114a6`  
		Last Modified: Tue, 26 Nov 2024 00:09:08 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194a28691d41b2f7c1fd6a77151468a661ecff4f87de71e5b9836c4f53f0ea96`  
		Last Modified: Tue, 26 Nov 2024 00:09:19 GMT  
		Size: 208.5 MB (208459378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f90b1e2c47fafc1823da54886ca761d416e7de5da7ad9d55f86051cc2e4458c`  
		Last Modified: Tue, 26 Nov 2024 00:09:08 GMT  
		Size: 4.4 MB (4407770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99959769ae0fe4be8970bc407c817e25b5ed2ebab0c24953845dd199d8b404dd`  
		Last Modified: Tue, 26 Nov 2024 00:09:08 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
