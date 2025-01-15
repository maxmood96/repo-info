## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0a10e6889b2861f4095e71d410cf77d7bbd4565a99fc166ecd7a8e3ff52e7d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:d4e15a9ca10f427fe0c5234c8abf65ee94b29da726f2363813f6cbe83bbd5a20
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224292648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a5ad562173a7b4af3584dc1d0efdd3d1c444d4f98edb73e95c91104850b028`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:02:30 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:02:31 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 15 Jan 2025 18:02:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jan 2025 18:02:32 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:02:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:02:35 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:02:40 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Wed, 15 Jan 2025 18:02:46 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bf7d6cf291a173fa812b1beea01b48e9be97b2a75c14490a469c618984db3a`  
		Last Modified: Wed, 15 Jan 2025 18:02:49 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57bb3a115fa2576bdff9e75faa66a23ad53f41f6530489574b7bc2b4fa5eec1`  
		Last Modified: Wed, 15 Jan 2025 18:02:49 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559bb460eccf1857d7d32d6e4b8dc47852ec62653182c86b54e14e58b6c10683`  
		Last Modified: Wed, 15 Jan 2025 18:02:49 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96823990206a1573fd9728510119fc912a24ad8a90df2cd525d0593ff6551fda`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b29bf9ae478f5d56de54d9ba9a6f26163b0ac16a538d6390114e5558568594`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 77.5 KB (77453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa17b6c7dcd07f83199b6b962d0756c62c7a643e67edb96e1540e7599353484a`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f506590ab4ef0a508ad36fdbbf73436648edc232fe7b95b1df766d6c9094a931`  
		Last Modified: Wed, 15 Jan 2025 18:02:55 GMT  
		Size: 103.4 MB (103441389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d4fe298da23ecbc4b099b5a78a05449b9dc669493ea2cf1f502fda5675e069`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 107.1 KB (107097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:5e8528682c0c144489fcd6226192a9eda3ea06a31635090596df97ca613a5b34
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258928384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3850a347a06cfd46b6b10b5245df3211b248d21bf13ee4b46223727da904b819`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:51:15 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 17:51:16 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 15 Jan 2025 17:51:16 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jan 2025 17:51:17 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 17:51:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 17:51:19 GMT
USER ContainerUser
# Wed, 15 Jan 2025 17:51:24 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Wed, 15 Jan 2025 17:51:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1034825aa81dbb64c28d9d6964144428070b1cb693ffaa181505189134740331`  
		Last Modified: Wed, 15 Jan 2025 17:51:35 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1306107e680e9ea7ae8b85dd64878d3c10f83034b8d70f1ec8673292bee405d6`  
		Last Modified: Wed, 15 Jan 2025 17:51:34 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b459f117e7484615452bab081ee9a5d402e32a73dc9bce3e92122aaba50ebee`  
		Last Modified: Wed, 15 Jan 2025 17:51:34 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a864ba5ac7209e01661b3ea85eb16c6a92110376b393e025adbc763a8f03d`  
		Last Modified: Wed, 15 Jan 2025 17:51:33 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b1abeb22d7abb840f784b4b02420e5b07235bbcf68f51094d99125071d2c3`  
		Last Modified: Wed, 15 Jan 2025 17:51:33 GMT  
		Size: 74.7 KB (74714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465d791791b3eb7c1779d0c84cc1363c6f75af080aacf2871992c37d1c43ff7`  
		Last Modified: Wed, 15 Jan 2025 17:51:33 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5a28c354836838edfb2db53532b0246496881acab52b9484f00ec7c903e3b9`  
		Last Modified: Wed, 15 Jan 2025 17:51:39 GMT  
		Size: 103.4 MB (103442079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4242736d81026d698e06dfdb2f610a5567f003cb68a48677d7afcb2db545098`  
		Last Modified: Wed, 15 Jan 2025 17:51:33 GMT  
		Size: 138.7 KB (138694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
