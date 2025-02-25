## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:910ce65ad80f09075e313f1bc361764ecd5c171ba91c478268b4265b6171005c
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:c9851d6c98cbd89025cc541a784399d842aabd27d226d41947fb6e32aecc6a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48476326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2b83592893cb1152082f9c9edd501b4766db07d69683a07c76c66958ac0e19`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75f49571c88e4a068558f4f7265eb4e349b54ad7ebafab3fe6f3e8ee7b1b2c`  
		Last Modified: Tue, 25 Feb 2025 02:11:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0dfec53bd694447884b5b67f487924ac85a059bd91582bca05c37fb9519f4906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7118cb6ffce4f1122b8a0e2a8d60c87bb17461b222db838eb9381b37321a465e`

```dockerfile
```

-	Layers:
	-	`sha256:cc26970307f17e9aaad2f61833c2b75ee6550b93888953cb581ce2ebac73a4a1`  
		Last Modified: Tue, 25 Feb 2025 02:11:24 GMT  
		Size: 3.6 MB (3619228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea71f4c8a1563cb12a025b83f6c103d340d717120b4a9a74acf624a35f7d9f4`  
		Last Modified: Tue, 25 Feb 2025 02:11:24 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:eb3b2df8fc5cc457f27b612f20b0454e5e2d86083a2d171e8a900c56b5869c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46006722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fc0f41cb2b5c5ba387b97ea43755ca9bc5f9991ec9ae9b6bd42109000fb7ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922461856551fb570729ddff6b6cf22a9c07af504e566fb3e2ae5735d4ea961c`  
		Last Modified: Tue, 25 Feb 2025 02:19:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f33ccf2644af777ccc7121a424c58821035ecb960e62e5dd5caa2272dbe022bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69d7c411453f3392b5a702bc23e255be896bcc259cbb15c8e963b2a3ecf05f5`

```dockerfile
```

