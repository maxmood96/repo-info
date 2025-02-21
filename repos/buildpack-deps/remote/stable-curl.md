## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:349348cbeae7042be1742a29baec50234c95e7861f52cd0b14d1e52c6209a27b
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:42d7b1aa9523c41d0706d716059774a5339ef9eff81732cd005cced66180810d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72538042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1456917498963d78260f6047d96e9ae5da337da973e2add039994a1c587c54`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e12a83fe4a7cb4e76f6fcc87651f6f22f1a6731dc00a5220a624343bcc75376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a3df9f3102541c5a0f162a43e695ce533b0c1013e1f7cef3bf1b926c193625`

```dockerfile
```

-	Layers:
	-	`sha256:296acce62133a37d0eb516ee2e6522e9f01ff2e94ff39445b822447fe3075389`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 4.4 MB (4359309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a7db7c9a3b4f61541a7a348619b6fe822b816462b9a8d93898ea295f5cc4cf`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; arm variant v7

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5ae5647ace04cdeb0d18fa92a5458b98739d5e1b6a4e84972df6d75f83e25f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74356794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69579a1de6ce4d9dc06535f0f3c4ae3e546e5af273b2bd63f1fcc6a8d2e2d5a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d76a6d719652aac549ba39a4834d8132fc60ef855aabe24f97e463e68ee6de4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ef9c8e03996088176ba3cc1763716840532982c3c319cd6ca66ba14404d3c3`

```dockerfile
```

-	Layers:
	-	`sha256:745272fbc1c3fc0422b6ee341b729acf588740860e6a4f1e48f81e7ddff3effc`  
		Last Modified: Tue, 04 Feb 2025 04:23:47 GMT  
		Size: 4.4 MB (4356366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d54d9627cb1d90d284779bac9fb37ec6014e715706131fbe1387006abffd9bd`  
		Last Modified: Tue, 04 Feb 2025 04:23:47 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1e45989e97eaefa92658fd519fe2bae68cf9b053f0ab1b4f97d2735d21aba44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78030525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0f70646e162cc979805350ac13127a566de8fb22c660b84d7bbd3faa2f3a5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2a7f7c65904bc8dbcef3f3674f9caa66ce22f118b10c07c5675c7bc71d3047c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b9b8c3614fab2c939b24f0810da2c3fa1417067587c3105ac1f38654dd8c69`

```dockerfile
```

-	Layers:
	-	`sha256:65fc8bdcff2c2f6b97523146ca1a93865fa69badfea9f63fe7fe97f682f0b786`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 4.4 MB (4363803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a2d971f0014ca2a549954a195e82af206f6943ced95309a2c4f0a7537e5c7d2`  
		Last Modified: Tue, 04 Feb 2025 07:24:31 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b2a040f9b5018f30ff73eeec1b0fe2f17a7c4929c613c58f2b112dbcc04b56e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71189070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6395dd5d74061c3b3bb036f052a372a32e9397377bb49e680986df2988310a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1cd79d9353a8a124773d7df05bae9236f4c1332118a1326552145122efe1b76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a06dc43215ca62307e19d496fb94d3cdbb3d051126d2acbe246a73e1c75a1ff`

```dockerfile
```

-	Layers:
	-	`sha256:c5153387a5e1a2df7538970109cebfccd70cb85fd9c58daf5aad24f956ff7702`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 4.4 MB (4359005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d92a83e28f3acadfd1ec9397c65d21dea67b1ad648ce759c72010c142c2c10c`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
