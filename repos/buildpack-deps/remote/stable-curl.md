## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:7f3c37b55e36aae1be8d4a72aad94fc47564a4a76c5e838cee9ce9640129fd4c
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:333ba289c859bc57d408574b988b31ca7bf9777b365c8da64727f68715518ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72478974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91801a68eb85de45a01bc36d92280721736a7c5addac6e78d6ff05e8863273d6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1423d97832283b5e2ed67f50a74444591d141c6e67b38f6e74c4694f6cd33d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4365883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b745e7c43332a1de3470761d50c97fdd44a58e8664ae8126a8a2f460e71e45`

```dockerfile
```

-	Layers:
	-	`sha256:cadc62ac2ff74e0b0dcdb09f35881911d51a9b56d6fa9e01d3fb8bbf884b4bf1`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 4.4 MB (4358719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f7bd7d08515975ecfc9ab42446b6b307e7b9f12fad7ab1a29fc84288afe0886`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e0557d7090bdc485fd9fcca4d492da1c562f6483d0da47075037b983dc7cff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68694266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4c7fd8b1e567696c73553988add6e853e507fcfd9eef583ef3abf64957e67a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92f0eecb0902c904cf1dad1c6151576f52ed736aab0bfbfdbdb998f9c806cc41`  
		Last Modified: Mon, 17 Mar 2025 22:17:13 GMT  
		Size: 46.0 MB (46004626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa782283a247b6a373c2a1bb96b43e6d698fec2513c0ac7f808329b094bcef69`  
		Last Modified: Tue, 18 Mar 2025 03:23:28 GMT  
		Size: 22.7 MB (22689640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c63da04a5545823d74bab1a22e2ea206880388f1f84bb77be7bddf98359c777d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af0ed559c6f2d66f6613308541301746bf012b959a5e9d735c206240249637b`

```dockerfile
```

-	Layers:
	-	`sha256:d2ac6cd791ae92a23375e795a34fc9592c20e3d0956d58eeb6fccde528d99233`  
		Last Modified: Tue, 18 Mar 2025 03:23:27 GMT  
		Size: 4.4 MB (4362235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bc7f3c3ebf133c9b7252daacd92b0ec301fdb48e61d3ebe25565af622c81c7c`  
		Last Modified: Tue, 18 Mar 2025 03:23:27 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0fedf677819399a4890675c080321b90777145ff180f1bc5e898e08f90a5edc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66140264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306115598a20b03b481cbfa53bfed30439d9081b3b1375178e8faa774626ea29`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5b9c68c614a4c1f964afe9a02e198e5347d8dbdf78f7f27b4837ff62df20b7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca217b092fa607ec7caafc4624772ad5487594f01bed66087730ef3f48144d`

```dockerfile
```

-	Layers:
	-	`sha256:6ea2228bc6a164dff1000cd503782edc90c75465167cd7bc802972cea0e20b88`  
		Last Modified: Tue, 25 Feb 2025 07:16:40 GMT  
		Size: 4.4 MB (4361624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88db7765a141e0f0d5d0f08695e6933b109a96c3e6d97b7410923ba391968eaf`  
		Last Modified: Tue, 25 Feb 2025 07:16:40 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a4ef43b568706d91b533aeb28acf2c15661b6c9d1b332c6b37dcd7d00a617815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71906283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69af06db0784df741a129793e7649834bf226f75267ca9a13fb1f7d778acbe53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0a57e0bcf173d3b353fa426debbd70cea1ab1c8bb888258912fc6341cb655b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496c3d74367b4b2ec8ce6f126f251d40c10384380f59bde82c4ce9e57ff1f07`

```dockerfile
```

-	Layers:
	-	`sha256:9e8867348647a6bae854812be326d7979077790bec5cf7f1213b6d02f74a2c70`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 4.4 MB (4359600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf94d50991dd56e8e28e665c9bf6d429cd456ae48d74153e45e0833d753304e`  
		Last Modified: Tue, 25 Feb 2025 05:41:43 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3a141c1432df22e29e37a42f4f6a1a60774084f91c8ba65a516998b18e8d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74301460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220fd3a6b367a2c721642b722d19ee3bbaaad040b003f9b5e717d9f7ed9c02ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e191898e03a9782c13272045f7c55ec3abba0174528b7c635be75c551b3666f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4362914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1a93929ace3d5733d664f48003ce09b2db814956b8e6216c85d333c7064ea`

```dockerfile
```

-	Layers:
	-	`sha256:c1bbbab70569adc06d7f1bf40195f8fa2bd794936bbbfa4620c4a86e6960adac`  
		Last Modified: Mon, 17 Mar 2025 23:32:44 GMT  
		Size: 4.4 MB (4355777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ce43ffd9f989625a81736199dd41bedfe80e8130176685aa757d25de4db1d6`  
		Last Modified: Mon, 17 Mar 2025 23:32:44 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4492593db5b2f8e7f63c2d231fac0fb4f7a016b9632fcd32fd1727d1c0abbc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72411228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f00d52ae6489c5983fe113e4856c858040228d832aeef87e6290c4161d70be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54f151aa1b87c0945bf97dbd3c72581adb102deeee7a48dedc6ef51580d82ec8`  
		Last Modified: Tue, 25 Feb 2025 01:30:30 GMT  
		Size: 48.8 MB (48758989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93e2f55385d2f9849f5c49ddc6a441349700a7ac20dcafe37c022942621cef`  
		Last Modified: Tue, 25 Feb 2025 14:48:27 GMT  
		Size: 23.7 MB (23652239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cc8b0d2c1cd2c1e69321c8754130d87eb745727f395a5bdd21269faaa9028653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4966027f91ba6c5a99246844583b24c07f2a7ec2a026d74692a6738394106247`

```dockerfile
```

-	Layers:
	-	`sha256:837e8dcf97e3764dedfbe87eeb376a92a0c7ba8355c755872923a19d8ea31b87`  
		Last Modified: Tue, 25 Feb 2025 14:48:24 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:20b086dca5eecde4bda9b1db3ea24196ec9a4c8469951b67dad35a0ba262851a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77956122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cb649c3141531c3786b05ae48c05053481eb9d332685bdc7d08fe4c9002ec3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa4729abbd28dec1e78b2f2195b1850011bc6158a1028859489d9636381c0b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81530781315d30c3f2f9b4d820e29d5dbc774b2f781011f9efd06a2b22f370f`

```dockerfile
```

-	Layers:
	-	`sha256:fbb6c2b7fce474043c3596eaa6a5b795dbaf8ad3afa2f65cf2b789719a0e57b0`  
		Last Modified: Tue, 18 Mar 2025 00:06:45 GMT  
		Size: 4.4 MB (4363211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e68ba407fa9a3013800e49f5237e5c3360bec1db9bad8af1890956af6179cb5`  
		Last Modified: Tue, 18 Mar 2025 00:06:44 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4dc5127c2c5291672caa864893e9598af33d6f45bbf527966bc7f4a114e09428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71135817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9862b4683d24d0ff4640a38403d3e0a3509df02dd51e3f32876c5e5fa9c3f13f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:16180c4c53fea8630b4b4779b2b14ba0941786412e49ba75a58c50fd8730e158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4365579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a27697355c640f5536d034ae5827bc41df529abad3264193e15f984e8b59246`

```dockerfile
```

-	Layers:
	-	`sha256:adff3bf045a0410ac69059939f27391a34d323c9f4445167e60fd8658a7cb344`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 4.4 MB (4358415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fab34465d986aacdf6402cc0d2e95e082081577e7babc21a89ec13e9ece0697f`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
