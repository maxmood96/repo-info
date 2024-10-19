## `eclipse-temurin:8u422-b05-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d1a743830e282f727a4a020568db52a2149bd82ec599cee333614a1cd06eb0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:8u422-b05-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:e77bb0ffe60bfa22c2e4965dd3c04da645e0d541afae10db0f364c5250264970
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160684934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431e01e8cfabd09fb6f53f6521c249b6f812e12b956bea1a1d94145e4c364efa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 19 Oct 2024 02:15:44 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:15:45 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sat, 19 Oct 2024 02:15:46 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 19 Oct 2024 02:15:46 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:15:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:15:49 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:15:52 GMT
COPY dir:bd3f71a84ff97f19c5f813ab519f83a7ce371de8869736d916abb749734d7b15 in C:\openjdk-8 
# Sat, 19 Oct 2024 02:15:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef510d5a7ef9c24e19f301f6c2e36421247b27b2be4f42b0f95ad5337c4cec6`  
		Last Modified: Sat, 19 Oct 2024 02:15:59 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62497f7668048fe72620584c6b29188830181fa7eede3714d29d0c88d304f633`  
		Last Modified: Sat, 19 Oct 2024 02:15:59 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141a43def00b75aaf6fb2a67b686ba8abe7ff5a232f90672d6b6dbc673ce9d4`  
		Last Modified: Sat, 19 Oct 2024 02:15:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6fd24fbfc910d5f1409d0459f0533f1d4cc92f7d4943dfb38568955e3edff0`  
		Last Modified: Sat, 19 Oct 2024 02:15:58 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5956ee27785fbfe8d1bd2e7944287444900bf2348516954598d57789225baf`  
		Last Modified: Sat, 19 Oct 2024 02:15:58 GMT  
		Size: 75.5 KB (75459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b6ab081bfda50dbd9827736919e5da07268068ca698a5ecbb9aa4ddb6cba3b`  
		Last Modified: Sat, 19 Oct 2024 02:15:58 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d374ef6be95fda6cbcdc72a970e8fd467ebcbde2ba0b80ba51ec17f957240b0`  
		Last Modified: Sat, 19 Oct 2024 02:16:01 GMT  
		Size: 40.0 MB (39992559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e368c7e5a18217ffc5529feeade1e0378e9b0f3a6139725d894668c1fb31b6ca`  
		Last Modified: Sat, 19 Oct 2024 02:15:58 GMT  
		Size: 100.8 KB (100756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
