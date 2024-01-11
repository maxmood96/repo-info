## `eclipse-temurin:8u392-b08-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:57eb5507efab24b4d265dd6672f3e97e76d639698d9612670be246f8b86ac7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `eclipse-temurin:8u392-b08-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:a4f5a01f981792ddfc568fb7106046c0331344ecdbea92b448b59957f46c26d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222635469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5434b52e892d817694ced35baf547dfd6f55456f52a31eb4c85067b2cc81e383`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:17:07 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Wed, 10 Jan 2024 23:17:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jan 2024 23:17:08 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:17:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:17:23 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:17:35 GMT
COPY dir:d9c44d909d2b41aad5bf6fa4f7c7d36e81063822ae5e7ef30e4851bbe7809503 in C:\openjdk-8 
# Wed, 10 Jan 2024 23:17:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8628ad7aa058ffb12fa3ef62904fd96d1ef4b84c45f7b942775a6ae02a830eb7`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b604f3ee0869ea0719f02c17eac778b3b2e716757ac449ba79ea5b654ddcca7`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8240708d47924cf34a43fb95c84a9f970eb54178ae1825f974cb9e894e03f41`  
		Last Modified: Thu, 11 Jan 2024 04:18:55 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650656b3a0668e024e51fca51fc22124e405ce5a0090747a36498c399156a918`  
		Last Modified: Thu, 11 Jan 2024 04:18:55 GMT  
		Size: 94.2 KB (94221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59fc61beb41f45677b64051f9a23fe2b986c84b8e9014b2162ffedae722ed1`  
		Last Modified: Thu, 11 Jan 2024 04:18:54 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47f3f00c9a52dc0e25b96e5170b25d2a3cd941da502dbebff6b4880124fe144`  
		Last Modified: Thu, 11 Jan 2024 04:19:07 GMT  
		Size: 101.7 MB (101693938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572b2ccb25562c5861e63118b71bf877a015e9644cb8b327073200c13c9b01f5`  
		Last Modified: Thu, 11 Jan 2024 04:18:54 GMT  
		Size: 72.3 KB (72273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
