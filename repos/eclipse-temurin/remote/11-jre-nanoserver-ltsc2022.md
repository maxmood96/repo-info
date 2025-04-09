## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:24963a38f22d3bd6eaa1ad2357b80d50245762e1e8536ed533e8102fbd97cb8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:cc78670bb30370d849f31e826f1d479eb2fde05b2ca9f6608915b5231b623c98
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164584768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ee55253aa03bba529247d7c1b9ca1e6788cff8a9797eae1a941816a1d9ce38`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:20:38 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:20:39 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 01:20:40 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 01:20:41 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:20:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:20:45 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:20:49 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Wed, 09 Apr 2025 01:20:54 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a33cdbea6e791dc3f830388d2f1cf828d3d8714ef703798b26e27dda9c489ac`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d1b936f97399f32997b0a18589d162b1ce5337d6393c1891635760eab9446f`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39629e246afdf18a62d855e1194c2c4c3a9f68a4f819b961dd603eef600a2ebd`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f03ce397c520a7322e1405920da0f677e4e113cfc1e657f0bd79699da3edbc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d23173c73b056b3e4cf8da67d8cac4b914431d018e513895ad6330f53817a`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 77.0 KB (77015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefe062dbc626c5bfc7f583839a592ec1ae4e757fe82ef3d93c652b44858d471`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab64173e5836ef45556affc5671e72cd3680c2e3015db5cf3daf3a8cecd0add`  
		Last Modified: Wed, 09 Apr 2025 01:21:04 GMT  
		Size: 43.7 MB (43656484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40681fc9723444240b4da9662c4f81a397778e046874639187ab0d6914586f7`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 109.7 KB (109744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
