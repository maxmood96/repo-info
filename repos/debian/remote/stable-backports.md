## `debian:stable-backports`

```console
$ docker pull debian@sha256:21f1c31140402ad9fd09206b18846731c9e8fac49b1e37337e738992214ff79f
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
$ docker pull debian@sha256:e27cbf40526686db82c96f2ddf59b72ba37232b0f8a6ccd2571be733cd07ecd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49302325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87ef4bea12f416c7ae56fcd39336a7baf0367a0da87be3e369aa4866d0cf592`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:15:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8061bf05062d424c77b9489757e4e7fdd853c4d882ae0ab30ea6bace2f806dca`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a040fd9e4af166a6f1ed2091636d7391b46d1da40e5962b97f23ec068cfdf040`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:843d32519ec7c58492ce2719e1b635c27a281394b7a5ca1e8676aa4924e6b268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be57d28988bc9b9d6091a000c55e9a507137a7d6165375f26467a09a341b0877`

```dockerfile
```

-	Layers:
	-	`sha256:a17bf44d0b19b5c37e0d6bd75f5072cec0ef9edffb204d597aca1f01a57a9892`  
		Last Modified: Wed, 22 Apr 2026 01:15:33 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c0c3d963ae1b747ddeb3c05b097e6ef40d52ef375b94b69fd09deabe3293`  
		Last Modified: Wed, 22 Apr 2026 01:15:32 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c2eaf25d7102b120f1281709cb81dcce7b411b25a07a356187906744ff3f276f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47466327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c935cf78d8b9989f58f9cf20d8f1762f73be7414820d43b0c20d9357fb491ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:15:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1b92f83862ad3589413c721535c67136c532bfbef449e28f8ed877dc83260dd9`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 47.5 MB (47466104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba0e39e519063db352e71e57736d248abca4d2e23e6ed604b28324262ebfa18`  
		Last Modified: Wed, 22 Apr 2026 01:15:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:daed2e9956aa90510e40d31a611db97b8c4628e95380f01d58bf5851903892f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e78985c9193f3cde9854bb1134afe1914292c8e00214bff8e1c0d24939c1e03`

```dockerfile
```

-	Layers:
	-	`sha256:b7b20976648ff7a5e0298903ae8455d2e2eaa7b39fcf290d15e1b8aabf4dbd2d`  
		Last Modified: Wed, 22 Apr 2026 01:15:51 GMT  
		Size: 3.2 MB (3173850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac2a9bd63832f8df972238f9986572604a51a92b89aeda5f232bba94b2d0b36`  
		Last Modified: Wed, 22 Apr 2026 01:15:50 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1c7d91fb0c6596fe379f400233233832483df67d2327ead817ab90c640f129fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45738420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6100bf48b3257e2b4176638f6877bf4b9fa19aa56a0683ac04d278bd351bc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:15:06 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:597e80ce2b6b93e238072fe4ac1a1e7773ffb2578b0fb5742e6c7bbe14f74f02`  
		Last Modified: Wed, 22 Apr 2026 00:16:58 GMT  
		Size: 45.7 MB (45738198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89251ade1fb45888ecf0ec3fd59e9fbdc018341c19565129140d6faa6bc92bc9`  
		Last Modified: Wed, 22 Apr 2026 01:15:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:18dcd81f0d769031ab31f3c09b100c93d365a6e29f15f748cb9954aa496fa396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b736ffd83cf4fed292fb5f1df0fac66e5c04f3e2715ff6c2f6968c0cb6a118`

```dockerfile
```

-	Layers:
	-	`sha256:4aefdcf566900cd6ddb1a3a49729e4eed2957417d047d66c3a3fefc0082bd77b`  
		Last Modified: Wed, 22 Apr 2026 01:15:13 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57df933c114fb0382c175258c0656d9c9bafaab243a34b0264428a41bf2c2414`  
		Last Modified: Wed, 22 Apr 2026 01:15:13 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b4dee84c8aa8998924692e02ad6c87abd3d37f99cc1592a15cef0a8f7cc6eb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49669467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0489e7c98e19135f0fb4e4ef227ed5f701301ce437f9be54a143e981d052fbc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:af0f848eaad9dee8a2e444559611664d0d8d12cb61a4dac40d312ae66c50e2c9`  
		Last Modified: Wed, 22 Apr 2026 00:16:34 GMT  
		Size: 49.7 MB (49669244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bb2bb9f66c276cac70672f9bf517e569f846c1e2a54e2f50d5a80304ddc01a`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:355ca21ed24b143b259b2736d358e2deab2164a26d3140b3556158ace712dad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af8874fad43e3be587828d18359db3670a7be5240cfcfdeb68b1db943ab47cf`

```dockerfile
```

-	Layers:
	-	`sha256:83a16ba041bc42c69eb2e3fc98f970007be18515a7c0c53383361df75beca695`  
		Last Modified: Wed, 22 Apr 2026 01:15:15 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b74f4337faee3260e1a485b0a1bb40690c0f62f5f383464e9a19453e4310553`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:f4f75666f19f1c1adbf4a0c5afb07b17dc553e32ff04590fced32e4fa9230022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50825580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaa927e2833dd5fa2eb2d6f4064833b72f8decbba305377a74683461f96245d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:15:24 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5366d60daf2f373b6602eaf6c98abd1a3445ced3f64fe1cca2a7471a9d9dd218`  
		Last Modified: Wed, 22 Apr 2026 00:16:50 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3c482bdb12bf3126d226a5c23f4ca876655b2b001b3481c94612101ecfc32b`  
		Last Modified: Wed, 22 Apr 2026 01:15:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5330f3b14a78c2b06b625c73f02e70cf00863eb9b41bbe3ba389c69637f14cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db302c5777437b1fd58c970575e0c1a1b3f58db52f5bb97e426069e6cf1155be`

```dockerfile
```

-	Layers:
	-	`sha256:7e5b96632df66486d2e43f0870905ca3e73a7fc27dda9f29cb85a2c06579098c`  
		Last Modified: Wed, 22 Apr 2026 01:15:30 GMT  
		Size: 3.2 MB (3168115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7b8047eaace0d1d6efdf865032b815652456b6e4a075efd8159f349c4a9a30`  
		Last Modified: Wed, 22 Apr 2026 01:15:30 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3e58411714dc02c3d8cf39d684ba946cedba05172ff1b0dbe9ab9086fdc322a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53123206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cddea6e597838be1d9d546ae4c271aa9dd5dbc747bcc2869556b8833995ca0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:15:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ec04ef0c2952e961987f01ff985303afadd0955b93e9a6ffe9f75b0bdfd98ffa`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 53.1 MB (53122983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76a5599e2c006855768ce21d0072afe0871d8e7b8e29f5bd946bcce63cf0b93`  
		Last Modified: Wed, 22 Apr 2026 01:15:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:44eb0f58b57ca16a04af540935c3b781838b303c1378a0800972af46649bdbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1277d09b3e2c31126a3190e4876618c28e79620cd714c414432ee433380cd3df`

```dockerfile
```

-	Layers:
	-	`sha256:164732d03a2880b9a70675ee986e464f8bae9232d83091a59173937e3fb665fa`  
		Last Modified: Wed, 22 Apr 2026 01:15:21 GMT  
		Size: 3.2 MB (3174426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a7bff01d59059ec2f4f1e1a4874214cec2d91a110da5931d7a685976854c4f4`  
		Last Modified: Wed, 22 Apr 2026 01:15:21 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:5ab685b344f51af6760f89a9d5f3af93a9843b96a94524c9eef4a3eaf12febee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47798436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379f8c06d9be713a7c16995a3b2574d38c5a1fa2447f1fb10fbde5d3fbdd4c62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 05:57:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2ab831617597f10eeb4f7a268b6da17b3b268b5f758c1427c29fe3518be9d92f`  
		Last Modified: Wed, 22 Apr 2026 02:22:09 GMT  
		Size: 47.8 MB (47798214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c091eb731877297756e1c5972dab167cbee33dad18aaccc2e3c056680695c7`  
		Last Modified: Wed, 22 Apr 2026 05:58:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:56d4fedd3d12a883eee8df01ba0eff292cda4318de5d36f339c0f5806e383741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e1ac14e4d48d06fe7ac4730897afc0c74aa3db90aadba50528c1beb067bc4f`

```dockerfile
```

-	Layers:
	-	`sha256:781a6c51caaca463b3e4d5216886b123977afb7343a0646ba27e65e7d3f035b6`  
		Last Modified: Wed, 22 Apr 2026 05:58:23 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f11d2c3de42cf374410bbb573029cf19a8b8e7be6758e3cb832345baec703c`  
		Last Modified: Wed, 22 Apr 2026 05:58:23 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:cb69bb27e1784b223270c5eb34136c847f30689b4987b0b8b43936b24afa734a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b25a73a4ebf46ce6935092de7581eeb13d095777a415fec464efe7977ce7a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1776729600'
# Wed, 22 Apr 2026 01:14:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6e48cdb6e56d2da8434609565fc55b1a806cc98aab46cf8ceefa77c2e90fe7de`  
		Last Modified: Wed, 22 Apr 2026 00:16:36 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6cd79f2d4783c5b70372002098a86c9c5080a92616a06e71709a2f8b136bc7`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dea9b57065a122b3a2603cfa2aab5fc6b4321506a07a07b3c47503afe7b824ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d531104d61605efe9e4315060c7a0dabe45a3fedc88903f8f0c26c32ffb548d4`

```dockerfile
```

-	Layers:
	-	`sha256:75bc71d903265100d1e737bed8cf8144a68429a60102e8e1de0721b03c1c120e`  
		Last Modified: Wed, 22 Apr 2026 01:14:13 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a086c9272db4981ce5b7bafc11785417f0d36b2fb3e8f9e462551132620b553`  
		Last Modified: Wed, 22 Apr 2026 01:14:12 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
