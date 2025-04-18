## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:3e613061ba6b552bb4bc4630cdce6f8d8a1a716623eb7844bd9bc6f4291b60e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:3755b93acbb4dee856fafa87ec655c701a491a37c9783a340f3c44f787adf4f4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303477812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f15f6d99a7d11dc67dd9744368f6bdc1ac15e9003ff072162efa857d1ef8691`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:32 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:34 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 18 Apr 2025 04:17:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 18 Apr 2025 04:17:36 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:39 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:47 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Fri, 18 Apr 2025 04:17:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:17:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a99aa1a9a0b042e06a5f98805176ea96b4746f16132a8a9fc5b48084db324`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a33e4e3ef58a1e4abd494bb415364d5baf8aac0b7c38dd5e7daa04ad83e784`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3653fdb29c5cf95a1233655090701afe15a5ff85a0da129093baeff4e3ac9aae`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f6843d060d4086a8d2640e5a3193753fdfb92b38eeb7c9fa9539d0eae3a6e9`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc62a8073c5a684ab1b6b24803ce5a99fc802561787c8eb0d96e665dda25bca9`  
		Last Modified: Fri, 18 Apr 2025 04:17:55 GMT  
		Size: 70.6 KB (70584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aafda8821e7bb8e4d8750b67ff412182073681e28364417bad7152ab479b645`  
		Last Modified: Fri, 18 Apr 2025 04:17:55 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbef775813a9c35ad86a28a8688772d04ffcf5ea7b4cfe29a8c50a812ba8a5a4`  
		Last Modified: Fri, 18 Apr 2025 04:18:05 GMT  
		Size: 194.6 MB (194556390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3347ea6fdd6dc5b46a68d8a1b6a6b88470a98f2a61032d46d909fc6d66804677`  
		Last Modified: Fri, 18 Apr 2025 04:17:55 GMT  
		Size: 92.4 KB (92382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1829adb57324eb40bfd635b64204488a2866c66d6e8ed7fd8e8a9b68fda611`  
		Last Modified: Fri, 18 Apr 2025 04:17:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
