## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:5be956156202e95227e6e88dfc496e522544f3a8625e402d881bb24652e5f5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:aff2d0760f8b5296b90a188d92783b8b85089ce6e15d1f510c51ec6bc1722f64
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299358174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9922eace97c546712b8cb9f82dd1026b85cbd7a5b4271e01cb1877b8b68b8054`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jan 2023 05:17:01 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:45:31 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 01:55:54 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Thu, 12 Jan 2023 01:55:55 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 12 Jan 2023 01:55:55 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 01:56:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 01:56:36 GMT
USER ContainerUser
# Thu, 12 Jan 2023 01:56:53 GMT
COPY dir:cba9eceeddb80383417f5e5518328c343fc4183981a343fca253ea7c2e4dfda5 in C:\openjdk-11 
# Thu, 12 Jan 2023 01:57:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 12 Jan 2023 01:57:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e58f9ad3b15a2a4882ab0a845e8e619cc8c3c411ddbe8b50046c1618a95c1397`  
		Last Modified: Thu, 12 Jan 2023 02:40:44 GMT  
		Size: 106.7 MB (106666138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea67a6bd980bdee35399883e5abcc31c738b338ad384b2f92d91a15cf09d9df`  
		Last Modified: Thu, 12 Jan 2023 02:40:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356d3317b2a7acbe0a2a9a3022ac4397679bf492de573878440a80997d915346`  
		Last Modified: Thu, 12 Jan 2023 02:43:15 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5a0d3b0e4ea5059b336e25d0fb94d76679f98c2d13906c7ea5871bda51123a`  
		Last Modified: Thu, 12 Jan 2023 02:43:14 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e7492a4d04bdc9f503ece8d8615060675e9043ff48f4c32c7760dba97f0e63`  
		Last Modified: Thu, 12 Jan 2023 02:43:14 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9913467b8967df9aca92ff94d35b0a64fac8c3d9d4674f5df8a85339f3d569ed`  
		Last Modified: Thu, 12 Jan 2023 02:43:13 GMT  
		Size: 70.4 KB (70363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e5e475e925acef2f85e2b7084a75cc0194d054deba4897f6f51384387b50e1`  
		Last Modified: Thu, 12 Jan 2023 02:43:13 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef17b41c48867186344c8570ae674d511ca0d5e56a6bb98213656823e9eff47f`  
		Last Modified: Thu, 12 Jan 2023 02:43:35 GMT  
		Size: 192.5 MB (192522334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed39b16781d938dc8a1fba00c39a9bcd332afdf42bb5203d9fc7e9f6b6456839`  
		Last Modified: Thu, 12 Jan 2023 02:43:13 GMT  
		Size: 92.4 KB (92376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0031b28257dfdbdb7b4f54d060eabe4d712a20ffb91754d804728c058721f31c`  
		Last Modified: Thu, 12 Jan 2023 02:43:13 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
