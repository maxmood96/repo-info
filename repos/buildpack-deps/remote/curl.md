## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:ef3733ec0757b22cd75e1b32aef71683819f713ce1d05516e2db175076041701
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

### `buildpack-deps:curl` - linux; amd64

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; arm variant v5

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5675865100b2e52f3e4ffc36011ad208cb851e9e440eb8e143c3332c27e6f683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66096021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c807deed6535e09dcb196cd0778c093fcf9496754ba79779e0fa7692d0626eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8565629e8ed015e543cefa30196338be3257d957a63564d4717cac726416a362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd664db978db1b3b62afcc8f9cd92eb05d7517f121398d5d9ed3f68208f7249`

```dockerfile
```

-	Layers:
	-	`sha256:09ffb4f2236d354556993a08f9f7852a6b1df843a60f25dad262536c250e81cf`  
		Last Modified: Tue, 18 Mar 2025 07:30:12 GMT  
		Size: 4.4 MB (4361016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e797d6f794b407b02b9313e3005650caf2074f60372bbe11c9ac87e812a7d47`  
		Last Modified: Tue, 18 Mar 2025 07:30:12 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:73642ca86646f211a202e5eb30d0b47d7ec4311c0ce3b054dffa39cf32d2f6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71849204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456d5282528f5adafa326d391d79188c28076c2c5d1ffef0db6a06a3c94a6bab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25c31e3ce8d11fa2faf3cf8bc2cc321dcf39b7c2930d0e4217d1d5c4c1445542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ce77cf6b6fa1c2722b950532e51860670fcb5f3d1f7cef538032643ada493b`

```dockerfile
```

-	Layers:
	-	`sha256:77ae5dba4fdb75288a67c075f8efa25b9fa98561877f2e9e10db4fe1fa546820`  
		Last Modified: Tue, 18 Mar 2025 05:00:36 GMT  
		Size: 4.4 MB (4358992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb3c14b65cc6893fbe166249713f0f0a5cd49a6ada332e88afd3596b1a26dcd`  
		Last Modified: Tue, 18 Mar 2025 05:00:36 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:84c204767cb7e0b90bafb12767fd1bff559c2c78870f258036b9624e96809e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72351760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcf474fa8fa3e36b696440aa460a51857bf8ed0384c2824817ecc7f81c12fb2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:579ff6a9178b7f862c70c40b253d6f0090e7792eed3ce083de0732adfc5f4826`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 48.8 MB (48756170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19bfe112f8e8e887df88219c2ac69098bcc8afda18a25b53168674379a8365`  
		Last Modified: Tue, 18 Mar 2025 16:33:21 GMT  
		Size: 23.6 MB (23595590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ad0c9a32b05d0670c51f799e311b9dbbd42de3b7cab9b58ef8244b318a90e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a8ee4820b7d1ece08f5c10e31c75d5d20ae3025dce0812ad05ee0861133c1b`

```dockerfile
```

-	Layers:
	-	`sha256:12c42f8f5255e5d3a616b4a71655ec5f8b16f30f189d9c0099ad85d5710b77ae`  
		Last Modified: Tue, 18 Mar 2025 16:33:18 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

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

### `buildpack-deps:curl` - unknown; unknown

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

### `buildpack-deps:curl` - linux; s390x

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

### `buildpack-deps:curl` - unknown; unknown

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
