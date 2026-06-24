## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:f76ad6f377335354862c0ef2cf4f2cedbc8f432d12b1fc885cd52e925d53e661
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
$ docker pull debian@sha256:82b3889f2c7637b2128a54f69d2c3c04296ff392df13e806de9bf1d63ba47877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48502265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6667ce939c340bf3cf905bc5939db81d832bb14c5610e358b8fcd7473b30f5ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:15:06 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896a686970712580ac4d61e3a65f2e455cafb3d11645fbe6bc3acc924256f63b`  
		Last Modified: Thu, 11 Jun 2026 00:15:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:df96ea7a17e4af5bc70c03880f96bde15ac076145c7cadabe7f0f3b85a8d512f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770e1531038f9f428f3b0aeb1b03fbfdd68914fac8791e76ebf959f4040c653`

```dockerfile
```

-	Layers:
	-	`sha256:056475c1bb51069f740942d21960ad83cf9276d93c55d4ffc3b58c5e75fc91d1`  
		Last Modified: Thu, 11 Jun 2026 00:15:13 GMT  
		Size: 3.7 MB (3734110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9302099b7d2d5607a0865d6feb15f5d44643d70e8ccede4fb2dc384994beaf`  
		Last Modified: Thu, 11 Jun 2026 00:15:13 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4263903d8cce16ea939d5a5e8e8999026e4c003ba06ea42770f241b934b19718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46038412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c8fce92982526fca7861d67b429c8edf0ca2ea3ec7dc30b83836055b5cc168`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:15:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3683b8a7792857dc507c3398919097537c8d564a235824e722ff16657599fe21`  
		Last Modified: Wed, 10 Jun 2026 23:38:13 GMT  
		Size: 46.0 MB (46038189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad149888a7977abb391f51604be4b50e777e17fd02e68fe477b2a423b53e101c`  
		Last Modified: Thu, 11 Jun 2026 00:15:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:02627ddeae12c6f260b560a8efb1c1191643e2537820539b5ab84c356d945c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553e3730adf1e51ede71d205f2eb6d4bb840f707c8c7369d83ded1dc52a4ed3c`

```dockerfile
```

-	Layers:
	-	`sha256:82b1d3060fa3e215808cb9c3613b0a0d0461e1fdc35c272174cc30c4c9270813`  
		Last Modified: Thu, 11 Jun 2026 00:15:31 GMT  
		Size: 3.7 MB (3734311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffba6aa195fc9c1e7f0a4a3df992338cb79dfc3cccd78c0cbbae409e902b61a9`  
		Last Modified: Thu, 11 Jun 2026 00:15:31 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:76c3a4cdb5a49d966a59a7e255cd94c33a8ff7d0a9689e73b8b89e482263d71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160cf0e4d5856f747cbf58cc6f7989141afb00a0f62452543baa4ed0cd9f0e58`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:14:58 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bd062a844a2aa95c7f7fd9f55cad2cc75f32547e5923b093a7ea04b6e7583b`  
		Last Modified: Thu, 11 Jun 2026 00:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9eca6621c47b22798a51d7424ce707053a60134dc26f8dba287ba7fe783dd680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f48fc2ead00a91178698f6a4ce2fd8952ae37ae1ec075f690b7858b20490f4f`

```dockerfile
```

-	Layers:
	-	`sha256:e1286610e5fb02d7563e7f2050f2c1732ab7d438e91cf7541814ad5536b0e93e`  
		Last Modified: Thu, 11 Jun 2026 00:15:05 GMT  
		Size: 3.7 MB (3736289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a19786919cc815fc76b6a0b4df4082ef86d2783ea45503f458391d749149d2`  
		Last Modified: Thu, 11 Jun 2026 00:15:05 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ac8012b067e7d4349e0f9336f5727488448c674e9b5ffaff5a4b2fb9b4f1401c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48389239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22fee9dab22a294d0ddef2b1f9b7c0a3db64cf2cf03faedf3bada42e877558c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:14:34 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc5f2e18f1c90fce9b0f2b04c5dbf8842fc1a9a270534f703c4e0f6e3eb3bbe`  
		Last Modified: Thu, 11 Jun 2026 00:14:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:88dd73a3df40e4d018cad35a190e9a5e3c424cdfd5fc2583bf5f41d3c84a3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4558fcce5c6f5a7bbed856ecba4129c841cd8edd1a21ac2bb8276ea46c17bd56`

```dockerfile
```

-	Layers:
	-	`sha256:0c1f9297424a73e669cebd30bcb253c330d45292fc8d80d13094d945c3483200`  
		Last Modified: Thu, 11 Jun 2026 00:14:41 GMT  
		Size: 3.7 MB (3734325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:532a02f8d57625f967976a3dd3011175266878bac2298cccdd32b17285bee72f`  
		Last Modified: Thu, 11 Jun 2026 00:14:41 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:5d12edcc07b9584ebe911b59ced4b0405be2452050d95477e18296d5fe982977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49491603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb9e80ecfe8e1f6a0e469ed0905ea04cb1052b19ba5dfb608679269e4535f62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:14:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:96cbacad9c1883b9ae87f68a0550ac0bd7e0b7ba2b15b142a793b89b5a5f36ad`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 49.5 MB (49491378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a6e71d6fdae0067ca7814009e714af79636f0fda964fa691fa61569b29c09c`  
		Last Modified: Wed, 24 Jun 2026 01:14:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:721865f144b873f366bddda340b0285c2cb116cdefa1e3f2f72cee44aa040c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a10a3a20ae0030292514394ffd7a7cc95fec599192fdf9850d9329130bcab69`

```dockerfile
```

-	Layers:
	-	`sha256:41ca9b63a1fc73db232822fd8241c1990d98eef22ae0ba39bdf17ac2335e2d1b`  
		Last Modified: Wed, 24 Jun 2026 01:14:33 GMT  
		Size: 3.7 MB (3731306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61497b1a342c44c5e8863dc36e2e995e140088e513a6a6a78389f2870cae2b68`  
		Last Modified: Wed, 24 Jun 2026 01:14:33 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:94b2632f6c45ae7d3f4ad33cb5dcdc5d5298d41048409eebc2cc9afbd4c40e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48793042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2b65d43117852a0450ebdd638c3f29f9ce54669921e15eb89643253edcf88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:14:43 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d06e8744a62761c63cdcacfb2a61022e2f4c0aa854b6cede18fced28342dc1b2`  
		Last Modified: Wed, 24 Jun 2026 00:26:53 GMT  
		Size: 48.8 MB (48792819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce86d6711cfb8c47715a9051926dc92ca2e565536ae48a851f806413902d840`  
		Last Modified: Wed, 24 Jun 2026 01:15:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5c4ba1501b7c10458add9eeea3ad1e69536dca578009916847761f00079b2c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336f1b074cb734d15ead68b8f84471db6eb4fb79e18ff5f840503c7458869d67`

```dockerfile
```

-	Layers:
	-	`sha256:8e42843955b81f96a9bea22d71bf74ff6ca0db0186e8b6a0aba76f539a2ed3b7`  
		Last Modified: Wed, 24 Jun 2026 01:15:01 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c6313af6ed0a6c387c9fc8f1315cdfe0e43739bc28807385a72dd5d93d708808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52347070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf6ef11645ca82ce10c6d265629e3add02704f830b5a3dce52034aa8a22aa53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:13:36 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40479814124522186531436de9ae56ee64f96c48c141f9304c560120d9da7e01`  
		Last Modified: Wed, 24 Jun 2026 01:13:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:253941af09d5ba9774d100eba8f495ff87d23d7dbdcd49afeea24c2231bdda49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39356030da2d629288dd26fc8132de53b877fc0aa15338fb758e45bd15ddb671`

```dockerfile
```

-	Layers:
	-	`sha256:e7fdd975f4938cc3d888cb449fcefac7cc56c3a391985ee5f72a338fc48bcaae`  
		Last Modified: Wed, 24 Jun 2026 01:13:57 GMT  
		Size: 3.7 MB (3738468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0b2bf392296c0e3328182eb1f12b285652549206d0926297261779bbd2c5f9`  
		Last Modified: Wed, 24 Jun 2026 01:13:57 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:c5ca198c062adbea520d41efe5f0319bd851139418b195a544c3ab300bbed58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47161898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a1235706ef2b2e5283cf289b728012e35144e7de9f7788efc364875fae9bf3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:13:56 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de485312453cda759dd6e86786aae42c606a06b41c7d477f1fb8991e8c9c6fd9`  
		Last Modified: Wed, 24 Jun 2026 01:14:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:23ef3bde979dd726711ad86fab4a0178fe65535335934a0bae5efdd600d94eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd50d01fb909df785b6b4c3f2a8cdbfc901a0721319aba0eceebc265d2cb47cd`

```dockerfile
```

-	Layers:
	-	`sha256:3225757a0ecc229ee6c736ca68806532fcc263c69507482d8584bd2ee93dc55e`  
		Last Modified: Wed, 24 Jun 2026 01:14:08 GMT  
		Size: 3.7 MB (3730948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6ac67469643ca4f439b8d3e08aee9259181dbe8ef98aaadd5e3faf8025cce8c`  
		Last Modified: Wed, 24 Jun 2026 01:14:07 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
