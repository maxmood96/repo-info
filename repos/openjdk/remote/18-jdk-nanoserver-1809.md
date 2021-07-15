## `openjdk:18-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6777495762ec153aa468a5bea77a78171ed0e7b172d07bdf5da10df8173678d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:18-jdk-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:df2ea95ef0bb93e0d44c9d5c9ff7563e242ffcd3b8c6d762e5ff5bd987fa9a5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289369829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3a2820f2d0ab1c51992d4cf1812889bcc3aa0e2384cc8aafefa3795d996972`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 02:53:36 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Jul 2021 02:53:44 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 02:54:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 02:54:08 GMT
USER ContainerUser
# Wed, 14 Jul 2021 02:54:14 GMT
ENV JAVA_VERSION=18-ea+5
# Wed, 14 Jul 2021 02:54:39 GMT
COPY dir:b02efc826f662f1a6ca35b784c4c8a4b9983f69ea6441ae49617e80bb64fcafa in C:\openjdk-18 
# Wed, 14 Jul 2021 02:55:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Jul 2021 02:55:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89509de1f10eea36c6e14a8f32bc735a7e52e07235bb588c9dff480855c851c0`  
		Last Modified: Wed, 14 Jul 2021 03:42:25 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a172401c9271ad5ee8356c8f36a409f68259854e9de596e04069a2a176db3c6`  
		Last Modified: Wed, 14 Jul 2021 03:42:25 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3247de649752bd08242527a227d09c6398c2676025c2527f3b65c5c8cd032886`  
		Last Modified: Wed, 14 Jul 2021 03:42:24 GMT  
		Size: 69.9 KB (69948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1baf3b57ea2d376291b5174f1db66c9b8d971170b6ec871bdbd1fc496e82d65`  
		Last Modified: Wed, 14 Jul 2021 03:42:22 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4904ca4b36826b8d73bb73a004c5cfec18a3d59d29f2d6ec3bffd6fdc8ff5b7`  
		Last Modified: Wed, 14 Jul 2021 03:42:22 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bbb36aff8095e77aac78ea1fe9f4fd7debb573472870903a3168571c8dd4be`  
		Last Modified: Wed, 14 Jul 2021 03:45:45 GMT  
		Size: 182.9 MB (182901852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb336194ba55715dbfe54b1638623a34d3118703c55834c8c4cf766a8f8b9634`  
		Last Modified: Wed, 14 Jul 2021 03:42:26 GMT  
		Size: 3.7 MB (3665510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d809868c47b519b157dd93b62e21af9a0b48e488ea91cf2a58c309436dc7b0dc`  
		Last Modified: Wed, 14 Jul 2021 03:42:23 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
