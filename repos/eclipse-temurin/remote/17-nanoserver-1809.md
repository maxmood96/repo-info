## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:d9578189bac50d1f71f17e15d585c0b95af279790599efac5aff902abefd4ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:dee3530fe92010cb1334d3f7faff8c30dec84ba610b430befef4e7244f306856
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.2 MB (347248583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667387c2a723fb95c883440ba7eef94332edb6c783585d40e8c69f1a65d5d878`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:49:54 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:49:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 11 Dec 2024 21:49:57 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Dec 2024 21:49:57 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:50:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:50:01 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:50:08 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Wed, 11 Dec 2024 21:50:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Dec 2024 21:50:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2e222d096fbd06f129043e1644a9297a0b95537a3fe57f216762bfa965c115`  
		Last Modified: Wed, 11 Dec 2024 21:50:18 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbf31651d606efe39bc8759291055dbc0455a793bc143e734303da66a9e768f`  
		Last Modified: Wed, 11 Dec 2024 21:50:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afacaec1071542e625c1381ef70eef0fb41f3c396bd6285b2eb1f479800159c7`  
		Last Modified: Wed, 11 Dec 2024 21:50:17 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2875256a56a9f07fc55057f18edfc1b76240c80f2dfb7cd702088dbd0d98ea63`  
		Last Modified: Wed, 11 Dec 2024 21:50:17 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e196b109d6a70831b26c716712b31a372363ce105bbd9519d1ea1ad417271b8d`  
		Last Modified: Wed, 11 Dec 2024 21:50:16 GMT  
		Size: 70.8 KB (70802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5880973cbf1a65305e0226c8f3bcc75a4222ba7b7ac586584fc4e1e0dcb50118`  
		Last Modified: Wed, 11 Dec 2024 21:50:16 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86efe78210f6ccb9081a0bfe049c406388b234967222e39a34bb7f6c46fe2c01`  
		Last Modified: Wed, 11 Dec 2024 21:50:29 GMT  
		Size: 188.3 MB (188303146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8097f71491989602671aa8f3d507c8c81a2bdffc7140947e7c7e20fa45244d`  
		Last Modified: Wed, 11 Dec 2024 21:50:17 GMT  
		Size: 3.6 MB (3636758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b491fa4cb92ceea141f3a7925ae96d98f37226c87d8ac8f35fd280cd0d10cdbd`  
		Last Modified: Wed, 11 Dec 2024 21:50:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
