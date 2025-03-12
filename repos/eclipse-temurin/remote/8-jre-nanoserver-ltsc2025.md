## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:8dc23202f8ed9a7fd57beadf655e69be50adffda7b83601893c675e3a815d7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:cf786852a4fb8a460bd464142e7ecca21573f39942880c1f7dd3bf28d5dec936
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (247028987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab785a5ba63fed0c978a5a7ef635eb02ecda87e097c4b17f16c6649e06b56685`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:00 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:02 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:17:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:17:04 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:09 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:12 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:17:16 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce2e201d1af7f5d86f70a6900c84ca210055bf152501e719e8eb24c2fd72074`  
		Last Modified: Wed, 12 Mar 2025 19:17:20 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd3b289e647fd123b2c4abe25c49d368fc0cc10331fe0f6285a41eb2469e597`  
		Last Modified: Wed, 12 Mar 2025 19:17:20 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731e3f3f1781cf224fe90dbbbd6b50224eba26e3d748c682ad976f4d3139a6ba`  
		Last Modified: Wed, 12 Mar 2025 19:17:20 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aaefc3ddcc9a41fda2ded2eda32d1dd78d5892b08223a91ba2dff9b1dee33a`  
		Last Modified: Wed, 12 Mar 2025 19:17:19 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2e7ff0fb1f1b72fb355ba5d05ae37bb462e3e0b29cbf9b649f96d9948510ba`  
		Last Modified: Wed, 12 Mar 2025 19:17:19 GMT  
		Size: 76.2 KB (76209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20963f84985eb7bcb59a93fd4dca9b6d94c26f0d820e6641ab526f61ed8229e`  
		Last Modified: Wed, 12 Mar 2025 19:17:19 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ab6269633770e7cabcdb5625a49d30fb222843c0966c6d2dd84c824e0b2af`  
		Last Modified: Wed, 12 Mar 2025 19:17:23 GMT  
		Size: 40.6 MB (40552456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7a12f7e402a747df77c1d028f09b45bd55b78344c36cc53ef7d1b231c4ea04`  
		Last Modified: Wed, 12 Mar 2025 19:17:19 GMT  
		Size: 92.8 KB (92761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
