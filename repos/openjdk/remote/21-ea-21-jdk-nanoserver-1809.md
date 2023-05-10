## `openjdk:21-ea-21-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:1d30fda0ec052df9799dedaf91be304eddda3035f869ce7c5ef3874f176d235f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `openjdk:21-ea-21-jdk-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:f7367fb51e47e5e2caa31fcec2e753713d9d2dd3ac3642d1975930324c9a9a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304801782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d081ae3d663e02b28d70d46fcb465e99b4ecb7de28b4ff5c6e17b35df1305e6`
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
# Wed, 10 May 2023 02:58:10 GMT
ENV JAVA_VERSION=21-ea+21
# Wed, 10 May 2023 02:58:25 GMT
COPY dir:8073f6627b0b13d2d0e6669e88b700d52872f6d6985f68438081a66f0741b9e6 in C:\openjdk-21 
# Wed, 10 May 2023 02:58:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 May 2023 02:58:47 GMT
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
	-	`sha256:e0d217830c13fbf9a2a2ab40cf1126751e7872fde686af58cb306b606d9d4bf2`  
		Last Modified: Wed, 10 May 2023 03:01:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391d03f34ff77ec3cb3e607af0e982d336739265a803af9b716f4b76c844e65a`  
		Last Modified: Wed, 10 May 2023 03:01:46 GMT  
		Size: 196.6 MB (196552497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3900f21d219fa7b9c5f4f2aa680c06f0fdabf5cabcba1c9f770c275220464`  
		Last Modified: Wed, 10 May 2023 03:01:25 GMT  
		Size: 3.8 MB (3791386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d492f103a24b4d5e4df272d07f99c44f41af051d0e386b85d8f473a27b6fe7`  
		Last Modified: Wed, 10 May 2023 03:01:24 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
