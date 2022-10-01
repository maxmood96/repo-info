## `openjdk:20-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:56075524af168f2daa87fe29497012afa1bd2fa1a1b413367a4a76e9a3597a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `openjdk:20-ea-jdk-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull openjdk@sha256:99f152e9e16d4c845514da9c48eea68f1a0df6a610d758e664deef2a3130f123
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299051467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4ed54e0ee8695c68c268aaec7e1d3f6e871cb0953e4168133bbe27a7cee0ae`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 16:03:00 GMT
SHELL [cmd /s /c]
# Wed, 14 Sep 2022 17:08:57 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Sep 2022 17:08:57 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 17:09:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Sep 2022 17:09:07 GMT
USER ContainerUser
# Fri, 30 Sep 2022 23:26:35 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:26:51 GMT
COPY dir:4c58c9370b3bf7980113603e02690c1728f322f9648c6281057d4324ec852efc in C:\openjdk-20 
# Fri, 30 Sep 2022 23:27:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 30 Sep 2022 23:27:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:233f09b2a52487084f2cfb5e06dac2815651432c9d37c729582f59cfcf66b243`  
		Last Modified: Wed, 14 Sep 2022 16:47:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67cb607010c6768708866762c8f245af049da7669af90242ea7dc3d1881f80`  
		Last Modified: Wed, 14 Sep 2022 17:22:54 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd0c7e3fefcb9d81347f1ab494f4177ae8fff7d71ac827f5e90d34ee4bf483`  
		Last Modified: Wed, 14 Sep 2022 17:22:54 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72046412150cabb4b6b5ba4cf56188800073ddce5f570b7d921bc62eb13c577`  
		Last Modified: Wed, 14 Sep 2022 17:22:54 GMT  
		Size: 67.8 KB (67836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea99aee812db540f38ee961b7634ec0afe7d8468d85e3adaabe234fee1414d5`  
		Last Modified: Wed, 14 Sep 2022 17:22:51 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c192e1065db9f4f5d8e40b33f8568f0c7578fbeb81a5592047613d1bee0803`  
		Last Modified: Sat, 01 Oct 2022 01:18:06 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dd7203967202c964b6d5f94ccd83f7d846e3b666e02c5e77e9cf89805331f4`  
		Last Modified: Sat, 01 Oct 2022 01:18:25 GMT  
		Size: 191.9 MB (191891436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eab684abe4ed6b37ad3e2d3ab1359b17bd96037fff0478a310af680ae901b8`  
		Last Modified: Sat, 01 Oct 2022 01:18:07 GMT  
		Size: 3.8 MB (3751062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9dfb6c49403e0ecc2d5c3ea0ee8a8b9de1f4c95f9f5ab6585c7d77b9b9e7c0`  
		Last Modified: Sat, 01 Oct 2022 01:18:06 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
