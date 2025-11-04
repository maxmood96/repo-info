## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:057e371bf2aa283040aaaa6d1f0e5cf3b008d8d3250cd293be7653e103cba486
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:a247bb934cd1b09311593402ed73ce99641a2d67eb10d471fb0e2f51f8efbf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2b33d072bb81dbe1ca475a6d508e951a8927cbb52d0a555ed14647152dfd98`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 04:02:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b30c56d690180db2d65d6dbb6c2a7b48742b946872654b44f34921b44b56dd9a`  
		Last Modified: Tue, 04 Nov 2025 00:13:35 GMT  
		Size: 48.5 MB (48481062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ad91ee8be7f94ea0c32ee91e9e45edf8f1769f971c1834fdf4ee11fbff6776`  
		Last Modified: Tue, 04 Nov 2025 04:02:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ae2be7be2e57e4ec4fdefab4b5cebd6258b61b78e17492435a1bc057f57bc2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94423072191559d54c67f5bee573bdba5ab289c8c3569b4fbaf1f0f0d3bb5e94`

```dockerfile
```

-	Layers:
	-	`sha256:d668bf244fe03961b6f4cf0fdd5d15589971a12d377af55421f5e6dc4a7db898`  
		Last Modified: Tue, 04 Nov 2025 10:26:52 GMT  
		Size: 3.7 MB (3733433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08499ad0cc9c6d347538a7f28d2f47c2699c67688564f13208d5cede6ecec318`  
		Last Modified: Tue, 04 Nov 2025 10:26:52 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b93fc122fd5b84ea3649774a748d4004a8e9bad4cfef0b0f89b53c0486e89f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b3cc389f519877b77de9a8137c61d8b3cd023de94398a10bc90717ac2b07e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 00:20:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ba3e984208185eebf501e446e9046cc294f49018e87c7c8b41687c210902e1a4`  
		Last Modified: Tue, 04 Nov 2025 00:12:43 GMT  
		Size: 46.0 MB (46016094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3a0419f7f98d55c4251e0b75686b8db51f0a226bfa868b4ae774d8dc3b9cec`  
		Last Modified: Tue, 04 Nov 2025 00:20:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50c228636279f79a49de2bda8dd6fa4b200a0a287e274a613d561cfee1f72a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b1295d3f401478d08cad6f4055ba1a44d4e69cd3f52864ab1600b23064b126`

```dockerfile
```

-	Layers:
	-	`sha256:9f57ebe728902dbf7403b8cbf4cbb1f47e7e0e2acafceede7aa9d0423a2635ab`  
		Last Modified: Tue, 04 Nov 2025 07:28:38 GMT  
		Size: 3.7 MB (3733634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cae2b5b79cff1a050f3e233a316dfd5249b37bb23179ba6d602ed9b3497ffba`  
		Last Modified: Tue, 04 Nov 2025 07:28:39 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:18ace577590e55064294100f5dfbd273325803e6897fa28d1bf9fa98b3f7464b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d3c5c71fa91adfa37558d4d454e2cabbfbbbe36f4a222ed29b4bb97ef512c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 02:04:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9fb1fc15c72033f73042c99f7e57a1af9f84c509bca1b3e1d2a602188264bd52`  
		Last Modified: Tue, 04 Nov 2025 00:13:32 GMT  
		Size: 44.2 MB (44196441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895b0bb0dda744ab0a7940faa2e82a1898b58a4241a805d7a4e2cc0e1dfcee7a`  
		Last Modified: Tue, 04 Nov 2025 02:04:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:31de4a288c3b5a217412103fd0bd117c28f483b537bea9267760d016d6b22fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae488aeb88eaa0aa97980350241fe292eeb2b7d6f32b99650400573d390cec3`

```dockerfile
```

-	Layers:
	-	`sha256:d9347faaeb615d6cc60bdefacd73b689d2c15f6218b5f0ff84f79dff921fbde0`  
		Last Modified: Tue, 04 Nov 2025 10:27:00 GMT  
		Size: 3.7 MB (3735612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa90bc454829dbf232317fbd80b69e6c06db0c26f55b06e1acd491486398e283`  
		Last Modified: Tue, 04 Nov 2025 10:27:01 GMT  
		Size: 5.9 KB (5865 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cce46f542d92ee386fdea9faf1279da415e35085c47d31b28453e29448bde9c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d433930239e4352684045c966b384ed069aac44b8da9db89f69205a999325c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 01:17:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b16888a33035a731f3caff6eebf95641ee255619c45e70a0af59cc7b0a583289`  
		Last Modified: Tue, 04 Nov 2025 00:14:07 GMT  
		Size: 48.4 MB (48359481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6435206efefa52b27910a6cf4d8f4f65e94793f4ac574c6b9cdc32f8c7aa604a`  
		Last Modified: Tue, 04 Nov 2025 01:18:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1e5888879263a626801c817efb855f5385ac5949ef31bf0b4960214a7656f22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dd8e6aa00e4a4394cd8fdf13a578279cfe4edd4e5597b5875694ae760e6709`

```dockerfile
```

-	Layers:
	-	`sha256:6e47c649d00ec67908da8c896ff3dee923534ca58e02be5252c142806a301357`  
		Last Modified: Tue, 04 Nov 2025 10:27:05 GMT  
		Size: 3.7 MB (3733648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4071ee16e7f97945841f502d5b2b5233b83fb37cfe26e71ac4459d8b00012683`  
		Last Modified: Tue, 04 Nov 2025 10:27:05 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:e2e88ec3d93b118b3886bed4bf534e974ef24f81a238256a52c3f3d3affbb683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc43a7387cfc0ea4dfa8c153a733b1c99016a4e7bb9bdb746c3b4b87443c958`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 01:17:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:831046d5982c331834fa6d46a8d5f04a989066a168f8f3e0b643f80f300a9e12`  
		Last Modified: Tue, 04 Nov 2025 00:15:03 GMT  
		Size: 49.5 MB (49467120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3048344e6a3ce481846078649c9443fcfab8b036860ceec67e407f7354dd74`  
		Last Modified: Tue, 04 Nov 2025 01:18:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2aeb1179d1f3f6fbb8c8018634cbd1699352b78a0d26e48b5a09d87c57e701b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1791e1f89d85bb2e946707d38137b19aec1371481e9e2844cc463c8110ec18`

```dockerfile
```

-	Layers:
	-	`sha256:ee4d97215ebddf503a981e409941bde55f3dc51c8b52b53ea3e5ffe4a9d2bc4a`  
		Last Modified: Tue, 04 Nov 2025 10:27:09 GMT  
		Size: 3.7 MB (3730630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da13e4b05cdd605b1c3476d87164de50c9d72b85c85134a16e6d3b5082136abd`  
		Last Modified: Tue, 04 Nov 2025 10:27:10 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:39f51cecbd7d51615d83c0b2aa58a5705feb523e688304cc2dfa9fa608b2bcdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4acb22665c2a6e77753700e823dc0be4033106b23ef9451c6f47d9333cdebf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 00:18:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:deb63f79a3e780f6c895b686d3acd3362fbff1594f406951d9ab487ed8966203`  
		Last Modified: Tue, 04 Nov 2025 00:12:31 GMT  
		Size: 48.8 MB (48761283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7607f678de5aefc085176faa2760356cef9a8904120c19c310a69765b6ae5`  
		Last Modified: Tue, 04 Nov 2025 00:19:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4a1f531d67d06fdffec91fb37ae5d743e61e69811de4d5309bcf211547dc9a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e717057119add05375763c2afb4512bd68e60aa901e948586c9ca7ba05811d`

```dockerfile
```

-	Layers:
	-	`sha256:5b0ca025be5499d38d98e8e1ab60ca89a37fafa81e7a5bd8affbd4a710edcbe4`  
		Last Modified: Tue, 04 Nov 2025 07:28:54 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c0138e8141995fc39089ea2473e462289df2677581a4c9e6cd88934afa871054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f26990a2a23527236f8847afd2eed7220fecc8a3af4c64ffe5bb2802256deb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 01:17:48 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7221f6a36a11611ac98f0938d5d0aec46d49d3405cf95b761704980981e9442c`  
		Last Modified: Tue, 04 Nov 2025 00:15:31 GMT  
		Size: 52.3 MB (52327281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a00f52e23fbc8dd91a77a5ab817059afac6e03c3256cbfe018d79670d7bb0f`  
		Last Modified: Tue, 04 Nov 2025 01:18:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:75490b0fb09c94053195e3241d6adb73ea4161b15bd4c0b254da71c713c8fece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91829884f7b63a335226143a33c95fd1e0b75e752ab778c48774cffb0d814dc`

```dockerfile
```

-	Layers:
	-	`sha256:05f01ff455b9f39b1f9cbec02e4f0c5fe826719d9457387c1058e3b15d6ded83`  
		Last Modified: Tue, 04 Nov 2025 10:27:16 GMT  
		Size: 3.7 MB (3737789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa687b355950f2efc5e3b43134c9a878da17414b0f95cb08b00360447b240e4a`  
		Last Modified: Tue, 04 Nov 2025 10:27:16 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:aef1b8b42295c7d0ec7d15cadd67902581ef17518202d9450f8190f5523e82e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47138325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca2506cee1ff90b2e34f38f7486602bc993b364c6239800bfa01d5b2226c8e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1762202650'
# Tue, 04 Nov 2025 06:41:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e8f1839050c18da150e6074cbca06850f889de57315d0e41ebbe09b6d09e5186`  
		Last Modified: Tue, 04 Nov 2025 00:15:16 GMT  
		Size: 47.1 MB (47138101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a0f53acecd18b5218dea37f1fd3edd4428da391f6dd7526419334da71c16f`  
		Last Modified: Tue, 04 Nov 2025 06:41:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:75f0f03015111219dbca763732d203be871ca3f3db5dca732c83bbb3f4886eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8ab2547fe7b1c7efd129a349cdded3172802e77f35e483b08b10ea4a5f13fb`

```dockerfile
```

-	Layers:
	-	`sha256:5e4d18eab8a2c31e9a4dfd67a1e8ce5d93f9d7ad43882347ef8bbe98d962c303`  
		Last Modified: Tue, 04 Nov 2025 10:27:21 GMT  
		Size: 3.7 MB (3730271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d889a14c88f3beb17cd30d6f5be362becc5191bf91ada8431765f5c9118934d`  
		Last Modified: Tue, 04 Nov 2025 10:27:21 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json
