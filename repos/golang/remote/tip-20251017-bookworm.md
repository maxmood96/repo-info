## `golang:tip-20251017-bookworm`

```console
$ docker pull golang@sha256:612a7cc3399e36ca36e192b6c1d36cc1968aa865933baeb738b806354b7db2b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20251017-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:90fe1fd16415cfae643c1aa2ebf6a4b552872adaa2233d1bdc8d1c18d0c60610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279875553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663f1264d5078bfaa0ca201962309d82c218a5833568737efa302118ae81b7f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7a3d2023fde3fc32a539522fa0820b19b1d2612873863e54ecb2e457278c90`  
		Last Modified: Tue, 21 Oct 2025 18:16:45 GMT  
		Size: 66.3 MB (66254834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e37a565b466ff673d6eaad95f7f918df4a47f13ea7ff94f9312bc4a254253fc`  
		Last Modified: Tue, 21 Oct 2025 18:15:25 GMT  
		Size: 87.8 MB (87837459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d59333023fc4182e1f2cdb2aa56169548a06078fed89ea62585dd85bcf664b`  
		Last Modified: Tue, 21 Oct 2025 18:16:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251017-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:527b1e845c21d685868b459e1cd98c6f3ed7f63c7673444bfd4d79b3eb550123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946f3554e17531ce4ea81bbfbb6ba385e008f388bf44498fee94c5174d1baa57`

```dockerfile
```

-	Layers:
	-	`sha256:72b9035f8da4b91cfb1067931a408c8110e1c7fc96b7bf7348cadd5b83438102`  
		Last Modified: Tue, 21 Oct 2025 20:24:04 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17536398c1201c0815876a3a829b8ee25171c019998c911998eaf77584896b49`  
		Last Modified: Tue, 21 Oct 2025 20:24:05 GMT  
		Size: 28.5 KB (28541 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251017-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:bf23c5b15705e8140e4f0f16f914bb27abf88441a7770a9f9190a32ed9d6a9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309588214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d7a6f2a6d81acf27b96ff05d71b981552cf55990c1b0711e09a974a0d71a5c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f4f4785b386a50fc27f4a95984f2363a047651dc26dc3c6993b5bc1281a9c8`  
		Last Modified: Tue, 21 Oct 2025 18:14:45 GMT  
		Size: 86.5 MB (86471460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c596fe60daead99d920e71d2cefb1c0329c841dbd8772728b90e497e3f4f21b`  
		Last Modified: Tue, 21 Oct 2025 18:14:12 GMT  
		Size: 86.8 MB (86788679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88319149479377a00e2255b092d8a9306f7da810c88fa26bfc2f74a3eea1d9fa`  
		Last Modified: Tue, 21 Oct 2025 18:14:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251017-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f8191eb726c75f7528e738598be0b3eb9027f7837feb2d69ec85e5b1fb3064c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5bb2fc5bf9edd5767a88bd628fcb092b58329af4fcd185262c3c2dda2b8e89b`

```dockerfile
```

-	Layers:
	-	`sha256:159115a1145a7f2c5924ffab2b3d88edc846c2bfade2dd63e8645434fefec2a9`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e94cbb36757e5cbc083a3fe56a19d987a128769f1cb07b1ba9efa1d60972023`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 28.6 KB (28565 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251017-bookworm` - linux; 386

```console
$ docker pull golang@sha256:964eb2b0680c96b7ef9a5c0e381a3a08688c30044c44dc62cb779e8b063d4abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320049650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9373b1d8b2ead7facde8e6ae8edf222f3c06e300f4b506c7d865ce6d52ca61d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39058bc352da86cee9643b9b447133a3295983ec455cdba2fac6cbbed8726db6`  
		Last Modified: Tue, 21 Oct 2025 02:35:47 GMT  
		Size: 66.2 MB (66231902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b6b436b837d0b68de2a9e25338255167ad9169b6fd64c0cd133ece0430a1a1`  
		Last Modified: Tue, 21 Oct 2025 18:15:05 GMT  
		Size: 89.8 MB (89823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f21a8159428f1559d656875bfece2dbae3e195e6c40dc6a160e07432d96a1ef`  
		Last Modified: Tue, 21 Oct 2025 18:13:42 GMT  
		Size: 89.7 MB (89663317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572214f53e55d6dedaf9655081c7ec25a65795042b2e4ea16ef591384bd4f64a`  
		Last Modified: Tue, 21 Oct 2025 18:14:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251017-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4533fa3395a6393c4afe2b399abcefdb67ea2cc6b4438a9625f16be2dfef4b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee05b8fe5849ed66d3799947996be49a9e6807a20ffb4523ada17bb1119af694`

```dockerfile
```

-	Layers:
	-	`sha256:a4065efbfc03480dc40100e99322566683200467c5d04f140eb8c74dd45befa1`  
		Last Modified: Tue, 21 Oct 2025 20:24:26 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c415b523f49828905d3d19ffcc73918944a02f15eb1304a98d141ee6352cdaf`  
		Last Modified: Tue, 21 Oct 2025 20:24:27 GMT  
		Size: 28.4 KB (28396 bytes)  
		MIME: application/vnd.in-toto+json
