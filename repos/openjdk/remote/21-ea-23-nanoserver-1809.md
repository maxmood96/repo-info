## `openjdk:21-ea-23-nanoserver-1809`

```console
$ docker pull openjdk@sha256:69524271be8cb855a1652056d95ca9e1f1d4e558791fd74a3b76929c84f6022a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `openjdk:21-ea-23-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:914789f3a5c758a6e13ef6ed61acb924ecb0babcaa7d9e7eec8476e62e5f1552
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305510038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a87f4306ba12ea64ea2a333c5ebb7bb4d097ba1244736783f4e8f4fa51b91f0`
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
# Fri, 19 May 2023 17:17:59 GMT
ENV JAVA_VERSION=21-ea+23
# Fri, 19 May 2023 17:18:14 GMT
COPY dir:0d67a80734c8cf6f9c958d59ff9158bf8c1f75f04170811a05c99878293c4c8a in C:\openjdk-21 
# Fri, 19 May 2023 17:18:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 19 May 2023 17:18:32 GMT
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
	-	`sha256:c2963d36c8972cabc67d65547238996189be24447d5dc2998cb77a549d9a402a`  
		Last Modified: Fri, 19 May 2023 17:20:41 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39041e80b7ea883530fc48b2919032d75dc1007d695d9e7e64c57e6755cc1bbf`  
		Last Modified: Fri, 19 May 2023 17:20:59 GMT  
		Size: 197.3 MB (197252628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e400ac58559c37dd0168d4f4380c618496a036ba3b3a78e806d4b728a4d161f`  
		Last Modified: Fri, 19 May 2023 17:20:42 GMT  
		Size: 3.8 MB (3799760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba648cc383e20460c04ac70cce325175ea8b54ed62358e88b2f5db584027512a`  
		Last Modified: Fri, 19 May 2023 17:20:41 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
