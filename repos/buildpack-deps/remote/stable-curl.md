## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:777620c05383178a36d21042f5e43a8b9bc0f39da1e6bb9ab723371932ae3ff9
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
$ docker pull buildpack-deps@sha256:6c3c650ca5440f9675e75f2483b7087edd4e0a08411c3f7553521cbaa01fc056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72501631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9934a592ba6842f87e05a281e86cc8f8a6f9d7cdaa175367ffbd29c5be9747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fadebbc385f6de799d5e86633ebba2d937b115aee0ec8e4675e7462f7c9e143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a29d9a26381bb7f64c7bb2dcc8921287804cff06c2cb886d4f21831fb607e6`

```dockerfile
```

-	Layers:
	-	`sha256:2e15aee1925f8db6639cf6446398ac489b1b861ff9f35d1b152c824eec67786e`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 4.4 MB (4360055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:237662db7ee035c68ee34a167711e09b9e8ec4936b5e5296a25084039680921f`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 7.2 KB (7163 bytes)  
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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28d439f012a0310c6db22f2297f146813de2421892f01b441505e3f4c957bb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74325334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fad1e8f27804d4c44d65c55510fec547c603732ea2c0ced6931ee9c6a2a1724`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ae395b20770e2a5d604e2059714080bf14f887d81d54b11f7c6d7abdd9740e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24ce351e2a0140ea50dffd88a454e30c9544e003f5a539a23a8492e599f8251`

```dockerfile
```

-	Layers:
	-	`sha256:0d4918b88e8c7436e5d0107229df039c88526f82d6546c404f4e272dac4deb46`  
		Last Modified: Tue, 08 Apr 2025 01:23:53 GMT  
		Size: 4.4 MB (4357113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf93331f841297cbfd242eccb050299e33a052285cf01dbccf961d78d8c81fc`  
		Last Modified: Tue, 08 Apr 2025 01:23:53 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

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

### `buildpack-deps:stable-curl` - unknown; unknown

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
$ docker pull buildpack-deps@sha256:2d595940ffb81f85fe34df6b14d059b0a940afd73168654884160f81ca034562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71159332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a53195a74708ded3f6528bda6a99af24bde5de1f3d12ae0fd3fd6d457e7f56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c33d0a443a02b325222c0894175e2e91c8639893f503d269cdb8f704f4c0d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0debcfa45af89c6ffa64a9be50e0014925c7855fc95f4ebff313f1c91976f866`

```dockerfile
```

-	Layers:
	-	`sha256:a141ff8893f692a0ca9ca5d2ce3a31dda61b020f1c20cf658c7af6730cdd8037`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 4.4 MB (4359751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2765bec492adfa03553cfa10226e232927a89c6a5b3037c157e4cadbb0ecc476`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
