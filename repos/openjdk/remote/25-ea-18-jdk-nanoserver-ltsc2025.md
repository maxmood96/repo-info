## `openjdk:25-ea-18-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:c389e0078a15c71360e5b559f2e802d72d4aaa1fd50b28f346e0f9f3bad1c45e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `openjdk:25-ea-18-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull openjdk@sha256:a6512774b41250cff18787e8e7aca33f6e73d209a2addef217ca6e19f25e7a64
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.9 MB (397894213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d496d28050573e9efef08608a41f7387326b66a61a5ae4e985b9a8352ef6d619`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Tue, 15 Apr 2025 00:11:30 GMT
SHELL [cmd /s /c]
# Tue, 15 Apr 2025 00:11:31 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 15 Apr 2025 00:11:32 GMT
USER ContainerAdministrator
# Tue, 15 Apr 2025 00:11:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 15 Apr 2025 00:11:37 GMT
USER ContainerUser
# Tue, 15 Apr 2025 00:11:37 GMT
ENV JAVA_VERSION=25-ea+18
# Tue, 15 Apr 2025 00:11:47 GMT
COPY dir:98e2e7765cda338b9693b53f1f8eb40deb194d41cda93e2a54447c0586fe61ce in C:\openjdk-25 
# Tue, 15 Apr 2025 00:11:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 15 Apr 2025 00:11:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c92a8816458c845e1c38acbbed7a5b38296974bc6ccce98308e7faeb35065fe`  
		Last Modified: Tue, 15 Apr 2025 00:12:01 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c4621c1b331dd14227413f3cd7ba256c8581f844be5d358bc290b8ecd3df76`  
		Last Modified: Tue, 15 Apr 2025 00:12:01 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27ee4fc0e73ae958c8221aebb6b38148562b8df6b3b5513cabf0233ff2c41d7`  
		Last Modified: Tue, 15 Apr 2025 00:12:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c319f476a20131a7cce5f66c00f49bbc38cff2ffd7772fc9d0a98952c8664c7`  
		Last Modified: Tue, 15 Apr 2025 00:12:01 GMT  
		Size: 76.4 KB (76370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2d91d0a6b0f453caac6cb0c0df8ec36b3dc7a92f9f8c308baa799ac70c20f4`  
		Last Modified: Tue, 15 Apr 2025 00:11:59 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd611c834100d3169468087de28f85f37f4735b9d5d687591b5456e702dd951`  
		Last Modified: Tue, 15 Apr 2025 00:11:59 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2bab82f63489b1b97021b7fc3780d90207f4bcee1e1587763d644eeeb3d60e`  
		Last Modified: Tue, 15 Apr 2025 00:12:12 GMT  
		Size: 207.6 MB (207583637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40305a7109de88bd6911e9cbfffa6e29b0f9296177393852ee5c6eb2fbb8aa1`  
		Last Modified: Tue, 15 Apr 2025 00:11:59 GMT  
		Size: 114.6 KB (114636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0da520c141fd52cf997d1d264ea7668620f028d4ab4604bc15a320b12ee2b1`  
		Last Modified: Tue, 15 Apr 2025 00:11:59 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
