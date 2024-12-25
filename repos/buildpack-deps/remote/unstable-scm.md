## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:b426e7b822d0d29804dddb5ac6b45ad6ff39331b0b034ebfef3de59a860d093a
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3172aeb659ebd16d00337d7cc34b37bc4344aa129bf32383852e1df549e7cd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140777453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac6b6267ec84e2668e73cd1adf1a5292d9902bbeaeec13b49a4da8ced772a0b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:b414df4f5677fe59988b95799e3893179cfd33808399b76d8526efe756540435`  
		Last Modified: Tue, 24 Dec 2024 23:16:08 GMT  
		Size: 67.1 MB (67136807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11b2301478d985327f8f8906f66ddf3f2613783795ac38826feac7bb3a813f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7639819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d4f4823102df517edf188bd170257916ac2f10a455cd70d209877aad518327`

```dockerfile
```

-	Layers:
	-	`sha256:a650565431162fd0370d4ef39233df9b18c312b7d6408527a55c212e8ecaf4d5`  
		Last Modified: Tue, 24 Dec 2024 23:16:07 GMT  
		Size: 7.6 MB (7632522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:386595a3f4f451e678f72c070f11766ce39a1da79cf2b2d9078fbcfcd7150c60`  
		Last Modified: Tue, 24 Dec 2024 23:16:07 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8997ea752b39ef39d6699b84881299fa7c626b9d5e32b9b2abdb7d06d97a6127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134058345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24b4fcef98578bf85854eaff58819dd73b380836c8b0d4dbe68a53802066171`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:1e3bfde18be32fb9febe492f8f4a14b4e0ea8e6484b78dfcceca3b9ea06b7f0b`  
		Last Modified: Wed, 25 Dec 2024 04:50:04 GMT  
		Size: 65.0 MB (64979315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:27f73228cb8a1da14fb10dfbd44c14ab5ae5c28361883d3252336214314aa2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7640155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7598582080348e670489b1849312bcadbdc48d873cf783a15e8c5655b3b8d8`

```dockerfile
```

-	Layers:
	-	`sha256:93545f80e154ff1a8825afdb91b23ace1c38554de0710789b3872c90047aa15e`  
		Last Modified: Wed, 25 Dec 2024 04:50:02 GMT  
		Size: 7.6 MB (7632798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18051bc67d6c86163b4bd5b37a24ccc37f5b8b88a82114e8e9b6a565842551d8`  
		Last Modified: Wed, 25 Dec 2024 04:50:01 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:387e61670c0dd5342002ec5ff918f89043546aeb014c47740d6a6eb73e793cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128315298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83744aacda8eb7e6caeaf7ffde4ac82bdcb20f28f3e0fd1209a6eb0f6e93d062`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3be1b8d31fc4a12cecca1f9e259b73553bed584845788fd1fc2b66b29ec0da2`  
		Last Modified: Tue, 03 Dec 2024 01:29:47 GMT  
		Size: 46.7 MB (46707234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9942887cd0e4c0dbd616c261161d431660cfe04df19f0fb88f7040ab43995e`  
		Last Modified: Tue, 03 Dec 2024 07:37:28 GMT  
		Size: 19.6 MB (19598543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e09ace64d434f04ef956980b3273a080b684493925dd0ee78451c801f466f0`  
		Last Modified: Tue, 03 Dec 2024 17:17:42 GMT  
		Size: 62.0 MB (62009521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dc94d5835984fdc1913e5dac619d4dde7f4a1411d27b563c296a3ac14bc1397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7674007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b45b5bbe0d268dbd9fbef0e1d7003f86def947cd36bdd6998c1492df05c71`

```dockerfile
```

-	Layers:
	-	`sha256:1b67bdad54ee7d3cf3d2bed02ab7da4f2712603a6854f36a13d5422c730edd72`  
		Last Modified: Tue, 03 Dec 2024 17:17:40 GMT  
		Size: 7.7 MB (7666651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f1e3c2cd17fdeaa8aab05283566fc3819f300894aa57674c19ce25ecbe50a1`  
		Last Modified: Tue, 03 Dec 2024 17:17:40 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ba6f42ba7aefae054d5f3f1bb2c078cc0b42154bf67985259ea51890f16e92f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140512658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4bc14651d67b3d787ab2c20f60a20cd4624ada311d68df39bb40b296c58f4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620061c3ebb2b35dbb417affed40f3038b1d12ab7ec1b666d509e18d8cc8ad18`  
		Last Modified: Tue, 03 Dec 2024 11:51:44 GMT  
		Size: 67.2 MB (67165131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa757aa7912e5aa5e678a45ae35e15003eb74a602d8da40aa9ffaf5e93f5a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7684385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ff85394930bde7b388d9d6c1cf7bab862637d3629f3cdb3e6953a2fced1b40`

```dockerfile
```

-	Layers:
	-	`sha256:035677f5fb6f054407dcea7a584fe83af8c3343ee7a4ee69e62dfb3955679e5b`  
		Last Modified: Tue, 03 Dec 2024 11:51:42 GMT  
		Size: 7.7 MB (7677008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbdd037048e81b72bd044d348d4ce9bb4e7a97b2f9ee3680fd1ae6a27f7622c9`  
		Last Modified: Tue, 03 Dec 2024 11:51:42 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8bfa59a490e13b9cd8ba10ab45f3771ac6591355585c3d7ad1cc095ce6969fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144544872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f0102a243e2baded5dfd0b8ac60d803716a8881a404f592914143749268e84`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:11ff84ea00dd6664e516545fe56b76d43f131cd690417ebf04c5ddfefe8e3e2e`  
		Last Modified: Tue, 24 Dec 2024 23:16:18 GMT  
		Size: 69.0 MB (68990976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:676b50d8d342d0f66e04efc5c0237b4bbdc95b018b7260e1e0c6b9a2f6ecb5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7634548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d5a4ed4586511e22297cae409761f15e160a366cb4129e133748ccea044a7f`

```dockerfile
```

-	Layers:
	-	`sha256:cf325be20fcf67a9b92cd0022740200094afda694f861a93269b7791aa0b660d`  
		Last Modified: Tue, 24 Dec 2024 23:16:16 GMT  
		Size: 7.6 MB (7627273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:296bfb47fb878576bc13b20ce122459b4e7daa31831d24d4c858322849f18126`  
		Last Modified: Tue, 24 Dec 2024 23:16:15 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1fe95458c2a1597e474ab22eeab992b0dd3ca20270c9cb0ad29e34b758dc1365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139310939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3f05b1af333bd7a1d6548c97aa50a24c70ffe4d0dfb262d84bda07341eee6d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:547779e8d3d4ddde41b340ccc5c55eed6547696507cc0168eca950de620def24`  
		Last Modified: Tue, 03 Dec 2024 01:28:45 GMT  
		Size: 51.5 MB (51502465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd17db4d55a0362abe181f4687b9308ab24eba56bf7c357aaf0150dda37b50`  
		Last Modified: Tue, 03 Dec 2024 15:47:12 GMT  
		Size: 21.7 MB (21747415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faad181192abe7945e2597dbe5a13adb7a6c4fc91c9cc8ed7907444e118bfa3f`  
		Last Modified: Tue, 03 Dec 2024 23:25:18 GMT  
		Size: 66.1 MB (66061059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c8e5db01f6b4a196282e03ee3a072fdb6b0441419552c9108c75a93cc07190d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602ee0707cc9c4d48ec4a571aec1a7a4f397e1c9249737bb9ec632733138fac7`

```dockerfile
```

-	Layers:
	-	`sha256:365963a85ceae17855bfd0702f9bc4c91835f90acdc457783db8dc5fb090e31f`  
		Last Modified: Tue, 03 Dec 2024 23:25:11 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59a6796beeb3b9d0867665f4811ee1eee275a710e6a5a458dcc6fb93f8e48524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151265275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75fd8aab6398f04086341d332deb43da5a6cd1a16ef1b5a5e6dc0a987ef76111`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77093ba8fdd419c4df155b02b29ff2686cd2a1d51168effbff5b4e39d31c96b6`  
		Last Modified: Tue, 03 Dec 2024 09:43:21 GMT  
		Size: 72.5 MB (72483296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5af9d705848c2dce3bc462b3b76df9b1b1d306e6bd09c2e26bd22bfc3f0c9876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f651af8b104ea346af37805901de2cc5ba97cf50ebaaa790cf0de9c570f5583f`

```dockerfile
```

-	Layers:
	-	`sha256:1db2caa964222e7b334c9d443db179aa27f6a7916d2932972cac65ad9c1e5d72`  
		Last Modified: Tue, 03 Dec 2024 09:43:19 GMT  
		Size: 7.7 MB (7673155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b523a122ad81c64df21fce3272cb02fca3d3a9206244cbe6d869788cadee4d0`  
		Last Modified: Tue, 03 Dec 2024 09:43:18 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1c11dc0f6cbccc5b2666d1000b1a8cabfc7e0cd69cf765e6f13551179129bdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137712618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050bcd9ec7b82998c38f40a2089324ac25931cc174dd8636cef601e3fb5e5402`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:b3a9bbab72f01dce27644d4f039f493ac5e6e54ff93d5cddb115f95af7c7ff7d`  
		Last Modified: Tue, 24 Dec 2024 23:21:04 GMT  
		Size: 66.2 MB (66171360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3045cb2fa1924b6ebe89757d807fcb7e1684649b7dc1197ddcc0b68d6d2237bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7629972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954774fc0b1411cf87f88c7fddf147a9a67c94c2fbd8a6fb5f40c87de61bc871`

```dockerfile
```

-	Layers:
	-	`sha256:f20d78cb250d0ecf18d1a75ac9fbdbd15ba56aa0cd81ec6ce0c50c55f7c6d087`  
		Last Modified: Tue, 24 Dec 2024 23:20:56 GMT  
		Size: 7.6 MB (7622643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865a6e8b3a3ac009d21d4ace920ddce3a7988bccf7b1729f9ae28f1d25db9d8d`  
		Last Modified: Tue, 24 Dec 2024 23:20:54 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d19ee50e9c87be055f057c2176a0f83ce2858755601752cd59ae5344700e52b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143122605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67a3d9f7958f8cf6734e2ce105a3ad5ee75476c28a8f7edb133b487715e2ba`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:5a51670f291e5f6590a069589cb9515f14909c76a4c6118030edb7558e2bad72`  
		Last Modified: Wed, 25 Dec 2024 03:30:15 GMT  
		Size: 68.3 MB (68331428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d7bcbc3c83946e452da71f2bf465e27279bb49f04e53aa544c72f693d9d6a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7640237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e816f9dd2f8bf480790d1421cfe02157a896b465037d4f030c5b7ef7a91e622d`

```dockerfile
```

-	Layers:
	-	`sha256:44382edf72e8bc1bd925493adfefadc963ac2d6b16e279c2c2467b984e7537c4`  
		Last Modified: Wed, 25 Dec 2024 03:30:14 GMT  
		Size: 7.6 MB (7632941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e2605ab10b2c60e4ad1c657eb445beba2b73faccb861ca71e9b914d3275430`  
		Last Modified: Wed, 25 Dec 2024 03:30:13 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json
