## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:160bfed01ce7c0c82c01f2d4e850f1189fffffbe79289b442cfe9769e30acc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.350; amd64

```console
$ docker pull golang@sha256:6160939cb971c3559deeb230a21ce5bdbbba76c95176d276d3744e2034d5f20d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262368709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8b01ecc07f0b6ea3478fbc57d60f7c6d33b4a044098df96e4d316a2a2e7e63`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Nov 2021 08:13:55 GMT
RUN Apply image ltsc2022-amd64
# Wed, 10 Nov 2021 13:37:46 GMT
SHELL [cmd /S /C]
# Wed, 10 Nov 2021 13:37:46 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:37:47 GMT
USER ContainerAdministrator
# Wed, 10 Nov 2021 13:38:25 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Nov 2021 13:38:25 GMT
USER ContainerUser
# Fri, 03 Dec 2021 22:27:36 GMT
ENV GOLANG_VERSION=1.17.4
# Fri, 03 Dec 2021 22:29:47 GMT
COPY dir:75899f42e0187d2b2462e6fa2635fe6503939c5561018ec0d756efbdd1e93fbb in C:\Program Files\Go 
# Fri, 03 Dec 2021 22:30:42 GMT
RUN go version
# Fri, 03 Dec 2021 22:30:43 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:83b9a19f898e6e25b6ee7e787da89582a8528b2defb5682f45364d04b35a278d`  
		Size: 117.1 MB (117116823 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:10d992a589a3ae9381768ac49d33610737b9d4229b1e142eb81c933bc18bab3d`  
		Last Modified: Wed, 10 Nov 2021 14:06:44 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe412e1eb92d2ce39086e8e3a6cbf14e85562659c252621eddb42083af428da`  
		Last Modified: Wed, 10 Nov 2021 14:06:44 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12b2791f99d57e11ce205d8d3e714391f1bdabe469d8c390f744462a9a13bc1`  
		Last Modified: Wed, 10 Nov 2021 14:06:44 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acf946a4ef74f9ecb59a8ba6f08956ab52a7997260d6ca02d2a753cfbe03440`  
		Last Modified: Wed, 10 Nov 2021 14:06:44 GMT  
		Size: 104.5 KB (104506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862fbd33abc7472e4616495a17e3553b5b80707464930cf8f4e27bccc4564dd9`  
		Last Modified: Wed, 10 Nov 2021 14:06:42 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5196acc1bd9c49a22c1cf18bd250fd855287d02f27ad2ac2d00c4b1aa619e55`  
		Last Modified: Fri, 03 Dec 2021 22:55:11 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d793c369b929a98486e93e617f72c56dc9a77689eed2ee0b7ccb26ea9ebc0b90`  
		Last Modified: Fri, 03 Dec 2021 22:57:51 GMT  
		Size: 145.1 MB (145072743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930597772dd3e0356d95f9540117fcc423d941b114441770c59d2e92d8394d76`  
		Last Modified: Fri, 03 Dec 2021 22:55:10 GMT  
		Size: 67.4 KB (67421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2e0a93a671d57eb45b379186d92d57d7fa8eb11762ad83a4aa02dd457184b`  
		Last Modified: Fri, 03 Dec 2021 22:55:10 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
