## `eclipse-temurin:19-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:30ce6f07dd9ab46f050ef9287b568d34fcde580fd8f5805a596e7646a043ff5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:19-nanoserver-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:cd5fbcbbfbe11831f07aa2b77d6b8f8c1c2fb741917aac279b65b65ebd829fec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303982181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa194d11365ebd9490f2d4f062eabb5b3521e5ae4d9abca4b230d2d18b9a0a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:20:03 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 08 Nov 2022 19:20:04 GMT
ENV JAVA_HOME=C:\openjdk-19
# Tue, 08 Nov 2022 19:20:05 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:20:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:20:22 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:20:40 GMT
COPY dir:2282de048661e89f3c315adc23c8954e0ca245f9a969462117712d8342758a69 in C:\openjdk-19 
# Tue, 08 Nov 2022 19:21:14 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 19:21:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c993e86216e660ce8da663a97e89aa7cfc3333d1d31e64365fcd808bf18ad8b`  
		Last Modified: Tue, 08 Nov 2022 19:55:46 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183931c033e89e7a1540537e2028fb237593411d17ecd43959a0de8fcc9d5890`  
		Last Modified: Tue, 08 Nov 2022 19:55:45 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfac6e35bc26a1a8187faf966bdadaee0c7e785bbf9a78bb0b589f943c628228`  
		Last Modified: Tue, 08 Nov 2022 19:55:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd0881971f1371fe48113d594b3ed6f53eb51d587ca7a1c5c4fc09a75ca4154`  
		Last Modified: Tue, 08 Nov 2022 19:55:42 GMT  
		Size: 70.7 KB (70733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e530576cfb96f30c04b69977f6cb2fbbe6e31a8c019ed3d47582ac90df242b91`  
		Last Modified: Tue, 08 Nov 2022 19:55:43 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc07137872f5754ebd19b79d4dace3992180ad4f227ee402d8c855dcb41ad81f`  
		Last Modified: Tue, 08 Nov 2022 19:56:05 GMT  
		Size: 193.4 MB (193445984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5625072fe74b1996e0c028b1627abd3f32a4f0366bcd3b68601ad9a54531f1a7`  
		Last Modified: Tue, 08 Nov 2022 19:55:44 GMT  
		Size: 3.7 MB (3735099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4410ec41a03042b77b8a52c34c848ca379bbe8f4764c8d680c0e8dbae9cda64a`  
		Last Modified: Tue, 08 Nov 2022 19:55:44 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
