## `eclipse-temurin:8-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:299b54ab57fd2bef71f014ba879ad4052e7c74b94553f000774d17c42756fcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8-nanoserver-1809` - windows version 10.0.17763.6775; amd64

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
