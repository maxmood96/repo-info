## `openjdk:24-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:f72d31e319dda7d15ad835a1a227a346d99428bb9b939174e524f83b0418f94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:22347b85360b5ac22f66bd34efaa40d73f61bb8da6b3342868d3fe35b74a44a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407709589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456d7bbc0035627f78e42fab405ec7ac9f9a44ecc41ca803d4f0f96247c9b25`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 21:15:32 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 21:15:32 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 22 Jan 2025 21:15:33 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 21:15:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 22 Jan 2025 21:15:36 GMT
USER ContainerUser
# Wed, 22 Jan 2025 21:15:36 GMT
ENV JAVA_VERSION=24-ea+31
# Wed, 22 Jan 2025 21:15:44 GMT
COPY dir:ad771fa0c4659d73c3b630b6d3ca25a6a36b0b9af26b2bc144bd47e6e5f888f6 in C:\openjdk-24 
# Wed, 22 Jan 2025 21:15:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 22 Jan 2025 21:15:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c196df0dcbcad7b28b77333688a4566bacda5c8060ecbca3e4dedf0f73ae69`  
		Last Modified: Wed, 22 Jan 2025 21:15:55 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7066d7aef230373fd2ece23b3654d905755c90bab7533adac3537944906747c5`  
		Last Modified: Wed, 22 Jan 2025 21:15:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d1002e26ba4c288d7212a99039899ac7a637a7d0c0c3c3d9e3656005f368a1`  
		Last Modified: Wed, 22 Jan 2025 21:15:56 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a5a84c3d5935b91fb5f89514d48f2d032bb6e855f692844267d96ce279d093`  
		Last Modified: Wed, 22 Jan 2025 21:15:55 GMT  
		Size: 76.3 KB (76310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d486900c52932c1190a08cb73f2a6682f3b130d4a1cc473c9ce8af7e335b25d`  
		Last Modified: Wed, 22 Jan 2025 21:15:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11373a7808bb0589ca1a854b84a8b3ff5eba92e64e75e9fa862c34525f4cbc82`  
		Last Modified: Wed, 22 Jan 2025 21:15:54 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e37ca5c11b0f8220657fee9587cb27337a200182594406a73348f127993e07`  
		Last Modified: Wed, 22 Jan 2025 21:16:06 GMT  
		Size: 208.5 MB (208468406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755a41c3977e36d93887a306686faf4b05c07716172b13ec790c4fba1c927ab1`  
		Last Modified: Wed, 22 Jan 2025 21:15:54 GMT  
		Size: 104.4 KB (104383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ae810003214249113253104ea0f49582fafc8d526af908cff1e0c9e2b8e836`  
		Last Modified: Wed, 22 Jan 2025 21:15:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
