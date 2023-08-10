## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d103800364bc7d2899b4adb38d794af5197ad6cc6da0c016f8fbc89bb933c9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:5f036ad7354c810f1d3b72ae8683871f49ba17b2e2e383398d1556dee024a399
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164046029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d458b03987ec1978c46e4f1405b9e133afd162ddbe4f17bfe9535161b3eedfd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:14:04 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Thu, 10 Aug 2023 00:14:04 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 10 Aug 2023 00:14:05 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:14:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:14:14 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:15:03 GMT
COPY dir:9ca8bbfe0bd954313c0faf4fbb854bc33f4a5f49acc779e58df6b82fee73dcb7 in C:\openjdk-17 
# Thu, 10 Aug 2023 00:15:14 GMT
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
	-	`sha256:19290aa2672dc4b3bfac6f7b2ed75863cf68e0fa65c755e75b4665237df814ed`  
		Last Modified: Thu, 10 Aug 2023 00:32:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bafcbcd5a5d937e101c985549a5f0f8f69807735436ec5ce1fe7e912c81395e`  
		Last Modified: Thu, 10 Aug 2023 00:32:24 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527bda37ca6894a3d189404577b32a2c0e922df3b8cc46f2c189348d071b6e2`  
		Last Modified: Thu, 10 Aug 2023 00:32:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f411cc9b8761f9302991748f1340aa26a947f733562dfaa5b82f2405c749bbb`  
		Last Modified: Thu, 10 Aug 2023 00:32:22 GMT  
		Size: 75.3 KB (75319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3456ed745cc7943cbf780dafae226451fdc70d166f5ddc6122ac173de5f00bf9`  
		Last Modified: Thu, 10 Aug 2023 00:32:22 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e7a4127ee2d8aa353ede68bc6dbf1a43549072fdb71e1ca8b7d4a8c951d860`  
		Last Modified: Thu, 10 Aug 2023 00:33:01 GMT  
		Size: 43.4 MB (43403137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa98bccb41cc3da598711c525f5b8b3db7fa884248020d619d4936f08e96739`  
		Last Modified: Thu, 10 Aug 2023 00:32:53 GMT  
		Size: 61.4 KB (61407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
