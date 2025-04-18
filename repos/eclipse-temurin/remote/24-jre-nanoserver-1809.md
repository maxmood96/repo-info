## `eclipse-temurin:24-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ae344cafbc93a31ca8c869b4dbf470ed44017eb201a74e903027b5dd51fbf43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:24-jre-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:d321487f705806591313728b448755c9683dc4c2e6ff738e96dc8de70290e271
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170424024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2325ded6a0aa9ba0e3899d3c5bb18408c07c8d35983e5f0ae46da0c82a14f929`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:21 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:23 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:17:25 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:17:26 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:30 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:35 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:17:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0d1d2cde6a32525822fb3541394395d94c195b46050e9feaaea5e2403d77eb`  
		Last Modified: Fri, 18 Apr 2025 04:17:43 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e353f3c125cc943456c6cb8f515955a07f73d0fcddb5de5644b74925c229a756`  
		Last Modified: Fri, 18 Apr 2025 04:17:43 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6d28f9c0b8ff013f68a60f87682646b76091afaf2d7c53e416b9fbd1e97b1e`  
		Last Modified: Fri, 18 Apr 2025 04:17:43 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a70146cfc0e9a2901839f1cc3f381ea3f1c86a943f937c3f0ffe47f550cade8`  
		Last Modified: Fri, 18 Apr 2025 04:17:42 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14096878a149676662dfd7623fcd08ab7fa224f8d90596278b1a3efccb28d5a6`  
		Last Modified: Fri, 18 Apr 2025 04:17:42 GMT  
		Size: 68.9 KB (68877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca03c4634929b2adf5d3cba824a7a692e07e2850e8a8db33dc0ab1a725ab014`  
		Last Modified: Fri, 18 Apr 2025 04:17:42 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b453066dd182cf08fff85f7a08195872cf116284768004f3276abb26b986a19`  
		Last Modified: Fri, 18 Apr 2025 04:17:49 GMT  
		Size: 57.7 MB (57700851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8e09ce66ed7c8f7231f66085f7a720ae4e964aee70d6d24e8c05db7961b060`  
		Last Modified: Fri, 18 Apr 2025 04:17:43 GMT  
		Size: 3.9 MB (3896808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
