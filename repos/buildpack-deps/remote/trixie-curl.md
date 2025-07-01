## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:5a54fccf457d0821a27cdcfbfb0f5261436c7b34a183230c099cad8b98002597
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

### `buildpack-deps:trixie-curl` - linux; amd64

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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a4c4524cf0a35057762c54346f1421c78d690525a63d46c728ce78c1d9250cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71772206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce98a44a7d44307bff605999e92b1aa745e51432911540c1f724a10ea8e4fd9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b3435ddf0421631c0396c34acfc4d54793f2c51e2a8b92677402c8f9e0513af`  
		Last Modified: Tue, 10 Jun 2025 22:50:33 GMT  
		Size: 47.4 MB (47445410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be3896271877b3e95aedbf07f86334bdb2f5374ed0d8dca30695208865ab49`  
		Last Modified: Wed, 11 Jun 2025 03:14:18 GMT  
		Size: 24.3 MB (24326796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3373997a2b95beb78ca2bb6cf7a05c067b8efa8aee2ccc709d7b3a419fa5fef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410de526bd1d6bf05cfd282f0cbb4a4904c4062580f30aef2aed9a8a44edfe96`

```dockerfile
```

-	Layers:
	-	`sha256:e3c408323f62458f04aba7eacab99facaaa861287bf036cbea1a2e2280cc98a0`  
		Last Modified: Wed, 11 Jun 2025 04:21:24 GMT  
		Size: 4.1 MB (4124542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90a9441034dbf63c8a844febb4bc8c0f8aa23dbe16948dfa5c3171aeec71cc10`  
		Last Modified: Wed, 11 Jun 2025 04:21:25 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:91f921e9ac6db87ba836c96321c3a736884a8d9a413f5b2b37350e9ee9afb254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74615737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee201c7a25cc687bda114aac2aa4f9a8fbd349ff201703be98ad4852c332085`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439ee882f07f6b24af6e46850d9521759d30430f3be41cdca454de5566ec0ab`  
		Last Modified: Wed, 11 Jun 2025 02:57:26 GMT  
		Size: 25.0 MB (24994209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9df3c0b997b4f677740658e772e78c961c2d5c039c388152a85695707021b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8967f4d31a292bdaab1afe30ce0b6d93f08a4744a0d3794b222534f48be8918a`

```dockerfile
```

-	Layers:
	-	`sha256:97321f2aed4f95657be9cad1245e3f112d505ce97a3077fe4d4b372b8763ebbb`  
		Last Modified: Wed, 11 Jun 2025 04:06:55 GMT  
		Size: 4.1 MB (4113837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa388c7db70a880bc5ddf7d9206e980cec5271edb2deae1011da52412e8e2c5`  
		Last Modified: Wed, 11 Jun 2025 04:06:53 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c4d1693da457c5a59005535592bd5eea2a5ae8b4932b894fb23c60d3657e5daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80073331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730ab30849c32af05ced9ed4788edbd3313076eea5569ec15771b7f172ffd015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:70a0e6b9f26ae2a311f0c79d7ff095922eec7e2aa39f94bd8c4e5b385cfa847d`  
		Last Modified: Tue, 10 Jun 2025 22:52:26 GMT  
		Size: 53.1 MB (53090933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e8d7ca19325e1e81102ab8668168b260e6e57b98b333eee8bca0ca1d7fb15d`  
		Last Modified: Wed, 11 Jun 2025 17:42:50 GMT  
		Size: 27.0 MB (26982398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb5e09d8cc6f709b17d51a3c504c66d27809339fc10126355ef8cba370e110f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe3ad39eada6831eb26a13026ac065b99591d26ab298c59e00a69767719f042`

```dockerfile
```

-	Layers:
	-	`sha256:bd710e1efd8ce6372c17e87d4f4efac2ade7a403d8e977ac8294f2ae5e4a767f`  
		Last Modified: Wed, 11 Jun 2025 19:21:06 GMT  
		Size: 4.1 MB (4125388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc38638c830dcceff3eb52915360f3261f6815a9b547c51364c988e119e9e13`  
		Last Modified: Wed, 11 Jun 2025 19:21:07 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:477fad43bdd6a2f82b63d3e9e76db9663226c146741e5029bb79197139de488e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76097193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb152ae3bb1affb848ee8f59609a009ec22a96dec9911d7ebdc92f6d615a6ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588affbec95a011eae8d19fbc59b872f3d6089f972f16713469d6820e2e3fe6f`  
		Last Modified: Wed, 11 Jun 2025 12:02:59 GMT  
		Size: 26.8 MB (26767425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18de74f2e1840dce3b34f2675bd0fb2beebecf4e788b1638cb675f461b540d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182d98dd9a6569e32b68f57db9c4d3db7ad0f369aca14911ce4710cfb4ea9751`

```dockerfile
```

-	Layers:
	-	`sha256:a29239fc5b7e0538fcda15659222d5569b3524d660be286c6c23c6ebdaf927d3`  
		Last Modified: Wed, 11 Jun 2025 04:21:48 GMT  
		Size: 4.1 MB (4122970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0457ff2a4cb7e3374085d8f52d17723e6c449c34e1586db5b77296ae8bc2df6`  
		Last Modified: Wed, 11 Jun 2025 04:21:48 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
