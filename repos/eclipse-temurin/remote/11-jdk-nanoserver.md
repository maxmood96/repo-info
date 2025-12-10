## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6649e95715047cf36bb4d80cdd932003457e0068e53120de9f325c210b5b3d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.26100.7462; amd64

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

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:e673a599cb5752af949b70c1e613d8b276caf032647c6aa5afd9d204d48882e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321231336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6060a7a132cd38e41ffbdb5a76f11e12bef5f52615a7356f5fde88c2554d9e98`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:41 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:12:41 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 09 Dec 2025 21:12:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Dec 2025 21:12:42 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:12:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:12:44 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:12:52 GMT
COPY dir:207a50c3961430a3231a748eb9ce354eec00313f0753b2d5e8f279d3afd46cd8 in C:\openjdk-11 
# Tue, 09 Dec 2025 21:12:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:12:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95361dc1d7d66c6d1cca1411b68c4130a2416a2274c8b466e22d712d4f5999bc`  
		Last Modified: Tue, 09 Dec 2025 21:13:24 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36315e8daf6649a15b2c4b2c37028c7ec59905404c51d517c7298e2d669ff0aa`  
		Last Modified: Tue, 09 Dec 2025 21:13:22 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a91b6546edf996189e8b9c02041d6cebbd6957b28afb3672e79b5b219fe280`  
		Last Modified: Tue, 09 Dec 2025 21:13:21 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4c45a97fc7fd936727c93d27ef6764eb38675044aa235acb82012ed9b941b`  
		Last Modified: Tue, 09 Dec 2025 21:13:22 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313c2dac1973f36b0a5368a606181d73a4ba7d6541ddb0819ea95f65ccd7b000`  
		Last Modified: Tue, 09 Dec 2025 21:13:22 GMT  
		Size: 77.2 KB (77187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787b2470d2dd16f7818e89bdc6487de29ef33d0a0ced2bb22963d07406825128`  
		Last Modified: Tue, 09 Dec 2025 21:13:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7898855d554f22690a42de8d5c53f6945b0e1f0bc4158c239597eee718cd938`  
		Last Modified: Wed, 10 Dec 2025 01:12:48 GMT  
		Size: 194.7 MB (194670556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7865079f23b4081049f55fe3d9b9b11730afd2d6f6791a6d6396fcb93e9cb95`  
		Last Modified: Tue, 09 Dec 2025 21:13:22 GMT  
		Size: 118.9 KB (118916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c7f2fbea034553c9ee06c9570d45bbcc6d486b828ab735b2e0544eea6091c4`  
		Last Modified: Tue, 09 Dec 2025 21:13:22 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
