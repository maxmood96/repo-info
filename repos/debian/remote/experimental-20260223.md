## `debian:experimental-20260223`

```console
$ docker pull debian@sha256:40b55b22eb593ed03dc4107b1d2797d7443040994038ab1e3898cc4a64446ecd
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

### `debian:experimental-20260223` - linux; amd64

```console
$ docker pull debian@sha256:9a4493cdbaaa0f44977e6bc1bce04eab0ab76128b9ba1fe561d9cf7677ba316e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48667148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c316de83ea3c6338f5de092c7325179fbc8c925f8adf61feaf2de5665a3747`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1771804800'
# Tue, 24 Feb 2026 18:52:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:bea2628104eda864c9f0d3eb45c03e4bc52aa12803b7a7ba1a14fcd34c3bfaca`  
		Last Modified: Tue, 24 Feb 2026 18:43:28 GMT  
		Size: 48.7 MB (48666928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e04eeb581b8789a62b4946e7639636b79213027a6eaf21930ab10ab957a926`  
		Last Modified: Tue, 24 Feb 2026 18:52:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260223` - unknown; unknown

```console
$ docker pull debian@sha256:089a3815a3894de86ac135d898280bbdee12997fb94453b4dcbd54c096f2c795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad46a9fc63fe72f5618d155aa308219192fab256798b3ef63feeff12d77d530`

```dockerfile
```

-	Layers:
	-	`sha256:cd8492254ef48f12fe5ee4b2beaee7268b56a461c318d982d10d865b371e4bed`  
		Last Modified: Tue, 24 Feb 2026 18:52:19 GMT  
		Size: 3.1 MB (3149119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be820535fb551da6a71c8b6120da546637de4ac92c733d10766173273877002d`  
		Last Modified: Tue, 24 Feb 2026 18:52:19 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260223` - linux; arm variant v7

```console
$ docker pull debian@sha256:c0e104582ab395a15b660aae8a297e28c1413f101954037f95e4f7fe7126309c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45650446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ee8f1bac651667cf412c89e1ca2e74304cb11e0b948aeaa5b11d2212159500`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1771804800'
# Tue, 24 Feb 2026 18:57:10 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:2b3ab55d01a3625a78b5f1c040467975e5c4d9f99e62bb5279b090bff1a1cceb`  
		Last Modified: Tue, 24 Feb 2026 18:43:12 GMT  
		Size: 45.7 MB (45650225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139482d0f00ffcd368b52b78d2ebf7e2c5abb119b8993ef2b14a42dda1ab0d9`  
		Last Modified: Tue, 24 Feb 2026 18:57:16 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260223` - unknown; unknown

```console
$ docker pull debian@sha256:bc4eea54a83202c50e7af574c745ad6e29cfe62897aae893d54ec4305993c5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ce37fb8a6d0efb2b43d3b13e3928a7347cb3b46aca5fd85fe1da468b7e265c`

```dockerfile
```

-	Layers:
	-	`sha256:42d196294d576a94c7d70ec71e7db3bb7bea9cf5da2432e3cc7209499eb723cf`  
		Last Modified: Tue, 24 Feb 2026 18:57:16 GMT  
		Size: 3.2 MB (3150495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7582459a828808e458f672045595c816ee433a556490d6f8c4b8c0a2a993f45b`  
		Last Modified: Tue, 24 Feb 2026 18:57:16 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260223` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2ab6fab1007c15f12aabfe0385dcc2fb7ee68538f9e895d00ea43ff0ffe62e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48709486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5926faeafa4be5c5ab4f925682088404461eb32878fdbdd0dda32f39e88455f1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1771804800'
# Tue, 24 Feb 2026 18:57:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:767d28d568dce52d308f9cffe3200536ffdf25826500d30cb1e6eef0815457c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:59 GMT  
		Size: 48.7 MB (48709268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd2059c1e2f6d624696e3de94ef948bedb8684282b38070ddbf11cdfadbc475`  
		Last Modified: Tue, 24 Feb 2026 18:57:46 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260223` - unknown; unknown

```console
$ docker pull debian@sha256:2befce4c83119e452135defe7fc3557e9683c0aabf19e1421e5c2e5d49459b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3162722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467f66965e65c101bb540aa418c214338ecf3c4e6a5dc3f3f9bc83beb3c0286f`

```dockerfile
```

-	Layers:
	-	`sha256:19d08f616720f1fceca7a52ce7e426b423b76c7c3efbb09106517b08ecd27138`  
		Last Modified: Tue, 24 Feb 2026 18:57:46 GMT  
		Size: 3.2 MB (3156542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f9fafc53850dae45a00083b7058917f9f96411a9798a5972a53aab9fa5a84ea`  
		Last Modified: Tue, 24 Feb 2026 18:57:46 GMT  
		Size: 6.2 KB (6180 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260223` - linux; 386

```console
$ docker pull debian@sha256:85472e6c35f66be0322c9012dda491f83c81f0257f166f9fa807a700b52e1471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50022339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d58529bd5671920dbfd257b9fa7c9bbc4ac5a7c21ae174a31fca65ebb9933a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1771804800'
# Tue, 24 Feb 2026 18:54:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6d16fa72a286412257f7649786b4e79e0b3c523063d1bf9be2a991bf9f5d6ce9`  
		Last Modified: Tue, 24 Feb 2026 18:42:46 GMT  
		Size: 50.0 MB (50022116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f08b04d293139e48e8a440a91ae526285bfdf96c624b76b0a5cd63078397c32`  
		Last Modified: Tue, 24 Feb 2026 18:54:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260223` - unknown; unknown

```console
$ docker pull debian@sha256:7568dbf4a8d61fd808a5fc3e6123e9f51a0c1a4c44c3b821ceac191f6db09d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafabb721a4c7d3f35137eb1aaf4ed13f8b0e26a9459a235be69dcea234dcfd1`

```dockerfile
```

-	Layers:
	-	`sha256:59fc59be92e99f47ecbcfd742c823948a8ac318f6bd5424f00cb5f928241e739`  
		Last Modified: Tue, 24 Feb 2026 18:54:34 GMT  
		Size: 3.1 MB (3146312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed9fe11c02d43994ebbf60dbc953daa00b3806a9d912f11b7d7aede23187a0ac`  
		Last Modified: Tue, 24 Feb 2026 18:54:33 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260223` - linux; ppc64le

```console
$ docker pull debian@sha256:974f925d5b61b66f4347b2e5cb4304512fe9e50f76951575c50ee3bef13750b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53670424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ae3582cf2729e9894ad3c6c61d35bebb9dea81f5bf2cd1e4adf65758ed004b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1771804800'
# Tue, 24 Feb 2026 18:56:02 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c84791b36fd700e00080caddc2900e34f9eaa8b32d8b61de0e6592c147c63e53`  
		Last Modified: Tue, 24 Feb 2026 18:45:45 GMT  
		Size: 53.7 MB (53670203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa6b6d33965322a291344b21ea4a952e2c4331d99ec583dacb97a9e69c4f4cf`  
		Last Modified: Tue, 24 Feb 2026 18:56:21 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260223` - unknown; unknown

```console
$ docker pull debian@sha256:711515b64c69b994307b55f5e07d63e28f6713c877421ba925b658f5ae56c05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c4101afca0aaaa7146eb3e8a7de757ed291a0b22b1bfbd41610389b1c39178`

```dockerfile
```

-	Layers:
	-	`sha256:fdab7f4a52e5106d3339f9614ecde13fc6b97eab93c8aede6174ffe1f34ca6f7`  
		Last Modified: Tue, 24 Feb 2026 18:56:22 GMT  
		Size: 3.2 MB (3152640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d508b09aef558cdd18ee4a4ed222989fea814456a43b02a253943c138730b328`  
		Last Modified: Tue, 24 Feb 2026 18:56:21 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260223` - linux; riscv64

```console
$ docker pull debian@sha256:2d8d6d154425fe831360375a46d3e7fff6323887ff0b2038a43effd31652414a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46910371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6d97ec87a561e04817296f572ff242ff3ce020e2314cb5c8408b8bf48da15d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1771804800'
# Tue, 24 Feb 2026 20:51:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5dd66db7bb3ec1b60495864489d01b68e2958aca2174415311a98c854ac1bc38`  
		Last Modified: Tue, 24 Feb 2026 19:01:14 GMT  
		Size: 46.9 MB (46910149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1b62437ae0abe70b5dfa20ce9ff64b3e7b85c4b06136516e5dd374481c057`  
		Last Modified: Tue, 24 Feb 2026 20:52:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260223` - unknown; unknown

```console
$ docker pull debian@sha256:d3b09c6a7896fcb88767b5d25b66196126d207700cddc977ed161dff52761723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6f8ac019392e14267f1b871b8661f88a60e0b4cf91917992270e431f69de5b`

```dockerfile
```

-	Layers:
	-	`sha256:29b24bfd2acf4530962d49d2e45819dede1b2d4c0882300baad51c3711a63a00`  
		Last Modified: Tue, 24 Feb 2026 20:52:41 GMT  
		Size: 3.1 MB (3140635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79dee571590d3d5f559e0bffffc34208d77247e89e0d456ea296cf9d170adc6`  
		Last Modified: Tue, 24 Feb 2026 20:52:40 GMT  
		Size: 6.1 KB (6132 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260223` - linux; s390x

```console
$ docker pull debian@sha256:2757ff3512f9bb66c8cbe1e2611c6a01c180384b5a95ebcc31ea4cfe14ac966e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48447932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2515c8484dec24e36b94f608bae7187f50d8154ea062eb7ccfc9bbec3251d90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1771804800'
# Tue, 24 Feb 2026 18:53:58 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b23ddf0e1d70e9ed908668c16dddb13040bfe9a28857034d958815b16da1462f`  
		Last Modified: Tue, 24 Feb 2026 18:43:58 GMT  
		Size: 48.4 MB (48447711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2484ca5c30dab7219cb3543aefb3127eb185318c64676c70d7fa4b64891d9635`  
		Last Modified: Tue, 24 Feb 2026 18:54:13 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260223` - unknown; unknown

```console
$ docker pull debian@sha256:e9d7a2b8abb5ea0cbea0436c6157207495cf63d6cd3569144138129dbda338c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4074a1189118e1767c9e35997d3cf43ab5a6f348db0a3d03a8f332a8697079f`

```dockerfile
```

-	Layers:
	-	`sha256:3c2c70c785b36220552112a1d469270f2d5cd04f767993e270cab5eb487c52f4`  
		Last Modified: Tue, 24 Feb 2026 18:54:13 GMT  
		Size: 3.2 MB (3150568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba766c2a1b6e3dce467869a8b54706daf6893adc23f84b25211cadb7d65ca987`  
		Last Modified: Tue, 24 Feb 2026 18:54:13 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
