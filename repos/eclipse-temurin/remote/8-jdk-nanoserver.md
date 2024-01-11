## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e149159d643549477c0472f79f70eefb9cbe9e40fc83848cdb56eb29cafaffd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:a4f5a01f981792ddfc568fb7106046c0331344ecdbea92b448b59957f46c26d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222635469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5434b52e892d817694ced35baf547dfd6f55456f52a31eb4c85067b2cc81e383`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:17:07 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Wed, 10 Jan 2024 23:17:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jan 2024 23:17:08 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:17:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:17:23 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:17:35 GMT
COPY dir:d9c44d909d2b41aad5bf6fa4f7c7d36e81063822ae5e7ef30e4851bbe7809503 in C:\openjdk-8 
# Wed, 10 Jan 2024 23:17:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8628ad7aa058ffb12fa3ef62904fd96d1ef4b84c45f7b942775a6ae02a830eb7`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b604f3ee0869ea0719f02c17eac778b3b2e716757ac449ba79ea5b654ddcca7`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8240708d47924cf34a43fb95c84a9f970eb54178ae1825f974cb9e894e03f41`  
		Last Modified: Thu, 11 Jan 2024 04:18:55 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650656b3a0668e024e51fca51fc22124e405ce5a0090747a36498c399156a918`  
		Last Modified: Thu, 11 Jan 2024 04:18:55 GMT  
		Size: 94.2 KB (94221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59fc61beb41f45677b64051f9a23fe2b986c84b8e9014b2162ffedae722ed1`  
		Last Modified: Thu, 11 Jan 2024 04:18:54 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47f3f00c9a52dc0e25b96e5170b25d2a3cd941da502dbebff6b4880124fe144`  
		Last Modified: Thu, 11 Jan 2024 04:19:07 GMT  
		Size: 101.7 MB (101693938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572b2ccb25562c5861e63118b71bf877a015e9644cb8b327073200c13c9b01f5`  
		Last Modified: Thu, 11 Jan 2024 04:18:54 GMT  
		Size: 72.3 KB (72273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:92cae9b3fc874ac055a5ffcfa5261fb9a82436702892a856e4e86145f07fde08
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206445934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb6003da973b5ee823f8f32f989e4085ef67885283c0a63b6649472b8c3680b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 22:41:07 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Wed, 10 Jan 2024 22:41:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jan 2024 22:41:08 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 22:41:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 22:41:19 GMT
USER ContainerUser
# Wed, 10 Jan 2024 22:41:30 GMT
COPY dir:d9c44d909d2b41aad5bf6fa4f7c7d36e81063822ae5e7ef30e4851bbe7809503 in C:\openjdk-8 
# Wed, 10 Jan 2024 22:41:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec88c6fd1d0cd14082069642ccb3b0dd5a7538a4b8b0c2d430549f345d8fd53`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a70ce583d963a632ef35f9621118c53550bfa3e2ede770446582b854c282042`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b458c740d49612fd593af7fbdfabd3958245ad1931a748d10694f35e9a23f5`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f8ab83b9667552a30989b2807670e54d43f9fd8c43e433f52d7bf74ce674f9`  
		Last Modified: Thu, 11 Jan 2024 04:09:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a79de0ed29ea826956427092d73b26807e20d9d636513da4988cf310828211`  
		Last Modified: Thu, 11 Jan 2024 04:09:19 GMT  
		Size: 70.5 KB (70482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24989b19b1c3828ca50012cebdcb8afc9928b3289edc89dc539a013fafd72539`  
		Last Modified: Thu, 11 Jan 2024 04:09:19 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6c9ae9c8d7026b68eef25911e564bd390b01af613253c76e8ab583213815f1`  
		Last Modified: Thu, 11 Jan 2024 04:09:31 GMT  
		Size: 101.7 MB (101696161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfa7b0b7a0368313e5029da7fd44eec5bf3698117fc20992fff72d9516efbd4`  
		Last Modified: Thu, 11 Jan 2024 04:09:19 GMT  
		Size: 82.3 KB (82347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
