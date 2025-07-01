## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:7b4a593025c0eaf0b7408577f89a392bb0f3f56e363b68dac17be8a37959df9c
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0beba9cdc24c8a5141a0f48ac4ce4f6c1af82901a589455f2728825d89bb81cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74881614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f75b6298ebd94b5d3cf350c7f56f21bebc34eab981886a3e9a053fe9f610876`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13567152126a6abf6e98a928a4206f022be687e979bd113ce89b0b1f41fcbaf`  
		Last Modified: Tue, 01 Jul 2025 03:19:07 GMT  
		Size: 25.6 MB (25617737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bdb68224bbfb3e1af9f9e51b6d312653284d9c681408b91d26e151eeb1e11bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f632765b131bd4e6a0561bb0d03ee57a718c915dc7c858c1544d85003d53b22`

```dockerfile
```

-	Layers:
	-	`sha256:47f0f0da8fe075249a30b3df6a899040cdd0ce387c87ca7a2d84c86357762914`  
		Last Modified: Tue, 01 Jul 2025 04:09:17 GMT  
		Size: 4.1 MB (4116352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354a3b8545bf2007bc184862dea9b7390727f3bdc8087f98e7b0d588e7e8c5ab`  
		Last Modified: Tue, 01 Jul 2025 04:09:16 GMT  
		Size: 6.8 KB (6820 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:74f3538cb9d899cc569855bd1c7de13abac2114f4cd0c6b4dc112c8a79539130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71780659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e80b966fa52336d051f0aa69111f3b747dbada727a2f809955d18f1ea2171f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8c456e7e2a39b691845cb9954fe5483a7f4a7e63934a177c56842196d0ce4501`  
		Last Modified: Tue, 01 Jul 2025 01:17:08 GMT  
		Size: 47.4 MB (47435500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653e9f2049e323a33a896b4a879cddc21245e9416fbec489493472f8cd5b7495`  
		Last Modified: Tue, 01 Jul 2025 06:08:20 GMT  
		Size: 24.3 MB (24345159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:af349a202588712afdfcca0e2788fe550fdcd1035ee41969852547fa2e304ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4135468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9e43a77db2fbc223f6e0e36c0a172c58472c1484bc84284784afe73413419f`

```dockerfile
```

-	Layers:
	-	`sha256:6f7f82af427dee4ad8db732ed92d66d65dff61034dea8ec7caad704bff33ecac`  
		Last Modified: Tue, 01 Jul 2025 07:21:40 GMT  
		Size: 4.1 MB (4128587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a17d0f22ae40e6ea9ecd8496a1eb946d041e98abc24880e9494d89f445374892`  
		Last Modified: Tue, 01 Jul 2025 07:21:41 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8e2e4837c94c2e0547286ee383fec24976479ba67ae2e3d60ac7c7ec3a6ee1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69301578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b5f32b8f7276130e20d80701a34ffb5fb0aea6105f8311cec2482993e19894`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6c3b2ac1d8de7f6b9efb67d4f8df7036728aec7a9268a04eebbdddea82d555f`  
		Last Modified: Wed, 11 Jun 2025 00:29:31 GMT  
		Size: 45.7 MB (45702045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b97e79d9850f63633fd52187a6c3a6855596f84e391aa2167c27363cd92c43`  
		Last Modified: Wed, 11 Jun 2025 12:02:56 GMT  
		Size: 23.6 MB (23599533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef6ed5706ddc0d85f56e4077e33d27b3dee000fa19e5d08d28d10244970ddcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975eccd1b5a747362489513780eaf0f424c218f9d5a9aaa57712d39b31766edd`

```dockerfile
```

-	Layers:
	-	`sha256:f857d8392da493bd2c80ef04c71802c9c785a7798be74195c4c6230ca9a359ab`  
		Last Modified: Wed, 11 Jun 2025 07:20:44 GMT  
		Size: 4.1 MB (4113800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40febf4764de4ae96531f7cd107b98cda0562db2172d5d9b321024bda20f9d9c`  
		Last Modified: Wed, 11 Jun 2025 07:20:44 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ebce0e9ce03932c4f656a61ca0859b9ec3f24454a5304b558fc218d76f2ff95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74638156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ba2fb257d48113f0baadc5520264ca032ca09a76df1c4ace2a6b02300f246`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064b8e4cb92aed27a99de363dac49c85bcb74d556fa925c921727dcdf03f7cb4`  
		Last Modified: Tue, 01 Jul 2025 06:53:32 GMT  
		Size: 25.0 MB (25008002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c3763c9b76adef2911b899b832af5a722e2b3aff53bffa1c10c8c923854f745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fcc8587d7c89618fc76bf18d0765960a0945bf6238c32bfafd41658781fa53`

```dockerfile
```

-	Layers:
	-	`sha256:a5139e1dabc8de057d7cd1f66c5fda0ebda0b0ee8a1add7c5f6fd0462d1bfdde`  
		Last Modified: Tue, 01 Jul 2025 07:21:49 GMT  
		Size: 4.1 MB (4117882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8456aaa37c48b23d17e8bd9acfd4f91b0a2ae12b1fec5e713d2542249c38520a`  
		Last Modified: Tue, 01 Jul 2025 07:21:50 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:54d5058a23267f357f20c4e1554f21f3213472d90376c9db64d03c19e3531f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77558904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc09c00d560ff39d8d3a3f10904bf815a851d5826120c0df849a7502d3c18ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d223755a7489df8352d3a71955e26d35281b9c0f0609e017af54d9e75e3b435b`  
		Last Modified: Tue, 01 Jul 2025 01:14:59 GMT  
		Size: 50.8 MB (50786756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d932d83e6c250bb0f5c2003ae98b3b4dc3d40d3915a7ebed763f315741368`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 26.8 MB (26772148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5197760d51a016b07d38140197ad02984002319cc9229b46c0a74092b2846a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbb7cfd218d3da4e2988bb29f505060a14d51ace0cc7b14fe7523942f9b8727`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec026f9c142114b17b9a0c649718b321462618514745806c423a0e67db2ce3`  
		Last Modified: Tue, 01 Jul 2025 04:21:42 GMT  
		Size: 4.1 MB (4113466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda6239e24e80398c57212f17bc1e066abc558351daa0f48747a78ced4e237ef`  
		Last Modified: Tue, 01 Jul 2025 04:21:43 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:411b6a79c9c6992ef2d5601d3064f79a05995b6f71d6f44e6b3f5f693c19ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80100505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d4e1ec739a393e89eec8eed56524fe65d8fbed8dfb20a94d76962d08bddab1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e868292aa714037cbba25d912564e5f392a5d355c383b03a8854e789c98ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:57 GMT  
		Size: 27.0 MB (27003269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:373cf00346c4a6c308761f5b8d1909bc395db69fea5d0debb69f5177db9daaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4136295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da18e32d8afa2ea7092ab8c5566e2b6d9e90074e6dc7f1c2d2149430c67c6ab5`

```dockerfile
```

-	Layers:
	-	`sha256:20654dd738d63b454ff920fd70d15d2de52c847b830d82278d73f8da8c223036`  
		Last Modified: Tue, 01 Jul 2025 07:21:58 GMT  
		Size: 4.1 MB (4129443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26110bf14bb5bc77c9f188cb330f4ceed2055d01c2bea13b6cf05ced7f38d622`  
		Last Modified: Tue, 01 Jul 2025 07:21:59 GMT  
		Size: 6.9 KB (6852 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:22c71c37ed7d3396773c84e52f06e2af769ae7a6ccfc9217ae461eeee8240fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72703116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c79ff217152c65ee870c07076ee56875093b73cb87dc7cd4762a35e86037afb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5ba72abe20b30be07f6ab1e6cdb1c6d040c269e383e9066cef6f8229dea893`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 25.0 MB (24952958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25a5c86415696231d390846baa26176de259ef21c0f3cd4bfc0b365e5e63ba3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56b8e8573276e082e158da53a9429dd4c5d95cb1e57367f8f46e92dd184248e`

```dockerfile
```

-	Layers:
	-	`sha256:ef4d52e5690de5bec8a368726c50771ab9f1e4bd012c8032de3deed847ccd1f2`  
		Last Modified: Tue, 01 Jul 2025 04:21:53 GMT  
		Size: 4.1 MB (4108854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34abcfe0c7ac9c3ae57964223592acf7e70fd5090938a3afbce38a0aab1b1c63`  
		Last Modified: Tue, 01 Jul 2025 04:21:54 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f3a3de7b9565afb3b5bc75030f0e9cad7fa9703da7865ace23cd02465ac668d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76129369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f50ae623c9c125a967ec4d4d400399b23077aec9c9ed5ec44c4a1cb4214df9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8974c848015ae735631f879693069b8c536e3428274d79917837c027655a80`  
		Last Modified: Tue, 01 Jul 2025 05:31:56 GMT  
		Size: 26.8 MB (26785709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:785cac082f5c998f791271b06c6c4e9328e7cfe44159d591e594314208e0a3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4133836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b68c26f67e6eb80ac246b3fea09a2f471ee001b129e6f676e163d257c102e2`

```dockerfile
```

-	Layers:
	-	`sha256:9f3f412ad55080d9d01f5dd82da2f23c22a707bba92c465826bcbae333a3260e`  
		Last Modified: Tue, 01 Jul 2025 07:22:06 GMT  
		Size: 4.1 MB (4127015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6263c0ff5c5480ec82d432746550b9a11e0ff9d7db4bac099cd01fca668c97`  
		Last Modified: Tue, 01 Jul 2025 07:22:07 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
