## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:9fce767d2a77a547ef96d6d09c3194b0604cbccce08fd9d8491516af4b118af4
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0ddbcca38daac5243c179bf5aa679ffa8fb81bcab4a9cbfcbcbe4b6a580234d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136903844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2bae2ef96201f71933649262a665ec6505a2c8983952d56cff6e878a1c81c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d3cd41d9b3850add2bffaca253bf035bb4e1a3916cf860f6e525265ef071c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7972758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcfb1578482d7d3085c142ac55a5b4ba1af164e90446460205487f3910c29a6d`

```dockerfile
```

-	Layers:
	-	`sha256:134b898182c71e9e4421b93254768bc363e3c3bf4b237e7670c7aaad6830762c`  
		Last Modified: Tue, 30 Sep 2025 20:24:14 GMT  
		Size: 8.0 MB (7965405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8450f4152255340f41b08b1a4cc3db8a87293802e58cfe82a9504c6b7c3ae4fb`  
		Last Modified: Tue, 30 Sep 2025 20:24:15 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fa3b85e27482443e00b7326f66c3eadf63d9460ebc88244dec4e088098662efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130728960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd766890d6c9b92f44878f3ff37ee85110cb6194295eda2eb35323cc84342af5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f9dd65d850ae18d5d5161e690c6c0b615e72aceac0e3bbc51ed315faf762f0a`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 46.0 MB (46015582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050a4079641da2be39571d354108d87d3709c848f35b60ff42118ae57f90dee2`  
		Last Modified: Tue, 30 Sep 2025 01:01:11 GMT  
		Size: 22.7 MB (22702536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340c17be5ee9d11a6e4c78d0f71ee3806a1aed959aff55f037aceb36923ab6ea`  
		Last Modified: Tue, 30 Sep 2025 02:18:29 GMT  
		Size: 62.0 MB (62010842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fb218b2d4040e08cbd4f5a309e6094618415d4dbe7fdaceedf873854d218b677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df019fec7410cdd0c1a832c9d4b7c1bb1375200041bd82fb43a0f7379c3fbc4`

```dockerfile
```

-	Layers:
	-	`sha256:6a1ca12ecc01d8f12fe9d9bf01466a7b7f2d4004ae464d6adf3d2096bace94ca`  
		Last Modified: Tue, 30 Sep 2025 06:35:01 GMT  
		Size: 8.0 MB (7967263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8445e726350fb59f2f780d2c5f19549deb0ea0fced8d4241b545b76688d3d321`  
		Last Modified: Tue, 30 Sep 2025 06:35:02 GMT  
		Size: 7.4 KB (7416 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3bfbd3e2af4facc9798720ca491fa0addc99a07f3d3e2bcebc43907e09d297b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125779164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969007560b76b4e4ffc86f4dc283d0902e88ef40bf71b8e2f2afafc3d83f3543`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:03e514ef7fa283c62434ceaa5569a1dfd7eb8f0bc5744761a741cccd05a62353`  
		Last Modified: Mon, 29 Sep 2025 23:34:15 GMT  
		Size: 44.2 MB (44195923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0c6a4c275fbc1127f1e13a9f6de6ca4fdc975838d76828750e675f4b1fd24`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 21.9 MB (21930710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c9e67a849318ef85c3217c9988076f862a279a4fa96c042c09b84353bac8b7`  
		Last Modified: Tue, 30 Sep 2025 02:39:14 GMT  
		Size: 59.7 MB (59652531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f0222676659d3759c83525ef97d6420c7d7abfae6209ef0d9766b6669cdeeba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d12917aabffb41992af6a33360dad178a5bc213b2cc3c91ddab86d758f22af`

```dockerfile
```

-	Layers:
	-	`sha256:c76c8ffc07ee680c98ced6a9a650fede9c231d9c915d2a1762fc151f449ffd25`  
		Last Modified: Wed, 01 Oct 2025 19:53:03 GMT  
		Size: 8.0 MB (7966682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f63f1fe1b2704df600b944e93ba7ba594c3c5097cdffd392ecdff454028735`  
		Last Modified: Wed, 01 Oct 2025 19:53:05 GMT  
		Size: 7.4 KB (7417 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e2047bbbe9c327626a8850cc382ba2118a7fe4756e76e394216f2215e1de04e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136324858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a99dd3458a1c9f67390c9c58cc4d28227dfdfbe44465f5fe7faeb4ae2988e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eed32ae6dd9c170187ec78609c601181d0e92a71b0ad1737d9ac56e1a92e3954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb92348e0e353779ba91fad7c9b49773e303b51e2059e120b21fbb776a0112a2`

```dockerfile
```

-	Layers:
	-	`sha256:0237d06da0ea2a173932caa02ef83b16538bd7e0c31e0203a10f162be27d492c`  
		Last Modified: Tue, 30 Sep 2025 12:23:53 GMT  
		Size: 8.0 MB (7971798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f64937a7c0da587fb94c76130bafc7ff29f123d69df6f5f66321f6bc66b402d`  
		Last Modified: Tue, 30 Sep 2025 12:23:53 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:91ab833671ce6acd9ba2d7192d9a2596bc79dbc1ea7c8d61ea5a1abdf78fcc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140560721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72218cb0307dda218eb28240b72e01b53f21b2a05f99d0984d41cee4e76c68c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a8a7ec291d92cb9effbdbbb7bb5864ca1d87b5e149ee45db584ed39cfc4eb`  
		Last Modified: Tue, 30 Sep 2025 00:20:19 GMT  
		Size: 24.9 MB (24860635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963263603b7fae742ca79dc45230eee7f46d0be670e6738f50212dea9f77470b`  
		Last Modified: Tue, 30 Sep 2025 01:18:20 GMT  
		Size: 66.2 MB (66233435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7f39d0aebae19d3bb2656d9d9cd9daf732269f24e56d5d723722b51858b6f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7968895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45585e5bcbf5980803c8d2063f6f85a3553cb43651be63a5f876188e4b2931f`

```dockerfile
```

-	Layers:
	-	`sha256:7443245ab540a15e0de142b95e8526e77be75dd028b6fd578ac6bf7e0f225fe5`  
		Last Modified: Tue, 30 Sep 2025 15:25:24 GMT  
		Size: 8.0 MB (7961564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e63a1907a55461e74a4f52969059053ae28f308086785492461fc360bd3bf2`  
		Last Modified: Tue, 30 Sep 2025 15:25:25 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:248283e99a3bd62e724d88bd5c6a1bc953d12c122e83e1b4c373512cc9c3c1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135681415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f465e4b6f95566f0068ab97659b0ce9a4d8904f067dffc6dc66e09ebf66a5c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7eacf7da1d9ca68e46013f3f56395614b995d68904a39e73d4a5bad90579014f`  
		Last Modified: Mon, 29 Sep 2025 23:33:18 GMT  
		Size: 48.8 MB (48760734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a1eca9595b83f733381d5f5c6ca135b5d5a79fcdb8204a00ace454f493a78`  
		Last Modified: Tue, 30 Sep 2025 16:39:43 GMT  
		Size: 23.6 MB (23611218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ad543e1bb93773e8c6b716a20da76b363bb9d042051784870a3254e450de6`  
		Last Modified: Tue, 30 Sep 2025 20:27:52 GMT  
		Size: 63.3 MB (63309463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2de6c34af8943e4ea4bcdd4db5c0b6f32d12cb447da2379cb3dc6f2023057c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db8a6071019ce1e1a3b61a4ff945cf8335eed62758154dea1725b1632d2bc0a`

```dockerfile
```

-	Layers:
	-	`sha256:8409955d4c268a7d1f140388c85198cbb802bc34877358628a0356860ed58a93`  
		Last Modified: Wed, 01 Oct 2025 19:20:03 GMT  
		Size: 7.2 KB (7186 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:658d22529dc811be8ecc188c27b4d726af6e767a3a8766c95078a612a2bff825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147841226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc37bda87910c51c9bec1b40f0b9f15442087e6688521043e889bc428e6cbfd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f96d9492071bbcb8f94f1c41ed34bb1a985729d6a6ad6f8a6d10f9bd6e3f16`  
		Last Modified: Tue, 30 Sep 2025 02:24:29 GMT  
		Size: 25.7 MB (25668919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559f87b306ba2a8705f64aa230b6840e422b552a6363650f02e37cde768fc14`  
		Last Modified: Tue, 30 Sep 2025 09:20:33 GMT  
		Size: 69.8 MB (69845543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:894a98a48c683aef0892dbbc08248e3fdc25eac796d3c34af7d3a6dedd285645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef9e022b7d3b7c7746f974415c9c8962e07c047732628612d05f920e16cbb10`

```dockerfile
```

-	Layers:
	-	`sha256:26c9ea1acca2e80dabfdd4e205e96ac3ade9c4f7b496e9709d72ff730e776a86`  
		Last Modified: Wed, 01 Oct 2025 22:03:15 GMT  
		Size: 8.0 MB (7973276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a728b2c7a6e1594ce30d1aa40eac86af69bbb1596fdc4a4cbe6097f867b38c2`  
		Last Modified: Wed, 01 Oct 2025 22:03:16 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0b74bcd524846a10d8ff7ecc92b6bf7d8132be85c786fc37200e27d52efea535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134662512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b7cd600b1b2f2d726e4039c638ce79cbe47d973f1d5337830ab5c21705e089`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2365377a8d4ecfdf70b8afc073fddfe487283a41bc28927b47a4757047f66c`  
		Last Modified: Tue, 30 Sep 2025 03:09:03 GMT  
		Size: 24.0 MB (24023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9730cf662a91a14b192c512ec1973efc8f7eabd745b63f8c6c877f23bf0d0`  
		Last Modified: Tue, 30 Sep 2025 09:32:19 GMT  
		Size: 63.5 MB (63501350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18ea58bc2b0599019fb88e002b96c6a103756d7829e7c991f32c89bdc1f18605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43e45cded7d73ebeca960b468d8d9242860ff48a92214d5537f4148473070da`

```dockerfile
```

-	Layers:
	-	`sha256:13e6e57e9ace9f85a38effdb8798e25713b73670179c90c9d51b86380b0c0d7f`  
		Last Modified: Wed, 01 Oct 2025 19:52:43 GMT  
		Size: 8.0 MB (7961718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd6a6a979dbc29f112a610a2e16bcd0c887f20e2dfdf50a5fee28d88bd1f538`  
		Last Modified: Wed, 01 Oct 2025 19:52:44 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json
