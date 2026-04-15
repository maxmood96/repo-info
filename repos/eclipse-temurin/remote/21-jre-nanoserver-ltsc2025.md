## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:c31358cfebfac370d619cad4531ae2863f5f5c530598200e800b77b3973106c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:ee1ec4c8970d571f32ad2f440ec09debd6c37d75a5468f2af6cbaa78207f6539
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248946245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c6369af5af7cf59c4cbea3989abe0fbf989091c8c8386ef9f2e07918d6ff5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:10:47 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:12:57 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 14 Apr 2026 22:12:57 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 14 Apr 2026 22:12:58 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:13:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:13:00 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:13:13 GMT
COPY dir:60f2977da675e9d6a11be1282de5c19d751a1b21ff04571f86a073fb3e930423 in C:\openjdk-21 
# Tue, 14 Apr 2026 22:13:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9283504e7a4dc0b9369ebeee673efd11bfea17126a3b7e1ef073687a6f63449`  
		Last Modified: Tue, 14 Apr 2026 22:11:40 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a84c04a7a7fd351003487b53348bec3bb21717f745c84abf08d5a4eadbd2092`  
		Last Modified: Tue, 14 Apr 2026 22:13:21 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0bd90af5c1282bff42a07605439d017a4c2a952c26dac19c0cdd7a284f04fa`  
		Last Modified: Tue, 14 Apr 2026 22:13:21 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85eab2d91acfb104568ce6d0b722b5445977120fedbb8f2718294e19c404608`  
		Last Modified: Tue, 14 Apr 2026 22:13:20 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7bd50d66ecd9b25eeef58540fb1ddfa68a80fca4d86e89db4514ee1de9d2fd`  
		Last Modified: Tue, 14 Apr 2026 22:13:20 GMT  
		Size: 72.0 KB (72048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbab15da4f17a604ce01fb20d275fafabd987e80d33cb3c9ec40cb48fca9f26d`  
		Last Modified: Tue, 14 Apr 2026 22:13:20 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61665e2923deb8ff50d36d9b43677d9743e5293c0a67b6dc0a3c7bcedde9223`  
		Last Modified: Tue, 14 Apr 2026 22:13:26 GMT  
		Size: 49.0 MB (49039598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e95ac13808bb0f753f3f81471bea0d4124875dc1f4470c35c8674cf4047fad`  
		Last Modified: Tue, 14 Apr 2026 22:13:20 GMT  
		Size: 112.1 KB (112132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
