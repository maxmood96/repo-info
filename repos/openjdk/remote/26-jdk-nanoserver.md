## `openjdk:26-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:0c27077ac6263fa55aa5f2ce57a2c73623a3e1b4a34988f7b1b194b4055d314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-jdk-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:55ed7ddc2d500dd6f8fe42a8b33712db8fafb5905b1611458992622593824803
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410704978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bb50394e366dba206b4e0f5a06e102b90c16a07716a197e85ba6fa325cee85`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Sat, 21 Jun 2025 01:14:08 GMT
SHELL [cmd /s /c]
# Sat, 21 Jun 2025 01:14:09 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 21 Jun 2025 01:14:10 GMT
USER ContainerAdministrator
# Sat, 21 Jun 2025 01:14:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 21 Jun 2025 01:14:13 GMT
USER ContainerUser
# Sat, 21 Jun 2025 01:14:14 GMT
ENV JAVA_VERSION=26-ea+3
# Sat, 21 Jun 2025 01:14:22 GMT
COPY dir:b52ef9dbe4c9943445d4965998b2dc917b23121cc15ee03d8e7d3bffb0fe3291 in C:\openjdk-26 
# Sat, 21 Jun 2025 01:14:29 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 21 Jun 2025 01:14:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2f1595abe304398cf3019810ab62391b22aa6be985ce77b20e762607ac6db7`  
		Last Modified: Sat, 21 Jun 2025 01:15:27 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cad1e8366306e07b63e8c5c0a3cf3a87954dd70a39d987d11d1261c4154f0c5`  
		Last Modified: Sat, 21 Jun 2025 01:15:28 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44378312838c3e93cb83e1af5faafe41c008d98c8306c9abb3a7fa85a9eb10d`  
		Last Modified: Sat, 21 Jun 2025 01:15:28 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8721479056f0bc9d2dfb66a74b1c872057cc0f42dc3ed9d91fbc33016096a`  
		Last Modified: Sat, 21 Jun 2025 01:15:28 GMT  
		Size: 76.7 KB (76677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5821db25250ba70e78a55286c85d2a12b57f48c43de42956ddac4deaa2409756`  
		Last Modified: Sat, 21 Jun 2025 01:15:28 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af65ce9c6a4f8e230d5ce894f95f68762dd7c97c062f75059aa1e9b4fb47e8b2`  
		Last Modified: Sat, 21 Jun 2025 01:15:28 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d7f23fca761c6b23c56a4af6c43b77421b348c5b84b21282f2f78972fc61bf`  
		Last Modified: Sat, 21 Jun 2025 03:26:04 GMT  
		Size: 218.4 MB (218425146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400c9e65711b36dd25526e355ee1be284ff40e02dc45744ee67bbf025f4a655f`  
		Last Modified: Sat, 21 Jun 2025 01:15:28 GMT  
		Size: 114.2 KB (114196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cff6ea60e37f3e7ed2553a2ec298887d0a4123facbb64492597cc4979ce0bdf`  
		Last Modified: Sat, 21 Jun 2025 01:15:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:bf5bf79ed5d7203430400d1abacea82e74d06c573bd3ff0629da875da8513c81
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341142523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4752cd10c1c76d4dc71aedf75f2d38a8eec1c63ebff1dd098430925384ab0036`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Sat, 21 Jun 2025 01:08:09 GMT
SHELL [cmd /s /c]
# Sat, 21 Jun 2025 01:08:10 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 21 Jun 2025 01:08:11 GMT
USER ContainerAdministrator
# Sat, 21 Jun 2025 01:08:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 21 Jun 2025 01:08:20 GMT
USER ContainerUser
# Sat, 21 Jun 2025 01:08:20 GMT
ENV JAVA_VERSION=26-ea+3
# Sat, 21 Jun 2025 01:08:29 GMT
COPY dir:b52ef9dbe4c9943445d4965998b2dc917b23121cc15ee03d8e7d3bffb0fe3291 in C:\openjdk-26 
# Sat, 21 Jun 2025 01:08:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 21 Jun 2025 01:08:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeb1c99ff6235300473a98ed7ee280b76e2d1250c15f8d6075c6ca87471adde`  
		Last Modified: Sat, 21 Jun 2025 01:15:35 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2651848c779db5c5622dfd103b39df87e5e29c53d957a4ae653efc982bc4dc8`  
		Last Modified: Sat, 21 Jun 2025 01:15:37 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d515e30d9a97a809f527e5349952c5618be40497ab838a1b631d6238e3565`  
		Last Modified: Sat, 21 Jun 2025 01:15:42 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5da6d2f5c6f61dff8eb846dedb2d0dc3a1e665ba1a27e8a841967238521a58e`  
		Last Modified: Sat, 21 Jun 2025 01:15:44 GMT  
		Size: 73.4 KB (73436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dfe7e8f0064ad2ff811a761edddfbb271dfdab3a88a57ce3ce544a5bfef80b`  
		Last Modified: Sat, 21 Jun 2025 01:15:48 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244d445adf0a9da2c9c00254c2dd090e097f8351bd93b8fde76ba1c35586e8bb`  
		Last Modified: Sat, 21 Jun 2025 01:15:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da902566499d1780b495502bd9d9f89841514f978ea593aa13f618c104702aec`  
		Last Modified: Sat, 21 Jun 2025 03:26:08 GMT  
		Size: 218.4 MB (218424355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178a28652e4d5f248ca6b85d16dd8c7d89a8972b58a0d9a9941659eb4b67d9c7`  
		Last Modified: Sat, 21 Jun 2025 01:15:56 GMT  
		Size: 98.0 KB (97989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8910c94977d5d34b1f190e2a3947e51832fffc8ee9df3cb650c023e1f073f8f6`  
		Last Modified: Sat, 21 Jun 2025 01:15:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
