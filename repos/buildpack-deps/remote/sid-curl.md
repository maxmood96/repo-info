## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:dae8cc63f52953b4d6b2787b16dbd31f27c67ce35e25e1b7f280504d176d4960
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
$ docker pull buildpack-deps@sha256:7009993ef47ec2d8339aa964d540a2d9cba3ff8b5bd8762dec13cb4275f65cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74905477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24505763049b7e05e191f9336a929271c61a78a7912c09c2d1eebb7139b34667`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a8fe1ac3f05529fe3bd8a59a20b641133e27374191e01da78aeed091f2bc7b`  
		Last Modified: Fri, 08 May 2026 19:42:43 GMT  
		Size: 26.2 MB (26171326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fbb5cf828880934b6e06ec3420087aa013d782fbc80d3f612bd489d1e8b81e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488cd8ab064c5a47de905c3081a3e9a1d56518b63885d7fd37cbdc357a8c12c1`

```dockerfile
```

-	Layers:
	-	`sha256:fe0aadc911749f75ebca3976d826753eb9e5e224bd40c30f59c401383644bf17`  
		Last Modified: Fri, 08 May 2026 19:42:42 GMT  
		Size: 4.1 MB (4073318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8b40c89a2ece08f7decf4ecc0d0d36855f0356dc41f41b5bf23f9143238ec1`  
		Last Modified: Fri, 08 May 2026 19:42:41 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5cd8446bf80c33e759544dd648d288efe3d80c941c8b363cb976d29b0a11904d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78152299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f73c5c54e97bb47f66af11d1a5e24846904552f2e14ed0099a45d2c41487608`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:42:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a68ed28706ac755be40447c885e7277b571939be826b0bcf8abd61cb9be646c1`  
		Last Modified: Wed, 22 Apr 2026 00:17:10 GMT  
		Size: 50.0 MB (49978211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7cfb20f6b3b5390ccac8a81632157b49e22d10f507d3bbe6cf94610b6b670b`  
		Last Modified: Wed, 22 Apr 2026 01:42:58 GMT  
		Size: 28.2 MB (28174088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:736ee28254e69546be67721c7273f954e836d552366885e0aae91f6dd2171f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8433551f2cb53929988f8fc85e21d33c0a52488a0438d95f9df7415e8c318ea`

```dockerfile
```

-	Layers:
	-	`sha256:35326c4230db3a91a3555f19aced9253cdb9f261f46b868298acffa686598a2e`  
		Last Modified: Wed, 22 Apr 2026 01:42:58 GMT  
		Size: 4.1 MB (4063604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82057d6bd7a6bcd31e1e62981c25f78ced63bfbec5d328300b6a73d46f769c5`  
		Last Modified: Wed, 22 Apr 2026 01:42:57 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:382d812347d34bbc8478cf1a51cc52e70a24791e9e9dfdd0b47fefcf94aae9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83159577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2484581be81ce7f5b08cca76e92f19a8a1ce05de8448d70df60a0c74e71d32e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 03:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f737822391dff66f42c11b9dc44b70287cb895238a82a880fb68ce9e44f2b3bd`  
		Last Modified: Wed, 22 Apr 2026 00:16:36 GMT  
		Size: 54.0 MB (53970920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d31f9fb5fb8a5668727ae17f4dee5b580a9b4c14b4594301d41edc4810d281`  
		Last Modified: Wed, 22 Apr 2026 03:40:33 GMT  
		Size: 29.2 MB (29188657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2773755831060259df2b4aca71bb9fd356b631b508308297ad1a7839de21b2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4076340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0af986fdebba2ee29d90b2c7b29a9639f846ee14567c922739120b3bc7f9b77`

```dockerfile
```

-	Layers:
	-	`sha256:bb417b58cfdc4bf8ecc0fd099b93217ad773f3880d22e3f5148848f3c04507dc`  
		Last Modified: Wed, 22 Apr 2026 03:40:33 GMT  
		Size: 4.1 MB (4069547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f368d362380fa066ee7ac78e237ddc7c067507d3963c8a3b917e8e872ae81da`  
		Last Modified: Wed, 22 Apr 2026 03:40:32 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:33632a1feeb046ab2fb859821948512513ec7d0f93630c6a44aa0fd35c5f449e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73214116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c836473c657c770955d32bd2e9c6417051e249719f9fa017f232e2e87a7d225`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1776729600'
# Thu, 23 Apr 2026 16:18:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:81bdcc2a2c75f60205e81aaab6ad24265169afebbe01f9647ffa51fb2405f8c4`  
		Last Modified: Wed, 22 Apr 2026 02:18:34 GMT  
		Size: 46.8 MB (46781244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f657cbba56f24dc0e9fdff00edac2ca19d5e98a8de59cf2582136511284eea`  
		Last Modified: Thu, 23 Apr 2026 16:20:36 GMT  
		Size: 26.4 MB (26432872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:73d2528621c44875903f3fb99a5a81432f1b6c65868a76091b8cdbc3f5bbe722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0219b294b2aadb682767470c1b92b2af4fd506d6711d88211f5693c961dee773`

```dockerfile
```

-	Layers:
	-	`sha256:17ca0a652fdb0937dc0651c6c8688b28db52317fd5de004a507339a4cae4ddff`  
		Last Modified: Thu, 23 Apr 2026 16:20:32 GMT  
		Size: 4.1 MB (4057394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84cbe4dfb449ada2658e0011f33788f106cfc7681f6455fedf6fad0bc8bd8019`  
		Last Modified: Thu, 23 Apr 2026 16:20:31 GMT  
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
