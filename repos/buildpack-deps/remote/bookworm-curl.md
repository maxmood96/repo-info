## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:ac3d92624e2ac5dd611fdae34a2db444f6d659d5cba511ba9ec36b4bdd971409
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:019754b6772aa831b51b71eb9cc893dec19bb1ccdddba7968ab77c75cbb27d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72530862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ea9b9744ea9095e647f8785881c26403877d2b2f41571daa21364d730e1813`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa7639c7ca20865bb3a70bd86db98f164cb1fcd471feef4eb365cd09c42419c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbd022d66e66ae51c3306de89248df4b03dba880ec218c14e5355926798db9`

```dockerfile
```

-	Layers:
	-	`sha256:a46cddaee8b107ca66c8d9dc25feb5b66d37fe81f277a77d98d535450d919bed`  
		Last Modified: Wed, 22 Apr 2026 05:01:06 GMT  
		Size: 4.5 MB (4514334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ef14e1babe048ed256b6b84eb7af5ab9069fc524afe0be24d1f1f882bd0b62`  
		Last Modified: Wed, 22 Apr 2026 05:01:05 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5cd858a0de9573f6f0236b0d45f54c49e6ce2f3f57951948b8aea53796fd58a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68737944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cfa28047890ba5fc7b74d1ca559f562df92de8cdea372ca84dac3c0fb658f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:16:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4c47739de5592cd0e20e88645e3c951f4f15c777c5919d72ffd47300390dc284`  
		Last Modified: Wed, 22 Apr 2026 00:15:32 GMT  
		Size: 46.0 MB (46021502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c7875a3d22c687eb5bf820de1b373b9b156f8c8be64706cf9bd3621ed23fd9`  
		Last Modified: Wed, 22 Apr 2026 02:17:06 GMT  
		Size: 22.7 MB (22716442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:137aa4354f7c698faa131489f41c84a12da96609b4fcc50756f80f851afe6ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7c4f38486ca0c6d336f3702e0c7a0c20d575b54b742761e1e4c739270184fb`

```dockerfile
```

-	Layers:
	-	`sha256:e1b790358799046ab9bec42194f983d01a2fe39aff9f0c8b070845634545617b`  
		Last Modified: Wed, 22 Apr 2026 02:17:06 GMT  
		Size: 4.5 MB (4518150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b57fad9aee4c9dd661465a3bf955dc84a0913396ed19ad7417416567b7527a9`  
		Last Modified: Wed, 22 Apr 2026 02:17:06 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:75b82df83fdc301f0382f24ec63b03385d697bc04965a482ef6d52dc4fa630de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66153995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e4a065a25d2468c7d593558686d7af1bcc528e9bd65475bb1f3a728a742869`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a78e7b2123c5c35e65ee1cc17df0d11c1db8ab3c4fe80b457270c2d9ae5003b1`  
		Last Modified: Wed, 22 Apr 2026 00:16:29 GMT  
		Size: 44.2 MB (44207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218160481dc948cfbf943718a4363de6a3663997f19a965c7b86136ac3e28f30`  
		Last Modified: Wed, 22 Apr 2026 02:18:15 GMT  
		Size: 21.9 MB (21946340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:37b81509725954abc62dadf0563132020da2b226a8e6d8726039793c5b828303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240beceb031192c68028077e138831ec70e548c55c4b37b2a08fc843ee2d2a09`

```dockerfile
```

-	Layers:
	-	`sha256:4f9722a35424077a8395b7f9fcf41f1be0265df258323e27280514c7d31ae787`  
		Last Modified: Wed, 22 Apr 2026 02:18:14 GMT  
		Size: 4.5 MB (4516623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b19cc59db80d51b09276485aa258a493f65633779dcbd37f035cb1dde3471e8`  
		Last Modified: Wed, 22 Apr 2026 02:18:14 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:65a01ac71df874de734395caf1ed84560884dccf6d13922133f22c7e00e39b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71982507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90242a192312af09a4141db9817ed4990b69d8a3b9074203f730ac46f19b997d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86a101a77c4549a60366efb42ff9575ed7f2873607d267e49b770c7d2ee37684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60ad0d7cce4d7cbd1533a7281e6d172e20a0138cb88428c942f7057e422e954`

```dockerfile
```

-	Layers:
	-	`sha256:aa72194d626c00a07438f8e8cdef39ea13d7e17c5506e9eb0e85dfd50203c6ea`  
		Last Modified: Fri, 08 May 2026 19:42:29 GMT  
		Size: 4.5 MB (4514595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:358edf62aa24a344b295fe51d05f6eb3e6e3249a31a19199b5ca805ef8db7ea7`  
		Last Modified: Fri, 08 May 2026 19:42:29 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fe4ee3c40b5e6bc40ac6ed028f22078417bd4d61db03c79ad4138968ceb2dd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74353441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659cfc1a94df4490bd131c27a3f65e3c0d07b6cd58f8c68095b12384ce563bd3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d771f6f5a1356deff0c1540de8894e5249a2f8c97ba7961a41235129f48c60`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 24.9 MB (24875723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a1f57eab683826de3b2015e67e8ab4d3da67111ae0367f8d9d1af2c99cefb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3315247ef5dc4086b4af99ca0dc0abfe7dee74b6967f2c7019002fcc2f885aa`

```dockerfile
```

-	Layers:
	-	`sha256:ebec7a961a8af09454d8d5bcfb313aab8b20e698609631b6556b1a5eab7e16fc`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 4.5 MB (4511453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:487f9523877de50faad8dfbef42a1d4770cf46c93d74ef0f379b3bbf9817c4f9`  
		Last Modified: Wed, 22 Apr 2026 01:42:30 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:86263a018b3e1c8c80bde40dc2b71976396c985fcb8aad5e74fc41167f2f691b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72398051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2252ef3d542b153037ed91b5f1a2f382de3981d6a3c91f0bfd3738ace5dd457e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 13:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d3be957b775aeb19be93537211a85a2a31f49a07f3bbc6044dcea43e1c8ad87b`  
		Last Modified: Wed, 22 Apr 2026 01:25:51 GMT  
		Size: 48.8 MB (48782445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689fafc394c7107b6f97558e80faf7c6aa5a2d625bf130259c59cbe1f85ed9fb`  
		Last Modified: Wed, 22 Apr 2026 13:39:30 GMT  
		Size: 23.6 MB (23615606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2eaec6b18a82247f41b6dddb8000dd9a77ef58baad933d664024ba7845adb58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f866043b5532623328216dcfd16cda65be540fee486ed8efc7b5edb07d08e65`

```dockerfile
```

-	Layers:
	-	`sha256:e40cb019248b51a5ed9a4cfbb7656295dec87f57f783541bdbb5358b61353ce1`  
		Last Modified: Wed, 22 Apr 2026 13:39:28 GMT  
		Size: 6.7 KB (6650 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5284ad77eeaf94c1754e9582c346a7f0fd94ef1eff608c1c8fbf63e1a58bd00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78016104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfc275c455fe8d76a1f4a70a78493943950bb07e0da3510072fb1845fb74cd1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:38:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c150273f4a5b502fcc97d9a922e79c7bc7d5035fb9eb1142f5adfbcea709a1`  
		Last Modified: Wed, 22 Apr 2026 03:39:23 GMT  
		Size: 25.7 MB (25679369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65b4b493932bc15928162e69702626e3488737fcd60cde0325a4ac892ea3d1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072d777d09a66b19aaa8d70fa0b0eb99c39eccc6391859a2282eddfe69f3afe7`

```dockerfile
```

-	Layers:
	-	`sha256:c1fb41e304d253ec618fe547d36044a510da4f48f72aa8b4752b6ee797769896`  
		Last Modified: Wed, 22 Apr 2026 03:39:22 GMT  
		Size: 4.5 MB (4518960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19dbefd38b8973b1ae9a8c6b426c08bdb8261f9579842cb8dc51166874571f9d`  
		Last Modified: Wed, 22 Apr 2026 03:39:22 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:57fc1f40dde83132ce4676a662aeb225c62de7889da5e47c789e2e4df7535d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71184333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07695240a43dcef4f344e886dfc6d0652eb0cce368ae4254baf5fc72ad9c1910`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac385f32c2d6e9209dd9f8ada378863aba00921ac3815f399e84f802ea5ce36e`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 24.0 MB (24036363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2f82309e4ab8bde3a48f512099a19ae298f27b4c2b30af1f3c83fc1bddf23a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093420b226a3827a6617cc61d00d5c5cb000c33169ce73ad460ab07b15177123`

```dockerfile
```

-	Layers:
	-	`sha256:85a33c90c8eb30dff9381213a1db3e2bab4c99a1d4aa3b0e3f9584f3c6339114`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aed1fc73ae6f9fb6635ada6bd54b4938d11c070e91a4c327fb2e1895a5a3980`  
		Last Modified: Wed, 22 Apr 2026 02:32:02 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
