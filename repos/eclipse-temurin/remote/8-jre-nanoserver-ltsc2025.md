## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d83f7ec529dddc8c38156c04364c686e8d43438a8db12e06818f948b682f8fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:7cad01c858dfc33019ef2785e6497856e6b4bd22dc224fdec28c19b429cc55d7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232810596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24eac56440f22268180952c9131017a386333dc4bcd6dc228a06d06be798ae6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:15:42 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:15:43 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Tue, 10 Jun 2025 22:15:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Jun 2025 22:15:45 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:15:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:15:50 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:15:53 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Tue, 10 Jun 2025 22:15:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59be36b211c7952083b5dcff6187c70769056ca6a184f565834867f9ef2419e6`  
		Last Modified: Tue, 10 Jun 2025 22:16:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6e2ef9c033aa68d2f6262f426d4896b3eecf16866f3a606d2c6ede0c68921a`  
		Last Modified: Tue, 10 Jun 2025 22:16:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d609bfbfe3bd5f31fc13d329ed03d0f02a3446b6f15bd39e774a684df015f26`  
		Last Modified: Tue, 10 Jun 2025 22:16:46 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8129b20168e437dc1b12bdb0e922409009549f08f4357fe5026851b8d4cb13c2`  
		Last Modified: Tue, 10 Jun 2025 22:16:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd17fe77e8055d10c4de96919f9a44647f7f652adb9b60dcea8e318fa633bc68`  
		Last Modified: Tue, 10 Jun 2025 22:16:46 GMT  
		Size: 76.4 KB (76424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c25dea6588dca4334f1f85ea600484bb79303ed7717ea321c8024a837a3fa1`  
		Last Modified: Tue, 10 Jun 2025 22:16:46 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e740c96d1619c432e7e41dfd74f10d874f410a1c47c05dfa9dc2f0e279598fc8`  
		Last Modified: Tue, 10 Jun 2025 22:16:49 GMT  
		Size: 40.6 MB (40554088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f769b08f52ad6880befda6d17c508cfd6809dd5e79a5c3f18b5d28280b621d9`  
		Last Modified: Tue, 10 Jun 2025 22:16:47 GMT  
		Size: 92.3 KB (92251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
