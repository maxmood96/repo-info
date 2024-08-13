## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b0440d7528733558230e2d4756e8cf7d4283289d3af56e82cf45c3e98f79167c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull eclipse-temurin@sha256:de8ad372ba57c78461748107506c075971f762a81ac4bee9cf266b3bf6e76563
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348898216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c742a67ccafda765342cc17eb2d90835ddf097ad326b943a86908e1fe25e88e2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 19:40:26 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 19:48:28 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 13 Aug 2024 19:48:29 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Aug 2024 19:48:30 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 19:48:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Aug 2024 19:48:37 GMT
USER ContainerUser
# Tue, 13 Aug 2024 19:48:48 GMT
COPY dir:b5e9d6d7234e205f01359f52140171f1743cc309a4dc5e4224755ced7d18fbfc in C:\openjdk-11 
# Tue, 13 Aug 2024 19:48:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Aug 2024 19:48:58 GMT
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
	-	`sha256:6a0b9c3c45adb5b76b8fa916d72548c0b6abf7933d1738a59113b109421e58df`  
		Last Modified: Tue, 13 Aug 2024 20:32:19 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c8ba66dab835fbec526d879c7bd7d50cbd6a6a3e103b880f97fd4fa448748`  
		Last Modified: Tue, 13 Aug 2024 20:32:18 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e73dd1929d66a94ee7a1c6521e69d48da654a99acc4036af3d115e69c29488d`  
		Last Modified: Tue, 13 Aug 2024 20:32:18 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc1fe8e679f1e113d59a9def40d971ed115cecc4ebcf294b2ff163d7e1a8da1`  
		Last Modified: Tue, 13 Aug 2024 20:32:17 GMT  
		Size: 69.2 KB (69220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784f6aeb0f8214ff1efb9efca573defd2571e6a8ae2c91b3ca4991e453dd81a3`  
		Last Modified: Tue, 13 Aug 2024 20:32:16 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bcc14a4305610b5c11c5d71f3008f570bccbe44f6c6e42fac01ee2333e5967`  
		Last Modified: Tue, 13 Aug 2024 20:32:30 GMT  
		Size: 193.7 MB (193658841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d6e4b8591a50c8c068970afc0efbae68e8c5b5800a9ce7a71af6ec49512940`  
		Last Modified: Tue, 13 Aug 2024 20:32:17 GMT  
		Size: 80.2 KB (80217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac93911037851d21d6699847774f06a167086c061493e073f02af7e228c84676`  
		Last Modified: Tue, 13 Aug 2024 20:32:16 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
