## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:89d7b6150654d98351a7066333a9232881a096fd8ada8af572b2721767ebd7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:90b1dc7e2a32e687b807f7a312416a51326a67f2341a222ed52d86551981ddc3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145164937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319ee8757f988129758e81d9fd6c613541a63a473f55b0cec7c888a6a66723fc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Tue, 09 Apr 2024 23:42:55 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Tue, 09 Apr 2024 23:42:56 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 09 Apr 2024 23:42:57 GMT
USER ContainerAdministrator
# Tue, 09 Apr 2024 23:43:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Apr 2024 23:43:12 GMT
USER ContainerUser
# Tue, 09 Apr 2024 23:48:37 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Tue, 09 Apr 2024 23:48:48 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f488ee65de2b011deb88b648a2fd4a8df01a6335e42405d991c1303f90ecc8`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852d1dc582f1e8accc43aef8daeca6eb89735a124fb1f967b7f73ef3f9be2e91`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576c3d12347d0a39213fcd0330b9f36d0b8dd7f058cb28dc6c5a90efab178eb6`  
		Last Modified: Wed, 10 Apr 2024 00:47:44 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1e9364eb12671c19584d282ec60e21d04e812386049c863e0a536a61ada0e3`  
		Last Modified: Wed, 10 Apr 2024 00:47:44 GMT  
		Size: 66.6 KB (66551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2b0dd596df841ed6302a2df14e30ef0baac11bcf940216ef52ac8afbde390`  
		Last Modified: Wed, 10 Apr 2024 00:47:44 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05475690ba99de61f49f9bcb963ea2e28d247dae783aa516ab53eafc5310208`  
		Last Modified: Wed, 10 Apr 2024 00:48:59 GMT  
		Size: 40.1 MB (40117597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58cfd7c63fadcc806fa012d963fd773e9269931da21c0c92d85d290a1401eac`  
		Last Modified: Wed, 10 Apr 2024 00:48:53 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
