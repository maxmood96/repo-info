## `openjdk:26-ea-3-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:bd31bac2c13d07e282d3ce217b1bdae53467d7609a96fe9836c36d44f463ffb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:26-ea-3-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

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
