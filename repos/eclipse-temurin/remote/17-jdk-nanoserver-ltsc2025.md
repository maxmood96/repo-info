## `eclipse-temurin:17-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:e20d5551968244097caab1bcb7a54ea8cb67248ab6b13f61748ec6405f943d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:353dfa348294b1171402730022f8263300e82d6515b73fa210a010f8abf7e109
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393734170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7022e7d31f70829efd8a585759333b0cae33fadeec6ac40925845e345161aa9c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:16:25 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:16:25 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:16:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:16:27 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:16:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:16:31 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:16:37 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:16:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:16:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf03bf4dcb2b8dd659bee7bf147aa24762f3a0cc7e2aa33adfddf0047d79215c`  
		Last Modified: Wed, 12 Mar 2025 19:16:49 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088269d513fb9983c4d3d983f4bcc662da1ea5f24b41d82deae65a87c00ba370`  
		Last Modified: Wed, 12 Mar 2025 19:16:49 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e892b7a0401538b74eb744808f4b9d416b3af0714905798af57f740b3de431`  
		Last Modified: Wed, 12 Mar 2025 19:16:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2f9daa939c353416c3abf677bf4b5fcc8bea82a0b3e2ea3b0813195156b57b`  
		Last Modified: Wed, 12 Mar 2025 19:16:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c5157d939e30c4c6d70441f9a00b2c348fe37fccc153781df3720e8b4f36cb`  
		Last Modified: Wed, 12 Mar 2025 19:16:47 GMT  
		Size: 75.9 KB (75891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6881ab3a5e042640bdc83d950d08a2e11d911f2dfc24294a70f90468ad053a`  
		Last Modified: Wed, 12 Mar 2025 19:16:47 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac3fec6e039209f3433c3148a973582252598ea93e30702222f518343589763`  
		Last Modified: Wed, 12 Mar 2025 19:16:57 GMT  
		Size: 187.2 MB (187235416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff621f45c77b0095a2b12ad443e732b221d7e9a054a83f8f4b1a1d5c69515154`  
		Last Modified: Wed, 12 Mar 2025 19:16:47 GMT  
		Size: 114.4 KB (114395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb20823de1cff5151ed66c25ed14cd36154d9e2214a11b89891c220a3b9f4eb0`  
		Last Modified: Wed, 12 Mar 2025 19:16:47 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
