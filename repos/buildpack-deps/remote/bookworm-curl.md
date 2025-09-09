## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:1e794871fdf63f180f560361bc51770f18bb90cddea344be0c1e53fbe7b8c0e8
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
$ docker pull buildpack-deps@sha256:0f66c5e288d9df084adeb860ac1b30259a14531df76d40c71d27dab7d3229203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72506606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce08901097d10e3b76414ec785977a100362baa5877b6fbd5e66081cc86d14`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:784afa291fdf2f6fb180a1ee20a7335c75d1e828b7cfb6bbacf0a11545863fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d121ff53e06440348994ca46ff75d9603e781325ef9d399947ee4a76e1f5d16`

```dockerfile
```

-	Layers:
	-	`sha256:e16b5a13b9f15db58b607e5bdfc96252f1efc321f3c276c30ba810895bd4fb2e`  
		Last Modified: Mon, 08 Sep 2025 22:19:43 GMT  
		Size: 4.5 MB (4513691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ebbf374ab4ca19ba7065b3ce2fa63ada96c3d2d691afae84976046bd1942c`  
		Last Modified: Mon, 08 Sep 2025 22:19:44 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7780129cf6798141f43b8785df367d7bc5427ea3efce8fa482f6be63d431aba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68718187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5c2307c6e872956566579dfb73f59d516a577f01a0cbc98559a1ac9a253ad4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb78550743da54c438514c9643e672e9378df901e1cdbedec41078f3c369313d`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 46.0 MB (46015690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021282bc493daf4a7f690f4c5ff13dd6b9ca0b3670be69b20780afc009b935a3`  
		Last Modified: Tue, 09 Sep 2025 01:31:45 GMT  
		Size: 22.7 MB (22702497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:893b8a67dcc0b29b006b38ed4bb5a6d9d307d5c1c25b7186df495a765ade34b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6cf04ac81b73f3309a5c7868e099faafe5e8b26fe2b7e2b04a1167912568c3`

```dockerfile
```

-	Layers:
	-	`sha256:3026393e895c81cc230de68de39ac982c05a33550ca658f738a48580a2fe804c`  
		Last Modified: Mon, 08 Sep 2025 22:19:49 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8acd60b8a70d0e5b6cddb57a68b515b18580d56cae89e7c0e81ef6908d95d98`  
		Last Modified: Mon, 08 Sep 2025 22:19:50 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:65138c5d1f551fe99caab2bb3d6a0548701a3538f7379630225c2c0d0324ffc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66127077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad3ef1fbfa9447d331eb79a039f74d9c1c65bffa40d51a959248331389160ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74366a34b72e71e782e589cd3e3680ae0c110755a3a8e744f1f950929ed9d4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbe6176d9c7207a738241005f1869067a40aff8a06707e84b26bd85f832539f`

```dockerfile
```

-	Layers:
	-	`sha256:d4ebc0220fe7ac1c566f189805eb6df80dd6cc97dc17f0daf9f7487a46c44ef7`  
		Last Modified: Mon, 08 Sep 2025 22:19:55 GMT  
		Size: 4.5 MB (4515980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23873d23150a5bb3d6918269e50afdcb204fc4de1327bdf3562900bb13ef8755`  
		Last Modified: Mon, 08 Sep 2025 22:19:56 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a04bdaa87d1e0d2ae2eaa2f3eebacc95e484e6e05f2dd5bac1346d3f1ff8735c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71953808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa08eea578bd445e023db58556032d94b57d5c3d9ed16e5101470687668ec77b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:95ee9f25ba9b0f25eb2307bed9a566c983f4b6fe4d3c5b99edc6261b76d4c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed0764e7e5890cc34051af2033cc4bab92883dac973430a1bf9cf0cc23991db`

```dockerfile
```

-	Layers:
	-	`sha256:4e9125a3c09617de10d3e7c3edf54af83dab929a6830b6448a160f724f3800e5`  
		Last Modified: Mon, 08 Sep 2025 22:20:01 GMT  
		Size: 4.5 MB (4513952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00dce961b2b2ac3ea2e3fab737b76ccd43de2e385dd6af584fb5c4b1241d5034`  
		Last Modified: Mon, 08 Sep 2025 22:20:02 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d1c56c3d826e42a9ca2203d2731984d2f7dd2b5f95b1639c63336b1588ffbedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74327342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3516b906c762d89624baf14b09078e599323790d3c3ad0bd5919255442eb7a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822d7073f1bfbc05d754234ff0c82bf81a44dcb6b19979f28688d3054a71fa6a`  
		Last Modified: Mon, 08 Sep 2025 22:07:56 GMT  
		Size: 24.9 MB (24860658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4f65327290105dba746fe7f63fb2aa5a23c762aa6fc6e7911dd09f557d457d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae6862b319c1ca3864c46b0ee3b45f0115fe0587cde0560fe4cbb63f01d6669`

```dockerfile
```

-	Layers:
	-	`sha256:8a93d0acdd7190a54e8ec30c7191cac0208c7e27b9317e7f425e43e115ec39b6`  
		Last Modified: Mon, 08 Sep 2025 22:20:07 GMT  
		Size: 4.5 MB (4510811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e423bb3a7fcd8bdf6bf61008eb48834c3f7f08b2189b17064e039391b40bc47`  
		Last Modified: Mon, 08 Sep 2025 22:20:08 GMT  
		Size: 6.8 KB (6838 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:145def6101dce60b4b8542c92b247e77940d6d51a4cc5633accf18775dbad169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72372167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6912ea2138c53e126b244ae7392e835c863e877777a8c5b53acc36af282fd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:32b0a76df497911c1adc85f7748d78b916d66733f6d0c87cdc6e9eb06317a625`  
		Last Modified: Mon, 08 Sep 2025 21:14:25 GMT  
		Size: 48.8 MB (48760780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4b1410ff953e9baafd271cda9e27ee11dab33c7404024b5d7f0a941e7606c4`  
		Last Modified: Tue, 09 Sep 2025 04:22:26 GMT  
		Size: 23.6 MB (23611387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75122d6a99d204246447a6fce878a8d2e093b89dfe4bef1a89b95abc53fe4dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67662f2c65f826ccafb7fe6d82cae72445b3f077371a107a820887fd4c8999a6`

```dockerfile
```

-	Layers:
	-	`sha256:2068b862d9803d736fe3b60f24027a6049f00a366dd31fce6a6928fe2771ecf5`  
		Last Modified: Tue, 09 Sep 2025 04:19:56 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:498604d142111529c4ff2769ecb7a0d50bf72afd2ad66cfc6e5a85f9676c1f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77995802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330d4b358f8e9ac83162dc30ed41622e256ed6c43911998d02568dc1d0b932e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b92467bcafecf194d3c4efbee466dcb9b2010a0899f7d2b928f9afed69de0`  
		Last Modified: Tue, 09 Sep 2025 04:47:21 GMT  
		Size: 25.7 MB (25668980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e2631dffbc244ca3d2bc7f446ee4e2cede827eead3375b7ac2ff7c6d59e0d4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdae484b84a8fce837291880db9656dd203a093690962c64500a05219d256b11`

```dockerfile
```

-	Layers:
	-	`sha256:3d2c947a71784d237f0c2286b3c090eaee9f8be32033b29fdf123aed10894344`  
		Last Modified: Tue, 09 Sep 2025 04:19:59 GMT  
		Size: 4.5 MB (4518315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3583c77dbc3ae486d9d934cb8d060d7c2282c6e0cd216fb949dbd6a6648880`  
		Last Modified: Tue, 09 Sep 2025 04:20:00 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fcf0652fb2b608adff09d5ac5906fcb26019115c7661e2c30a88d16392708d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71161404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590cadd464416701e448cc583c84df8517f3c6b037f4ac146014dd4e5707049f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f0c679ec7b70d7fa5065a6e28276437547a7d43502b4e016c2e85aed8c84c`  
		Last Modified: Tue, 09 Sep 2025 01:20:52 GMT  
		Size: 24.0 MB (24023865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:96a1986005d7790f02689ed73384915e6d0df4c4be366d65388601243b5d6e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdef802df8750fc4c0f6bda38bc0b6948fb815eee7c1b4de999b51880bd2d2f2`

```dockerfile
```

-	Layers:
	-	`sha256:978251e77df51bd5508fe9b3787ce38f46f977634d53c9fa0969965a8b96efab`  
		Last Modified: Tue, 09 Sep 2025 01:20:01 GMT  
		Size: 4.5 MB (4510495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d977c820adbd75ddb89ed3026ced13a2b1a7ebc55f9db2c076bb0f4cb473bdc`  
		Last Modified: Tue, 09 Sep 2025 01:20:02 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json
