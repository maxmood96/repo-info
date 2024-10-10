## `openjdk:24-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:259642612c5ebd7ba2361a6f89ab78f54f264370f9aaa29e532cd12b5807d78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-ea-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:c7d59a913560510ad36513425a02a91452ab36e5e4655f7a1d33f7349b73583d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367775826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349faf6e02671f91b6af49330122f461843171d8314bf6aea3244050d2564cc2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:02:38 GMT
SHELL [cmd /s /c]
# Thu, 10 Oct 2024 00:02:40 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 10 Oct 2024 00:02:41 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:02:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 10 Oct 2024 00:02:43 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:02:44 GMT
ENV JAVA_VERSION=24-ea+18
# Thu, 10 Oct 2024 00:02:50 GMT
COPY dir:f5140de5e996aa4094129ad1a1d9758b1b65115ff663859b09e72bb409560f2c in C:\openjdk-24 
# Thu, 10 Oct 2024 00:02:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 10 Oct 2024 00:02:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19baddd2d11ec37c7c05452ad69b37bfa236d5431809f5090c44d4c94d5ab03d`  
		Last Modified: Thu, 10 Oct 2024 00:03:02 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81ecc997538c3f2864b2d5a9ce297ee3f40c926c01ee73b1afd84cb245b61f5`  
		Last Modified: Thu, 10 Oct 2024 00:03:01 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059b24dbaa365a75eb8a0e7611fb9f990c86db769bc8cc098ac9ac10591501b3`  
		Last Modified: Thu, 10 Oct 2024 00:03:01 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cf32fdc8f3aeae4efb627578122066ad1f6db4c24d0ebc461202002ad7d5df`  
		Last Modified: Thu, 10 Oct 2024 00:03:01 GMT  
		Size: 70.0 KB (69973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d70769aac4cf2dfcd512753eca65105dd1ea8627dc6424a6645ffe57871957`  
		Last Modified: Thu, 10 Oct 2024 00:02:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f4ade54d1eb0059845651b0ab06caca76f5f4dea80b24058d6bd6b76bcb28`  
		Last Modified: Thu, 10 Oct 2024 00:02:59 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b50d0247a455bd46ce711d8460566f4d90438bdff320434a48fe289403a20`  
		Last Modified: Thu, 10 Oct 2024 00:03:11 GMT  
		Size: 208.0 MB (207999608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091d3c52f49f40456c97792f7b93fc555418bc97be2c595df996ad3797ef8b61`  
		Last Modified: Thu, 10 Oct 2024 00:03:00 GMT  
		Size: 4.6 MB (4606414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f25d6afce39e6ac19635c462e0c0eccb0a83b3a4e000288ad11a806e27ebfd`  
		Last Modified: Thu, 10 Oct 2024 00:02:59 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
