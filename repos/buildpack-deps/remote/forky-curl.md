## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:e7621bd83a99a8fbeee588800c166d3423b7ca2832b555ec65c2a2a70dba0a62
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

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2119d7cff978f0174f37ee82711026e978377bae27c95d35c51d063ca5c79741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75588322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1f6479dc6dab6ab9ebf3bf98e94d21df8aa4334dee7dca0e5fe634d6cf3270`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:23:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2642fa4ec2a9746c709cd3ea129863f7b5d0a1937a5b2a2f95a75245bf1fe8`  
		Last Modified: Tue, 19 May 2026 23:23:23 GMT  
		Size: 26.9 MB (26891116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1634e9717661d04708fd64dbdade7ac85fa65b2004640f5c3c9bfa065d423ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0acbcf44d87a1bfaeb5ac80b8a59843e210cb512c2944f814f9cfa4042d4384`

```dockerfile
```

-	Layers:
	-	`sha256:b2674e6484dddd3dbec0629fe6df3ea3658a2eb71d0e6e43c2a9d930d64ff0f9`  
		Last Modified: Tue, 19 May 2026 23:23:23 GMT  
		Size: 4.1 MB (4067350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb21ea399f534e5f0a3bbb6b191c191fec65c1d865474c969915525467c65d38`  
		Last Modified: Tue, 19 May 2026 23:23:23 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3f3d2b13d08710ea9a747d9fccb82e0960f17f25ba56b6db8a1c38a651d63dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70187536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a60deccdd338b483a5891c25726392d3d8ea093640fd53e140b7936b533852`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:44:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1d504d75b0bac1a71363cc538d085e2c22d8b451c5112cd1892dea705c788f73`  
		Last Modified: Fri, 08 May 2026 18:37:09 GMT  
		Size: 45.6 MB (45559652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9e557f096b0076a9b942cb90588ca852b5e2621c1b8f7db68c5da56f1d563`  
		Last Modified: Fri, 08 May 2026 19:44:57 GMT  
		Size: 24.6 MB (24627884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d163080e69257dfb3e472825fc49028c676974d19c73665c66430bb9e384d5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4084124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77121cd152d4ee50c4b234bf7bd3b2deab79da8fce4254cec18696a1271e751b`

```dockerfile
```

-	Layers:
	-	`sha256:b567e4927442f38b660a29449f7fa8c1c01af5b251266300979e50e0d9cb306a`  
		Last Modified: Fri, 08 May 2026 19:44:56 GMT  
		Size: 4.1 MB (4077287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d818569fa3a09a86ceb3923b5bf935b577c51f361a028ea499e9bcc2796a2c1`  
		Last Modified: Fri, 08 May 2026 19:44:56 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:43e15152cc0d1ff5bb477984aa0e60ae3e4189be56b99a023f71d7dd58cce1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74890196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713cac82648b466902a0f80291afba6de891e29b262c99cb98512f55d7e221f1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6efa7756521280bd54091d885e5326bdeb8ff205564db4dd0b7c81ed203199`  
		Last Modified: Tue, 19 May 2026 23:27:03 GMT  
		Size: 26.2 MB (26170165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dddcbb564018e70e021d15d2507e5431aac5b32e946e39989f92667dc53d2423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45645291c01a1661ed7c1cb014a51237c424ce49ec6e03d57c2ef077a110ae24`

```dockerfile
```

-	Layers:
	-	`sha256:8db5dddb036f6531b9d4f3aeb3a1e0e2f0a888ba3ba813129b0fa010c4941535`  
		Last Modified: Tue, 19 May 2026 23:27:03 GMT  
		Size: 4.1 MB (4072709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60559495d8e634b8d70220409e474fab8ba3b93c4e9675bd614b653c03614a00`  
		Last Modified: Tue, 19 May 2026 23:27:03 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d9f46a714174216fcfe035095dea5f2a62f30f8712b7f5af3d8424cd6b09c867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78171556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96d1fa0dacf63a35bb66f34367078ec23d03b22f1085c248434a1440413d8c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:43:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce975e5bc9e5b821fdbe31dcc55ec740aee98d254347a49a09e2157accffc9e`  
		Last Modified: Fri, 08 May 2026 19:44:04 GMT  
		Size: 28.2 MB (28247335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d15cc3707fdbef2ee0a1b3c523fce7047086418299b393eb1c4a5b6a6c0bf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd5d62462cf456f8c244304332a86a3c014fc1a78f5048a8e0a45d065a78a15`

```dockerfile
```

-	Layers:
	-	`sha256:a29565d5e7e4d10013d78ffb45a4af269e78f3257522ee8f358ae24a9a70d4d3`  
		Last Modified: Fri, 08 May 2026 19:44:03 GMT  
		Size: 4.1 MB (4072898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017ff43b39a6d26bf32b1a57f97dc98d5e0484c4ba75791a4e2a2f245a9ee802`  
		Last Modified: Fri, 08 May 2026 19:44:03 GMT  
		Size: 6.8 KB (6750 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:21adac4cc673459817beca6a53bd9804d6a136d31417ecf3698cecb262d0047b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83195951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722992e8040a69587e746a68a7d431104e6f955f385bcc22844f4f99934c69e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 22:31:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b0beeba61b823ca3e14a339f1111ae37331fca42dd43aff18c04950bc3c9921a`  
		Last Modified: Fri, 08 May 2026 19:44:35 GMT  
		Size: 53.9 MB (53926974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f3b32fb543eab144095fd22346cb5e6a9d20cf9a632717c0a11d280547f7a`  
		Last Modified: Fri, 08 May 2026 22:31:29 GMT  
		Size: 29.3 MB (29268977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bdaebdbfed0c7e09986cccecdbbc2dfea879b88a734ce8a1f6ed9ab2f8afcd0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4086469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f01eb7c9e1f52f09a8eff04c1162d4f68e72f62385389ee820c3f0caac53e1`

```dockerfile
```

-	Layers:
	-	`sha256:a9ee8b9ab2062d5d50aa6f9be73866e93eebcab20354ffff92f64bf945d65469`  
		Last Modified: Fri, 08 May 2026 22:31:29 GMT  
		Size: 4.1 MB (4079664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349697923af1c1d059000bbffe33728a6d9db72ea3cfb663255b51750c45e971`  
		Last Modified: Fri, 08 May 2026 22:31:28 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d510b9eb3192dc6068d9a9002f77def7a533c5e1a591bf33ec00bc09fd8cbec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73265369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3632ea85d3e167d35118a0e8fe166f4b663f587a88867803a25b55d10906f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1777939200'
# Mon, 11 May 2026 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f7ac0cf25d901b0f78c05ace03b84988d685b5007a5c2ecdb859ecb56d3b46f4`  
		Last Modified: Fri, 08 May 2026 20:22:22 GMT  
		Size: 46.8 MB (46773178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3f17a612f2a3435e0c1ae9abad061b774e7306b25478218d81e34d30f64a36`  
		Last Modified: Mon, 11 May 2026 00:50:05 GMT  
		Size: 26.5 MB (26492191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd7d213d9b4ae1621184f5e395720630e2685f3e5f86bc3e20cb2c6333d9d0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2343ddcc5af2d73916c580fc8b2a2d63f0518b51441916c663de56b9478447`

```dockerfile
```

-	Layers:
	-	`sha256:6b99e8e7867e2f82e67b1a517d17e69c78dc89b341bc5770bc7cd37be49016d7`  
		Last Modified: Mon, 11 May 2026 00:50:01 GMT  
		Size: 4.1 MB (4067507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:116b56ab32ad173cec8ea464a0c6ce321e0f337eef260add62b42b82c1cf1c85`  
		Last Modified: Mon, 11 May 2026 00:50:00 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:61062f67b299d0dd69097af8e6f73c6b8c1fda54dd5acbb5147726b41118872f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75129193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf439a1fd6f4ca82d31a3559bd5655610d2e3274b877bcf5cccca78d723b8b5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 00:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7394ea10bf5bc140ccf55e31841e993aa40f4cd465376d373dbae4fff2479c30`  
		Last Modified: Tue, 19 May 2026 22:35:35 GMT  
		Size: 48.4 MB (48440526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fee0ef4f478ac4a827949260fdd413d25005b05e8864d837f644813aef5311a`  
		Last Modified: Wed, 20 May 2026 00:18:29 GMT  
		Size: 26.7 MB (26688667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6d9c463451ff35df8bbe3505fdc468877666d419371abdac869ccff166a22bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4075535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58dd3f29e4d4dde664a2deace214363a61c4b5ec9ffe53348ca9ffd1df6f687`

```dockerfile
```

-	Layers:
	-	`sha256:95311d4d4cbee9bdce269862e8c20310d1026f2ab8f3437c9def0f411f910a40`  
		Last Modified: Wed, 20 May 2026 00:18:28 GMT  
		Size: 4.1 MB (4068762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f488c1a5678b8e9a956ae42d002857769a88d97fb6a75e18d8ab4a8105f196`  
		Last Modified: Wed, 20 May 2026 00:18:28 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
