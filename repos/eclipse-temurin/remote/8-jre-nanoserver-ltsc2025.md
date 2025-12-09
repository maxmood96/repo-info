## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b13cf08b1f77a8d49e734afc4eb8b4f9fa2b5bc01294dd668281b6f51265c105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:4022d0e58a65aebcdc75a7c159550f078a5530c20f665e7a56358e802e627853
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239599429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ddb2bc01a057b8f5d634aa4d7af5d2af670286275b1588dab2c890b1cb31c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:12:53 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:12:54 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 09 Dec 2025 21:12:55 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Dec 2025 21:12:55 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:13:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:13:01 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:13:08 GMT
COPY dir:d46ae848a780de83988aca6679aeefb6cb592f306ae2eca344ddb66bc6559a89 in C:\openjdk-8 
# Tue, 09 Dec 2025 21:13:11 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3aa2fd9c43d5870304ea449c22f4fbf73f16c064a13e04297c92a2a200461b`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a84791a5302372ac1f5175231260a7065468b14a2615ba832f7501681b299`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5991b916d86531dcc9647e67a0536c3abbdd902ecf55d80aafd6bb0ca663904b`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4d530a6c60d5e4761e3649337cabfc83fa669955032022ba1a5bded852582e`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934014fb7c3a6e7444b514d76db0ec2bce2b4626e4fe34d15c7c72bcc89ba2ee`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 72.0 KB (72006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36669f76c27756eaed2038dc3127e39456f397b4eeacf306aac778f34e52547c`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1a4def0b2580735bc537e237574ed99a9405bc2b84e4e9d69cae0cd64918c0`  
		Last Modified: Tue, 09 Dec 2025 21:14:13 GMT  
		Size: 40.6 MB (40555198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3b47e4bc1903de20c1f5daaa0bd475e2726c1e86abca212632f779537b1255`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 93.0 KB (93017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
