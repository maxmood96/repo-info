## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:080318f3bb827754dab1d480decdf854d7d485f96bb4f72c73ad30d3a8876bbe
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
$ docker pull buildpack-deps@sha256:2e7e85bc0d64366d791bc02bdf57dd4679d804f5da6777ea6c899cefef37657b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74893166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a5149afd60090de47b540f8e27a2f2cef56bf007268a106000e4f5cf955d34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e781444058f922b1e03be67e5443f10b96948ac463944e06a0fa1525feb4210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3d0801e95444b03e2224bd65bc839c1454a606c432d21729182fe3d6d40b65`

```dockerfile
```

-	Layers:
	-	`sha256:9f24c36fc1566cb6af03cf9d9eccf024effa84267feee11100c7ad513cb0bcd6`  
		Last Modified: Mon, 08 Sep 2025 22:20:16 GMT  
		Size: 4.1 MB (4118790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178caa113898b2c3da58a94a5a913cded15a516eaea4b4092907ce163a4d0c04`  
		Last Modified: Mon, 08 Sep 2025 22:20:17 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4904e3e62a55dd9b3ea73149b0caf900ef2224883271c0780ad24b1d5ca3cbb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71783647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e620ddabc620d2f787b8815bdcd964b47206e93380062963354814472ee8d1f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:93fee7f039682b45509657d20627a8677376fb460d8b9d61131616286dad7986`  
		Last Modified: Mon, 08 Sep 2025 21:14:46 GMT  
		Size: 47.4 MB (47443594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eda5e1ec6a0c1f6af96a205011570e8f52ef368e949e16b2f9a27f81c436e0d`  
		Last Modified: Mon, 08 Sep 2025 22:27:55 GMT  
		Size: 24.3 MB (24340053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7cdf997ff9fa1e94abff35b0e9b10cebce105de1b5f718800c3bf6ef390aaacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab0be926cc4cacc77fb152b64090f0cedd3e24e570f06fb5b1ebf3045461dc4`

```dockerfile
```

-	Layers:
	-	`sha256:736ade1d2e81d61b5a2b2b2849b419eb3bbc309c4d9ad37842e239bffc125ebd`  
		Last Modified: Mon, 08 Sep 2025 22:20:21 GMT  
		Size: 4.1 MB (4121780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfad8b9642a8550e9f40bccab4670bb7ea57b68894f8094ec06bc830abcf740`  
		Last Modified: Mon, 08 Sep 2025 22:20:23 GMT  
		Size: 7.2 KB (7201 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:42c11d2d59bf5a446ef9afef72bfa2e8c46dbd33355008dd9080b1bd7646e732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69325750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb824f6c065a68ab599c654c6f04b3b030e66e4775044656d3029e08fd4264da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:395f9ad3c9d37c6ea60897f33e8b189e9cd41fba6c60ab63882fd95de8ebb9f2`  
		Last Modified: Mon, 08 Sep 2025 21:15:43 GMT  
		Size: 45.7 MB (45711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87266d99f84095bec303de1733ad218d485653dfb6da729b7a066c18810645f9`  
		Last Modified: Mon, 08 Sep 2025 21:57:48 GMT  
		Size: 23.6 MB (23614030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4f5da1b14b6bbab64c6dad30354651b16762d3966e3a85b40b29ae6d7603d266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb05c4fa7e4ad4f21788c05d5a1c38bae143b8312a3dedc6b5b4686027a51e0`

```dockerfile
```

-	Layers:
	-	`sha256:2fde894dca18e7c41209c3128d5cbbd1f12425ce86381a6f7168e7fc3f26c0e8`  
		Last Modified: Mon, 08 Sep 2025 22:20:28 GMT  
		Size: 4.1 MB (4120291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4226765342cbad0a0ec0e94c586df9f2e39515618f92fcf0e3373bf1f12fba`  
		Last Modified: Mon, 08 Sep 2025 22:20:29 GMT  
		Size: 7.2 KB (7201 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4370673eaace3a7f8dc3fe0df856d09f11d5bf8d05cd5ee21033a7151a2c68fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74659067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22078bdc2c81235024d1b3faa58607491f51d50aa5c747222c7267613aae5990`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd36c08acb8bfd3ecaef97bc215303e9b1c59f47cb418c4692d97f29cb1b17c`  
		Last Modified: Mon, 08 Sep 2025 22:26:04 GMT  
		Size: 25.0 MB (25015321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64a62face5cd57aee41f97c28391e9b4cab928bc1f97d88339e386244e82ddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f977a5cb113c5aca1e88490c6779b242ee6c1475ef3942d2e59516b7e81b9b`

```dockerfile
```

-	Layers:
	-	`sha256:c56135d1e9d5fde32b51917876d986a677d8220b524af343f0e8e52e797a8b92`  
		Last Modified: Mon, 08 Sep 2025 22:20:34 GMT  
		Size: 4.1 MB (4120332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a555d8ae19e63f63415d2e92ebae4433717e1758305bf75d0c7b0eb68035a2d`  
		Last Modified: Mon, 08 Sep 2025 22:20:35 GMT  
		Size: 7.2 KB (7221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2422225e8f33f03d82c2f5e621a6b23ad76c87691a6c5a96e8a5594281642cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77568460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852139ee3bddda399aeb76401785affa3e79d635768130dd8e86586356abca43`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95e6ff4859ead75e29b179b0636a999dd68cde264f9c74ad8882d9d5dcfc9c7`  
		Last Modified: Mon, 08 Sep 2025 21:55:26 GMT  
		Size: 26.8 MB (26773510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e2a2fb63d48b0c4fe1ee57ae31e465ec4a7bdc292d2230d3c37fa416051a7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9415d1a9b1044e775fbb862ac906b0faa6843682106eae822737de7d969d4f30`

```dockerfile
```

-	Layers:
	-	`sha256:abe1aec5ce335ae2c6a78a7b21d3eccc9334268425e2fea3669d8801dea7f77f`  
		Last Modified: Mon, 08 Sep 2025 22:20:39 GMT  
		Size: 4.1 MB (4115898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7faed3b4c7c1d2e4df3a1975ec992d7e8be6c262cdeaa959d1dfd1764f124dfd`  
		Last Modified: Mon, 08 Sep 2025 22:20:40 GMT  
		Size: 7.1 KB (7102 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7c8f3512829f9222c4d09f2c9bd914779771e3afe3027f3224eb21fbb4d82d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80096252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46494f6099b80a32cd7780d37c9f40ffea66f89243cf066dd64a8ac601ebec53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:32fa2a85187997e792aebc62c3cb1ee63c7df313a0b5ee3b98226a6412f167c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b041ec9b6be65819a2d3e540fe8c73b1487b87ba4f6d2a8fd98df4c005375`

```dockerfile
```

-	Layers:
	-	`sha256:4add0fcf1b66604bfe9952b4d48bb08affec242833627d09547532e0f7ef80cd`  
		Last Modified: Wed, 13 Aug 2025 13:20:21 GMT  
		Size: 4.1 MB (4121155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f195416056961775e08be59d2b32099305598ee1a82820b31d50dbbc3849e38e`  
		Last Modified: Wed, 13 Aug 2025 13:20:22 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:141e6ef170db84b282f34de405a2a82320eba1e38fcac97e5e67cf7a3be34929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72714887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3966b701501d3ee71a570e436896f6a08d3b9f322570e5f9f6ba5733746e0fa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e41821bc74a26f64d4f81be6785aac1d7f09df07149a206784ae23523e36a`  
		Last Modified: Thu, 14 Aug 2025 14:47:51 GMT  
		Size: 25.0 MB (24950584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9285e8807d5a555e1b50ed354646f54b61c2f3ee84d62a7a162c952506758746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bbd324719cd243ba8a55f39b4b7c579bbfdf8dfce2400df7ed5a0a82b18523`

```dockerfile
```

-	Layers:
	-	`sha256:ec88dddae2618ec6ce65af34101ed29f1a1844c069293561535ce03625407606`  
		Last Modified: Thu, 14 Aug 2025 16:19:59 GMT  
		Size: 4.1 MB (4109819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c64cce5699b480e61c79b11216e978fd32851e9a1da300301d9308094a60659`  
		Last Modified: Thu, 14 Aug 2025 16:20:00 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:497c16421714207732e41403a38b2380acc7c9d5ad26a49fb398ae48172436c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76124741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684163f560d89e0de6713a16b3cdec4bbfc40d72536daf5ad166c5402530be37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:415a914901fe80a38412ecfadadff85e2638af84f2481d2452e5c06552f6219b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a3969f6ddc0127ce57c9f7ce99deed50c2ac52feb32866ebbf92a3c5f9919d`

```dockerfile
```

-	Layers:
	-	`sha256:ae6228e898b6c6f4917c10223f28853e056231c2a239846dc7b32d511e7be419`  
		Last Modified: Wed, 13 Aug 2025 04:20:09 GMT  
		Size: 4.1 MB (4118719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41bd85b1a341eaa191f4d361905c85455e3c70bd91303b34b18e5dc1d1e0d62f`  
		Last Modified: Wed, 13 Aug 2025 04:20:10 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json
