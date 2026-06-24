## `debian:rc-buggy`

```console
$ docker pull debian@sha256:12a99a2f44fdf023210c58d1157e8882184989d299950d9bc5f5ddc61f024de3
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:575a976e47dc70ad8866ed5a4c225308ee032ac3009da1b93a19710d668d1247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48801437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74c2d3e585daa3916050faf0c65b0e111f35eda28f44e08d4fcd8bd6e3ad8df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:16:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e4bfb5fe24dc0230d4f97c7feccc03abb781a438997364a53c10057b40c735`  
		Last Modified: Thu, 11 Jun 2026 00:16:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:eff2c7644bfdf6cb1ad3e1299c5590bceb12b192c00c7c627942b7550f9541bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591ce2b94d3a56b142e034a1fba2cab9aed79273a455fa2c49a2200573cf4a0b`

```dockerfile
```

-	Layers:
	-	`sha256:6a610bf347b5c0fd8e70a86a159c3f77565db14432d26cde08ff383c5873d56c`  
		Last Modified: Thu, 11 Jun 2026 00:16:20 GMT  
		Size: 3.2 MB (3153477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8063c8e208576ff5f98486ef6b59ebae8888eaba8c1e635258165c99180e77a`  
		Last Modified: Thu, 11 Jun 2026 00:16:20 GMT  
		Size: 6.1 KB (6055 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:64b80277b3be0a923b2b9a2b92b65542f774db9dfe75ad7d8cd7f4aa8e8af598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45703465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a236065e56bba9dd93ed63e18cf618679dfd9f08a71d1a427bf68b50088e8dc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:16:04 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6dddbc4e0b590efd809489171b20c0c05ae23facbf49b0dac491dc8f542364ec`  
		Last Modified: Wed, 10 Jun 2026 23:42:26 GMT  
		Size: 45.7 MB (45703240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f48a3dbdc2a4dd43b6c0aa0290d531f0398ce02b5bae36e8beaad10663c428f`  
		Last Modified: Thu, 11 Jun 2026 00:16:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:1cd801e24dfb159ace5af159cb5dcf51a52a7af905c4957fc0dd9da7dad4134a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f1729c403d0c9572fafa098268b22b2ac23725488f0baf01a06e911976a17`

```dockerfile
```

-	Layers:
	-	`sha256:1cc6306a69eadf77ca9589d6f0ede44db01716629bee6d045d2805e7c69b75b2`  
		Last Modified: Thu, 11 Jun 2026 00:16:10 GMT  
		Size: 3.2 MB (3154847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc778f0387cd671e42a633a217ac3356fbf932e6b589e58b5b30e2299c1f6d14`  
		Last Modified: Thu, 11 Jun 2026 00:16:10 GMT  
		Size: 6.1 KB (6117 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:febc13602ee3ee825613224c7fc545ac8b216c063ae647f155f22f2e47c2488f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48818782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce93c81d966df9c90aec6a680b0b7df2f0945cdfa16f0d0d71285c24da96813f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:15:31 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6690e347586746af2bdedf6049221922a991b4799733e8eae40a661a548a49`  
		Last Modified: Thu, 11 Jun 2026 00:15:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:9c1dcd0817f2034813731d24c8ec3c81f057f41eb65b7a2cbb4ccbb1022cc2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b29fccf5a8ad88d2b4bf53a36934b4718b45498e5611dda1ea8b02e640013a`

```dockerfile
```

-	Layers:
	-	`sha256:7878a17f9cae5b4d3f5839fc0e1bdccd3f5f3b533e1ed1552620c7fb8250cc9e`  
		Last Modified: Thu, 11 Jun 2026 00:15:38 GMT  
		Size: 3.2 MB (3158159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb10560c3245f4c96be27c09a42ab52d0ac6369d7033d92ed59b2b2586e4feb3`  
		Last Modified: Thu, 11 Jun 2026 00:15:38 GMT  
		Size: 6.1 KB (6135 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:9a57af613e70f86cc59a8130bb3120dabefabf0723dee17d55366666239253fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50081179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea8abaa6fe942d64d3906e94c7ad1049ce87be52cd11c7b4af903282458a276`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:15:01 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:466f7f9acdfac81cb720fa13d53a50111bee95182357f963947200187b3ae3fe`  
		Last Modified: Wed, 24 Jun 2026 00:28:18 GMT  
		Size: 50.1 MB (50080955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e407e1ae81a10142b3ea248f9b1c73fb16de231a62d22cb2f2952c3c564189ef`  
		Last Modified: Wed, 24 Jun 2026 01:15:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:b037044a99a8aa514c47db523e1b59905009770163c7782ffa8c1cb89057c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ffbf6459818f236cdf91b6e1045d100827b5c671b2300dcab22c1d0412233c`

```dockerfile
```

-	Layers:
	-	`sha256:c71459cab6d945d9912da97afcd3b3bf3d226103e23381ca641b5b5f86708dec`  
		Last Modified: Wed, 24 Jun 2026 01:15:07 GMT  
		Size: 3.1 MB (3148849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4194bf12558356b79d10461c9bce4ee36ff44d7bc9a1ee03e7353f938c8792f`  
		Last Modified: Wed, 24 Jun 2026 01:15:07 GMT  
		Size: 6.0 KB (6034 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:86cc4eab805d6c00978c8d5a8ae9bd6cb88cb5df62477908983f00cb39ee6700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54098203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1d307e7bab7324ed9dd7c0b7a64720d87f977012812a9ba217451aa880fa08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:207e1fc4a0d78092eada2cd0c9c038e7e28d176a37a4e995ec935b5f148a7e59`  
		Last Modified: Wed, 24 Jun 2026 00:29:01 GMT  
		Size: 54.1 MB (54097978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb62183ea3de24ad4477cd8e283781fdbf98dbd5b318ad99ef0c953b8871cf10`  
		Last Modified: Wed, 24 Jun 2026 01:16:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:895a89a70ae6bb8b9ba5f6977b1199e233a0230a78ac6c2a5d1808d13af6b2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503ba7ae42ff70c42b6d67d8978db7b81355a394aff9c3914d656179a1c8d08a`

```dockerfile
```

-	Layers:
	-	`sha256:fcf6e579be633f96250458a582a04510fcfdc4707fdc84ab4ba26db420eb9c06`  
		Last Modified: Wed, 24 Jun 2026 01:16:11 GMT  
		Size: 3.2 MB (3155153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6319d65245e0a5bac877815f2556c6895afe51c69fe3858a69dd1d79b787461`  
		Last Modified: Wed, 24 Jun 2026 01:16:11 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:e5f6eb1314448c2077c147cffe68b145d27c9274cc12b8886c74e681f749a75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46911860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896fef1740c899abd8d747ec75f771126d420e00e822e6d90daea8408e7417c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 22:16:15 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e2efc7e0091930e45ea6218e0e9380e67d07fe2085c100b1d3d74190636f5938`  
		Last Modified: Thu, 11 Jun 2026 02:48:51 GMT  
		Size: 46.9 MB (46911636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d977d1e4a68d70f60429fe8dd383230d0c636dd52a5157fc8e6209dd0a4c84`  
		Last Modified: Thu, 11 Jun 2026 22:17:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:d5a27b3eeeb6919c95f35b4151de5611eec48707921add2cd04fb71433915785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eece859ce3a659c67562c80712892d04610a894828b23554dd709bd0ca26ad2`

```dockerfile
```

-	Layers:
	-	`sha256:fbfc6e8b5acc0386d8788e05cdfbb807cab8ccc9ab0473b8204ba190be32ce55`  
		Last Modified: Thu, 11 Jun 2026 22:17:11 GMT  
		Size: 3.1 MB (3144989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9200b4eb3d8f736c596d413e195e634d52f8820b831bfee408344e1c3098a1b0`  
		Last Modified: Thu, 11 Jun 2026 22:17:10 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:c98830c4850fb1dcb9b156ca4fe1c7a2ba34825d161a72e48307315588a8ebc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48518022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfefa8e4bee7193ea3c149834fbfdc7355ee19e5927879959a457b68800c067b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:14:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:1e9b72b44a72df002ca2c8ad8ccb65d46205892b54ff8d9ce0b5dd7be73544fe`  
		Last Modified: Wed, 24 Jun 2026 00:27:46 GMT  
		Size: 48.5 MB (48517796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7bb484be8e85df606bd80a31148183bdbc9292b58cf585497e93f21ccd5bdb`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:a1c877a25b04acb1229806ebbc1eeba72a9d8a9927f877868dffad5eb15e6d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcc85ce17e0257341e430987a4c646de5ee0d85db2e4c801a6ff903957104e9`

```dockerfile
```

-	Layers:
	-	`sha256:93881c57340b602694b5908bcbbfff2c7819d79a06b28ac3ffe43b00ae2b461c`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 3.2 MB (3153101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41abbde934a80ecf1c39e28c72bf95bd80ab5e7362a19dff37e3678392bebe05`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 6.1 KB (6055 bytes)  
		MIME: application/vnd.in-toto+json
