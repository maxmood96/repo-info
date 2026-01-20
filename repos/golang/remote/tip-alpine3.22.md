## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:5563100aebc9b1892b660c7f11b84deb87a93b42cff176f7c6f35c2ebd75d06a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:f78f18c58c54c30cddcca088874ff76cb0faac5e5795b499a660ae4fde783550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99145616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1a3cccd540a38a0a617e2fdd8caf8efc4b2e22b607632f0f0e067d33adbfa3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:44:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:46:37 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:46:37 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:46:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:46:37 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:46:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f321c77cbe1a64869c624e60e54ba1a99bfe468144cb3f10df19c7feca51c76`  
		Last Modified: Thu, 15 Jan 2026 21:46:58 GMT  
		Size: 291.2 KB (291155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e09070cc4c8c6b4577469e540a043174ece319f2134af5f8b6f76f4d7806aa`  
		Last Modified: Mon, 12 Jan 2026 20:05:02 GMT  
		Size: 95.1 MB (95051851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d615a0377fe653c2fe64330cef61dbf92405e56df7f64c82dd0e5fb85a162034`  
		Last Modified: Thu, 15 Jan 2026 21:46:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:15e1b1037c30a95f274a445c2961b38c616eaec34b9fcabad2af04c9d71becc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d2d30226fa6ea4ae23777bd0297f3b515f25529f8e3f67d6482d85a190e397`

```dockerfile
```

-	Layers:
	-	`sha256:c4daf6da6b004132395fcd78a142e61399a6f2207ba78a836f38f76f5477e702`  
		Last Modified: Thu, 15 Jan 2026 21:46:53 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8c12fe48f074ed7c456ba57bdcbcf2c8b1a1f30d240ed1d8ee858dc3caa6ba`  
		Last Modified: Fri, 16 Jan 2026 00:26:27 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:8ed97cc2a82ff9cff19e0aca10daa9e3d21b00680f7be15a49db4a77d4450c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95197570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d978d0ce62d890c39e4f72003d4c597c458fad2f8409c17a7e665989f80b9d7c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:42:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:44:47 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:44:47 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:44:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:44:47 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:44:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:44:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bd4a3b2fc63732891334d736e42ca6465178dc3a185d3f4454389c99d4d950`  
		Last Modified: Thu, 15 Jan 2026 21:45:02 GMT  
		Size: 292.3 KB (292323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fafe2d1996fb8d6337cd2dcb6acca5b8c22581c5ef4fda1f58bec46f2b5c18f`  
		Last Modified: Mon, 12 Jan 2026 20:08:13 GMT  
		Size: 91.4 MB (91401008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df744fa0f94618af0b38a069f91816f8c6ffc9ab617d21e02840638fbeb366`  
		Last Modified: Thu, 15 Jan 2026 21:45:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:15aba1ff28583781badb9ad40b3e92af327de655feb9a5209199998f209efbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ae2b8f975a41418a4f4d8e2eb1c10b44e877d5a7fce0d215a5d287e85eb8`

```dockerfile
```

-	Layers:
	-	`sha256:b4da044e57ffd60eaf4a42ff5ff02b5f28a758be7759f675e76c3471900f5bb2`  
		Last Modified: Fri, 16 Jan 2026 00:26:31 GMT  
		Size: 24.4 KB (24361 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:6018b5fa9e5a30ec4ee4641fff881397903d9ac20a8c4bc5fac0ef50f7a3c1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94647322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054452f7ad1079c9ca92d6b59141a0677cdb59d526c04b39ba3efdfbe7faf084`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:45:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:48:14 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:48:14 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:48:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:48:14 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:48:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:48:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0b62833bf0b11bdb2c64a0d0287e99f9900ea49b10a499462f1aec466fab4a`  
		Last Modified: Thu, 15 Jan 2026 21:48:38 GMT  
		Size: 291.2 KB (291215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb06c5933c094de46d52df9ed5d5962ecacceb10cdc72056e1307b0ee8c18640`  
		Last Modified: Mon, 12 Jan 2026 20:04:24 GMT  
		Size: 91.1 MB (91134394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896ef5f240f5cf21e1d92f211892fea264b10aeda3cb0d75fb93646e73e7f51`  
		Last Modified: Thu, 15 Jan 2026 21:48:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:af315ccad5d8cd325fafbf6aa6dc1ca1c9a7507633d201a7174af3c43bf92662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a8b27923faa2b4ba6cec9b201a9d60b73c1edc3966a4fade537a12e3974363`

```dockerfile
```

-	Layers:
	-	`sha256:93dbc5939de4a535cd20161dd6bac3e59cb9418b1a7a5f26168e6b843d69490e`  
		Last Modified: Fri, 16 Jan 2026 00:26:34 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886381d62426fdc077616b65c08d13bbe4bb9066a9377e07d4bb586f6b0e53da`  
		Last Modified: Thu, 15 Jan 2026 21:48:32 GMT  
		Size: 24.6 KB (24576 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c13d4c615efd8b2518229bd5fd2aacb50c51d87b16bc73cdec1c576ca6e85837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94569659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b82dc19e6e204c6287c39c3163fd842e6fe3c1be71cc140ca123a5e88d91053`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:44:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:46:03 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:46:03 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:46:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:46:03 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:46:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:46:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57829e1a4693847650eb531da883a926d104f5e02ba87662451d4d7c7fb0859d`  
		Last Modified: Thu, 15 Jan 2026 21:46:26 GMT  
		Size: 294.1 KB (294122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cab7771dc3fd9d6c93b2e8fcd20d3b05cdc987b52c3e09c78b1417acc8931f2`  
		Last Modified: Mon, 12 Jan 2026 20:04:26 GMT  
		Size: 90.1 MB (90137309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e36002015dd759bbfbbb5d17bb70e8a1a12076f5d52654aea689f740bd402f`  
		Last Modified: Thu, 15 Jan 2026 21:46:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:8ecd0a9fc3fbfd7f3da702e75d52234c09b5c53323de883a2f0ad90b48da838c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc658fce94c0ba6f4c3c6d736d8e71aad8ef20e03570149d1120d2dac39f99c`

```dockerfile
```

-	Layers:
	-	`sha256:504156950f922bb8a0bb94c021bd4f1ffa15294ee1ed4815dc3ac5bdbe57fd95`  
		Last Modified: Fri, 16 Jan 2026 00:26:38 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d84590695d6da7a2b729e90ebd9e12b7ba6d8f8996e6eb4ac1013c256ffd88b`  
		Last Modified: Thu, 15 Jan 2026 21:46:21 GMT  
		Size: 24.6 KB (24600 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:44af08e3791604d0af13f1c977dce7475875dd81d53543064109837f4812ea71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96856281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a59ee9160cfed2478f26b2a8800e3d170f301edd2983cf289225c77f11dbc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 21:45:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:47:29 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:47:29 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:47:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:47:29 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:47:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:47:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3613b9b670d3b2f91d9151758e1f91becba669899ab2360cdab916b59c8ba186`  
		Last Modified: Thu, 15 Jan 2026 21:47:44 GMT  
		Size: 291.6 KB (291637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42b2997976651e9da981a359adb745663b505ba580ded35d1fcd67a84ec5f37`  
		Last Modified: Mon, 12 Jan 2026 20:05:27 GMT  
		Size: 92.9 MB (92945554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf78c1e4e58dc7f72c137ffc831501b5ae6b5ac282fdc74753302821d673c2f6`  
		Last Modified: Thu, 15 Jan 2026 21:47:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7eca84e750589a7fcedfc20e8dcb7f0431c6470aca776a723fe73aa5c50a351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d891bea9b91273dd572e2e60f5a24172683e32075358b02ca4e18e4f363c08`

```dockerfile
```

-	Layers:
	-	`sha256:26d44cc6e91d9b9166a796f99f99609349eab3b5733da2aa0c8f7ab52b2af76f`  
		Last Modified: Thu, 15 Jan 2026 21:47:44 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7665cccec83e520d16f7169abadf288263fc3227412c93b5c2914fcaaef91fd2`  
		Last Modified: Fri, 16 Jan 2026 00:26:43 GMT  
		Size: 24.4 KB (24431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:357249aa594b9b37930b8986174cd8195e5fc5fee7b0c33c64cf9f40ecda3fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95710912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433bd983018a0e0f6ca7ca53b6ff0d5ae8eb15a198c768e1e4f76fa40f2913f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:00 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:52:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:53:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c1f34a163f68379a85adaf1396976b01cd79b6100ad42ff3e6581c97310f7b`  
		Last Modified: Mon, 12 Jan 2026 20:06:42 GMT  
		Size: 91.7 MB (91683920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f06aad430c09510676f17e9b62f992486b57571124e6bb8cab6fbc7323521`  
		Last Modified: Thu, 15 Jan 2026 21:53:23 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a5e59561f1c6eeafdef82f706b198cc3b26d987d03e6e0c8b024ff51e4608e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd516a2723f3928a325528c5d4edfe63b26cd429936a39ddcc6e7bbf1573d90c`

```dockerfile
```

-	Layers:
	-	`sha256:7e6fb2706948920c394f309e8a6f9e81d495a1bf1c85529b0d67b9b2a08a3bbe`  
		Last Modified: Thu, 15 Jan 2026 21:53:18 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf43f7b6224b6a247662c4b55f5c3bd080d14c81a8c3e9c4a19a702e9408d061`  
		Last Modified: Fri, 16 Jan 2026 00:26:47 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:b9457f6ae0c7f111c5ea3ae1430820e1f813d2c86af72c464d58981cbf5a2bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96122798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0353ff8633b1dfdfaf37bb60f91e7e9b85b3455180edb4be3cd0dc1c196f71`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOPATH=/go
# Mon, 19 Jan 2026 21:38:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jan 2026 21:38:33 GMT
COPY /target/ / # buildkit
# Mon, 19 Jan 2026 22:18:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 Jan 2026 22:18:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:17:39 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a3cc83856871e3a177f0a6b27128217f73d5993c49818bd1374bd92a6bcb48`  
		Last Modified: Wed, 14 Jan 2026 03:12:04 GMT  
		Size: 92.3 MB (92315877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a19461d8b4bb7bb1df143516b4b1640d2ef9f1dc9a2ceab2ed0635e03d666ef`  
		Last Modified: Mon, 19 Jan 2026 22:20:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:66c5197accf41705df3641327bb3c170d8a8e965b152bb85f869b9c769b7bad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b113429ee2bfac29475a5848e3f21c00bb8ddea9d90c1d2f17d89c06cb74cb`

```dockerfile
```

-	Layers:
	-	`sha256:4ef9240ee899ee41cb5f79ea30548a0a0a3e9d3447c0171a9ef50bb5e8ff1e8e`  
		Last Modified: Tue, 20 Jan 2026 00:23:59 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a381386b0e5e7cab0e2cbeefa77be91302b01415012a6927f8ab5ecd0b609d8`  
		Last Modified: Tue, 20 Jan 2026 00:24:07 GMT  
		Size: 24.5 KB (24510 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:d5fdd49f8feb72a8bdaa5cf8ac5f93747cd17c544f0627b2cf36de9a0eed3470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98171459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd974dfaf907c46b1c7b86fbb50f1e98dc4bc3fe88a26a3603f6484c5b218fd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:29:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 21:46:49 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 21:46:49 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 21:46:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 21:46:49 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 21:47:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 21:47:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f9d29ef25b91c67ee1e00545a6d668d3bac1c38574e667175946c9679a1b62`  
		Last Modified: Thu, 15 Jan 2026 19:30:31 GMT  
		Size: 292.2 KB (292153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c721b150b3efd4976a8fc9ccaf826512a0d88981fdddc7ad84ff81c3bfa69`  
		Last Modified: Mon, 12 Jan 2026 20:20:29 GMT  
		Size: 94.2 MB (94229904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1f259023f4a5da24afd433376369b0db883e7fe5ced360345f29a799a1f51a`  
		Last Modified: Thu, 15 Jan 2026 21:47:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6d2c99ed13040b1e56a4fb4e8896b7279aea71825ff3685c85a141d3d659bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa04145b923ce1844cdaa64c62a6d93442e4bd7900091dc252571575f6bb437`

```dockerfile
```

-	Layers:
	-	`sha256:70fda27964dd8f97d32fa19886dd9bfc9bfee0968b3b56b9ee389587f0a54251`  
		Last Modified: Fri, 16 Jan 2026 00:26:53 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9d60381d94549fcd32c563c14085ad1499aaf054ffdd08bb7ce0e4315793894`  
		Last Modified: Fri, 16 Jan 2026 00:26:54 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
