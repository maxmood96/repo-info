## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:6ca8e65a7ff92b2bab4f8d864cc079eda632ea1fd5bcb5b027d621dd22cb7f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:65c34183bb3f9258d2897300201abad7dfc20dd93f7ed4a92771e43b643c2e53
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243539797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74aa88be85581178eccff103d5635ccde5d4a28b154803bed2d13a9b99fbca`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:19 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:20 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 22 Jan 2025 19:34:20 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 22 Jan 2025 19:34:21 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:23 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:34:26 GMT
COPY dir:a15dacd11bbcaacf83a6b6e1490d6483ae4af68a125407fd4cb6bb7a70e4639c in C:\openjdk-11 
# Wed, 22 Jan 2025 19:34:30 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b98f3d20c41eee1e23fd666adfc9c6967631a8a6e0aac6ff7d46224130ae7c`  
		Last Modified: Wed, 22 Jan 2025 19:34:34 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b0fc3eed3b7cd82e1c4ac8319b41336b6cda5ceca8f801d2d1ad4406ba0ec`  
		Last Modified: Wed, 22 Jan 2025 19:34:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9faef4a9223fc180b11d35c158906df85e19b5388ff10d7c6e1bc4cedbbb78`  
		Last Modified: Wed, 22 Jan 2025 19:34:34 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a2abbb0137ae8cf73efd1c7d2c2b950d24b1d0559f49217d94ff7a6db4cd02`  
		Last Modified: Wed, 22 Jan 2025 19:34:33 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b77f03388bb961ec959e592156acc7e768d9963ce0368400b5cb80f2ea769c`  
		Last Modified: Wed, 22 Jan 2025 19:34:33 GMT  
		Size: 75.9 KB (75914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d0ee671a41f56295f7cbc02ff1bd9564cc362116099bb0a875c085e4d12fa8`  
		Last Modified: Wed, 22 Jan 2025 19:34:33 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d5deef7959c55d21de8ff4cd9c0b037c46db89847a50aed2ce8e82e8492b6b`  
		Last Modified: Wed, 22 Jan 2025 19:34:37 GMT  
		Size: 44.3 MB (44309513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b1a33a7b430cfd19fa978eca0dea76acf87ec96688888662ad3dc60ebef2e`  
		Last Modified: Wed, 22 Jan 2025 19:34:33 GMT  
		Size: 94.8 KB (94813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
