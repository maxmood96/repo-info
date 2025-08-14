## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d1c443f344160b6a22989bd841cf248bd123302647a81225304ab62cc155db75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:99e71ca341912b82cf5d1d01d4e1ef9b9e0f08d761f0d9cafdb3037638b7f6a7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310205058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f4ade86a3bc185bbbd5c71bd85f9f955e37816421614ce4b5924bebea1af23`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:49:51 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:49:53 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 12 Aug 2025 20:49:54 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 12 Aug 2025 20:49:55 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:49:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:49:59 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:07 GMT
COPY dir:9871f8b851cdb90a4def8faeecdb142e7e99c62806f58a649ca6456cf4e2326c in C:\openjdk-17 
# Tue, 12 Aug 2025 20:50:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Aug 2025 20:50:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7356810f43750220dc390503b01eff114c6410a6167f7e66c76516f2fd6fa1`  
		Last Modified: Tue, 12 Aug 2025 20:51:06 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc68fdf22c0b7cb73f2114a97d2132d8893afda85bbd3d1c1a2668ab72e41430`  
		Last Modified: Tue, 12 Aug 2025 20:51:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aad4096812cf84993a41904348eaea66056fd054434cb3cc9ad95697a49d0aa`  
		Last Modified: Tue, 12 Aug 2025 20:51:06 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a018a038eee20514181380fffc016ca358dbe350486b67e30b05b3ee02ac15`  
		Last Modified: Tue, 12 Aug 2025 20:51:06 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab33d222263627ce121c2e91442689ae20476fe7fa260fe8bb55c12a767193b`  
		Last Modified: Tue, 12 Aug 2025 20:51:07 GMT  
		Size: 78.5 KB (78453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228f0edfa80ab3d5494534afb9cf4b95cb6605deff719326108c4e05847ce1a5`  
		Last Modified: Tue, 12 Aug 2025 20:51:07 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05575c1974cfeb7fcb3793b89385f4657b8c912cb597b471dec6c35e7779e4a`  
		Last Modified: Tue, 12 Aug 2025 21:14:40 GMT  
		Size: 187.4 MB (187352787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef1f81ec64c62e5e854b5dbdf05e04faaf094a4344b55f2e93d330b57de5000`  
		Last Modified: Tue, 12 Aug 2025 20:51:08 GMT  
		Size: 107.2 KB (107240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc0594ddbf7df874ede08ad46997cdb8be99b02222458d670188b93ca071f3e`  
		Last Modified: Tue, 12 Aug 2025 20:51:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
