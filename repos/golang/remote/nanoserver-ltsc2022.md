## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:deb90218ab95fef4b4cbd97cd9553abf9d2f886e4a8b986e19a6aa2ba53a64e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull golang@sha256:18c1a7e08ae0e865338b9ba7c27fe52f8077f8dfbc0c46c83571452a90528362
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275520588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319dc63da34599f18f79822a1adbc939d316241cd5c0427f39c2187ff4526de8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 12:59:22 GMT
SHELL [cmd /S /C]
# Wed, 14 Sep 2022 12:59:23 GMT
ENV GOPATH=C:\go
# Wed, 14 Sep 2022 12:59:24 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 13:00:05 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 Sep 2022 13:00:05 GMT
USER ContainerUser
# Wed, 14 Sep 2022 13:00:06 GMT
ENV GOLANG_VERSION=1.19.1
# Wed, 14 Sep 2022 13:02:32 GMT
COPY dir:8931e4de46b22c4907fdd32bb2e3bdcb14b258c585caf020889cae248acd1241 in C:\Program Files\Go 
# Wed, 14 Sep 2022 13:03:22 GMT
RUN go version
# Wed, 14 Sep 2022 13:03:23 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66db2526be0f06c7bd6ba20bdc126ca2d5645acfeb41b5784e4664de37e72b49`  
		Last Modified: Wed, 14 Sep 2022 13:25:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218b9cf76f654e06a3b6ef23073f7aa93beb2d7a009f84ece64ec3e3d1e7c5e2`  
		Last Modified: Wed, 14 Sep 2022 13:25:26 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb708701bd5e2013191955685f70bb81113076e9a185d3a60689a9da8f296a63`  
		Last Modified: Wed, 14 Sep 2022 13:25:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a0722a534d7c153c052d9de736838075e3b4058d1d45fe5698776b85014a61`  
		Last Modified: Wed, 14 Sep 2022 13:25:26 GMT  
		Size: 85.4 KB (85374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7486bac86e8639da1434b9a65d14589fc776aa03daf816dcb7eeae093674535c`  
		Last Modified: Wed, 14 Sep 2022 13:25:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf611308a3f336651fc786257dcdef16daf9a450a2162b0c76cfd93fedc1610`  
		Last Modified: Wed, 14 Sep 2022 13:25:24 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d66bcf13d1d997f24a43de1928086cdcc5731acee28e65c1819b245f0166b6d`  
		Last Modified: Wed, 14 Sep 2022 13:26:00 GMT  
		Size: 157.2 MB (157247053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbb7534b4703e300e08fb6f5ab207d5f30cf16664aa4c4060553f4fe3bdb41e`  
		Last Modified: Wed, 14 Sep 2022 13:25:24 GMT  
		Size: 49.7 KB (49704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43350cb8cdfcd97fae12f45fb5eb721eab1169e86405d0efd4dce12bd1637ac`  
		Last Modified: Wed, 14 Sep 2022 13:25:24 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
