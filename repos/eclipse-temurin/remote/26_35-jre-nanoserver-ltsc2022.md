## `eclipse-temurin:26_35-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:38de90fcd818e67746e9e212127dcfd679a469789b7c5e6bf043a8d6ba53f6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:26_35-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:00df1580dee9360844e3c3d149cf380fc7b5e636d4839a603f7ff4d6e75c83c7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187127272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a1393d9b8c3f4ced387e72ac16a3b3ada806a291a032bc242c886a3570b946`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Wed, 08 Apr 2026 18:16:42 GMT
SHELL [cmd /s /c]
# Wed, 08 Apr 2026 18:16:45 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 18:16:46 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 08 Apr 2026 18:16:47 GMT
USER ContainerAdministrator
# Wed, 08 Apr 2026 18:17:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 08 Apr 2026 18:17:08 GMT
USER ContainerUser
# Wed, 08 Apr 2026 18:20:01 GMT
COPY dir:45edd54e05e2fb7ffc611e6ef0c2df37aa13ac9c3c9a476003fc542e9ad17481 in C:\openjdk-26 
# Wed, 08 Apr 2026 18:20:07 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c52e8dc7185acdf335f3e66a4717a90b37648943d2b2a62e58ac7fb994854cb`  
		Last Modified: Wed, 08 Apr 2026 18:18:36 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c981a6f75f9ed56a17b30f4ad0d927abacfb8b22b4f1afb6524e8ea30c026316`  
		Last Modified: Wed, 08 Apr 2026 18:18:36 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8619d6b7f5e7af3351c34b725959bf0183e9058375dea5a8142b3207ab8d4880`  
		Last Modified: Wed, 08 Apr 2026 18:18:36 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b17064cde33ad8eb5a19f7de5af5b266a60638019c915532c8865f9724a7a57`  
		Last Modified: Wed, 08 Apr 2026 18:18:35 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b982e7e2760363f18c3dead1835ea7a7e60fd85e7256482c93a57c01b81f38`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 84.9 KB (84946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d31be68e33cfbc0cdd9001fcd3a3b8bf53e62a516e7ab6e2f06cc929a078fa`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bace4768cd1804694ae365d054f908bdcb881addf972740e614874d69c239f`  
		Last Modified: Wed, 08 Apr 2026 18:20:22 GMT  
		Size: 60.3 MB (60266607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0710f7c33f7cec0084b6e012ca86fa857da63331e7dbab31c6260e5e0fa4c`  
		Last Modified: Wed, 08 Apr 2026 18:20:14 GMT  
		Size: 119.9 KB (119913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
