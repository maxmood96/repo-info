## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:d072d7a4cadef784362dc21de80b6f5757398b9a8b31acd6d5070a9a2847e6e7
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
$ docker pull debian@sha256:f5d35bb392244cd3e8367d42a59a08b53d433a3c5a0458f32862ab625ee099ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d501722ed9666e959c0d92273a6f0883f5f16e5aa6e3837273697589fc539e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:32:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:193b03692450e7cace4d0d2ca1fdfa555e6b02853e20cbcc770433394c1fdf06`  
		Last Modified: Tue, 07 Apr 2026 00:10:35 GMT  
		Size: 46.0 MB (46021671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f944245394f8cdaed87fa8ca28cfdc08c0b64bace0616257322f34f3823a23ee`  
		Last Modified: Tue, 07 Apr 2026 01:32:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8ae45feb2d9b6edce3ade30837824c045b8392be35b038cf758aace57f7f5d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68e7ea14110a93ed36884aa40a6f51886d824466ec72d4bac35dd772acf7907`

```dockerfile
```

-	Layers:
	-	`sha256:1218a6ed74ae952424afaad2bc5e581888ebe20680e3b5b9d71ede44a14c4f7b`  
		Last Modified: Tue, 07 Apr 2026 01:32:17 GMT  
		Size: 3.7 MB (3734277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:156e41a0cc9b730937de748b20ea962eefee4b9a1b4b3c40c9809c034b4c93b7`  
		Last Modified: Tue, 07 Apr 2026 01:32:17 GMT  
		Size: 5.9 KB (5865 bytes)  
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
$ docker pull debian@sha256:734c8360b46cd2759272019708588c050901f2be6bc39d1e649642a86a9e01ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce404188828baf5899deda219d6dfb88fd12271c4b4071b9d1758eb99bb35b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:15:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ac7efe00f580ac8e3b05db2c37237fe430575ec0c60c4d9e964da81fee650aaf`  
		Last Modified: Tue, 07 Apr 2026 00:11:44 GMT  
		Size: 49.5 MB (49477920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1178e823acfd31c92b4a0019a972746b6faef6178c48abed99a61fdf9261dec`  
		Last Modified: Tue, 07 Apr 2026 01:15:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4a582907dd2284430dcf87b5e4321c2c4feab4121f12784a59c1a982d3d191b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ffe5d1a72476d70f3e48a5f7433c4d9bf4636b08f5430bb5998037d25be397`

```dockerfile
```

-	Layers:
	-	`sha256:5645c2efc7581127022735a7a6a277a9dc42503eb5416117516e8e7e99d03c49`  
		Last Modified: Tue, 07 Apr 2026 01:15:52 GMT  
		Size: 3.7 MB (3731272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c96004c6a7bd7412cef4c4688a1cafb2b1d62cefcd694871abccc6972a064146`  
		Last Modified: Tue, 07 Apr 2026 01:15:52 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:eb116ce762a307f03ae99d132dfa5fbd48cd9cf0da2e39a1b8f3bf6178bae3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d036893fa25134533f92d60388ea1557c5a3c1cdd4d9ff068c38cf95553808c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1776729600'
# Wed, 22 Apr 2026 02:19:33 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2f77296ebbba469bdab81ae9310261a58bbd9591c96c92d0359b92441a6976d4`  
		Last Modified: Wed, 22 Apr 2026 01:26:53 GMT  
		Size: 48.8 MB (48782445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed0617de9897ec67d18214dad8f0f3dfc54732e5f8895449d0a5e8dcb073767`  
		Last Modified: Wed, 22 Apr 2026 02:19:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:af2351cad75f122e0e24923f47366a343eaee9cf9b43fbb5ac1cf05083167294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c45f35c9b5e2ca8d78d8b72c825704aa80a01fb48f38ed8a6f7338f6fad0498`

```dockerfile
```

-	Layers:
	-	`sha256:e30e43ddf7b81efc8aacd9605929979ed7f8275404e431c8e6df93c756cc1872`  
		Last Modified: Wed, 22 Apr 2026 02:19:49 GMT  
		Size: 5.6 KB (5632 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3346d2dbff44735e94613fd038b71f316779ee96e0b0a13e7a5c995b5d217694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80af212379fe7ee600411a7c3e564868eb08eca74dde5447f8173a33dd6d2a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1775433600'
# Tue, 07 Apr 2026 01:16:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b5a9429b3c324961270f24408bbe430f24d57c979ee7a32f4336735c85553d9a`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 52.3 MB (52336943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654d60bafeedc1fc1c53e85dd10e3820cca613c507f96140371fa2d8a599dca2`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:949433bae96dd3ca07ce81f84bde02fe49a7883e46baba3ed279ded1af72fdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8da4c8d1d00f6314025282d3c7a826fd8ce676f1c29f7fd6ee486eca57c457`

```dockerfile
```

-	Layers:
	-	`sha256:65f60c0905aacb93ebf392b022732fb6e4078ab605fe1ae969e1eef83418579f`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
		Size: 3.7 MB (3738434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d30174c5d52e9927a0bfeb88827858ab7926df122282b1e2e3dedfb10ef2843`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
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
