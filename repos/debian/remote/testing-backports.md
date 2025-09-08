## `debian:testing-backports`

```console
$ docker pull debian@sha256:7cedb6242ef8c17fb4d6f2857960ec598fd2d8cb99671f49fc874568c42bc2ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:54a561de783da666b7529b23fb509718627122dc63999facd6006576f8abb5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49575260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6481dbf0380933172bc70750d8164fe882173440fa70563c71525e7d164e7bc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6ab7b67a197cbaabd3b9625fc408e9e525cb4827257b84c6dffb4f74f04d2b05`  
		Last Modified: Mon, 08 Sep 2025 21:13:07 GMT  
		Size: 49.6 MB (49575039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa46af712b1e91b6a4f16eb5c0c553519ccfdeda3fcf0d1100a377e951d1fa8e`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:69e320c557a159600bcce2e1caf31f47a9f309ec4e1774779c25567cb738c961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58a4144bd2c930c8585d64da6a3ace43bbad168c10b3d2a5d21dee139005e3c`

```dockerfile
```

-	Layers:
	-	`sha256:8c4483a300eb9d4b852729f486035308376d26a984a04970673721ee0f2e8f91`  
		Last Modified: Mon, 08 Sep 2025 21:30:24 GMT  
		Size: 3.2 MB (3170759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54eb886b88fe19e32e66318f42d8c81066e2e789b27016241f0daf63c15503ba`  
		Last Modified: Mon, 08 Sep 2025 21:30:25 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b209cce512432fb17981d96e7932b0c0cf6231c639a71f4230e91939ac46a026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45943442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3eb3968e57135352f9843181c1bdc38e696df323b4ae97b193366462408e92`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ba62ccc5496bfc6fd1ebef0a0ed2ee36e196b6f68339f9bb39ef9f0cdbe0130e`  
		Last Modified: Mon, 08 Sep 2025 21:15:10 GMT  
		Size: 45.9 MB (45943219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d99877e3f3f6f0e4893a2c8da77c7f09d97956df212acc0333a49e792c33bf`  
		Last Modified: Mon, 08 Sep 2025 21:54:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:46c51279258bc737572b96d7b8d3da76bdee7315b018a99b69982d9ad9da41cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c86e6fc6ee3d8ca5bae4c53982e16b95c0a06d658f8812af43ca8179440a9a2`

```dockerfile
```

-	Layers:
	-	`sha256:d8c2793d7b50587565dba7793505f051018523d0a9984dd15c4a80f9c8709695`  
		Last Modified: Mon, 08 Sep 2025 21:30:29 GMT  
		Size: 3.2 MB (3172133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1de16030a95ee5a8dd8868877cbe40090d2f6c91eb8c0a2303036379146269`  
		Last Modified: Mon, 08 Sep 2025 21:30:30 GMT  
		Size: 5.9 KB (5893 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:87759d47153f1dbb1b1bb5779370eedb243bbb579df09823bd3f38a68cb31fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49863712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7db8259e097390c5214131af2baa18c7ec3a65cb7bd032926e55da9a6721f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:008c1ca0cb19a0a582dad95007bc30c33500300de3bb8e851eb4f56693a697c6`  
		Last Modified: Mon, 08 Sep 2025 21:15:15 GMT  
		Size: 49.9 MB (49863490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ad4f342a9f1855bd55f7d262331906e46061b6cf0c19909b63d17a98e09df9`  
		Last Modified: Mon, 08 Sep 2025 21:35:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:02a466de85416e0721102500d10f425d236f9ee1a65ed77b034c57de36319102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7652ae05549832f0102b1d68e10d5b71451271589f05f0ed0c49cce047ff57b`

```dockerfile
```

-	Layers:
	-	`sha256:0934fd2a99eb5c78c40238bbfe798a787df50a0f9e47be1d104f976d3f5d4f4d`  
		Last Modified: Mon, 08 Sep 2025 21:30:35 GMT  
		Size: 3.2 MB (3172240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0eb67c0c01680d34737238f314d2cb320fed36cb6aec49eeb92229e59415fbe`  
		Last Modified: Mon, 08 Sep 2025 21:30:36 GMT  
		Size: 5.9 KB (5903 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:8325ea465f96a4a2b37d4b64b93525c719682c9602545f2cd4827b57e9d8c31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51050030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3092519fcf0f4ef89fee44d42c25cc17bf3bbab313ee7834675754bf94232757`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fe0bda1df27d431e020638bc07b0e6abed9dd904eee676c5b8d3eb6b271aada3`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.0 MB (51049809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e3161fd4b3ebbf8f77ac435f5eb0d4607fd0a47eaf99a0ac42c07655b2680`  
		Last Modified: Mon, 08 Sep 2025 21:52:47 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:159f344e03d9c5f8ab82378d525d67ba43b6d5010b6afa97a61828322d30889d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ac275698acba719d145586c9b136a7ba61f4ba4953ae6465108abcb2dc6873`

```dockerfile
```

-	Layers:
	-	`sha256:4e5253efa793a47ad023906e74c423698ee4c12378945c0f9c0e5ae26dd44d65`  
		Last Modified: Mon, 08 Sep 2025 21:30:40 GMT  
		Size: 3.2 MB (3167963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff2062d8889075517fd9ed8faddb0ba0ccbc831ec686c79a715bed3598ffdb0`  
		Last Modified: Mon, 08 Sep 2025 21:30:41 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d943e3556e2315f86aa4bfdac76234900b3296fa1d455e3b5334ae8550ca8269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53391919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03be953ab8044d01de451d7d0e667bcaaa2af35df51af02ea955c2bc55fc7f9b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:96b4ca5ee980768194b7b8007765bc50123c81ee67cf0d113b71633ee6be6175`  
		Last Modified: Mon, 08 Sep 2025 22:20:11 GMT  
		Size: 53.4 MB (53391696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219e0df3c85ccea3eee2f0ffac95cca0f7bf35a30dc2e69db0d11ab3d6df4ad1`  
		Last Modified: Mon, 08 Sep 2025 21:56:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dc25d5f21a1356aff5e9687add1bd7fb751a164f99c1c13597f5ff22921aa751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31343abe3b44160c90844bcca257d5f55290708aaa242c0071455b5715f95bcd`

```dockerfile
```

-	Layers:
	-	`sha256:70ec4862f86f394d330688ec3fd0e79e579ceae532b56c36441e11222858d2cc`  
		Last Modified: Mon, 08 Sep 2025 21:30:46 GMT  
		Size: 3.2 MB (3174268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c590c4524f65f1cf5579b6e9c1e96b609e95b98210b9ec5b5ab31202fbec53a0`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:6051ab1d15d0e39fc9c8b7b525340c443c589ed95b9b38070de492db2334d083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b245a475968fe233b91d68da01c28b4592b14b309ca578802ffdfa07e0fcef47`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cb9a52a499db4647b784ad4549ec7a50c9127ce8c522037fd781151ac4a51159`  
		Last Modified: Wed, 13 Aug 2025 01:10:02 GMT  
		Size: 47.8 MB (47764300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdd75b191917817098e283e27553ca30ae87b913559c536e7ff6cb31cf44881`  
		Last Modified: Wed, 13 Aug 2025 08:20:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4feabb968fbcfa6e5a219561c35a0168c18e0e96926573ba00c845ccd37d557d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bba2a6205cf66764af6437b878c21abef3e7827353a3d1cb7ee7a267a2a1638`

```dockerfile
```

-	Layers:
	-	`sha256:7a4410c14a529b6a6e4b7f7611dd991643af017aa9270117bbbb8b2589a94745`  
		Last Modified: Wed, 13 Aug 2025 09:25:05 GMT  
		Size: 3.2 MB (3160814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825fc194efdb876b05dff0d5b4e54072dc7c9e7a7cf3d14a9f0efb85ba523670`  
		Last Modified: Wed, 13 Aug 2025 09:25:06 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:97e42664af374c21e18df89f94852fd66ce683b7805b9cac593415d13d61069e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49583403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f38c84a3a8c8c8d89b8c7af2ba31b49d0de2dc7ebe9851d8301ad7ffd4b817`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2cd29a40290eb73c0f0fb2c946ea3afb7559c33b6f5ca431ef71a23380e9eeeb`  
		Last Modified: Mon, 08 Sep 2025 22:20:17 GMT  
		Size: 49.6 MB (49583182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e99c6cb74e56b55c2f72a17cf443129e59c669d7c4fa1355501e590dea151`  
		Last Modified: Mon, 08 Sep 2025 21:54:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b9771ced832d6793ca5c08ba92e9225b7c0bb492ae7c8ba1073e5a76098e4a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21657fddf5989a8b112105e758803a05bbe38090271dd127140683576294134d`

```dockerfile
```

-	Layers:
	-	`sha256:97713d61d76d74f6e6adeb26427213e6e04feabb1bb6471fdc90fa6e61b8f1c4`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 3.2 MB (3172206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e305fef28cec631c3fb5980acbfd21ad103f054e047c899c7bedc4415d1e13c0`  
		Last Modified: Mon, 08 Sep 2025 21:30:56 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json