-	Layers:
	-	`sha256:c783de9fb81de3e1b905c08e4811feb5e8e5830ced1c4ec8749bca9c83f17f4c`  
		Last Modified: Tue, 25 Feb 2025 02:19:42 GMT  
		Size: 3.6 MB (3619429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626b9e91d0f1d13cde149090df707c63d7dd5a755b2f88b7a69223debef3f818`  
		Last Modified: Tue, 25 Feb 2025 02:19:41 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4c3c944e6b76557fedd346836a49bef7ac1a6652c6dd32109b84ef44569ce3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44180519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ab6d2630abcb8ad97c7740fa8962ac6e4d3b13e9fee818edb2bee4ee99fe6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5354c978c4dd25baea22b5003c86753538968e0af75796db1241bdbb036ba0`  
		Last Modified: Tue, 25 Feb 2025 02:15:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:581320e8122fde555fc2ccfc68fc029a70c59f63b580143f7adc89d0fdddbc3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a56b76209ab2e0540c3693fa9d338c4601e44e500e32eb0af78484ae95e461`

```dockerfile
```

-	Layers:
	-	`sha256:d95c518cb912516d285acb79e7273dc0d058ce2aecb3629caa897dd5b0030e9b`  
		Last Modified: Tue, 25 Feb 2025 02:15:23 GMT  
		Size: 3.6 MB (3621407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7489ece7e453e8c11c310d4048a1b4cce61cc6ec18e46fcb37eee818802569a4`  
		Last Modified: Tue, 25 Feb 2025 02:15:22 GMT  
		Size: 5.9 KB (5898 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9317f3baa2b87e247a8b2e748666c00e90bf86b4d37040cff7f55bd7090347c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48308233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0463f2d79a25a6297003049bd2ab247248f8d3618869ca52cf5d8c907874f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c40279e9b6ccc322b861b92b4c965fa1562f0395123d7a39472d88aaac7142`  
		Last Modified: Tue, 25 Feb 2025 02:16:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:784798099ad9f6c7d9288d42756dddc82639d0d97756d0a202f653bf75daba65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860ca889c3d6397a4e7a63f36130b746a8c15275516e93b81519cec50e1757f2`

```dockerfile
```

-	Layers:
	-	`sha256:956fb97d57e9742f27522f56248c3a55ac4b109a3c88ae5ddad46b8cc5e12c93`  
		Last Modified: Tue, 25 Feb 2025 02:16:24 GMT  
		Size: 3.6 MB (3619443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96cbf1ed7fab290f21f48b919d21a7e4e2a0230b2e8f8e4ab9e4c3fe860631ca`  
		Last Modified: Tue, 25 Feb 2025 02:16:24 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:ded17891001ac79f8b79f25ee8d97dd1e9edf09c2d19d933df1ff4c4e1985876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49458678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7a813dcd161d81591850578f449637832d0fb3067dd73b36095a41e922fa19`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb000b22a2f56a7b14af341ece626476b605a961a94e845f4c490ba626f103`  
		Last Modified: Tue, 25 Feb 2025 02:11:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0b5f1100518b2a02f0f3483bfba411821613e78391a181f30479c15111eba911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb3e183848988b24ab705b1940ccd63142f5f6867dccd957865bc11364fe37b`

```dockerfile
```

-	Layers:
	-	`sha256:88a67a64f2be7ab98321cea95ab208208a3a64babef3f46fed453647664fca18`  
		Last Modified: Tue, 25 Feb 2025 02:11:14 GMT  
		Size: 3.6 MB (3616389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7adf909a620ccebff0bd93d8ea27806eabd822d00415374a1ef08ae82a93ab57`  
		Last Modified: Tue, 25 Feb 2025 02:11:14 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:0d9bd211816e9638aafb69eb9d6100c7b253a980fa02c446101d5047a6f10901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48759217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03baa5ed760d987fe515104e7478b05bdcc85138b93cc3adf4d553be59b8d7d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:54f151aa1b87c0945bf97dbd3c72581adb102deeee7a48dedc6ef51580d82ec8`  
		Last Modified: Tue, 25 Feb 2025 01:30:30 GMT  
		Size: 48.8 MB (48758989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a2a6fc4d39959c008b9733fdaffd03e2e1c1c9a5acd5bd6b876cc51d7d873e`  
		Last Modified: Tue, 25 Feb 2025 02:12:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e86bca817607b8a8a54fa5dbb936aac77d06714bc3ece62ca75bf468be8395db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57619d112f6767d9c8d1592a4b7de3d35b98221e373b24920e7e718baaaec22`

```dockerfile
```

-	Layers:
	-	`sha256:7140778767d63a3b4d43326175c23ee01294705b76c55b48b70523910475a562`  
		Last Modified: Tue, 25 Feb 2025 02:12:58 GMT  
		Size: 5.7 KB (5670 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c1a02f7572bfaed319ede8a6ee4b2042b23a31a71e59d480988d4de6af0a98a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52307878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dbc0eb5dc3e9a64274f5e8db261e08c56a303b858e9dbb5035ba45322b7ada`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5717193f6330d608fef1a1158f4e75653529da619b5a19a3552fc44f86e43a`  
		Last Modified: Tue, 25 Feb 2025 02:14:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8434f1fe7f9331a1af4221082a7b38bd16290a8d62bcc383621160f6fc6365da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572b12471aad17ceb61029b3e3248f2e26a4e67fd5eb01473ef97b824471c0de`

```dockerfile
```

-	Layers:
	-	`sha256:ffe39d43ccbb6dc06cfe2696937a0f2ac553f869c94cd27af04a5f8fd2623afe`  
		Last Modified: Tue, 25 Feb 2025 02:14:39 GMT  
		Size: 3.6 MB (3623488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea60d5ccea8de4f2029860a8ae853dc0edd88af10e92b58724d3cdb7cb187ae`  
		Last Modified: Tue, 25 Feb 2025 02:14:39 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:a299789bae4568bd736c9a0f41055d6c0af1836c96afa0b2b6d9febf6198f6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47130216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57276bff46fb5f23baa7682d627c26874f58b561c06cc593b9b85aaefd8b1965`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98337b9fa6097a5ed17a301341678a2fdc818fb568e08ace828c04cb511dfc`  
		Last Modified: Tue, 25 Feb 2025 02:12:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2f92442e39061bf08f168328e90f413005cfd6aabd1d2d562856e8231e17dc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddd28b98494e6223809e38b3b902f97540f17d44c1aaa2c251aa9319d40d08f`

```dockerfile
```

-	Layers:
	-	`sha256:37a5616ce611023e296ebbfb63a191f9197fab6005548781bc3bd757b1a0e28d`  
		Last Modified: Tue, 25 Feb 2025 02:12:54 GMT  
		Size: 3.6 MB (3618958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5e2f716f70cf1823ba2aa22202612b22d116d38be9f9fb5e0bde678cead48c`  
		Last Modified: Tue, 25 Feb 2025 02:12:54 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
