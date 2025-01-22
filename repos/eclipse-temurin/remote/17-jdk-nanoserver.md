## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:135ef1c1a4b2a54f67445f3a62aebb08de5acb5d218032194e4fda02f388bfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:591cc84656a8e960ef7978a1508c0dfddc4dbac4502d041c53f4fbe2f0583a3c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387548149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8a92560e1203f5d96b9f6e35f8ca5e2ee3efdd1534a1e79c4a1008afe0bbb7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:35:32 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:35:33 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 22 Jan 2025 19:35:35 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 22 Jan 2025 19:35:36 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:35:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:35:41 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:35:47 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Wed, 22 Jan 2025 19:35:56 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Jan 2025 19:35:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdfce138d1cd86cfc9d6961e5ed4a10051f261411ee561fd4ff9e4cd5b0ad7b`  
		Last Modified: Wed, 22 Jan 2025 19:36:06 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b36ed111ed1c818b6fc2e6f58ff0e61a4d36ded883be033be268816dfbc944`  
		Last Modified: Wed, 22 Jan 2025 19:36:06 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74016344965f4c72939424d1f0db3f62921bb1d26777843ddec85381425064c4`  
		Last Modified: Wed, 22 Jan 2025 19:36:06 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c0d0690f038e12f1dbf6eb140e5dda1d3d283b1f46eb1e0e514b85849b5517`  
		Last Modified: Wed, 22 Jan 2025 19:36:06 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a186cd8add0ecc1a18673d1ec53a3e13800e0ab113284d4b4cdcaf0a7a08e0`  
		Last Modified: Wed, 22 Jan 2025 19:36:04 GMT  
		Size: 76.2 KB (76196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c5f1331bbc6172d43997fcb449fffcdc42697ab4dc4390dce232969c685936`  
		Last Modified: Wed, 22 Jan 2025 19:36:04 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6476a3c934c10a19e9c10cb1ac456f4df08264c7fc0a63c4f3d20f75dd149a`  
		Last Modified: Wed, 22 Jan 2025 19:36:14 GMT  
		Size: 188.3 MB (188304960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2462b0a6a2c29d315f31edfb9417a65a5dea03e4a5021280a8b6efa9d4b844a`  
		Last Modified: Wed, 22 Jan 2025 19:36:04 GMT  
		Size: 106.4 KB (106351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087f929618596727e01a666f5552e0c922cb021b4be3859115d5eedf1405ed4b`  
		Last Modified: Wed, 22 Jan 2025 19:36:04 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:eef5d057e767d2cc7079a601009c54e8405565467211580b55c43470cc8fbe1c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309153263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64290a94365e1e7863ab27e909c8c77226f805be30b4c8da0287d3ab56032500`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:02:13 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:02:14 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 15 Jan 2025 18:02:15 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 Jan 2025 18:02:15 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:02:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:02:18 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:02:24 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Wed, 15 Jan 2025 18:02:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 18:02:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cbc892de2553269d86e565381c2ed8d8618fe41aa710b7d0ac315ebcc1961e`  
		Last Modified: Wed, 15 Jan 2025 18:02:35 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe5cee5ef012353b5dc63f18f9d30d09e926ce350542b17eed9fe4e8999be75`  
		Last Modified: Wed, 15 Jan 2025 18:02:35 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568c53f0ddbabdba5d8fa0c2df6c85916b49afb7f303b3b4c13844528108c14d`  
		Last Modified: Wed, 15 Jan 2025 18:02:35 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea32fe9a5342a11326d55bb36b6bf28af5e9c3a1c23598fbf4e28c7d808a1f95`  
		Last Modified: Wed, 15 Jan 2025 18:02:35 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ae0d73bd7c62ae769c16a4ca4aae0bdf275a716f65e667dc65c5688e216c32`  
		Last Modified: Wed, 15 Jan 2025 18:02:34 GMT  
		Size: 75.8 KB (75827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96175f1ce9c2ff1c71e5e4be520ae4131c359ad0b09416595feacec6ac2335`  
		Last Modified: Wed, 15 Jan 2025 18:02:34 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8514ee05e34ad0c2feee1a9671946a0199e2e2020736806627c0bde6f660fd5`  
		Last Modified: Wed, 15 Jan 2025 18:02:44 GMT  
		Size: 188.3 MB (188302328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9d14b783e2b5339d748c57adcb31b15198954b3eb0933d26832d9e168d0a57`  
		Last Modified: Wed, 15 Jan 2025 18:02:34 GMT  
		Size: 107.4 KB (107369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283fa5bd251938a80606759ad6809b95ad9f256be4f25a9d720f7820d45284f5`  
		Last Modified: Wed, 15 Jan 2025 18:02:34 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:1e465d28cdd0beddb8cde35ca5ee92a5a3daf0275fd9479f00ec52d08641cc80
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347268411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a823a83e8b388283a33ffedd37ac1cbaf6314f0c120b23f0b357f6bfea4642d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:54:50 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 17:54:51 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 15 Jan 2025 17:54:51 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 Jan 2025 17:54:52 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 17:54:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 17:54:54 GMT
USER ContainerUser
# Wed, 15 Jan 2025 17:55:01 GMT
COPY dir:52d780064906626480ed3e0e10c20681fda9fbf2926de2858bcee46524c2c3aa in C:\openjdk-17 
# Wed, 15 Jan 2025 17:55:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 17:55:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45bcd7c9b59ff3db2f91eb2b8bb2cd92b1896708f53c56904dd8287837eca93`  
		Last Modified: Wed, 15 Jan 2025 17:55:13 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623944b481f83aaad6ccb0693e07226409ba0376c26604e631fea7dcad843cee`  
		Last Modified: Wed, 15 Jan 2025 17:55:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33069a22dfb29a79372e61861f08168103b0fe16ffd51082aa6a923040a32e33`  
		Last Modified: Wed, 15 Jan 2025 17:55:12 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765a65dec6f570a4f95356120cad3d45801e86bf816ee56444701601639e9875`  
		Last Modified: Wed, 15 Jan 2025 17:55:12 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4559b6df6a7b4442c0841e7e4a8c28b48479923adc8e31df0c5f894c0bb30ec4`  
		Last Modified: Wed, 15 Jan 2025 17:55:10 GMT  
		Size: 72.2 KB (72184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e639da243ffe28a8780e309af93e71cfc8715507a3340f8d8a8a858616fe08`  
		Last Modified: Wed, 15 Jan 2025 17:55:10 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61cbe3b3a5b3111f3440803cde370ae329796513010205f2466a45ae923a4e6`  
		Last Modified: Wed, 15 Jan 2025 17:55:20 GMT  
		Size: 188.3 MB (188301058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7296046628b17a9138021932d78791313d819608dc8770095af2dfb974c6be30`  
		Last Modified: Wed, 15 Jan 2025 17:55:11 GMT  
		Size: 3.6 MB (3621363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a70892ac227898182f9c6b5c7e78a15f405def79900beda472d1061963ff33`  
		Last Modified: Wed, 15 Jan 2025 17:55:10 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
