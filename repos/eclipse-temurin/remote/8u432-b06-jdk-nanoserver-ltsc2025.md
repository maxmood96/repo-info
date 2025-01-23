## `eclipse-temurin:8u432-b06-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:e4995f11d9fae71efce2e191b682da15f097e28989828d4cba26d09838a0e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:8u432-b06-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:d559f0c42fbbc9611f7dd9a094056f1a6033e8362de2be739a72269adf6f6a4b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302683071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4c07ad98b0b73a900a7478fd07d003719f25f23788126afbf0ed27165b97ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:23 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:24 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 22 Jan 2025 19:34:25 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 22 Jan 2025 19:34:25 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:28 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:34:32 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Wed, 22 Jan 2025 19:34:37 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ea404f085ba0dceea5e80685527f16d876a95dd7f08384da8fe18946dbc885`  
		Last Modified: Wed, 22 Jan 2025 19:34:43 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd90a909cadcdeec69cd4746434b3d474f839e1d61465f45134a1162ca540848`  
		Last Modified: Wed, 22 Jan 2025 19:34:43 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84ea640e8c87c286a0b3cb75b790e2f62e07c93d7da5a3ec0e907ca5c2c50dc`  
		Last Modified: Wed, 22 Jan 2025 19:34:44 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9710c3283ffab773d4c85985f173c8e2704857353a1338acc0fa16cd722816`  
		Last Modified: Wed, 22 Jan 2025 19:34:41 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0698c5bc46d6ed42cb2aac4934eea8d9d3fb431fb34e549698c6234883a52dc`  
		Last Modified: Wed, 22 Jan 2025 19:34:41 GMT  
		Size: 76.3 KB (76324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c25cef5b85ba31ec9794cd97ca526d0477e79fa60098eb9d81115de47a02e7`  
		Last Modified: Wed, 22 Jan 2025 19:34:41 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa8a9874a8bcdbc4a5319d0e4e93a35b6ae8276ace8c4997d3d9a7494423be`  
		Last Modified: Wed, 22 Jan 2025 19:34:47 GMT  
		Size: 103.4 MB (103442443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f13d6bb15db7e9919ac2256be268d122a9d8f83f2f91736412112f35883359`  
		Last Modified: Wed, 22 Jan 2025 19:34:41 GMT  
		Size: 104.8 KB (104805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
