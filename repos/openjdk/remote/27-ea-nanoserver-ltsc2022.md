## `openjdk:27-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:c19ab5b0ea00a90074d1cd456e07978a5f63dd61770de11220bedd71545b32d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:18af2af9411b81670990374130875256f10177990422f2952df3076f653c40a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350271176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c71d4b56c720deb8a09c9cf50bb522291be0b11f29dd73504feb9648d81c1b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 08:17:34 GMT
SHELL [cmd /s /c]
# Tue, 02 Jun 2026 08:17:37 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 02 Jun 2026 08:17:39 GMT
USER ContainerAdministrator
# Tue, 02 Jun 2026 08:17:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Jun 2026 08:17:59 GMT
USER ContainerUser
# Tue, 02 Jun 2026 08:18:00 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 08:19:55 GMT
COPY dir:548e2ff91354155ccc5ff2b06e6682160bdc15feb1f883e9b2a88ea1d455bbac in C:\openjdk-27 
# Tue, 02 Jun 2026 08:20:07 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Jun 2026 08:20:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782992fa9978ec2f51b99320653fff9dab2b7c77299a32693d0c0b082a303c4c`  
		Last Modified: Tue, 02 Jun 2026 08:20:14 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5797422af52a581cc9c9eeb1fc057e31485285be218dba1eeb319fdf43e817`  
		Last Modified: Tue, 02 Jun 2026 08:20:14 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774acd8c5222949bd1648c6ce35974a18d0c840080c74a0be75b851584cb866`  
		Last Modified: Tue, 02 Jun 2026 08:20:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e894b1743bfa76f05cf5236f1949479958a269216b2d4faa9fd869dd9a0adb1`  
		Last Modified: Tue, 02 Jun 2026 08:20:14 GMT  
		Size: 72.8 KB (72803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae81b1c58cc2fc6f3076d7231d84664f4167bf5a9625bc9f23e2b7db5352ac71`  
		Last Modified: Tue, 02 Jun 2026 08:20:12 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb03b05c5824ffe7aeabaf0aea93d59a2c039e0f81597df91a25d8557d85b25c`  
		Last Modified: Tue, 02 Jun 2026 08:20:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689c6f5af23a22ebb4b1afafa759e8d3cec999319dbbd61d5a2be1b33a219129`  
		Last Modified: Tue, 02 Jun 2026 08:20:27 GMT  
		Size: 223.0 MB (223026333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9732d5c32e22b322d853145a82b3f0244bb540b68edcd1cb418c6261a018600`  
		Last Modified: Tue, 02 Jun 2026 08:20:12 GMT  
		Size: 126.9 KB (126910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0355085c9c658bf1974a0fd8bb02aad365c97707568da9f52efcd1bfac7913`  
		Last Modified: Tue, 02 Jun 2026 08:20:12 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
