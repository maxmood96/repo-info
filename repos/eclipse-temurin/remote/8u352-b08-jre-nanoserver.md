## `eclipse-temurin:8u352-b08-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c587cb7ed0c2d8e4dc0572ff4f9fbfa6e4fbbfbbc03fd6349d0b2a2751082f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:8u352-b08-jre-nanoserver` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:700aae79831cf67a8ca2924444fcf9e54365446aeadea5e848c63149eb604ffb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161575055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9294708b667a034e242e63c675e9bebad2d7a02de81d780ddeb46f075cef966a`
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
# Thu, 12 Jan 2023 02:21:09 GMT
COPY dir:4e862dd3e9e3173048336ba652726d009cc7bbbadd67bc711cdb421cf611c5ab in C:\openjdk-8 
# Thu, 12 Jan 2023 02:21:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:5b39ce57c0577970f740f33a4be28df220fb048dcba921dbaac23fdfdfe9fa9d`  
		Last Modified: Thu, 12 Jan 2023 02:51:23 GMT  
		Size: 39.3 MB (39323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b719332cf750f59ccb18b7d63b2cc8b31ca1167457431a2841b874127a65fb`  
		Last Modified: Thu, 12 Jan 2023 02:51:16 GMT  
		Size: 58.7 KB (58689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u352-b08-jre-nanoserver` - windows version 10.0.17763.3887; amd64

```console
$ docker pull eclipse-temurin@sha256:d92d533c2f268ad732709843963fa255600d6d4a2aa3611d4f3f4c03bbddf1ad
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146183451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10cc61ee617057048515bbd7edff0b902519bb71b9a8ddd5b01ddd40625f2c2`
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
# Thu, 12 Jan 2023 01:50:37 GMT
COPY dir:4e862dd3e9e3173048336ba652726d009cc7bbbadd67bc711cdb421cf611c5ab in C:\openjdk-8 
# Thu, 12 Jan 2023 01:51:03 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:0b2962fd655e0884102da4dc7aa00c3c2cd71bf925a39c3dd52d160b4c08a67a`  
		Last Modified: Thu, 12 Jan 2023 02:41:36 GMT  
		Size: 39.3 MB (39322702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72368fb870a2a8a2067a143a5a2deed680b955f5b3fb63fc2ccef75b014f0736`  
		Last Modified: Thu, 12 Jan 2023 02:41:30 GMT  
		Size: 110.9 KB (110895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
