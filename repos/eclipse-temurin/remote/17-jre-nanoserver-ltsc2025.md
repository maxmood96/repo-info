## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1dd152d34b59f2c367b71ffa9d76a2e49905c5dd22aae57f06de8995582e6422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:60d0960634335e930ec5c8afe657ec9e3d8a0d14b24f2a7a8b3d9423d414cb49
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235332057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066d1c1db517bee1ee69c0e7f3d0d9912733b11e7905f0d5f626fca0c73e2dbc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:45 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:14:45 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 14 May 2025 21:14:46 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 May 2025 21:14:47 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:14:50 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:54 GMT
COPY dir:6f6fcea1890c098492beafa1d6f550d144651035b2d4a098a7658e545737cf82 in C:\openjdk-17 
# Wed, 14 May 2025 21:14:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a7b3ff86be05ccf046e9249d9f06587f5e1e097077cb2e4d6f876f64b00e34`  
		Last Modified: Wed, 14 May 2025 21:15:02 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb3203be181923c907b7985a9a096e6ab7762bc24e7fb423ab309ff18ccaf`  
		Last Modified: Wed, 14 May 2025 21:15:01 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e6cd53fe042de505cbb6a0ca6d0fc2cf63a675e02532b81ca09c849012d6a9`  
		Last Modified: Wed, 14 May 2025 21:15:01 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2899e26c751a84f62e85834400c7f19854e515bd104cd0c103a2c25dbcfed920`  
		Last Modified: Wed, 14 May 2025 21:15:00 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be574b82940cec6c0c3eed5ef0cca9d693adc335f0fd6a2e52dec0051545e02f`  
		Last Modified: Wed, 14 May 2025 21:15:00 GMT  
		Size: 75.8 KB (75850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6655a66fe18fd74dcd871dc1d91581b6e4bbef6fffbc6e357e40404a88d6fea2`  
		Last Modified: Wed, 14 May 2025 21:15:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1637804aabf9c1f5a419c77493bc850a83ac89532dfb381597947fd78da798f9`  
		Last Modified: Wed, 14 May 2025 21:15:05 GMT  
		Size: 43.7 MB (43736602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafb0006886b1d0888b6152c452884dc86144acccb179ba72566a440dd6d6b00`  
		Last Modified: Wed, 14 May 2025 21:15:00 GMT  
		Size: 102.3 KB (102313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
