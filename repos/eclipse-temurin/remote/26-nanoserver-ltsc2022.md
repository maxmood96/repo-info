## `eclipse-temurin:26-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7691d93b8c231aeb193c41602ca0bb3aab5d7be0f823626ef1179eb3a21ea9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:26-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:69992fa8dab44ecb742f0e6867bc4e913bed0b15ba9810e22638b31ecdaee9c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268488485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef61a110667cb88f1bbf992dff4d52d20ab5027c5e2b3beefd7b31fc44a56bfd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Fri, 15 May 2026 21:25:56 GMT
SHELL [cmd /s /c]
# Fri, 15 May 2026 21:25:59 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 21:25:59 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 15 May 2026 21:26:00 GMT
USER ContainerAdministrator
# Fri, 15 May 2026 21:26:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 15 May 2026 21:26:18 GMT
USER ContainerUser
# Fri, 15 May 2026 21:27:02 GMT
COPY dir:254440c2db85c674475ced33fb249e9ba634466f55592d23f645db2e3bf929d7 in C:\openjdk-26 
# Fri, 15 May 2026 21:27:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 15 May 2026 21:27:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb8e31ecd6facd70d76050945945bacc13c73575e37bcfbdacaa45ee57464c7`  
		Last Modified: Fri, 15 May 2026 21:27:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829dc88c2fb8d4e0d01dc63423d0af4225fb189b2ba60044705806b26e7aefc8`  
		Last Modified: Fri, 15 May 2026 21:27:14 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a52b5332ded073489aa2b022ddc2cf5e2625a9a12477d8b2646547c036e75e`  
		Last Modified: Fri, 15 May 2026 21:27:14 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d757993bdb31e2d63ea20d1ab1b3f100c7f15e21b4470c98818111bff54726df`  
		Last Modified: Fri, 15 May 2026 21:27:14 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da892f725214a39549711267bc98d2d13bcf12204e888de04749a0ff4e545af`  
		Last Modified: Fri, 15 May 2026 21:27:13 GMT  
		Size: 72.4 KB (72400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8510a82094720d352b84ddcb6bc6dd120fb8043d760b63802a7923c700350c7b`  
		Last Modified: Fri, 15 May 2026 21:27:12 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21c396dc8d16145327bdc204c4d28712a14120124f4f525d2f6ec16bb1dfb4c`  
		Last Modified: Fri, 15 May 2026 21:27:25 GMT  
		Size: 141.3 MB (141273284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d938ba893f6c4176b006867c2dd7b49cf0f4af893c5771f9ff3100a0260fb584`  
		Last Modified: Fri, 15 May 2026 21:27:12 GMT  
		Size: 97.6 KB (97629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f6993caee6172b63407e0c4b50540395fbe97efc97a2bcf37af87184713765`  
		Last Modified: Fri, 15 May 2026 21:27:12 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
