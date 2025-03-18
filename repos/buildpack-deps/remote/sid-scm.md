## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:39dd6c40a60b3098e77e77bc44259b8f7cb351765c2f88621a9f33d02803e7c1
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

### `buildpack-deps:sid-scm` - linux; amd64

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; arm variant v5

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a85c1ffd9ba5233c0913fbef21088e079ddf62b4245d5ba8ab0f9311882669f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130591211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0361c5edbea29b43986f7743904d07395aa3e4da11ad63db786120f127391aac`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3b9b505d2f2f0a849a74a095acfe5025f5d72fb01d82d04f1365cd960707119a`  
		Last Modified: Tue, 25 Feb 2025 01:32:18 GMT  
		Size: 43.9 MB (43880302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd562fc242f36f82e6cc8e66ce3b8e9aacffd6f2c454b8c1521cbb050ded690`  
		Last Modified: Tue, 25 Feb 2025 07:17:52 GMT  
		Size: 24.1 MB (24088476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720f19655c88ddc6bc9f7163357a30ca6c32e0e8136a77199ab4041d2b3ad565`  
		Last Modified: Tue, 25 Feb 2025 14:19:56 GMT  
		Size: 62.6 MB (62622433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7b94ccb6f92de9ee3c1551b80d979f1b68e1ac33edac14942bdf280803e3ec8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7588001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2770fa7ae24b9794361c215ad438fad034eeeebad24b5981295f0ad29155e77`

```dockerfile
```

-	Layers:
	-	`sha256:e08fc4317dfdca4d555739dd3ce833d45831c14dbc9c0e3abee6407d38c08d6b`  
		Last Modified: Tue, 25 Feb 2025 14:19:55 GMT  
		Size: 7.6 MB (7580644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5a2c137a9019449a6c9516092798756b8befbb29de8bcca75b9d7cb4960948c`  
		Last Modified: Tue, 25 Feb 2025 14:19:54 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e66e0efb5ab950474bdc7edcac8baec75a6c1cf1ab504bad4e27536d53a9ace8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141029299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6b9e4817a922046008f5ab7a5f636d4a60b7fb50ec4f650ca5dd86d0932ed1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:82dee3ca1e84a7a17d41ea99cc856a25e454e910360ce904862612b751069507`  
		Last Modified: Tue, 25 Feb 2025 01:32:16 GMT  
		Size: 47.8 MB (47842599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fdaf1ee62a1e8985dc4f6dd94f1ef4b21fdb86969059a5e1bf8b87bfc3b6ca`  
		Last Modified: Tue, 25 Feb 2025 05:42:44 GMT  
		Size: 25.7 MB (25656066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b361fcdee5d50fc8a582c25e48726784dea4601570e0bb7149e796c01faa8`  
		Last Modified: Tue, 25 Feb 2025 11:55:29 GMT  
		Size: 67.5 MB (67530634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb79c4e7d46447b9a50666558bf7bef8131d7cc7866856c9ba77e946c124ee55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7595812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a47fa00c3d6b949a6ce78b81f7a35be0d8012789a840d35b4dccedf89ebce62`

```dockerfile
```

-	Layers:
	-	`sha256:860d524a54b81e777ee29ab4ce79a0d477a50845ca240e0983f69e61a99fcb31`  
		Last Modified: Tue, 25 Feb 2025 11:55:28 GMT  
		Size: 7.6 MB (7588435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95bd47068bed70c6ce53f324f3e9695cb0bbd2052a56e95fa779112f4960bc3c`  
		Last Modified: Tue, 25 Feb 2025 11:55:27 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; mips64le

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d97932300293bcb2f826c89ac845d33a5dc076d30366ef41029d561ad08d6c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151707545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b570b1552d82eb1313d8f9cf0c5b012eb14aafcb2749f3a019ac353c91728976`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9370c4ccc640520942cbaafa9d1bba72d3a14bc22c93d4c585e6cf8f83d65274`  
		Last Modified: Tue, 25 Feb 2025 01:31:22 GMT  
		Size: 51.1 MB (51109956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a14d42f5e429844e608bdea207bfc8db8bb3a74d08ade67bcacfe19c5fbf8`  
		Last Modified: Tue, 25 Feb 2025 04:33:25 GMT  
		Size: 27.7 MB (27746070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7aaea582b8b7ff6324c9b146d200160cd89f84b7db9c384d8893b333eac8a62`  
		Last Modified: Tue, 25 Feb 2025 08:21:01 GMT  
		Size: 72.9 MB (72851519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:477d22810d6674d2faaa34748543a23b4fb9517bd2e31cc220ded65fd3b4cc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7600644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa98aba4c18f6f4bb36fae47a274a650f430f8b874ba475ab471598e7981b8a`

```dockerfile
```

-	Layers:
	-	`sha256:17d298c6da21b5a0fa98eb051cf81f672549a34fa4da447cdc15012fd0ff53ef`  
		Last Modified: Tue, 25 Feb 2025 08:20:59 GMT  
		Size: 7.6 MB (7593315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11fe8f77672b8710d25cfb8abcb6d43b65e94230c53520bdd2179418650b9809`  
		Last Modified: Tue, 25 Feb 2025 08:20:58 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; s390x

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

### `buildpack-deps:sid-scm` - unknown; unknown

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
