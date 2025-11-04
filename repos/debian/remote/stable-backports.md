## `debian:stable-backports`

```console
$ docker pull debian@sha256:69788b772b13d3223b82c98def8ddf348f1ac5adda71a356cf2e13614ecc8f12
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
$ docker pull debian@sha256:08ebe383c233f113fb6da3902b8a6af1f217343b5502014ad5d99c9946601d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49285192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59f754ccb325bc3faf5ffdb640abb38262ae7047ef9ad43d6e22df5f6dfb753`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:afbb87cdd2f191801874b88166d2c1be827f36a582a56eac5515989615d0b41f`  
		Last Modified: Tue, 21 Oct 2025 00:20:22 GMT  
		Size: 49.3 MB (49284972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cb47237fa7d733659b6e627be3f8a135cc611e38de912de09b63946ebaedbd`  
		Last Modified: Tue, 21 Oct 2025 01:16:39 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d2fadac2e22143654d2d4e41045950a4ec000ac2a27f9d402e547eb73194b52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837f697abebbf323774a64e5ad96c15fa47ab5b4961fd5797543a92f0b213774`

```dockerfile
```

-	Layers:
	-	`sha256:3f26a30f69e2b5d5aa2bdcfc6a7f0b6092f17b43a26585f489af0a2a83b79ee8`  
		Last Modified: Tue, 21 Oct 2025 09:25:18 GMT  
		Size: 3.2 MB (3170024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae610d4e41b4ed5f453a3c4d131ffac26bf78ddcf6523466b55f98cccbcb8dc`  
		Last Modified: Tue, 21 Oct 2025 09:25:19 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dd8345396cb2d6ce3f7ce7bde65b221eb5eb9c1f2b6122041de818d0cc919db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47449646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574810a1b7f717cd010efc184a819d8a78d8b98451175302ed110fc9dd3203d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 00:20:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:13e2b347cffdfa905cf7541d0015dc671cf86dbf35766385bc92b9d27b7cc42d`  
		Last Modified: Tue, 04 Nov 2025 00:13:01 GMT  
		Size: 47.4 MB (47449426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a914c765a7fa2bf97503d5a6262cc0b4972847689d00398a0df446308ac394`  
		Last Modified: Tue, 04 Nov 2025 00:20:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:63bc22f2cb5a0cfb2ca587b586345612d2ec1c633ecf31087e75c0a2f29ab319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13f590bd05596c8d8f684810eaf13e2c7d8b18d5db68397e4aa750294a1412b`

```dockerfile
```

-	Layers:
	-	`sha256:ad8966ff3f37f5218c6ce1a9aa16357ade145ab94fcab47a98497daeeda52ad9`  
		Last Modified: Tue, 04 Nov 2025 07:29:22 GMT  
		Size: 3.2 MB (3172961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135bfe798fe0a04bb8e8478736844dc4e873eac8c612dfc5482f0c7dc49be7e2`  
		Last Modified: Tue, 04 Nov 2025 07:29:23 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:bdc91f9aed0fa3cca95872e890e4411144d6726e6ae797149f9a342d5a5eded1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45716716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c7bb7e1699895ba65cc1bdd7a7f79fd0ef8db5923dd5742d6c9022ec6c07f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6094e0777f0295fcbea13a084b1536e28eefb801d6edda7518be0248732efc2d`  
		Last Modified: Tue, 21 Oct 2025 00:20:46 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc80795d134d3fd84ea690c85621eb05721fceaab0e206c49408b0dc26943efa`  
		Last Modified: Tue, 21 Oct 2025 01:16:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d65f22b3c26c5a04cd07aeb282f5a5961be2f3d89b8465374687d7f8325aff92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5d070147c7927afa44b27677ff4dde22aa5c729763704f4f5b94eebeb25dd`

```dockerfile
```

-	Layers:
	-	`sha256:845e0e64f30b336fb68ccc0da23d499017a3d1674bae90d6f27497bc3a2cfa49`  
		Last Modified: Tue, 21 Oct 2025 09:25:25 GMT  
		Size: 3.2 MB (3171398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c51b1f2527b42ba12dfca48fac8c745b475b05ef4f25743697fcf161ad775e`  
		Last Modified: Tue, 21 Oct 2025 09:25:26 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0c035facdf8a379aebbecb051721e2647075411775654f0cf0e99ac5022d7429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49649969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de6adc5af1798333e8bb3b4918bdb3c48c529904a3150c366274fed0559d665`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a0638943724c7e7c3cba9ffd5318b66135dd29e2137f84f824fd6ff1d2ee2dc1`  
		Last Modified: Tue, 21 Oct 2025 00:21:50 GMT  
		Size: 49.6 MB (49649747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0836dfcc2ef48bff09cc84b3c1ff10482ec5471ec1c6c254cf126b1b5f9372`  
		Last Modified: Tue, 21 Oct 2025 01:15:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f09dd9a0af8e7861461555f6bebc04f8535af9e412cb9fac333afdf95ca1e79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2d117e0e817371c94dc75b62e72e123160f8aca469c5a5a3f70587e6b57ffc`

```dockerfile
```

-	Layers:
	-	`sha256:887f9242318efa54f610098da0533a5de648376fbf6456b6f233cbb9e0261350`  
		Last Modified: Tue, 21 Oct 2025 09:25:30 GMT  
		Size: 3.2 MB (3171505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd97b2dfadcc86d0dcfdbdaa0bde27221a3f373e681221e405eeecbb7d44aa4`  
		Last Modified: Tue, 21 Oct 2025 09:25:31 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:510a4ef004a01cc926519cf6d7b826407a12c0c4bd6d8c44b0ae75777a18175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50800790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24077884a7b2bd41090cf47c9f2c635cc7afc668424b91908e689d87bae737bc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0f2e55b7c7d872a3f5eae1640c0e45576dc89bafd5a3013866011959473cdd09`  
		Last Modified: Tue, 21 Oct 2025 00:20:42 GMT  
		Size: 50.8 MB (50800569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b95d78088087ef26510af1a81762b25d14580bfb6b47e72f3ae4a6a79de992`  
		Last Modified: Tue, 21 Oct 2025 01:16:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:163d7aa033a8940035b7448bae1cef7fcd6d2de74bedc411e13c05f24f638938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463706ef76dc0bd36e2826761ff5b0941a1900a64b34c85012fae9d799a26733`

```dockerfile
```

-	Layers:
	-	`sha256:9872c3d1da2bf0efe202fe63c6a4a948c91a45d92da2028fb7b79bd372707159`  
		Last Modified: Tue, 21 Oct 2025 09:25:35 GMT  
		Size: 3.2 MB (3167227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4092cc364c42bdba03b9ed8748807b9b8856e67dad68abb3ac2e6a710b6d8faa`  
		Last Modified: Tue, 21 Oct 2025 09:25:35 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2ed85bf8dc961602c912a03992d48f722a88dcedfb2936acc9060bc24fa7e9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53109700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb43d54c709127f916fd01d4026380910f4738cb6d87d2e2d64b1f5e12b75629`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ca94fe6a275d41a3b12e4c7e00cee592d38d6155166afaa561b4cff2231ce178`  
		Last Modified: Tue, 21 Oct 2025 00:24:25 GMT  
		Size: 53.1 MB (53109480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cbd16019fcfc11d5304fb60e137cd43ac9ab20bc2169f5df05eee4afe88042`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2e984b6a3a691eb338ebba4826fbb5b98c3c5d1cb15883c3774733e2bd64a769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cac4d833cb6ff0f4300a5e2910a2fb2b17d9cb38f8d0defceac3ae455ecd1b5`

```dockerfile
```

-	Layers:
	-	`sha256:69ecf7a5d0878a17e39071d31864f45a75721660fb846cb46c3f84636804c386`  
		Last Modified: Tue, 21 Oct 2025 03:29:50 GMT  
		Size: 3.2 MB (3173535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eeb143e68340d6c437d5c5183a2be1a98f80dcfd907ea564e73c252b7806ff5`  
		Last Modified: Tue, 21 Oct 2025 03:29:50 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:5f126f829a845f90a79c63505d39e21617d417b2cc6d65f209ee0a16a940f197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6ed5b208ca305e1295c6fa53aa31facd806a5d67d24104c5fb0d39020ecbf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1762202650'
# Tue, 04 Nov 2025 01:19:49 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2528dd148b36df470732f8eb1cfdb230a730e032a76eca2a67e06418aa90966d`  
		Last Modified: Tue, 04 Nov 2025 00:20:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df5e1135c56b98ef321591b1f814b331ba598ba67b93771605ea303b474859`  
		Last Modified: Tue, 04 Nov 2025 01:20:49 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b4c78ba1f23b9d8cbb528a2d3e83ea3f1bdec9e7f7a8e455e110a938fe292f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0201a99de425e4e98bf4253366107d6c083d4dc1dac789eb0588c5fe4605d7b8`

```dockerfile
```

-	Layers:
	-	`sha256:717678815fbcbc772143e2182cb1ae8f648db492f4ccd1f9c44be47825fbbc73`  
		Last Modified: Tue, 04 Nov 2025 07:29:41 GMT  
		Size: 3.2 MB (3162347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0e8d750da6bb9fac0ddc80a0fdafdc65eb9d0630d591e30bf5874eb693b91c`  
		Last Modified: Tue, 04 Nov 2025 07:29:41 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:cc912186db07cdc73d1ab39a122fb53cc9a6a7dc1e602852df5ed7c442cc79af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49351921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac7bd81fec7f986b41378d03c4939271c7a0c1d6905f10fbf980b1cdb8bb91d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8e1220200624cfdd58d57667ccbf998a0f86f915373fc900482a65672f078f95`  
		Last Modified: Tue, 21 Oct 2025 00:25:36 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e9c8204480f013c60ba96d3d3a69d32c3826ff5385d07472180b0d262e2178`  
		Last Modified: Tue, 21 Oct 2025 01:19:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c550dbd5211ceeadae1e393db15aded05ab293d879b50a509cf9a8a1a189b94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9a844ffc9849b5eee664ff59d356e4fabfd28cadad93e1576cf8d72a30be97`

```dockerfile
```

-	Layers:
	-	`sha256:dd45a5efc37443c772e90e3b801b55a83a6575f226765879e021a16eb6fbc2f7`  
		Last Modified: Tue, 21 Oct 2025 06:25:04 GMT  
		Size: 3.2 MB (3171471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7559f65f9a24bb59614743b66c467ee725c1aca744ed27d6d304dd44094689c2`  
		Last Modified: Tue, 21 Oct 2025 06:25:05 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
