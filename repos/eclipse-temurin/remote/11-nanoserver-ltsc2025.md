## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:758388687b959e4bfae90ab0f3d957e88ab364e88eb935959c4babe763014108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:2ec727b2a14fbb5dfa057f58a66a607face9db34981e633d5b2b559ac828fb19
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384920636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779e47e5cae4a4a736c6ec16ae59b9c8de2fe1463734cc67b0e3f1c2a37a51b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Wed, 23 Apr 2025 17:16:59 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:17:00 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 17:17:01 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 23 Apr 2025 17:17:02 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:17:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:17:08 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:17:17 GMT
COPY dir:c61af6ceef573b3d63f31a61f55e07ef4d3bfab78d8c06e63a667655942ae5e8 in C:\openjdk-11 
# Wed, 23 Apr 2025 17:17:25 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 23 Apr 2025 17:17:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f128b6459ac8021ed37229913fb059a6d0ce77f42cc7c7cc9ab9bcca16efd43`  
		Last Modified: Wed, 23 Apr 2025 17:17:32 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a28024421f20a1d9efdbf1be1959d9e6aa66cf9d31ddb01bd271bb1f6fe874`  
		Last Modified: Wed, 23 Apr 2025 17:17:32 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd63b80873541d518e85247e19b9be2b6c92bdf1360ce664c46ef809e93032f`  
		Last Modified: Wed, 23 Apr 2025 17:17:32 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c51dbc06bc04216b3324acea06a15ff4fb23e268144a6038ada5f86be6cae88`  
		Last Modified: Wed, 23 Apr 2025 17:17:32 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f6e2c7b57051f0f7f38238c9d433cca6dacdda40fb26acf15c3bd79b737eff`  
		Last Modified: Wed, 23 Apr 2025 17:17:30 GMT  
		Size: 77.7 KB (77676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8ab83b86dbc69d081101ecaaece797c86e4797b12338a4ef2cc08f260789a1`  
		Last Modified: Wed, 23 Apr 2025 17:17:30 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e496d558ae731005a956526981ba7579181d994d43c27d05e846a17318f36d0c`  
		Last Modified: Wed, 23 Apr 2025 17:17:40 GMT  
		Size: 194.6 MB (194577765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdee09ba1d205b84236a0e059937635952e0d880ca59e3849d6d4b7bfb30411`  
		Last Modified: Wed, 23 Apr 2025 17:17:30 GMT  
		Size: 116.8 KB (116834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef1eb8222fbb89c999bf704a6a8c5f5c437869edd743ac5e711fb6def84ffe6`  
		Last Modified: Wed, 23 Apr 2025 17:17:30 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
