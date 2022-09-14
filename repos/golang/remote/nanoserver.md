## `golang:nanoserver`

```console
$ docker pull golang@sha256:a88f0a62ea119ff1dafefc0fa90abc35e72528630d7b405f2f7cbb42dc31e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `golang:nanoserver` - windows version 10.0.20348.1006; amd64

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

### `golang:nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull golang@sha256:cc0e5da9dfcbda696c58cae66b6d2a8c326de90175df1a32bda8648cb8b02eb3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260731189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ade44d53c40163856382df3b1aab40d6f4739f923f106fa155357524a55491`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 13:03:35 GMT
SHELL [cmd /S /C]
# Wed, 14 Sep 2022 13:03:36 GMT
ENV GOPATH=C:\go
# Wed, 14 Sep 2022 13:03:37 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 13:04:01 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 Sep 2022 13:04:01 GMT
USER ContainerUser
# Wed, 14 Sep 2022 13:04:02 GMT
ENV GOLANG_VERSION=1.19.1
# Wed, 14 Sep 2022 13:06:40 GMT
COPY dir:8931e4de46b22c4907fdd32bb2e3bdcb14b258c585caf020889cae248acd1241 in C:\Program Files\Go 
# Wed, 14 Sep 2022 13:07:23 GMT
RUN go version
# Wed, 14 Sep 2022 13:07:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0668477bacdfc2e7df1cd4268b246175ed9b30cf07ccb4bcfcb258d8bee830e`  
		Last Modified: Wed, 14 Sep 2022 13:26:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd835cc99524be3bba77b73a838666949cf7d47639a399e21f6d14634a36d6b0`  
		Last Modified: Wed, 14 Sep 2022 13:26:18 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676957d5345611461c5bb939bd80adc80391d96397aa8a4511fcb998a9c57870`  
		Last Modified: Wed, 14 Sep 2022 13:26:18 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4570eed23060516293c36e26c87bcda7c57eaa2e2677941747fc0d245eb30e3`  
		Last Modified: Wed, 14 Sep 2022 13:26:18 GMT  
		Size: 70.5 KB (70482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528822ef8700498a1b6039b0b3fe96dbe512d72f9f888362aa2b2bcefa7e0fd5`  
		Last Modified: Wed, 14 Sep 2022 13:26:16 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad6e06d47ba5b61c19c028e955086b79606e56e63b9a0b4b916914d35181f71`  
		Last Modified: Wed, 14 Sep 2022 13:26:16 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f639b37f602bbde78b8fa542eec00944917acfe699ec051b8b83cf8c14cb0d`  
		Last Modified: Wed, 14 Sep 2022 13:26:54 GMT  
		Size: 157.2 MB (157245862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ba3b643ec7c9c05aff887ea1712f94a0b229f90ba06ab932f2c396055a5056`  
		Last Modified: Wed, 14 Sep 2022 13:26:16 GMT  
		Size: 73.5 KB (73509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6352fe87f53474d59bd493202a546780fabb7fdb706b965c49198b600ebbda94`  
		Last Modified: Wed, 14 Sep 2022 13:26:16 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
