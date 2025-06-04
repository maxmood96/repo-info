## `debian:stable-backports`

```console
$ docker pull debian@sha256:d22e079e1e719037965c657b8111d44814bd6e5c74e892bcf8d4fb2c978f184d
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:dacb002b1310519f0f924b7ee7f37772d60d6529ea622023157189c42ff211ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ff800408058c2067647b7338daa11292bf3dbef8e27042a32cb72a5773a63a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:94a7539175dddf3672b0f1f52ed78d2272f48b48ac2ac4852112b1ce472c8c01`  
		Last Modified: Tue, 03 Jun 2025 13:32:47 GMT  
		Size: 48.5 MB (48488246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d702d26539853fc55af2b2c6da967e868edc7aa134a46ed636a18422a448fa54`  
		Last Modified: Tue, 03 Jun 2025 16:53:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:287c008aa7a4bb2c3a42fd1878719b95d432582fe3f7ef6ece81eb02ec74310a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db26b5ce2ef17c046f0276a5a710a8196cb172f4cb0aed83299fbb483a1c7d3e`

```dockerfile
```

-	Layers:
	-	`sha256:062c0772d2284220197fa6864c145fba80d26cd8b9104145c5ed84815d4b378e`  
		Last Modified: Tue, 03 Jun 2025 21:23:12 GMT  
		Size: 3.6 MB (3635840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac3df411a430087164c9081cf2605ae503799644b8f1e2f3fb2de010f9d294a`  
		Last Modified: Tue, 03 Jun 2025 21:23:13 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9cfebe9771ce8c3160b613ec8853db458a01744af6b8fff7d13d414c74243d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18482e27d7460aa09a10e8bdfb76a8238dd1f316e40ca920b391d7fe292eb46`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:477967cf802170159ca318ba4f72a0013d240e796fcf3801a49a937071ce1e65`  
		Last Modified: Tue, 03 Jun 2025 19:59:03 GMT  
		Size: 46.0 MB (46021486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b91596792a26ae61a835fae0b39eec7ae3efaffe0a28da2c722fe39408c208`  
		Last Modified: Wed, 21 May 2025 23:12:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:de5cc0e29a22b60c0ae2bd7bc3f073736bbe9c24af07b26b34bc0880451837b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fdee0f872ca382fcc62ddcc826b2c2dd0ae4fe05df191a2e96931c5d19d71d`

```dockerfile
```

-	Layers:
	-	`sha256:6afd04de48e79160b5c793174224a51fcec2abb1359f5f4001a5504a8427ead0`  
		Last Modified: Wed, 21 May 2025 23:12:05 GMT  
		Size: 3.6 MB (3636041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41c40dbb7fec724eab1e0e046376c31ed55909de881457fd7b4209f947ce00d`  
		Last Modified: Wed, 21 May 2025 23:12:05 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c7ea745c7ecbeb068684bbf05a292ad09fcb8df43a3a4849baa4de93ac0dff09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44202996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d336232a842c318f82969758c8f772d166eb07b38dd3efd34ba347559111ceb1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:22b9e79c4c4ef5bcebd0e45cdcbb4a4ac5a90aa0865b783697594422d92721ce`  
		Last Modified: Tue, 03 Jun 2025 19:13:51 GMT  
		Size: 44.2 MB (44202774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944ccb0ccd6485169d36e4692c06cfd6c37f22a2ba303950266229345d888811`  
		Last Modified: Wed, 21 May 2025 23:12:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:63f617a0e2738364766a760ad7cb19746fd0a1e09ef74ce6a17f2a26fddfcb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3643898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf200b72b3082c7cd6ac077a773149f810edb3a1579f9862bc56b5b2c25d52f`

```dockerfile
```

-	Layers:
	-	`sha256:fce966b0ba44197bfce0aa97a0b9e1786390f656fdb8904b160662056ea1afd8`  
		Last Modified: Wed, 21 May 2025 23:12:58 GMT  
		Size: 3.6 MB (3638019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d0aae2c86a1be16f7e2ca978fac5beb8b81f7809b8d2c41a1356f773bd1193a`  
		Last Modified: Wed, 21 May 2025 23:12:58 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7b949ad618659ea48ae684f9d3167033b18a326a23594a086a97b8262cf3e2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48327404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe02ebe2e3847ebda814cba755eef35cb58309b36f624d302fcfae76ff49a0db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5acfd33b9130a6d1d6c199e8ea1ea2b0625b02bbc51b71f33545c65b96851763`  
		Last Modified: Tue, 03 Jun 2025 13:55:25 GMT  
		Size: 48.3 MB (48327182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc487633fa7156ed814ca9cc4cd944fd2280857da100a04d3361ed6616d6b646`  
		Last Modified: Wed, 21 May 2025 23:12:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aa40b1dca120b1800eefd2abd4ab7e7163b98371dbbdc5664ea43b3a3c2993ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e840cecfed8409a365e92361bcf791cd48402094098d31dd7369f22db2b3041`

```dockerfile
```

-	Layers:
	-	`sha256:bf679a3844186f5b9bc3d8575b9d0311036b2e3e7c89809d2eeb0aa689bf8424`  
		Last Modified: Wed, 21 May 2025 23:12:28 GMT  
		Size: 3.6 MB (3636055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c28fb3b3a9ae2855e7ebd37bd37042943b9762f2945512c3b0ad5854095c29`  
		Last Modified: Wed, 21 May 2025 23:12:27 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:e4d550022c679149792a5550f0d61aab071640e0b5cc840b2f98e065d608ed99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49471789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49c5eb1b9c29493d31e451ee86e6c150ebff44e01c5f3509ac5107199d9058c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fc103459c16ef2e962e07bd8b26432b3548b1794e2b5c5a2c8a4f0fdfab1147c`  
		Last Modified: Wed, 04 Jun 2025 00:21:57 GMT  
		Size: 49.5 MB (49471568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a33e2ccb1f401b92aade970d738097a334483e2bab79943cf11b37637cfc8`  
		Last Modified: Wed, 21 May 2025 23:11:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7993809ee69dd9f2a3eb77460a8458ae93997838e708d9fc96c6bf8985249cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3638852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e0b5d8916749a7a563b60a632814192d5cbe80dca3ff849fcfa255e04a6422`

```dockerfile
```

-	Layers:
	-	`sha256:683cfa85ac9f08b406bb9a671cbd6a41a292bea369f238f3eeaa43edb6209318`  
		Last Modified: Wed, 21 May 2025 23:11:51 GMT  
		Size: 3.6 MB (3633042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a7b91c5cbf8eeb00633147d95b294d2cd787dc778bd8264395a6c30b8651c1`  
		Last Modified: Wed, 21 May 2025 23:11:51 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:dba9c74e2e0de01d6a3d03738dd11ec671a6f7091abc8a97b394ace3fea0d32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48769974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5754bf51130bc1f3d8f56537421972b18feb0d74e2bd6d4f796119ad2f4abd9f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:26e848e85b58dd7c634a9bad89da62de8e243bc05f7171697b5b1122905cb710`  
		Last Modified: Wed, 21 May 2025 22:29:49 GMT  
		Size: 48.8 MB (48769754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42022cdcf8d7b37aa9cf4023483be10aceb31af371608a9c95937de1f2c07ee6`  
		Last Modified: Wed, 21 May 2025 23:18:46 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:603ae5eb9849e49fc919277f1eef11c66dfcf7fb1f13778ac0a5d1e8fdd35108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3f627aa6c4d7c09aa62e6a91c1c5e627c6277d4c377533f2ac1df71609308`

```dockerfile
```

-	Layers:
	-	`sha256:391bf5b50245c08c103727bbde75f4e647d3f123f9848f6dc24db30b8cd5e2d1`  
		Last Modified: Wed, 21 May 2025 23:18:46 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:8757f779836f26a0aaad9f7fdc7a5c3744f755444c06a4b66aa418ff7f4622b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52331839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e275f8d183dacfd500ed7adeee7e709eec4dc5b615bc7e6a7988436fe95d453`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1ba2039a66f7977fe2d2d04629b7e57f26a56091d813ece87d7b5b3cf6a273d3`  
		Last Modified: Tue, 03 Jun 2025 21:24:02 GMT  
		Size: 52.3 MB (52331618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb5369e6e1dcf34b69457f5ecbf5c07d09bd2d39f324a8c6c97a6e6cad5e38d`  
		Last Modified: Wed, 21 May 2025 23:12:09 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9332c02ce2efb41b4f741a2a0dbbad4c30bfed8ba14e71abfaccf7ac4a92b92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822e38bf11083c1565f9f341fb097fe22b4cad57546adf05fa2c6e0ef6a4a2e4`

```dockerfile
```

-	Layers:
	-	`sha256:27d3a4584ef38a8b6aa7e5c7faf341d9b8678f6bbb543cc710cd6c4dc809ba30`  
		Last Modified: Wed, 21 May 2025 23:12:09 GMT  
		Size: 3.6 MB (3640186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3acf71b59c03dbcdba1026eb8bdf12fb39082c3427a10df00be83ff44980402`  
		Last Modified: Wed, 21 May 2025 23:12:09 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:59f8c3436d7ad7ff60b5684ad15c04a59c13741d10df170170f58ce777a2b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47144067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ca0d6a7124fdafc4fa4a6a17d297e20109c2488a4e1aeb95b49fd2d40fcd44`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:24535d496c396d6255b01b1ceb22f8b16e24e74fa85b4e2f999f21f774c99c00`  
		Last Modified: Wed, 21 May 2025 22:29:58 GMT  
		Size: 47.1 MB (47143845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e61c44486b182b9e321443b7066db0d06461e0f9f29d65fb8e23a01c966ef05`  
		Last Modified: Wed, 21 May 2025 23:12:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c4be0df6e9990d935a8cd9faf08a55deb7ed7cd796fe9c083431e9c8e8686c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e9cc77926f7b3c4f1f89420f40d430ac02679fa7e73b9f1895e1681156ee07`

```dockerfile
```

-	Layers:
	-	`sha256:e30bf2871ba1e711da59190d64c7b95ef430d92c1c0c177d7301a6725db6d80a`  
		Last Modified: Wed, 21 May 2025 23:12:06 GMT  
		Size: 3.6 MB (3635570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbefd17ba9795afb4b4b5869771ea10bb1c51bb399fdf496470d7a4f75387b41`  
		Last Modified: Wed, 21 May 2025 23:12:06 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
