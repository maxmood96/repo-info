## `eclipse-temurin:24-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:817ddf949571ddf341d621558543d56cae123e08e33dee27f5b9ad5b879bd7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:24-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:5f06dafae2ccf2ab3129abf6914e1cdab4f57fcb6d100f81edc364f6357d56b6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (248003261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549b967169787b5ffbe80d7448f1086c802ee3acbbc814d492feed008e8c0ab0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 02:48:04 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:48:05 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 02:48:06 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 02:48:07 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:48:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:48:11 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:48:16 GMT
COPY dir:90c9828944ffcd2978afe702f80884cbf787022d7dcd7becc7c91cd2ab6f7dd5 in C:\openjdk-24 
# Wed, 09 Apr 2025 02:48:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58e57df9cb0b3f9be5ca25da624c3bfbd98f77156d2e9d88c9f498753c406ec`  
		Last Modified: Wed, 09 Apr 2025 02:48:23 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cada0c0871286fc4dfadbb67a58dffa2960997f6f1027bd35915c72c80cefd`  
		Last Modified: Wed, 09 Apr 2025 02:48:23 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c28a41271797d54ab8b6f4f7b275e599ddc4d9a18c0bc8783bfaf43b8f0b781`  
		Last Modified: Wed, 09 Apr 2025 02:48:23 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ac4fba4dfedcb7094afa90dc3f499e04e9ce4f2dc8ed57c7678264c67f2dda`  
		Last Modified: Wed, 09 Apr 2025 02:48:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1c287073d6b3764d780015abb0100c9896dc62e8598d9e8ddd5006b0bd32c`  
		Last Modified: Wed, 09 Apr 2025 02:48:22 GMT  
		Size: 77.0 KB (76968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6bfb57f26db7d389e21b23cfe2db6766f3181270685b5c79c1943dfd4db86a`  
		Last Modified: Wed, 09 Apr 2025 02:48:22 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7ed762f03d913d914780c9474309af2681b1dea41e1b7366899f4fa8af2c4e`  
		Last Modified: Wed, 09 Apr 2025 02:48:29 GMT  
		Size: 57.7 MB (57702457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed98c4266dd8c12973d02ad3dbffff4332afe6ad611551f214e686ba6b2c5469`  
		Last Modified: Wed, 09 Apr 2025 02:48:22 GMT  
		Size: 105.3 KB (105349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
