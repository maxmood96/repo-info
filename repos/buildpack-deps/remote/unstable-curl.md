## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:70754ea23cbb9ae0ee46bd7ceef3aeb88b9760f8057e06c6e35dcbbb12a10264
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:479aca9fa144a8f06cf07b758f3f9727b6c2d35bd5186a775d54ccda8e668ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5667f7f701f9c7fd012e233dde8b0dc7f4fdb2090e6e509b85981828f139f303`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:41:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28b937e10116ada256c357287a871c307568d210af49526b0b54d19c0dcdf5da`  
		Last Modified: Wed, 24 Jun 2026 00:28:07 GMT  
		Size: 48.8 MB (48778379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bdf1cc0f4003e9838db969a7f68f358aa3694f09878b6330bfb2bfae2ae4e1`  
		Last Modified: Wed, 24 Jun 2026 01:41:40 GMT  
		Size: 28.0 MB (27989488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd71181f82bc2a2d9c97a1699aefb3122ec62e7f7e6998051ca6eb4270448258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4050663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7810766e9f70356ae6abe3b7dfaad63ef57e6f750815d23e8d62bbb891f3fae5`

```dockerfile
```

-	Layers:
	-	`sha256:1ad4dc5d12bab27b1c9c46c9f2731fb5bd234c12ad72d5b56f5f4d29d46a850f`  
		Last Modified: Wed, 24 Jun 2026 01:41:39 GMT  
		Size: 4.0 MB (4043902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fae281c1ee92f5fc103b6bd57554eb19c64141abec5f395898bb885816a881d`  
		Last Modified: Wed, 24 Jun 2026 01:41:39 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c4b14228be344f51ddd7391cdeb11eff878abf609eaec8517d2fd7d51f37ffdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71016085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174e2bc4053d5e73c8544581ea07733be49aa2352cc93a378d561bd008dce69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6dddbc4e0b590efd809489171b20c0c05ae23facbf49b0dac491dc8f542364ec`  
		Last Modified: Wed, 10 Jun 2026 23:42:26 GMT  
		Size: 45.7 MB (45703240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86724da0b6362c0867d62fcf26f2b64559186172953570f5baa9b4fad9928363`  
		Last Modified: Thu, 11 Jun 2026 01:26:19 GMT  
		Size: 25.3 MB (25312845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f36a530a4cc208ef803fe4cbcc2ee341b9b21fefa0188a6e4a7c7b9ac672c433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836ebe1ec116d731ec2087643917a754443f5b4480989ffec61e845cd924fb6a`

```dockerfile
```

-	Layers:
	-	`sha256:49cd5abd5173f3421f1d3c0dad4755f2a2ba4b4a6ade260d54dfead97be4d9c6`  
		Last Modified: Thu, 11 Jun 2026 01:26:19 GMT  
		Size: 4.0 MB (4048843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a12250227b8a8c118b88047764f968a2b7dfe816ae4d7128856590d0fa1f2e`  
		Last Modified: Thu, 11 Jun 2026 01:26:19 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f1c5684056780adf5938b84f6556d281f128686a9c6695a2b66981d97ccfd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75942854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56acaf5d6f220fb2073b0159034f511208da04076b557b5f4f2fc49705ec39ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bde100970346a8633eb293a95aaa718b901d789108bd4e63e4f66d9d3771ea`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 27.1 MB (27124297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1cfe9d1ab18162089195db3a5ea4d33516cd02dccf20f5b9d4f3d07924b863ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857334696a409c2ced6b95c74c88c2a9925eefd67a80b6f49f11dc35be52a897`

```dockerfile
```

-	Layers:
	-	`sha256:8028b1960efd439548990b1b7caae7dd88b7b61e5564fe3c0470091ea8f86876`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 4.1 MB (4052715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b33d67b68faa91981241aec3565e668468013ef834f0f37ed7056a72369561d4`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1ddb231e9a7a821928ca481dbe0ed826eca3d7e9191deffcc5e1aa974e46c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79198360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a4de0567f1345169c1307e2f3b2fb3a38ff8ccf5b2ace8f410800b35126db0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:466f7f9acdfac81cb720fa13d53a50111bee95182357f963947200187b3ae3fe`  
		Last Modified: Wed, 24 Jun 2026 00:28:18 GMT  
		Size: 50.1 MB (50080955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4172c1f095cffcf024eb812b3d434c5ab119bc7e7ccee1fb4953b378a0a4d2`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 29.1 MB (29117405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a76bedeb287d0f95b2c3181fdb442d75fa4aeffe215f6c522eed4c065db5b327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4047758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06c6e2d8d67f0d0d88041695fa80178231fb609ff81546a4e0f44dbdf582b6e`

```dockerfile
```

-	Layers:
	-	`sha256:746e80a2b47ecc809dccfb482e660e869c9d8d493b217a713ea7c3cb27d74402`  
		Last Modified: Wed, 24 Jun 2026 01:44:14 GMT  
		Size: 4.0 MB (4041019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c0ea8a13e8fd61207b0c81fea8cee701a56c144cbcd96baddac72d24832cfd`  
		Last Modified: Wed, 24 Jun 2026 01:44:14 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ba81e0fec9f8274e0fe1e0cba3ac312b01310315746d5947a8cf1462bc70f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84249978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac1ed55db14415426af6794337e3971830bbbd4aec2a87573aaa23ef98fb605`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e0ce2460747d14df6cfd1da4b61c0c9b7caf034c9fddf19fabbcba65c2416ba`  
		Last Modified: Thu, 11 Jun 2026 00:23:09 GMT  
		Size: 54.1 MB (54132513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f91ba1bf8c0d9e7dee82b12886a4f7ee70c339c3778c5cf99a230830c8d7b`  
		Last Modified: Thu, 11 Jun 2026 04:44:58 GMT  
		Size: 30.1 MB (30117465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8328cb04c7af92ad6fc1c5e67f25e03bec16f0cecdbff83cda3a23e9c6ada13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586969906a3affdb95524a749d845fbb8309cf7a158e1721b0644e94cf227b22`

```dockerfile
```

-	Layers:
	-	`sha256:50e793a8962f723b44811852d26b68bc208ff20c07961880c5ac787fd04e7075`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 4.1 MB (4051196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f22b18f19847b3549334fd9121f96c9585b972a5a5b9ef8b400d1ce650d16b`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:309c0ee196768b7ad74b92a404ec9457ad533c16fe3b8544056be39d92e55800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74150092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae7524dbe175e949a5a9241441d0f7fda17c56c9fee50687b2b271fe9def1d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1781049600'
# Sat, 13 Jun 2026 04:41:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2efc7e0091930e45ea6218e0e9380e67d07fe2085c100b1d3d74190636f5938`  
		Last Modified: Thu, 11 Jun 2026 02:48:51 GMT  
		Size: 46.9 MB (46911636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b18596f8f629861877fe419ef9028caff67b10f2dba8a160480c551f8733fcc`  
		Last Modified: Sat, 13 Jun 2026 04:43:12 GMT  
		Size: 27.2 MB (27238456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4b566387d40ddb2d6093cebbbcbe96075936b850d1852d03c63542eac3d4066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4045836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f45f138f1bce7a749fb0466803d6a178f4afb4084281f94f91a171e848ee7b4`

```dockerfile
```

-	Layers:
	-	`sha256:b2973dcf1701c2481ed36c8689014fa3a2125e2bf7da4bf3ae54f89191610f56`  
		Last Modified: Sat, 13 Jun 2026 04:43:08 GMT  
		Size: 4.0 MB (4039043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e241618679241926e6e5ca613f2152f522658553d8f03dd9b211b7100c14d47`  
		Last Modified: Sat, 13 Jun 2026 04:43:07 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e60c23937a7faad3f804fbdef5f89eff97185f65549baf51c8329ddcce42a98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76093880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6beb76272329f045ac8ce9b39c958e41d74a4fb5e4ba70dde270fe886ee12b60`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 02:46:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e9b72b44a72df002ca2c8ad8ccb65d46205892b54ff8d9ce0b5dd7be73544fe`  
		Last Modified: Wed, 24 Jun 2026 00:27:46 GMT  
		Size: 48.5 MB (48517796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d84ec64f6d4462ee570697b4fa616aba8bdae3a994fb4acb8bbc6decb3dc15`  
		Last Modified: Wed, 24 Jun 2026 02:46:41 GMT  
		Size: 27.6 MB (27576084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a79af2b03aac648c82048ce6ee6418b3c82b4309ed59f0492b43ba5a07ac22cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524c9f41a984e55f7d55c5d6a26c5667d24d6038f2a43192ff92975cddc53b6a`

```dockerfile
```

-	Layers:
	-	`sha256:112f7c042d905d8bfb55f1a98632774ba0d1014a0e73f2715e332b486fa78e13`  
		Last Modified: Wed, 24 Jun 2026 02:46:41 GMT  
		Size: 4.0 MB (4045314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36953af5a0a9a2dd11c2356f0f85247dbf590aaf1584c0c37a8b73ef7eadf90`  
		Last Modified: Wed, 24 Jun 2026 02:46:41 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
