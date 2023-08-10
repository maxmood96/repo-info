## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:7d1453458bdabc3b3d587e06912748fe002ae2d0748f5d00ff022c1c8788877b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:c67988d0619a07dd2dd41f22c20f84f1b3f15ce3a9599c5fb59707bc3210e47a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297716983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55352af7d6fc04622905030b78bfd36a3379ead0394493aee26fa8026480047b`
-	Default Command: `["jshell"]`
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
# Wed, 09 Aug 2023 23:49:05 GMT
COPY dir:0494f0c3004dc0f4e40e3f6c0c6e0f2ac35120ffc9906421c49b5c62e99eee70 in C:\openjdk-11 
# Wed, 09 Aug 2023 23:49:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Aug 2023 23:49:17 GMT
CMD ["jshell"]
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
	-	`sha256:48fbd024cd7b1d2186bbd6a136ae3fa9f5f4560bfa089732cb8b18955fbf235e`  
		Last Modified: Thu, 10 Aug 2023 00:23:59 GMT  
		Size: 193.1 MB (193101815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d92dc320019e34b7a865fbe7d5617a262af567c5e53241617ee80a082f2e12`  
		Last Modified: Thu, 10 Aug 2023 00:23:40 GMT  
		Size: 81.7 KB (81662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561acb94bdeac9d45fa26aad5a987b154a0ced81f587f5eef5dffdf3dbef8a2f`  
		Last Modified: Thu, 10 Aug 2023 00:23:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
