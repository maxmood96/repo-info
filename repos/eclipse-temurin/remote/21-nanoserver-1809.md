## `eclipse-temurin:21-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e1c6513bb0843bcb764664af136d2ac580ce8edde057bc9d298690d39aa53c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:21-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:10b4accd40a866f76a91efcc7dbf669e4d345ef78f41668136a5e9addb388969
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359763211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1b2cea1194ffd0ebe13e2b8a355c6cdc0922ea7623d6f95a3cba7e86afd7d7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 19:40:26 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 20:06:39 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Tue, 13 Aug 2024 20:06:40 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 13 Aug 2024 20:06:40 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 20:06:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 20:06:49 GMT
USER ContainerUser
# Tue, 13 Aug 2024 20:07:05 GMT
COPY dir:a4ffd7e89e4f3b2e7536e802b1dd43338b71e63559dd6ffcb51f99d655bc67fd in C:\openjdk-21 
# Tue, 13 Aug 2024 20:07:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Aug 2024 20:07:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee91db53edb9eaa638d7d926c33dc3d39a0bedf5ace2c9ff25f8c413bc3ea2c6`  
		Last Modified: Tue, 13 Aug 2024 20:30:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0deb805e6379b5d3f397ccc06710f35d7480c0285f91e21af374fae855e2390`  
		Last Modified: Tue, 13 Aug 2024 20:36:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0b7c23349e323f21206e4b636c72ea7d51c6636c215abd8b3147704f71928e`  
		Last Modified: Tue, 13 Aug 2024 20:36:38 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13487ecda3d98bf5980e5b787bc6c11eb7ebec8a5e3ce01bb61732230630762`  
		Last Modified: Tue, 13 Aug 2024 20:36:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e0940bd59c36b80bff90a9329b6dcabbbd1061a01c434f305d6b02819a99b6`  
		Last Modified: Tue, 13 Aug 2024 20:36:36 GMT  
		Size: 70.4 KB (70362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe83703b4c540402521167eb41ac828ee18dbece075c9b22397cbefaabe1d47`  
		Last Modified: Tue, 13 Aug 2024 20:36:36 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094a5b3712f19ada35c43aebb1dd7cea139b58c4b5ea4d3e1a60a27fa37a78`  
		Last Modified: Tue, 13 Aug 2024 20:36:50 GMT  
		Size: 200.8 MB (200777414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf1a7caf2ffa6166e7e461b43d31f0f8481a393726417156844082cb8d00f01`  
		Last Modified: Tue, 13 Aug 2024 20:36:37 GMT  
		Size: 3.8 MB (3825448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bee3b0032cbc56a9f24282fdcdcbe734fb4a8165546aa631ef013677ca77f7`  
		Last Modified: Tue, 13 Aug 2024 20:36:36 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
