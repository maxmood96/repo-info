## `openjdk:23-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:a4e2423eec64ddcc0582c1284a3b0073043d767f5c12b2ba76d7f0db187d13b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-ea-jdk-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:ff89663cc96d0935db1bf74d10c0feb81c8b631e2c54ada55d20ca57bb711546
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365271255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c32a10b2858d1ddca1586c5c9e82baae4155ea0e0b1c42b32bb6624253d9a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Sat, 22 Jun 2024 02:00:40 GMT
SHELL [cmd /s /c]
# Sat, 22 Jun 2024 02:00:41 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 22 Jun 2024 02:00:42 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 02:00:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 22 Jun 2024 02:00:45 GMT
USER ContainerUser
# Sat, 22 Jun 2024 02:00:45 GMT
ENV JAVA_VERSION=23-ea+28
# Sat, 22 Jun 2024 02:00:52 GMT
COPY dir:395e7ee1a3626bfc5aff610213dcea9d0900e81a370cb9622cb2a5eea997ef1e in C:\openjdk-23 
# Sat, 22 Jun 2024 02:00:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 22 Jun 2024 02:00:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00946c126f7bae823aa7e684c13152870944330b5ec97a3c5d09ba0c1002921c`  
		Last Modified: Sat, 22 Jun 2024 02:01:03 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931dace04661b72b43def6c66b0149f621a7157e4b903df0789fa44d51481ad9`  
		Last Modified: Sat, 22 Jun 2024 02:01:03 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37340f183bd88d2b99c95e630240ee32aff462f1f1e342d4c93de590a87703e`  
		Last Modified: Sat, 22 Jun 2024 02:01:03 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6e689c5ef38fec6fce5780a156cc8d09be8b0218811ad6155d33aada3caa32`  
		Last Modified: Sat, 22 Jun 2024 02:01:03 GMT  
		Size: 71.5 KB (71465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adfebf227d878a105ea31b231eb02b2c0d4e2bdf54a49768ec16f1a8104f1f1`  
		Last Modified: Sat, 22 Jun 2024 02:01:01 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101c83d32dc50081bcb080d8b4fd810b830564ead1a87c035ba6270ab631c4e4`  
		Last Modified: Sat, 22 Jun 2024 02:01:01 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b312e892d5c043a44dc1601f7ad9eb88c2662fe91cef6701843aa26b188e0d`  
		Last Modified: Sat, 22 Jun 2024 02:01:12 GMT  
		Size: 206.0 MB (206046819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0af63552352dc6d2bb290f50dbc1fe2f3ad7128989d464260d849e5f2a2a9c`  
		Last Modified: Sat, 22 Jun 2024 02:01:01 GMT  
		Size: 4.1 MB (4113409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caead5e3a752f025333f69fc550c61b786642bf7946781ec21376c47c1a7a616`  
		Last Modified: Sat, 22 Jun 2024 02:01:01 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
