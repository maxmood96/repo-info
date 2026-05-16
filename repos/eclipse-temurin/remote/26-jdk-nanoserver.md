## `eclipse-temurin:26-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1fb0dbbc1783e283d8688baa97d617e33d050c36ce5112648f3e0889a7e75175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:26-jdk-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:56d97b28c236ddcb6d44becb7c0446d8c729f4233502f879d9dfba23998c9ae0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341200559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0eee892022538cd6601053eead34c3b366af7c4991eb7a4f2bcd3de941fdc5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Fri, 15 May 2026 21:40:59 GMT
SHELL [cmd /s /c]
# Fri, 15 May 2026 21:41:00 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 21:41:01 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 15 May 2026 21:41:02 GMT
USER ContainerAdministrator
# Fri, 15 May 2026 21:41:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 15 May 2026 21:41:11 GMT
USER ContainerUser
# Fri, 15 May 2026 21:41:47 GMT
COPY dir:254440c2db85c674475ced33fb249e9ba634466f55592d23f645db2e3bf929d7 in C:\openjdk-26 
# Fri, 15 May 2026 21:41:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 15 May 2026 21:41:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1624a7ff6f133ceaffbc4fa612ac6af6e294db3bcabc0af5f7cae5e6a348f996`  
		Last Modified: Fri, 15 May 2026 21:41:59 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb1d296036f492a21e660ed143bf50a5dee9fa9b6401503f5f780d0702410fe`  
		Last Modified: Fri, 15 May 2026 21:41:59 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf92a1f8b1d327ba854f9069f8ee81299e346417c0c111a914e3ffa167cfd036`  
		Last Modified: Fri, 15 May 2026 21:41:59 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ddf1ef13491fb27812f7cb1776cbe4a2da843ae2476a8fea4606ef34e5fea1`  
		Last Modified: Fri, 15 May 2026 21:41:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d3f043b3abbf0102c54812587297161bb09f0f45b54a874aeaf09d825aba95`  
		Last Modified: Fri, 15 May 2026 21:41:57 GMT  
		Size: 69.8 KB (69761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2996d419519f46db7d79fc0988db54a7549f213dc0358026a659a52b448b260`  
		Last Modified: Fri, 15 May 2026 21:41:57 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c8d8c855fdceeb1b491ff467f9fa3632e304c6f122471cb0d78a05b3c0c999`  
		Last Modified: Fri, 15 May 2026 21:42:09 GMT  
		Size: 141.3 MB (141273193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f4a948b97ec5149a27b59a9d2bc558407f18c64a5e90efa2b11a20b78857a1`  
		Last Modified: Fri, 15 May 2026 21:41:57 GMT  
		Size: 112.4 KB (112373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43f09983172725b5f799ec39bba2bf1d5408f020123fb44b9d151ebc0950ad7`  
		Last Modified: Fri, 15 May 2026 21:41:57 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:26-jdk-nanoserver` - windows version 10.0.20348.5139; amd64

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
