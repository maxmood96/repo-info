## `openjdk:17-nanoserver`

```console
$ docker pull openjdk@sha256:131b29fb28f95d37965edb6d1b0954b7a6ae4f325e8ad5a55287c4875f568592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:17-nanoserver` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:da9d95c5876972e2445efe521e9751242b2330bb800249c1d6087fac3093a098
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288564348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceaa0ca912ab30396d9977612e87574f890bda4e770d9089b7277ac508d6638`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 11 Aug 2021 17:30:38 GMT
SHELL [cmd /s /c]
# Wed, 11 Aug 2021 17:39:31 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Aug 2021 17:39:34 GMT
USER ContainerAdministrator
# Wed, 11 Aug 2021 17:39:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Aug 2021 17:39:51 GMT
USER ContainerUser
# Wed, 11 Aug 2021 17:39:54 GMT
ENV JAVA_VERSION=17
# Wed, 11 Aug 2021 17:40:14 GMT
COPY dir:16139fd5761a261a0505c9fb2561cbcbf9614d8d2403d5d2b56478bd7a396d2c in C:\openjdk-17 
# Wed, 11 Aug 2021 17:40:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 11 Aug 2021 17:40:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae0a5a946be2ad0e39a8260e454c0060a31a9f7e5be75d1f9038dc13730abc0a`  
		Last Modified: Wed, 11 Aug 2021 18:21:28 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43ae7a804fbb94b78c5049e9646665ab4f9e9d568427d641f7d01bfaeb5f6bc`  
		Last Modified: Wed, 11 Aug 2021 18:26:14 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40029af5e998937b3c864fa556be6782637cf0ea869a5b2030a17058317c40e2`  
		Last Modified: Wed, 11 Aug 2021 18:26:14 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b6a7b7de8cc762cc37ff39e738555356ecaa18bec56516378c41d6367fdd36`  
		Last Modified: Wed, 11 Aug 2021 18:26:14 GMT  
		Size: 67.8 KB (67760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af482eef114247a76edb4ef44b98dd949cc77380f545f62429aa2377899c53d`  
		Last Modified: Wed, 11 Aug 2021 18:26:11 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a04ff2b6ebf57f6965955d443d95de5a0cc52df3812ec445e0c731da2c45dc`  
		Last Modified: Wed, 11 Aug 2021 18:26:11 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db557a2d6689601de45721c075eba459f63ab7be087d5a4e510aaf8a11b1bd61`  
		Last Modified: Wed, 11 Aug 2021 18:26:31 GMT  
		Size: 182.1 MB (182079827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41af7e522a2136a2a9503d2b69f6b221bff840936abcbf6de034ac1e743cde2e`  
		Last Modified: Wed, 11 Aug 2021 18:26:12 GMT  
		Size: 3.7 MB (3668593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399822249dbae0cbd62a42b90ff49f0a05dabffe812862a31b93b2dc511278f7`  
		Last Modified: Wed, 11 Aug 2021 18:26:11 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
