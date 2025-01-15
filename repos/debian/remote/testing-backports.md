## `debian:testing-backports`

```console
$ docker pull debian@sha256:0d48a773adba354c2de18215c380d9a3098111527e0cf1a077169c340971b016
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:67e91a62585b4c19ec8c45bdf34c97f1a2c4ac6d6752bc64de52df3289d3924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48276309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23b21534a2d50f88a9a6d5445eb3d1afc68817ea6f4212551b7735bf670b429`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6b9b09e5bd5862e77d8a11756f2940766adfbf008b1b99f2e5908ebefec90b4c`  
		Last Modified: Tue, 14 Jan 2025 01:33:48 GMT  
		Size: 48.3 MB (48276087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab1b49db88848f695c71d7bfd725f124ddb230f58cda96f97647aa44cbb95e5`  
		Last Modified: Tue, 14 Jan 2025 02:15:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6bc75c7c0a16f17130e37992a4ed62356a447e6b0f5e9b4c969ee367853cb2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53347c2eb5e497130e09e61ae025044c77361724356a9d670058b3465d0ed721`

```dockerfile
```

-	Layers:
	-	`sha256:7a7910eb0c18a3edc51fd7fa18f1bb20dc1a2728b5329f760ee796642abec5a0`  
		Last Modified: Tue, 14 Jan 2025 02:15:38 GMT  
		Size: 3.1 MB (3119378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60a41a5bbe0b267721f79817a85c0e3e8a8c6a7b7e4bdb0a117ebb67b43165c2`  
		Last Modified: Tue, 14 Jan 2025 02:15:38 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2a31fd4ad576f4aa704060539fdd940d053c90d851694743c51949225a0e87bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e65c41e25a5fe5bbeda9c41bf789906103e0f0e67c47a0f83ed7d716271c1fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'testing' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5106986de9bba1ddf9fd9c3edf625eb4874a8b9d1338b03441a8adf21c06838a`  
		Last Modified: Tue, 14 Jan 2025 01:35:11 GMT  
		Size: 46.4 MB (46441715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339e9a19363b81199b5b7f2dfaa67f6374e40688f07627e74babe93c0f9d2518`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b49d8ec12a1cc1870394fec57f8483fcf32244ed58dd8b31000d61bed4ffd344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83093bc55087e193b4c9ff829ae2f4d44f5f008ea3a1d94e8eb5e32dd3acdebf`

```dockerfile
```

-	Layers:
	-	`sha256:45a3850e892b1dac1b034ec392b53f4def87953537caf50d7c07a3e211f42ef7`  
		Last Modified: Tue, 14 Jan 2025 02:16:49 GMT  
		Size: 3.1 MB (3128396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11817ffae8a685921dcf14170afb8e0024a8da380e93fffc1ba3c85149e4dea8`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5bb9255ef503a269c0df910f5ffb725070a46dcb1d56a355766c4485f6647d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44580678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c62c7e744135d11b5211968f3164ea52c3c0c27c2d80a2aea0440d57cba8c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ececcdaf6ebe11f34d3a742e6c6719e14acc21ee6bc22c9a67531097875fd23b`  
		Last Modified: Tue, 14 Jan 2025 01:38:26 GMT  
		Size: 44.6 MB (44580454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1843db943ff8248e0fdd297c605a94b024ab59aabd0e3db4735df30110db46b`  
		Last Modified: Tue, 14 Jan 2025 02:18:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8a29a197ec0358be783856a5e74acdbe14e158fb35307a129c60b731942bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3126803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d608d22a9dae58419835e67d66767bbb6bb01c1df3cdf157cf9a759047be50`

```dockerfile
```

-	Layers:
	-	`sha256:968b48520a42c21a331044ddbdfd06f281c55cbd7bc79cac3c36b87977a39e37`  
		Last Modified: Tue, 14 Jan 2025 02:18:45 GMT  
		Size: 3.1 MB (3120914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b595ffa455154922cced016fa1dfd3b9781215ecbeb06a56588761ec9f013cb9`  
		Last Modified: Tue, 14 Jan 2025 02:18:45 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cf50dda843950bcfb6e3048fdab9f25f1ae5fb8f168c2f6b802ca3551f992600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48661725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7353fdba615c50f2510c18389792d8278b8527f4dc6c0085369b0f9cf7d8b29`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:815bead3f6991928b64cef505ed69cbd5a441a6bd7c3256bb2cb7ef03b7997c1`  
		Last Modified: Tue, 14 Jan 2025 20:50:13 GMT  
		Size: 48.7 MB (48661504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e4df4b58f5821b3cfe0b937877a3da695952e24175963380c27ecb0c964cd8`  
		Last Modified: Tue, 14 Jan 2025 22:04:49 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a818e790a59dce0075283f8a75987d631e1837c80e8f831b792c3d1f605d41de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a571fe095803b331269f33a5114028d1ae191cff6e18a3e3b1116977318ee`

```dockerfile
```

-	Layers:
	-	`sha256:a9d88f165072bccdbec7a6bdda5f3c2faffa1b7c6cb7b0036c5df62423eefab4`  
		Last Modified: Tue, 14 Jan 2025 02:23:56 GMT  
		Size: 3.1 MB (3121660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5f20e23388a0e1cb3df23c066175cf2b0d144980533edabc5fc1eb1ed55f2b6`  
		Last Modified: Tue, 14 Jan 2025 02:23:56 GMT  
		Size: 5.9 KB (5904 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:7f60eeeb38724b385c74dd87d6c01e6186291aba1ea934f66d72e8aba615c1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49675924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d74105dbd9ce8767596cbfc9400eb1c6fad7c0ced370e5c03fa0050de6fff48`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:78124e775da5335dae99432dfc19ed2b222bb6d5bae5905528d0fe513aa19d76`  
		Last Modified: Tue, 14 Jan 2025 01:33:45 GMT  
		Size: 49.7 MB (49675703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa1e7e73ed7beba43f89be2115b00b16a3f106aa013d18f244d5a674259d612`  
		Last Modified: Tue, 14 Jan 2025 02:31:22 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2f97bcc31e1246da9313add11ad34758f51dde7a663d7b5c9003ddeba9231487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3121715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f23d472038a8ee8331cfa91be5d259e79d9cbb70a647155f7daff972212ad9`

```dockerfile
```

-	Layers:
	-	`sha256:3cf8de4a1a978a75e7b826905d06be34a6d13bffe8a27656c3bd3329177ec589`  
		Last Modified: Tue, 14 Jan 2025 02:31:22 GMT  
		Size: 3.1 MB (3115895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2ca468648432b3d2d24a7eaacef5312497d031966bf22ba113ae446973973c`  
		Last Modified: Tue, 14 Jan 2025 02:31:22 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e3b60a8f1aa5b4fb446bc1b7a4cffa0a0259cb1803b9d09483738440eb34f88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48390435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c861ae1b8153de1a60b899c9481bf8ffa4f967c789ea27807e31c6f99fdbc6b9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'testing' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:71c389d75391ffed0beb698c740a3b8302a0b2993771fae29c6c7676c23db06b`  
		Last Modified: Tue, 14 Jan 2025 01:36:36 GMT  
		Size: 48.4 MB (48390214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd94c6020fadd3af300a610de292360ebcb81cc63203f2b8de32130d8bdd441`  
		Last Modified: Tue, 14 Jan 2025 02:19:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b80f8206222bbc9830efd3738b109d556622a688c707583e5c19b16928072d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437d43efe96dad4eff6778fbf8afc68d4d030ad614b7cca3e7b3b6eddf71418`

```dockerfile
```

-	Layers:
	-	`sha256:a3c27eaf8fea34fe8a8dc2bef7d1bd9262d8c0d94b782d9ae008260ac7bdd7ce`  
		Last Modified: Tue, 14 Jan 2025 02:19:11 GMT  
		Size: 5.7 KB (5660 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:644a07d18345548fc0c74ef0d7a4135f86a3b4b0822b0b0a24a8de9bb450413f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52043349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9209e01c7eff256479d1570c137c744d226f37adf074dc14f5508b0c9b09e5a0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2af2e0cc696c39045cef14b1e616df607fb1a880e337f0e0e1a99c9469aead80`  
		Last Modified: Tue, 14 Jan 2025 01:39:55 GMT  
		Size: 52.0 MB (52043128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9857c756c2fbb130ce405af1f3e4957d243faacec7b42029f04052c4868ae403`  
		Last Modified: Wed, 15 Jan 2025 06:01:06 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f517340c1506b68bbe4b5a7aa5cb57632d84e915d266aee968559204e48af814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc562db52fec5914974db60e588cbdd63e6437e1b5770e59e7fd3e04cd9aa48`

```dockerfile
```

-	Layers:
	-	`sha256:c289baa19f249e9dc6207e9ab759a4b0d51cda67659c6ddb7112bf4042e5bce5`  
		Last Modified: Wed, 15 Jan 2025 06:01:11 GMT  
		Size: 3.1 MB (3129204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:146bf14c2d4e2cc41f5c74430a79ab038984e32f8b38e83df4fd72d4e695bf55`  
		Last Modified: Tue, 14 Jan 2025 02:39:05 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:32ce297f8b133f556bae864f824d48dfd42ba361d748c153cfc6e895158e95bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46838518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee2048d903b3a3694910dfea69cb422af3dc18b5f2261cf0ca885822028b1aa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:24ee1ec916960f2cc63cf0ab20fe59b982176179c69bb91accb7fde6ebc7bb15`  
		Last Modified: Tue, 14 Jan 2025 22:19:55 GMT  
		Size: 46.8 MB (46838296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bbdf302e642c78184db8be4f11ec31512dc3b7a5431ad3f307a55cdcfd8180`  
		Last Modified: Tue, 14 Jan 2025 14:17:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cb4e89642ce1bb1bccbe6012189f2c202b5cb58705c89f28f12d165abb632988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3117944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67bf8e05474a2c55204b5942927650c2960879a992205ce25ab33d681872a9a`

```dockerfile
```

-	Layers:
	-	`sha256:8d1a5b4a9dbebc23666ef0f5274898bc2250e5fbd45fc44ef683d61706c40ca6`  
		Last Modified: Wed, 15 Jan 2025 06:01:20 GMT  
		Size: 3.1 MB (3112081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff5ad8c14b15321029c685f0f8b5142a2b32ed0a5c65e3fde16cf8f34f8966d`  
		Last Modified: Tue, 14 Jan 2025 14:17:30 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:f7c5968c19ebb8e8adc8a4601511390d8af0c08b3955c1f87432e3fc30b22e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48329958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37616af8da0f535a91c4f739ff96cb4f6a14090fc42b000ddda7a74bb9b6874`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:44a67b26070060f0727a3c7840a2ae53f8a453471c9d7bc5e966fa51b11cf84b`  
		Last Modified: Tue, 14 Jan 2025 01:37:42 GMT  
		Size: 48.3 MB (48329735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dcef7dfd2e1bcc324dda4f1a2660b64fa43d0328d703dd3dc5785de0411663`  
		Last Modified: Tue, 14 Jan 2025 02:29:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:13d4b573a322e97c91a235a30081b4d26543807ad20f235ca8cb4a979ab9e5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076eb80bbe7afd7ae762e55cd0c1361b05012c0d1221589565a6caa797bc4340`

```dockerfile
```

-	Layers:
	-	`sha256:ddb60d97517d28defb44b4c6486a9208e642e25e2373c85a6821181663e2a444`  
		Last Modified: Tue, 14 Jan 2025 02:29:30 GMT  
		Size: 3.1 MB (3127186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b47a55ff0b82958535bb28bbaf433edcb1104476ef60ef897d07d4fbfa329b17`  
		Last Modified: Tue, 14 Jan 2025 02:29:30 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json
