## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:c4eb5c07c03608ba96f73db0bdcade0a28e5de1e2bd4f320406b7e9bc377f05f
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7a5905b40bbd9a3561911337ee505f2964b448db2a95914edf2d643b8cd40958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75528603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd85c3a34cf788706950b102d5501b0d86e335840595549b28b528b353ee9ff7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bf1407f5d0a1803a6c62439e0f74bbbc4e011619cdf8ff34937549c5edb22d`  
		Last Modified: Wed, 22 Apr 2026 01:39:36 GMT  
		Size: 26.9 MB (26858023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ab9356a6287e97d658c6aa7bb06b2be3b186f691b1d99ea55732cb5457edf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f60f82ef98643af5a85ec554142bf5366130c320e5842cf026d714cbb559081`

```dockerfile
```

-	Layers:
	-	`sha256:093549d8ac7d2f60738bce83f582a0b9f461ad58559965d07dc01f7b77d2beb7`  
		Last Modified: Wed, 22 Apr 2026 01:39:35 GMT  
		Size: 4.1 MB (4066499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c366ff1257aadaf940b2a48906d005fd7aaf5e2d24f29dcd23f8fe483aa5123f`  
		Last Modified: Wed, 22 Apr 2026 01:39:35 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9e689e5ed75cb4031a7039e14bd2162e8e7972cfffbeddcabeafed1a97f97358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70178801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85607b48b1c7ed3bf6887eb95d674ee4330a0dd5d2c505e19169cf5a63e4ba3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 02:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:954ecf3bb623246e76e048be8db255040be0be61ff8078225017790f93fc2baf`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 45.6 MB (45607386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4a57ff6691b334a65a098db05baf2d825403eba2a4b68b46ed1f8e5631b721`  
		Last Modified: Wed, 22 Apr 2026 02:19:27 GMT  
		Size: 24.6 MB (24571415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f28318e0bb3b75f13cf6b3726e37f1abbcb92f4b6377f84992d9651752761434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a971c7f03620683c46b462b6e9ef8814826f7e3eac08b2e8db8ef8e7ee3a462`

```dockerfile
```

-	Layers:
	-	`sha256:671082e34b533fed80ef07b944bd6f58b17d92fe58d751fd9e68f87943847c11`  
		Last Modified: Wed, 22 Apr 2026 02:19:26 GMT  
		Size: 4.1 MB (4067986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e52a797c2645fa7aa15fe442f7ac981c74b659e94c09100d06f127d9f05baf`  
		Last Modified: Wed, 22 Apr 2026 02:19:26 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:84f5ab0f69b432a796304ec67d5fae05a40bb1a9390f4407d07bf4cfba8af84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74853652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb5b78415f43a09d49e9a6c8ca79100d703e65a76fbb781e5516a9f2ecf8732`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36d1ad0e4ab39e59341cbcc6c49601be7cf05a2f81f334bc0215a0d3ddd3d6e`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 26.1 MB (26142281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e21e6d01e010cb3358e9bed2c9508f0633fec69a6397102a5aebbf6c68c8ea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d23d8f2cd3afaae15ba5c78d6284d197fe0b312d11f9cc06fc1be644ce402a`

```dockerfile
```

-	Layers:
	-	`sha256:bb9bb50441cc349202dd4a6436ab27e56dc8a8495574134665b751d987e75329`  
		Last Modified: Wed, 22 Apr 2026 01:43:33 GMT  
		Size: 4.1 MB (4073138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c663e463c170fd721c91ce28c059ff6e30b5a22622867ec7b09ca11080828cf`  
		Last Modified: Wed, 22 Apr 2026 01:43:33 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:341f76a9b3f546b12108f54b58d466111a28dd2e5f2ffb4120fc09dbba21c368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78280764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de063d160a05c146a836bce7b6cafafdf44e349c5319bdfeab3b34d52f95ca8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:46:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c9bb2730bc0ff710016a40d05d0bbd6ab5db1f6ed39dbb5569902bdddb97cb`  
		Last Modified: Tue, 07 Apr 2026 01:46:36 GMT  
		Size: 28.3 MB (28287053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b6110ea3b3e29ee9303e272012a3288bf7218909462f19d4bb3104166348873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1c58eaea9ff77c9c571f496b3cd1992302faed55c805bfb55a456480b2c951`

```dockerfile
```

-	Layers:
	-	`sha256:74409808c8cd9e845a59c21798b156274b16db5827e350cefe2f8229450130e1`  
		Last Modified: Tue, 07 Apr 2026 01:46:35 GMT  
		Size: 4.1 MB (4063403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529204a2e5f56e4ad8fb4cbe946d756962259927a0583d82bd85a8491065cfa`  
		Last Modified: Tue, 07 Apr 2026 01:46:35 GMT  
		Size: 6.7 KB (6738 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:988b4f8e959683097ba947aff3b5b4d95ed23b1aef62ff82d6a470250e99e33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83414454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e476accfd389b5215b57bcc6366680e29e64875af431f842d6ffce235563fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 04:22:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8091a6b5ece83586bfb56b6975e0b2d9bc01c78d84b526c5c6e82463bb755232`  
		Last Modified: Tue, 07 Apr 2026 00:11:11 GMT  
		Size: 54.0 MB (54001950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3485868c65e901d140674210bf2ba257ab5ac6120dded36f6536c4e9c5178623`  
		Last Modified: Tue, 07 Apr 2026 04:23:16 GMT  
		Size: 29.4 MB (29412504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:23e3f56ebd2f98cdf3ad1335de653a5beee1cf4588a9a1a3f5458a27c157fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4076926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900ffb9597b986a8901cd557f8d6be62a29895f4de2bdba82ded1304e5aedc7f`

```dockerfile
```

-	Layers:
	-	`sha256:9195b61bafd083f360532ae39d0cdc2b029f5642b03cfcba931fb5d685839a07`  
		Last Modified: Tue, 07 Apr 2026 04:23:16 GMT  
		Size: 4.1 MB (4070133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f6fb96a206ee42b4ed7005dfe411a4e3d0f39435b2c6b50e122cc022c8aceec`  
		Last Modified: Tue, 07 Apr 2026 04:23:15 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:56ed67b53edef916f9a3d4087ef856749facc162d365a68e71bf7310318548ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73374017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c496c947a20887ba10cac91c434170adb13cb4510daabfbdfa89c2aa8fe40c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1775433600'
# Thu, 09 Apr 2026 01:50:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd96dd3de127541ef7e3bc5f9bc63bfe49b8f35d0526495ebca95ce89fe40405`  
		Last Modified: Tue, 07 Apr 2026 01:43:52 GMT  
		Size: 46.8 MB (46786906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b785d28162b0b158cf1aa6f3a70ac887d4e1f003e08018a8a82c545e382db`  
		Last Modified: Thu, 09 Apr 2026 01:52:08 GMT  
		Size: 26.6 MB (26587111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f9d54ae89da03bff0ccac933d5f13fded79b93223aed2563ddd6480f512ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009e7f3101a698fce16581ad3f67deb3e821fcd37c713be9b425c0a38ad7b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:98297a3ff6a28ad638bc234f99aa43e8d447e6e7bb8f1f4ac3bf1ad88b19f6cd`  
		Last Modified: Thu, 09 Apr 2026 01:52:04 GMT  
		Size: 4.1 MB (4057976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac058a37c391d344605619e0cd6032ba323c4690e99e91c168fc5c9369afdb78`  
		Last Modified: Thu, 09 Apr 2026 01:52:03 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:57d4efa570e9219d47ab20e0faf5b8fc14e1597cd17b8a7dea47185ec1346f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75068526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe64899afabf1d752a40d83342b995217d90d8fc992567c4aa092841f9ddafa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 02:32:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7b993b1f311a8e0a662fe34124c78c97a70f47ef43d775021c60d64af67fe6f9`  
		Last Modified: Wed, 22 Apr 2026 00:16:09 GMT  
		Size: 48.4 MB (48410950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03da841295960c3b83bccaa55b6f75ac7e7d9ef75a26fbbd602f5481561c77d3`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 26.7 MB (26657576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:76d0fd24774a0db03e431acd9aac3ea9d199eae7c11c7e2f7503351825406a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ea37a25a7a0f0f72220a78332f42d31826a98866ad640eeec486f072a4baf`

```dockerfile
```

-	Layers:
	-	`sha256:b180e778a866b6aa2b87b6c1c78ac7f0ce14a249dd721c737fd09ecc4ba19ddc`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 4.1 MB (4067911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16d2bb7f26b237658bf986d832c9c8ec3f1b5c247246ab8dd0021ad4fee2b68`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 6.8 KB (6760 bytes)  
		MIME: application/vnd.in-toto+json
