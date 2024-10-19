## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0702c225b8c863253dd4027f3897a097c4f7b20765faa9fcb6f8404ece7c8137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:53ffc6141929927d5554080a6ded8f3f06178199a29d7a1c36d514e697ba160f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164033850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9f250224f4f1479e6ed0d76d0e53735388e7240cc24766defe4003f2723e1c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 19 Oct 2024 02:15:14 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:15:15 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sat, 19 Oct 2024 02:15:16 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 19 Oct 2024 02:15:16 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:15:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:15:20 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:15:23 GMT
COPY dir:7f1da5c11a4cbbc6c387d93a093a3b2f392c6d129d077f799c5268d1f2cff46f in C:\openjdk-17 
# Sat, 19 Oct 2024 02:15:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbd8baf5dc70c6eeae8645f93fdd0d1fea8a869d163d03082dd31152568bf1e`  
		Last Modified: Sat, 19 Oct 2024 02:15:32 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b314344279302b808cbf92e7c0a174b49dd93e8aa9b0fb0d46989f7c776f20`  
		Last Modified: Sat, 19 Oct 2024 02:15:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a11c99208d1518312ad1c552338d6fd60d0ee71eba1ae36ebd0cab2c6ab8965`  
		Last Modified: Sat, 19 Oct 2024 02:15:32 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd4ba01b01dfd58f0e662c0ac0c54cddeebba0ec1758469216846eced65b6d4`  
		Last Modified: Sat, 19 Oct 2024 02:15:30 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8f8bb3c7ca8f23c3da108a3fbf637a32fb7878ea64c04203cf8742cdab0e2f`  
		Last Modified: Sat, 19 Oct 2024 02:15:30 GMT  
		Size: 77.7 KB (77700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae897ab76c52c94ed62c2d7af35d24f385cfe2ab85560ebe9e8ebd369333d0e3`  
		Last Modified: Sat, 19 Oct 2024 02:15:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa46e8b664b90d2884d1256ae4d3667fd3358a8ad3d5f18864d8851eed94fe2`  
		Last Modified: Sat, 19 Oct 2024 02:15:35 GMT  
		Size: 43.3 MB (43338869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dff9b9077b645b3faf2411a075eeb7792e50687f8cbdd905ae7ea2f3f1288e`  
		Last Modified: Sat, 19 Oct 2024 02:15:30 GMT  
		Size: 100.9 KB (100923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
