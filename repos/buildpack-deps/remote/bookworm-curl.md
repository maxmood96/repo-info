## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:ef27c6c9a5d47f302f5f66a0fded9c6f4490ab15b8c1e0d03d96b46426d94dcb
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2774beedc151d53302e9f67ca851eefe328fdf3c7e8cdb1f790e731e0b2f62b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72509461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e41a9a25faf07c1735c1ae59baf39d552e253234209d6b9bb31059df6ff0be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f2320d46c154b6a7efd4a91a82d20953ad03b6ca4ebd3ce0f67c5bd6daf0c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be7f0fbcd39379e28c368b390c577172770c1474ad9d66f69fd5eb0344516ca`

```dockerfile
```

-	Layers:
	-	`sha256:a5c1260ee2dfcce076bbd2cc180e06a192718c6e140c43278e765121c41f35c5`  
		Last Modified: Tue, 21 Oct 2025 09:11:03 GMT  
		Size: 4.5 MB (4513691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ce01f9dca9f2409e98ef7cfc98109fb1a57f5375d030afb07f5a440f17944`  
		Last Modified: Tue, 21 Oct 2025 09:11:04 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:792fa54013af03edd3250bd3787252df7a5792d31f1bd70756049cee1dedda7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68720852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc0d60e010e8906921c5abde44f754f08f6e85843a747115cab83d6220bc9d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6b0ca95b13ee68ac33e867e046c01d5a40daee1d76922dab47dd1edf2533e94`  
		Last Modified: Tue, 21 Oct 2025 00:19:45 GMT  
		Size: 46.0 MB (46015580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f052363c254a265c1c1981af32f1173b8e1aaed39bd939fefe1c6df9415293e8`  
		Last Modified: Tue, 21 Oct 2025 02:31:20 GMT  
		Size: 22.7 MB (22705272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b0c9eeb081f1fd65b88e5b03b5ac518a4b09d83636f9c79d2515697c79fe16c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b134f3b4f4466bbcdad07d9d02943837c44e2ad8470f6cc02de518094a7676b9`

```dockerfile
```

-	Layers:
	-	`sha256:df2e01261dbd277a9e088676f18f534e7eeac9c3e84ac7ba363e6ee7af9b6057`  
		Last Modified: Tue, 21 Oct 2025 06:21:21 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eda1152c0400f5a539f5cc58cc5f9fb6347e7917bb6d8c311532a3e9baca90fb`  
		Last Modified: Tue, 21 Oct 2025 06:21:21 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0ee6c37ad86b1ebe3118e4e93f814da9ea7b9c2bb25c1bd90feb6036da703167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66130415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccccb0e64d87419ee311dcd8c1243f1b9e16d77c2dfa98cd474f2d933ef8f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7dbfb28a8f384a49e792c3f6d5886b853c4b3a16b26585c10c85fe20f66660af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72cc04e3ee2e3efcb51f7fdded945f2c48dbe09b214bc1b0809654bc12f322e`

```dockerfile
```

-	Layers:
	-	`sha256:dabc53146799a2fbeae743d4d9972c378416f5bed5b7fa422d43ecb99fc944c4`  
		Last Modified: Tue, 21 Oct 2025 07:19:47 GMT  
		Size: 4.5 MB (4515980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43bbc4bfabe5545c9c7f8f91515896e75d25e2b60813e67c42f723b2511760ad`  
		Last Modified: Tue, 21 Oct 2025 07:19:48 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8a558d6d9e45dbd0e4cc744c67d855b3275f2f552ef6794fa90c96c416c2981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71956987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03464a18c64a5334ab7daf34a2189d9ff2efa2216ac8d431a2a938b3a2f8294c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0680bb12a4bcee489d711aef5fe702343abb3b28acf7b1b26ce726f6a55d7901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd11890c523123d4da4061758617e0a0cabc5288da4ceb2569e0484fcf80eb06`

```dockerfile
```

-	Layers:
	-	`sha256:46264bceb4f7b416dc23de07c374dd74dba6bb1a906dcbe2acb4843523768842`  
		Last Modified: Tue, 21 Oct 2025 08:08:55 GMT  
		Size: 4.5 MB (4513952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0edc4d6b3cd4b507262e71758ff835c5b9ba6c5a132fe34a11c5c6381a3968`  
		Last Modified: Tue, 21 Oct 2025 08:08:54 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:98d4b27ed63704b76ce647617bb6de3e75969f823d1f85381a0810645c3c9bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74330928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2524ac1fb7285857b203d8db86f7ce7ba049cffa76d796c6eb63eb48fa8b41be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:259418761587247ff19c3240808ae3d049450952417449ad239932fdacf2e47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d187258055f9847fc3cdbcce4e74ded04ded7ba7d076c63650cb89a62b4a0bd`

```dockerfile
```

-	Layers:
	-	`sha256:5590a998626f42bd0d7898c3315a6d43a9bb8b515c3556b82d758cc973cf6810`  
		Last Modified: Tue, 21 Oct 2025 10:05:08 GMT  
		Size: 4.5 MB (4510811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9c76e8d35ff79a004d07cc45aa4892aff6426c63d644224b59cc260bbaa343`  
		Last Modified: Tue, 21 Oct 2025 10:05:09 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8dd0e6869330da6eaeb86067ba3025451d2ff0c9b3be4be6d6a2b59c8e40da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72374544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3745ec6acb0fa96bea05e3037b35c61848e44b17c48eca0e6b01198bf5fd6f20`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada83e05f36ace3b39ede326eee5e8c640f47f0d217601cc47ce49334a0f7e2`  
		Last Modified: Tue, 21 Oct 2025 17:26:33 GMT  
		Size: 23.6 MB (23613801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f64dc80f912c051150225de454966d3d686c099a78f33bf464f01dfd2876509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7388131f1dc489233553ec0778cc18bca2b1e05db337c55c2dbe878824bdab`

```dockerfile
```

-	Layers:
	-	`sha256:9fcd1b45f6a765d165dad245229f5d6dc9b8564c54c02584367d2b59b1c8ab28`  
		Last Modified: Tue, 21 Oct 2025 19:19:49 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3830e35ebca2144b61562d137ee517c858f7e827d2e100132e0daab3ac0bc928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77998906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c961c0e0799f9e6b71547d3f1ae94b5aeeaaf7604e900b39d28274bf8f67ba3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665a6d4e6976a738d68a77f188daf2501160c6ad54e4788282d2395e926b5e6`  
		Last Modified: Tue, 21 Oct 2025 07:42:57 GMT  
		Size: 25.7 MB (25672119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:499f841f23fbae43990b74cd06242d032e0306017ca05ec7abd6c72e75c53e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108a42a4e4923beaf90aca7607710136ec490b17b687250b1289f3ac14e64837`

```dockerfile
```

-	Layers:
	-	`sha256:4eb95d935b2fe6435f4a6356ce598d2f45e139ce842395476dadf04c380d7f95`  
		Last Modified: Tue, 21 Oct 2025 10:20:05 GMT  
		Size: 4.5 MB (4518315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf15a9101815dd80688af07ed87de415635577a88e038430c84a5b706e37ab98`  
		Last Modified: Tue, 21 Oct 2025 10:20:06 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:74a09739c4cf6faa35444fffc3ea17963a7eaff09b11cda2285e52e752e158fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71161162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cec9f767a8122d0f042f74a1a8275bbbd525f2ecf9314a682368a1f0196bf5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2365377a8d4ecfdf70b8afc073fddfe487283a41bc28927b47a4757047f66c`  
		Last Modified: Tue, 30 Sep 2025 03:09:03 GMT  
		Size: 24.0 MB (24023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dace99948766353728ecde9993364acbfc4417f87feb565035c30d8909871e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a227a746758e36830eb5cf4545241f4df0492172b2be6d02cd19e6bfab5fe86`

```dockerfile
```

-	Layers:
	-	`sha256:7e3d4c7549befb40b9b0bb755cd56b09993334410370e2a39e5d3414fdc84759`  
		Last Modified: Wed, 01 Oct 2025 02:01:19 GMT  
		Size: 4.5 MB (4510495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20ccdd8cb7156eb5e55181aa2947c66a26af217e19b6ab51863909c8ad08bf4`  
		Last Modified: Wed, 01 Oct 2025 02:01:19 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json
