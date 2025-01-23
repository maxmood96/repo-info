## `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1621ebebe90c27dbce23e962e545630d0dd02d7473537a4b73bbded4d1097274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:c36212abd185c3e85811b93dff09e9d2e9b4da05ce9095c6d20020bc0322d692
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240293073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53773286b069a26d7a617970297b9784f6ba7f623eb17f811a74858a664a813e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:18 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:18 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 22 Jan 2025 19:34:19 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 22 Jan 2025 19:34:19 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:22 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:34:24 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Wed, 22 Jan 2025 19:34:27 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2800bbfdd74fb337f34757e25867402876293c2e974757cfa673ea1fe5f6ea`  
		Last Modified: Wed, 22 Jan 2025 19:34:31 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7348d714fbcf9c97c113ce7014a2c87816501cb1b919f52db831046749ddb2ca`  
		Last Modified: Wed, 22 Jan 2025 19:34:31 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb380d63d698a7b18be16ac945e3eedb1a344b9f9f478de9daf9b380625fe33`  
		Last Modified: Wed, 22 Jan 2025 19:34:31 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9394e0c8d553a22749862fb83f2dca3a9a9fb9fcb8a95a30ca1fb4fa3f5d428`  
		Last Modified: Wed, 22 Jan 2025 19:34:30 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a70d930018d636903a48d07d479589c26c94737bd5302a532b5a8f6d24f2d37`  
		Last Modified: Wed, 22 Jan 2025 19:34:30 GMT  
		Size: 76.3 KB (76270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ba1fcd41b7411bca59f5e70d7c5a2e18945a32d7a5ed004c550b435a765b6b`  
		Last Modified: Wed, 22 Jan 2025 19:34:30 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a8650fc7c0ed92c581289f87f8c2705d534b6e44e632f48eab8d8b38d7306b`  
		Last Modified: Wed, 22 Jan 2025 19:34:33 GMT  
		Size: 41.1 MB (41061457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6582b7d3264f41f49af1fe5c16de85fffe0aa6147d2d0331cbddab9b13bc8c6`  
		Last Modified: Wed, 22 Jan 2025 19:34:30 GMT  
		Size: 95.8 KB (95788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
