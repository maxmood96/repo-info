## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e7c692440d1dba63d4ecf162f7c020ea24daa2b8f340f286f6da6667689fc3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:d1675ff78f052f17a2423543dcdf772e982557d89fa9506e53644693cba58263
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149786277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283b65e98a5b65c82ebddad41f6bb746d08544773b60785b7461edef80d598aa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Thu, 12 Jan 2023 02:01:13 GMT
COPY dir:f12bd30467bc1b7f61ca05a6124e6eb838888f3685c56f372d6fed2165b193b1 in C:\openjdk-11 
# Thu, 12 Jan 2023 02:01:36 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:cca035f5cacd375d4b5e1ccfa35c11b91a3b056c97b66ac1252a18681a2666d2`  
		Last Modified: Thu, 12 Jan 2023 02:44:33 GMT  
		Size: 43.0 MB (42961329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5799d44edae9893e8a509c1668ea42f5dad96e2f0a9aaa7b71b661e45ad9406`  
		Last Modified: Thu, 12 Jan 2023 02:44:25 GMT  
		Size: 82.6 KB (82618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
