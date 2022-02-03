## `openjdk:8u322-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:d9ac597afa3a776d17bf13538f1003569ae3dd1b9371bdbd47b629fb99de141a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:8u322-jre-nanoserver-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:3955d26e38ae647088236ea840ea09f70bd0d112a1f290a1af70d18dee28fe8d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141472692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e431363fa745829915449e017a57e2f46004493d93e5225e8c920d116211882`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Wed, 19 Jan 2022 22:25:45 GMT
SHELL [cmd /s /c]
# Wed, 19 Jan 2022 22:39:29 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 19 Jan 2022 22:39:30 GMT
USER ContainerAdministrator
# Wed, 19 Jan 2022 22:39:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 19 Jan 2022 22:39:39 GMT
USER ContainerUser
# Thu, 03 Feb 2022 20:27:17 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:30:30 GMT
COPY dir:f4c77e4259f68c5f890bc7ab442034fb0a5366735393f4c5400d26f276285797 in C:\openjdk-8 
# Thu, 03 Feb 2022 20:30:45 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a1b3e13bb7b3d4b61b5f49a91d6eb9bfcf5539ab89c3687d608f17713c2409b5`  
		Last Modified: Thu, 20 Jan 2022 02:21:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338bf0e38fb7f2b8a0fb5e7eb7fab0a55b72f807f8f29e8a8cca893d27d9a3a8`  
		Last Modified: Thu, 20 Jan 2022 02:42:25 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad2e28cd185f66eb0db90aedacf18508ccfd1a587b64c68b818e6a6ccf36580`  
		Last Modified: Thu, 20 Jan 2022 02:42:25 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734a1268ea949016e9c473f5bdb78cb61ed8fe90ee65b5ba7b2ebd765496205`  
		Last Modified: Thu, 20 Jan 2022 02:42:23 GMT  
		Size: 70.7 KB (70719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d88295d21d31aa302a0382ecc8affcdb2d99175e66a11a9467f383a411d75e`  
		Last Modified: Thu, 20 Jan 2022 02:42:23 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0648c8a62783a7b11fca5e2be3809acab53076a9a7d0222b50c4b3b7d67a17a`  
		Last Modified: Thu, 03 Feb 2022 21:29:54 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eab474ff8c69c8d47cb63a8845809cd96db5e24b4360e2f07ec6fc5f5e0e33`  
		Last Modified: Thu, 03 Feb 2022 21:31:37 GMT  
		Size: 38.3 MB (38267902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9233a5bec3144ac6faec0a07a72b731f9c1a367ab0d3652d0016a2bd7b325d44`  
		Last Modified: Thu, 03 Feb 2022 21:31:31 GMT  
		Size: 81.8 KB (81847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
