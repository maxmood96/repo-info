## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:98dd577c966b5901ccbd5ee010383905f5485d290f05fdb458edcec202f438ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:af561c4a261e999aaebd5f76519267623b74d46cd14fc3d3ef9f4380eb0265f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a481dc8bfa5c014172cd53230ab6584be8ac22b837b0c4559d5c5fb0116474`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac758735be4df7bbee87d37924a15ccc254964d763d0b8620fdba9dc6d6774b5`  
		Last Modified: Mon, 29 Dec 2025 23:45:40 GMT  
		Size: 15.8 MB (15764112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4f8b3af1bc91d60d820ab399221e9019de6c6313207b6552a8a44c44be43d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2032f8b1bd2cda1ad71a049c7064e9e76016ca331464077c55ecef4198fa2be3`

```dockerfile
```

-	Layers:
	-	`sha256:caf676c0275090e17a602fd7a969fca1d574b8345eb882736809b5c3b44555f5`  
		Last Modified: Tue, 30 Dec 2025 02:20:54 GMT  
		Size: 4.6 MB (4629099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7fba587b0b280acc3d91e3ca6225ab4e690fa7032c6a7bdf8a461b4fa004f2b`  
		Last Modified: Tue, 30 Dec 2025 02:20:55 GMT  
		Size: 6.8 KB (6763 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:18620399cd9a09c0bfd82696471889040ade2c3632a26f4a232cb39f8755fc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63925934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbea80853c8febbefe65a5cbaddedefdd91022d7568772dd4f2279008a043c18`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b46683c1e86f7a120aca01c56dfafa77513b188a88759ff45f42ce118f9a337c`  
		Last Modified: Mon, 29 Dec 2025 22:25:41 GMT  
		Size: 49.0 MB (49046401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf8c40ad8b4e8cd6362fd57fbf345b792e3a334f7cfacc579cfaeef4447f6`  
		Last Modified: Tue, 30 Dec 2025 00:34:10 GMT  
		Size: 14.9 MB (14879533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:463e60ef02e23fb31858c1fed4b1ee30e550e51479b0e6949bb66cd9cefe3ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1c996bd5ff772b120a228cabc9c4728b0b1765bba551a59b29ed3b6e0a7833`

```dockerfile
```

-	Layers:
	-	`sha256:f32dba80855d505f14190e317e3fbebf8acbcc487ad36b76bd5232ffbed1d43f`  
		Last Modified: Tue, 30 Dec 2025 05:20:42 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b35ec140d5d2f21fa8b1f1e93b64fcc672056eaf4875ef3d109738aad799e69`  
		Last Modified: Tue, 30 Dec 2025 05:20:43 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe678dd54e6d7fc1d05ec3c8b77831f97e1294998fec9f18b620c0feef883846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68007151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0eead5cc89f7beaebf820ac68a8a2e36bca680d8b748820a35ca2a947703e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549a4595c672d6f3151acb8314dc1cf09736bd0b263013f6ec6856c4c63f19a`  
		Last Modified: Mon, 29 Dec 2025 23:46:10 GMT  
		Size: 15.7 MB (15749381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e66643ddcbc92c3f86ad9824bf9da22031c9dd4d87f7de275ee9070fd9c2b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936e3bd47d50026782bbfb14bf2b93312fdddcb817ddc8df96b4eccee214d425`

```dockerfile
```

-	Layers:
	-	`sha256:0880043d6f0dbb5a014412b1a68eefd0e79089b10fb9e7438eae50cc6982cb3c`  
		Last Modified: Tue, 30 Dec 2025 02:21:04 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad739803068ebe6508eb8559e343ad7d8f30fbf6a3fc3bfde2d48682b8290a4`  
		Last Modified: Tue, 30 Dec 2025 02:21:05 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b6f9577dfdb222af75997dda97cf1babdc7dcf01a0ca61a516ebc8ae5b2fef9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0ba0c7bea63ced14c74ea6fec25c53eb60e92280c08d9b48ecf064eeb3d0bb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:025f128203ca36b1f5bbcf71b38334a935a5d6b64f4bfdd4dee99a843a623eb2`  
		Last Modified: Mon, 29 Dec 2025 22:25:07 GMT  
		Size: 54.7 MB (54699587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3022123a59bc3e9201838d9bb8187e2c0436e8d72f121e714ce751ebf40452d6`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 16.3 MB (16267837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd88261e2ca987bed24ae129a2caccf1b67fc5945b9043bb3025eedf0250e383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e415cb5e7821ee53fe1fd7107d2c291c67204b7d7551121a3bff82372779e2`

```dockerfile
```

-	Layers:
	-	`sha256:7712297ee7f4731c7981f7c822a356fc415253c7e3fce443b8f12592adc327dc`  
		Last Modified: Tue, 30 Dec 2025 05:20:50 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22caa88fe8cd895603289c697d4f88fdc354fb38a7e0a6a5b4b6a563f618e938`  
		Last Modified: Tue, 30 Dec 2025 05:20:51 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
