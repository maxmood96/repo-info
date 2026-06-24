## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:0f14c1dc52095f501f5045eb3151f7e06bed0dbf41eb2791e81effc7b3fb2910
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
$ docker pull buildpack-deps@sha256:6ba715df17d2b4a8a4dd594a0a4d88c3b96f612b3ca81af3ce77a85aadca41e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68756179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdfc3b39a854cfdfefb0507b2428109a8bf27b5549e30276e2fca5817d08413`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3683b8a7792857dc507c3398919097537c8d564a235824e722ff16657599fe21`  
		Last Modified: Wed, 10 Jun 2026 23:38:13 GMT  
		Size: 46.0 MB (46038189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c451565562cd00a6664508aa8323b184e76b5b0de69ee46d3c1372a759dd2d`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 22.7 MB (22717990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:277709050f924e972fdb724215b7b468e4723c03c7a7166db4799124d5f75099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffda32c4a2b801b870bcf7414fb0fc94f52bafc2445dca3871d00d1b1893865`

```dockerfile
```

-	Layers:
	-	`sha256:5f88b6eae6bc883621b9ff3d69888fc6055f45f5d4921ba9a400026ebb63a3e4`  
		Last Modified: Thu, 11 Jun 2026 01:21:08 GMT  
		Size: 4.5 MB (4518186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:711ad1b36d68ea709cca3a9c07429242525597865dc117a486baf129202dda94`  
		Last Modified: Thu, 11 Jun 2026 01:21:08 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:657e24bbab7921237254d390aa783ed3fb68e9e72f1d6dcd5d03bfc4f27765be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66157938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6274275a3a98fe9b07ddca9a8525fe4a7c665a1252732a5bdfc8c9cd5f08ce68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e351bf888e49af953ed9ca8b7019938bbf39fe04156e4714a846245e98b63db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6c92d39046c0cc60c2bf966f317bfdbe1c1c836054dc66e937b5c6e9ccc2ca`

```dockerfile
```

-	Layers:
	-	`sha256:e7592d8f081e175d0487c58d8d5c97dc964baed2a3e551c19fae8d4534e9e74c`  
		Last Modified: Thu, 11 Jun 2026 01:23:37 GMT  
		Size: 4.5 MB (4516659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcab072c50bb21f632a636d5892ec79b5d88596906fc9d3050b28dd2139f7306`  
		Last Modified: Thu, 11 Jun 2026 01:23:37 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bd167d35f644b0e41f6d0794471eec2a9a3c3c5f52f553eee4f725f7efdeed23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72002312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa46eaa27b7b97a1ab9ef5ffa4bcd9383627458ed6f66e3094bb28049e00aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a87f16766abbe34ab9bc5a9602c35022c5459e8f8d33d902aeafd4e2aef74397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75df71bddfc65f7f8527b6822449e416fe3a177d398cd74dc96fb6beae4f69f5`

```dockerfile
```

-	Layers:
	-	`sha256:779ccd8a5930523c65115180b5f2d6178dd63ceb58ea98a7bf5e3d2243c2797d`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 4.5 MB (4514631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37460920efc699937f457c95363e3fd95fc5ebf024224b6b8304fd624155093c`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
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
$ docker pull buildpack-deps@sha256:633f35d115aa0d7e4918dd910bd6989be406fe351952e8ee885087fc2b18e80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78033464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bde7a83e03da81091800bd0d89c2e6bc343ab3e9a6d086cbf049342fa89fc76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 04:43:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45654aeab75acaade8b0e13728139de28feb7f503c7e094076fcb9a6e4ed987e`  
		Last Modified: Thu, 11 Jun 2026 04:43:46 GMT  
		Size: 25.7 MB (25686794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39ad51568c2134e384d34f6fa5c89803c264a6fa457c3c0fb947575c8042670b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc22b93a5856c972aef252f1ba9fc630a3c62a9357039cc66d24af2dce6ccb6d`

```dockerfile
```

-	Layers:
	-	`sha256:e1542d5e3523bb1b7bda9a8fdc96f8cd3668d8b0e34dbe3a7b76878ea60781d6`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
		Size: 4.5 MB (4518996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa25f4769ce7022395cbc9eb0197f6913af8dd0935b24d80b6c7706123d68c0`  
		Last Modified: Thu, 11 Jun 2026 04:43:45 GMT  
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
