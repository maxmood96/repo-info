## `eclipse-temurin:17-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:46d421afde1577a6d8305fd00f7c77d73b5e7249995eda42c26a93cdf79a43f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:83426e3110f7e5a842e8c4e1f4c0ee5eecbebefb1affdd4ce955138b3e0339b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381094617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280c5e960e40ca7ea0b34f1a3100f4508716e1fb01a721d07c22a3ccf980ddf3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:19:50 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 10 Sep 2025 22:19:50 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Sep 2025 22:19:51 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:53 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:20:00 GMT
COPY dir:75620c5ae31b24727a476334c04df62052433150d79cd2f45de8191a02ae0b2f in C:\openjdk-17 
# Wed, 10 Sep 2025 22:20:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Sep 2025 22:20:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a0d50a3009ff585dca19000fb117b0eb0a0459c6d47a3211cb6fd822dfd25c`  
		Last Modified: Wed, 10 Sep 2025 22:20:53 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fea2d7f7e9d3b430f289f7035142ffdaf609ffab2847424d07c0b6c56890e28`  
		Last Modified: Wed, 10 Sep 2025 22:20:53 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4aa0bf7dea462cda1d9c83c03d49c79e222e32a777ac740a65a1a41abbb6acb`  
		Last Modified: Wed, 10 Sep 2025 22:20:53 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3c583474c6954937ccb2b064fe2ea59c0073173d270b965cae6b2b99842078`  
		Last Modified: Wed, 10 Sep 2025 22:20:53 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e785d525d64068750fda59f8ee8495ee4d886c34439f16eefac4b66b9e68f4ac`  
		Last Modified: Wed, 10 Sep 2025 22:20:54 GMT  
		Size: 70.4 KB (70411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55697e874b23857f9638575d33fbf5d415bf3cf6a89c19332b8694449a5732d7`  
		Last Modified: Wed, 10 Sep 2025 22:20:54 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680a93dc6ac5d0270f6407eb41c0e98217ba4fbd79527f2027222f7f93637e0c`  
		Last Modified: Thu, 11 Sep 2025 00:14:53 GMT  
		Size: 187.4 MB (187353654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8780790c054ce4daff3b693c00ae71765c087109186baa08093ba300f6072b83`  
		Last Modified: Wed, 10 Sep 2025 22:20:54 GMT  
		Size: 113.3 KB (113341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1491721331cdee315c5ab414cf40f3c494892191bd6265b5fb0c48d3a335e42a`  
		Last Modified: Wed, 10 Sep 2025 22:20:54 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
