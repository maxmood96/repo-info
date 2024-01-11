## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9fc9e6889db61b7c4f473a31328b88532270f4daca59ee5f75edd4b9ca87e438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.5329; amd64

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
