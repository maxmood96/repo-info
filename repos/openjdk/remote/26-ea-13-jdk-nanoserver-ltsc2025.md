## `openjdk:26-ea-13-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:beee479a38832e261963b28c874f95543718e7b20e8ebcd8c40f7336fbfba579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:26-ea-13-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

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
