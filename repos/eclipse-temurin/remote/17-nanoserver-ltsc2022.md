## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a11e6132e870b37bc2338a452b042974bb934a095f6466e0033df53c603401ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.288; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:a05c3c693147aab51778a2af1c91bf2afa0a617b6e63f6add98bd32a15894229
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302065142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9750a9d8b0b6d34d0327d3064ddb1b15dad6cf06e1d1ea28ff086226e5aee4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 19:02:30 GMT
SHELL [cmd /s /c]
# Fri, 05 Nov 2021 19:44:53 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:44:54 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 05 Nov 2021 19:44:55 GMT
USER ContainerAdministrator
# Fri, 05 Nov 2021 19:45:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 05 Nov 2021 19:45:05 GMT
USER ContainerUser
# Fri, 05 Nov 2021 19:45:22 GMT
COPY dir:75727e79a870c9066772bd3811959a8f3c491ac4b54ae3b2c145d1638b6bc93f in C:\openjdk-17 
# Fri, 05 Nov 2021 19:45:37 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:45:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ba797e8f93823c3d71c52fcae413f3a33ca28ff2711c09ba5141432948f8298`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcc88ba9f3dc1ac524d4cc83caa7f4187bb26c4f3359de76f43532af63ead53`  
		Last Modified: Fri, 05 Nov 2021 20:40:14 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824488832e7a4093e66432ffa8717416ac3b13aa02c4447f57054fa670d27e92`  
		Last Modified: Fri, 05 Nov 2021 20:40:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8e7b377f18c96454726518bca09656194cf1c5bbbe88b8e5672d15b091b78d`  
		Last Modified: Fri, 05 Nov 2021 20:40:14 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738a5325c8ba5c88770c12f79705070ae4708be20cdc4bf09db53ef65b4807fc`  
		Last Modified: Fri, 05 Nov 2021 20:40:12 GMT  
		Size: 77.7 KB (77653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc10d950639f6496530ffbb9564221ac7d68432a68e478476bdd1fc2c36f894f`  
		Last Modified: Fri, 05 Nov 2021 20:40:12 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee152a967c533103b53c3d0c41002cdf43c1f3e5fdf21530758969613415a56`  
		Last Modified: Fri, 05 Nov 2021 20:40:30 GMT  
		Size: 185.0 MB (184951598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9945c0b1e3fa8f5b68260fe1478900cafa024b5d66dd6663d1c40e9c6080050c`  
		Last Modified: Fri, 05 Nov 2021 20:40:12 GMT  
		Size: 89.5 KB (89534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de21411d8448597752e512fc993efe2ca3b4395b0da418de0454dcde23f1c29`  
		Last Modified: Fri, 05 Nov 2021 20:40:12 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
