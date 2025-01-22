## `golang:nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:db971a09fdf1500bb7f0f42cabe26e2e535415a560bf16a6922e3c646a84daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `golang:nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull golang@sha256:1d3430a75acfc3142a372085ac724c53158d575e33c252d5cf3a6b5d2d2b37ef
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276190505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09aa2547b5e352eb3aaf07a13ace0387d61fd3fa0cadaca8df519e262a9d597b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 00:31:45 GMT
SHELL [cmd /S /C]
# Wed, 22 Jan 2025 00:31:46 GMT
ENV GOPATH=C:\go
# Wed, 22 Jan 2025 00:31:46 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 00:31:49 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 22 Jan 2025 00:31:50 GMT
USER ContainerUser
# Wed, 22 Jan 2025 00:31:51 GMT
ENV GOLANG_VERSION=1.23.5
# Wed, 22 Jan 2025 00:32:58 GMT
COPY dir:686423f35bba4280be244c38d9d939799b38be8e943dabfe1a129b187496242a in C:\Program Files\Go 
# Wed, 22 Jan 2025 00:33:02 GMT
RUN go version
# Wed, 22 Jan 2025 00:33:02 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afe8090e9a89a6ffec74070c2fcbfa84db43403b27412f7ee5928939d44211c`  
		Last Modified: Wed, 22 Jan 2025 00:33:08 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6d0be54ddccf801ad3d03d9c9f9d70d02cff13a8d6d1f9c4883679b85261fd`  
		Last Modified: Wed, 22 Jan 2025 00:33:08 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cc6707b7c3e4bcf83362a7014b4dcaf9e41000100c429fcc80bde0ac6263f4`  
		Last Modified: Wed, 22 Jan 2025 00:33:08 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c47a9f8c72e6b9a7c49b7af035a007de89ff80b262feadaa7eabacfe380a8e3`  
		Last Modified: Wed, 22 Jan 2025 00:33:08 GMT  
		Size: 76.1 KB (76117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05994658523b1f7f0562fc779452ab5ff12bdb93b8fd412c2573ad6b9f054865`  
		Last Modified: Wed, 22 Jan 2025 00:33:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199954f1cd39d3b03523484fd919499a03bd0d48b2c6d9a4725a78e961fd51a6`  
		Last Modified: Wed, 22 Jan 2025 00:33:06 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abae5adfeb63bd097c0c7bac52621925064713c74a985ad61b21e2b8e508dd30`  
		Last Modified: Wed, 22 Jan 2025 00:33:18 GMT  
		Size: 77.0 MB (76965544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85f32c1e4e868f02687c68148e3e49ad66ee2b934c4365578f23e808f85f681`  
		Last Modified: Wed, 22 Jan 2025 00:33:06 GMT  
		Size: 88.1 KB (88100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5d6b9428163c5301a7cc1fb3c87ec43f7b8bd3108eb6e401f8abf143abd53`  
		Last Modified: Wed, 22 Jan 2025 00:33:06 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
