## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:52facfb85597a0fcf41457a6b68f79c25b25e4464361eeed4f6c8241eb1be847
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
$ docker pull debian@sha256:71b4dd4010d39fb3e8388bf926f42586e2f1f770d6fe0c07a584b1b42850e009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46004849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a0fb062e985bcfcd46f2eef3f66e049f790bb34624e38e8838926e98381d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:92f0eecb0902c904cf1dad1c6151576f52ed736aab0bfbfdbdb998f9c806cc41`  
		Last Modified: Mon, 17 Mar 2025 22:17:13 GMT  
		Size: 46.0 MB (46004626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71d419441e68a06b792bbdb888a0d953b5ad0d45dfa60117fdd7690ca88e07c`  
		Last Modified: Mon, 17 Mar 2025 23:11:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7457a676ff70547b742ccc148452ceb135fd6c1303bb437c9c495974cb23a8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab08c64b2878f8e647c4df4fe12ef69dc4922c979d08744933c0eb6907d54c6`

```dockerfile
```

-	Layers:
	-	`sha256:873d830e4c976e83d4060ca6cf50e880900b6cf75d7eae585188b59883cb0244`  
		Last Modified: Mon, 17 Mar 2025 23:11:56 GMT  
		Size: 3.6 MB (3619437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5ce514742af4a62f90baedb05b618f96cd9abd84a37e2473d451996d33ebc3`  
		Last Modified: Mon, 17 Mar 2025 23:11:55 GMT  
		Size: 5.9 KB (5898 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8aa9e6d1176dfc4b6a0f49e23784900ef04ebfe4ece2e365f565ab5cbfae524e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44178228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc6a404a845b12a0aecf1d8acf90974161b9522d2fb8d212bfdf892ac1f3684`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39358a00863ca4907b5cef219517bb3d97f74112c3fd5771eaef75e9a3364a20`  
		Last Modified: Mon, 17 Mar 2025 23:11:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b37c83b9d033a2272906ab4b25e1466c7620c6cb8f65308955afddfa9a4d7023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5751b85c734c3f0c1de3741727d6b2dd0a6a14ca923d5a03eb9a48c49d76e8ae`

```dockerfile
```

-	Layers:
	-	`sha256:0ac7a46009ee66d2ae42466d0598996e9ac638ae0b0f319b8203ef104b559dc1`  
		Last Modified: Mon, 17 Mar 2025 23:11:55 GMT  
		Size: 3.6 MB (3621415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a75529847324511310460c8afb741f8a4b80acf871ffe1a98ac28dca552f46`  
		Last Modified: Mon, 17 Mar 2025 23:11:54 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e72e50eddbfd74e1b7317efed466592193b0aa8ba07949b220b521fb6fc8949f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48305078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f1c71962d2f46bf001d7044db48d1af7422401a2c7005e92cbc35689a6bf1d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a720123c1c511ef6896bcb344872b200e1195c666f330e27f687897a61b24e2`  
		Last Modified: Mon, 17 Mar 2025 23:11:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:67e8002f6da5a32b9860613e90e551ca5ef0e97e5c39b7e29ce8df60db457342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e479cc2fe0afc7ef7b025845ead73e275d72b3b52a297e38b76ae67010d8665d`

```dockerfile
```

-	Layers:
	-	`sha256:b126fbb4f6d54c10d4c89c84e711b8ed5f0e205932ea562c875590c18cc91ce7`  
		Last Modified: Mon, 17 Mar 2025 23:11:57 GMT  
		Size: 3.6 MB (3619451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf23998386bda229a5f9d4bbf9ecdebfca1ddcebf4ffa065149135a34e7062f`  
		Last Modified: Mon, 17 Mar 2025 23:11:56 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:be09acc625f29aee61785d248c52e692df4f0a88eb5748eaf3a22e6da91ea849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49454704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd3ee360cd93111ed4b4ef331c8218b12a51c175c5c29b82def04b5cdafe500`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0b523b016df27cb891f3b2a78976c134df47e0a5dfa2e6d56d580e3f2dd07f`  
		Last Modified: Mon, 17 Mar 2025 23:24:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9db72ef57ab3f3c759115d98ed1f83c8a9b737ef97d0d977750b52bc8411127e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f6f7e281c7e4b73ff7f0a4f529e016c18a34be50c300ada7eea16829d86eac`

```dockerfile
```

-	Layers:
	-	`sha256:cee120a46c618e61080e2f653683afec7e0f290022a914a5bc1a96eedde87c45`  
		Last Modified: Mon, 17 Mar 2025 23:24:51 GMT  
		Size: 3.6 MB (3616397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dba65b6ab3b24a8e6247e4771705129fc1ce3a562a6588ef439069f63f257dc`  
		Last Modified: Mon, 17 Mar 2025 23:24:51 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:acc048ea6ba07afe7732bf1bdce8e342b6606256c5fb394d305604cff0d36732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48756393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014d064393d8a7bcc30228e9e6ac7b53362b0dd2d7dad3e25fc2ccf9aadba036`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:579ff6a9178b7f862c70c40b253d6f0090e7792eed3ce083de0732adfc5f4826`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 48.8 MB (48756170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff8505c3e1aea75d4a936bffeb1d44c4f580e9489cbcbe8eb1728fec5eca93`  
		Last Modified: Mon, 17 Mar 2025 23:15:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3b8fe758ec7e309ccf2d734f61a443606c08a87eee2b0da5427ff766e717883e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a039e4e16c355b2bc3318f686a22abcab104ddbc5be4c5822d927ec29d96011f`

```dockerfile
```

-	Layers:
	-	`sha256:a5ce513dff6c7dd5f67a77f47cb61c9866b0a9c1fba981e66e34eaa764060401`  
		Last Modified: Mon, 17 Mar 2025 23:15:48 GMT  
		Size: 5.7 KB (5671 bytes)  
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
$ docker pull debian@sha256:7000427f17c4194351b9e6d4c2447690c856076a5f12df691dd74f94bb5c38a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47128063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5f0576723ad07fbfe8f27de6435e750a555cfc87eb8476db2b3e0d418c1f39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3997222d054d1602e52bc260c8d67514be03c9395648e66916a2b002dc35d06`  
		Last Modified: Mon, 17 Mar 2025 23:13:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:21452e638ebe7804367f134258b7f8244dab39006fc94360bcde6d729e425a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c21bf087cccafe0d5067442ffb72b7e2dfc78f86b9fc76509e60a36b1a8af9`

```dockerfile
```

-	Layers:
	-	`sha256:c84d43cf24f7f21952860206c0cacde6f6ed3d461e5d8b5bf6cf77bdb34dd6e1`  
		Last Modified: Mon, 17 Mar 2025 23:13:39 GMT  
		Size: 3.6 MB (3618966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1221f1d8175e09b6073d9d29e382b4ef5b7820557f08b715b2e9dc2178aa81b0`  
		Last Modified: Mon, 17 Mar 2025 23:13:39 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
