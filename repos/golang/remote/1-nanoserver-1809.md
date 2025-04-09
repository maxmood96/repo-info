## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:86db7ac6c1f9d32e4b65a338b58bf2e48a90ce7b86885b467489638b74c29faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull golang@sha256:a540d3f02d4beb1137ce7feec6093e0407104e5e2ae8565f767cdb150b9cef61
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188900305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d774b97208776d059fea4f35bd3cb7dcb5705955bbd8e31ba6a5a0b0dc60b54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:23:26 GMT
SHELL [cmd /S /C]
# Wed, 09 Apr 2025 01:23:28 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 01:23:29 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:23:31 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Apr 2025 01:23:32 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:23:33 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 01:24:34 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Wed, 09 Apr 2025 01:24:38 GMT
RUN go version
# Wed, 09 Apr 2025 01:24:39 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515025a66f9cf040165fcb5dd30fb291d77e51744f4d9724c685a2a735698916`  
		Last Modified: Wed, 09 Apr 2025 01:24:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07b6b853b11483d1a2187ea7898f1ed0c38da01cad414df2bc50a3710e1b38c`  
		Last Modified: Wed, 09 Apr 2025 01:24:42 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc456654b7201a33fab76e48706e2479ea819c0c6c5ac2dec64d6e53d366cc5`  
		Last Modified: Wed, 09 Apr 2025 01:24:42 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefdbde751e588299abbbe677f0faff209a2ea76c245826b9e3ea88304b654eb`  
		Last Modified: Wed, 09 Apr 2025 01:24:42 GMT  
		Size: 69.1 KB (69095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda7e29b579add2ca328e10a595ae71bc9aa8279c01b3b18d7aac6b93f5bc6ed`  
		Last Modified: Wed, 09 Apr 2025 01:24:41 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c982e95e90d5714f97a4f86e0db081f6b147c76b183009ee3ca996c6a28fec`  
		Last Modified: Wed, 09 Apr 2025 01:24:41 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdf5b5fba642a7150128797333cf531c7f664cac812d2db6dc6981518656556`  
		Last Modified: Wed, 09 Apr 2025 01:24:54 GMT  
		Size: 81.8 MB (81824948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ef881b346f1e552777516792d3df6e80bfd60434f1fa3ed44b7e4b93f9a885`  
		Last Modified: Wed, 09 Apr 2025 01:24:41 GMT  
		Size: 77.3 KB (77326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037dabcf6589c4a5f981bbc87b79afa33df0268c662d89f1af0ef2fa6474505`  
		Last Modified: Wed, 09 Apr 2025 01:24:41 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
