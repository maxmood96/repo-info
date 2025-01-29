## `openjdk:24-ea-33-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:f024d312d776cb501babc0f85d658fd00fc732dfecf59e574133d7fb780bba4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-ea-33-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:1571a67582a97f09bc2f5b06ff6c5903382aeed848fcf2276dfe2d8954013dcf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.3 MB (329329203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138122080a16c14c826ab63e1fab751de0f25928cd14070feed375b0c9f8e580`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 29 Jan 2025 00:27:23 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 00:27:23 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 29 Jan 2025 00:27:24 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 00:27:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 00:27:41 GMT
USER ContainerUser
# Wed, 29 Jan 2025 00:27:42 GMT
ENV JAVA_VERSION=24-ea+33
# Wed, 29 Jan 2025 00:27:50 GMT
COPY dir:0501e586ce21e14cfb645b0134706225edb213a038c5d5da062ef05b40a90877 in C:\openjdk-24 
# Wed, 29 Jan 2025 00:27:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 00:27:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f474b7bed30e00264915468de818bd74c81954bfa7355b352339f778f9c2e97`  
		Last Modified: Wed, 29 Jan 2025 00:28:00 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6486392f9c67365da516dd7b1723a161d1f6ad9c553d8970c1cc9a969d05bf81`  
		Last Modified: Wed, 29 Jan 2025 00:28:00 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca3ec4012effeb63c54c082b2abac4988ceae880a6e59d4d81fc5a6c44f47ed`  
		Last Modified: Wed, 29 Jan 2025 00:28:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042a3d0ba736a308885dc6b28d1c5d5dcd347ab924b3302d67ca0e5b923c38ac`  
		Last Modified: Wed, 29 Jan 2025 00:28:00 GMT  
		Size: 73.1 KB (73141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ee19f22d1bc62fa3ca860edfdbcda897556525501fb1f90341da45f1dc099`  
		Last Modified: Wed, 29 Jan 2025 00:27:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efe0c8ee6e229c038e3978c9c5114df6f093c1a68c8acfb3c5fbdbd7c9746e8`  
		Last Modified: Wed, 29 Jan 2025 00:27:59 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea799b9e89ed3411b70022dd81037eb25ee11da90a07a7057432a7484d40311`  
		Last Modified: Wed, 29 Jan 2025 00:28:10 GMT  
		Size: 208.5 MB (208490453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c80ad46b46d05131eebffead2aab8bd65fa453a163d1ba92c0d39d36d63877`  
		Last Modified: Wed, 29 Jan 2025 00:27:59 GMT  
		Size: 97.8 KB (97842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcf37ee1900462cdd9f897619bc9afd55598345310409f5ac6f851b435dcac4`  
		Last Modified: Wed, 29 Jan 2025 00:27:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
