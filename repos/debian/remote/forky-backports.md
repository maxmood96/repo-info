## `debian:forky-backports`

```console
$ docker pull debian@sha256:4858af3683704e94587eaa42bf0aa529b3426821e30f1ae79f4cbd1c7750dfe3
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

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:b5988a9ac9a2394af81ae59804a9e9606cd9cc2d4885a72e88304c21c6d3adb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cded81419612248d0fad4ad368d2806c3f2b1570e7c44a9f56ec17f16b36734e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 22:58:24 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07533996578356b026bb375d6fceb3ce1cdc6c2b5b735c2a5d98397bd873d96`  
		Last Modified: Tue, 19 May 2026 22:58:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5b703f962706657ac7a831d77e1c8ad79ad67fdaf0d9081aced85212d726690e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e3c999adc6a313ad3fb761f9686d353804767215609346cb8b4442d26a7c04`

```dockerfile
```

-	Layers:
	-	`sha256:6ab5c3638e05bfa5e6157154d8dbc0fa1474aa9524afaa27b0f97e1bc48d8a96`  
		Last Modified: Tue, 19 May 2026 22:58:30 GMT  
		Size: 3.1 MB (3146242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02f424bd06fdd1cd2389b74d1973d3625e4d4ef6ba56257b99ddd222d40ac13e`  
		Last Modified: Tue, 19 May 2026 22:58:30 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:55f234bd8a5bf9137920ca65c47b2427a5b955807cc76d98d1df029d0008c8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45603410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2953b771a0c01451ad3a171800a5da799d182d215f9f3b1057d990593843bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 22:57:08 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b6df9d4a408084133e98c8d6c8e0e3de38b9e95851bc2206e09b39135c71bba1`  
		Last Modified: Tue, 19 May 2026 22:36:31 GMT  
		Size: 45.6 MB (45603185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52a23bdd8c8f0956a0a0236bc2ef677ee3f1b7878f0814689925240b25cca82`  
		Last Modified: Tue, 19 May 2026 22:57:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c7f168832e4ad42e209ded029f4e4207a10cf133913e44a815f43bd37d4c4460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6517ff738ebcffa8e9f9c75d439f7cf1a9cbd1174cdee56c72a88d745dba1ebb`

```dockerfile
```

-	Layers:
	-	`sha256:e45bddc2d03438850e127d1167e1d6abf64909430acb44c7996c6826d03f374e`  
		Last Modified: Tue, 19 May 2026 22:57:14 GMT  
		Size: 3.1 MB (3147604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4fa09f82ddc9d516073d05ecc3c085c1301a4f72751b15e7847aceb04690b7`  
		Last Modified: Tue, 19 May 2026 22:57:14 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7f78ab9a1f853e379c4fd5744ec11d8873d56782806ad45c8f28a8ca81b6aa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48720256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef79201957f846241a13ee3c5f413a12424cfd87df027178db63f8d7a9ca975`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 22:55:45 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78168bba01acb368a73fbd82c29d6e1a7e70047994da7f180d84eec382674d3`  
		Last Modified: Tue, 19 May 2026 22:55:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:59dc9af02b621fabfabdd59aceb3aa3ae29025fd63043be57a68ca0202fe428d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8b2275545c168996e83c8c3dbdcb0870b3113940b84d5060ea789db9923103`

```dockerfile
```

-	Layers:
	-	`sha256:0e2460c18439ee4af19ae86b5d9ed86e0af8754d1512d5a650556d3d8f53ce9c`  
		Last Modified: Tue, 19 May 2026 22:55:51 GMT  
		Size: 3.2 MB (3150912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6fdca225699fd28c9e75d0704061d8b918b5105fcb15e01717111e6c70efc52`  
		Last Modified: Tue, 19 May 2026 22:55:51 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:5af52c88579bcb51a70f3c156e67a4e23b377cbfe8d78aac2bb4e8bc9472fbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad21de685fd377feb1efe7c22409846cdf1d4f7e78a79d789461fe334e9abfd9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 22:57:06 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7af1962edabe3d58af5fbd06f3e345528b78b672a4b879b72fcf2e0d92549637`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 50.0 MB (50001944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3301452b6cc13e86e36f0364b6dae460e7c8a689c5c3b07bd0f3d0c3883b39`  
		Last Modified: Tue, 19 May 2026 22:57:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c5e5c557a1c161576ac06be4e8be8ecc02d401251dccb666e64d83cd748cff13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfde275b3608b617fa5a8469a2bd61b7d78147fbd2ac57c644171e9c0a3dd69c`

```dockerfile
```

-	Layers:
	-	`sha256:5d24dae381bab04fc04a70093b2dfa1482db31c1f0fe2054d2896b8ef44f804d`  
		Last Modified: Tue, 19 May 2026 22:57:12 GMT  
		Size: 3.1 MB (3143439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d41c6f0686b068db8a4d050cb982dee9381dcc8d4aa1b30f22e0e259162667e8`  
		Last Modified: Tue, 19 May 2026 22:57:12 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5f64a04d0af8b0de365b1abc974f91969701082d14e6bfcca1e4bc2be08b39b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54021505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c6b0556f0b2ff9034bac541752a6e3ba2baf307843f69d812b6e2a9e868abd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 22:55:32 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2e5564b9da7290f7430ffd86cfc5f2b22a68586fade0aa81c8610704c43fd41e`  
		Last Modified: Tue, 19 May 2026 22:35:40 GMT  
		Size: 54.0 MB (54021281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc9faae5fb02aa9c7ad313a36642b0c1ac4a2fe5f1b150f52d7e1b15abcd66a`  
		Last Modified: Tue, 19 May 2026 22:55:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:32d2dc68b5b46f950d715fda6a55bab8afae5d7a513a9a4abee59f93e450105d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40499d402bbfa7b3d0a892b15e5abbc8f4464d3e5b99da5a0eed7d3bab92e9cf`

```dockerfile
```

-	Layers:
	-	`sha256:b8f4e206ff2e93aa08adbb162b799197f538d431c7732eae22af39760811caf6`  
		Last Modified: Tue, 19 May 2026 22:55:47 GMT  
		Size: 3.1 MB (3149753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b6ea213c2cf7b6922f5705d13389e5faf24ffd54af9b652033380db67d16863`  
		Last Modified: Tue, 19 May 2026 22:55:47 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:ea114c3304529cc8410a2a099f9c3c579e08fcf1977b9c5b070bbbc148ef368d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46773402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf6c907e238293de634bf169e2d3356a6f9d60843ff8cd205df840ffea4859e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1777939200'
