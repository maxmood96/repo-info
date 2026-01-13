## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:89ce950c58ad83efa4c9afac41f3451a87b92d7c6efcd3931550ced0632a8eec
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
		Last Modified: Tue, 13 Jan 2026 02:11:21 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:30:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:22:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:18:45 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:22:57 GMT  
		Size: 4.1 MB (4121414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a3f9537cef0cd4a60c5af5d20f2e29b510bd5034bf03e4f3a2002d758d4089a`  
		Last Modified: Tue, 13 Jan 2026 05:23:01 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:23:07 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
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
$ docker pull buildpack-deps@sha256:c6199ff44dc6f13dc78a5826dc81d332918d343d4f3f91ef972befb0ec65ad35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80105302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2426d874f0ca285e7c8029b22284010f00964640a36004749561cd7802c266bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44afe623a2af1e017b0756e314b5b0882afdc551ddbb8ab4a0e0d718eb8f20`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 27.0 MB (26996817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b32d1c8d8611549ed3b530efb015083aea1f6ef1ef34c2cef62e3e411d6a22a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadc8e4e7658d3c0f9455d3ef94f3d7ebdb32573c8c1ba542e91fdb4041e3991`

```dockerfile
```

-	Layers:
	-	`sha256:0258a3735c1d06990e9050ed75dec64f9c3fa1f1eb9cdc968ed44f150226c6ac`  
		Last Modified: Tue, 30 Dec 2025 05:21:16 GMT  
		Size: 4.1 MB (4122720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a7c52c865f47f81fa21b414a1de26dd00f57b0aa6e54c83bf1279265eb0294`  
		Last Modified: Tue, 30 Dec 2025 05:21:17 GMT  
		Size: 7.1 KB (7123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d89572bc8e733e13aa0c64005afb33c1828b8008aadeaaf81220f6d367d7235f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72725016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a5728c2e5c67ca84411317df10e3709fd52cdbe88d77f227fc7820982c659d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f7933c6ef71f06a1f0f33145f157cbfe6df70a0a3efc496c514e6bf0f3c52`  
		Last Modified: Wed, 31 Dec 2025 10:17:43 GMT  
		Size: 25.0 MB (24953863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:880bb221d54d31e0f4444035023ff01b4e481a43ecd7d4ba8c48f2c28dd31f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4697e4610a087700d2ff59caa5d9cd57bc364898cfbdb15acfa59c3815b2cf7b`

```dockerfile
```

-	Layers:
	-	`sha256:888ab53a5fdc7fafef0ccef1f1793012feadbd6455aae29e2267d31da8d3375c`  
		Last Modified: Wed, 31 Dec 2025 11:19:59 GMT  
		Size: 4.1 MB (4111384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ef3bd4d1df302f481632287670f007e159816c3f329671fd9e0d98e0c4a61d7`  
		Last Modified: Wed, 31 Dec 2025 11:20:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:11:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:23:20 GMT  
		Size: 4.1 MB (4121323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6968accb3814b448c724735a63d3898f62dfafd24e6a64d6162e2e122c7b0c64`  
		Last Modified: Tue, 13 Jan 2026 02:23:21 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
