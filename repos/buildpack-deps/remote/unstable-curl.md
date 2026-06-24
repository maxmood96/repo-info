## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:9672693043e008de828142b4626f499a11597e81caa63a833936e4cc49b42865
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
$ docker pull buildpack-deps@sha256:2c4ee93f9516f609f4729e90cbf6c2024ab1afe5c9b5826c9214b0565b8270da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71053022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3659fc200e8693ba1d96af048a7f42e3f4bee6da4f20ba716202528b412cf257`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d675c589a8a116f3580b1211f18fa575a815f4d2314413ec9c2112d3a61d24a6`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 45.7 MB (45678632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0274b6b7737c2b06a1765a2a054ed7c230000ea352ee09b5b9399df372d1dcb2`  
		Last Modified: Wed, 24 Jun 2026 02:24:52 GMT  
		Size: 25.4 MB (25374390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9534eddd569651aa49e6bd9caa37e03ba32a5d6a2a776c8079bac4c76c332e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce7f10c70d8704e662126c7dd0537c71c56e3742f27d73f0d2627765c0ab0b5`

```dockerfile
```

-	Layers:
	-	`sha256:b2f8bb4a4d3b0675f25f242e4d17758418746fa72a7d0792372ff1374a3d0d42`  
		Last Modified: Wed, 24 Jun 2026 02:24:51 GMT  
		Size: 4.0 MB (4045389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21762af61975f024f7b00f651e88e7c533615121d149eb0409ba3a0adb44e4e`  
		Last Modified: Wed, 24 Jun 2026 02:24:51 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5a68a808de60988e3ac5c1ffe3af1615b13e5d4c94ec1db8e0f5058b2d16629e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75991306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eff722d235c209077bec90a3e92d9194e04a44b2ec3815b8ccacb770708ba9a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:45:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4fddf52615bf1690082a9d73cb8346614997b5b51315236c93a190fbd50fb899`  
		Last Modified: Wed, 24 Jun 2026 00:28:05 GMT  
		Size: 48.8 MB (48798835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfb65123f81cd28e0545a5e6f88cbd0f9d83e9d96851b068d4ef01e4482bd0`  
		Last Modified: Wed, 24 Jun 2026 01:45:17 GMT  
		Size: 27.2 MB (27192471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4caa67162c8bcb8874506aeaba923e9ee1e6d1629b6d1019dda603553ccb1933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a23b3bfe8dc2452e972ff29f56ab9c70dc805e12e51a36d53c80e1b986fec96`

```dockerfile
```

-	Layers:
	-	`sha256:f38ed60eb2062a19b9216e112f3d27e6a0c9f3180d7728a1d98389d76b6e6d01`  
		Last Modified: Wed, 24 Jun 2026 01:45:16 GMT  
		Size: 4.0 MB (4049261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8907ce80102752b733734436dd525f47a5e75c3e741b206311caa6597f49de`  
		Last Modified: Wed, 24 Jun 2026 01:45:16 GMT  
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
