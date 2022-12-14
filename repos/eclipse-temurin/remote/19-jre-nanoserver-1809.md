## `eclipse-temurin:19-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9abe744d8fe82256155a106fa97d73fef799f84f389c27b5aa7d1980b36d47c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `eclipse-temurin:19-jre-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull eclipse-temurin@sha256:4d1535dcea0d493b07255c2a22a7e797514b538fef2ad0d20d33fa14d6517209
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155054650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e774d82a67ce35bade4ccb265bff3a4a26fe0cd676209d9cd5b98d01135827`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 23:35:34 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 13 Dec 2022 23:35:35 GMT
ENV JAVA_HOME=C:\openjdk-19
# Tue, 13 Dec 2022 23:35:36 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 23:35:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 23:35:56 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:41:54 GMT
COPY dir:f8bde2ca36462d5d41624c06c50c3ec39051aaa6a88f0dabf8bb55af828f5608 in C:\openjdk-19 
# Tue, 13 Dec 2022 23:42:12 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fe06cbef5ac46e54edd743daf1bc2bfa36b294c7ce9104837061c41a4bde7b`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f68b7e885d66ed0eba48bb193bccb7968801a474086ceeecbc25665892cde1d`  
		Last Modified: Wed, 14 Dec 2022 00:06:06 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64569820ddd6825d74fb1ad26e95851b8358d6836281b2a09b4ebe01e25fabd`  
		Last Modified: Wed, 14 Dec 2022 00:06:06 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5b28f89e2d26cf7dfaffe0be35abbd6bcc331cdbf20ea0a3811adf4b5acee1`  
		Last Modified: Wed, 14 Dec 2022 00:06:06 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b5e793b324e97df4319acd05cbf59f60f752cb4604a25ca98bdd558db8b411`  
		Last Modified: Wed, 14 Dec 2022 00:06:04 GMT  
		Size: 65.0 KB (65022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ca2ea22a1e64ac9f75d13c73b4cc2fc0c406034f89fcd74164f2efb677de9e`  
		Last Modified: Wed, 14 Dec 2022 00:06:04 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c440fef674fb3380485d10d1b20e6ce1d9034cd8981cef4694dbabe0dd54bede`  
		Last Modified: Wed, 14 Dec 2022 00:07:32 GMT  
		Size: 45.2 MB (45228891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0462ca92e8c041b8d8048d07838cd02ef8614e4f34df453d440a5db9d1299`  
		Last Modified: Wed, 14 Dec 2022 00:07:23 GMT  
		Size: 3.1 MB (3083908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
