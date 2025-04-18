## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:8b5153f7283b256c8eafefa54865a25e55a1eeaf9050874b170593a19a53b61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:43f79138754db0c89d5e87ecfe1883b5189ed7f1926d3902f1de0cc69ca416c5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25984012b4bf08536b30bc6a20771f5958bf7355b74e3ee607550c7eec91a1e3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:27 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:29 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 18 Apr 2025 04:17:29 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 18 Apr 2025 04:17:30 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:32 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:39 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Fri, 18 Apr 2025 04:17:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:17:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123ca03bf2dff56b8b5c470ba5cb4fcc68a8fb61b2421ef22d88f1e3f4db21b9`  
		Last Modified: Fri, 18 Apr 2025 04:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272abc8933c8436464985b09581cf5c31265b77e51ac88850c15a82027c3ab02`  
		Last Modified: Fri, 18 Apr 2025 04:17:48 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bf44a423b36f4f4ed885426b21bc963131854a13cc5ccd783076ebc9e9f6f4`  
		Last Modified: Fri, 18 Apr 2025 04:17:48 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f09be68bf98e6dc2a27b600b8f2b8550678b37a9aa4e7e93e0866e0e4eb23f2`  
		Last Modified: Fri, 18 Apr 2025 04:17:47 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe6354d11266e423f74acc53f6f475c345debf35191ce773af725af7964eeb`  
		Last Modified: Fri, 18 Apr 2025 04:17:46 GMT  
		Size: 68.9 KB (68937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18137ef8e108148a037acc8dc3b3748abc9b339284c982def8022cc8b97f046d`  
		Last Modified: Fri, 18 Apr 2025 04:17:46 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e8f461cca167b5b0b83e0900807510af08f84a808cf5ca56f0c1ecbfe90ff3`  
		Last Modified: Fri, 18 Apr 2025 04:17:58 GMT  
		Size: 187.2 MB (187233682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3d83b2cd54ce2823ff5149894bcb73b579cdfacaee049db5105e1d9c15138f`  
		Last Modified: Fri, 18 Apr 2025 04:17:47 GMT  
		Size: 3.6 MB (3623683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a77370dac691a801f260ec1a5a527a903afc221327ac4c84fba137c24174de`  
		Last Modified: Fri, 18 Apr 2025 04:17:46 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
