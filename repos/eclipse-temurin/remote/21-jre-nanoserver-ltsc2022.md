## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dd858a4cbaf7189464badea565ecb8242055dc0f7f604d2ab818dd3a3e97349e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:3fbecbc87a4dbad24ea117d0b392ff1400a5a06b02fef27055a5630cd56c1699
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc8b26fbd1cc94e15422845ffe374c7322308ce5c8f0a955e82b2e205a3720d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:19:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:17 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 10 Sep 2025 22:19:17 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Sep 2025 22:19:17 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:19 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:19:23 GMT
COPY dir:1d2e38188fefbb829677ed8e6106bab9aec7034078d0a523158404f660841581 in C:\openjdk-21 
# Wed, 10 Sep 2025 22:19:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb71ee99ae4fbc59387ca62eb1803d115377382e754dfbfe33d34ffe86dee4a0`  
		Last Modified: Wed, 10 Sep 2025 22:19:49 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3beaba365b46fdf17ffbcc791b2ce0df88413e79aea14f50fa85b8ee06b7dc4`  
		Last Modified: Wed, 10 Sep 2025 22:19:49 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54deefd05ce00cb29e0dc9ffce5e22e7c52c2d51762a3617a5235b4bfbce2515`  
		Last Modified: Wed, 10 Sep 2025 22:19:49 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eba74b03c5dc2e4d413c292e21d5efb609b6bd704443e92f2c72da7b549af5`  
		Last Modified: Wed, 10 Sep 2025 22:19:49 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6051fbda16a644dc8cb8e34cdb6e605dfeaa17042c9b4559fdd382d5295b96d6`  
		Last Modified: Wed, 10 Sep 2025 22:19:50 GMT  
		Size: 76.9 KB (76857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342a707e419e7d4de5b718e9d7459b552f4e599c3319f23bb3f3b6976c966c59`  
		Last Modified: Wed, 10 Sep 2025 22:19:50 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d59abf1b98a8fc7186790133b2ae04acac464b1786f0641f99cf56aea17e9a`  
		Last Modified: Wed, 10 Sep 2025 22:19:57 GMT  
		Size: 49.0 MB (49011464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701619fe7fa5e37ebed645f30d11e7baecf3c92fe4c09f95a3efa3c856541818`  
		Last Modified: Wed, 10 Sep 2025 22:19:50 GMT  
		Size: 90.5 KB (90515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
