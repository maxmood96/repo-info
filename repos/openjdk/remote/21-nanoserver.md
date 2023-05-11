## `openjdk:21-nanoserver`

```console
$ docker pull openjdk@sha256:da30459a491183d137f756811fbd3a62aa33a68f265038526bc485cf0c2d590e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `openjdk:21-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:cc94c249b182d30cd570cafb8bb8f3552945c857d57e9e507efebf153f2f3f1d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305097165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289b7f74ea11165fbb9a70b788d10c8a382ec0e5b7e300a9b087fb5ad4339a9e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 00:40:01 GMT
SHELL [cmd /s /c]
# Wed, 10 May 2023 02:57:56 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 May 2023 02:57:56 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 02:58:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 May 2023 02:58:09 GMT
USER ContainerUser
# Thu, 11 May 2023 22:17:44 GMT
ENV JAVA_VERSION=21-ea+22
# Thu, 11 May 2023 22:17:58 GMT
COPY dir:fbfa1101a39fdaaf6211472c1535497c9c7583855c1ea9e206b0f3a9ed3bd73d in C:\openjdk-21 
# Thu, 11 May 2023 22:18:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 11 May 2023 22:18:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b79dd15c5dd82bc10521b9a4e49241f70088bc6edbb286f90be198abea55e23`  
		Last Modified: Wed, 10 May 2023 03:01:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40d6657961af59b636be2db4aa1fcef304eb245271a8ae41504adce8615cd1d`  
		Last Modified: Wed, 10 May 2023 03:01:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906b9562d5b2a03bb6c35a1ad6ee0d9becffcc133bb4d938b390c69e08ed9ed`  
		Last Modified: Wed, 10 May 2023 03:01:26 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa4992dcb0ef11fcada4b2f46b4a9c8cde731d43e793119cd32bd5fed253cd8`  
		Last Modified: Wed, 10 May 2023 03:01:26 GMT  
		Size: 66.9 KB (66929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee642db739fb63532d81702ffb8160c34a27c60b4725dcea8a48eae94769a63`  
		Last Modified: Wed, 10 May 2023 03:01:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7d6656b04ee5d737cedb3bbe14281cd691cdd44fb986d28497b41d2c2e6f17`  
		Last Modified: Thu, 11 May 2023 22:20:32 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7c5a94fc90a2a0994c2fcfa4b65b78ca70d334440fcfeefd487b5cc0381bbf`  
		Last Modified: Thu, 11 May 2023 22:20:50 GMT  
		Size: 196.8 MB (196841272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a964d889934a1c527dc121cd5dc87a13aa338faa2ca5553aa301909f79be137a`  
		Last Modified: Thu, 11 May 2023 22:20:33 GMT  
		Size: 3.8 MB (3798046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af47f2cd60ae9a7a96c45c9f075edca0148c40c26843209d4d39e0aa81eb227e`  
		Last Modified: Thu, 11 May 2023 22:20:32 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
