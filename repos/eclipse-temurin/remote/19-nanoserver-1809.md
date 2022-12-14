## `eclipse-temurin:19-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:7445bfabc8a7a4cc31ee40db2987fd902d36796154e35963e2ba49dddf3aba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `eclipse-temurin:19-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull eclipse-temurin@sha256:1df280bda262e0dcdd16f443faad7291f78c7bb1bc1f125b44b79c9e820b4638
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303905895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5be30518bb4455815b706081e2ed37c862f7058d4611b21793cc9b506bde661`
-	Default Command: `["jshell"]`
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
# Tue, 13 Dec 2022 23:36:13 GMT
COPY dir:2282de048661e89f3c315adc23c8954e0ca245f9a969462117712d8342758a69 in C:\openjdk-19 
# Tue, 13 Dec 2022 23:36:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Dec 2022 23:36:41 GMT
CMD ["jshell"]
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
	-	`sha256:09a166778a72f6a318845c26c9e297fd069244137ea475c14e975a6ddc13a38f`  
		Last Modified: Wed, 14 Dec 2022 00:06:27 GMT  
		Size: 193.4 MB (193446340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf2ee59f2df6e7a10c57d23ace5f4a44120a64d6809d093b82cbd55ab83dbbe`  
		Last Modified: Wed, 14 Dec 2022 00:06:05 GMT  
		Size: 3.7 MB (3716537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0e076d5af4e655c451811d154dcc895c6f7856683938da043f9ec1e3dfe1bb`  
		Last Modified: Wed, 14 Dec 2022 00:06:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
