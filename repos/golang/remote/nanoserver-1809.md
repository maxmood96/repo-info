## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:9c14fbf871c48596910fb2e03d23f23a10be7024c6014710a44aa4e6d15ed603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull golang@sha256:110b97f8ca6b2fc0b94536dc92dbb5c84c93f1587dbc4bc74ed886462e2772d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 MB (237094684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df05420060f5945de3a5efac38c979e1043edf71340bde397d00cffde446bb66`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 12 Feb 2025 18:31:56 GMT
SHELL [cmd /S /C]
# Wed, 12 Feb 2025 18:31:58 GMT
ENV GOPATH=C:\go
# Wed, 12 Feb 2025 18:31:58 GMT
USER ContainerAdministrator
# Wed, 12 Feb 2025 18:32:08 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 12 Feb 2025 18:32:09 GMT
USER ContainerUser
# Wed, 12 Feb 2025 18:32:09 GMT
ENV GOLANG_VERSION=1.24.0
# Wed, 12 Feb 2025 18:33:11 GMT
COPY dir:c62b8dc6e9060a1c90492bd4af0627f1fb2ef88d5b0c6bad980916fff57ef6a8 in C:\Program Files\Go 
# Wed, 12 Feb 2025 18:33:14 GMT
RUN go version
# Wed, 12 Feb 2025 18:33:15 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b68b2823163ecfb785399015ad879d0a832984e9ecb3e53a91234731842bbdc`  
		Last Modified: Wed, 12 Feb 2025 18:33:21 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f99071263612f7bd104223ca292889bcc0997ba3f0a5490104f889d7c556a`  
		Last Modified: Wed, 12 Feb 2025 18:33:21 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cdb412ddd055b48f06d95c9dc1847b3f747d5f221ccc54b5c0bd2085bead17`  
		Last Modified: Wed, 12 Feb 2025 18:33:21 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530054e818ee1248724d9c91a73a80cd1e6723d74c71573d23e1c8b42fb92f2`  
		Last Modified: Wed, 12 Feb 2025 18:33:21 GMT  
		Size: 66.3 KB (66321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c8c5d88bb1acd07f4707661ee9970e3bb0a50d261607980fed383161f6ed32`  
		Last Modified: Wed, 12 Feb 2025 18:33:19 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d153455dd7a13f97e8c904ce3175a7c1ee7d30e424246bd5c9a614700c0086e1`  
		Last Modified: Wed, 12 Feb 2025 18:33:19 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c342ba90bdb0b47ee7f613594a98ba54e941403d38d1baa51dc146fb5a59e4e7`  
		Last Modified: Wed, 12 Feb 2025 18:33:32 GMT  
		Size: 81.7 MB (81686520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c24d0205217ac9f421e7f3e48d082e738ff66d7791d807822eec2f3ff78604`  
		Last Modified: Wed, 12 Feb 2025 18:33:20 GMT  
		Size: 67.8 KB (67790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945780a676d0aefea0c58a87477269db964d87233cb2f50447706f8e69f35dd8`  
		Last Modified: Wed, 12 Feb 2025 18:33:19 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
