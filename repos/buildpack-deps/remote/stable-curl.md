## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:9bc238e47ab0829b590fb56193b15c801a80993878c388ecd8818a6e2ff05ed6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:52e52e7363ce80b1600acaa10362705b2ea2532a6133ae98ada944fda667f3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74899031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ba52b1c5519c832ca766a67555f7a93e7a64ac6cb8bca28461fa115520408f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7d0ab2a235a1bde0f2f9829037fa0ae2289186a6986b8f913bc637d67cf3faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626678e1ba294ebf395f6ebb7e6c18b2d32d950ee2ee6cf0b4832befa2c77076`

```dockerfile
```

-	Layers:
	-	`sha256:0ade1d6d2dc3fe258326334320ab038d769b0ff50b4bd3b17ac56d6a50eec07c`  
		Last Modified: Tue, 13 Jan 2026 05:22:45 GMT  
		Size: 4.1 MB (4119913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:900ea4a54c7d527c477bc3b064d14514b9650ec1ddfbe5effe5975e1c8a5ac6a`  
		Last Modified: Tue, 13 Jan 2026 05:22:46 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8a8eafae7fc5e6976140d7851eddc998e5c4c140b4ad139d74a396c9332ca938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71802228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf693a7a2c164af13f5c64b6b6cd1a5296e25f229acdcd19705f52a20978088`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16d4329ceaa8dc305221873389c356e4c5bf3cdb5b245a79ff75a1b1806f3778`  
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
		Size: 47.4 MB (47448362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac90147d1f1c4bc0ab2c1c245fb4105c9ad56d7e5e75726e8ec474c79f05f`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 24.4 MB (24353866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:efcf210de9f5e5b0c1e38f2c09a8b9469e4fb3e347a271e8fa52c74ae6d7e86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1811e91ca3c2bc94b8fa6ac54069bb1e7db47af784af9a43fba3ff399f49785a`

```dockerfile
```

-	Layers:
	-	`sha256:fc37f4da198133822e9194ecf15328c4dce554ffa398e86185ad9031851442b2`  
		Last Modified: Tue, 13 Jan 2026 02:29:56 GMT  
		Size: 4.1 MB (4122903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eed8348f8f456f5865d46c15892aa9bf53584dd702df6a25815e60505736670`  
		Last Modified: Tue, 13 Jan 2026 05:22:52 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4f5b168407ab7579daa5195a0591566eb8c11d6953f2d840599df1f7c107400f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69344485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e91e1e402006636869ea21d0ab21969368a18fa8f89bed5d76dec16da72dec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:04 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4022af9daab8fd128446e9b47577c5e05501df410609b93136282ae4910bc68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25df1c361bc05fa243aca07409e8291bc836c1a1e61c29a535756819cb0a962`

```dockerfile
```

-	Layers:
	-	`sha256:d54ffcd94ada5d15233720a8c7468bb60f327c57b8184657eedf4e295eb849e4`  
		Last Modified: Tue, 13 Jan 2026 02:59:04 GMT  
		Size: 4.1 MB (4121414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a3f9537cef0cd4a60c5af5d20f2e29b510bd5034bf03e4f3a2002d758d4089a`  
		Last Modified: Tue, 13 Jan 2026 02:59:03 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ffa846549bbb651d58ec0fe396744675436cbb5046d281894edb320ec840d0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74670719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fe8c2ed96ba04cf6319393e8c29ff68c96d1c23523c46a4cfd9a1e086271cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6df3fcaf43359699105dd5e2720e0fc7e48c61ae4b58e6b34a8b41db8efcc593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766b5f17f38613bce07730dfaf3bfe8ef136fe7651f114c9c0d500a24dbcc348`

```dockerfile
```

-	Layers:
	-	`sha256:3e3619bd51407e3233d5fc9a1712d8d45d6262c1274ce286f79a79da52d84ece`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 4.1 MB (4121455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a017f18799b511939ea31ef74a3581f8f31fe33b9fc6e55164ed5e1fa76f9e0`  
		Last Modified: Tue, 13 Jan 2026 05:23:08 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:24088d6328926594d988210fae255478bbb6d3d69b3424a46de8f5a82d71773f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861de31eb2bfcc3bd79a85e1757a273453fe03fa5220c0a5a94c0dd9d175ecc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:47 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c7588c780f957c00c72badc134ebcd9f717f2f9e39056c493bf2e617791f777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e281f2ae5996307c77c9016ce53acf8aaae8be411573c1cfe5fe257efee98ef`

```dockerfile
```

-	Layers:
	-	`sha256:a02920076e353fdebcd8bfb2e5cd2f976f59957cc213e951fffa5d2fb49ac8a2`  
		Last Modified: Tue, 13 Jan 2026 05:23:12 GMT  
		Size: 4.1 MB (4117020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad02a95157b3a4132ad12e70c7db8633c71a631d929fdd93ad218209cbb33fd3`  
		Last Modified: Tue, 13 Jan 2026 05:23:13 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47d7c45dc4ae8b6277ef9ee08a7c69503b8c43441a303df703e62ee89601fad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80105014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56737046c59ae7c848ea3299724d948db41113a449b5106e1bb2cf5e7d072895`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:09 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b41bb47c086a9df336f7146e2b3c4d581690c4d493c2abb87406110dc01af896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7b47e80182fd7d452e326f93690472feeb200706ee885a221a76f9b7b6f7b5`

```dockerfile
```

-	Layers:
	-	`sha256:57fb69b9da141ebb54dba3ddc074fd4047a0f297688c5e200a0c7fed30995eb9`  
		Last Modified: Tue, 13 Jan 2026 11:20:11 GMT  
		Size: 4.1 MB (4123761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630080df278466ec098cf769c985da4b7ca0f0b1afb50df49d762370cde9a579`  
		Last Modified: Tue, 13 Jan 2026 09:16:26 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:953a04b991d3d7a0611fe965973cf3943b90400232dd97207e5e7cfbb496bb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72723579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7d71c6a4d4b2a66a9caa3a8fe4ecb87f80af742f20de94e5fba4c2d41cfc5d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:47:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f36a5fa281a3384abd9a90a26442f28edb507f1b9c537a07e1f5aaeb769a1`  
		Last Modified: Fri, 16 Jan 2026 06:49:13 GMT  
		Size: 25.0 MB (24952736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:970b78aeb305e78337b319a0880be9a023e77b0ed16ec19ce3a7ad7355190ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba1c0e914965ebb49dafdbc315c3563c14d051e797e635e7afd854bdd7b61f8`

```dockerfile
```

-	Layers:
	-	`sha256:792dbab9a006e657d8bd23909e1b06c99e6b8a2347ee67d261ac404f58617137`  
		Last Modified: Fri, 16 Jan 2026 08:20:03 GMT  
		Size: 4.1 MB (4112425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff972c99913c6c88371cc6530c33f3f465080d896b017740658865328d3766ba`  
		Last Modified: Fri, 16 Jan 2026 08:20:04 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:76cf6d56b4c29a87fa66676a22134292705c43c5c44ceaaa766718b1f9f226cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76141596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5cdebf8c9a37f0a8ed725621cf3bcd5d228814742730acd9e76a902e7a0a8d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:26 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:37a4de4df42fcfaea4f5148ae42a25463df13ab33af9c0ed7de844f9b658cb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6533a1075bf0521af464509b0224287490eb46ce13be38439b7910c868d21cda`

```dockerfile
```

-	Layers:
	-	`sha256:9f7c1175a993c300ae923a2bf07d70006ff16b307c8555c93214fe7748e28851`  
		Last Modified: Tue, 13 Jan 2026 02:11:26 GMT  
		Size: 4.1 MB (4121323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6968accb3814b448c724735a63d3898f62dfafd24e6a64d6162e2e122c7b0c64`  
		Last Modified: Tue, 13 Jan 2026 02:23:21 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
