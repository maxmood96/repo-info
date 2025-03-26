## `eclipse-temurin:24-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:3ec82d67d218e6a84bb6afc58bf4019dba2c0abe6e75b9a3411c5d5b819e9640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:e8cb80cff1cf0f787c8e4e046fe1407eb6d6083d38670ddd43a12f7a823cd6e3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264178185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b8f0b9f48ead99709caf89f3be43cf39ca3bdc85b57f17e3ebd0152044ea51`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Tue, 25 Mar 2025 22:12:51 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 22:12:52 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 22:12:53 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 22:12:53 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 22:12:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 22:12:58 GMT
USER ContainerUser
# Tue, 25 Mar 2025 22:13:02 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Tue, 25 Mar 2025 22:13:07 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb647fa7ed2635f43b536686a3e62e23c2090b29ce299c11f569bf6962cb8708`  
		Last Modified: Tue, 25 Mar 2025 22:13:13 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b09f0e264b81c0bafabbeb8e28067bf297d70dd69746bf0cede6003ba7849d`  
		Last Modified: Tue, 25 Mar 2025 22:13:13 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b479da94240c95456a32c253fe0676639a0a567b63f9e7a3a9c0fd16a080f7`  
		Last Modified: Tue, 25 Mar 2025 22:13:12 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012e843b677f712576f9a0c643ef15ed60e4b60658e535763aaf42322db00283`  
		Last Modified: Tue, 25 Mar 2025 22:13:11 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2232ab6250a0f6d93e0beadcb80e37e325c53cd1636ffb7462f769c4be77de78`  
		Last Modified: Tue, 25 Mar 2025 22:13:11 GMT  
		Size: 76.0 KB (75987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1519959fc5570a9ba256420794eecd8311a22dec5d3e6472e4187404bf7ff887`  
		Last Modified: Tue, 25 Mar 2025 22:13:11 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ed35eddd4406e44359c490bd809ab860fb848a0bfddaf665406c2c5771f0c7`  
		Last Modified: Tue, 25 Mar 2025 22:13:18 GMT  
		Size: 57.7 MB (57701308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cd84de29d2b62c6a59b3bdccf7742bf657a1b03918bb60740423f8ecf96cd2`  
		Last Modified: Tue, 25 Mar 2025 22:13:11 GMT  
		Size: 93.4 KB (93399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
