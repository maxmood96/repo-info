## `eclipse-temurin:8u352-b08-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:00eeee40ac2324b2b8f7544210cbf95b7a63b739ef8248dceee716ed5c01f731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:8u352-b08-jre-nanoserver-1809` - windows version 10.0.17763.3887; amd64

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
