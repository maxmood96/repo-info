## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b43039aa5b428fb1167c5b5eca1382157009952dcb222abcd1201c66e7942dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.2461; amd64

```console
$ docker pull eclipse-temurin@sha256:640d426a50b0f8a0b4b25488f3be09474a7e4c9fd547a33e05d73f68c82e71cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307395456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2888c79f8ae26657a7d1bc384d0ef458ea4d6f6e106024e962b8af06d40068d8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 20:32:41 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:35:37 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 15 May 2024 20:35:37 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 May 2024 20:35:38 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:35:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:35:48 GMT
USER ContainerUser
# Wed, 15 May 2024 20:36:04 GMT
COPY dir:58180deb8c422e61d331dbc12d9d7d83d7afe3e9097adb59bd0860aff4211c36 in C:\openjdk-17 
# Wed, 15 May 2024 20:36:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:36:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5560c76ac3d9aa2d8a6dbf79d443a7e1d170aae31c940cf791c9b532d5756a1`  
		Last Modified: Wed, 15 May 2024 20:58:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2af4dff65a8f7657e3f8dc08fae0ef486f6d3c9923c29bbee8cfadbc6406add`  
		Last Modified: Wed, 15 May 2024 20:59:38 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e0654ef638e94acb97228830762c2f874b771d55ce15f35bb027284ccd5f44`  
		Last Modified: Wed, 15 May 2024 20:59:38 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b26edc3058244499bf8918dd920be0f68040cf0765a3e730a61f0a74f167f8`  
		Last Modified: Wed, 15 May 2024 20:59:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9385437ee992cda054dd58b68cdec45639198f6aeb496b0a2155e08a9fcfcf`  
		Last Modified: Wed, 15 May 2024 20:59:36 GMT  
		Size: 79.1 KB (79068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42fdc8b3c873f6e72310929b5759a1572779e4ffde6e357cdcd1f54d5706530`  
		Last Modified: Wed, 15 May 2024 20:59:36 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926fdb864bd036e230dde9ba43ad1f845bdde3300979d21944089cca10c470da`  
		Last Modified: Wed, 15 May 2024 20:59:53 GMT  
		Size: 186.8 MB (186822763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670b12458d67a3ab08a4cd5b945a3ab4b1c0c4437242d5f1cd601fcf5f54f498`  
		Last Modified: Wed, 15 May 2024 20:59:36 GMT  
		Size: 61.4 KB (61383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504c8ab0de376c42f12e1c64a08e78faa4090a1cc40b8ac6c3546814767c420d`  
		Last Modified: Wed, 15 May 2024 20:59:36 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:df226fcbc9f329a3521380843644bc6e55856832955e1033ddd16ee0077f14ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345449278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89311e6c8b48a6825ba432279a2d16a3b1726d05c0d96a511ce8d07080be906`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 19:42:01 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 15 May 2024 20:04:35 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 May 2024 20:04:35 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:04:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:04:45 GMT
USER ContainerUser
# Wed, 15 May 2024 20:04:59 GMT
COPY dir:58180deb8c422e61d331dbc12d9d7d83d7afe3e9097adb59bd0860aff4211c36 in C:\openjdk-17 
# Wed, 15 May 2024 20:05:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:05:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a511fea8e874efc08e5058ac5b12b6433c36ba6570862a619dd80cfb0e190`  
		Last Modified: Wed, 15 May 2024 20:45:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da49c4b8012eb26cf69c376d99dd8f1cb1e3ca715beb7254db10e9807c4fc9f`  
		Last Modified: Wed, 15 May 2024 20:51:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80045ad85cfa6eab06f555a848b724489fc2aafccc21d8dc6ac3b9201980ff7c`  
		Last Modified: Wed, 15 May 2024 20:51:09 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d438955ec9000bd485218afe17f2d42614a0ce5ef330651ce4c2940273c187`  
		Last Modified: Wed, 15 May 2024 20:51:09 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c63495db38074e2cb31d8afcccbf3f3588fd25c298c3f82cfce36b2deaf2b39`  
		Last Modified: Wed, 15 May 2024 20:51:07 GMT  
		Size: 68.9 KB (68939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49bc8a43e83602c3561ce59837b5348440e9d183f9f759da75dcee6267db095`  
		Last Modified: Wed, 15 May 2024 20:51:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738a714e59c4b1f12ea75f9464ba04edc60ffd95bda3b05f2eee986e1adc55a`  
		Last Modified: Wed, 15 May 2024 20:51:26 GMT  
		Size: 186.8 MB (186828072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f38da31e90682cc2a1244b437f26ec0258a2bd4b2d2e8aa66673f7a39d1baad`  
		Last Modified: Wed, 15 May 2024 20:51:08 GMT  
		Size: 3.6 MB (3603919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb9a00375cf2fa691459cb646837cf9806aad37551772a6067afcb59c220a7`  
		Last Modified: Wed, 15 May 2024 20:51:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
