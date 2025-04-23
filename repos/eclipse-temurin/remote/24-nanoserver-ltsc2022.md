## `eclipse-temurin:24-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:791a2250b0597af172f9ffccac06af0ef5218135157dadd886d9916cba4888ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:24-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:b9e3acc10c60bc5f2c16fdd64f700b7e712db763a62a130bce2ecd3466201878
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260080172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fe12b8da29729370a633c734194c3a3655f6f8e59aa3099d5a2d1e5e4f8bf5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Wed, 23 Apr 2025 17:16:00 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:16:01 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 17:16:02 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 23 Apr 2025 17:16:03 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:16:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:16:18 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:16:24 GMT
COPY dir:ab006ab9903f5de6ad6a158af78f8d39737a3dacdd719a53420635ed01783e4e in C:\openjdk-24 
# Wed, 23 Apr 2025 17:16:31 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 23 Apr 2025 17:16:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170aa6c028d2c2d24b2a8d5abf6644e51aad9460c14b565e165ca51a5f7f8e1`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072bcc5edd61e9778eb345dd111bee04fff52d7125f638be4ddd11b293dab858`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a872c0c6a7ab1b6a9ac3c1fa2c3817d29fe87569b4a86b9916efe139e85a5a76`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1373d900308e582ef196da3b0059ef509ef55ce6d7833623ac74c139c4940db6`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c87717a3afee9caa3e6b917b56190a6dfb83d4a85b969b9f8083c036fad94f`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 72.3 KB (72329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbe2e58d1e86e142c0e7c52350cc471b53d64c95198e632d2d746ddb1942642`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a8cb8a9af09212966cae62158f7258d8b24f3602c812301e8cceda6cc458d8`  
		Last Modified: Wed, 23 Apr 2025 17:16:48 GMT  
		Size: 137.4 MB (137364774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d01cc8d8dba9338061acc6b5b13dfec41ffbc38ceaa2d3dd852c4d203b162b`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 97.7 KB (97660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dd68b3e80d73f9694c060d6273b4cf86c1cd3a07810d065cfecb7ceaebbdd0`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
