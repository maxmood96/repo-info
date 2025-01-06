## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:aba951487ae0b12e9949a1fba8f722cde8a1ed64269be3f084d1801feb7ca291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.2966; amd64

```console
$ docker pull eclipse-temurin@sha256:dec074c0e29550eb0411663d984fd01e9bc2d5343329507f06d7c5a685b37757
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309095044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23129738b37106932087c392b14bd58aaca6e6651449b23ba546ab4253c0af9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:43:11 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:43:12 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 11 Dec 2024 21:43:13 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Dec 2024 21:43:13 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:43:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:43:16 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:43:23 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Wed, 11 Dec 2024 21:43:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Dec 2024 21:43:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf4f6d103501611228fce046c7f2fc8ff0697e6cb4d8fcafb923bc590654530`  
		Last Modified: Wed, 11 Dec 2024 21:43:35 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3ac4e76bb28855a0b60f319890fdf9db413b078ea1d9db61cffefc3aebe386`  
		Last Modified: Wed, 11 Dec 2024 21:43:35 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0563045832f8b0231e81c97c2efcab4509d0203389f06126a536ab8f7d069e6c`  
		Last Modified: Wed, 11 Dec 2024 21:43:35 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea0c642c73972d1f9df79860b7cf415b44f7636cd99106e35eeab007150c61`  
		Last Modified: Wed, 11 Dec 2024 21:43:35 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b656844444f6c32820c4e2fd6eb0697e478ec00ed001ac6d0d1c9f4c943263`  
		Last Modified: Wed, 11 Dec 2024 21:43:33 GMT  
		Size: 76.7 KB (76721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8736eb6ab963790dbc8e06f936e102edff7002147928fe885024768390ecf`  
		Last Modified: Wed, 11 Dec 2024 21:43:33 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4683b1892730c95e038501963723951952d824ffd938613407c88b30e8b9bf`  
		Last Modified: Wed, 11 Dec 2024 21:43:43 GMT  
		Size: 188.3 MB (188303761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399c4c8558cffabc37c64e8178d457868bf30b539402acad75f1b0b7404e0552`  
		Last Modified: Wed, 11 Dec 2024 21:43:33 GMT  
		Size: 107.1 KB (107068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1119839ade91827ad8d810abf2c1f0b901858f530462702dd808d2aacaf84a`  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.6659; amd64

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
