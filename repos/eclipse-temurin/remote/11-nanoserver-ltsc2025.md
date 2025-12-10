## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d80184886e878514fbb6f5eb5968406ba7a86c870fbefb8841a84f984ecc89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:85964f4723a2f09b1d9e4d985ebf91979355abedd8ec2169d171c7247093dcbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393705236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb34882f73dfc7fd1b6c06a8f83b93ffc8b30a25cc5b14708ad6e2f3f7b31922`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:13:13 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:13:13 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 09 Dec 2025 21:13:14 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Dec 2025 21:13:14 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:13:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:13:20 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:13:29 GMT
COPY dir:207a50c3961430a3231a748eb9ce354eec00313f0753b2d5e8f279d3afd46cd8 in C:\openjdk-11 
# Tue, 09 Dec 2025 21:13:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:13:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c3e9ac772555dbb907a48e4dcac3181c5961b789f6ef74dc9cf30cd0cc60ba`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e4d26f8823157bb78feb5536d652b2785a2aa7428cbb0b1844e77d10462b72`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7fa4311d0d11e2a3bbf7b5b1ee514095d022b056ae76b17b698dd9884f1c1e`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6756e7e30ad06d571e4d49702fd1f3de3e7b92bb37ca3fc15b9e1d3ec4c842`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942a3737af72f4ca2d1e6247323fcc11fa0603da359e9c25c2e579b3bc72ea03`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 70.4 KB (70447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c513718acc72763f8a26c402e5164813ab69189d6c3db2e616a167a0dc0be97`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bca4504f53a62f3c1b7f914fad7643f7082cd59a596bcb0879a68379266ab6`  
		Last Modified: Wed, 10 Dec 2025 01:12:52 GMT  
		Size: 194.7 MB (194670862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36a644f50b772da5383527f17a649183e1197919d326d9409b131c46835fae4`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 83.6 KB (83566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c927c7585a0d2ccfa37af6f071ffbe17e18946a28694f6b6c42e6124406ee90`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
