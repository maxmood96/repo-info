## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:404fb3963689e1041da1cee0ff544d76a6d833ab6f393fb04dbf7bce147461f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.1487; amd64

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

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:866c96fc0d28a30ca5a7428e5469f3e2e46e274aa09dea93105f71e0c12b01c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207365807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdc7a7fbb36cbdbdc0d763d69e39e5dbcafd041c59326ee152d1a981a9fbf0d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jan 2023 05:17:01 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:45:31 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 01:45:31 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Thu, 12 Jan 2023 01:45:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 12 Jan 2023 01:45:33 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 01:46:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 01:46:08 GMT
USER ContainerUser
# Thu, 12 Jan 2023 01:46:19 GMT
COPY dir:3f9950b949d84f617218d6370bf5d9344385a96fee23c5d0245f1523c4ce092b in C:\openjdk-8 
# Thu, 12 Jan 2023 01:46:55 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:f70ece9aa5dba4a420fbe5a19439965c2a9d6ab9fada0c7c0a6308b2545f8246`  
		Last Modified: Thu, 12 Jan 2023 02:40:16 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9cb5df8142abf75041e5c420128ed72188c90e0b13f9216e08f06df45b65b2`  
		Last Modified: Thu, 12 Jan 2023 02:40:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40b495656e2122c2234505da38597c31a65e067e0e8edd86eae58be1fc6e72c`  
		Last Modified: Thu, 12 Jan 2023 02:40:14 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b0c0d712f017a285a01483f43c34980673f728f3115d140387ea3b4f2c3828`  
		Last Modified: Thu, 12 Jan 2023 02:40:14 GMT  
		Size: 77.9 KB (77876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13eddb10db3e86cc4de1a423bf8a43ee4e003c32ec89b52d08031042666b81ef`  
		Last Modified: Thu, 12 Jan 2023 02:40:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30fd34750b9000e8becb59e42a96d41615916fd4e400c3b21781e096d7223863`  
		Last Modified: Thu, 12 Jan 2023 02:40:31 GMT  
		Size: 100.5 MB (100490298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c3f72c6c3b489dffbbc3a5e98f244320ffc2f0db7e1d8285ddb6ec9d25ce1b`  
		Last Modified: Thu, 12 Jan 2023 02:40:14 GMT  
		Size: 125.7 KB (125655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
