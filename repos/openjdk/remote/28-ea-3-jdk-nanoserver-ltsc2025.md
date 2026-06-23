## `openjdk:28-ea-3-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:cd86afd7684e4e256d674a472eebcfbc6c4af8cc7db16a525d4cde0071eb878c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:28-ea-3-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:e7d6a76809850674a71680cdf9b67a50e66c4c33788da0ab5ccaff7e03b272c3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.9 MB (420875817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8601bb227c497daf622fbf8206d1ede0f7beda0fbbee38bbd245c78bc4c85b6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Mon, 22 Jun 2026 23:09:35 GMT
SHELL [cmd /s /c]
# Mon, 22 Jun 2026 23:09:35 GMT
ENV JAVA_HOME=C:\openjdk-28
# Mon, 22 Jun 2026 23:09:36 GMT
USER ContainerAdministrator
# Mon, 22 Jun 2026 23:09:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Jun 2026 23:09:46 GMT
USER ContainerUser
# Mon, 22 Jun 2026 23:09:47 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 23:10:11 GMT
COPY dir:143aad653eaf1eafb22a0522125924463ceb107c7fe7f919363f4a6a05e7f3be in C:\openjdk-28 
# Mon, 22 Jun 2026 23:10:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Jun 2026 23:10:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834926281133e5abf1c51b7351f9fab8669b188e96d89bb4f19538466966cdc8`  
		Last Modified: Mon, 22 Jun 2026 23:10:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96646fd92a05557bfda2ae7665775c141670345ca00efc83bc6ddf425fffbc61`  
		Last Modified: Mon, 22 Jun 2026 23:10:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5852b366286c3a136d5602fe22598d056674e117ae9cf96d9a91f33606543cb3`  
		Last Modified: Mon, 22 Jun 2026 23:10:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453cbcc2746dc57efc4e6e76f6955f54166a5c1c1dd7cdfe6d18193d5f48cb52`  
		Last Modified: Mon, 22 Jun 2026 23:10:27 GMT  
		Size: 70.6 KB (70573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0c1d980cafa3ec8b165b74371b2aafdc5c426b2c33a2cea38a9a6629c1072b`  
		Last Modified: Mon, 22 Jun 2026 23:10:25 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf82044cc1dd649d151090deb393e3831991848acc1bbae558987efd4efeeda1`  
		Last Modified: Mon, 22 Jun 2026 23:10:25 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32087660bf608303cd5f1dd2c863f76a23cedcdf129e7bebf28959b2758344dd`  
		Last Modified: Mon, 22 Jun 2026 23:10:39 GMT  
		Size: 224.0 MB (224028221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7899daed09ff2913dec337190608a6bbcf6572f6ba67885428df3af99e8bd167`  
		Last Modified: Mon, 22 Jun 2026 23:10:25 GMT  
		Size: 102.7 KB (102686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44b4cf6e42c5e1d26a1bdda7cc06a4ef06e318b0690a22ee4814edcdd669435`  
		Last Modified: Mon, 22 Jun 2026 23:10:25 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
