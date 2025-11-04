## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:5c8d499814d8f90802d4e9dd2780d84f91e796d88eae9d6d4678e36c58a4da69
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
$ docker pull buildpack-deps@sha256:fa337b94b37af08728e6625fcb6c5862cc9aa93a1c1203e317f4ada752dc4102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68721848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c554653f8a70c63ed3c521ed8e0dd4b787df9f79dcaab627d9f0790fa03495b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:27:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d0780482d9b97d506bfd55bf3b805f2de1b9731c75e1b5800b5d53bb5388e1d8`  
		Last Modified: Tue, 04 Nov 2025 00:12:37 GMT  
		Size: 46.0 MB (46016089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68533da42b7795728d851e519aa05d6a90a43ea0bd8e6cf63e7cd6acc86ac61f`  
		Last Modified: Tue, 04 Nov 2025 01:28:06 GMT  
		Size: 22.7 MB (22705759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1b0d6bbcd264031791a43e5ce9986647829f904049329fdedc9ac51a2815ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1decfd7dbe7feb4ff142ebdff6b01e7b7b6b61a2b9c66341bc4c1e6acf4d0e04`

```dockerfile
```

-	Layers:
	-	`sha256:790bbee4787791eaa4ee94ec53cbfca6f7526f9fd9226e2cd7cbec013df9b83a`  
		Last Modified: Tue, 04 Nov 2025 07:06:00 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178b0c2a1393baee33e8f04992eb1bfc2ebbc6936f5d2b2e732f7de15a1b2c0f`  
		Last Modified: Tue, 04 Nov 2025 07:06:01 GMT  
		Size: 6.9 KB (6881 bytes)  
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
$ docker pull buildpack-deps@sha256:02a98251995ea35d4466d37c5d3ab23cc061ffc5dba04b76f193489111164ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77999334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3058559b2e16941292c20b2e912a29740a53335ca73cb40f5ab5fc5f060417c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:24:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a69074b98f99ca928580ca93ef45b80d247ceb89abd2c09f9515ba7ef4ea70`  
		Last Modified: Tue, 04 Nov 2025 00:24:46 GMT  
		Size: 25.7 MB (25672054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97bd69fbc0c8b039b6e418dc7e79cfa0e8fc00a91896e180cee3c17bdacd9181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369cc6f49cc1500d954f6d73be8fd07833f5f245f4480e25226825b49a167da9`

```dockerfile
```

-	Layers:
	-	`sha256:fed0b9fe8466d1e929817d89a57bcfb706098c60c300c4629d621ebce6d47b06`  
		Last Modified: Tue, 04 Nov 2025 08:22:38 GMT  
		Size: 4.5 MB (4518315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a088c7f62806c4e667526c14c0857a47b468625e8fe920e0b3a5e5d7fd2b064c`  
		Last Modified: Tue, 04 Nov 2025 08:22:39 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ab1f0a34341a6ec7791a5ecaa4707840a2e39cf96ca8216d9e9b233ff79bee55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71165510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d90c5ab1b49b976dc33597f7827d9e59f4d07114c68b754f035523a520c771`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:16:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a580bca43f6d623617841d967d82ecc7cf55ebeb22ce79064b23dd0b4a10ce0`  
		Last Modified: Tue, 04 Nov 2025 03:16:55 GMT  
		Size: 24.0 MB (24027417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f99b531a772e6fc542171323307be8816346f39371381baca6c8e8f9725e8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ac7662e89639422bf146c4c2ee0fc11e0843e3ccc460f99ffa8f1f3a11ece`

```dockerfile
```

-	Layers:
	-	`sha256:7445465fb4ad6f9b0e92d3f6926826679ba840baaaf59731b8101fe8192008ba`  
		Last Modified: Tue, 04 Nov 2025 03:16:48 GMT  
		Size: 4.5 MB (4510495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9b005fa9bf6ccc5defc48d52f1866a0c96d485ed6c7e18c8b0c34c3469eaba`  
		Last Modified: Tue, 04 Nov 2025 03:16:47 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json
