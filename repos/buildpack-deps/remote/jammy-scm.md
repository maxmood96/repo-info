## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:979a81e64e5dab0ff9d7877ee6aaefd11b11aedae32646a00631afa3bc68060b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8fccaadfc9efa29dd68747c23b7b2a388aa0acf1b952e1107c844d8d7bda1199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76129975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457fbda0cdb04df37577383e9a9bec1d7a1bf4185974c5f16a55b971f44d3029`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a882c2cc2b3487f954b121776f38449e97c30ef32043eb9907c13c525178e473`  
		Last Modified: Thu, 02 Oct 2025 04:52:17 GMT  
		Size: 7.1 MB (7106046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7eae3ce667e15aacdd991f13045b9040930a5ccb6f865a903a8cd4b8e17a3a`  
		Last Modified: Thu, 02 Oct 2025 08:26:19 GMT  
		Size: 39.5 MB (39487111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f50f8dbdfe49705e1f7a6abb78d87bada87e2c3811bc5dddc529270001d80626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f66d7a4665be1dcecc535543f8943853bc8539a13a91fac6e9756d6d4a5624`

```dockerfile
```

-	Layers:
	-	`sha256:4e23a64da0161e66be020a8c2957102d02f6591f4e52111e8376f4f1ad9589ba`  
		Last Modified: Thu, 02 Oct 2025 10:19:20 GMT  
		Size: 5.8 MB (5812698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37947529f60beb55b659a54985626629272e720e06819b8a1acfcd2801dfc7f`  
		Last Modified: Thu, 02 Oct 2025 10:19:21 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3f1cc6e581c34cc874cab705a373cd13e6cf6406764523f77c4a4ad76311dc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75904916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e0b2c94a1c5f5a4311ec74dfcebd1d65dc1040acb3595ad71059948dfffc58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7939f961de8cf091ed251aa1d8e432c16ec7506130ed39a1db4028efdad8fbfe in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33392950d914bf1e16e980fc0bbcec6367a2d2b8ecbd726dc5fc65b4c96ce79f`  
		Last Modified: Wed, 01 Oct 2025 18:17:15 GMT  
		Size: 26.6 MB (26643435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9171b5af741a0ace05e08730bfd3e3d15b256638bd578879f8bec957a53865fb`  
		Last Modified: Thu, 02 Oct 2025 01:11:04 GMT  
		Size: 7.0 MB (7009648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad66e157af2e652af3caa8bd7ad08a7179d484f1b6882961c023ec58b25c05`  
		Last Modified: Thu, 02 Oct 2025 02:15:10 GMT  
		Size: 42.3 MB (42251833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a5cdba9c7597b9f9cea28730d6394ee323006493ef2894b0a2ecb8f9077e45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29af769892639733d21b40cbbb16e854bb4f1a78df8923b82363c2c535958589`

```dockerfile
```

-	Layers:
	-	`sha256:e09a84db7a849819f8af8d8e64874a910bfedfa28a7fe17a74dd90153a00fbc2`  
		Last Modified: Thu, 02 Oct 2025 04:19:49 GMT  
		Size: 5.8 MB (5813978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a45bbf037fc4872259915c020062e207f686ba29fd12170f7ea2f73cdead484`  
		Last Modified: Thu, 02 Oct 2025 04:19:50 GMT  
		Size: 7.4 KB (7387 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:84a1620a334fbb2de619997422e99abb4d31dc64f5e8b158273302569d07af78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73817717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6768513c81e369faaa9094cf09f73943a1fc4094cbdfc3ec67150585f3772e34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fbec883712e8b92ee5a8fb96accd816f1bd25c1cb91370bc6a156f3923503`  
		Last Modified: Thu, 02 Oct 2025 01:11:19 GMT  
		Size: 7.1 MB (7052114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0761247749305bde9fb9bf7bfca381206a20dfde11549ca1ba13996d4f60209`  
		Last Modified: Thu, 02 Oct 2025 02:14:20 GMT  
		Size: 39.4 MB (39382496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:872f592fcfd1152989bc6383983e002b209c27475b538dab78f32beb0453e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7c853dcd17fa77ddd05ff5103ebcb93c085881728877b4de2af64dc532a252`

```dockerfile
```

-	Layers:
	-	`sha256:6b387d85e53d0c3ca58de3db9fe8d8886af71127054edd83c3355a9d6b0d8ca2`  
		Last Modified: Thu, 02 Oct 2025 04:19:55 GMT  
		Size: 5.8 MB (5819092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860fcaa6f50eb6de4bb4e8a44243f7bb5dbcb96514aca7fc2d19c9fcba20b5e2`  
		Last Modified: Thu, 02 Oct 2025 04:19:56 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d9acffdde6889d6d3004d5df0625d1eca048fad7d261b0450fa1e9eb512b1ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86391221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb79523ff910aafa4cb87e1a690bcd02d915f46aa03eaea91520c85295d4be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85815504a72bcb6a041dc9c6719b247fec1e21041f41b6f9131d482de517db9`  
		Last Modified: Thu, 02 Oct 2025 01:11:05 GMT  
		Size: 8.2 MB (8184433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5327de806c5a472e2179a5a497c8fd14d1352f950e28cee0d7d2c2cba9df9dca`  
		Last Modified: Thu, 02 Oct 2025 04:59:10 GMT  
		Size: 43.8 MB (43759999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:145e5cefb827fac8303420479de803012c2a3ee939e5ba39ad3694f5075476de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb53b30de84bac1d7fd1568ade34e3bb178ef4e8bcb9bb81750a108d1e5b8433`

```dockerfile
```

-	Layers:
	-	`sha256:4fecad7f23bf83988c1ab6ac35ae1eee2f3ba74e3ba50ea3824dc04b55a8bf59`  
		Last Modified: Thu, 02 Oct 2025 07:19:38 GMT  
		Size: 5.8 MB (5820542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e16b8e88c1da5bd4d79bb39ae06468a866ce7294faf625fc6ebe66afb92344`  
		Last Modified: Thu, 02 Oct 2025 07:19:39 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d92b23c701f25586bf4a09e726df2141e75f499bcdc008d5f697f6bacce2c5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76467388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ff7b6b572000c09572ff817458c31f1de72c680632f0404fa8488fa92b887b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:49eb482a54d27b9c245629c57f816d00d3f70ec4464924555d739fc1cf52432c in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b665bdbb2ecbdbd42e0b5941fb0e987604652880a86a9c6e39dc865d4608cf7c`  
		Last Modified: Thu, 02 Oct 2025 23:19:28 GMT  
		Size: 27.0 MB (27042913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893aa869679582303e282b01c1bd41bcfd462f1e48f9682a21f667992b24fdd1`  
		Last Modified: Fri, 03 Oct 2025 17:42:19 GMT  
		Size: 7.1 MB (7118496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32593fe2ff620017b7d57a17f20b61654226d9355f1aeb99f248cdf3f45408f`  
		Last Modified: Sat, 04 Oct 2025 10:46:17 GMT  
		Size: 42.3 MB (42305979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0465382bdb7be34907dfdd70b19b687494c38c9125cb770dbb6bc35e4b91753a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b9a30f774e5f6b3172853ea0f43c7ea8c42aa7459d6681282ec454408ebb1e`

```dockerfile
```

-	Layers:
	-	`sha256:7b50b475ff4071835439afc4e69934cb0b45cda73c4ed51c0f325d05e19fbca9`  
		Last Modified: Sat, 04 Oct 2025 13:19:35 GMT  
		Size: 5.8 MB (5803084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90046042fa38d63c62f4c88eec61df669978a50fced9122755ebf1147fa55e2b`  
		Last Modified: Sat, 04 Oct 2025 13:19:36 GMT  
		Size: 7.4 KB (7355 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cb1dd6c16e527015d3eada940a47ef3b912f0afa71e9e788859d810daa3ed12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74441299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0218f861b0f0a4ebf561fab8b72bf29434d8b70dcd79b05d573614916cf5cf45`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c17dd0c731fba631ccfc3aeb70e205e57d15badc6b26edc465d60bb61dd3c1e`  
		Last Modified: Thu, 02 Oct 2025 01:11:00 GMT  
		Size: 7.0 MB (7018299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7a6b2fe5670a7425cebb606528db0b3bc0b822a68bc9de4e677f95e0e8f766`  
		Last Modified: Thu, 02 Oct 2025 02:39:57 GMT  
		Size: 39.4 MB (39419587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ceceadf25f3c01eabc20d628d0022353453e1f83a38083d5020eece77c81e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005660f332aa0ef882856316ae2d9ade4212b9a9861b469d49cc7155c76649fc`

```dockerfile
```

-	Layers:
	-	`sha256:c23a36a111813823d7296dc875fd20a422b9a750f82516e64d39b5f556617df4`  
		Last Modified: Thu, 02 Oct 2025 04:20:11 GMT  
		Size: 5.8 MB (5813617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0d3cb54c89cd7a4c2fe215cc9d4d84e299629fc7706f54616edd3f27165fbe4`  
		Last Modified: Thu, 02 Oct 2025 04:20:12 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json
