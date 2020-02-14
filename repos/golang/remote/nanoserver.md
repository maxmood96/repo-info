## `golang:nanoserver`

```console
$ docker pull golang@sha256:e75f0b408c269958c90bca15d38ddb81af4e3df280bebc0837e9f6bc3c783df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `golang:nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull golang@sha256:0a2ac8a387333c3b0a9144bed61c33151979f4e32e8ab39c04d3c814b337fac4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230714742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d7b0bda019491340d8697cb25f85b5d1dd2fa0c04b30d7b2c7024a51f2b56c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jan 2020 13:30:43 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2020 13:30:45 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Jan 2020 13:30:46 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2020 13:31:01 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 15 Jan 2020 13:31:03 GMT
USER ContainerUser
# Fri, 14 Feb 2020 01:32:28 GMT
ENV GOLANG_VERSION=1.13.8
# Fri, 14 Feb 2020 01:38:26 GMT
COPY dir:78abd178cc2579a6515b59239585933050ae9de5ea9a6e599afdd8562d55bd12 in C:\go 
# Fri, 14 Feb 2020 01:38:46 GMT
RUN go version
# Fri, 14 Feb 2020 01:38:47 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6d2b296a71d6933ef11f4e74561e6121347a2ed94dca1fe05411acddda6dee1`  
		Last Modified: Wed, 15 Jan 2020 14:22:06 GMT  
		Size: 915.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655360e4f5b854fc477573e7aa01a5bd2d1a98ab61dc034faf439252c8e5f6bb`  
		Last Modified: Wed, 15 Jan 2020 14:22:06 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a112b2082077143e3991a1c8271eda1759f92aaeed15fc7be7d1833e5a060ce`  
		Last Modified: Wed, 15 Jan 2020 14:22:06 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080c04b06396990c98c38d890143af9a6095e331d70bdb3fa41e377ccad5011b`  
		Last Modified: Wed, 15 Jan 2020 14:22:06 GMT  
		Size: 67.9 KB (67942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f61b854e0e2419e287db310a75064a06d74adbd4af044d4364108e90defb20`  
		Last Modified: Wed, 15 Jan 2020 14:22:03 GMT  
		Size: 917.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcd2784936c1cc9c3f24cfc237e05aa82792c2ee62c1d37c8b8389e4d6a2fa7`  
		Last Modified: Fri, 14 Feb 2020 02:46:52 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6089b8d0fe660aab81cb41ce3c84c41cf562c6d9c7615fa07eee33e35af5591`  
		Last Modified: Fri, 14 Feb 2020 02:48:52 GMT  
		Size: 129.6 MB (129550830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963cde6bd42165688ed77447f460328d81803fefc48297eac8c9c52ec5ec4cee`  
		Last Modified: Fri, 14 Feb 2020 02:46:53 GMT  
		Size: 35.9 KB (35856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf57d98be6ff12b3e85f4744910aadec9bb6aad1f017c79c1a862f389c3fc41`  
		Last Modified: Fri, 14 Feb 2020 02:46:52 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
