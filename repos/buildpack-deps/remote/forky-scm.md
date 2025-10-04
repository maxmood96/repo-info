## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:bd3f98ee0c181d8228f2f654ae38780ed6d4ee1325abd9c7662386cedf6a213a
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

### `buildpack-deps:forky-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5559e1fcf0d35001220f3e78f057bbd57ef4e41a8f90600e976089869d4011fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144125566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97abb5f3b65d9b2ce114da86da43fdb5d485588944994b6edfd5478501de8229`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075219ece41f099ca8ada652efeda87c6ef755098af129d14764aea953222807`  
		Last Modified: Tue, 30 Sep 2025 03:17:10 GMT  
		Size: 25.9 MB (25851839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf321420777749b1953b35d223d4252c4f58791cfbd9906817af3697f147d98`  
		Last Modified: Tue, 30 Sep 2025 03:18:15 GMT  
		Size: 68.5 MB (68536909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00fc51c0d6ff86d6ecf1f76652e3988d124f1c85ed2b24ede14284965988d50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199bf70331e7cbddf559b646a3ff3222ac79df34ab2ee8d760ce6d184e11fc0e`

```dockerfile
```

-	Layers:
	-	`sha256:56a5c6ab97f6362b6d3598233d15118431e4a25d0ce29964b36ca4b2eca57090`  
		Last Modified: Tue, 30 Sep 2025 22:36:42 GMT  
		Size: 7.8 MB (7765483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f1c32a7345a77f1e0dc9e6297a2c4e2fa2a29166eb2d63a513abf909d06c9d`  
		Last Modified: Tue, 30 Sep 2025 22:36:43 GMT  
		Size: 7.3 KB (7308 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:05d71f61faf84cbfe46e5e4b5cd86ff7e7026d42553e6b33cf72873d366533ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133086848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb7ff9f230be45226c79cbd78d60b53e5e5a34ca17fc745b64c396b36c0ab53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43934bcb3ccabc44fd5dd6a6383f81957a551493c079cc1ab7f71f687b26a8cb`  
		Last Modified: Mon, 29 Sep 2025 23:34:21 GMT  
		Size: 46.0 MB (46020847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c128e1aa14ec2c1ed27b97b88786e99053986c4d3e241f522a65c9ca20a3c3`  
		Last Modified: Tue, 30 Sep 2025 01:07:25 GMT  
		Size: 23.8 MB (23753836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eb4cd8e51aada198f64424fc2e53d3c2f6cc1667729584cdf6a84940b99a1d`  
		Last Modified: Tue, 30 Sep 2025 02:39:35 GMT  
		Size: 63.3 MB (63312165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7609a837c289767f88eadba7055d7b28f1289ada088c2fa738c470e63c823525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2564d7bf631ad73fa9e7b2a7419d0d26d5465ed8bce80332a850829d05c75e`

```dockerfile
```

-	Layers:
	-	`sha256:bd489ac00fd5e427ce2c157a2b3cdc7ab63bc64f81b936cf390ca8d524091bc2`  
		Last Modified: Wed, 01 Oct 2025 22:20:50 GMT  
		Size: 7.8 MB (7765982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71099acb2d92a540020c8f0c4aad987f9c3de56d353dc7d33f58251fac846689`  
		Last Modified: Wed, 01 Oct 2025 22:20:50 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:98f3971a030ec04c585db789c9bf941fed13ebce02cbf669ba34489d194048d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143268987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9a0082a2951e85a77c3b2310b9d8e4e09f3df22b7ae7c058d3365d4bf4fd9f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7009e42d3323422f2397c63e68313d31e460dfa892d093803cd931e5199733e2`  
		Last Modified: Tue, 30 Sep 2025 01:18:56 GMT  
		Size: 25.2 MB (25209361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde70c2343e98e974396577ed833e905203bb8d9de40b076f03dd816afd1872c`  
		Last Modified: Tue, 30 Sep 2025 02:14:07 GMT  
		Size: 68.2 MB (68179749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fe3f109daf1ead65a8b459a6bdbff6b26ad31fd8a432d3c01a8da3ccab35033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7780535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acf1af5bf3a0d26c11ec627b2447632eec07253b791ec381bb363b12f792bcb`

```dockerfile
```

-	Layers:
	-	`sha256:60d45375e2b61eafc76853974f61035bbad5069680e3b7dc268bd743962dd182`  
		Last Modified: Tue, 30 Sep 2025 13:23:52 GMT  
		Size: 7.8 MB (7773146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d88811b43f5ba231168a051b377003176fc625683544c4fbcb51686a4d116e9`  
		Last Modified: Tue, 30 Sep 2025 13:23:53 GMT  
		Size: 7.4 KB (7389 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f32e40c74fbf0446547ec526bf84d331471c26b47e7ab9395e6cc3900e121bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148442778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668d2da733cf9e804a9a34df229e07096ddd3672e0ab36df1a0da11e837edb58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccf114b881a561e278525714169b788115fe512463f3cf36ea76912c59a87cb`  
		Last Modified: Tue, 30 Sep 2025 01:18:44 GMT  
		Size: 26.9 MB (26896436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ce394ea3b0f58521d466c625f21c99b1a0c4601ea3a202665effb24b708c5`  
		Last Modified: Tue, 30 Sep 2025 01:19:29 GMT  
		Size: 70.4 MB (70426922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65d86a107fa5c722f95631794417505e7666ddc103444cc317f77095adf8aa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cefb9ae6ee7b5b0d02d2298fb7557e7da959f777fafb5d5a1658310a7355467`

```dockerfile
```

-	Layers:
	-	`sha256:149ff5729ce956245c002f762ca286a30d5e219be9371914d5699fbd67d6e428`  
		Last Modified: Tue, 30 Sep 2025 16:36:59 GMT  
		Size: 7.8 MB (7761633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2378e7fa288955fd7432da39cfb36ed7a1b1480a02fe8de0b4a2760b7db1af`  
		Last Modified: Tue, 30 Sep 2025 16:37:00 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:28c8100b23ad5aee6bc805ea21faf9544b88cf8878dc42bb514cffdbfa7af0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155652836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bd81172b642f0a0fb95d87d02a98f7b94cb621856be0175d98c7b3638a6a98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c998caf3e9e3602596b17377df87ed145d1ff51c75338d4bead32fdc1773c859`  
		Last Modified: Mon, 29 Sep 2025 23:35:22 GMT  
		Size: 54.8 MB (54750879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457c9822c8c6d2c9e044696c2965d09ada732a8ed5c4fd9aae6bb4d5485465f`  
		Last Modified: Tue, 30 Sep 2025 02:26:32 GMT  
		Size: 27.2 MB (27195197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2cacabb13745ffbd8c02c2e802891bf54d67d9061039099ae668f992cd1b33`  
		Last Modified: Tue, 30 Sep 2025 09:22:13 GMT  
		Size: 73.7 MB (73706760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:130766db4f4d3de8c5d07ba63ee4f91b0c9e121f75dbc1d1afa5ba52887064d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1311bd480b1494614152ee8ada54a6227a842cd31a6bc76a7b821818f29ad6df`

```dockerfile
```

-	Layers:
	-	`sha256:b757ef154919d6bdf8dd3632c5c83d43b4bbdc369e303185e1717fac79aec879`  
		Last Modified: Wed, 01 Oct 2025 22:21:05 GMT  
		Size: 7.8 MB (7772580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3dd082b97a0a6c6a00b5ffcf1f6c743f068fc8506512d9a7c77e763feae97cb`  
		Last Modified: Wed, 01 Oct 2025 22:21:06 GMT  
		Size: 7.3 KB (7341 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:95cce70f9039c8937a1bfb054a54573b6dd3b9e706b574b0475b00f67ef043b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140373853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb256749c23e184aa2770b593ac7a4698c8ab9838ab78e1445b614531e61856`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:db7be57cb42d3da83b1f69e7698442aa575eac43cfb6c579690c32c4f1cc1c22`  
		Last Modified: Tue, 30 Sep 2025 00:49:36 GMT  
		Size: 48.0 MB (47970093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d1cecefcb8fd1e3777e94b0c79bf25f44457085d008c5a4fee32d8fdc9d9af`  
		Last Modified: Wed, 01 Oct 2025 10:49:03 GMT  
		Size: 25.1 MB (25109277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee41da47ca678334fe3f694139d0ebf4d315d1d06f09134537dbbab73cd4e46`  
		Last Modified: Sat, 04 Oct 2025 03:31:05 GMT  
		Size: 67.3 MB (67294483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b0278c332709771cff75c72597b9a52f98d9991ee05001c3a233d2124d6eab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ea977e863e34befcfbdd73fb8dea9255361d60bbcc43ac93306d45515e7d6b`

```dockerfile
```

-	Layers:
	-	`sha256:05845119d3a9ebca467aa0d61608169a609e1d274eeaac29f4fd8d8bb07478d0`  
		Last Modified: Sat, 04 Oct 2025 04:20:05 GMT  
		Size: 7.8 MB (7755283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772acd04c461fbaa8a4ba8a43756691067d294593cdb1eb4c90934604848a50e`  
		Last Modified: Sat, 04 Oct 2025 04:20:06 GMT  
		Size: 7.3 KB (7341 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a0b1a24bed8a815df2e477b3426a19ac01c4be2e96f67acc03ea0af4caa9751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145808558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290dae844a741a56e286931c0476a4bee1e56962c4cbeb9b618d57388178af71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f12f0b09af6c73f5ac02ec4057426f99780ba4cc2b7ffa5da8754ce19dc3c40d`  
		Last Modified: Mon, 29 Sep 2025 23:35:21 GMT  
		Size: 49.6 MB (49576014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd2fa0437cfacaf00281ef1e68d7f757d4929c7cd7fef87c86f4fd3b95f9df`  
		Last Modified: Thu, 02 Oct 2025 00:43:13 GMT  
		Size: 27.0 MB (26987131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0807bf042d979330a7fd99ac96e452f05bf73f9d878b1183e51f9b13a14fa197`  
		Last Modified: Tue, 30 Sep 2025 09:33:41 GMT  
		Size: 69.2 MB (69245413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:06106641a8ed784af04561f44600c39b60fc95a7a0dc6e3f82a1cd262f951cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32252456b2bf5aff66a931d03e50caf2932ce5bae2ee92c426425bffd08e797c`

```dockerfile
```

-	Layers:
	-	`sha256:90385cf326c884bde665289616b597dcb4d96efdb621bbedd1291456ad009743`  
		Last Modified: Wed, 01 Oct 2025 22:21:15 GMT  
		Size: 7.8 MB (7766396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6dd9025ef2849a3c58060ba1aef2fb6b3adbca5f967d076f5c31f58c78affd7`  
		Last Modified: Wed, 01 Oct 2025 22:21:16 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json
