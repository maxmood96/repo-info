## `eclipse-temurin:8u352-b08-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c8000321eca74654777e374f5f168e1058514c39025266e79a8ed3a0e2ac1dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `eclipse-temurin:8u352-b08-jdk-nanoserver-1809` - windows version 10.0.17763.3887; amd64

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
