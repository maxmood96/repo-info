## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:11a793d9e77a894b967f79bfd175cb5f3ba1267d51c873a5b25065ae82c3ef8f
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

### `buildpack-deps:bookworm-scm` - linux; amd64

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8df11df6854c43b861bdfa36cb2124117264827bedddd880dcc1e92fb7ea081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125779903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f3dae968e315a8a940efa8f741566d46e056fcca1d3b180693179fb32edc82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8fb006981127731180a5d548f700fd609cacd7e365cb66fbcaf2fd1e979c`  
		Last Modified: Tue, 09 Sep 2025 06:17:59 GMT  
		Size: 59.7 MB (59652826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f6ca0e8e4f61bd9478c1cc65f638d43bef03eff1d16e4ccf4a2bab726670495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a925cd8c53dbd4dece85c6c40bbbd20d6d5f7721d755cd594fbd41fe3f772`

```dockerfile
```

-	Layers:
	-	`sha256:afcc71167e78b9a200f06322f2d52a9850d9f18e22c82d38ecbff1ed946442ba`  
		Last Modified: Tue, 09 Sep 2025 04:20:10 GMT  
		Size: 8.0 MB (7966682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a64743ce31fc24faf09fa2c47002f9b62a164073e56b2254f9706f990e3901f`  
		Last Modified: Tue, 09 Sep 2025 04:20:11 GMT  
		Size: 7.4 KB (7417 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; 386

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5f94680e0b6fb7fc65f589371d3b84fceab4f2e5f9990c19cd35c903c661ec57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135681547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c7182998a7dff66a3de77a00c438d1a74c842a351a056e091c649cafe598ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:32b0a76df497911c1adc85f7748d78b916d66733f6d0c87cdc6e9eb06317a625`  
		Last Modified: Mon, 08 Sep 2025 21:14:25 GMT  
		Size: 48.8 MB (48760780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4b1410ff953e9baafd271cda9e27ee11dab33c7404024b5d7f0a941e7606c4`  
		Last Modified: Tue, 09 Sep 2025 04:22:26 GMT  
		Size: 23.6 MB (23611387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee49a4f2d47eca9eb39dcaf1cce76f6da099edc10cb571b790f8588eb5731614`  
		Last Modified: Tue, 09 Sep 2025 17:57:06 GMT  
		Size: 63.3 MB (63309380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ad57b1481c360eed5655c88df392b696ec900e12dc5bfe7eeea6e7e6e99e495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b63a82004a5eec4723104b29f0c6b835d119dab8020b5beae345012ce35a03`

```dockerfile
```

-	Layers:
	-	`sha256:c0e12730d6d099b7022e32b369bcbcec9adfdcb84421e676e74ddbc6deec4c1b`  
		Last Modified: Tue, 09 Sep 2025 19:20:03 GMT  
		Size: 7.2 KB (7186 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:198e72c635c3ad2057320139b242a81fc92e863e88ffe0f18e930b4429cb06a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147841602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6619bcf1600600cfbf8eced4472a18ec22b16491ecf95edd52791c5d6338b6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b92467bcafecf194d3c4efbee466dcb9b2010a0899f7d2b928f9afed69de0`  
		Last Modified: Tue, 09 Sep 2025 04:47:21 GMT  
		Size: 25.7 MB (25668980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aad37d5c4461745e898b391fa21157366a7f13cf28ff4bbb1e1434d87664d3`  
		Last Modified: Tue, 09 Sep 2025 15:23:55 GMT  
		Size: 69.8 MB (69845800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:09de360469cd8f38acc5bd95adc00784a03a9542e65aa566bab71a1139c74a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d680afe4f070afe53f44db754a1f97544a512b99d9dff47d169cb3fa8e8b2af`

```dockerfile
```

-	Layers:
	-	`sha256:0cc56d8cbccc8a1195ab67e65f765a79f70834ba8ef9a2ee24e4655c54dd9874`  
		Last Modified: Tue, 09 Sep 2025 16:20:01 GMT  
		Size: 8.0 MB (7973276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a7b65758a8ab85ee0739746b0b90bb52a2b75c9daa00d0a8947efe58b323c9`  
		Last Modified: Tue, 09 Sep 2025 16:20:03 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cb3c35881b690b32e9fb6942c8a09f288e6716795e0d3784e6afcd910cbd3362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134663246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f480478cb8e4b8e4209f19f6835945dd6103118dd4dcc4fc7ecf50e17e658d3a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f0c679ec7b70d7fa5065a6e28276437547a7d43502b4e016c2e85aed8c84c`  
		Last Modified: Tue, 09 Sep 2025 01:20:52 GMT  
		Size: 24.0 MB (24023865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed122f74eb7bf77b1109cb95e13be357040ccb22119f5f02e566a491bcc45e`  
		Last Modified: Tue, 09 Sep 2025 17:52:15 GMT  
		Size: 63.5 MB (63501842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:32ff9bf554c040979e2afa91d58cc4c3854ea450a4cfa52bd51b53f08cdc5acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23dd1a3eedb11af9378068c4ef88a439e1a3b2f0ef87aabda169e843b3d9bbe5`

```dockerfile
```

-	Layers:
	-	`sha256:b256ea3483c3a625a393899dc865f12fe725efde756711279f1a78c923cce6db`  
		Last Modified: Tue, 09 Sep 2025 19:20:18 GMT  
		Size: 8.0 MB (7961718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c538e12c004def167276809f3893f3e8275dafa80709a5af267195b53c0799`  
		Last Modified: Tue, 09 Sep 2025 19:20:19 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json
