## `debian:stable-backports`

```console
$ docker pull debian@sha256:cc3a8bb06f1237cab8850a185a517dff4c1b65730317dfb63720318edae931bc
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:20c6f719dd40a523f8f05b8180d7902a0a3a82888c10e4b21720ea834f453b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49285844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a194384948d5cfc41c18d46582e01bc220ce6b42a6ac44fe56dfb547bef0bc3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1768176000'
# Tue, 13 Jan 2026 01:16:32 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:85738c3f705a487e0716efdff2051d14bf36f81c20122e66fbb82db3a00c4e4d`  
		Last Modified: Tue, 13 Jan 2026 00:42:52 GMT  
		Size: 49.3 MB (49285624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cebd524452cabdd93fb68d2dae5c833c133294b7a4f351b5b81baf4c522744`  
		Last Modified: Tue, 13 Jan 2026 01:16:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:397af4e28b9927c77bc7a03213d006c8c2e3a030a31bde7a2166662935f24704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c697039277002fc311b7bdc590a19ccac85492217c392e65eefad6474e39a16`

```dockerfile
```

-	Layers:
	-	`sha256:40f5fe97e1586b576a5ffa4fd258b4b7053099af4d35448a56cc238d8560f85e`  
		Last Modified: Tue, 13 Jan 2026 04:26:48 GMT  
		Size: 3.2 MB (3170877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c8d7c32ec8f136540d05c2abe0deb236b3429f5ad3216e9dd0f4f080db6e69`  
		Last Modified: Tue, 13 Jan 2026 01:16:38 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:915b2deb6b916ebab262c148f22e3bdd03288a0b24d95b7a0bfe7d5018a47ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee85b580226e622cb96466a83f98ef5f723f820fef5cac620d21623afc71f24b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1768176000'
# Tue, 13 Jan 2026 01:17:13 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5daf785f868cfdad03bf94a862ab2e2dc63a81c9a7ebd3cae4aaa27ae03aece8`  
		Last Modified: Tue, 13 Jan 2026 00:41:12 GMT  
		Size: 47.4 MB (47448362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad507f5c708b96892d6e1703a66f1cf06ba773a099322bcd4929eaa9cda9364`  
		Last Modified: Tue, 13 Jan 2026 01:17:22 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:20d9b8fedf6eae9c95df7a2badfb97430583c44148aeaa9b9920a3269ed3074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4f7091cb30a24af7115cc9f15900093c739008823ff403104748ce00da06a`

```dockerfile
```

-	Layers:
	-	`sha256:59ddcd982ea1247036d5efbf57ba7b850bdb3e92d33202b777ed72b0af2ad236`  
		Last Modified: Tue, 13 Jan 2026 07:25:17 GMT  
		Size: 3.2 MB (3173814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5058a2452859745071c4439c52e37fb9630319903176d53618a3b43383b94798`  
		Last Modified: Tue, 13 Jan 2026 07:25:18 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:99c8ebe48fa020e7fa478f236ad5c394da48f7ed89337e5a176ff937710bd926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45718037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47f83fbd5ddd2b3fcf0268d2a52af1dd860448a716c71c9fced5e0091203e2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1768176000'
# Tue, 13 Jan 2026 01:18:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bdcd8ce1fb681b74c5c63750c610150e89490e6733dbd8b90e067d239cbd9163`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.7 MB (45717815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a6a9e7e37ac6c09a69f742fee0e17157ab99964bff404cec2354bb4ff1c0c9`  
		Last Modified: Tue, 13 Jan 2026 01:18:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:096fdcb8368f489e6fa6ca58a91dbdfb9ee4430bf64fe93ed8038a711d192f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b4806ee92a4a058dc8782624a10c4c90523302aa7561bb5ca6f3f944537f87`

```dockerfile
```

-	Layers:
	-	`sha256:d2ffcdd68aa586f62399b765ac6e769be8f41aa6cb1c0502ab2c0e5cd4d9be9d`  
		Last Modified: Tue, 13 Jan 2026 07:25:23 GMT  
		Size: 3.2 MB (3172251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6c08b24b5e60d54b1e2061a1c04c89338a944c09c71742820e49c15863338a`  
		Last Modified: Tue, 13 Jan 2026 07:25:24 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9f6cdf23194ceb6cb9ec4a07b8ad974c8ce176ca0299b0d7f88bb2363128d080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49648304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49b2b63c84d37dc33002150681d3b7fcc6870fcc65b215f095263a23123182e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1768176000'
# Tue, 13 Jan 2026 01:17:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f952bf6667e1a51ad70905ca88b9f1b6b95a6a63a55b64df47dd4c8a2edf7511`  
		Last Modified: Tue, 13 Jan 2026 00:42:35 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1429997449af6981e693fbe9d6b17e360257cc5098dddd34672064a8a2a238`  
		Last Modified: Tue, 13 Jan 2026 01:17:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cd638091c25a7e7f90b227c55924680adbcc27ae0689c4c3b981c719696f97e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90af2425b59d2621449092bee442a8ad1cc26fc6e2cd96eb4677cbfcc4ba6c4a`

```dockerfile
```

-	Layers:
	-	`sha256:1cd5aa6107ca026de500550d0b5b955b960d91cdbf038653bed1343d69e9ac81`  
		Last Modified: Tue, 13 Jan 2026 07:25:28 GMT  
		Size: 3.2 MB (3172358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a146a6a4cbc075f4915ba9fdbd95e351ef08c81cde242c10d4391017220c817`  
		Last Modified: Tue, 13 Jan 2026 07:25:39 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:47884ea6a58f22c9ee47b1138f307f1fd825c56e5233c175a517114c3b7b9f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50799096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f069af4482a83984e7397f47ea7fd11dac1fcd18ed271bf203a646182da3531`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1768176000'
# Tue, 13 Jan 2026 01:17:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d4b0bbb5d12f6aa0551aae272bc1aae9b1101f305499f702de41ab60e6342e46`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 50.8 MB (50798874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339dc31fee6b62dec94d627e92c6492dca96560cc11e7334be330b9ab6d85bdf`  
		Last Modified: Tue, 13 Jan 2026 01:18:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:539851b14d8b6fc186ce6b437de40b682c9375627e3a733ffe8a0f81147f16e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b977c0fae81936d3413d928243c69967e6f54b816703ad4e6b6aacec195caa`

```dockerfile
```

-	Layers:
	-	`sha256:a7862d7ed8028a4a473e9963d5e15d3b9a27b4e685422ebc84cf8fb78dcd02ad`  
		Last Modified: Tue, 13 Jan 2026 07:25:43 GMT  
		Size: 3.2 MB (3168079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63be5b304b5485196ae84e457b956484be94f2d077dbfee4ca6579c8f47385b6`  
		Last Modified: Tue, 13 Jan 2026 01:18:04 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a16396c22b60243448506f023e465b21cb1dd263cfc5a16eac537ff1c242e01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53107184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72df92fe1ff4114cf13d1f6684b93839466817e5806726d4bcb0fdbba1174a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1768176000'
# Tue, 13 Jan 2026 01:15:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e661ae2b6b2e47825feed01c6e777873bf7d877c8a699de7af68db55c0dd5ef7`  
		Last Modified: Tue, 13 Jan 2026 00:56:34 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654349ba8fc1d94d095585dedfdf714ad3a1f70be1f2d38da6462d1d00bae4cd`  
		Last Modified: Tue, 13 Jan 2026 01:15:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4da1c0659ad9ad9ba9e5e4fcd1e63c32197209042e6f079eefe01798c9ef9fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9981be030a1b6d68fed9240118f34bcfd9998d8a44395cfcb6a2057c138f873e`

```dockerfile
```

-	Layers:
	-	`sha256:5267e6e1a831754ebdc95288c8c595dd44ce01576e2fe0850840a8e3291b6e61`  
		Last Modified: Tue, 13 Jan 2026 01:15:35 GMT  
		Size: 3.2 MB (3174390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a21cf945e5c0d9cd09b24deafec2f633e2025783d08ed1fa5cfb920e8976095a`  
		Last Modified: Tue, 13 Jan 2026 07:25:48 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:514eaa12d0ce458049394705debd48274e2202b5f5b7802114cf8088788aeaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54266151e43e33c6e9c8b5128f82a24297156480b6faa52983655033fe0638da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1768176000'
# Wed, 14 Jan 2026 04:05:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0930ad1b8ab3a1854b92ab0f18f171a0353703da550999d7645775e9b4a3b85e`  
		Last Modified: Tue, 13 Jan 2026 00:59:35 GMT  
		Size: 47.8 MB (47770846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c49fa9f9ed21003e5ae3b6f5935920402908267fd93de22fd363e8aa042be2`  
		Last Modified: Wed, 14 Jan 2026 04:06:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3d0f3fc7e0a90565272dd0a66a41e93449d3cfa576b12e8f0963056a15f98f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800c5f5ac912e54e07edbac90ae1a3596ea4b70ee4119ac250f01cab9da55568`

```dockerfile
```

-	Layers:
	-	`sha256:700580e410e119a76c05b45db560485e5994ca5c59cff769c721de1b93dc2dab`  
		Last Modified: Wed, 14 Jan 2026 04:24:41 GMT  
		Size: 3.2 MB (3163202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f9790b56535ebecae14e6beac52f97d9c61189ad5ca6f8ec8ccf44093c8886c`  
		Last Modified: Wed, 14 Jan 2026 04:06:21 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:86af58f2a5cd29e46a28c2b943f8670947309f2485e3f0be3d35ce41b40e667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49348925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525006650dace488bf8386b9c550c7ff2dee31bef7665df148a62dff8dfe005e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1768176000'
# Tue, 13 Jan 2026 05:15:34 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c9a62eb9bc7b94b62657d84f09346210293c025b8647fa976016e6536bd3a190`  
		Last Modified: Tue, 13 Jan 2026 04:22:20 GMT  
		Size: 49.3 MB (49348703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0084ec4d4e6faaab44b684a41b1f4ac6e785283bd1075821012efa02a45685f`  
		Last Modified: Tue, 13 Jan 2026 05:15:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:13b3e5d6aa8acce4d4df33106bd0d739137924c4e743b149f3be160ebd4f50ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843ac0eac33da57efcbed8a1d95e2afb59172b804f3287b66564d61c41fb1f8a`

```dockerfile
```

-	Layers:
	-	`sha256:336381cd3f608b1863002b6d92c06fca6f512b7873023afc7bc59b17ff0a8d3b`  
		Last Modified: Tue, 13 Jan 2026 07:25:56 GMT  
		Size: 3.2 MB (3172324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666c3c9fe74939953cb1969964d46ab90eafde38490dfbe134e9e92e970bd309`  
		Last Modified: Tue, 13 Jan 2026 07:25:57 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json
