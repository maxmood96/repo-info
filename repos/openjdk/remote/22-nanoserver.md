## `openjdk:22-nanoserver`

```console
$ docker pull openjdk@sha256:9d5ce70db214d10ca7c32f27fb481ae35843b3e3108fd68aeca08a965892cffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:22-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:d9e8a980a2096d17bea7384e84d511453da659a5787da7b0e4c46a95ebfc7824
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305960559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122189b5c0a266dba6877d8ff058ed3ee179389a0346eb583ae8fb2e33a22406`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:07:44 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 21:07:47 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 14 Feb 2024 21:07:47 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 21:07:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Feb 2024 21:07:50 GMT
USER ContainerUser
# Wed, 14 Feb 2024 21:07:51 GMT
ENV JAVA_VERSION=22
# Wed, 14 Feb 2024 21:07:59 GMT
COPY dir:ce7c8053267780a9233f43fd4d9a18cc1368b2bafecd86f958b1f78643bbb9b8 in C:\openjdk-22 
# Wed, 14 Feb 2024 21:08:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Feb 2024 21:08:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458cae7585e661a6a7549145d53dfac9ebb50b69d6ff0905f70349774c4bf04f`  
		Last Modified: Wed, 14 Feb 2024 21:08:10 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c33ea36791ba6bf76815c392b1c28d9737c8e7482609fa5853b9beef134ecd9`  
		Last Modified: Wed, 14 Feb 2024 21:08:09 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1252183e13363759a9c0eeb3f8a2c10efd0abdcfc072a8689033ca40d1656df1`  
		Last Modified: Wed, 14 Feb 2024 21:08:09 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11399dd1e152afc3c69ef0b7b2bc30cebe202a4e8363c5980529999ec72faf5d`  
		Last Modified: Wed, 14 Feb 2024 21:08:09 GMT  
		Size: 83.4 KB (83431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c95362869cdf30ea9d5d4f1e28f759b39b5f1fe10c8c2cd27cd8388556f066d`  
		Last Modified: Wed, 14 Feb 2024 21:08:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8184d1bdb2b9a72ee8ae0b4b388dcc2f61cd4a86b9884ad6dce02a0fd191c890`  
		Last Modified: Wed, 14 Feb 2024 21:08:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e8bc229e6edf281322bfe2f8a9ca7ae3a45b1a0fe6ba3859c855d8c7421e68`  
		Last Modified: Wed, 14 Feb 2024 21:08:19 GMT  
		Size: 197.4 MB (197367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13372b8396aece50a22edddec14f99132eeb0dab01d3c9874dd94ab855a60fb8`  
		Last Modified: Wed, 14 Feb 2024 21:08:08 GMT  
		Size: 3.9 MB (3881121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7769ab3f21e31a0e17861fbef1011620335db2b12988edb1eca50b196d1215`  
		Last Modified: Wed, 14 Feb 2024 21:08:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
