## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:b8fbfa0ca3bb2a2252d0dc5ae74fcc20400f90261c6a94ce06ce10262c83b5db
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d295ae1c869f95a9f9e9061a82e02f11b4dfac2f37c0dffab94812804855f163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74919245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c23e19bc0c99d184f5937b6ee665851244b6e1cf003a964820a5e86d996c7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6670ac6a207ed43b14d9d5a61c9bacc87aa29186a0d79da3c2248e5a8aacec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ffc037b978e483455165db31e5e264a741818c44eb7e29b4bd2824a88821f3`

```dockerfile
```

-	Layers:
	-	`sha256:2b57adf0f4c82e987050883ef13d96d1fce3bd90bccae51c5244e0e3b75969e8`  
		Last Modified: Mon, 16 Mar 2026 22:38:24 GMT  
		Size: 4.1 MB (4119951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d35fd21bd4267eb25532b8a0ead8c72e9a82c40ac53c42a005edae5d7bac7fd`  
		Last Modified: Mon, 16 Mar 2026 22:38:24 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; arm variant v7

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:056fa0a98cb8f5808c95eeb4967dbc50036cafe75ce2875b3325b2c9b80f73e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74688681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3e5250f8046bc00960d54b931383af2c84ab5f75f2a9585568c88e81e6226d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cef1888616375ed979a8323d00f43f5bcd6fdf4507d0bd2635bc19abe74d505b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630f8811187fdea307ec9021f9b2da58f8e523c5c63fde9dead40c16e05704f4`

```dockerfile
```

-	Layers:
	-	`sha256:1cc5b60f2be86a956d5caaa4af14846e911999e0d38bc6540885c7fc911f4a6f`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 4.1 MB (4121493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93293e9c3241943e492b24138bee6be2dc03cf23c2aab4a419ef4540c7877fa`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a8a7fa0b52917b08fde8ffdbf1cc014a920525ea68c736a435a62dfe6a0db50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77602331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2885a54e159286955fe6b3a4cefba2ed9821b81b8f08ee1785de58c0b2565e9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db2aaf35fd2a2c9adf573b12a548dde1e9e6733b0a9d987c465038a81dcb2`  
		Last Modified: Mon, 16 Mar 2026 22:44:31 GMT  
		Size: 26.8 MB (26783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd4b4dadc2476c05b74fd72c6fd200da823ec7d541e55cffefcb77d4828ce1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eb6301ced305c8a42d13af5d792660ddad1b1d28e79e314a4e8a56430710c1`

```dockerfile
```

-	Layers:
	-	`sha256:e95f0a3ecbbf8074650b996616a71c43bd847233ea7d7747d77d45aad7cf5b85`  
		Last Modified: Mon, 16 Mar 2026 22:44:30 GMT  
		Size: 4.1 MB (4117058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f07fe89164916fbec34d335ec8e736fd5f9ce6c3d5e5b12842cf337064ecfde`  
		Last Modified: Mon, 16 Mar 2026 22:44:30 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:be3b8f5f44f728c1a7b21f1bfa95833d6c731828a1715d4eba2bc713b3effff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80116636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e811cd2a801e874bb0127a6332410085d860882b1a34da2dba050632bf2eb330`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88c878e5079331d2b0e1bf13313604e6e446232728ee7b159499795ff9def2`  
		Last Modified: Tue, 24 Feb 2026 21:23:39 GMT  
		Size: 27.0 MB (27004375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ab68f78f76562c6ea00898031359c9c66c8eb81937598fda8caaf0a82440b24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346bc971f7669a467d0e237585a434f2e7b4789a86bf46477b0cb11eb6b5afa3`

```dockerfile
```

-	Layers:
	-	`sha256:64749f2adb33fca0ecdc5e0bebd9f4eb18b8aecf90337d23bd933fcf243afc61`  
		Last Modified: Tue, 24 Feb 2026 21:23:38 GMT  
		Size: 4.1 MB (4123761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b121ec9626fa7ade0c2146b565c040b84e20a50a3b91d7b959b896a3942f1055`  
		Last Modified: Tue, 24 Feb 2026 21:23:38 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d0efa23bf84eee669361a69920e342bfd8c7ab2217630f281a4391755e29f629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72728755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0a2ff869eee6a2cbda607c640f0b109e7333123d4baf2e4805ee3376f917de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c3a1cec8ab5f3346656c92bb6a04391222dacf945336ca2f360cb9afa1d32`  
		Last Modified: Thu, 26 Feb 2026 21:45:21 GMT  
		Size: 25.0 MB (24951819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea66e384cb137e305f6886a174ac9534f7fbbfc3ff3b2b1ecabc6280ad99da96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9ffa0f635143979b68658d6bd486015093fc4728ab052400a7c7e2ef9c4ca2`

```dockerfile
```

-	Layers:
	-	`sha256:dc91bab7a7668a89ad18d77f2a91031ec2e5e75e486f15b9b1100e8c60933a9c`  
		Last Modified: Thu, 26 Feb 2026 21:45:18 GMT  
		Size: 4.1 MB (4112425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24c5253a413610ed0f54c964a4672ae427b1f07e604c847db814e32f5e112cd`  
		Last Modified: Thu, 26 Feb 2026 21:45:17 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

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

### `buildpack-deps:curl` - unknown; unknown

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
