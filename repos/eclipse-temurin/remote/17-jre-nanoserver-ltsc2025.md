## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:3c352ab45f1a8b303aee53afef4e4adb1ea545dd08e43328805637bfdd91101b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:be0aa9ff13e53e7ede00a767551d68ae09c86322ee0e74c117199943da4f6d31
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243742007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3541eca464782a064cad584e998b71b580ff08cd5fae154ea29e1a7328e45330`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Fri, 08 May 2026 00:18:41 GMT
SHELL [cmd /s /c]
# Fri, 08 May 2026 00:18:41 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 00:18:42 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 08 May 2026 00:18:42 GMT
USER ContainerAdministrator
# Fri, 08 May 2026 00:18:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 08 May 2026 00:18:51 GMT
USER ContainerUser
# Fri, 08 May 2026 00:19:04 GMT
COPY dir:2f70d7e82fbe25185baf6a6b1e05b870cb38c3ad05aac5b5932c695a93320f91 in C:\openjdk-17 
# Fri, 08 May 2026 00:19:11 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165902819274ecf59f65439cf0040e76b39d032e3f1d6916573397eccf9ed613`  
		Last Modified: Fri, 08 May 2026 00:19:22 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89da7f30358ecf153bfe84c998cfa8a4b8b9b725c1344830af932a301054b51f`  
		Last Modified: Fri, 08 May 2026 00:19:16 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d53928356d54cd50d636870c0d885ba5d47a96745ca8449884919bbe25cd4bc`  
		Last Modified: Fri, 08 May 2026 00:19:16 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83afcaad3f5116da8c0f41422a2efdf4f366f98f1d7730db82a59d2e9c76bc83`  
		Last Modified: Fri, 08 May 2026 00:19:15 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c92a5ce7f1e3aef2c1335b24f626762cdf731d7a336d1fe13ecaee5180edab4`  
		Last Modified: Fri, 08 May 2026 00:19:15 GMT  
		Size: 71.7 KB (71666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a708e59709f59a81ccf2454a1ac512fabc94ffc28917200de2addbe27bb9a7`  
		Last Modified: Fri, 08 May 2026 00:19:15 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff31783391b5f6dff590f1a72f804ab84e5a326ba530d6d73fc53fbb0e2cc026`  
		Last Modified: Fri, 08 May 2026 00:19:21 GMT  
		Size: 43.8 MB (43834304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f55bbe11e52aa07ae242a3cfeda4934c2dce9985adc6c5760c0c2d0a2832e8`  
		Last Modified: Fri, 08 May 2026 00:19:15 GMT  
		Size: 113.6 KB (113617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
