## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:3d09538db489810f4ad9ff289676339cc4e087fcda78f1064606c278dfdf615f
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
$ docker pull buildpack-deps@sha256:c480efcc8c3b03f6cb7af812d7ec8c8e5cf905020f88b5c7c264eed5cbaf4692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141247077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731408950116fd2eaf81cbb1439cc276281228149ac1de401c7ddb9514bda36`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df0497091d0cfc8e931a73bef35cfd57d59f19322fcca6f87470d3b532a9d8c8`  
		Last Modified: Mon, 17 Mar 2025 22:17:40 GMT  
		Size: 47.5 MB (47542630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cd1ca2661836ac2dcfb48519e1a1fcf2b3ddbc182b83cfd451a37cea0328fe`  
		Last Modified: Mon, 17 Mar 2025 23:14:04 GMT  
		Size: 26.3 MB (26258246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149407641e16b36b863b091be42c587e870ccda41512acc3340e09ccd2a747cb`  
		Last Modified: Tue, 18 Mar 2025 00:19:02 GMT  
		Size: 67.4 MB (67446201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cab208991b8352543e58f1011fec6044fc2a53efeb0789ead2456f212a270107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7595761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62775d45e9debfcc99a083981638002583305e95b91ab1b2f3ada94f42627de8`

```dockerfile
```

-	Layers:
	-	`sha256:c8d7b6addfc52fea41d9c6d5ab491aea61fc47aa7b58e15fd7983eca5a66e02e`  
		Last Modified: Tue, 18 Mar 2025 00:19:00 GMT  
		Size: 7.6 MB (7588464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e502f973b8a47ede0a20bd9c86de715e7e1e47133b17a7b89a43d0d60cf926f4`  
		Last Modified: Tue, 18 Mar 2025 00:19:00 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4b8cb649885f173add39115c34c1176b822f7c87e24221c88259af5e236e15b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135735094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d1f663b24a5d657c96f1005a115721d655ec2afdadcd3d97816476e191a732`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:181ed5745a356167f17446082e0f91fa4520dec07c3cc08122f73d6e68f0ec6f`  
		Last Modified: Mon, 17 Mar 2025 22:18:17 GMT  
		Size: 45.8 MB (45764033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce18890e4323b22dabb2af5cd6dd6ee47e0cbe22914fe96ed5ec5652746adc9b`  
		Last Modified: Tue, 18 Mar 2025 03:09:17 GMT  
		Size: 25.0 MB (24962637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404f8f7fc411f8ff4d9e0e372fba1e5c10c5194b11ce9185a2da79073a4ac30`  
		Last Modified: Tue, 18 Mar 2025 05:17:45 GMT  
		Size: 65.0 MB (65008424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:730ac9c5a2e1538fa36cd60ff8fecc642c90adbf22911fc099578f36f3f41889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60638d368b2d9d81c0cb70fb38aa5b87dddf35cbe2809a64091735634253f293`

```dockerfile
```

-	Layers:
	-	`sha256:07c7153a4daf4952d41229ae9339de39c3737bbe1a70514bb57f45d87e099b2a`  
		Last Modified: Tue, 18 Mar 2025 05:17:43 GMT  
		Size: 7.6 MB (7594773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b5e63b0facc4dcc7d63a5fc0aa45bbfe8324c13fe7681aba39180569da9ee7`  
		Last Modified: Tue, 18 Mar 2025 05:17:43 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cb6a860df68f240f1080950e46cb2b0a6d7db7052ce4d3173e95deec4a8d8c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130605599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccc27cd999c812354a72b97069f3b97585200566e7e544a16ef1e4c22872980`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d0067c75852db589ec6309ccaa1c2e508a0e7bb3c58863fcadae19a1c1537e18`  
		Last Modified: Mon, 17 Mar 2025 22:21:44 GMT  
		Size: 44.0 MB (43957597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d864355272bf90fd1144966fdc99f539dd4252af76ad0a5d7e1ee868d856d`  
		Last Modified: Tue, 18 Mar 2025 07:22:02 GMT  
		Size: 24.1 MB (24132404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef046ac7256a24a47a1208d1dca17bc5d10a76b0eec3d2cd94577b18be639d4`  
		Last Modified: Tue, 18 Mar 2025 15:31:50 GMT  
		Size: 62.5 MB (62515598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5e2ba93def939bb93185461c20171b3e35a5d38e267f0c16ca2da5bfeb58a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7595673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af48e9b86ebd9a1a2bcc864f635dd6408e7506545f07d5f25276feed858746d6`

```dockerfile
```

-	Layers:
	-	`sha256:34ee1aaf6e91f0c95e5120862a6bca9679bd1d518ed0a7400abe51d85b4cc8f2`  
		Last Modified: Tue, 18 Mar 2025 15:31:49 GMT  
		Size: 7.6 MB (7588317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc0887e18c2fae6e74e29401330cfa80b37aeea432c182072ba3e0fc78c93c3`  
		Last Modified: Tue, 18 Mar 2025 15:31:48 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30f194a69a5c5331493f30dac2a24da8056ecbfe88d4c40991519211790a9ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140944992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2f8018a42371e40946c0421052c0b750c0295094acc0cc444949b8ed8e22c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94a031aaac55d50c4495d8888a65973ac1a320a931aa0e73e9fb6cef43e2efd2`  
		Last Modified: Mon, 17 Mar 2025 22:20:15 GMT  
		Size: 47.9 MB (47916898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9c585ccfb21ec8756fd9ca6b5b83f6e36d0003a2342f6f55b3087ee0d0f4c`  
		Last Modified: Tue, 18 Mar 2025 04:59:39 GMT  
		Size: 25.7 MB (25697882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6d5c4d521a51c32b5544ee4fd67c57ead31e48e0d9a394edb180d78318d630`  
		Last Modified: Tue, 18 Mar 2025 13:17:35 GMT  
		Size: 67.3 MB (67330212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:617fdf2cc54bf661d8905095c7fc9486960ee733668e180920980e67ceb46be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd64101264af48e7b16ea79c040ff3ff981a12a211ba4f49ae61ff7aa91b611a`

```dockerfile
```

-	Layers:
	-	`sha256:4ff7d295ab228804ae281aff7f0bf871d5b93f8e1e3fa23667c6595ac435cded`  
		Last Modified: Tue, 18 Mar 2025 13:17:33 GMT  
		Size: 7.6 MB (7596126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7568bca48c62340611dded011153ccde850ea650a89eef9c5c6159c8b00a1615`  
		Last Modified: Tue, 18 Mar 2025 13:17:32 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7a0628a4cc57e8821fa94285053666caff1732381a057774b4e55b0803ca9cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145749802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665fc68ab7ed4e76835da83459ee48ca2bcec0d066f834de685134a5d58e9eea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f3d6c6a3aa49b126cd200d7ce5830c3bb8ef015d44bad711b523cd3cad501611`  
		Last Modified: Mon, 17 Mar 2025 22:18:06 GMT  
		Size: 48.9 MB (48863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888eee8ccf6b7f4f49c878caf4a23b48de26dc0c12d38b4a0f13ce0b7214d834`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 27.4 MB (27396309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a0a08d8deb9509e0c71bd1f0ab45d6576afc1729935f007ef7d9163649bcf0`  
		Last Modified: Tue, 18 Mar 2025 00:19:00 GMT  
		Size: 69.5 MB (69490332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:926a7efba1cc7199fdd74d3729f6c0d0ef7515013148ca2b7ea508fd176d0f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7591164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6019bb97b8d406de053f04fdb23278b78b6d3f2f7209f4b9ca57683ccababd`

```dockerfile
```

-	Layers:
	-	`sha256:bb0338b9c7d9c9bf9f59236cfc7c6563bb3607de6d23717b07cdc6fcd732525b`  
		Last Modified: Tue, 18 Mar 2025 00:18:58 GMT  
		Size: 7.6 MB (7583889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae3d3ceb22d0ba9fb7dd9b05b1e415aecab54e43129794c0af2598581fd5594`  
		Last Modified: Tue, 18 Mar 2025 00:18:57 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a28364f054c146d17ec7941a856df0718e097a26317a4fd9473fcd726ff976dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140596210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c389a6f49f61717a5721682024a7b11fc9f0bd820e876771d15acb1c5ded196`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34ea8e316aa47eaa9617f1b9a35d3a8120ea53cd407c4add1aafff37c0381edf`  
		Last Modified: Tue, 25 Feb 2025 01:31:10 GMT  
		Size: 47.7 MB (47672872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d13ce39ad4744d80777f693b612839d6935dc5ee1e34838c927f4fa9839112`  
		Last Modified: Tue, 25 Feb 2025 14:50:38 GMT  
		Size: 26.2 MB (26241147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99f7abeee55e42bf6af8399f8945e651d4fb037fbd0f0edcba9023eb4a7ed34`  
		Last Modified: Tue, 25 Feb 2025 22:29:34 GMT  
		Size: 66.7 MB (66682191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:738c4709b1ee769519bbdf01bb8ce30268890b74449755bb14ebac8560334c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71afaf7c57e7c4a09f8a45510602677956495775a1f97e940728922fd383d846`

```dockerfile
```

-	Layers:
	-	`sha256:a8736bdb6af3ab1f50139a03d76b73053b4995f9b11826b8d54430a195a3351a`  
		Last Modified: Tue, 25 Feb 2025 22:29:27 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e42519f34446f7588d389bc3637752554d92126d4456e1352260cf2c96029e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151724962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1349883cf691f5076f40af2d1ffd55de868a46e49f93a81626b0fa400f08d38`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4f7ad9881f20bb4c15e9c02d5c71121438e0f80af4492bc3595dca35345480d6`  
		Last Modified: Mon, 17 Mar 2025 22:22:55 GMT  
		Size: 51.2 MB (51201856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277e01a580518b309bd39ae29e17784505bd4ae5bf702764ef69018aabfb218e`  
		Last Modified: Tue, 18 Mar 2025 00:01:23 GMT  
		Size: 27.8 MB (27793733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1b9cddd723c4c8c3ec8dc918782516b3f18afb7b43c91515f8578d7f2ee55`  
		Last Modified: Tue, 18 Mar 2025 07:11:29 GMT  
		Size: 72.7 MB (72729373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89b7df5211265aa578760e6bc57d977d8cef3c402c9ccbdc8d1bb183df766137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a05c7c33dab5f791d2f249714c5c8ab937e48a09adc98af69eb58c018f46245`

```dockerfile
```

-	Layers:
	-	`sha256:2f6d60e49c054c15ef97b5077caf2377e2969a07ba4b646fc2aacf9d3ce48451`  
		Last Modified: Tue, 18 Mar 2025 07:11:27 GMT  
		Size: 7.6 MB (7600960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea4d952c7468ce83328a8304e47d3b8b9837b1fc87ff5300e1b13ac092ab215`  
		Last Modified: Tue, 18 Mar 2025 07:11:26 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6d173148ce93962c4e28dbc5ae84576b4c819f3bc26e8098562e315155667b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137976906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc0d7f43dfe131ac05f1638a2938f8ea01cf35e15f9a4750cab0fd5c72f3069`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e088c063eb399e547ca6ed33d1ebd46f19289743d98703ba83311c2214184834`  
		Last Modified: Mon, 17 Mar 2025 22:34:26 GMT  
		Size: 46.1 MB (46065424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a540c8b69cf893a7a0a6c436d4761b79fd51f1845aa5b66555a58dc019b8cea8`  
		Last Modified: Mon, 17 Mar 2025 23:27:02 GMT  
		Size: 25.6 MB (25578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791930e93dca7c6cd366e9acff8ae855c1dbb03f800b05d14c315a184e79b1fc`  
		Last Modified: Tue, 18 Mar 2025 00:21:17 GMT  
		Size: 66.3 MB (66332717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bee6af81504056f12961596102f869d3f5c5cc8a22c7a13f246fba2aaf0a1284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7584412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57479b1c3e713b222b3bd491aa001ed50cdd08899e6860fa8f3cc5b055fa6a7`

```dockerfile
```

-	Layers:
	-	`sha256:716a564ea8e08d2a9d7515ef8675a230a8819d10a944127123fd541317d9e0b5`  
		Last Modified: Tue, 18 Mar 2025 00:21:09 GMT  
		Size: 7.6 MB (7577083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2270cf11b16d82d7798dd98cedf54471223d106a533c4ed8e0aa946ce2e3d1b5`  
		Last Modified: Tue, 18 Mar 2025 00:21:07 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d54984cd29e40cb6efb0ec71ecbdd6f5c5c37ac1e2f3f1404afd02413f268172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143092428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a0f102b754de476a80f9982e445eafb2b4d99fe325bb16081804c3289cfbd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:18840c5918002e02a891410ac8cb796ccc166700f997d1063ab46da46dc721f8`  
		Last Modified: Mon, 17 Mar 2025 22:42:36 GMT  
		Size: 47.6 MB (47571368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d448240a5617efe437620dbc6c199b4b34036766dc8ba22365b81ef5e32d08`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 27.4 MB (27402692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e745d023c42b8954a78b55b72c865750f57f9ee36521990f6f841b155c5ea`  
		Last Modified: Tue, 18 Mar 2025 05:56:55 GMT  
		Size: 68.1 MB (68118368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a99534960cc6471e52818fcfb7e2241ac2e4f373d50f904b5c9cdb203c896561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7583324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f06996a7424526efb2bead9dab512bd063ea2edce3d098ecd039982c724417b`

```dockerfile
```

-	Layers:
	-	`sha256:1476c8557ee496cf4107184e6ddfb8e2409a176b6aff9e08e02783b4bc0022aa`  
		Last Modified: Tue, 18 Mar 2025 05:56:54 GMT  
		Size: 7.6 MB (7576028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4b62b6df2696f5eb812954216e52b074e10c19838990566b83ebf739706170`  
		Last Modified: Tue, 18 Mar 2025 05:56:54 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json
