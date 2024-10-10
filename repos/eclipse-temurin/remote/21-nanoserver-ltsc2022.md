## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5b7bda90b1d36ac5845b04c00c1b2bb28f1c8459946ee5f0c982278f84e98534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:d73253df0b44d8ad93682beb61fae16cc92d8e55f64d7788b60fb4afa27bde59
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321434068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7d860f662e5796e7dd8bf43cf56e7de98cec249e09b63355dfaa5cf7d9aad0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:11:44 GMT
SHELL [cmd /s /c]
# Thu, 10 Oct 2024 00:15:42 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 10 Oct 2024 00:15:43 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 10 Oct 2024 00:15:44 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:15:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Oct 2024 00:15:54 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:16:08 GMT
COPY dir:a4ffd7e89e4f3b2e7536e802b1dd43338b71e63559dd6ffcb51f99d655bc67fd in C:\openjdk-21 
# Thu, 10 Oct 2024 00:16:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Oct 2024 00:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96818114ce85fcf68e8af61951767bf11ed374ffe6a9023b6150122fbad46d51`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4381491f7a621ef132d497c650d372228e1972466ed342d9b253bb8f8696a99`  
		Last Modified: Thu, 10 Oct 2024 00:34:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbeda7b20a180c15ea2662bc0f428e75aeeef3bbfbcc6ee3d2f0ea2c57824f0`  
		Last Modified: Thu, 10 Oct 2024 00:34:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20825ba114810a7a5938603953ac3cd5926bc7735726a8781ebcf79bac79ba17`  
		Last Modified: Thu, 10 Oct 2024 00:34:58 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df05ef02b28f3298c5b68b730abf5da2175b95061afb183d6d7d405e0c218f94`  
		Last Modified: Thu, 10 Oct 2024 00:34:56 GMT  
		Size: 77.5 KB (77533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e53603dbfba3bc09f2ee9a4f12315be3fdca7ed1df65854abb2122bbb9c204`  
		Last Modified: Thu, 10 Oct 2024 00:34:56 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f60c53cb25ee367ee1f13f1cd4ba1abdd0f0cafa2428240589f07065e002013`  
		Last Modified: Thu, 10 Oct 2024 00:35:15 GMT  
		Size: 200.8 MB (200777135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce2c748fe78f99c3c0f7f00b00c148e934fff0cdb57856b7f03debc695b0895`  
		Last Modified: Thu, 10 Oct 2024 00:34:56 GMT  
		Size: 61.6 KB (61567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03f84315b2fe208c3bad470f819022d6fa878f9b9a1e3c394f440affff19f4`  
		Last Modified: Thu, 10 Oct 2024 00:34:56 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
