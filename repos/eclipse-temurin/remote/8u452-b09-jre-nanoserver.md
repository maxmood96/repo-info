## `eclipse-temurin:8u452-b09-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c146814d6605280150d464e78effad4cb98c609b60b64f7bb33bbfe18d2e7552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:8u452-b09-jre-nanoserver` - windows version 10.0.26100.4349; amd64

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

### `eclipse-temurin:8u452-b09-jre-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:9b0dffdb19bd751d51d87119ac5251bf9cc4c756f9505d33651e45fb5cf7e533
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163273523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fae7af5c3584540cdbe57f7972d9b05691b1d949f13c6194f301d1eb13cb54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:12:49 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:12:50 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Tue, 10 Jun 2025 22:12:51 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Jun 2025 22:12:52 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:12:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:12:56 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:12:59 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Tue, 10 Jun 2025 22:13:03 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f85e6b79fb65cee18292553318c63d604abe0339c73efe73eb6ea487d3fd9f`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e93d200952c01b63e15da6669e3af841dc1c5faf762c8cfeb9c5d94473e8013`  
		Last Modified: Tue, 10 Jun 2025 22:13:34 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fa12ccdeef41adda1dbf9ee952b96f601fa91c7f632d3cd87150ecade5eea8`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb0bbbebe9dcf237d903466ce5a4bf5e85f53e0c4b8e226cf30da33b2d13bff`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7e53ab8b13c0ef004ce505ac9b8d800516670d9c1a589f9db51d94f845207`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 76.3 KB (76332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe782cd0fa9a2219a5dadbfd7a3a867d0b7821dae9abdc0c8ebb8d745081780`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d793aeab7ee806a38c6dac21e70a166b2f7fe9e8a3f2893aba1b59ea6a50003`  
		Last Modified: Tue, 10 Jun 2025 22:13:38 GMT  
		Size: 40.6 MB (40552782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4303b2a44a2a8ab8348f10138b78057ad49bbe4e2bcaac9b3ef1bc01d676d55`  
		Last Modified: Tue, 10 Jun 2025 22:13:36 GMT  
		Size: 98.7 KB (98663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
