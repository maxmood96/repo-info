## `openjdk:25-ea-20-nanoserver-1809`

```console
$ docker pull openjdk@sha256:5aba8888d19baf50dcd65a054ff105d99f10178084193bcc8c85e1c545cdc317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-20-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:c422d62d23a367e3db494571eb42614bcf4f9f404619a22a6991a27bf729f3f8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320886455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da393a71d1888952b8e5b00dc1a53674ec2a297d3767046b9ef0af5c4cc3e752`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 22:16:38 GMT
SHELL [cmd /s /c]
# Fri, 25 Apr 2025 22:16:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 22:16:40 GMT
USER ContainerAdministrator
# Fri, 25 Apr 2025 22:17:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 25 Apr 2025 22:17:01 GMT
USER ContainerUser
# Fri, 25 Apr 2025 22:17:02 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 22:17:09 GMT
COPY dir:68bac63248f06b5a3c6e48fd170d3fc54c730eec81f70554d15d79ed34fe2288 in C:\openjdk-25 
# Fri, 25 Apr 2025 22:17:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 25 Apr 2025 22:17:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4124e28a2a84c691d98069fd4db717fb9f662ef91e62ee2368f5e3a2d36b6e2d`  
		Last Modified: Fri, 25 Apr 2025 22:17:21 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4371229a096d4b461b2835dc2475cc1209d0ee06121fc6c98a3049b1e6631bb`  
		Last Modified: Fri, 25 Apr 2025 22:17:21 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762469014b03799043b4eaadf732e0c53db37928faebfa5e249f7d9bea79ce9c`  
		Last Modified: Fri, 25 Apr 2025 22:17:21 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b1ab208e5df793b1e52d074b57d8fa317786a78f36ba5afe019ef25f82c5bb`  
		Last Modified: Fri, 25 Apr 2025 22:17:21 GMT  
		Size: 68.3 KB (68301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113dbddb03b847a01262ccf7d870307c5e743a317ab502d26f384e6ee12addac`  
		Last Modified: Fri, 25 Apr 2025 22:17:20 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2326e7bd1a74ca5ee071f27a498759857ba18b4098fb8726cdcbcc1a443d628c`  
		Last Modified: Fri, 25 Apr 2025 22:17:20 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512a99d0df04a385ce7dbfa73418d7be09dab45faf4be268942817a1fe444526`  
		Last Modified: Fri, 25 Apr 2025 22:17:31 GMT  
		Size: 207.7 MB (207700826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96991270863c6a793cccd5f9ec418bf4f77dfe5175bd73bff0caf0c7358445f8`  
		Last Modified: Fri, 25 Apr 2025 22:17:20 GMT  
		Size: 4.4 MB (4358473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c05f6048f5485de612fb39fed95bc4ff45b408a445a995a94631c496e1aab18`  
		Last Modified: Fri, 25 Apr 2025 22:17:20 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
