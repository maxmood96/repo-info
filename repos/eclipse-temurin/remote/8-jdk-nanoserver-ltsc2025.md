## `eclipse-temurin:8-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a0e18c380bff1742d33d152d13de6929f912fd446c9b04a536970c6e8d1f66f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:64e2192048beba33124688914d88662860bcfe3c3fb55434e78c7cf7a455168f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301522161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdd0fb594231f457383b4a0e72a6ce64463ff7ea254965c3cbbdd2cee238a22`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:40:46 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:40:47 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Mar 2026 22:40:47 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Mar 2026 22:40:48 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:40:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:40:53 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:41:06 GMT
COPY dir:076949d8a0679d24528f11c4150b1ea7a552717f0bf1fb11a9fa610f7e5e2ea0 in C:\openjdk-8 
# Tue, 10 Mar 2026 22:41:11 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf6224cd21bf161844346f3025994c2e26638f08f91e12dcda3c0bb82cc0a5b`  
		Last Modified: Tue, 10 Mar 2026 22:41:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4581672c9360ce656a683d6e1bf5396f306a704d3372208ef548956b63b21f1f`  
		Last Modified: Tue, 10 Mar 2026 22:41:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a067f2d8dc696fff14269fab0c528bdce2e54cb489fd4b53b74ab7b8e3841ca`  
		Last Modified: Tue, 10 Mar 2026 22:41:17 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7b76e06a7d85e26cb0149457536bd2ef3abf7719a6ac246d3cb67cacaff57`  
		Last Modified: Tue, 10 Mar 2026 22:41:15 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603bea8a1d4b25cc29c92021d0aa2033f1529abd7618f7fbdf25bc3301490fb2`  
		Last Modified: Tue, 10 Mar 2026 22:41:15 GMT  
		Size: 89.3 KB (89344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0b1680ae173e21650423320098628e3a0e5b97d81b39a41ec1a02a573c0164`  
		Last Modified: Tue, 10 Mar 2026 22:41:15 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dad3725d26fa37c807b370eb36dec5df1ea1773e6bdb3b359379a12d60ac2c`  
		Last Modified: Tue, 10 Mar 2026 22:41:23 GMT  
		Size: 101.9 MB (101908823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2dc77f01259dc13cf238eed9f8b41ab4e2972c548025ac06708bde94381794`  
		Last Modified: Tue, 10 Mar 2026 22:41:15 GMT  
		Size: 109.3 KB (109329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
