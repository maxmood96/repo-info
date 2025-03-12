## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b991032693753a45a1781181bdbdd114da407594a870b2ec155498c21050de99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:ec1e9c2f72bb6857549daeb9632f3a6a6b11e2ebc7a4630c8d3de732f77f806b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164530042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376d59dbf377144ee5bf1c01e197f61c9ed6d6904d13e5b5715a24cbbd08d1f0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:22:23 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:22:24 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 19:22:25 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Mar 2025 19:22:26 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:22:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:22:30 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:22:34 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Wed, 12 Mar 2025 19:22:40 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6d5dd241c8df3723b88d96edddc785749f178487ea32ca46ada88de836d52d`  
		Last Modified: Wed, 12 Mar 2025 19:22:46 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850270c6e1c4907e8b2729f6ad7652e380fa8e818fcc3894575aa4fff5fc5476`  
		Last Modified: Wed, 12 Mar 2025 19:22:46 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87572e3e2fa6739e4c98d68b0d3b9c0a86258465b497da6281a1a0f2e7e959e7`  
		Last Modified: Wed, 12 Mar 2025 19:22:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b01b46e5a9ff6e2107469a1a0eb0068340b5e52f1207d57d76a2fd7f1c4483`  
		Last Modified: Wed, 12 Mar 2025 19:22:44 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f6bf87869c53842866b1e238c8bf6c629e87f9cdd22508dd3cfd67d1b5cf19`  
		Last Modified: Wed, 12 Mar 2025 19:22:44 GMT  
		Size: 77.8 KB (77842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6676ca6b6a112c0c383a1080f25445e1014d629b9edc56bbd82d6147e3780e44`  
		Last Modified: Wed, 12 Mar 2025 19:22:44 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8242cdc3d95740d3e34c2b22214796cbab9b3a068896d6e653e0598bf54c248`  
		Last Modified: Wed, 12 Mar 2025 19:22:49 GMT  
		Size: 43.7 MB (43656609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a356a43510ebead6f228a02ff0e5f667d15265cc023ab8db5dd976e4718feed`  
		Last Modified: Wed, 12 Mar 2025 19:22:44 GMT  
		Size: 94.7 KB (94737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
