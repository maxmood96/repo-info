## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:69cbf6ce8bb276d6f7de01db381cef26f32e187c142f1e91c81a366f1be4f226
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
$ docker pull buildpack-deps@sha256:225a2765a060fabb94199c07058ab5481735980b0e401bcecdae575a5d0607c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74907686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485a8676213d18a850583acd16f94f53531fc066486359a473d86075d2134c8b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:760cc2903d722922027fb5d10025696658942ecb41330109ae590e6d80a5791c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd93506501ed075000b78473d7634719bef8215bc708e66f8faa14c6582d2558`

```dockerfile
```

-	Layers:
	-	`sha256:3a9b2d813c8a2cd8ab975f332ac5807a39f592579491c843e765aaf2c875a8ac`  
		Last Modified: Tue, 24 Feb 2026 19:20:16 GMT  
		Size: 4.1 MB (4119913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ecd85b20163f3b80131dfadce9dea35d5e1f3637e3f089e6aab6e7ca69f0bb`  
		Last Modified: Tue, 24 Feb 2026 19:20:16 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:740c4074bba7a07c46ef3671539caf3f405a377ead0d0f83fdde0aff8ebd1d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71815641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46deb79ada679d782e99a8b07991b63304e755c553576995a81402d107c9f33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:56:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6c0530a0840df8a05679f77d095cbed0674c87160dab8f0e65ed5257ed4b0ca9`  
		Last Modified: Tue, 24 Feb 2026 18:42:14 GMT  
		Size: 47.5 MB (47454162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc237884c34f3f7758c4fcaea06d5eb8bbc53d28e124d2e90e646c55a9ccd0`  
		Last Modified: Tue, 24 Feb 2026 19:56:25 GMT  
		Size: 24.4 MB (24361479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3452d15bb7a7a06787daeac9c29a5544da5edd34d7da9d9dd0f3fe32a868d2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63aafae1d52d29f84e8411f48accfcf1ace161b92eae699b6d26011596675a6`

```dockerfile
```

-	Layers:
	-	`sha256:91ce495183891eabb4aa7d173a3fad2d650d7200d1f718617e29838d9860e0e2`  
		Last Modified: Tue, 24 Feb 2026 19:56:24 GMT  
		Size: 4.1 MB (4122903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd12d14b31942ab1d1fa94fa021b20ac047e8a6bdc64a076d045e0002ce54877`  
		Last Modified: Tue, 24 Feb 2026 19:56:24 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f8e126b80d6feb220a16a7fd3f5e3ac969e73482381dfc5a8b38ba6691d3ea86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69358748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707b113081c4b053d97888a0daf4cae05ba3016109fc57b99ac2dca19ee13b1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e7e4c87ce6959403c140ef3f01bab08f94d7dd517c0acf6ae810804957e70b9d`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 45.7 MB (45725086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77120a84626d4a7f2d6bdca75bb942d16ac419ff1bc25fc6e9d95035fe35f65e`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 23.6 MB (23633662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:336b09b8179a981924382bc9a69e976cc708ae6ef2317547e7c0f47928521417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff538562fb4557e581547062c74874f11173e2d3fcf2c2bc68b8523d62d04128`

```dockerfile
```

-	Layers:
	-	`sha256:374a98f5982fedc221f65e936db2cddf6a0f5718dea10940224cbcf2c520f1ad`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 4.1 MB (4121414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289537aaccb578a14173dd184db85b8242f626750a97c8fe693766748be2d336`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 7.2 KB (7156 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1f1ffec66a36906cad7d607d09e35e329a4c512a8a147797f68e1127a7f147cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74675661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86aaabf78494c0b0b23a70fa4c02973ed7de04befda2a2945bd46fd205a67ec1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fb8992036e68c75f91fe04fa437de57464af5ebf22f24b2a91cc0c57eb979ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20cfeb1659016e3c7f3d88830432efc6d5eee85f3e6827fa692f42dc958a14`

```dockerfile
```

-	Layers:
	-	`sha256:0de0c43c06ac41e05176dd1826e1978431e18d9cbe1c7c98e9c36d10b27ecb09`  
		Last Modified: Tue, 24 Feb 2026 19:25:08 GMT  
		Size: 4.1 MB (4121455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a38b0ecb626de10158025bba8752777a36299d89b7f998a11dfcd6b05f0e31d`  
		Last Modified: Tue, 24 Feb 2026 19:25:08 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9957fab98c5d47fb8e0d9fd488111bdf999692b9a80778b576909e41ba0c4c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77584924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23960a9478f76351eb918d1dbf45f5e32d7c0a4e2adb255bfc4660da56ba5acf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c637225671ff7a033f6873454fdf6a539c15748206b024d30b37d32f91f3c21`  
		Last Modified: Tue, 24 Feb 2026 19:25:06 GMT  
		Size: 26.8 MB (26779652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:406e610e3628a517dded22e8a880793d71d67e89c87397297f8aed6fb8a33bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656709fe06fee39d7ce89735629340ede7e6836376dbad5ee7706c1fa961624b`

```dockerfile
```

-	Layers:
	-	`sha256:3b89236b2d3c40f994941aef2893cc5dbd2bf54da3e2f05d8071cc0d0c997e89`  
		Last Modified: Tue, 24 Feb 2026 19:25:05 GMT  
		Size: 4.1 MB (4117020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975cff6c9f50a047e6054d925763878f2ae4d1dbb24b5d6d44d7363ec6f009fb`  
		Last Modified: Tue, 24 Feb 2026 19:25:05 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0a7cb44704f0c1e43720dcf7dbfe1293bfcac750ad6b281c7d976aa92566f5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80110259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b80cb78af919df94a9c1b87c325f59a5b9c761fc46b9fcca236cf0ff0a45c03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bdc2ae5f94587ddf291ce56c3dd3c244bdeaf3ba39bf6598fe7a02816ade7e`  
		Last Modified: Tue, 03 Feb 2026 05:24:24 GMT  
		Size: 27.0 MB (26998144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18bcd486b91ffbc8caf4517d3643c9cc37816b63ec3400be0f0a77caa81f4393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee36cf3b96ef70d1864fc8bf31bb855b9d9d933decb2d34a67229da966d8cf9`

```dockerfile
```

-	Layers:
	-	`sha256:2649f5268149aa9d13bf855f01acf022dcb29768f127a70f5bff05818c8aa9a1`  
		Last Modified: Tue, 03 Feb 2026 05:24:24 GMT  
		Size: 4.1 MB (4123761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c922d8f3978a91453a0cc21910452a687e3efa543e7c25a975084bd32f526b`  
		Last Modified: Tue, 03 Feb 2026 05:24:23 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:644929d25e6b308ca55d5d9b007cf24503ca7e52d9cd0ab3193b7740d26082ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72729924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c156dac39ca4655c89819b72e0715499afe9f393844c5eb58fff1852fae19eec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e689506e8938c3b552c90ad33fbba57defdbbcda283a92391186d21213ea281`  
		Last Modified: Thu, 05 Feb 2026 03:20:07 GMT  
		Size: 25.0 MB (24953161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2dc3a80a9b4ebadcedc0a8a0ee426c323223d6bec31a7157ec7f2c966c4aa9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe121cab290c170555c0a35e3c8e09786d09c6ce6053241e6304f7a7eb3792f`

```dockerfile
```

-	Layers:
	-	`sha256:bc9d9ca39ebd45e326aee2eabf3fabb25a2e0edd6b717fbca8d016e271aa5637`  
		Last Modified: Thu, 05 Feb 2026 03:20:03 GMT  
		Size: 4.1 MB (4112425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9bb802ab32c59865aeda5bf3b9e34770af67722ecbab57d05569d61c6449a8e`  
		Last Modified: Thu, 05 Feb 2026 03:20:02 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c2425b236a6da218f5b378165eec5699dba474c940c6cd5f1d8c11b401f2e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76155605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141dab50c2d91ea066caa769224c13b7b409a02360751abfbd04991fb6abb13`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b9712b896509afe6ce616cc91aa36b272afd379950384122674a69ff7d6929`  
		Last Modified: Tue, 24 Feb 2026 20:59:42 GMT  
		Size: 26.8 MB (26801071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0fb050ec5d78856b9ba8601c7f376f7cd927deafab4dad2708c731556120845f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e15417da5a9065f50028dea716121eef9040208caefb1cf61fd6c97cf47706`

```dockerfile
```

-	Layers:
	-	`sha256:9b951949a4661748158f5fb97c653cc8b958e78d8eb83d82f41537cea1a368f1`  
		Last Modified: Tue, 24 Feb 2026 20:59:41 GMT  
		Size: 4.1 MB (4121323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e43b6896a9c0b072519f513c60d5ad56a12180b9804bf970fc467c2034850d`  
		Last Modified: Tue, 24 Feb 2026 20:59:41 GMT  
		Size: 7.1 KB (7085 bytes)  
		MIME: application/vnd.in-toto+json
