## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:4499eff0fcba1b17b147da75300c3c46dd64fc5677c3527dd104d973daec2a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull golang@sha256:167aeba9c6589eb850d68064bcb94fee8334f4bb9ce11aa5f7da1840aaf59053
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235133783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81e09c559b445ddefd00c4430a599e4c105bb743574dc4a31dae101ed0e1b0d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 13:44:35 GMT
SHELL [cmd /S /C]
# Wed, 13 Jan 2021 13:44:36 GMT
ENV GOPATH=C:\gopath
# Wed, 13 Jan 2021 13:44:37 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 13:44:52 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 13 Jan 2021 13:44:53 GMT
USER ContainerUser
# Wed, 13 Jan 2021 13:54:28 GMT
ENV GOLANG_VERSION=1.15.6
# Wed, 13 Jan 2021 13:56:24 GMT
COPY dir:4d3209dd6dc0a28e201f1dba6a02512d8e7c8ebc13640177c71b45b1bb90fef7 in C:\go 
# Wed, 13 Jan 2021 13:56:39 GMT
RUN go version
# Wed, 13 Jan 2021 13:56:40 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50358a323c5421695eacfec8cf19b70cfc54a72e6dc491bc2bfd4391d84dcaf9`  
		Last Modified: Wed, 13 Jan 2021 15:13:44 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7b504f15f2836681dc74e6bf27d7be538fe7e6a6f53ea4bf3d8be6bb6545d8`  
		Last Modified: Wed, 13 Jan 2021 15:13:44 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf6648d03a5b65f08b03a3cf89c0de5e57b386f48c5316121c697a7d4f12488`  
		Last Modified: Wed, 13 Jan 2021 15:13:43 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdc9022e2634f8a89707e4bfa55b2ff2a86865a3d7e5508effdc4abd5e92405`  
		Last Modified: Wed, 13 Jan 2021 15:13:43 GMT  
		Size: 66.3 KB (66267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3d33148024d9121b1452536b9df85f11745d7d415b1537823e481164375713`  
		Last Modified: Wed, 13 Jan 2021 15:13:38 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673f98dcf7e7e94f0b56dc2147b1599dc5336f294174b658ca1255fa33f8379b`  
		Last Modified: Wed, 13 Jan 2021 15:16:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149d52ce5b0fee61a1c73262e7ac2e54c8a3c01d7b3ca5e73ccd7d30de979611`  
		Last Modified: Wed, 13 Jan 2021 15:16:41 GMT  
		Size: 133.6 MB (133645778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e031a648c881d5adc173593290a4c7fb3cf78558bbc88abf86aa67bd2ca4b609`  
		Last Modified: Wed, 13 Jan 2021 15:16:15 GMT  
		Size: 76.2 KB (76203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3ff9a9c80172a9e339c2232db3a3c38d7cbc06bd8513a2a2f36175e1bab70a`  
		Last Modified: Wed, 13 Jan 2021 15:16:16 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
