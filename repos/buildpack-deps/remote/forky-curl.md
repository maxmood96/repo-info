## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:8eeb61fb392b880125722770d33a9645b278aed00b09d254f16a8c54c7a6a71c
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

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f7a15b17676868119a25564d116b37e80b39e2c7ee3d0f97238c0ef9740fe3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75234749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5aa327bb11cfae3964aa47ed2e8642f10d8dfd25984c1b5b51704e9c1278bc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa3cdde7daa1c8617934a7f6fc5999acbd8f13f45edd54e774f4a3af8f31fa8`  
		Last Modified: Mon, 08 Sep 2025 21:54:27 GMT  
		Size: 25.7 MB (25659714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e2bb4c23b0c1c800f86d8de08d795cf799c3adf754111b841338da59ead0cdcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4677455a9bb68181e48ed3586f1c9b2ec4197aa3dd0d5a7f16f44e4e99b7f9`

```dockerfile
```

-	Layers:
	-	`sha256:fad733c11fc031a4d564bf25a243c6463d8314a849cd6f9ef822c0a990363f81`  
		Last Modified: Mon, 08 Sep 2025 22:20:29 GMT  
		Size: 4.1 MB (4115731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74ee2699c2f42ef0baa11da5642a399e684fe3c44b63da73f821e5760cc9e00e`  
		Last Modified: Mon, 08 Sep 2025 22:20:30 GMT  
		Size: 6.8 KB (6815 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1a6815a172c8a584569ef695eef1554108cce649d38282c4fea5f6a79cdcd7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71773474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c5b9be8e27a18f95e1635abc37da2d926745fa253d0c77bafde838d0be412f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2fa5a98b9608d692994d9abcc2a7007473cf39d4da546665901804b35bd8b320`  
		Last Modified: Tue, 12 Aug 2025 20:45:48 GMT  
		Size: 47.4 MB (47442421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e8c08416a0595c07b904b87179f903faee6f0a25e5b00b485a3c0b0df46b2f`  
		Last Modified: Wed, 13 Aug 2025 06:07:53 GMT  
		Size: 24.3 MB (24331053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8fe06d7c89b41cdc4d96eb2530d82f3ae73d412cc1d131c177c0881923c0eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264be9b520599485c161fdcf09d8348737b089d992503631bd8f7965af19366e`

```dockerfile
```

-	Layers:
	-	`sha256:83de946f87466516d5701b4d0332795668bab3ec4e4115089a18eebf3569047c`  
		Last Modified: Wed, 13 Aug 2025 07:20:21 GMT  
		Size: 4.1 MB (4119981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3ff33f38e9b4f3bc6b2c8e98f302f7bb0ed431c9b94ebd4ba270df6b622d30`  
		Last Modified: Wed, 13 Aug 2025 07:20:22 GMT  
		Size: 6.9 KB (6876 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e0593d850eb9b18f6a49106c47b1826264b30104e5a7f6944dde2d06b254feb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69608006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d446a034d66d0d80f3b6d105737f17f57e2792ff8f5aec795d94af19e73ef07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37213742d2f58ba09fd9f68c8a57d0aed21f04fbd865207a40734ff3e6e7a8c6`  
		Last Modified: Mon, 08 Sep 2025 21:14:40 GMT  
		Size: 45.9 MB (45943220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce86adee590a893d066c841440cd9d1bbc41753c40fc6a723dd85c4ca79b9b96`  
		Last Modified: Mon, 08 Sep 2025 21:56:31 GMT  
		Size: 23.7 MB (23664786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:523ae429277c6dee71206d174405fa89c110cfdba440b914dde9142bc1230718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2132b5a5c177e7b11957f4a72b5584dddceb4e192016db12e7696989c8cfb5e`

```dockerfile
```

-	Layers:
	-	`sha256:0df8cc22529b2bd0848f1c5afd244d46ef7f28adad2affeb80bb9b9ccfd4427a`  
		Last Modified: Mon, 08 Sep 2025 22:20:42 GMT  
		Size: 4.1 MB (4117224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d13d5e73ba4a9d0980081ceae64b162a9dc93a33b11a7a95ebf936d0550f842c`  
		Last Modified: Mon, 08 Sep 2025 22:20:44 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e30b6bdc110fdb5c3d99b1e51c76f18256ed32272b28b481ccde30ece8d0d0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74942587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d00fc64282d174889922eeb6d9e3f3aa8d01175e726d5abeaf7fdb3409d6c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ec7eb396047bfcd475c3064af0e813d0c880bc68b69e6192c860aa1172659`  
		Last Modified: Mon, 08 Sep 2025 21:39:56 GMT  
		Size: 25.1 MB (25079091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:feb27783e1885cf8264c49eb5f4d0f52d25fdc701054c9838e1729a26268a128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d549cf54bd6a27ff5064fbd46ea54e475eb3a292e256500a8cb1f595c76810d`

```dockerfile
```

-	Layers:
	-	`sha256:c3f8a8034eebaeb9c6a5d31fdde3138defec5bb7a504e5a623b0dc503d022754`  
		Last Modified: Mon, 08 Sep 2025 22:20:50 GMT  
		Size: 4.1 MB (4117261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd5865ec001f94cbd892b734b524cb4c6acff5f6e748f8b27a6d487caf1dec0`  
		Last Modified: Mon, 08 Sep 2025 22:20:51 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:544b356ed39e6ce49b7c2bd32cafa6c5d2f9b826fcdcf2aee3c3c152baf836a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77874282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3b3cb2bb2c150a2011973dd07b2d5a112c924f25070bbf77ce5dc25e36deef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160456f8adc4b90f7d6b65b9febd09b29220d231ef5935250170717564dfc2ef`  
		Last Modified: Mon, 08 Sep 2025 21:54:42 GMT  
		Size: 26.8 MB (26824472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:baed161691834f2dfa104ccbcc2bde39a285955480aaecee4676d216958c7f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217e5a56c6dff4345398f8f405d3be8c17072b2b6d460e143a8516f19717c7dc`

```dockerfile
```

-	Layers:
	-	`sha256:6ff40508d6a09e675f61d6a53df80352beeb75a56f939f6da9b9798b00ec2c2d`  
		Last Modified: Mon, 08 Sep 2025 22:20:55 GMT  
		Size: 4.1 MB (4112850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68f466e418a20a6860c0da6d74a0dc99a61b2ef323eb7e740fd91f1e002e453`  
		Last Modified: Mon, 08 Sep 2025 22:20:56 GMT  
		Size: 6.8 KB (6792 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:21ec086ab6d14f1eeb6a0d6bd1d753b526bd23f31df30b9fdaecad9e2cb12521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80090296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a886e86032f075882a32b417dc45e087ba129a9f6fe82806f227ff3dff6219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8b7a7f44f45faa95497b08557d13fcde72165c528469e03cbf308c4f4631f2dd`  
		Last Modified: Tue, 12 Aug 2025 23:06:59 GMT  
		Size: 53.1 MB (53103377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840e735c8e0187da0a3a1c46a694c6d194b251001f4a96704e0ac845ec18ebe3`  
		Last Modified: Wed, 13 Aug 2025 12:13:41 GMT  
		Size: 27.0 MB (26986919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:640e24ce11552c3b07656bab3eae9f80c9d5cf3dfcb5784938e0f53871cb4533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f958eecf46bb1d28497c2dcddbce7cdbffff86ca2db5451afe221f5b3743e6a`

```dockerfile
```

-	Layers:
	-	`sha256:150896906a9a13f1ab0fa02ac22a37cd917f949819911a4769a59cc41f300ce7`  
		Last Modified: Wed, 13 Aug 2025 13:20:33 GMT  
		Size: 4.1 MB (4120839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfad59d7ff10c4f17498a41144bd65d1156a835c2fba54e3f64e765aa1949207`  
		Last Modified: Wed, 13 Aug 2025 13:20:33 GMT  
		Size: 6.8 KB (6848 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bb33d877ed8b11961555e345b744c4adaedddd904d32837714f3447be760979b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b936495f303024f65e1d9ff715c7ada50d52dc0c30e3ab55631e89f591761ccc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:18eac9f463d6a4f3c60a520935227506dbdb88fbd69eb2d7f1db2b18bab3b76f`  
		Last Modified: Wed, 13 Aug 2025 00:59:52 GMT  
		Size: 47.8 MB (47764299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40195d2e04aeb657d27babb7b990135b099dce2244de1f5f044377d8fb07f57a`  
		Last Modified: Thu, 14 Aug 2025 14:40:45 GMT  
		Size: 24.9 MB (24943412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3507986d071f5c94d93611b27d4e07e642ea4c57139f32bfdf584ba180edc75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4594ced68a56bac237ef21f1443de6d265e5035563044381199e74c44344aff0`

```dockerfile
```

-	Layers:
	-	`sha256:72ceae34aeef767f036594bb205e80204c874dc271b16182a149d05aebb714d0`  
		Last Modified: Thu, 14 Aug 2025 16:20:10 GMT  
		Size: 4.1 MB (4109503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931a2b80aaba0dc2b5b1358848721154c76036b988e04810b7280a5c2f0030f3`  
		Last Modified: Thu, 14 Aug 2025 16:20:11 GMT  
		Size: 6.8 KB (6848 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a987360c1a9b428c80252fc40785ad704b975053dcaa0b1ed8d6861eca5594dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76116825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea6d9373b2e1a83efc358f7bd7b7d3595ffe84a48d33a101007f0ee48ca63f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:737129d56eecb9e531486098db9ca11053ee0c83738b761209455c817b0cc095`  
		Last Modified: Tue, 12 Aug 2025 20:53:59 GMT  
		Size: 49.3 MB (49345157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788bc8e33ee7a99a1a339be1f8a021249410c7933d3ffbff46b2196b2aeb3d7a`  
		Last Modified: Wed, 13 Aug 2025 11:11:36 GMT  
		Size: 26.8 MB (26771668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b8f5de906d8d738a0ad00b12edf07da8989efb50a00f5ca65cca156c2c570252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facdc28852d639831fa4d3d71ff84aa3d7037f0c7626ac91bf59bbb8ded30be2`

```dockerfile
```

-	Layers:
	-	`sha256:8876ad1de9e3456cd00330b23bf93c8ba74116db4597bbf819b04963ecdf9edb`  
		Last Modified: Wed, 13 Aug 2025 10:20:01 GMT  
		Size: 4.1 MB (4118409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c5e7d7ab3f3d5d0da90d5f0188b47e355059737478371d521b42c7edf46a8f3`  
		Last Modified: Wed, 13 Aug 2025 10:20:02 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json
