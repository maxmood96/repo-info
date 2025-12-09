## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a71e5caa835852fdc16c44b8178c4b76eec840c582805d1444858e51de63c56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:8401149b63ea1d4b856bc61fa85a00b347c4bb029c64d5c707ebed40ff0198c3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167079964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cef3271505978d4527dfbdcd4a1758084dcc608d28da894a5abf340723d9f1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:08 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:12:08 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 09 Dec 2025 21:12:09 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Dec 2025 21:12:10 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:12:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:12:12 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:12:16 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Tue, 09 Dec 2025 21:12:20 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e4bbd94f6866974611ee8943ff09ce009d2d821f9047398dbedef687b98c2d`  
		Last Modified: Tue, 09 Dec 2025 21:12:35 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2884fef0dfcbb8a34b34c72a255c312a373e35dd8c5192bc253b5669dfa9927f`  
		Last Modified: Tue, 09 Dec 2025 21:12:35 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79e6ba4546c674bcf11f4cfcd25cf8d548cdd7e5c488e889e8482dd930f131d`  
		Last Modified: Tue, 09 Dec 2025 21:12:35 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a2d559e6eb59319ea274f4f258e89710810adcce28e845f706a137d0558cb7`  
		Last Modified: Tue, 09 Dec 2025 21:12:35 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdcb84427dd50dc1e8b1af7635e483cc93d344ea720a827615d3c986b56adce`  
		Last Modified: Tue, 09 Dec 2025 21:12:35 GMT  
		Size: 72.1 KB (72079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7488d5a1ef80e820b0673525075e161f3b6435dd55bafe71b2b56dcb91774a3`  
		Last Modified: Tue, 09 Dec 2025 21:12:35 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ad170022770c081c0329e78bb5f571a1927492b1cac3e29ad2554839d68222`  
		Last Modified: Tue, 09 Dec 2025 21:12:39 GMT  
		Size: 40.6 MB (40555152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d143250dbcc57cef7c5624e4e42466568ab2d49696839dba1b4c2269383a72`  
		Last Modified: Tue, 09 Dec 2025 21:12:35 GMT  
		Size: 89.1 KB (89098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
