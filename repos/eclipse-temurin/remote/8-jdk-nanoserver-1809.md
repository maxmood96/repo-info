## `eclipse-temurin:8-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:296ee93e4ee64bc3020dbde639460f4e8e16b2ac176dd5424f2b67db2ae22aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:8-jdk-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:cf304e9e1d113c0e7422e3e44108def28c021af0db2e64f72b1af48b6f6c21fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206732572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17bfbbf60d97a99235017e14c47bbd40c5cae3740c4ffaad93701ec3bcd0886`
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
# Tue, 09 Apr 2024 23:43:22 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Tue, 09 Apr 2024 23:43:37 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:0f2c5c84e4bfc598dbfa945a8183260add87485c8a16c6a92fd691a8294ed4d4`  
		Last Modified: Wed, 10 Apr 2024 00:47:58 GMT  
		Size: 101.7 MB (101691153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a1c2067b9bcd3aa72c53535a61ba921444722288bbd1aba07df4601f50d0d8`  
		Last Modified: Wed, 10 Apr 2024 00:47:44 GMT  
		Size: 80.0 KB (79964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
