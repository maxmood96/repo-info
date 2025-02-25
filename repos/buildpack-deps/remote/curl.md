## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:7da96811cfa0a17dd60fa3c5b59ed49a8916e6d401ec8b9632b3223a739d2b11
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:24981d5031a6851277117f886be42dd65688619cfafe0636e5e050f897fc47a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72534630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54143f557ba9e9533f0b3c6a2d8a1c80b253e2787fc16d5daa59c4c2c177683e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:03a7c89a1e94266cbdc9fb40c27705efb16b3f18289e19f8ad481ed54f6cfbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a826491c5a429d39aa68b83a76cb99e1bbc744503c7d0d84e9bcde69c6f9f4ed`

```dockerfile
```

-	Layers:
	-	`sha256:5b5077bb1b769db6c3e517152b636aa468887e632fad43374756eef20d5a9638`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 4.4 MB (4359327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7657dd4bb7944c1cef636fdfdaca8bcf825b880cfc05a9914afe26d6bdda9d84`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e764456a3e6c6389335e0ff69bdace1d13c5b030d304243e1722290b471c286a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68739676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935f4abb4053724cc68a4354ed014db1217540a036a7a3be554253d0245f80b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e186710650f352511d1d5a8d92e82b4ab611675b2a2c1375576087c3ddccab51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7549865aecc31cfe80ffb5ae0b5f574d035521979b19941329b24f42049e4458`

```dockerfile
```

-	Layers:
	-	`sha256:a2a0e3ffc25240693dd5981e32252a6d46b6492deb1caf4f83d8df12945ab3ef`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 4.4 MB (4362825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4285e68bcbab8f2e3fa5e86740901937dd15fa0a0ba0e735aae994683fcc1a03`  
		Last Modified: Tue, 04 Feb 2025 08:03:03 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5464a6c00bf3369df4e693237564ff47e99bdd69bedd99f741b52db54e54d73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66144137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bc793d549914afbf589b58b35f4dd5809625733da540c83cf4151be1bae929`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00aa2b046765f483b718594d34141d1f51f7fd20833bf7286ffa4b129556ece0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb903435b396d5ad4513c37e475a0f08b129bf393393a9e2530643c7ac14bd7`

```dockerfile
```

-	Layers:
	-	`sha256:34bb158550658f03bcce8efa68c7969bc65c471a9e506cb28d798eec15a2076d`  
		Last Modified: Tue, 04 Feb 2025 10:41:48 GMT  
		Size: 4.4 MB (4361606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66f515e983898730e103baf32e4c46a679bce32182fa75c84d83de2c26f414f`  
		Last Modified: Tue, 04 Feb 2025 10:41:48 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9a4473adf94868119cd23aba34822796765e1e9ca2940b49af9d2c4a69981be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71904981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea33a0aedad9c06ff0e0a5c609080c1e233bec6767c5bf71303b3517faf7bd12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4f6f6f87f04b8778fa5ec2ac9bd44ab8d4272d110e8ba102b99dc2e2f5eefce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e487cc9f27cd8a6885e25366917d0762a29ac694a53b4e83c7cdc71e66e323b`

```dockerfile
```

-	Layers:
	-	`sha256:93abb4f4a6447eac7f2ae14bcf7f21dccbf201596f3d540fef65c480fd0d530f`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 4.4 MB (4359582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44aa7ce5f133036d4aa1d5fca2e277494c35e7224859760bf9d33b7ae677652`  
		Last Modified: Tue, 04 Feb 2025 09:00:05 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9b479dec0569a1fb876c0130ff088c70b8eb5f3b448fe0cec1c955e34e6bf39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74357805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f871ce3171071e5c73a2ced52a730d9be6c933459b78358dc7da4ee4217a40e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbb8e2f7d78683a7580c45774ee348e288cdf39f89510c68056f4dbd230e62bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb3891eeb41ce1dbafa56faa400e8bae2203320cc5b8198a37c5f921656a9ff`

```dockerfile
```

-	Layers:
	-	`sha256:c2aec331a700b34dced46c20714c8cc5801023483d1384d1d77c162519e2ff75`  
		Last Modified: Tue, 25 Feb 2025 02:24:08 GMT  
		Size: 4.4 MB (4356384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c736370a3802117ae9ebd3d0dfb10f6121022ec853d42e7d3066cfe2a4d91f9`  
		Last Modified: Tue, 25 Feb 2025 02:24:08 GMT  
		Size: 7.1 KB (7136 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:26436bea8603486ad02d64e35a5b8ea9e381434dcd344bcdded0536914020cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72410024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d6ac055b113b9ad9b47d87b17bc1ba5c2bdd6488692f32ea106e81d6542942`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:467081b053e1cbae3c04ca1529cea6d968f9b38249f5cdd15b07f60be084dd00`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 48.8 MB (48757800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7faf65582b7e0fbb4eea14df7537078630b3bff0936e1fc964a494519326b5b`  
		Last Modified: Tue, 04 Feb 2025 19:25:23 GMT  
		Size: 23.7 MB (23652224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d5a09e154e8c9c22e9749a201035a89593898fb3f8faa330dd76c72add5843d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a6b71bd1aee21bc34542f88cd87efe4533dbd76779e1d1f8adc8306d30bdd6`

```dockerfile
```

-	Layers:
	-	`sha256:80277d4e47d48b1069b876cf42cf3a0a8ff25594e0b38ee3de111bedb3b4014f`  
		Last Modified: Tue, 04 Feb 2025 19:25:21 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:077a34637a749b3a43099c51c786c607832092ac323697d123eab7114ca58f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78025725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e2b28a6c13dfde19c69f4c01304280791a8b51790c658c2ea64ac0126a13c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:15c60896edbdad9a10030d589bf85bcf3fb1c0802becc396e2fd0f7f928e0229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce4f8aede9958fdd2a5370299126de5bd6b9635e2ee49ed994b766196e247c7`

```dockerfile
```

-	Layers:
	-	`sha256:5300fe4fb6e4fea4577d8f9e0b1f50a94d878ee9db340d9cfccf7560cfbdf638`  
		Last Modified: Tue, 25 Feb 2025 04:32:33 GMT  
		Size: 4.4 MB (4363821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb736f27de1f13f3da09799b86227266509c85e37d0d9bc6e6148d3318f3034`  
		Last Modified: Tue, 25 Feb 2025 04:32:33 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:53ea1f604f83a98e6b818095fc926631c7fc1463aceb13f81d1ed725eed59725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71187731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dbcd045e2ced314d65e9122112e5912e50ca3ddbca7accf720dade201c7b4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f17e6d44962cf75a1f49524e69d8f90a37aacd08a9b881e6d35bc9991524cd00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28c98e27105a35f40832f09c1317b88642562f618bfa3c64709c66f28885d10`

```dockerfile
```

-	Layers:
	-	`sha256:f3139b8c795033539ae18c779681f4298ea316807f277e0a22283ec327841060`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 4.4 MB (4359023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87bff308ba27084c9be8a478673ad8b387758198fb246b1bded1c69816c74c44`  
		Last Modified: Tue, 25 Feb 2025 04:04:14 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
