## `openjdk:25-ea-21-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:ceb6f03f4780cb43fabad0818182ff81de879322e0a4e5ee1ba225ea3837c6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-21-jdk-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:d2ac3ed03eb4c2a6845ea4e5fac232104336ba160fd27b985029f89a934b03e0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.2 MB (399188981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3dd09bf09998e6fc2d599f0b681321d0188f863fb3e0994141727ca932670e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Mon, 05 May 2025 18:15:43 GMT
SHELL [cmd /s /c]
# Mon, 05 May 2025 18:15:45 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 18:15:48 GMT
USER ContainerAdministrator
# Mon, 05 May 2025 18:15:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 05 May 2025 18:15:59 GMT
USER ContainerUser
# Mon, 05 May 2025 18:16:01 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 18:16:11 GMT
COPY dir:38c9db30a8dff81edae6bd00112f30e7c6eed8d0f73c59888875d8c30a4a8de1 in C:\openjdk-25 
# Mon, 05 May 2025 18:16:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 05 May 2025 18:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafb9f71f8d35a779092d3a9cd50121413cafc540a91ec3fc00148f688304858`  
		Last Modified: Mon, 05 May 2025 18:16:26 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7999c4994c4285bc63ecebaa9b077168bbf2ec0f487f6b4540a2a4226be894ea`  
		Last Modified: Mon, 05 May 2025 18:16:25 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a8c685ac339a5531ee6d2f559b1835c04ef20206e852c574d89df6cbf5af75`  
		Last Modified: Mon, 05 May 2025 18:16:25 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60085c4619c552efa7c80216a91deeabb5eb45f0783bf9af3d5167a36ead87d`  
		Last Modified: Mon, 05 May 2025 18:16:25 GMT  
		Size: 76.5 KB (76510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4c805ea3329b4deecfbeedfd7ca02e146318d7df630fa83e3f6b02c03790d0`  
		Last Modified: Mon, 05 May 2025 18:16:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f299a69fc1175bc39bc4a219bdaf17134399dcdf28c1d1386cdb683d0b1e77e8`  
		Last Modified: Mon, 05 May 2025 18:16:24 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94757bc67637d3787e05740f11f27a50138bc32a7539e578af682e49d4a303c4`  
		Last Modified: Mon, 05 May 2025 18:16:38 GMT  
		Size: 208.8 MB (208849514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d1f558df9705d1b0cf98a1e627e44ec506764db15d97c080e1fa397b18d2`  
		Last Modified: Mon, 05 May 2025 18:16:24 GMT  
		Size: 114.5 KB (114542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99deacf4608d0f6ffd2a1af961e4b43a7da719e196f999911d2faeee1f06ff9e`  
		Last Modified: Mon, 05 May 2025 18:16:24 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-21-jdk-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:4b81b26d90899edb00590749c155e35ef662f6b96826dc1328598a5bf7fea821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.6 MB (331576073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8e912a07fe069e89dde27d8d1aa4df1b4db358355c7bd6e3c791f2bb2302a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Mon, 05 May 2025 17:36:19 GMT
SHELL [cmd /s /c]
# Mon, 05 May 2025 17:36:20 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:36:21 GMT
USER ContainerAdministrator
# Mon, 05 May 2025 17:36:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 05 May 2025 17:36:37 GMT
USER ContainerUser
# Mon, 05 May 2025 17:36:38 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:36:46 GMT
COPY dir:38c9db30a8dff81edae6bd00112f30e7c6eed8d0f73c59888875d8c30a4a8de1 in C:\openjdk-25 
# Mon, 05 May 2025 17:36:51 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 05 May 2025 17:36:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9635bc147a7cf7815d9348f116cacd975415a199d02d61357d967a665154dd40`  
		Last Modified: Mon, 05 May 2025 17:36:56 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492d96f02510e216edec6dc2cc936db9a94b20c98468d0bb61af77f9a6866b82`  
		Last Modified: Mon, 05 May 2025 17:36:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446d06add54d27d68692b4da073d387ba52f04f092e6fc195152bf54da5fc5f2`  
		Last Modified: Mon, 05 May 2025 17:36:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cc3c2f9a2b8240ca8f309ef15b11efd398db669e95a6840e37bd5c84dc0f95`  
		Last Modified: Mon, 05 May 2025 17:36:55 GMT  
		Size: 84.3 KB (84260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17dbe5c39933bf7bd887ef0a24be24f912bb099b3d81395ede1291930883be8d`  
		Last Modified: Mon, 05 May 2025 17:36:54 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e76599aad8b709c1e5b59d8de38b9b1c688472f471a62ce14453b0e77acc661`  
		Last Modified: Mon, 05 May 2025 17:36:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807ebeebeece88b9d681369be31fdb24fc92ab8749b19d2b34c74daf192ab1b5`  
		Last Modified: Mon, 05 May 2025 17:37:06 GMT  
		Size: 208.8 MB (208848902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1117ba3ba20ecb79eb47c1bfab4edba1a492a50ff9404b1a1221b5c9f5b9f652`  
		Last Modified: Mon, 05 May 2025 17:36:55 GMT  
		Size: 97.6 KB (97641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2696902c14fdd3f554fc8dd9981eddc64aa74ad2363f53d74f9b22cab80842c9`  
		Last Modified: Mon, 05 May 2025 17:36:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-21-jdk-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:231a829db0c31764d77d2f78fee0de7562dfd5d3390188bb4adca95e778027ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322347869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f954adc5055b7f675358b23cd9aee795f87ab5757d4bea43a445942ab1bda8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Mon, 05 May 2025 18:10:18 GMT
SHELL [cmd /s /c]
# Mon, 05 May 2025 18:10:19 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 18:10:19 GMT
USER ContainerAdministrator
# Mon, 05 May 2025 18:10:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 05 May 2025 18:10:29 GMT
USER ContainerUser
# Mon, 05 May 2025 18:10:29 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 18:10:41 GMT
COPY dir:38c9db30a8dff81edae6bd00112f30e7c6eed8d0f73c59888875d8c30a4a8de1 in C:\openjdk-25 
# Mon, 05 May 2025 18:10:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 05 May 2025 18:10:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce93b8eafc58c0c9e0fe40d1f12a473525c44e9813d498c5aad120415a54a89a`  
		Last Modified: Mon, 05 May 2025 18:10:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88de9bb883edfe317e9c2f63b3bd934348f944f4d71145b3c29a68b2df9a4a01`  
		Last Modified: Mon, 05 May 2025 18:10:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b1938e7872143a2fd9bc282154b39aef3b780726ab03ad2b3eafc156cc41e3`  
		Last Modified: Mon, 05 May 2025 18:10:52 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0a4c54e0abd44ef849e65aea191b0062c17280cd2e30cbe7e34d926079f5fc`  
		Last Modified: Mon, 05 May 2025 18:10:52 GMT  
		Size: 64.2 KB (64231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87c17ca7ad0b9c5353087f739967e7467232351872c9b6d902de3d0adf154bc`  
		Last Modified: Mon, 05 May 2025 18:10:50 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b050ebfe696340ad823d8805ebf9ecdaf44660d657be1aac7e036c42c1dcb7e0`  
		Last Modified: Mon, 05 May 2025 18:10:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67799c804181d88a2cf0e361138443dfdfa20922755b753f6050f176fda35b25`  
		Last Modified: Mon, 05 May 2025 18:11:02 GMT  
		Size: 208.8 MB (208848831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91410ef755ac4abf7f8195f4a16c0f6d350d0deedb874b7a13dc78525b3eed6c`  
		Last Modified: Mon, 05 May 2025 18:10:51 GMT  
		Size: 4.7 MB (4676291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fa446cb2c7396927227c1b625da1e13a4da6115320c03f8a43c6892ae02ed0`  
		Last Modified: Mon, 05 May 2025 18:10:50 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
