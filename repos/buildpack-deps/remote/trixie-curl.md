## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:06de598d5fb8cee810f332459797edc3224254b9f6b264c0a0ea2defddf247c5
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

### `buildpack-deps:trixie-curl` - linux; amd64

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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; arm variant v5

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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; arm variant v7

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
		Last Modified: Tue, 09 Sep 2025 00:02:54 GMT  
		Size: 23.6 MB (23614030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; 386

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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b80c4868e9c0a3bf0239530ab87e01528d509b5b26d425f1c9cb20b55cf6ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80098304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e048a54b9f2189b2266559b85f55ed546be892c589a6df0f94a0310a828082e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8361abe83114791a2a102586fa75978a8b64a5b73c65617cf458d291318852c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0627aa731eadfd5120788bb671193103245dab039abc47a23edda2c7df58d616`

```dockerfile
```

-	Layers:
	-	`sha256:cdbce461a85b9219924f278ca0f0ea44106b5927695a06e994cf5a58d302b1f7`  
		Last Modified: Tue, 09 Sep 2025 04:20:22 GMT  
		Size: 4.1 MB (4122636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5faab3ed5a5f0bcc603e65a133d648f1d04ea03aafcb55a6da4ff2630e35d801`  
		Last Modified: Tue, 09 Sep 2025 04:20:23 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1b40da235739436fcabf813d766c95395468cdce047b5742eccfcfb30199c7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72718237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851bf3fc6cde8bbd6526ca1a4b61b58474695acfddb047079e959beddd05ec28`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90d76a47de5813a426d271176bc3804b41f13cc296cbc341ba49afc8faea7d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea065661941296964e38fe7caae732cbe70cc71af35944a7f5f508c669c781de`

```dockerfile
```

-	Layers:
	-	`sha256:7a5a8dd7f211ef4dc60665d83dd78f3b62cbd8fc9fc9cd1307bd3d2ddd54ac25`  
		Last Modified: Thu, 11 Sep 2025 04:19:58 GMT  
		Size: 4.1 MB (4111300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb0ddb3bae600813007d073a85430e5956f62ba28de2e1f29a7e787e30bbdb0`  
		Last Modified: Thu, 11 Sep 2025 04:19:59 GMT  
		Size: 7.2 KB (7167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f68007848de88b413c1ea9e0afef072d29071029caa31da31a7522735ae776f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76126694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cbe6c30f5800125fb4bd4b9163359ffcda8d5e80bbe476271722d1686f6df7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2433a2f3080f45247d8632714ba3450eb2a2515eeb6f805695ce753eef05e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e5ee39193cc138b3e3826c9e63175698fa9d4488eea4c0b9db95abe91d32a9`

```dockerfile
```

-	Layers:
	-	`sha256:24951376ba687ec9e853012d16f636161054b12088248199a0176e6d2b718aaa`  
		Last Modified: Tue, 09 Sep 2025 01:20:28 GMT  
		Size: 4.1 MB (4120200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:480b5aa58deb00a88aeaef87044c9f89210c531ba2e022f5696d6b9a7ad066d3`  
		Last Modified: Tue, 09 Sep 2025 01:20:29 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json
