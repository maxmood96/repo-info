## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:25f95faa20180c2768eb6e56362b858b080f916a56f8601a330a1a59b58d9008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull golang@sha256:a04f1f3c17eb0e55567bf25ec5eebc20aafbd0904ca596aaf35a84b0dea534d6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272152939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2cff3b4c50f9f469840c149e0de79cf77a6dd7789896e5d374228e6cf3970d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 02:18:10 GMT
SHELL [cmd /S /C]
# Wed, 09 Apr 2025 02:18:11 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 02:18:12 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:18:15 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Apr 2025 02:18:16 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:18:17 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 02:19:26 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Wed, 09 Apr 2025 02:19:30 GMT
RUN go version
# Wed, 09 Apr 2025 02:19:31 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4653069122c9077ba7e7d028e3950e0a805dc84d7baf2dee8e612c58a536e5`  
		Last Modified: Wed, 09 Apr 2025 02:19:38 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb7f2c355311382803cda85b322471e9aa4ec50cfccb24203323e730a7b8793`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72445483af37d3ae7532bd1b75b78922d1ebec20684241a86bee0b34aaec95`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939cd2886834e617e519237cfbe8a9e76e271952c13cb887cc903991776853b0`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 76.3 KB (76254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957a055ae985b700531bf2b5c06860559611671f47a1601bf7ef422aff75565e`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d93d414b6d3a255bb99f193fd1e6de33de1be2b63354ac9edce00ce7f34462`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b5785894f8e4c1f72f744a3a3dbf3c3f0c7395a892396a10dca34fd2ece44`  
		Last Modified: Wed, 09 Apr 2025 02:19:48 GMT  
		Size: 81.9 MB (81866295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34e6d2a6ed6b84ff1d5ea658f7d7c89145945e79c4c7b49785e0c260837b11d`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 90.6 KB (90601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be16d96d4d983a1cf7f7d1611cda72ed7de3c5b6f0e312d5f50863e694f7332`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull golang@sha256:9e69fbce3ab15b2f3d5fe4c82f55164862e476849737db029091c2e73c300e45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202721028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66415b6a86291ceac146db2bd5d0925115f553facdc0b4378f8baadcbe28b8f1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:22:28 GMT
SHELL [cmd /S /C]
# Wed, 09 Apr 2025 01:22:29 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 01:22:29 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:22:32 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Apr 2025 01:22:32 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:22:33 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 01:24:25 GMT
COPY dir:c31dd4b35955c3b7ad87aee80c32a76880e815054766f9fc2b5a42c53d1c95ce in C:\Program Files\Go 
# Wed, 09 Apr 2025 01:24:28 GMT
RUN go version
# Wed, 09 Apr 2025 01:24:28 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3ddc7301e8f3e22b42f3c3a6f001e006eb4adc38ff152e029ae45044c841e`  
		Last Modified: Wed, 09 Apr 2025 01:24:32 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1be42b7509310fa4f1e903f10b3abed420cda3ae4cc17d589e12303b7f2941`  
		Last Modified: Wed, 09 Apr 2025 01:24:32 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716fa522579dee364f7a233abfc2a15bb6b8decc6292a8f32cb887f907346d26`  
		Last Modified: Wed, 09 Apr 2025 01:24:32 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c19066c440307925bab270a98df411ac79207490ea1baf566260c2cf2c0d46`  
		Last Modified: Wed, 09 Apr 2025 01:24:32 GMT  
		Size: 75.9 KB (75881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aaf82202852056d91b7ad081cf9c43db0638af98551daa3c4b43e6aa21d7de`  
		Last Modified: Wed, 09 Apr 2025 01:24:31 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89b6f041d9935b9b85aa2228f077a260f4854a6d2442e95b5b4ed70e0f7afb1`  
		Last Modified: Wed, 09 Apr 2025 01:24:31 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265f600cff2eb976f6d349579e3431d634d23d7179eaf53df94456a471b56396`  
		Last Modified: Wed, 09 Apr 2025 01:24:43 GMT  
		Size: 81.8 MB (81823960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f9cfafc7e8452e9503c4590aa723a5138696f79452501eecebbdc0e5ec6d46`  
		Last Modified: Wed, 09 Apr 2025 01:24:31 GMT  
		Size: 78.4 KB (78367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6ffbe17aa8cad8eaeba86be588e2487d890e9c8e21f99bbdf14f272fbee543`  
		Last Modified: Wed, 09 Apr 2025 01:24:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.17763.7136; amd64

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
