## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:8d909fd8ef9c6a14b51953adbeaadb2cfc16fa3e8d9cc0180c2d612fb66b5f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:0ea225cc7018de4b188a48525429ad6e94ff4d1811f9fb74b3444dfc918cacfd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146771889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a35aa47bd63f02fc5db5da9d64f0d456babe4833e61e21c5b2a967193fdb10`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 00:45:50 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 16 Mar 2023 00:45:51 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 16 Mar 2023 00:45:52 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 00:46:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 00:46:12 GMT
USER ContainerUser
# Thu, 16 Mar 2023 00:51:48 GMT
COPY dir:dcd2674e91fb412db18990a7004f7a484148b702bd6de08f5ae3a3d6f6a3f6f8 in C:\openjdk-8 
# Thu, 16 Mar 2023 00:52:01 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea37c9502d3bcdbbc2eda316dd7dde5525b3c4523d8b934f5fdd7351c4340d6`  
		Last Modified: Thu, 16 Mar 2023 01:42:42 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c839e1c668b550af962755db6bc5dbda77773ff7bf2f0b6e3551aa4e9d034d7b`  
		Last Modified: Thu, 16 Mar 2023 01:42:42 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620cb44234b657aaa3604f3eed13984d197384638b5ac9b4471e430e2549e54d`  
		Last Modified: Thu, 16 Mar 2023 01:42:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bc9547dce91ba94db8caaeaf10a53946ea8a975bbb9ad529fab8913958f34d`  
		Last Modified: Thu, 16 Mar 2023 01:42:41 GMT  
		Size: 69.1 KB (69121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf8194336aa0d18a09a6ca2d7fadacb0b7661b11f336c510037feec43be8c8a`  
		Last Modified: Thu, 16 Mar 2023 01:42:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb4531a69bc464306118cbd0ef26bd09e7571cf0ce9a2f8a83203a39404e482`  
		Last Modified: Thu, 16 Mar 2023 01:44:18 GMT  
		Size: 39.9 MB (39929619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b9701de6c6a083ec8a51243d9ed53edacf042f24518eb2288406b5e663d9a3`  
		Last Modified: Thu, 16 Mar 2023 01:44:10 GMT  
		Size: 83.1 KB (83133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
