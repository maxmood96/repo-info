## `openjdk:26-nanoserver`

```console
$ docker pull openjdk@sha256:a21ac4eb470304452b6540d5e9fb1d7ed0b7a96655461a625a05c6bdc9b040d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:26-nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:a8de7f1af5d193b2113b5401205429c4ae81447d618ac34808ee16402af88563
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.4 MB (412412402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ea97b5231f46820829a375f34a4af423f2ca3b92e26005f1820744cca2611d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 02 Sep 2025 18:09:47 GMT
SHELL [cmd /s /c]
# Tue, 02 Sep 2025 18:09:47 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Sep 2025 18:09:48 GMT
USER ContainerAdministrator
# Tue, 02 Sep 2025 18:09:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Sep 2025 18:09:52 GMT
USER ContainerUser
# Tue, 02 Sep 2025 18:09:52 GMT
ENV JAVA_VERSION=26-ea+13
# Tue, 02 Sep 2025 18:10:01 GMT
COPY dir:08ed6392bbde5a6a9f4df62a4d13cd725bac341043a31a8c49758849f45c1fba in C:\openjdk-26 
# Tue, 02 Sep 2025 18:10:07 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Sep 2025 18:10:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdc212d74e6bd7622a90756dbd759d60b94770978edbd4f8b1b8fcd57ade260`  
		Last Modified: Tue, 02 Sep 2025 18:11:09 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12f2146cb77347507e755c7b5e48bd6a6120ed944dd88a3fc47806931b7e994`  
		Last Modified: Tue, 02 Sep 2025 18:11:09 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce67392f50bea424e83d3ede19d4faf9b4bf4bbd0ab97be9f3cabad8d6ee4de`  
		Last Modified: Tue, 02 Sep 2025 18:11:09 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9d451333b7dec0d9b64b2a4b6f2488ed5341562b2bae0ddb7587e5e360a1a`  
		Last Modified: Tue, 02 Sep 2025 18:11:05 GMT  
		Size: 75.6 KB (75592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba23e711b5a9d67b74686d5a84d96b065a42f3c306810931cfd87f44b0ebff7e`  
		Last Modified: Tue, 02 Sep 2025 18:11:05 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e52da25b81a17fedc82a44e8273fd02ec7024aec5c213257cb4208be5e4f885`  
		Last Modified: Tue, 02 Sep 2025 18:11:06 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a388cd9073a8fd424e88fac09e9cfe2ec2d75856312cd04cae26af89522f1604`  
		Last Modified: Tue, 02 Sep 2025 21:24:44 GMT  
		Size: 218.7 MB (218747190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46885c1517cad4b73b20d7f486100db73f3652d6dce0601db65b8de0383b562f`  
		Last Modified: Tue, 02 Sep 2025 18:11:06 GMT  
		Size: 113.9 KB (113865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e23113df663f04e6dd8e347ab57cbd2db6e5b48ec1d4593dd1c0ac460e5f8`  
		Last Modified: Tue, 02 Sep 2025 18:11:06 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:74b0f911ce0e9142b31298ad446c90a0c46941e33e9dd5e56a65b2dc0ac3006b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341591860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9c79859b6bd859632ced704ddcc215e76a0e6d13443bc629b57ab881913975`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 02 Sep 2025 18:03:28 GMT
SHELL [cmd /s /c]
# Tue, 02 Sep 2025 18:03:29 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Sep 2025 18:03:30 GMT
USER ContainerAdministrator
# Tue, 02 Sep 2025 18:03:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Sep 2025 18:03:37 GMT
USER ContainerUser
# Tue, 02 Sep 2025 18:03:39 GMT
ENV JAVA_VERSION=26-ea+13
# Tue, 02 Sep 2025 18:03:47 GMT
COPY dir:08ed6392bbde5a6a9f4df62a4d13cd725bac341043a31a8c49758849f45c1fba in C:\openjdk-26 
# Tue, 02 Sep 2025 18:03:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Sep 2025 18:03:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1608fb69ec834877c53973da3e2024776df5b6a35276cb5187bdae1f8ccd2f23`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc9e6e68bebf5b722ffea5d06739f07488262f9ac09d1fa96005d261b1c4f1d`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a0c669714f1065ddaa8312d31a0348a04209e8f7b1064be8e2d85100855b73`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2631e3c1802a43155d88954fbbb67e149b3b3e89d7ffb922760da25bf02d5b`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 73.8 KB (73833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbff9673a22f6eba653fe961b3fb3988b537c331775f79e2368900afb10fdfa6`  
		Last Modified: Tue, 02 Sep 2025 18:04:43 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2515bdead523fd741e07e5063ea1d14176d0aa4f9c8def68a4f0b4cf90029a`  
		Last Modified: Tue, 02 Sep 2025 18:04:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cbbfcf79c6332a62fe9c330311a9f52d8ffbebc18aedda596ca9e4bd83cbbb`  
		Last Modified: Tue, 02 Sep 2025 18:24:20 GMT  
		Size: 218.7 MB (218745061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba0abe3fa10b96429acdb1c29df730e2f3fa1f1d7a6de0a2d62719b483d23e3`  
		Last Modified: Tue, 02 Sep 2025 18:04:47 GMT  
		Size: 106.5 KB (106456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9e1daff97448c32a91e8067d8e1596db114d7a904ef34ae6133fff79d034c5`  
		Last Modified: Tue, 02 Sep 2025 18:04:46 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
