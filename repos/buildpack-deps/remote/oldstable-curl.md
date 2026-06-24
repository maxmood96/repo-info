## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:7c7a3dadf6368c8de1d8353d1760af409b1aa17bd09b64f1fe3cf9d2bb8024e1
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:15983e351f998050b8fe05145d83124c37e5518b5bb8bface133ff594bf1c1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72546256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afdd44c448a08536033c68f9b6c1cfea0f3a5813572b3885cf0f06adbb586381`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd7bf6f6036613e20f62549df75ed694b99118002358bea5a81baf3929d1ff`  
		Last Modified: Wed, 24 Jun 2026 01:41:33 GMT  
		Size: 24.0 MB (24044046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1869b101ef2b5cd3773734e40b61f6e8e4b011b4edf600601c255c9fc1bb13a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e307f73fba439237653eeb738b403b79d2a17133994d5f79ac62212c451ba2`

```dockerfile
```

-	Layers:
	-	`sha256:c2b985538f18e205b237f57fcf2d64121b0f4f0ceaea5dd208106a73cc251b08`  
		Last Modified: Wed, 24 Jun 2026 01:41:32 GMT  
		Size: 4.5 MB (4514370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6a947478876436c1e1770975fbcff20e6aee39d1ca783b64f070323e2807468`  
		Last Modified: Wed, 24 Jun 2026 01:41:32 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7ad6c071e6b0148371461c6a9180b1b20ad5e66c617a52c9384ac224bab01383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68756397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237a7552991fee5ca4aa52005597275a3f6177948e386506851dc57aaa4133b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:19:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b6f26285ba03744a306577b3de61c2f71cba83b0beff1d4a59aef5f7dab736b`  
		Last Modified: Wed, 24 Jun 2026 00:27:23 GMT  
		Size: 46.0 MB (46038207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2576c00204f880be8e3a137f521b0b0f1c2054ec6a7e9d73dd6d20fdf1707cd9`  
		Last Modified: Wed, 24 Jun 2026 02:19:23 GMT  
		Size: 22.7 MB (22718190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e07d89c26346241b8098f9feaad77a221cbf55f3a278c72d4fefad2e77a3416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21321d843e132c6ac9945ca734df09a5728c445acd3372b27060e8b6c7356b68`

```dockerfile
```

-	Layers:
	-	`sha256:3b7bd36a4176897f0d77e83598c6ec9653a3785c2d967c6f78a7d1f4e107f823`  
		Last Modified: Wed, 24 Jun 2026 02:19:23 GMT  
		Size: 4.5 MB (4518186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c48d68cb9eac7780b204006c001758e892557ca3eb1133ceff5b4da42fe74ea`  
		Last Modified: Wed, 24 Jun 2026 02:19:22 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ec79889462d713659e11697f18e28985956315c5e19c33f5bcbc267dd690b9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66158080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c9e76113e29de2d613a60b3b7bfa10ac62a1848c91bca8814ad327d2dcdff5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3622debffba3838b917703fb6dd9c161a4d93d9fd97c61d3e8400a2245f93c67`  
		Last Modified: Wed, 24 Jun 2026 00:27:30 GMT  
		Size: 44.2 MB (44208145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0df8de55f365d832099cabf27409104999d59b26292d91202ca6e160c4b513`  
		Last Modified: Wed, 24 Jun 2026 02:22:52 GMT  
		Size: 21.9 MB (21949935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9cedfc9a878526043956700487ba2ee364671b56ba0514ed9d86ad191241f0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac82c2b949d4d673aa063fd5b8d745b3548c46d611105eaca9bcf30e9fcabd32`

```dockerfile
```

-	Layers:
	-	`sha256:62aca44eeb5f7ddceb95e176f4f737675a5d06cf917d202c08c2a4bfb4fdc759`  
		Last Modified: Wed, 24 Jun 2026 02:22:52 GMT  
		Size: 4.5 MB (4516659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c0cc30dbbfa87fcd5161846ebd45e019c652936061d5371a035ac90d513384`  
		Last Modified: Wed, 24 Jun 2026 02:22:51 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a18e08cbcdf8aa3d1eec51564ce8b93b9e9e62af5608f1a9361deafb35216037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72002517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c86145b229dfcb8426706d2f5bc2994685584a636133e97c4f1ed9c3ffb19`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebca214f1a4b66acfdb0bd20aa3ee139d1747885ef4b0f3d07aa2a68459230`  
		Last Modified: Wed, 24 Jun 2026 01:44:48 GMT  
		Size: 23.6 MB (23613316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8696b9d2cb983f377c81048638fca83b4d91b80891989e687ca52f997e890bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012eb053a7f0df53919ee43f527dd81545b54d6c406f7f82f95bc09d04fbc2db`

```dockerfile
```

-	Layers:
	-	`sha256:9d7d84c10995cc83d22164eea287b091fc8381b18c313bc2ebce617148dd591c`  
		Last Modified: Wed, 24 Jun 2026 01:44:47 GMT  
		Size: 4.5 MB (4514631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d453337e666d197eb5ef4560adc3d830a3af3f9595913539d24c51d263ff1a3`  
		Last Modified: Wed, 24 Jun 2026 01:44:47 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9235050c05efd18767c1eee7dadf284a03c266b8f5c5ee8b2d64133a5c9eafb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74371118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f440a975ed0e7d025e1703e5496556d90964d93af328a37bcd18af039b01af9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96cbacad9c1883b9ae87f68a0550ac0bd7e0b7ba2b15b142a793b89b5a5f36ad`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 49.5 MB (49491378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45c9ce5ae5ea6ab37787312be8b0a9732642c1221f97d5689baacac874b4cd`  
		Last Modified: Wed, 24 Jun 2026 01:43:48 GMT  
		Size: 24.9 MB (24879740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7db5b45e3e5dee7bad880e7baa09b7198534c2891b6d1c00258055c31631c4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678576a4af93d4d1f26d07245655ea69be09049cd12943a591b063ec4eb90e89`

```dockerfile
```

-	Layers:
	-	`sha256:0ebf011f78600c9203e20347029891471d96dfcdc2c832e15c82a624aa4c898b`  
		Last Modified: Wed, 24 Jun 2026 01:43:47 GMT  
		Size: 4.5 MB (4511489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bce666ab93905f5253dc4356f4c95548cfea72cf3128cae0337003c923b64c8e`  
		Last Modified: Wed, 24 Jun 2026 01:43:47 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cf092d258f9ea491bf1b0ecf624cf68d34244945dc3ef6b1627e07e952dfda4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72416750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52f23c87d075e905a179884fede0c30898304f75c47cc6c75fd00195816327e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 17:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c4a18bb29be3659c76b4d9b55eb7f69e2b6fcb341523ef1670ac059503a592b9`  
		Last Modified: Wed, 10 Jun 2026 23:39:38 GMT  
		Size: 48.8 MB (48792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d391bb145fa329ccce2ad9a5e686a519ff55f48ee4a211ba2c146ad64db56d80`  
		Last Modified: Thu, 11 Jun 2026 17:09:36 GMT  
		Size: 23.6 MB (23624039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de9b9f73e7d3060c344a9c077d331b1cb6312e9e2f9bbb2bafcab94ab0bc3cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af064d93ce5ea601aaa9e770355b050e2f863cf0ac5ef1bcb4f038c786a55e0`

```dockerfile
```

-	Layers:
	-	`sha256:d46fff5208d908b550c7f50305340cbd8ca71dad0400c7b99152f2acd947f33b`  
		Last Modified: Thu, 11 Jun 2026 17:09:33 GMT  
		Size: 6.7 KB (6650 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dfdc35b2ee93a696b0900d0449ac0bd624704ec0926c90d7123be1bf0c27d865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78033895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88cfdcff73a35c66132a7df42c72e37525487c6455df435ab2ea13030c8c305`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217268ac6656bd05839d5770fe7b3c0c976d29750b0c5635d099e473a789a10`  
		Last Modified: Wed, 24 Jun 2026 03:25:44 GMT  
		Size: 25.7 MB (25687048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c2e6a6799e312c9ff5b47e1378c561f3535de79002195a739ea8fcbf31a1b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6f4357b988773da4815533ce5dc2beaff3250bae263ad54d696f6c69568e5d`

```dockerfile
```

-	Layers:
	-	`sha256:654598fccab7d0f4597bfb6677d864ceca93f40ecf3725423e510dcfdd6beb62`  
		Last Modified: Wed, 24 Jun 2026 03:25:43 GMT  
		Size: 4.5 MB (4518996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4872dac6f29d462e99a27d80936dbb1dae4b65b043f95e1364f99439e15aa5d`  
		Last Modified: Wed, 24 Jun 2026 03:25:43 GMT  
		Size: 6.8 KB (6848 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0efdbefd75bdee620f85deaa2afb9edec243174283f257fe11875fb2ab97d82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71200672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5701b16735ad0f9499bc4c5539ef4b3d76c32ba54c5116ba98d8eac6cb8303`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:45:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075239c7f31ef6bc9923503289fbabd4a216a0cc1314ab546cdb22b3aa178273`  
		Last Modified: Wed, 24 Jun 2026 02:46:07 GMT  
		Size: 24.0 MB (24038997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e2f8d1c0f5b4218d0a37259fec5b64f3639dfe060bd6b5057b6d1f68aeb4af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77783a3017d41d7b49cfe2a27a4820c482017900fdb5d5532ded1f2be9a7b3cb`

```dockerfile
```

-	Layers:
	-	`sha256:ea63b2bfdbdbf2af3c5405c4a0e3078b480b5eb16d980ab18567bdd535b88d1e`  
		Last Modified: Wed, 24 Jun 2026 02:46:06 GMT  
		Size: 4.5 MB (4511174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e2d27e1bb5af859f100db654ae22d2a009dd40883788764245155bdd6c49a0`  
		Last Modified: Wed, 24 Jun 2026 02:46:06 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json
