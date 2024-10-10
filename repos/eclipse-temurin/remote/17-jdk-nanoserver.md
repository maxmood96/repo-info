## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:132a650b956e7978484fcb606a7807af464515ff21fc662d7de8fbc1d5d43c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:719cfd396b27fde604f610b0b5da0ebb17c6f4755a711a1e5b82214ea685e1df
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307115481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5db89b52c23437adb8801a01866f0a47a1bd49a95cea4b8bcf878bc09bd7b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:11:44 GMT
SHELL [cmd /s /c]
# Thu, 10 Oct 2024 00:14:20 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 10 Oct 2024 00:14:21 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 10 Oct 2024 00:14:22 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:14:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Oct 2024 00:14:33 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:14:46 GMT
COPY dir:11f935f87b5561ba9de5a02e585d9b073f4114e9ab1765209f28e6005e01c91d in C:\openjdk-17 
# Thu, 10 Oct 2024 00:15:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Oct 2024 00:15:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96818114ce85fcf68e8af61951767bf11ed374ffe6a9023b6150122fbad46d51`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9349d39233008b4b01a5a45122a3f0ce101ac42823cce0b2c9da4e23bfdcf0`  
		Last Modified: Thu, 10 Oct 2024 00:34:16 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a88948c573f25296e7fb9e5462b405ea1d04275036d0e9e54ff7ccc7ea550`  
		Last Modified: Thu, 10 Oct 2024 00:34:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5027fbf91035446eea340563bf15148e87fae0e401cbb7063f27e45ff85490ec`  
		Last Modified: Thu, 10 Oct 2024 00:34:15 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2fecaf9e2fe9c74149948522974e818e75d31e33d62bafcfcf8026b0059263`  
		Last Modified: Thu, 10 Oct 2024 00:34:14 GMT  
		Size: 76.8 KB (76805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3c15dacadb7611c3a92b206003ff3106b0e55b706fa53067ef20e9924a2906`  
		Last Modified: Thu, 10 Oct 2024 00:34:14 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21dcf35e04cad3dc5e606fdd3495261366992287168e72516f53800ac6d6389`  
		Last Modified: Thu, 10 Oct 2024 00:34:31 GMT  
		Size: 186.5 MB (186459344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc4571395f22963cd727bc997432d7c69e3def67dd8473e1b80788bc9f3c5f7`  
		Last Modified: Thu, 10 Oct 2024 00:34:14 GMT  
		Size: 61.4 KB (61421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc357d3ab8d42bcabce48924e7c24f8a5905381f3f14f3c8fc573ff61a5e1e6a`  
		Last Modified: Thu, 10 Oct 2024 00:34:14 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:45f216aa7a551f8ee0693fc34bd7794473ee89533cf74f1131eeb61599611e19
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345233039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aece579d91320c5f30d3f5deb38b290a6f5826ebbd11a39a983403e62b9225c2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Wed, 09 Oct 2024 23:37:31 GMT
SHELL [cmd /s /c]
# Wed, 09 Oct 2024 23:52:38 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 09 Oct 2024 23:52:38 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Oct 2024 23:52:39 GMT
USER ContainerAdministrator
# Wed, 09 Oct 2024 23:52:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Oct 2024 23:52:49 GMT
USER ContainerUser
# Wed, 09 Oct 2024 23:53:01 GMT
COPY dir:11f935f87b5561ba9de5a02e585d9b073f4114e9ab1765209f28e6005e01c91d in C:\openjdk-17 
# Wed, 09 Oct 2024 23:53:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Oct 2024 23:53:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6adfd98d9a05d48859cfa5f6e1dc162be56797c9e86e7647518192a16af3d27`  
		Last Modified: Thu, 10 Oct 2024 00:20:41 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd5871594ea0edb1cbe05e7b9044e155182eaf5c9ff9fa5e5003755aaf045d3`  
		Last Modified: Thu, 10 Oct 2024 00:26:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b34251fd4c18da8ae9561441a25ac8a0daa460833af4ed83b4241ebcb6dab21`  
		Last Modified: Thu, 10 Oct 2024 00:26:35 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9aa5d601461ab6ddd6030a5b48aa92a7f868c149bae892010555b52b3faa863`  
		Last Modified: Thu, 10 Oct 2024 00:26:34 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce71e9d146261dcf74a7ede1fc033cc346be0af1c36fc62864c309bf46621b17`  
		Last Modified: Thu, 10 Oct 2024 00:26:32 GMT  
		Size: 68.2 KB (68222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d66c591d22da5ec7ed481cc918f39f364764653592e3d3dc7eaf3086bd2078f`  
		Last Modified: Thu, 10 Oct 2024 00:26:32 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28edfd82e8e4a6901bcb9cf3ed4e81263b384103d523f1f6f4229b43b3ec1169`  
		Last Modified: Thu, 10 Oct 2024 00:26:49 GMT  
		Size: 186.5 MB (186459346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90a712c32649f7b52c7ffcb592f75e46a00cf8f2641ab372b6e55c1d10811eb`  
		Last Modified: Thu, 10 Oct 2024 00:26:33 GMT  
		Size: 3.6 MB (3604991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01d9b7fbb2cd28af7fe3fafd9124d2fbb58c5a9f2bb6380ca1e6a808d6f75a6`  
		Last Modified: Thu, 10 Oct 2024 00:26:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
