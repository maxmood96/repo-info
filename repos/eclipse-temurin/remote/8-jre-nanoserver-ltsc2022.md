## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:779c260c4bb58fe6a32a42c1fe29177edb207cbeb74236bfb4bc47f4f553c8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:10e8989ea0c04030fa33368740d7d0df982d271cbfa902003601eb0637dc8b26
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161469517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd705e070a844d39bc95b23c2eac961ef715e6d947b5efc1bcacd5a4fce4d93`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:54:13 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:54:14 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:54:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:54:15 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:54:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:54:18 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:54:21 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:54:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cd5e09260c9524dadea97e28f87b14aa5d1b3a9ac02bf3e635fc2a23df7530`  
		Last Modified: Wed, 09 Apr 2025 01:54:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f08195c64d704602fd2c8bfdad632facbf35210b54c3ec5431220ed0ae73c`  
		Last Modified: Wed, 09 Apr 2025 01:54:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55da8f6efa226ebad73eb66aa55c8258c3b78656d0311cec416ab70de90e9f`  
		Last Modified: Wed, 09 Apr 2025 01:54:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9aa83f4f7622154c7573bd5f261d45f0b8622cef16eaad426ac90c70b40492`  
		Last Modified: Wed, 09 Apr 2025 01:54:27 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d579eea466efaab9fbde60edd8d7dbef8ebc8ddde7b36a01414bc69f541e50`  
		Last Modified: Wed, 09 Apr 2025 01:54:28 GMT  
		Size: 76.9 KB (76895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f902e5f73347c2f03e8c6cd73c3b3d9729b7ae93bdd59b65f3f049eea1702b`  
		Last Modified: Wed, 09 Apr 2025 01:54:27 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd6d803a131832e9d4b22065277aeb76c475b2bb3b5cf609050275c3ae9c44`  
		Last Modified: Wed, 09 Apr 2025 01:54:31 GMT  
		Size: 40.6 MB (40552174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1f51f449f8cdf70a9ae13d296330ed31151fa9f3af301e1c6920eec5229462`  
		Last Modified: Wed, 09 Apr 2025 01:54:27 GMT  
		Size: 99.0 KB (98992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
