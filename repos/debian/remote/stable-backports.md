## `debian:stable-backports`

```console
$ docker pull debian@sha256:422418d6032bbfc9ba0956490a56f2fedc199914c787dede6c36ce6cca0473e5
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
$ docker pull debian@sha256:02d8e97c4279e5d7171a83cdc01261a15495e6f4ce86a7ac171c89cfbdb5009b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a1245b1ce791b3a300439035fe0412ecfb1ff17ac850bda6e416bb9b668917`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1765152000'
# Mon, 08 Dec 2025 22:31:41 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f908b51d7e52bd5026eee2895501c9f641f07122a96322ca65d814671eae1e90`  
		Last Modified: Mon, 08 Dec 2025 22:17:45 GMT  
		Size: 49.3 MB (49289515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce66f7d6bf19ae8ad09e6f53f98de1174b0b0027062904b32c626423e99c620e`  
		Last Modified: Mon, 08 Dec 2025 22:31:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ab6942e726228cf3e236bd0470ee95e06030dd97b25310513c53533e806b8cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4643fbb37cae42752748cca010ee7f1e0ec0c5d9aece61b7e5b0b2d0b4025176`

```dockerfile
```

-	Layers:
	-	`sha256:d683bc4705d5c09e9ed71d092b58454e89843320dd5d6648dd60ebc876598194`  
		Last Modified: Tue, 09 Dec 2025 01:30:39 GMT  
		Size: 3.2 MB (3170018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9a51d3a7a3db0eeeda98f877fc6ad6eebe1955894ae1a56950a0e84bb61414`  
		Last Modified: Tue, 09 Dec 2025 01:30:40 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:1250afcb993bddab7cf6bacd9447524a418e587438cd76b2e6d276fe5b656a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149c411896a00d50b55c87b5ac4b36fc2c226f64cb1072dd923716115b314cd2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1765152000'
# Mon, 08 Dec 2025 22:29:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7a2b110fb30c1f0db71bd31fbd2e321b0bbc414b2b929bb7e145e22fa16c2e96`  
		Last Modified: Mon, 08 Dec 2025 22:16:38 GMT  
		Size: 47.4 MB (47448722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035a2291359e67d5f2f469619dad308d6766dfc9f13bb9227ccdffd27b8454f`  
		Last Modified: Mon, 08 Dec 2025 22:30:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2f59295c3cffb3ffda5501ebd8b9a5c2a75098dc7da687254e216f2ebfc68828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9b4a44aaed14c4dc387e5fff70f42ea7f9c9eb84486e089110fa5c304bbd9f`

```dockerfile
```

-	Layers:
	-	`sha256:5ae8aa74a9f0fa756b2c02efeaf2d5badb37152d63fea534cc4ecc4c0802309f`  
		Last Modified: Tue, 09 Dec 2025 01:30:45 GMT  
		Size: 3.2 MB (3172955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e14ae6d9a23a8563cdecacf3b84fcf1d29a237d80ed35e94bf093e6d5336a504`  
		Last Modified: Tue, 09 Dec 2025 01:30:46 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4ea4172468754caa9bcbc21a7e327ea71e14c70c0f9b34b7bc31eaa360bf2501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45718508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c721504d9a3193c950ca4b9a24fa8ccac95330699a258a6ad1f2550fd21a74`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1765152000'
# Mon, 08 Dec 2025 22:32:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:276317f36a7dfd6a625608e209230ea7e4132c1c2f7f3add2fca7906530700f4`  
		Last Modified: Mon, 08 Dec 2025 22:16:16 GMT  
		Size: 45.7 MB (45718287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad716f0fcb34336a1716fbad5d42c4781b755941fc55953d46638b60f877c74`  
		Last Modified: Mon, 08 Dec 2025 22:32:41 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e3993c5f238298417be5ad24ad9d2442c37376fe3f751fdb2ed5c62e1fbe5a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e352fbd6faaace6c874c6360731c5d9f5ee8d34c7654f14016a762e1a653acff`

```dockerfile
```

-	Layers:
	-	`sha256:4ce8bff01e7beca0441f792cdf984020a82cd8e81bbba6e91b135a8ec672a7e1`  
		Last Modified: Tue, 09 Dec 2025 01:30:50 GMT  
		Size: 3.2 MB (3171392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ed3ab5e1fbae938d183eab7d1198cc4a1ae31f99e67eb836d186d7b1adfd44`  
		Last Modified: Tue, 09 Dec 2025 01:30:51 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fba75623eea9102a5525802d3337b9f6442c85302863353d10d44b2b1c1006d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49650442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e63ae774622389fd0c755b3e967f91c35da55fd9a39ab33d81b21bc4e080b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1765152000'
# Mon, 08 Dec 2025 22:32:42 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e40276d4b9407d069e1578ce891dcd1f968fb641c1d0b7ecd35d83f324bf505b`  
		Last Modified: Mon, 08 Dec 2025 22:15:58 GMT  
		Size: 49.7 MB (49650221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d8ac9496f6cdbbd007f166cb8177c9bd4f4e1e23a8c4f2a909ee501c3ed80`  
		Last Modified: Mon, 08 Dec 2025 22:32:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a9f6565f5766bcd64572065e67240de2f3074612fa9c70dd5b222220b2ccd300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb1423cb1780d87ab30616be40d5e0aba3df5df2f8c14919d6ac77753ad3ba0`

```dockerfile
```

-	Layers:
	-	`sha256:d40ba9bcca88c68f717943e22583d99f70c0e59584b7e8b880a2d300147cb46a`  
		Last Modified: Tue, 09 Dec 2025 01:30:55 GMT  
		Size: 3.2 MB (3171499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5380d8bca8e5b2e2245c95e717f8424dca7d209e0f89b1dd4ee55324ffd5a65`  
		Last Modified: Tue, 09 Dec 2025 01:30:56 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:9143ec77778428e14f017c17fc474f85d5fe5a969cb11bd14ad8b33b0dec44c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50801864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac1849ed30a7582d2d67c41d27ec19c44dd5f0e896dcde6676e626b264f7e0c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1765152000'
# Mon, 08 Dec 2025 22:30:09 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b12c9336f6ae82b5f05539982fd86de6f504b774493823ebeb620b54c299b7c9`  
		Last Modified: Mon, 08 Dec 2025 22:16:42 GMT  
		Size: 50.8 MB (50801644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4c226ab59bd8fdcb36af001534c21f5edbf7aedc643ba6d90549c2991be837`  
		Last Modified: Mon, 08 Dec 2025 22:30:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:03530688f60c1925031a57730fac171d4611edb41e10e7980854ff817df80946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82493222008c113f5decee08b5b1879184e7379f2fd7c18be9f6b405cef4867e`

```dockerfile
```

-	Layers:
	-	`sha256:430d19e87452052c190f901ff56a77548664a69e9fb567880ecf67ab57a91de8`  
		Last Modified: Tue, 09 Dec 2025 01:31:01 GMT  
		Size: 3.2 MB (3167221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9f51b44bef688df9db408cbc656466094cb5ba82f9d30a25fd55d848093600`  
		Last Modified: Tue, 09 Dec 2025 01:31:02 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2d429f4117a2a2f58bf9d5091beea673ac59784c63795d3f2bc300c002503ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53108708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37595cac0c453bc303fb66c60c7300a82c9cdbf58a043fd148f1cf008e632ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1763337600'
# Wed, 19 Nov 2025 03:09:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:03ee59299e89b6be7fccae2f2c1295890dc1568644438d7cf367cc54571bad12`  
		Last Modified: Wed, 19 Nov 2025 02:56:38 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7c0818f8caffa49e68adaa69a4323cde8914a5196c25bbec4c1671641d4944`  
		Last Modified: Wed, 19 Nov 2025 03:10:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:67ec66eb1dd2bfac27f0e0f56c8002ebef47b671982acdb5b349fdc6c832e37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd815f5f39325a49a091480429c0b72431f01f38537585f83c4fd8dd949fe5d`

```dockerfile
```

-	Layers:
	-	`sha256:1b002cde161adbecec55417b2e06c8159e39f99d5328a52ab71633de56350f94`  
		Last Modified: Wed, 19 Nov 2025 04:24:35 GMT  
		Size: 3.2 MB (3173529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3071fae80b922e2cf03287f56bf79b796ad070027a3e02e245b33c127b0d3779`  
		Last Modified: Wed, 19 Nov 2025 04:24:35 GMT  
		Size: 5.8 KB (5808 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:78650b07111dce419494c533cc4c25fc218a01fe436d787fa95598dfdfd5616e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d46500b81c8ffe0b9313449dce344bee6a576001fbb11f43dc8b41bb4ab3ca2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1763337600'
# Tue, 18 Nov 2025 07:56:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0097f4f57d7b72ff21aa1d700ec81c45dc5b93e4075b869b7b9e06d2ed964815`  
		Last Modified: Tue, 18 Nov 2025 01:38:25 GMT  
		Size: 47.8 MB (47771196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7822a16031b14ec8f8c1bb03975d48c774d8772a3bc7d6c6feefe8f903f42830`  
		Last Modified: Tue, 18 Nov 2025 07:57:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5987eecb38cf8b16fa77cd58f4dc5626371676bab41a9fca7855ecf2ae7241e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6e07ed5fed97ee584d60829583e1d3e22fbd1f705f21a2f20d278b116a1ba8`

```dockerfile
```

-	Layers:
	-	`sha256:3ae2319c6c4d8800e4ce4586b6425f021bd91b1b1ae4269a2f13a88ad24f3bbf`  
		Last Modified: Tue, 18 Nov 2025 10:26:25 GMT  
		Size: 3.2 MB (3162341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e90528081db7226b2d7ba019238d0bd4af32e017934b6242a6c5406a05137d04`  
		Last Modified: Tue, 18 Nov 2025 10:26:26 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:a77e0e08f896937469aa1a71fbb264ab6484692fcef71392ba441626e5ddaacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6ba29e31c74f4470d4651a7e9293420fadce0bd694add11bd563248e502ab1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1763337600'
# Tue, 18 Nov 2025 02:13:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3a0c301a30ae17916447993faa87319010c0e6222a5c30eac3f5c06f5ec59507`  
		Last Modified: Tue, 18 Nov 2025 01:11:57 GMT  
		Size: 49.3 MB (49346016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2fb2a44d6b53c7f9c9d75eb3d1962fda44eacca21252c419f716af9f1a79c9`  
		Last Modified: Tue, 18 Nov 2025 02:13:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f12d1b46f138a67285be238e428f0ce5362d9df562e8b0204797c5ebc0c9da48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1085336baaae52eedcaaf5acb4cbfe6659d53e6aaccedc9b6443b16831b22af`

```dockerfile
```

-	Layers:
	-	`sha256:825735e21610a78818e196b8fb0deb28cefca558a3be1fbf5691be63dfa0c6fb`  
		Last Modified: Tue, 18 Nov 2025 04:31:57 GMT  
		Size: 3.2 MB (3171465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ac36b6ecf33ef94e94d5df8ced75443644e8c54c6029201f30c116a7295997`  
		Last Modified: Tue, 18 Nov 2025 04:31:58 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