# Sat, 09 May 2026 13:48:21 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f7ac0cf25d901b0f78c05ace03b84988d685b5007a5c2ecdb859ecb56d3b46f4`  
		Last Modified: Fri, 08 May 2026 20:22:22 GMT  
		Size: 46.8 MB (46773178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6ddd2eb877962717bcb1f88fd7cfe097f3e667125ec7ee758dee8650375518`  
		Last Modified: Sat, 09 May 2026 13:49:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d46e57af754dc4d03d9fb2ad7caa59993e97d1e32f034042c3b1398b8dee44e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d79bc1eafd3c818e1aa554a14fd94a5bb80e8d4a495356a50479e1e7cba8386`

```dockerfile
```

-	Layers:
	-	`sha256:19a3a06f9e17cf1c87a66e91b94e96130eda967d4e78a0dcd24845c214f5b068`  
		Last Modified: Sat, 09 May 2026 13:49:17 GMT  
		Size: 3.1 MB (3138367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2d8bdbfd364efbd5d9ac33342b608d8a28f8bfd8dda8bfc86f90665a55b700`  
		Last Modified: Sat, 09 May 2026 13:49:17 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:3698057b91f31701ed2222c1525f47920688e18d6dc51cc751437ad09e6d1163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48440749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db19bb045aaa37eafe0b3532578557365b6c617d4b4ebee42aa0192cf65df674`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 22:56:10 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7394ea10bf5bc140ccf55e31841e993aa40f4cd465376d373dbae4fff2479c30`  
		Last Modified: Tue, 19 May 2026 22:35:35 GMT  
		Size: 48.4 MB (48440526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0b3871de0e27b7e31367799c19200a1aa7c555923bb71a56364b7412480037`  
		Last Modified: Tue, 19 May 2026 22:56:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9ce42f50b1821f2b96780583cd7deb8a1f801a0681cf8d25337bfa9daacf6106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769bc66d7124bc52977137402ffa42647447d6a78d11e3274375608c5ffc5e2b`

```dockerfile
```

-	Layers:
	-	`sha256:f2fe5d37350aaf735445bb8f294a01e73d4d735b76f8e5e141d3a95f1ec154b5`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 3.1 MB (3147693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24245ba5ad02a435fac308637e456f53bd81c083ac5bb6646241083de7553512`  
		Last Modified: Tue, 19 May 2026 22:56:21 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
