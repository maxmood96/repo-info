## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:5712681bb74d5949f42f62f576d285b7946d4f9ec8c45081a58194587d86b52b
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e0fe68c4b061a8ffafddb203973e4b66b91cc1de3cf300788e50dfc035cdcf0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74903576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7852ecdf1490acb07acca731d201ea37fab7538d3292046e16cbb6536fc1b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:316ca827b517ca613365384ac440544ba0cad1d4fc83eeba6f204034372122a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a84a9deb205b5f7f8740cbbcae1dce6a9354616a76f426f2aac68e642cd2ae`

```dockerfile
```

-	Layers:
	-	`sha256:8b08444225b26fcda576b91b707b3384399f3efef48ed60ce91cfbef1ee2521a`  
		Last Modified: Tue, 30 Dec 2025 02:21:04 GMT  
		Size: 4.1 MB (4118874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402534085c27735c33a107f0cae6087af5c6b30f7300516ec76504967f485ae0`  
		Last Modified: Tue, 30 Dec 2025 02:21:05 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cc3a30d2ce8f4aad9eab821b8f4df82581e4573c72ad6bb41c2c2610e1305f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71794499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4c54f18b631695f1d72462aee2318905abb08fa54a8815d22c0fc69edafa3a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34295e8c92d32055cf38cee5aec380c4d26fb9f87d9d69deffe81403a9d5a203`  
		Last Modified: Mon, 29 Dec 2025 22:26:50 GMT  
		Size: 47.4 MB (47448770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cf1b0fd719c142e9016b7b007d0d982443d9aeedfc75f9de33d17efc3342d9`  
		Last Modified: Tue, 30 Dec 2025 00:29:32 GMT  
		Size: 24.3 MB (24345729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60114465c3e0cf3a57c2ba855b30f25a516b406a989b70616fecb9b820579441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a984fccb9ecde034961d34f2bdfa61b5415852d6535b82c20a90b969224789f7`

```dockerfile
```

-	Layers:
	-	`sha256:5b788229f8a19a9e5505dbf17bfbb3c68b5427eb700c63a0f5ec043b86447b49`  
		Last Modified: Tue, 30 Dec 2025 02:21:09 GMT  
		Size: 4.1 MB (4121864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f91a4298e610d4aa2c0ba62f8180c23641c04e4e03d20dbfaf734c4ce6dd60`  
		Last Modified: Tue, 30 Dec 2025 02:21:10 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:241dc7dea7ee80d42da2880707f59be57290c90aba60662e9e1c59c7626766d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69338228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd1e33bb8ddca3b0d9ac3aaa7719cf3ad3f725e1283e2bca2071e9e7648a58d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468c2ee0f43e81d6e097b24054de66ae95db50d77cef08d1eabe51a5dab43cd`  
		Last Modified: Tue, 30 Dec 2025 00:36:02 GMT  
		Size: 23.6 MB (23619911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07a0e60c83649ea55291abc24ba3e5ccd87989ac0f3c596e2ec3fb08324d0b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c75000572eff2b9dc0042aaa7fa83b2728666e3d8f95040b07df63f32506722`

```dockerfile
```

-	Layers:
	-	`sha256:1be3d571f6557c468381bbbba01e8a458946ea814cc094ceffe1d368511adb82`  
		Last Modified: Tue, 30 Dec 2025 02:22:24 GMT  
		Size: 4.1 MB (4120375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca768c256282f0b55d963d791fcf16d0520437e0e40ff50421b9979b81bbb17`  
		Last Modified: Tue, 30 Dec 2025 02:22:25 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a65ca32c6bec847c737c9b3afae4e787aeb54468f4ab50d1e0a8b8a16beeb97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74671238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22c0f7cc70fd16dad8e81ce06ec9b8303d532a768193cd41680645877f96f57`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7c3d81b5c4e9b21a8ff0107f35a479e9363288903fd7f4fba449382521d630e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac076e799a0906a4664ee567bee395decabd360a6c9d2fe396caf5d4ab93bfb3`

```dockerfile
```

-	Layers:
	-	`sha256:69aeb4f8d80db4061f8e2dc3ffbfe02af0062b949e3d2bf75ecd142b88d79baf`  
		Last Modified: Tue, 30 Dec 2025 02:21:18 GMT  
		Size: 4.1 MB (4120416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d72bd8f8298480da03de4e8fb985f40f3914a05366ac9d766e1545525f080d4`  
		Last Modified: Tue, 30 Dec 2025 02:21:19 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7a29b9686b12b273edecaca42464879617acb0ecdbf9a70b0e639f43ada75e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77578059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be839a9e85a1a292075a8288d93370ec5f1af0576fcac06f9b7c006452b997c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb00c990eb2d1ca8a4037bb0b9c6e0d0d8b6c6fb47372c8ec75cd65588cdd8`  
		Last Modified: Mon, 29 Dec 2025 23:47:40 GMT  
		Size: 26.8 MB (26776375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d97593b12a9f693020a9e7739bd293d0bcda18f87688a903febbd6727e6e753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b86bce751cd64288fed5e3a1c6196152112bfea6a07cf84e88bcd09e4949592`

```dockerfile
```

-	Layers:
	-	`sha256:cd650eddcfa049dcb7feecf483451c385da130ef8af63a9f25e54ec89029a7c0`  
		Last Modified: Tue, 30 Dec 2025 03:28:12 GMT  
		Size: 4.1 MB (4115982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a0f351d7fbb8dd1edd79537df02821039a44d4ee11320548dcb0a98fad6027`  
		Last Modified: Tue, 30 Dec 2025 03:28:13 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c6199ff44dc6f13dc78a5826dc81d332918d343d4f3f91ef972befb0ec65ad35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80105302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2426d874f0ca285e7c8029b22284010f00964640a36004749561cd7802c266bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44afe623a2af1e017b0756e314b5b0882afdc551ddbb8ab4a0e0d718eb8f20`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 27.0 MB (26996817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b32d1c8d8611549ed3b530efb015083aea1f6ef1ef34c2cef62e3e411d6a22a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadc8e4e7658d3c0f9455d3ef94f3d7ebdb32573c8c1ba542e91fdb4041e3991`

```dockerfile
```

-	Layers:
	-	`sha256:0258a3735c1d06990e9050ed75dec64f9c3fa1f1eb9cdc968ed44f150226c6ac`  
		Last Modified: Tue, 30 Dec 2025 05:21:16 GMT  
		Size: 4.1 MB (4122720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a7c52c865f47f81fa21b414a1de26dd00f57b0aa6e54c83bf1279265eb0294`  
		Last Modified: Tue, 30 Dec 2025 05:21:17 GMT  
		Size: 7.1 KB (7123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d89572bc8e733e13aa0c64005afb33c1828b8008aadeaaf81220f6d367d7235f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72725016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a5728c2e5c67ca84411317df10e3709fd52cdbe88d77f227fc7820982c659d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f7933c6ef71f06a1f0f33145f157cbfe6df70a0a3efc496c514e6bf0f3c52`  
		Last Modified: Wed, 31 Dec 2025 10:17:43 GMT  
		Size: 25.0 MB (24953863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:880bb221d54d31e0f4444035023ff01b4e481a43ecd7d4ba8c48f2c28dd31f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4697e4610a087700d2ff59caa5d9cd57bc364898cfbdb15acfa59c3815b2cf7b`

```dockerfile
```

-	Layers:
	-	`sha256:888ab53a5fdc7fafef0ccef1f1793012feadbd6455aae29e2267d31da8d3375c`  
		Last Modified: Wed, 31 Dec 2025 11:19:59 GMT  
		Size: 4.1 MB (4111384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ef3bd4d1df302f481632287670f007e159816c3f329671fd9e0d98e0c4a61d7`  
		Last Modified: Wed, 31 Dec 2025 11:20:04 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:76cf6d56b4c29a87fa66676a22134292705c43c5c44ceaaa766718b1f9f226cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76141596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5cdebf8c9a37f0a8ed725621cf3bcd5d228814742730acd9e76a902e7a0a8d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:34 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:37a4de4df42fcfaea4f5148ae42a25463df13ab33af9c0ed7de844f9b658cb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6533a1075bf0521af464509b0224287490eb46ce13be38439b7910c868d21cda`

```dockerfile
```

-	Layers:
	-	`sha256:9f7c1175a993c300ae923a2bf07d70006ff16b307c8555c93214fe7748e28851`  
		Last Modified: Tue, 13 Jan 2026 02:23:20 GMT  
		Size: 4.1 MB (4121323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6968accb3814b448c724735a63d3898f62dfafd24e6a64d6162e2e122c7b0c64`  
		Last Modified: Tue, 13 Jan 2026 02:23:21 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
