## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8f81815a6cf916a94cad363377a10131630997319ca89bcba2fe37ed9bae0ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:ce48b4cef5ccd2538bfc8ef6d3e678f42bee0ce36c832bc4567df962a58882bd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163879760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267311b0496fcbe9b6fa3a106d01c4e41e9c9843b6a205aecce77ea1a2c5f035`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:12:45 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Thu, 10 Aug 2023 00:12:46 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 10 Aug 2023 00:12:46 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:12:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:12:57 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:13:45 GMT
COPY dir:bb977dad5ac490fa947ae016040faee9a62c080b2232e87b0466ed93d95df9ed in C:\openjdk-11 
# Thu, 10 Aug 2023 00:13:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3572ac06c9147f0946a40530f2197bb0101b82dd45b1defe04a8904a1c81a18`  
		Last Modified: Thu, 10 Aug 2023 00:30:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3585ee163e7811a248a038e7cbe6a30fddab3e7cff338299caf4fb3598c5d4ba`  
		Last Modified: Thu, 10 Aug 2023 00:31:36 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340e22b0be8b090c4dd8b95d88547278c9fcda10b561b2d80d752db7b7ffd69d`  
		Last Modified: Thu, 10 Aug 2023 00:31:36 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f709ab4c1d708fb1d441674b982b48b57c7d51b2773a9e053bb31fa1d65808`  
		Last Modified: Thu, 10 Aug 2023 00:31:36 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bc452fdcb4a26a123e0a9fdb557b435ebde27ac6e6d79fafbeed127f1bd1ec`  
		Last Modified: Thu, 10 Aug 2023 00:31:34 GMT  
		Size: 80.1 KB (80129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c839e94c1a7864547fda043ac20045a3922094eb635d20971d93ef3d14fe82`  
		Last Modified: Thu, 10 Aug 2023 00:31:34 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609e659b3dfe0001aa9bcf696791d563e7f9f0b49d07db5b55417366b75167e7`  
		Last Modified: Thu, 10 Aug 2023 00:32:13 GMT  
		Size: 43.2 MB (43220700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e55d6a672a9f7febe38d70fffae40a34ca455bc5b6aa6b6566761c35923e9e2`  
		Last Modified: Thu, 10 Aug 2023 00:32:05 GMT  
		Size: 73.1 KB (73064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
