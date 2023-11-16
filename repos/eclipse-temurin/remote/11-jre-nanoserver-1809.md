## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:578e32fc65fa7060c8958496ad8c07d76cd6c1c44ae87341c176de3f8ef8128d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:b4f3633f1540ff801b399121a787736acda0994d7538264970d8104ef1409f8e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147988670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b862c43db8151f3ebb9c4fd55483ab00de631d00a9423e5afc97e60464c76857`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 01:51:25 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Thu, 16 Nov 2023 01:51:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 16 Nov 2023 01:51:26 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 01:51:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 01:51:38 GMT
USER ContainerUser
# Thu, 16 Nov 2023 01:56:37 GMT
COPY dir:32725fa0f7edeee10e8937816f70b588636369ca6a0eb68560cc5c3b2b3f76d9 in C:\openjdk-11 
# Thu, 16 Nov 2023 01:56:47 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4310155f8eee56b296d809c0b64c304b9eb3a29e2f1d02624f32c177cea95882`  
		Last Modified: Thu, 16 Nov 2023 02:30:49 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650e34bd545b29edcc2ae1affdae2a78a27f414d2209a19da4dbc369bdcbb686`  
		Last Modified: Thu, 16 Nov 2023 02:30:47 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99cc8499cc732cad3ae9183c5dbbbfd8108c86124844783a2b2593c0e3e8f6d`  
		Last Modified: Thu, 16 Nov 2023 02:30:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97ecbccad5d7f6feacf54e359e81a90cb90b80773cd9000e04b3ecbc011b51b`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 68.7 KB (68689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af0fcd14761493fc6db7fc3e0ee0a2aa3f69e8c62004c86ffb367b875a276d2`  
		Last Modified: Thu, 16 Nov 2023 02:30:45 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e2cf60de3c1aa8beaed173167851d2e8b74e60c682f522875ebab53acb067a`  
		Last Modified: Thu, 16 Nov 2023 02:31:59 GMT  
		Size: 43.3 MB (43335807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d0fa7078cafd5b563d756bb8bc47d13186da95215b95f766da215d5594facb`  
		Last Modified: Thu, 16 Nov 2023 02:31:52 GMT  
		Size: 81.0 KB (81012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
