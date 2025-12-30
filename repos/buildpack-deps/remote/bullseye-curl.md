## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:a7c5564c5a1693213413709a2e2982910404f4652c500bf268d69b91c0b41003
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
$ docker pull buildpack-deps@sha256:3d256da522be7179f083e9020640055ab9d70d1f5eb931361d35b466571397da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63925693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cac37a051547531ae07ff0ca1b950b6e1b6d35e2fefccfda264ca4dc052b50f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4b405dcfbbf208b50f83cb073fc2340dc0c1fad234dcbd26845122feadf5cc1f`  
		Last Modified: Mon, 08 Dec 2025 22:17:00 GMT  
		Size: 49.0 MB (49046374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bbf36f43e54145168310c9263866569faa887bc243d2f3bed9e99c1532e0cf`  
		Last Modified: Tue, 09 Dec 2025 00:05:40 GMT  
		Size: 14.9 MB (14879319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce1ac6e6ce07115109fbf5b9520ddcd4e38b46555721647cacee85c256d8096f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfb2dfd35d4d0aeda8da4bda790fec4ac78afaee92ec0013c957fdd6e774649`

```dockerfile
```

-	Layers:
	-	`sha256:5403df84e09a244c3a7976846c6ee49106100cefa8661bbf492f5f69788f678e`  
		Last Modified: Tue, 09 Dec 2025 02:21:12 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2197250f22dfe06db0829d41a7b186a306662cc29ac7b40b97f88808c0be3568`  
		Last Modified: Tue, 09 Dec 2025 02:21:13 GMT  
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
$ docker pull buildpack-deps@sha256:127a90dd16e12bbabbb53f74be5e94a53e5a311231c24dc3509ed930c95fa574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fa7b84364b9a99c68139e8dda5776f402ca8f1a694fcdb55d7e2ffe75df52d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20381eeb836e270b6cf9dd675babbdf823eb79206c868ce7f8ae8aa6250aa68b`  
		Last Modified: Mon, 08 Dec 2025 22:16:45 GMT  
		Size: 54.7 MB (54699532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b1d3bd8e8172de52ae5d3823cd522bc420b102de9f2d204bcdd0b93d98aeda`  
		Last Modified: Mon, 08 Dec 2025 23:14:29 GMT  
		Size: 16.3 MB (16267791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4bd01b34ebef18135ff2355ec394cd961b3ac86a7453f8f607b2cf94cb10e926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be082a63d1f80617cd1f6459933ec5d1b758fbb1ea525d24384301112ef0287`

```dockerfile
```

-	Layers:
	-	`sha256:14d37c4cf63339f0a73ec68939f417798d3e707645921517a0f99fd3c7af0816`  
		Last Modified: Tue, 09 Dec 2025 02:21:22 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361a08e1d6047bc513562c5b6e67169a0f5c7abae514731691b7e025e25617ed`  
		Last Modified: Tue, 09 Dec 2025 02:21:23 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
