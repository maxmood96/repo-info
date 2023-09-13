## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e5e04f43fb2dea7d2d2a435648a0539c8bcaac3451f9a2a9fbd9f42bf61c8559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:0bf8a65bc5d16b898e653e5dcd7f9467f9ef9d40d34d2f818bd9e41e789b49c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313812616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5198f3eb4abe5b430745c2ed46196cd0429a051635cb5ad5d5510a3dad8488`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 03:28:54 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:30:07 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Wed, 13 Sep 2023 03:30:08 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Sep 2023 03:30:08 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:30:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:30:16 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:30:30 GMT
COPY dir:bc17122f89ccac6825b72157f71faf8ee914101def60109a37803e17ec7fe7f6 in C:\openjdk-11 
# Wed, 13 Sep 2023 03:30:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 03:30:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d67aef4c483590cefd40495efc212f13e4c62993e8036c20bb4e19bc8620508`  
		Last Modified: Wed, 13 Sep 2023 03:47:03 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a0b30f2089f682233e849be924051a10d628f414320caac8a5a6f50b98d15e`  
		Last Modified: Wed, 13 Sep 2023 03:47:43 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b7cce41e641a325af63bf023a73c01e332b7e83e98b12728c75261f7c241c8`  
		Last Modified: Wed, 13 Sep 2023 03:47:43 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd204e8f2437159f557f90ecd6b3c0f3c7aaafdb4cc8be3ba9b4960934edd74e`  
		Last Modified: Wed, 13 Sep 2023 03:47:43 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31acb22a6c8082f300c7132162fb8038358488a6f8bbdfd550c5cc1113a417eb`  
		Last Modified: Wed, 13 Sep 2023 03:47:41 GMT  
		Size: 86.8 KB (86798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12df0fdfaaab58abba8ee6bf0b57eb81b8b88f8332eab856004b6045687499`  
		Last Modified: Wed, 13 Sep 2023 03:47:41 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c388741565e78b8872946f2006e29b1e2737aa8bab2f8b5f20f84080eb4b1c8f`  
		Last Modified: Wed, 13 Sep 2023 03:48:01 GMT  
		Size: 193.1 MB (193090761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f8c4bcd2a09364a6092f4f3da3fdd18e06c48e7575ee9fe84c9ec1df504ca3`  
		Last Modified: Wed, 13 Sep 2023 03:47:41 GMT  
		Size: 61.1 KB (61111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204e1f5f440610a4fedb24fb228bcfc0e312dd217a857bc9069db7bcb5f00351`  
		Last Modified: Wed, 13 Sep 2023 03:47:41 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
