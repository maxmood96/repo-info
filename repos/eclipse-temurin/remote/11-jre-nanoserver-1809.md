## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:66b8ab4e697a5aa162caa047ba7fb00a9310a60f5342c6e56de0b121616dcfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:985854edb8b01f50910567d3cca5948037edf531921782fedf95de2986ae3434
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147840376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604b8bae30d8ff006588a101702405dd0576d492fe3a458e3bd8ce5ecf7af0f1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Wed, 09 Aug 2023 23:48:39 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 09 Aug 2023 23:48:39 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Aug 2023 23:48:40 GMT
USER ContainerAdministrator
# Wed, 09 Aug 2023 23:48:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Aug 2023 23:48:49 GMT
USER ContainerUser
# Wed, 09 Aug 2023 23:53:13 GMT
COPY dir:bb977dad5ac490fa947ae016040faee9a62c080b2232e87b0466ed93d95df9ed in C:\openjdk-11 
# Wed, 09 Aug 2023 23:53:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1c9c761cb2ccfe68da9c448d617d878c610bdaae520e16fad1fef07a03e1ad`  
		Last Modified: Thu, 10 Aug 2023 00:23:42 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a069a8466bde795232b06ad5a9868190b357a65dce0a11dd22e71d9fe09795`  
		Last Modified: Thu, 10 Aug 2023 00:23:42 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befd3c7f8bac74aba87080728fbf731b01c2c429c37e2b5e9483a27120090ba6`  
		Last Modified: Thu, 10 Aug 2023 00:23:42 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e37e3d38feb934a8f1a37f2e5e093e6d0e9d5a68bb7d89c422645a2ba4e9861`  
		Last Modified: Thu, 10 Aug 2023 00:23:40 GMT  
		Size: 67.8 KB (67835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fc967a86e47de945d9f4a7c1947679ef1a448ed45df3f8d926a01caab2c1f8`  
		Last Modified: Thu, 10 Aug 2023 00:23:40 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabb91d633d617b5fe580c0cf20a3da415fa5ffe602f1b689b45595c2fb354be`  
		Last Modified: Thu, 10 Aug 2023 00:24:57 GMT  
		Size: 43.2 MB (43220518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53269f2dde52f24e156f35675bed0d6a98d8ab4c936c967dfd1a4d5a1134ad7f`  
		Last Modified: Thu, 10 Aug 2023 00:24:49 GMT  
		Size: 87.4 KB (87386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
