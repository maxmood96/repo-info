## `eclipse-temurin:8u422-b05-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:02838f00c7ab00508565f3dd10b95ca157b3585f3063e6ba005bd680f33e4d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8u422-b05-jre-nanoserver` - windows version 10.0.20348.2762; amd64

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

### `eclipse-temurin:8u422-b05-jre-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:74d7265bb9940d1e6543ec78980d6953235f5f8f3b3d1aad1be8de6d5db48670
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195224255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6ca810c2c13099473929297138fb4e5ff4a884171b960e749c6b7a9c1d76b5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 19 Oct 2024 02:07:12 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:07:17 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Sat, 19 Oct 2024 02:07:17 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 19 Oct 2024 02:07:18 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:07:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:07:39 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:07:43 GMT
COPY dir:bd3f71a84ff97f19c5f813ab519f83a7ce371de8869736d916abb749734d7b15 in C:\openjdk-8 
# Sat, 19 Oct 2024 02:07:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98d8af1c17eb3422825379304fac42ab8a4e1bc2239e782a3ee5348f5a7454c`  
		Last Modified: Sat, 19 Oct 2024 02:07:51 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e5a8b99b08a2b7b6495a90070337120502d462fe6a2f941c6fca0116ca6297`  
		Last Modified: Sat, 19 Oct 2024 02:07:51 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdc0c48e8dc687b50ecaa4061ec7619391767b0043c6985d67470b51d5af20e`  
		Last Modified: Sat, 19 Oct 2024 02:07:51 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b154dc955488ab311d2fc29009f5c6ee0007f0ec4948ceb13524d31e071f9390`  
		Last Modified: Sat, 19 Oct 2024 02:07:50 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71219b83a62510501d7a21738c5fab2503f66360ac3343eeaf556143fc2b3c8b`  
		Last Modified: Sat, 19 Oct 2024 02:07:50 GMT  
		Size: 66.2 KB (66198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9a3289cb3e94e2be727d8b8d290b694329479ec8705398dee2bed5ffa290fe`  
		Last Modified: Sat, 19 Oct 2024 02:07:50 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d993e97712663d949eb2e3b057b968ba5fcc39c1a84be6eb7edb0e39ba9a7f`  
		Last Modified: Sat, 19 Oct 2024 02:07:53 GMT  
		Size: 40.0 MB (39993002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8c117db6682af472678cd436d162a66b54e5426f77cf56299e95e558cbee34`  
		Last Modified: Sat, 19 Oct 2024 02:07:50 GMT  
		Size: 66.2 KB (66222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
