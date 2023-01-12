## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:bc48493300ada7aec88dc75172cdf560f3927ea9ff5552697af21d3eb23b5d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:987dfeb11c51813a0c564ecb2a6e3d2df1f77992422f7e3e35b77544308ec703
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.8 MB (222756315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63fc31bbe7f3b46824caf4737164dc980c703a01223835fa0554f605f57b403`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Jan 2023 23:36:49 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 02:19:48 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 02:19:48 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Thu, 12 Jan 2023 02:19:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 12 Jan 2023 02:19:50 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 02:20:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 02:20:14 GMT
USER ContainerUser
# Thu, 12 Jan 2023 02:20:26 GMT
COPY dir:3f9950b949d84f617218d6370bf5d9344385a96fee23c5d0245f1523c4ce092b in C:\openjdk-8 
# Thu, 12 Jan 2023 02:20:55 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:83e9437e818022c1c28f0e07002dd46995c8614e62b9366138fa23b94f43d9ad`  
		Last Modified: Thu, 12 Jan 2023 02:51:06 GMT  
		Size: 122.1 MB (122099566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbebbf572ebe7984b715b8dfe99bc1273403a831c0079b95afa12162b7266f16`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac7d468bdb6a099795ee184e23d7c26764a8e451ec0477faec012ae08ff63b5`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdcadd904c8aa3749640e7e5de4ca50b3f0a2afafbf20eecfa5c32ed84ac24b`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78325accf82cc30e1a1cf2683c75b74be6551a4ddfa229082958effb18b94d72`  
		Last Modified: Thu, 12 Jan 2023 02:50:36 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fddfac47d5b4f83760df7fc4954f4419a399914dbe8d8455c83e3ee7b76e86`  
		Last Modified: Thu, 12 Jan 2023 02:50:36 GMT  
		Size: 87.8 KB (87828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483c6db44e09d3f3f97e05de8cbf54ded06c9f8d9cdddc65b7f941587e1f5f73`  
		Last Modified: Thu, 12 Jan 2023 02:50:36 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e3cfa0c7fa5d47b5024756f605eacc5c2af4abd961331f08114e1f05e6f03c`  
		Last Modified: Thu, 12 Jan 2023 02:50:52 GMT  
		Size: 100.5 MB (100490059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99744c2c9534069cb2d2846236ec9df53d0c957a2f2ffbda784e09f657869373`  
		Last Modified: Thu, 12 Jan 2023 02:50:36 GMT  
		Size: 73.1 KB (73053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
