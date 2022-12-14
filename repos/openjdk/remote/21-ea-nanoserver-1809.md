## `openjdk:21-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:1726f4da9163bebe4eb28c30f9397953a5678da321af16d3d1d7a8d2813f4000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `openjdk:21-ea-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull openjdk@sha256:c3d1ec828fa4bacafcd791fb1bea30709e9a2906cabdd6a8b647e1de5893074b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304392232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9243d3df1d303736c073c9289b85cebb551ea03d05ada20720efae5b2e78db2b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Wed, 14 Dec 2022 02:56:32 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Dec 2022 02:56:33 GMT
USER ContainerAdministrator
# Wed, 14 Dec 2022 02:57:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Dec 2022 02:57:30 GMT
USER ContainerUser
# Wed, 14 Dec 2022 02:57:31 GMT
ENV JAVA_VERSION=21-ea+1
# Wed, 14 Dec 2022 02:57:51 GMT
COPY dir:458aa16d503862314de3049f27b7a29a28f06f9c00ef58081a4d94b178313b3e in C:\openjdk-21 
# Wed, 14 Dec 2022 02:58:42 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Dec 2022 02:58:43 GMT
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
	-	`sha256:f403eb4656dcd257924d61f24cde07e6a0bd4ea52ceb2fbb6aabbe94c2b76b67`  
		Last Modified: Wed, 14 Dec 2022 08:47:11 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfa39493326e86ec6b2f2fd8125ad183b1ed64b2c3f2a4461f05d827cc0926a`  
		Last Modified: Wed, 14 Dec 2022 08:47:11 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b7523c236c3ef82ccdd5905f89f123933015a7d581e70a248676aa7e3a76df`  
		Last Modified: Wed, 14 Dec 2022 08:47:11 GMT  
		Size: 66.3 KB (66297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063f4c761ac43a960d04eea23db92193fd5460a992bd8ac71186731abb9de13c`  
		Last Modified: Wed, 14 Dec 2022 08:47:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4e2a20b1d19b5f8e9422d47f41843c07bcc34f87b9188900da6d0f4f676d77`  
		Last Modified: Wed, 14 Dec 2022 08:47:09 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4da4141bb8d7df5c6cf5f486d7c9c2a1ee4cff6374ac192a100fd4464c30fed`  
		Last Modified: Wed, 14 Dec 2022 08:47:39 GMT  
		Size: 193.9 MB (193874727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93ab5df9272ddd1d05953e53afd2bbdda44bd886b3801a84218862f1cd5ea20`  
		Last Modified: Wed, 14 Dec 2022 08:47:10 GMT  
		Size: 3.8 MB (3773236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20882526934492afbc0d558009950b8f7c5fe1c477fb951fcfed1d37541adfff`  
		Last Modified: Wed, 14 Dec 2022 08:47:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
