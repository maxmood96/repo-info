## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:c32e024888128335f6f733ca42fe337dbd2bc0ae24f08f5b0ed17a478c385f36
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:9698004e26789aa8cd692cebc22e45af207b82e06832e820f442f4b85a16fb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd4972531e6194ed29ab5660143815ca0d2d65e17ad124128133aae5552d068`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4960e211f437dcde4551063819c86cad34ece69ff51b6f8afdc74dbbc120ff0b`  
		Last Modified: Wed, 22 Apr 2026 00:16:15 GMT  
		Size: 48.5 MB (48488633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54427b75a30f079e0372c937868596ced3959341a0649007aa927ce6dc3e330c`  
		Last Modified: Wed, 22 Apr 2026 01:15:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:eb8f5b214a6f54190065acc14df5ac8c9b9b4fc87c4b7dd91dd280a29d730a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b62b9adb86e9cff6fc3476c64a6357a789071206e36e78ca0f4e384bc27c0f4`

```dockerfile
```

-	Layers:
	-	`sha256:f67246d2b9666db028e5893b324119d798811449dd397c33b663cc670340a84b`  
		Last Modified: Wed, 22 Apr 2026 01:15:25 GMT  
		Size: 3.7 MB (3734076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0d60ae876c281d1a41f4c01b62a41ebc65dae58efa08d100b9d3aef0c90eb9`  
		Last Modified: Wed, 22 Apr 2026 01:15:25 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f35506123f28543aa8c370b2d6a4fdc0951b3f8a5889c99f865a6a3d6f58ebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e36dd863e5ac66b0e332f0729dc272740f2216ae66cf9c21b03faa3116af371`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d0438a00c8d0bcb131fddc4640e8e6c18b232661f332d650491b91b0ab603d5f`  
		Last Modified: Wed, 22 Apr 2026 00:16:19 GMT  
		Size: 46.0 MB (46021505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0fa19e00b65d3d33006b565f3534035df7cedcc44609222527c5f19454e80`  
		Last Modified: Wed, 22 Apr 2026 01:15:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:eda11322267e2f1360a2c5e4e019c76f10024740ab6f71ecbcf08bf67cc98318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbbb26705a28edb6c7efa59b5832fa926fab43ce37221d705a365d4e71269f4`

```dockerfile
```

-	Layers:
	-	`sha256:90bbfc4b8ec9a6c105cf5e49e0b60a694af3817efc9abfa1f06477f220862cd7`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 3.7 MB (3734277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876a41275d28f63a608cfd5eab469d660a9476c4c49eb0c33753dd19ac1a02a0`  
		Last Modified: Wed, 22 Apr 2026 01:15:19 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4e258a635ed2e8455d0313413f375391380956a43075262801fab530f4382e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44207887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6057377e9cbdbaf4ad21fbd021579302a53933b99e483ead042b054d93b1e41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:17f0cc03124c4b194e862070c9ab8c1bb328b264ac1830df2f0bacfbde21e15c`  
		Last Modified: Wed, 22 Apr 2026 00:16:52 GMT  
		Size: 44.2 MB (44207662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b64681e5d558404809c610cdd336199d97bdf4a8a467db788c1c0f29b7bfd90`  
		Last Modified: Wed, 22 Apr 2026 01:15:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:14d2b35feecec1fdd3ad2992b31ba19e5bd4565b38ee97b32c3dd5f03ee2c303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc25c597cb392a6dcd578620510a5815f2e5fa30369fbe7c9fd7eaf8883e68be`

```dockerfile
```

-	Layers:
	-	`sha256:e4f1b70336cbe0f1ddb7cb6472b44c7358141fb96a821158e2dc0a80e055622a`  
		Last Modified: Wed, 22 Apr 2026 01:15:08 GMT  
		Size: 3.7 MB (3736255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b323e3db9a05ebc47f2cf4eb3c8f1130f9830928f6d6200cf8518935e80c9247`  
		Last Modified: Wed, 22 Apr 2026 01:15:08 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:85e6b062bce98e42f954299e09b528ba6b117aede99bfd10ca77e6ff0409653d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a291e895467dcb5e1a55c25ec581463a4ea1ad0dcdeca9ec241451c7b455310`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6affc13e8d5d2c38d0b9e7dfff8b87c9499f2b8370fdd1ef8e2fae57c8a6434e`  
		Last Modified: Wed, 22 Apr 2026 00:16:16 GMT  
		Size: 48.4 MB (48373075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ff5d1214dba3c21c4667d1b4f824a91a1aaf071577c5c7ca2b9b87686bd4a`  
		Last Modified: Wed, 22 Apr 2026 01:15:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fa5e880822c147d754233d7153d8b7ac75d99045a0efeea43b9cc35d551b5674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96e79ed026a54ee1b20e1ad40d68ad246d233243fdaa5579af174b8150e5ede`

```dockerfile
```

-	Layers:
	-	`sha256:18cc4323fdb259b8701f4005065857eb55a34185d55079ef5d3b82ebbb9e33f3`  
		Last Modified: Wed, 22 Apr 2026 01:15:12 GMT  
		Size: 3.7 MB (3734291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b2712a4c879c5eae8dac63b72808db73ceede739006ad7ee410c6f372e5c78`  
		Last Modified: Wed, 22 Apr 2026 01:15:12 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:6c4de1a26a9d720f6e56ad92d68f591171197e5196c4e2258e7f052d7f1e2c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbb59494abddbc7179198db806760d0e2cac15a13bd471b7c4a1a151e185c4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cea13026aa2eb8d858777d290cf199373f4461b9aa2213bd971259b390929764`  
		Last Modified: Wed, 22 Apr 2026 00:17:05 GMT  
		Size: 49.5 MB (49477721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c4833258d2c5fd6440b9ae71a967b746f0fa1d69c287b00a5c82ff29a58c53`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b48291f8ac74b6782c2a874423888390b8d122e772e5891141b6e72e7608c12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8a96418b3ff1753e81e4113a74dfacd5e101cd4aa22ad29cacea9ca9d45450`

```dockerfile
```

-	Layers:
	-	`sha256:c473edbdbf4fef99e2f909d7fb630c14360585d5826ad5e775234f43d90c64d0`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 3.7 MB (3731272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6beed641a8876f8155be637466dc7a5647d7b78712fc1387e76cfd49bb142a6d`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:253dfae5a8e3a5b10ce7ade6893de48a858f82a1e18a468ebd4c333019b9a934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ec007a57166a8ab8dcb142ce696a748e76e370f55d0e31a7a3f54c32c3162`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1777939200'
# Fri, 08 May 2026 19:15:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:36b0e902bb102cbef4bd7c716577263d6b4efffad6336b549ba104e261c3cb67`  
		Last Modified: Fri, 08 May 2026 18:20:36 GMT  
		Size: 48.8 MB (48782515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710cce78964966e31fe7e7a7020a31f27d8e63b781b46f0184724653aa0cfc48`  
		Last Modified: Fri, 08 May 2026 19:15:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:451f8405dcd4ae733209b4f2681203f2b22241090060aaf4a7f9922397a63cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb44a8c3b2fcf70c0d87988415afa5c3fdbdb1df8d2d6ed769f902f73c8feb0e`

```dockerfile
```

-	Layers:
	-	`sha256:8abe634d6402506d9d4caadc7386a94d72191cb95b2adc2a578a6c7d01ebcdda`  
		Last Modified: Fri, 08 May 2026 19:15:39 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2bbbaaa16a2e4f1bb3fb87c30ded35d204f669e80ecd43f9e7a2327397215585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52336965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918aa6126102c89ecd36e1c09615f45f079696cba7e7ca642e1a989e2c8adef7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1776729600'
# Wed, 22 Apr 2026 01:15:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fc80edcfb14ca8d802ceb5cb47918958be873e5e92ba96a0548ca86d03e94d3a`  
		Last Modified: Wed, 22 Apr 2026 00:16:12 GMT  
		Size: 52.3 MB (52336740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b64681e5d558404809c610cdd336199d97bdf4a8a467db788c1c0f29b7bfd90`  
		Last Modified: Wed, 22 Apr 2026 01:15:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:345cc0d2734a9bb2c75853dbdd6e946b87b7f00ac061b1917afe037d118794f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb42f290ff65a18a28764e66130c7b3c773d373debb41d266227ce786a6ec27`

```dockerfile
```

-	Layers:
	-	`sha256:699640dc0b9e076aa5ef5f35ed6504ac54493978d7e5813c739bed944510d41a`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 3.7 MB (3738434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f87b5940124d632c58e3583e937a37aaaac56012e331451a0770c78f31f687b`  
		Last Modified: Wed, 22 Apr 2026 01:15:20 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:2f25e764f8459e9b0fc6321e3e4247d083ec52ac9dd5d3a63f0b1038d7770332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926ad41487fd56eb6861ff306709b4cbb1267e201e49b984935de6135147e805`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1776729600'
# Wed, 22 Apr 2026 01:14:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a2f3f40a94ea8f4c96c38cf1e0d0c0a33d6afd63a04903589d0a2c0c6e484f8f`  
		Last Modified: Wed, 22 Apr 2026 00:16:04 GMT  
		Size: 47.1 MB (47147974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51730503edc9a59646526d489cd38c01b6dfa0815990cbc6da0f491219d5d68b`  
		Last Modified: Wed, 22 Apr 2026 01:14:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ec3e46cddac57ceeb26e81bb0b8d7a152d7ff06cddd428e501ce7c24fde7eee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feeaf5d5ab15f9f38514b4b6ab678e4aae48c90a93cc25ee1dd96b7c50a06389`

```dockerfile
```

-	Layers:
	-	`sha256:9e28060042785ba6834eab74c422e253680b694fae3ed4745eb8e36ed02d7c7d`  
		Last Modified: Wed, 22 Apr 2026 01:14:31 GMT  
		Size: 3.7 MB (3730914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45856c8731b9f7c74f713978d5b43bbe6466732fc25dcd0141b5b4c66ed4c1d7`  
		Last Modified: Wed, 22 Apr 2026 01:14:30 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
