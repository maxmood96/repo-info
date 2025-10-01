## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:ce6e7a3626456279330f386b5eb218c85cfea4f8122906dfc70685c079a0473d
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

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7e93862223747cc5394f6eb431714def5e3f387d0ab679dcc30b9d4651943e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142684385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fed493eede9d76a665504661cce3aafa0cd68c9c24a703adc1ad063d90396eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbf6823a4c93adc4b9b9e3856fef7fb964927ed82520fd5adaee3839de9f50a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3789f0b88a481a2e6c4ffee3328cd7f2e08c9289d82b03fdc1884110efd91353`

```dockerfile
```

-	Layers:
	-	`sha256:4341ee45c035c43a7a31e33bd90135e73670cafcd854cbc66a47fd3233d630dd`  
		Last Modified: Tue, 30 Sep 2025 20:48:18 GMT  
		Size: 7.8 MB (7766996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3fd5106d8b45aebef1e93f2fff9715d089ed2392665e1e8758b2b89c1aa0dc`  
		Last Modified: Tue, 30 Sep 2025 20:48:19 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9e27ace0d1de193c5e0d1e2977b5952729741d286b1b4f238c1b5f977c6f75f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137107507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff501edc3e7b888abce2fb5bf630e8b4b2e3a278cca1adf5b2c1745d5c032ea1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0096434708f67385cef0fbdd93979f2d8849a82842e1217f692977f3e6600333`  
		Last Modified: Mon, 29 Sep 2025 23:34:22 GMT  
		Size: 47.4 MB (47448480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465ab5ce2f6d84d807e4534e3dcd0b62e1a1f4c158895b4c7b3539c651a1fd9`  
		Last Modified: Tue, 30 Sep 2025 01:01:28 GMT  
		Size: 24.3 MB (24341544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cab31d748b7b8f9f94774a6883d028265fd21b230de80c9e3380a4eb4afc67`  
		Last Modified: Tue, 30 Sep 2025 02:18:18 GMT  
		Size: 65.3 MB (65317483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a822ad2ce8bd49b23e2142e394a0f367f71a04774ea40f4cc768c9a85de6bb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d72f12a5265ff68f0745b241efefe27d8e16f6b08dec1379bb100a01ac7afa`

```dockerfile
```

-	Layers:
	-	`sha256:9076055fc3abfe6bf91ffc9476e90962d571d3a10e2f756fda46aea1db7fcd8b`  
		Last Modified: Tue, 30 Sep 2025 06:37:13 GMT  
		Size: 7.8 MB (7768034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204f0d267698b0e422eb9016cc4c337bde9a36250a2f0bd900fb8aa68ee6b52e`  
		Last Modified: Tue, 30 Sep 2025 06:37:14 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5675190ed78c6432984b71c40aefda17d5b0e8b959d115b7c68392687a169616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132045349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4d83255cfec2487ed537736edf4b5a4efdba9391f38fa7739b43e17c6d2806`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:395f9ad3c9d37c6ea60897f33e8b189e9cd41fba6c60ab63882fd95de8ebb9f2`  
		Last Modified: Mon, 08 Sep 2025 21:15:43 GMT  
		Size: 45.7 MB (45711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87266d99f84095bec303de1733ad218d485653dfb6da729b7a066c18810645f9`  
		Last Modified: Tue, 09 Sep 2025 00:02:54 GMT  
		Size: 23.6 MB (23614030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0847685b749ce0208c0ad2a407e89f30279b1c8515c5c33f13a9c9b4c5e3da02`  
		Last Modified: Tue, 09 Sep 2025 06:20:22 GMT  
		Size: 62.7 MB (62719599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:12c013865ebe19ff6dfcaa245b08f41f0897ae095b6bc335eda54a7e3ccc7f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acfa66e3ddb198ae58ce5d167c4ff9068503d4afde371d86a2aa66a322f95ec`

```dockerfile
```

-	Layers:
	-	`sha256:31c0221678b6550b7e669e701a9e25ea573921ef6b51317a02727b473b58d662`  
		Last Modified: Tue, 09 Sep 2025 04:21:28 GMT  
		Size: 7.8 MB (7767503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09df06308ba7572e05c80386a19c08ed731866804cbf4792cd82f8f13d6f901c`  
		Last Modified: Tue, 09 Sep 2025 04:21:29 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0190f69593fd4f12c3355e4a54c2e2add6bc7dfa57f0bac1bb142542b0970a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142248042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49102b8007fbd8f0ea5953bc6649ab02c081a42aed19138e1af8b9fdf464dcd5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c9631087ef516f060328537d417f223e1f264c968e39186895696e78090b7`  
		Last Modified: Tue, 30 Sep 2025 01:20:15 GMT  
		Size: 67.6 MB (67582977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd1e24cfa7af43aea04b01afcf8d3079ea46a16d66b640257f4f15967dd036a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239de39a67ede0e016545d90fcab5af340671e442d33a9496f74af4dad721a08`

```dockerfile
```

-	Layers:
	-	`sha256:8098fb79c28dee28decbb7012dfe31d45d83bcade4dff4e5cd5b1f52016a716a`  
		Last Modified: Tue, 30 Sep 2025 11:48:09 GMT  
		Size: 7.8 MB (7774671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477514c19a8ba7b433c8952a625aba0c53fb98a673a0dc6f9a9b0236c466b2bd`  
		Last Modified: Tue, 30 Sep 2025 11:48:10 GMT  
		Size: 7.7 KB (7712 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f22199875003e99268f914d659e35ba87a9a901da57a80f5168278f6937a2e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147369373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad10eb619004c7af6df9553127320768a2a4c0bd9712e0e28c3dd69f9f8a67f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e5d861644e3a43dbea9917a86fd0d6ccf184bc7514ee58118ffa521ac4bc61`  
		Last Modified: Tue, 30 Sep 2025 00:21:14 GMT  
		Size: 26.8 MB (26774670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acddf1ffebf58f05179a0e8a785ab62df40c7d1c75ee543282d404ca07d3ffec`  
		Last Modified: Tue, 30 Sep 2025 01:21:21 GMT  
		Size: 69.8 MB (69794474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e12a6306ef9b9d6e4f7b18923ee6148171e26586696e36388745b084f6df833b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1a19ff1998b29ecc65f7f5b296dfb324f2b87478f360ffda24ebe5ff08a886`

```dockerfile
```

-	Layers:
	-	`sha256:94bc44f01cfdc0521448addbd13db72f015b0482ccff267919a84b8f1eead5a3`  
		Last Modified: Tue, 30 Sep 2025 15:25:35 GMT  
		Size: 7.8 MB (7763131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f068faf754ff36d1d3a7b9bc3c719a1046eeaf5434234b227d9f9b4042480a`  
		Last Modified: Tue, 30 Sep 2025 15:25:36 GMT  
		Size: 7.6 KB (7593 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:389c2ad4368f4cb543d27a8c30b8815cd568f87073bab75e668205828c66ef8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153131932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf6f961f88562c2f85fa3f9dee86d88f4135a524dd278e0fdc74d730661f390`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bf3914a916f37a54163b2eb02b685f6e0d654680e02a5e51b78387e81e4077`  
		Last Modified: Tue, 09 Sep 2025 06:02:47 GMT  
		Size: 27.0 MB (26993871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31355a04af67dd51f580585ba523dfd2b5ad7d91e873cb7213748a572df48bb6`  
		Last Modified: Tue, 09 Sep 2025 15:30:51 GMT  
		Size: 73.0 MB (73033628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2dcac6020136f5ce440bd562972c327c1f85f67ffaf33dcb6dce8b600f90f724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e865f3f3d60d1c52b9a29471308dd60a12ff51e2c1d39d4e3d30e64253bbfee`

```dockerfile
```

-	Layers:
	-	`sha256:6f79db21df52e34c779eb13dab56c2274510b92b2f08f14555abe62d61a5df7a`  
		Last Modified: Tue, 09 Sep 2025 16:20:44 GMT  
		Size: 7.8 MB (7774119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e188cdb2d48bbf77c2783c837a72e2602ff34e7a6be0141327f3ddbbac94c2f`  
		Last Modified: Tue, 09 Sep 2025 16:20:45 GMT  
		Size: 7.7 KB (7658 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:58dc9789d8612eaeb629de974ece6cd6804cb0a2682924862def12acdbdf509a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139378598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1ab58ebab5a608b8e665d5ee9045e2abfbfe300b3ed83b360f8aea8b0e5910`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1afb27b72dabce7ba373ba8319bd1ccd2205d7724f23909527bd3da7476b1`  
		Last Modified: Thu, 11 Sep 2025 01:43:59 GMT  
		Size: 25.0 MB (24952790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32856986223852ec3f854d1a7c152bc97555c3c9e06114ce074d65dc96a8dee`  
		Last Modified: Fri, 12 Sep 2025 02:24:28 GMT  
		Size: 66.7 MB (66660361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:055ffd23a4f5d87889afe72d0eb146e0bd5a14cb39f1a25136514c2940b9c459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50a7e0363e6e0c10fa635218089bd851e069a76def2cd7ee2776e5864a90458`

```dockerfile
```

-	Layers:
	-	`sha256:b789e202b4b1cae9f39b5de78d70bd977924cf935d6ceca31859eb1fa1a9d801`  
		Last Modified: Fri, 12 Sep 2025 04:20:40 GMT  
		Size: 7.8 MB (7756832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe90f436c3bbb0503aac0134fd0c899d90d80f9740e71ad7fbe0d439b96cca48`  
		Last Modified: Fri, 12 Sep 2025 04:20:41 GMT  
		Size: 7.7 KB (7658 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e8b964ae2c4798c15f6bc2078a1d4e5d4fb428d1f61cb3be5ce9e171361332bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144762726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c78b4bf9bb0a775a91e7580f77154676946c4d642338baa3f2bc46f5345224`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775d8e7868b319a235eef909d5a12163c48c579e84d18d78ed794653cb126a0`  
		Last Modified: Tue, 09 Sep 2025 06:02:49 GMT  
		Size: 26.8 MB (26780367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76c2286bf1bfe1b0d2250435d28c0af55c645ac84ddeac003b9da9b68c9c87`  
		Last Modified: Tue, 09 Sep 2025 12:08:32 GMT  
		Size: 68.6 MB (68636032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ec7d152d60c81cc963542e18963951b5c62eb336b5593b3214b44d3fe9fdb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35a968e5da833f05a2afaff67c2da84878f8bf854da6f775dd89c73c84fa985`

```dockerfile
```

-	Layers:
	-	`sha256:5e27e07c126ce165959b6f495d56fc5f76dc0f58cf86bdfe9dd23f69a09e9ec8`  
		Last Modified: Tue, 09 Sep 2025 13:20:39 GMT  
		Size: 7.8 MB (7767909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c72852c08ab1638e1529a1ee76eddcf6d002971a508821b4bd26f6ceb274bf`  
		Last Modified: Tue, 09 Sep 2025 13:20:40 GMT  
		Size: 7.6 KB (7619 bytes)  
		MIME: application/vnd.in-toto+json
