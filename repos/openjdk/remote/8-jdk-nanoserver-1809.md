## `openjdk:8-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:3c381dbb75a375fcbefc554cda2ab478a66a19d4c6cc043b6d12cdb1169d4be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:8-jdk-nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:2b18eb08db5fd56cd7a93c680d2c1ab0c2fe73766bc429d9bec421b7b7602a1d
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200714414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115b5cbd4eb3ba351b64c99ff2b1f058823087c4c0b5d77a018d0a3236a97fcc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:49:48 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2019 19:20:51 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Dec 2019 19:20:52 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2019 19:21:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Dec 2019 19:21:05 GMT
USER ContainerUser
# Wed, 11 Dec 2019 19:21:06 GMT
ENV JAVA_VERSION=8u232
# Wed, 11 Dec 2019 19:21:54 GMT
COPY dir:423f1b6bc7bd2d846b13aab5eb2a97e2d8834390209ac9e4daad889695778323 in C:\openjdk-8 
# Wed, 11 Dec 2019 19:22:12 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:163d55b77f49371136083ba8066ddbec4afad6e1f4fbba77fa4ffebc99a8098a`  
		Last Modified: Wed, 11 Dec 2019 20:01:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb61aa9ed888d0d8d9389961f20030f4a91dee66b494c53ce01ae05416822da`  
		Last Modified: Wed, 11 Dec 2019 20:15:16 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c52d307080359dbdd2967108a2b78fb118dc2cb86367c6525165422abb66d11`  
		Last Modified: Wed, 11 Dec 2019 20:15:15 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dccb35e243d53cdb6b59dea00c5ee42dffc3692497b747efe0ab8123e38189c`  
		Last Modified: Wed, 11 Dec 2019 20:15:13 GMT  
		Size: 66.4 KB (66414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5cffbab6f7106e2c1524589536a02a575a708871a81691726ea72f02116b49`  
		Last Modified: Wed, 11 Dec 2019 20:15:12 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945bdf78ec06ce0b5607cc075c43b4b50456c1984ad0d98423bdec4976bf9736`  
		Last Modified: Wed, 11 Dec 2019 20:15:12 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f16a6211e7b42973694604eb408aac2261395849be4e3d3af1b0eb2b701f05`  
		Last Modified: Wed, 11 Dec 2019 20:15:29 GMT  
		Size: 99.4 MB (99436667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4091d57c06e37fb6bb03879cc9f8a6d5c0092ebe360081f062fdbe99298753f8`  
		Last Modified: Wed, 11 Dec 2019 20:15:13 GMT  
		Size: 100.5 KB (100541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
