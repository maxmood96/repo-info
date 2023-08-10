## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ad5f39169ae3de0a788b4418629b0e59b01b0c889a535eb664f85bdf63ac52e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:08ebdb8f6f450ce9f7dfb20f651c6502c384a8450e5ebd2b2017ea0a9173ba27
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306375498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76726861bd9028512917c6db355301323973e5ec237fb1983da269bec815bf3e`
-	Default Command: `["jshell"]`
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
# Thu, 10 Aug 2023 00:14:30 GMT
COPY dir:feac886cbf24087a98a3b6290107e05d81c840e59da2a1e8e2f12f6e62993a44 in C:\openjdk-17 
# Thu, 10 Aug 2023 00:14:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Aug 2023 00:14:43 GMT
CMD ["jshell"]
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
	-	`sha256:b3b1c273ad60767ba95f896cc4efbcabdded57cfddd37b5d14c5ba6903b935a7`  
		Last Modified: Thu, 10 Aug 2023 00:32:41 GMT  
		Size: 185.7 MB (185731438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0114a08cf70e0914969501b108469a3891d21f7c0a154cb36b004538085e8f25`  
		Last Modified: Thu, 10 Aug 2023 00:32:22 GMT  
		Size: 61.5 KB (61548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fca595b0340671312eb529a99e3b15ddf818cb393a0fb2acd4f3abdca90b53`  
		Last Modified: Thu, 10 Aug 2023 00:32:22 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
