## `eclipse-temurin:20-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9b10e078a893172ebed1797e6917a854e927f984767ad620705d03a1660934e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:20-jre-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:fe92ba10ce2db30bee9a41e7403aa20526eda98105017139733281f59d74634a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153549942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983ac3091e237ab06268c8a510b7523dfddbe5f10381d23a3729f1b2e80236d9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 02:29:44 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:11:56 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 03:11:57 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 13 Sep 2023 03:11:58 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:12:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:12:10 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:18:26 GMT
COPY dir:7e69bb3960973ab39fc2ba0552343e70b32506a25a841e69600e9c49be1d11aa in C:\openjdk-20 
# Wed, 13 Sep 2023 03:28:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5bcbc9b0f0398bf8f14c235b24ba85d9acacf855518119cd1ce338a235a15`  
		Last Modified: Wed, 13 Sep 2023 03:36:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e8f8b6a865f909378039e86ae667b406118a25b3a153bfc989219634e11931`  
		Last Modified: Wed, 13 Sep 2023 03:45:27 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a9140c6a0cfd95053c573337fe186e7c914e2cddc4ded5396d633f8168d811`  
		Last Modified: Wed, 13 Sep 2023 03:45:27 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ad06a8f04950c85d8c4f1f0bf2976f8279ad5bddaa2eeb25ac627a5322ee4f`  
		Last Modified: Wed, 13 Sep 2023 03:45:27 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d27824264e82d62f11110ce00b426e3404ff58b09ac8981602874b9d0f4518a`  
		Last Modified: Wed, 13 Sep 2023 03:45:25 GMT  
		Size: 68.8 KB (68806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03cb3c15586ae832292360f56f1ac78eaf96af2d83bcb41622737199018f5d2`  
		Last Modified: Wed, 13 Sep 2023 03:45:25 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658d250f1e13f7f305f2b10bb024d9f491b8a54238a4913ada91247e962d180e`  
		Last Modified: Wed, 13 Sep 2023 03:46:52 GMT  
		Size: 45.8 MB (45836457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ce7ffdf7dcf733f52083c70fb6374f9fb13dddb7bf6c7394fb51af297ab8e`  
		Last Modified: Wed, 13 Sep 2023 03:46:43 GMT  
		Size: 3.1 MB (3146455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
