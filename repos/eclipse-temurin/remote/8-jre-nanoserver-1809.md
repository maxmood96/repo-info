## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:df044e1b435530b3886a0ccf343968550a6dfda20af994b84ffcdc0af3747986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull eclipse-temurin@sha256:3d48d0e5407a094526522a85b0f1475fbda990e9a265ed62e8bb48973c8fc788
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142678847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b6c37951002aea79c122a3e8848af061eef73922a5335fee0eedd3677dc7ca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 15:57:08 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Wed, 10 Aug 2022 15:57:09 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Aug 2022 15:57:09 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 15:57:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 15:57:24 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:01:17 GMT
COPY dir:9db60ee3ad3f16cf75b351ecd1309f1d56f486fa1a4d388cea2f63f8b51258b8 in C:\openjdk-8 
# Wed, 10 Aug 2022 16:01:30 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e311759fe52617719f0115d62283a87a02a50dec926806fd298c9773b886e`  
		Last Modified: Wed, 10 Aug 2022 16:38:41 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced15d0035dc6551025a63a9ca6ffe6dcfe5b4e9269c8eeb94e7cd34b6e68f4`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1eac95613cbcc6dda9c0c4a1c29c106e2bae07bebb33434f15f0a4e5b6be58`  
		Last Modified: Wed, 10 Aug 2022 16:38:38 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee633e7ddaadee071d586552f49204902628c75d0589b60615a84b4d7ca00458`  
		Last Modified: Wed, 10 Aug 2022 16:38:38 GMT  
		Size: 70.6 KB (70600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c811f22fbd70c603b5faf1b9616964b5efab3a3b67ca50e03555a7da1611eff`  
		Last Modified: Wed, 10 Aug 2022 16:38:38 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b408bfe50d7cc4c700daf967b6e44388b09854d7099ceacaba488a954264a6cf`  
		Last Modified: Wed, 10 Aug 2022 16:39:44 GMT  
		Size: 39.3 MB (39316382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1db8ea0a38302d96aac708e2f79b16756f892b98c0442cd030b2acaf204f2fa`  
		Last Modified: Wed, 10 Aug 2022 16:39:37 GMT  
		Size: 81.9 KB (81928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
