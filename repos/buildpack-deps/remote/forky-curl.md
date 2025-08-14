## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:9cb99ed0990f44e731c88e7758d22f1fa4cd898e6c6628c4d68c46a48567cdd2
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
$ docker pull buildpack-deps@sha256:33fea92a6536b108754dfb948179e3fb94b1cf367bd83165bba8cf95276d3cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74883593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c5629d53881ff2a3a35a855a6be00011944ee54c78132beb4ab73759680a17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f2da15d6ab4eca366627e054ac705fca48595c86940e1079388acd7fb2c8df21`  
		Last Modified: Tue, 12 Aug 2025 20:44:42 GMT  
		Size: 49.3 MB (49278278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b32c67f37fb1bae3e7791507a85c187bf40f5edf279234d1f8dd1817c91a868`  
		Last Modified: Tue, 12 Aug 2025 23:13:57 GMT  
		Size: 25.6 MB (25605315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da1c7f11a407ac1cd804656edc31e15c2939e3eac0430f5151b256aa8105648e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823a1096a33e6dcf776c6b42bb6c1e916482f8b4c66a586a86b538c60982017d`

```dockerfile
```

-	Layers:
	-	`sha256:7877e8fe83e26f33aba0bd4d2521bb82e7b93417365c928989cd28e17a63447a`  
		Last Modified: Wed, 13 Aug 2025 01:20:59 GMT  
		Size: 4.1 MB (4116999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdf7ccf57a1f3a2807171803d5e5aa35d72321e9a66422fe47ddd0c8dfea624`  
		Last Modified: Wed, 13 Aug 2025 01:20:59 GMT  
		Size: 6.8 KB (6816 bytes)  
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
$ docker pull buildpack-deps@sha256:34afb9f44dd3eb6efa82aea9ba77b6d8318f2b2c0bfc8622ed09881f1d1117ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69318119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d3af06a981199389daaf8034c11673a02205aaa1f73d5c10c22f4e0878ffd9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ebefa9d9514d88e860c22acef070a7914aeebb2faf205f156980b98aae6239b`  
		Last Modified: Tue, 12 Aug 2025 20:47:38 GMT  
		Size: 45.7 MB (45712626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e92b397025ea1962fe06ac411410e1176db804c6ecdee14d21141a79f11c0`  
		Last Modified: Wed, 13 Aug 2025 17:21:05 GMT  
		Size: 23.6 MB (23605493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:640938a79ca6c66eec97516c4ed5c0c1dc83a8a311e5aa0d040c655ae420e3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fafffc5c7be06cc5c1c1979c85467348e67b110c8bb27d965213285dcb5945`

```dockerfile
```

-	Layers:
	-	`sha256:41f76c69e3443f8ebb8313d9e4b6a4647af7b7a8f4bab1c67a16dd20be2444a1`  
		Last Modified: Wed, 13 Aug 2025 07:20:26 GMT  
		Size: 4.1 MB (4118492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00569613a23633a5d1048ecdec002d1b425cb903990535c9fb23608a0f225e26`  
		Last Modified: Wed, 13 Aug 2025 07:20:27 GMT  
		Size: 6.9 KB (6875 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0f74e4b29e73ddbada41e3dfda15d80cf9e0f7a2379278c1292fd3dd8ee9c072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74648153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1b2e861a00315785d48c0641251d17a168430bd00ca2663be773aed84b134f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:273757ec3c30b589868c996d06fc6679616be5750d77150b4ff9e1c76d62fc59`  
		Last Modified: Tue, 12 Aug 2025 22:09:33 GMT  
		Size: 49.6 MB (49641601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f061b8abd2163f95be76efedd7a660366135f0445c2148195b2efc5c8b4e4520`  
		Last Modified: Thu, 14 Aug 2025 12:01:20 GMT  
		Size: 25.0 MB (25006552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4f5b7e0e9384f97e78331591ccf99484e932af9cd621bcf98b7eace973c9be2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbc2572a62dd446610ef307e4d67b00b90bf5d622abb8fdc3ec50251e31ac87`

```dockerfile
```

-	Layers:
	-	`sha256:570d95e7b0f9366e6b2b42e9b3f5c18e96683e739065e036444cb11c4af7b312`  
		Last Modified: Wed, 13 Aug 2025 07:20:32 GMT  
		Size: 4.1 MB (4118529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9d76cf0e331226bcb48081e06fbdb1e0f8080c371ea6bb2bca5bd94112bd13`  
		Last Modified: Wed, 13 Aug 2025 07:20:32 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4dc5a3b3e7d01629eaa436061444323370c3623f66a13b2cd34766324a8ca4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77559197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9769ab0ec8519d040cfb1d9fb0daf5bd9724935933d2c410c2a9d0fbefb877`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a7661e4f52ad2bea3934eba54982654dfac7e7138172dda967b99622aa0bbc62`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 50.8 MB (50794254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6bb2de85bab19d6809a38d4ff9a79ceb4e077f6d30db2f012711f90b937292`  
		Last Modified: Tue, 12 Aug 2025 23:14:35 GMT  
		Size: 26.8 MB (26764943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:078cc37587b2f7cf3fe61d23b3f794be244194e20ed923e73dd789af15696188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df61ade66edb88d1e711ff5a863bbdc3bbbf9c0e1cd87b430b82d6df206be8e0`

```dockerfile
```

-	Layers:
	-	`sha256:6d020d501c1b6847e2f993e4de0cbce531d2b9682bfed5cea4ab0f80b7a80253`  
		Last Modified: Wed, 13 Aug 2025 01:21:05 GMT  
		Size: 4.1 MB (4114112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8db71ab75077d366ad2ee19ccacf96a02965b8e64907e8fe26174c5ff92be30`  
		Last Modified: Wed, 13 Aug 2025 01:21:06 GMT  
		Size: 6.8 KB (6794 bytes)  
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
