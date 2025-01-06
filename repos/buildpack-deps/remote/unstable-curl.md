## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:84e0280e9023fc7bb7da715a025af647b0f57aee089756265ac2e00a9c59f5d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2bb7a5289f4f6968a75dec2675a4869ab1b85f8bfea4efd5dce067e217d84246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73640646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d3400572aec24c2e5f0e96b03cbc855a42e34af47d35febceb381998ccd778`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f5cb15ca6b13e712531ab64cf0ca7c69c2e82cc28e9adaf6b4610737a1ba0734`  
		Last Modified: Tue, 24 Dec 2024 21:32:33 GMT  
		Size: 52.2 MB (52225405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a81d57692e85975a86c41b040ba4d1697f343d6fa8db79612558993ad0d1444`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 21.4 MB (21415241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8fd5fee44c3aebacf36db7da42e9535be45ac61f8d2d58bd3608e9a0c5527a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4040849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13afe1f8664dbb056ea9d8716026ab8f51b0b9539edb47f7774177339c5df17d`

```dockerfile
```

-	Layers:
	-	`sha256:c247980952fbb49fec4627afa8fed86058af85fc9c68d7a606dc0b3fa15d97d8`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 4.0 MB (4034045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250f0a48c5bf6f0781ffbf6ba316f23054e71f081aa24e0468635adab2691251`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9763f030d25d5e67ca1c80f706ba7ec9bef1798b4065a6314d10d28b63f8a8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69079030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a3f1e02c7d1539b0a1366600aabd5d1a6b4335059fa61acdf4536892572941`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc33f333779e1bf21a11cec34fde351758a9648cea4a206cd5ca5e5c267d5ca`  
		Last Modified: Tue, 24 Dec 2024 21:33:52 GMT  
		Size: 48.8 MB (48771903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef48cdc7993c776d6ccec56389e66a4c68ee1ceec1afa89a25ae9e60ac171c2`  
		Last Modified: Wed, 25 Dec 2024 01:31:21 GMT  
		Size: 20.3 MB (20307127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:be7e3c2aaccf0a4624905d35602ac9000826d9b8224ce48ee3c537fd436d50ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436322604a1f72d12d74a7a5f0098258d5062b6c40a46de0c6a786f43ab2b323`

```dockerfile
```

-	Layers:
	-	`sha256:a878c4b5479471f28e6da949ac432bfd5cc695ee412cd99bdabbcb0549cf4bb2`  
		Last Modified: Wed, 25 Dec 2024 01:31:21 GMT  
		Size: 4.0 MB (4036265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdef733c12a31ba40d8a10196bab82a325f0a19c66dc60979fe4aee3ed5cb819`  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d7a98462c8b2665ec5ed80d3719a6b961f7dc27be6a1e73b0d6955e27280adab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66372254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f4c926a645700c6a60e137cbc517064f73cc493dc1f291b9db160493b7bf81`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd381bc5446358c906dd1f7ac3878d03bb1e1267963891069c3e6e2c97919218`  
		Size: 46.8 MB (46763305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d419ccba1fe0df7cd0c879e1f8261dab91d1fe412b8df835212e60f95b90dbb7`  
		Last Modified: Wed, 25 Dec 2024 03:45:03 GMT  
		Size: 19.6 MB (19608949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5b3c6617ddc7dfa5dea4d3466e8399618b939191fffa4e666881163ce473a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4041932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042a5ec05a2dbcecfd32ecd687fa246d4491292091e2d89c797d7af6f643785d`

```dockerfile
```

-	Layers:
	-	`sha256:b6aa0f1914b7a5871c3455f98cc4a855f772f57484729913ba9ea9074a616a84`  
		Last Modified: Wed, 25 Dec 2024 03:45:03 GMT  
		Size: 4.0 MB (4035068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226f2c9463b01100e1886f2b39cd87877b091b38888e03a35733eb5434dca693`  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9e7629661fbcbd4733850b561d9181cef350f723e315d5276bec320c7e827ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73484469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ca2d548d3885d5538ed15fc1134947a41b12ed0198eb482f6579bb06423723`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5111921f4f194856cc1156a3664c32c64df54cbd5ad15f8c94081cb0e3440253`  
		Last Modified: Tue, 24 Dec 2024 21:35:38 GMT  
		Size: 52.4 MB (52432315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20d0977c0428e556b738a4854988cc1f65b6192c33c235195555a4b1c8e5d58`  
		Last Modified: Wed, 25 Dec 2024 01:50:20 GMT  
		Size: 21.1 MB (21052154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1bebb0b1739565b1ce74b7170e0636093ee6f1c732e3fe16e8f85ab674848ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b41656f24abdb96514dc03da66c76aa94440358e0ee62db2ce92b6c13759af`

```dockerfile
```

-	Layers:
	-	`sha256:7340f1623eca87bfb388b83d4f8ffbd41ad2763512bceda6a43583f9911cdef2`  
		Last Modified: Wed, 25 Dec 2024 01:50:20 GMT  
		Size: 4.0 MB (4037021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4ed2e300039242f9e5661fb9c66b029dc219411e411ce23158327bf7d8c99b`  
		Last Modified: Wed, 25 Dec 2024 01:50:19 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a7a34e322e0f00519388e01ed4c31b237aca6699a673c30965af5269d0d02e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75553896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59f2c074b50c7fe3061ab04381a5380b4eac2543ea6b0094fe81f84b2d4668d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:314d11be1a34669d77f82c7dd25250c0aca0d10b528a45fcc768df2c73d1a359`  
		Last Modified: Tue, 24 Dec 2024 21:32:39 GMT  
		Size: 53.0 MB (53038809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794215da1008afee770eb56416f34dd01e9c2b54727b8c520b5cbb72c9a0c70e`  
		Last Modified: Tue, 24 Dec 2024 22:14:45 GMT  
		Size: 22.5 MB (22515087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a86ba4c1dba0ce0ecaace9f894517c63edcb2dbdb29b2d1f20e93fd54157920f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7cb144549cc9a3a00cd7aa3d846a1f1a52b52e3b3db9960b845f04588d2107`

```dockerfile
```

-	Layers:
	-	`sha256:f504663ead259590b966da71eb308acf5e247519cf93cd56ad3572a4404f90d0`  
		Last Modified: Tue, 24 Dec 2024 22:14:45 GMT  
		Size: 4.0 MB (4029800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:794b77820ba371b7805594f4340469aaba072c843284ddb0c31d61ad57609a40`  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:50e70f2127c9f6e52940262154905830dffd9631db8473b38d0585a06e999163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73512165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e647cc1399184363c56fcbb5caba756f2172cad8a5a00c2cef5ee01e7359bc4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2225e4bf9a501ecd52da3f4301136a4a3ac3273d704acaffdf95ff67153847e7`  
		Last Modified: Tue, 24 Dec 2024 21:33:59 GMT  
		Size: 51.8 MB (51771333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8315cddf1f38d3ec912dd995fc72b7c70105918274b7bd71b5f66a9e8789a52c`  
		Last Modified: Wed, 25 Dec 2024 11:47:53 GMT  
		Size: 21.7 MB (21740832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5cc60a636a3bb6bef78af7f5c6312f9142ffa4b2ce3bac63639b71a25062fe38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41d5aa923e4bc77a98b55948f98024c6662e9c4aff1c2c79316455aa4959ecc`

```dockerfile
```

-	Layers:
	-	`sha256:a04c57573b2f348060f05c85d208a1e09720aff18837ff96060774daef4f3f0a`  
		Last Modified: Wed, 25 Dec 2024 11:47:50 GMT  
		Size: 6.6 KB (6636 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:261eccb1fbf322c8560a2aea5ef88fd25b2c71baba73ead7998b6b08c362bcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78852320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17c05ef036677d2e677df950da1ddc040d6b08432e31b7d809b6f619539ba3d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8080cf22cba920897d6f69f8cd18b32c615d4fe71eec9143a4055b490742fcea`  
		Last Modified: Wed, 25 Dec 2024 00:33:18 GMT  
		Size: 56.0 MB (56045011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec24b97fe03e846eeb6353a5a5009e4324e4fb188c11fce7c104a3a8159b2eed`  
		Size: 22.8 MB (22807309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c854f9dbc0b75ad34548c282a02dd53497d2ee2d2162e402f51c120cd1f9a1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4044145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65bed8316eb72fe49f159acb639dbc6372c90665d165f45290fcbfe23588450`

```dockerfile
```

-	Layers:
	-	`sha256:2945471a977bc79fc65ab1b0291642d646fea7a53ebf73f9ba48a602721089d6`  
		Last Modified: Wed, 25 Dec 2024 06:15:10 GMT  
		Size: 4.0 MB (4037309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633e76ccbc3b1c75a9365f242d137f91d83d6bdd76c2e2ae6d907c7605e9f04d`  
		Last Modified: Wed, 25 Dec 2024 06:15:10 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:50021e11eee76dba7ac182e699db82016047b4bfb03614b607e8f10dcf7f56a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71541258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd3d28d52f8c78f85479acfb52556916a6e52200a534c191dc24122d5dda25`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34dc7eee421e2547a72cc18fd960cb61e4cc000ae2301ebea5c1db40e2f928c9`  
		Last Modified: Tue, 24 Dec 2024 21:35:00 GMT  
		Size: 50.7 MB (50711803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b3be9202d049cfd8fab2840745aba862531c266ca24caab8785a1201a2bb14`  
		Last Modified: Tue, 24 Dec 2024 22:26:29 GMT  
		Size: 20.8 MB (20829455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f53b2ac9fed4061453562312e21afd15faad1577fb53f0b0f2cfb205f6a061f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4033707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae945f46e3609de2dbefeb26f1a614dc9d20e61bc0b77b7045f2cc3d12d0cc5`

```dockerfile
```

-	Layers:
	-	`sha256:6bca95a5f4bd3c228815e0bd31fe5ff166763bd835d40040cef458ae93f390dc`  
		Last Modified: Tue, 24 Dec 2024 22:26:27 GMT  
		Size: 4.0 MB (4026874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de7857568615e172daa16b49de08a8ce618e0608088db6eeb7400677eff33a0`  
		Last Modified: Tue, 24 Dec 2024 22:26:26 GMT  
		Size: 6.8 KB (6833 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9116da4b07183d0de0215b2ec7dbeca346cde1b6a0bd55bb08537ba999a4d772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74791177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f000c4167e3ec307c30efc0d01a500498961302f05f3f6cedc7de3c26f5b12fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d2cec60b297953cc4fd2d941f10377b6dad5bfe41703a7cd8819244b88d9c21`  
		Last Modified: Tue, 24 Dec 2024 21:46:45 GMT  
		Size: 52.2 MB (52169916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a975a9a4c83047fb6ec13cd27d1e9c9a446b78d685e928ba2f4297e75463ff9`  
		Last Modified: Wed, 25 Dec 2024 00:17:26 GMT  
		Size: 22.6 MB (22621261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f8e5119c4285a6bbd487c652207a52aed0fd5cdd0a1717a6e8ca6cc8e2b423f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4041773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca19918790ca784fd351eb71933f835e517f2162cf11c8e394fd204dfb5d3af`

```dockerfile
```

-	Layers:
	-	`sha256:19378e35c4d3a91b22289eeb0137f32bc07a7f7e8109a6bfebea289cd7d59cb2`  
		Last Modified: Wed, 25 Dec 2024 00:17:26 GMT  
		Size: 4.0 MB (4034969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddabea051d8174cc32d4fb86261fd2183aa95a5398db760f3cca927ae41a970a`  
		Last Modified: Wed, 25 Dec 2024 00:17:25 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
