## `openjdk:28-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:1631502fd92853db50b94fb0852d28777d006ebce8c75dde69a48a9cacf70e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-jdk-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:4e792ab83f62c6d4fca61a6a4c82e7aeb421f22040c3b444deb1a8168ddcaf87
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (420001796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328b68a5138d7ff91a82327e08f70fb023f9b4bd8f5560f0566c8d410630bfe4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Wed, 10 Jun 2026 20:37:26 GMT
SHELL [cmd /s /c]
# Wed, 10 Jun 2026 20:37:26 GMT
ENV JAVA_HOME=C:\openjdk-28
# Wed, 10 Jun 2026 20:37:26 GMT
USER ContainerAdministrator
# Wed, 10 Jun 2026 20:37:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Jun 2026 20:37:37 GMT
USER ContainerUser
# Wed, 10 Jun 2026 20:37:38 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:38:41 GMT
COPY dir:d3edd7f11c25bc3efe911cc2f0cdaa199b881a543047f3cee13829105446f724 in C:\openjdk-28 
# Wed, 10 Jun 2026 20:38:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Jun 2026 20:38:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9cd76f1a8e9075785a90ec96b1391aa04deb1553efba6e94c71f59f9bb8662`  
		Last Modified: Wed, 10 Jun 2026 20:38:55 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ef2c4be72a6dece2f57ee3d02aaebbc91841bcceaf7f3b4960460866fcac96`  
		Last Modified: Wed, 10 Jun 2026 20:38:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af78c60fd9623301d902ff4f943967362fcf3273155dfcc3304dd364824829a1`  
		Last Modified: Wed, 10 Jun 2026 20:38:55 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2a91342c8a4e011ceed3d2391a98134c906e80062f7775eb08930a5bdc2ac`  
		Last Modified: Wed, 10 Jun 2026 20:38:55 GMT  
		Size: 69.4 KB (69423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d94bf4af515e1dd9dfe37aa4443d93b56853e3eac2b4f4b0787ecc36d5cea2a`  
		Last Modified: Wed, 10 Jun 2026 20:38:53 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9eb7f2fc6613c5698cd1f262ab32a85e419fa73963e4d17705bcaea8b94a49`  
		Last Modified: Wed, 10 Jun 2026 20:38:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610c6743864cc88f32a795377adbb3b66980d56306837bba3e794251b24c77d4`  
		Last Modified: Wed, 10 Jun 2026 20:39:07 GMT  
		Size: 223.2 MB (223165114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2ba13f15997f18680f55b85e3623deeab03e25b722828c7eff261d62e3aa7b`  
		Last Modified: Wed, 10 Jun 2026 20:38:53 GMT  
		Size: 92.8 KB (92820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698f25fe0462bc718434df84af16db6f6eebd6156a2264b9fc414f7c3fae067`  
		Last Modified: Wed, 10 Jun 2026 20:38:53 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:28-ea-jdk-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:431d16f6f70eed8a1a072a485a388cf53c5d16a97146bc8d3147f8dc240a567c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347352292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5b23b5dc850a970f9226f8935aab71d8079559513d1be1b489842c31353fad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Wed, 10 Jun 2026 20:37:41 GMT
SHELL [cmd /s /c]
# Wed, 10 Jun 2026 20:37:41 GMT
ENV JAVA_HOME=C:\openjdk-28
# Wed, 10 Jun 2026 20:37:42 GMT
USER ContainerAdministrator
# Wed, 10 Jun 2026 20:37:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Jun 2026 20:37:43 GMT
USER ContainerUser
# Wed, 10 Jun 2026 20:37:44 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:38:46 GMT
COPY dir:d3edd7f11c25bc3efe911cc2f0cdaa199b881a543047f3cee13829105446f724 in C:\openjdk-28 
# Wed, 10 Jun 2026 20:38:51 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Jun 2026 20:38:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcac46283eacfa1c1f5138d1699de36de9bd8dc8bbbcfe7799bd365c9ae41d7c`  
		Last Modified: Wed, 10 Jun 2026 20:38:57 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812f2d8fabaa518cfd710755103e27516edb40c323564450451994566f6a526e`  
		Last Modified: Wed, 10 Jun 2026 20:38:57 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d1e027205b4480ad94250667016d04e068e201edd23e6aad00af17656dfb8d`  
		Last Modified: Wed, 10 Jun 2026 20:38:57 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b494e90435458bea55015ba9ecb51038e4cfd83ec5e346c0c2bff504adf4fd25`  
		Last Modified: Wed, 10 Jun 2026 20:38:57 GMT  
		Size: 76.6 KB (76627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eae2ef31d15affa54741f0894d5213678164f825fff2fce35b6fb3b96a5201`  
		Last Modified: Wed, 10 Jun 2026 20:38:55 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786488257f2115f85f324a7137108d1cbc06c52b544a1f1bf44590d57b58b720`  
		Last Modified: Wed, 10 Jun 2026 20:38:55 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e5bb46d36897aac9ed41905b02c36aa05f45a31b2f6d2b0682e5e7615aecc7`  
		Last Modified: Wed, 10 Jun 2026 20:39:10 GMT  
		Size: 223.2 MB (223165040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d45143502a0473ebed07393fe00269d6504852ecc35e9f6f0c32501c2d69470`  
		Last Modified: Wed, 10 Jun 2026 20:38:55 GMT  
		Size: 106.8 KB (106790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636490db7b7f6cbabb6b753632b180a17db413aff0408f3aa3b0e8ea9102db20`  
		Last Modified: Wed, 10 Jun 2026 20:38:55 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
