## `openjdk:23-ea-34-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e2db5909f37f3fe968b8169784467263307a90c8ab6d1e1aa2d5852ce0ef8002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-ea-34-jdk-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:0c268edcd10a94170c392d71107772b4d3d0b8756cd12937561f52c8c005fabf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365292937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510bddc081a0411bb175f906088abb33d05e2e17cc27771e7d90cd839ffbcc67`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Mon, 29 Jul 2024 18:57:06 GMT
SHELL [cmd /s /c]
# Mon, 29 Jul 2024 18:57:08 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 29 Jul 2024 18:57:09 GMT
USER ContainerAdministrator
# Mon, 29 Jul 2024 18:57:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 29 Jul 2024 18:57:20 GMT
USER ContainerUser
# Mon, 29 Jul 2024 18:57:21 GMT
ENV JAVA_VERSION=23-ea+34
# Mon, 29 Jul 2024 18:57:28 GMT
COPY dir:0c6632ca01b1fe80b52aaec8170c9d58d97f7c37632491f9ebb4a70acbe454d7 in C:\openjdk-23 
# Mon, 29 Jul 2024 18:57:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 29 Jul 2024 18:57:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc1eb3a682c9bd292feeadee8fef3a7afcd768f0153e7ac38de2e23df70a9a`  
		Last Modified: Mon, 29 Jul 2024 18:57:42 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dd4539471f3f8edb5b95ee3ce02b73574d6999df05115fe1d27875044286e0`  
		Last Modified: Mon, 29 Jul 2024 18:57:41 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934565c8310aeee2bf979e098359ba39f67108d0e4b4012b8af114bb3711fbb0`  
		Last Modified: Mon, 29 Jul 2024 18:57:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bb586337c1fb94ff68d559d45af957497c45a4abbc48e3bc72b1424af67d67`  
		Last Modified: Mon, 29 Jul 2024 18:57:41 GMT  
		Size: 67.5 KB (67544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ee392e8b72464ce372d759dfd2b2134d9afc565ed08567313376e770be0262`  
		Last Modified: Mon, 29 Jul 2024 18:57:39 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c111f1324c12beea99c1979a0304aa40ad3bdf6190a09f1e7782aab9f5861632`  
		Last Modified: Mon, 29 Jul 2024 18:57:39 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29065cf367b6b0806347a1c472bc5d95829a97fcd87e7281d75c1defbf9ae5a8`  
		Last Modified: Mon, 29 Jul 2024 18:57:51 GMT  
		Size: 206.0 MB (206046690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33cafa55aa2ec1a89d7489dcbe0128536e6bc55e4aee26cc2f6489c724d32af`  
		Last Modified: Mon, 29 Jul 2024 18:57:40 GMT  
		Size: 4.1 MB (4091048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d143b1a2aafc4b75c5c32f40710c8eaea17c6cedff37a7bce18e43d9d3b77e2b`  
		Last Modified: Mon, 29 Jul 2024 18:57:39 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
