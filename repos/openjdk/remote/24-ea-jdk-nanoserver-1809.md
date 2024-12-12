## `openjdk:24-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:04e168532debb96eba8e3a0e1bbc2d15711d144b3c6f2f5594c72ec4c2623f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:24-ea-jdk-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:e3de3f9059b5a33648b91c214870aa2788a12b3cd483936eb3521a117c9f5f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368142079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50571724c8c4f9e3c0a802357636ddc322d2fcf298f64d72cc9f01afd1a80a3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:45:28 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:45:29 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 11 Dec 2024 21:45:30 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:45:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Dec 2024 21:45:33 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:45:33 GMT
ENV JAVA_VERSION=24-ea+27
# Wed, 11 Dec 2024 21:45:41 GMT
COPY dir:742091ed6dd70bfaf8aa0c105e548ba4349e24f3ab2840414b5a569350576e65 in C:\openjdk-24 
# Wed, 11 Dec 2024 21:45:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 11 Dec 2024 21:45:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe807f81176f9996330a1ce4aa10f570fd3af34c5a8ad3aba1187dd5884750`  
		Last Modified: Wed, 11 Dec 2024 21:45:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c69b03c135f63e60e4a4c2151225cd9fbc185ca46a62ff2db5fb3095c213ab`  
		Last Modified: Wed, 11 Dec 2024 21:45:50 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc43d785a3b97e3522cc90b5ff132d7c97bef10d6f2fe8149f469b12314b238`  
		Last Modified: Wed, 11 Dec 2024 21:45:50 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80c57340886aa02118c63fe1bfbb6029c14c732d8ddd368878bf623a8835566`  
		Last Modified: Wed, 11 Dec 2024 21:45:50 GMT  
		Size: 73.1 KB (73076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4559512a0ff8d82ef6cb055605507b31e7dd67d0b07733e91768321b857dec6b`  
		Last Modified: Wed, 11 Dec 2024 21:45:49 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecab66a04b3506ecb2278a5f22a4622533cfbbf30c29df8a11082b4f8916f8b`  
		Last Modified: Wed, 11 Dec 2024 21:45:49 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89c4bf17bef06fc7c6abff4c96349f5d85835b1e549306ee87673ee98b3d30a`  
		Last Modified: Wed, 11 Dec 2024 21:46:00 GMT  
		Size: 208.4 MB (208435944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988fd914ad71a07bf36e92c7d17aec46061e4f7b1f35c7712ef740f7b924d0e`  
		Last Modified: Wed, 11 Dec 2024 21:45:50 GMT  
		Size: 4.4 MB (4395103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0e31d7c05b402e55e9c0850c18305667f7eea1155002dc9ac6f28bb8276061`  
		Last Modified: Wed, 11 Dec 2024 21:45:49 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
