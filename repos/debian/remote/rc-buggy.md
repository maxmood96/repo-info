## `debian:rc-buggy`

```console
$ docker pull debian@sha256:976b9754b3fdab5ebff306fe91e7a85e54c98f4239d05a7c252d4d0aa52e59e9
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
$ docker pull debian@sha256:5393b515421059820fe35d5cb2c384d4b6c9b8112c788c0e1d72325156536357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48778605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09227f5245264568c5c3c9e21101d7528776e0b7d550fe336b9d3893363e4fe3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:15:51 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:28b937e10116ada256c357287a871c307568d210af49526b0b54d19c0dcdf5da`  
		Last Modified: Wed, 24 Jun 2026 00:28:07 GMT  
		Size: 48.8 MB (48778379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d1d380b011318f84343d0253746c7407a1751302997bb734f5fceabb827b4b`  
		Last Modified: Wed, 24 Jun 2026 01:15:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:3b6d88c8e71c2fb9f968014562ce866a3ea27efba676f20b47d90fe2d9d01268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af40fad897d9f35c16b0059142da8013dd860326f618cf80a0cd4a86cb93375e`

```dockerfile
```

-	Layers:
	-	`sha256:dacefd0ab6ad5824e0c81b8c5bd3ba6fd560776e43bad8d4b49bb1337063c715`  
		Last Modified: Wed, 24 Jun 2026 01:15:58 GMT  
		Size: 3.2 MB (3151650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6404e5b8615564160bc02530ebae550bef2be40cfc2bbd9883dbed24a491bc89`  
		Last Modified: Wed, 24 Jun 2026 01:15:57 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:619b2d39bddeaf9940a121aacce17162d3d979a6d53c8d367ab93ed52917d7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45678858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c216e2a44c4aa771affdd522c1170b23abaed6f7fa4e0630fb7aa40bc0c7cb7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:15:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d675c589a8a116f3580b1211f18fa575a815f4d2314413ec9c2112d3a61d24a6`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 45.7 MB (45678632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d828da2b6c9d23be4dbde744cfec2f2e8c94f3341e2275f005a83d0a6c75e14c`  
		Last Modified: Wed, 24 Jun 2026 01:16:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:7f0751d9d48750b0e0543af8bebc7f7f62da05b07b80fe3239ac115c52cdca28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc10bad90df478fe318b4dcde1713bb9d7759c3ccff2a81c176c04abdcfdcdf`

```dockerfile
```

-	Layers:
	-	`sha256:4be82d6aade8dd45a6de1ed797f4ada565531da41ce4b982fd663d523cf6bb94`  
		Last Modified: Wed, 24 Jun 2026 01:16:02 GMT  
		Size: 3.2 MB (3153020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc059bf579e6ba8e42e8d4f2094f9de827c9ad910d07a6a4669038e7ee05f56`  
		Last Modified: Wed, 24 Jun 2026 01:16:02 GMT  
		Size: 6.1 KB (6120 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:20ce11137c2296476c1613314b2d02b95549d4e07a2db4d35f3c2174f5797540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48799060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2513998e1de4fc302c22a6b238f031cc60dc0893bf27c4d1a9809752157d3b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:14:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:4fddf52615bf1690082a9d73cb8346614997b5b51315236c93a190fbd50fb899`  
		Last Modified: Wed, 24 Jun 2026 00:28:05 GMT  
		Size: 48.8 MB (48798835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f750af72784af70bd79ac0ae9394f2fcd0f1ff6da11258557d8b8e73098a3b20`  
		Last Modified: Wed, 24 Jun 2026 01:14:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:5f7456b2b811fddc4342ce59d98831ec93c68e7e6890e031ba82c76c339c56cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3162468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f39786ab40bbe44b0923c7050ba5ed32b9087ed4e91cd560283ac3607d9e441`

```dockerfile
```

-	Layers:
	-	`sha256:1270d4aba6627c24c9a5ea29deb0c1903cdc8f0b8512d62eba7a5e08bc4332fb`  
		Last Modified: Wed, 24 Jun 2026 01:14:53 GMT  
		Size: 3.2 MB (3156332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6534fca252f6571eb2ed32e01a43d55c91c84828dc23366565bdb9bbc4cdcc85`  
		Last Modified: Wed, 24 Jun 2026 01:14:53 GMT  
		Size: 6.1 KB (6136 bytes)  
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
$ docker pull debian@sha256:efa5a58c6fbbcb2856a859551c732fd1051141987461ce93c714c70c6cdf42cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46898476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3d9eb4bed44ce8e9cbc8c8ecf7a5d35ef01a7c2f34366c082f2a4ea86a5e76`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 18:41:39 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e8bae1b6870c9b437f01d25a862e15ba295e7a79fd96767c6645eb7fdef5abfe`  
		Last Modified: Wed, 24 Jun 2026 03:29:21 GMT  
		Size: 46.9 MB (46898250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbdab165bf4d31a29402c157cf1da64e6537efc61be831199262cbc78a7994d`  
		Last Modified: Wed, 24 Jun 2026 18:42:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:d0f2c8c9bb5a37fab5201bb97012ac93acd41c768ea9ea2f21b2b17be6031f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e87060d2e9918c875db401fa3703a0e1c3c736df63bad9375a86ab946e5a49`

```dockerfile
```

-	Layers:
	-	`sha256:ea6673b1e36e7a217d9d848b9279ab8b267d2ac5bb38c56e668200017940fd3b`  
		Last Modified: Wed, 24 Jun 2026 18:42:36 GMT  
		Size: 3.1 MB (3143156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093b8214194d25a68b7231b37102e66942235bf805fded5e2c75218c5101ae33`  
		Last Modified: Wed, 24 Jun 2026 18:42:35 GMT  
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
