## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:7ae3e8d2ecfcaab58627f03e0da3cc87b28fe99ae9e8a2b5bfc49733c06b3b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull golang@sha256:2e9eeac347bc26f10496a54cc75c5e29779cd76f485a9f0c00cbe9aebd6854e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97476e2649bd26db040b70cd4e2bf3503bfb1e00667d46db91fa80e61950d41`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:02:54 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2025 18:02:55 GMT
ENV GOPATH=C:\go
# Wed, 15 Jan 2025 18:02:55 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:02:57 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 Jan 2025 18:02:58 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:02:59 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 15 Jan 2025 18:03:57 GMT
COPY dir:c57def00df00b8073b50c57c8023ceae4d144aedef00a4df4374a7bdf40392c4 in C:\Program Files\Go 
# Wed, 15 Jan 2025 18:04:00 GMT
RUN go version
# Wed, 15 Jan 2025 18:04:01 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289835f94628689f4f4163843f138789e40e0cadd9cdda2dbe7356216ba5e7ad`  
		Last Modified: Wed, 15 Jan 2025 18:04:07 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8baf4e5644f71c977dab1d900be8235d0e5daa7d4f4fe8bbf1d70add2b7ef5e`  
		Last Modified: Wed, 15 Jan 2025 18:04:07 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1f13b5f349a328d58a1a61f4559024534b981502e5096853468c3559277dbc`  
		Last Modified: Wed, 15 Jan 2025 18:04:07 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722ae0a3e311a418cc049d63bcbd8298fa3ea955111e8adab2293a7022c5a51c`  
		Last Modified: Wed, 15 Jan 2025 18:04:07 GMT  
		Size: 74.1 KB (74079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210119b3631b411512c40e76314cae4a2dc29d6cc24f41a7e9c26b1df5dc8a67`  
		Last Modified: Wed, 15 Jan 2025 18:04:05 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab75551faa32f909db6677df0ff9d08f682c7a89abec6d5b75a2b5240811ec4`  
		Last Modified: Wed, 15 Jan 2025 18:04:05 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc9ff4d86c42b350f08f4bdb47adfe93c647d3e7864f2b4a27947cf6a4bdfc`  
		Last Modified: Wed, 15 Jan 2025 18:04:17 GMT  
		Size: 76.9 MB (76948663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22efaaf02302cd9ba7efd17eb7f88ade8ad9b7b17553e58eba285bbac68bd48b`  
		Last Modified: Wed, 15 Jan 2025 18:04:05 GMT  
		Size: 71.9 KB (71899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d604df50c984c997a36b581d85b9fd52677f1dd15e2149aa1ed867c615e48c6`  
		Last Modified: Wed, 15 Jan 2025 18:04:05 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
