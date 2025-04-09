## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:3755afccf80c5705cba4a1af750f3373f0d9ba1e8c03252f5dcec8461750dfe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:1c01cbf1cce2ecc546aa0f54f029c310d83355285c09541213953a78a2c591ed
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234016561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03e099f62042f3145caf06119d0c02fbade2ed775792a2d9375aca3fac403f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 02:17:15 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:17:15 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 09 Apr 2025 02:17:16 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Apr 2025 02:17:17 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:17:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:17:21 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:17:25 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Wed, 09 Apr 2025 02:17:29 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc5ae0430016cf2cb002f46af4aaa8169fb2c5badcf5eeb49be1c7fae0de854`  
		Last Modified: Wed, 09 Apr 2025 02:17:33 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7854e35d86cd9de464b61700c307cddf64c55a53e3c5bc242e927b536937d4e2`  
		Last Modified: Wed, 09 Apr 2025 02:17:33 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bb9708f7bbd2838fa0f8bf9f95b5e184b57917c2452a6665315e3df2d5595f`  
		Last Modified: Wed, 09 Apr 2025 02:17:33 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5542e2a37df7c27297e79197c7a6b064a860a6d50f2df5d1cae8f4fc019c06`  
		Last Modified: Wed, 09 Apr 2025 02:17:32 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77786ed6f297f768d3707067cebd22955042c136166fc7fabd667cf3c5bde03`  
		Last Modified: Wed, 09 Apr 2025 02:17:32 GMT  
		Size: 76.3 KB (76328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109316969678b62c7f38b26acdc50badba9a77c28a66b90fdd106d02c426a052`  
		Last Modified: Wed, 09 Apr 2025 02:17:32 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244385b3ad35485feb3eb3c83ffdc07732e1550c86290d6265c2277033ed6680`  
		Last Modified: Wed, 09 Apr 2025 02:17:37 GMT  
		Size: 43.7 MB (43729009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c29d8f0e6c90393a9a58b6595453837d8be2005b8a182c8a3d23c1c279ac28`  
		Last Modified: Wed, 09 Apr 2025 02:17:32 GMT  
		Size: 92.7 KB (92654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
