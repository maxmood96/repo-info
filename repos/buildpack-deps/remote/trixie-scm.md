## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:8810a268d81f1f870eba1d297b2d2ca8fe9ca192e1b054706be0d232b6bcac09
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0080247c3791897912801ac38be74815cbe9b03d4739517f8a2d29993337c77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142671296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764f6bf619595c83f009d547aeb93e0c38eaab94c23ec5d886b1e229f1a0bdac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:0f696393bed22361a2f932d3f084750c0cdf7e1f7186888c327230081e6257b0`  
		Last Modified: Tue, 01 Jul 2025 04:12:14 GMT  
		Size: 67.8 MB (67789682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:580d323d8bed040942104a925f8130cf77db061661cb948bdc9b187d2960ae33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a850c58eccbae4c43c580821ee18b42b3a18ff0a6d68e8f19d4a0d965462f32`

```dockerfile
```

-	Layers:
	-	`sha256:ed96140e78673ce6ff8f2a38d5ae2c4c17b45f352b98b10dee95618bb932276e`  
		Last Modified: Tue, 01 Jul 2025 04:21:36 GMT  
		Size: 7.8 MB (7759027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80be17777321e64411e991bd7725636d38c93b7522e1c4ed437a226923721c0c`  
		Last Modified: Tue, 01 Jul 2025 04:21:37 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ce39b5e406bfbb64a6445e9fc0676b7dacc6933860eba3eacc108f3e58f8d1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137125456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4416446732b0ebca622a6cbd97c879ae158a37101dde11ff9948725593a9f76e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:76fd80456b32133234b703a95814a6830eeec2101deb4bd4582465bcb61a60cb`  
		Last Modified: Tue, 01 Jul 2025 09:30:44 GMT  
		Size: 65.3 MB (65344797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9554455119f4e7d741651d36cd3eb894a91e30ded8c6c27ed87110cb77f5277b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6237e4f79c4d6023379c34b1c9c8dc07f50e69b2228ef8176b3d4c82b67fe379`

```dockerfile
```

-	Layers:
	-	`sha256:a92602aa7ff83e6715964caa22f191497a5f1d808e8e91f2a1d1b8ffce8e2bd2`  
		Last Modified: Tue, 01 Jul 2025 13:21:24 GMT  
		Size: 7.8 MB (7769310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e065e70e5426f48fa1ad33cee4a45fcad477427e91413dd3cd32f250d89ac1a2`  
		Last Modified: Tue, 01 Jul 2025 13:21:25 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:841b355943c276b2aaff5b15e583af715ea0b47f70bd539a06808735e98cb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132073652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6de4f6d4f2f79663dc2b759e233df920b86748e143bc9cfc1c4046fe0a7e8ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:40f0250cd76d089e47a026dd511a8391d815ac5e1cd3ef860f0d3c434d13a9d0`  
		Last Modified: Fri, 13 Jun 2025 23:07:15 GMT  
		Size: 62.8 MB (62772074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9cc2afe9fdab2071a2e63acb35f30fb85e7e375948b0a72fa8790ef86b6c4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e4eb8dc1f5c78e7b22712257ab418f69e5bb5abfcdd37dc249b1541c1ca80c`

```dockerfile
```

-	Layers:
	-	`sha256:b5bae8db5dbaf575234046f55cc8df5a2278303bd9ad09506d3a9bce736da0dc`  
		Last Modified: Wed, 11 Jun 2025 16:20:59 GMT  
		Size: 7.8 MB (7755481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180af898d9589b388127a74230c111288c2a07acae2bdee026fcce5d75903ead`  
		Last Modified: Wed, 11 Jun 2025 16:21:00 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bad77fbfaa0afed3274707150e38e74127a8cbc7c776e50b3ad79358902357b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142252242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed90169c3bf6544f01334a37cc9a158f1eb642c6286af8397f96a9f08865499`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:ded0afb06efd2b7ed68e17cae5e6e1baaad41593041fa16eb9d856160e2bca6d`  
		Last Modified: Wed, 11 Jun 2025 10:34:07 GMT  
		Size: 67.6 MB (67636505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c49280d1021abc5433a892c68cbd12293cec650b21b72b3e1c835c7bfd6d0913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59817eaf15bb620d5fd1ecd08fce5f045a8d50aa1efdb3ccb8c74b8c87f9376`

```dockerfile
```

-	Layers:
	-	`sha256:d5a4b4d4196f5072c0b97b9facdf7a358f3ce71e6290e35b284a6b381f3c4d7b`  
		Last Modified: Wed, 11 Jun 2025 13:21:17 GMT  
		Size: 7.8 MB (7762645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:447dc6ca22798449377296f45fe3e9bce459931df1b4422290e22ec73bebdc73`  
		Last Modified: Wed, 11 Jun 2025 13:21:18 GMT  
		Size: 7.4 KB (7394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dbf23b3ea970deba46b608a5b9ad938a058ba3a2307e3a956f1f0bd3e0493a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147389210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fde234cf00922b5d70b7802490477873e7a382556212eec8cddd740feaf3db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:ac34925744005802787be957c67125f2aabf94afd5e8609668cc037c46d09591`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 69.8 MB (69830306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:14a9f25e29e548172b13a1df1e1cfed3838f5928b5c890f154db65c148b9dd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c639d8be936e2009741afd545201e093745e46a28cb403810b1c7ed8dcf51e2e`

```dockerfile
```

-	Layers:
	-	`sha256:14fc467fa1e5f6a02cc269b7cb76e5d06fd81c7c00197e8ee41b9ccdd7c3c735`  
		Last Modified: Tue, 01 Jul 2025 04:21:56 GMT  
		Size: 7.8 MB (7755168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477a316a5364e95c092f06aaaa833de506b90f8ff6d2ee1a81d09b2eb0f02e90`  
		Last Modified: Tue, 01 Jul 2025 04:21:57 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:920fab3bb33a1b897303226655311a05f5f1fe95fb9507586edd5b671adbc4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153169448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1713d2340540082469690153809f011724b834b84bd942668abeaef833e36912`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:0a7107fc95f855d7880e921bbc85bf915f07c907c70d7d6f6a5334a32ad6c832`  
		Last Modified: Tue, 01 Jul 2025 10:12:36 GMT  
		Size: 73.1 MB (73068943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d666bc934d008a3de22438af710ebd155c05d6527be38b61fe3ea02f21c16a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c87c45145a047f483ddeaa71d2871aad482c4bcde8b577c6bf4f55d0fbe079`

```dockerfile
```

-	Layers:
	-	`sha256:528b07c03d9b8f1fdb9b4615bf405b103039d144f89dab8af5fe7d38b80deb9f`  
		Last Modified: Tue, 01 Jul 2025 13:21:45 GMT  
		Size: 7.8 MB (7775395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81f541e26bb9b9517c815212206c6a62e4051bffa11d1035762281e42f4c6bc`  
		Last Modified: Tue, 01 Jul 2025 13:21:46 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7c1214390214c9bf29c898d1fed7362423321f69217901bb0ba9e3d34f671b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139372211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8af00be58d32cfc44cfb9d59bee46cdbbd68b063e2577919102e9a2deb1096`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:39d4236a35a94e37c928bea093f065f7444cfd390eed1e2bcb50207c2c1b8a97`  
		Last Modified: Tue, 01 Jul 2025 04:21:37 GMT  
		Size: 66.7 MB (66669095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:443ba036d6c004c9d0fb2f92c0dafda60dbb269550d5eae6466356a7ba472cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2790cf91f092d6d354134eaef78ffa748240851aa9a2d8ef722f2afcade075ac`

```dockerfile
```

-	Layers:
	-	`sha256:9c1e9f564cbb9e32fa57f3dfc3b8c113b4b8531b043b7771ae25297ab066fdd5`  
		Last Modified: Tue, 01 Jul 2025 04:22:10 GMT  
		Size: 7.7 MB (7748855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616a6ed9470257eec4adc40b9ac715e3cfbb1f0cf0c15cdb709584c6fadc8647`  
		Last Modified: Tue, 01 Jul 2025 04:22:11 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e35ea640c857ee15a4eb8d17def017c2beafbeb77ebbed3d736560aad2a99c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144793193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71844af78107da44f2172ad508f7b2be8051fd88bcbc3b93486f497592fc7a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:0c7360cccf58cfa285cf20d3ce14642c23bf3a2795b93396d0b9b743ee2e0779`  
		Last Modified: Tue, 01 Jul 2025 08:59:15 GMT  
		Size: 68.7 MB (68663824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2da27f8a391e9fad72a2e1ab16c024a4138751a02a2e52ea0ced48084f2816e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146f1e53de9b1d6e32146164f44dd1dae44979e52d5f69fdee905f0870572a44`

```dockerfile
```

-	Layers:
	-	`sha256:a93f9009e116dfe9f0f7ece0a73afcbc866ffd8577771de507133d99534abb3d`  
		Last Modified: Tue, 01 Jul 2025 10:21:24 GMT  
		Size: 7.8 MB (7769193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe3bfea2a553540e85f092c34b5efd0a36df370a8947b09d1f0b1095b02b2d0f`  
		Last Modified: Tue, 01 Jul 2025 10:21:25 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
