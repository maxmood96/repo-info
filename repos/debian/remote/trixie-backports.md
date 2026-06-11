## `debian:trixie-backports`

```console
$ docker pull debian@sha256:79ded819079d5ab15d9566eef150213d271e26b39b724d6ec8a8c0b0c574144f
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:68713f9d555355139b594d46866b18d5fd00cc23d9b74ab8d6a980f5e42d899e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49317344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3152c30b28f63611807a32b6fa48bacbe071953ddfb1a7b3a06febeb5076c66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:26 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3078aa1de4195b56a5d2a4dba6c639f4d6a0084cde3e3dd35966cf09e5aea7e2`  
		Last Modified: Thu, 11 Jun 2026 00:15:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d27f70220f902e6c05c663bcf5a8fa3d6e0987572cea8752334ddcac83d62415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e2480e2d919e51c4c4d82499fb3757c51a648ebc6191567afb933fd4629261`

```dockerfile
```

-	Layers:
	-	`sha256:c96f6d8a45233c2bf6e021878acc22dd780cbad91777008af9567ec7564301c2`  
		Last Modified: Thu, 11 Jun 2026 00:15:32 GMT  
		Size: 3.2 MB (3170955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a6d2a8ab77bccd68d5f43ebcfdcf2409aa683ac324184d059d3c72fa6e2c02`  
		Last Modified: Thu, 11 Jun 2026 00:15:32 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a3ba6476590c427ff2d5cbade5cd8e128ebbc8d752782dd3c80382e1f83cc75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47495033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e576fb12538ceabc3ad199c86bdcbd645c5bc354dae401078507f4b6b49d9ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:06 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f4fdc449648c31ec97234c27647662108b2d6bce3fe83032a1af88265bf2ff35`  
		Last Modified: Wed, 10 Jun 2026 23:40:32 GMT  
		Size: 47.5 MB (47494811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c7aec27d8d7251d4ab1e72a48ca37d3dd7b38c179ba32a129512e1cbaa7c45`  
		Last Modified: Thu, 11 Jun 2026 00:16:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:55e42476250d5bdff7e92779e48c6ae8e3867f2c37db6f72f54365bb82636e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d0b13a59f94fa70751d3e0992df69d05f797167e42af483d854332b2d4dd3d`

```dockerfile
```

-	Layers:
	-	`sha256:7733c3c1cb0c8f65fc1bf8982ede1e3b135cf794b27568e395682b11464d579d`  
		Last Modified: Thu, 11 Jun 2026 00:16:13 GMT  
		Size: 3.2 MB (3173892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1ea2d430ad569073fc062f0ce469d466194a6ace46f25e37c01556f80fbb5af`  
		Last Modified: Thu, 11 Jun 2026 00:16:12 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f266e2daf2c99a781df2491d5b28794c11a3cfbc631f63118177e64d5d2e9d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45748865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b5943ce6a6482dea9a8dcdfa6ba1ea112f4e48a5653e3d58fc94175ec9e7aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ed6609305b4406dccd7df3eaa23566e8fbca377df7f71b6e93a4204f3dc65`  
		Last Modified: Thu, 11 Jun 2026 00:15:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4be321ce65dddb97a260a71c087a59c3c34d83259be069d5c8bdf85acf0263ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a53cf8c5a2b3a09179f521121854c93b79856af265d33824ab8669e85cde570`

```dockerfile
```

-	Layers:
	-	`sha256:a56c623e21efe5e5f497657d86a49510213bb4430ea0f3f45ee225c81f988e63`  
		Last Modified: Thu, 11 Jun 2026 00:15:39 GMT  
		Size: 3.2 MB (3172329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15eea470f37a15e2dfed271e3db92a216a2414eac6823297a0c89774c73f8c25`  
		Last Modified: Thu, 11 Jun 2026 00:15:38 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ccf19b17558e4b161d9e46b024e78bcc2b240daf935f99529d9196707576063c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49678391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ae5dad9c6e4b823d82292a20367a9fd87314e504c22bc94d81d5d773ed13c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:49 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3765bcd17e740df4e50d048dff74d9da573fd433946ba267483f43b8784488`  
		Last Modified: Thu, 11 Jun 2026 00:15:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6587eb66e0e91cf3cd22522d91c9dc36f9bd124b085e3e4e9ff454f0afb43e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a09120ec3ec6b61b1d9d5358dd8e221da148056d41bc033934b8c7be558022`

```dockerfile
```

-	Layers:
	-	`sha256:f6f0c637929b2627b36098de220bab9510cd99f860097643a918cd79e272fc36`  
		Last Modified: Thu, 11 Jun 2026 00:15:56 GMT  
		Size: 3.2 MB (3171799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39508f3253bc0245bc6d4c8bdd4690866b40c4500c2d71c3f7f0dd2f2401eac`  
		Last Modified: Thu, 11 Jun 2026 00:15:56 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:fd33a42562c2d1995f63c73be074c4989b8549ebf9b02893cc2263f37103ec5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50835786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344b9c18d202d3277859317678cda1efedde2bac1fc4dc86d87194655d554a38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d444596c40d058a23f7843fa8568dd45a73c5d75e2e630fb94eae7b7ae6e8d2d`  
		Last Modified: Thu, 11 Jun 2026 00:16:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:04e10b94f9d522bb3243d844a8b0e0967a3a86b3d720901e37f197d1a629b094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a9a2e031e4654d53199c911dc9e7d7c18bd447b8cd00b716bd57c01a470f9e`

```dockerfile
```

-	Layers:
	-	`sha256:0146ef3d1c318136f5d5066f333785e65b283770465305b8fd8f1e6b3a60a0e5`  
		Last Modified: Thu, 11 Jun 2026 00:16:07 GMT  
		Size: 3.2 MB (3168157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c5e5d884a2fa9d985c6916af71a5561a010db102e918bf248a59eed2dbe7f0`  
		Last Modified: Thu, 11 Jun 2026 00:16:06 GMT  
		Size: 5.8 KB (5766 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:260ce20efcf4435d16b25c54f0447817a79db960d9203ce5238b2b6209f6f1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53138161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86af0336a4951fc8b72054011a297ec5cf8e06c912f4bbebb8438df540762db9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:21:43 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b25931127b1000b26e8fc912f6a2ad5821c6210070d91d2284b26d3b1113ac`  
		Last Modified: Thu, 11 Jun 2026 02:21:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c6d874e5ee4cf3a157c9a8862d7c903f3990cdd1a8afae313d3c24db9ddd1bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece764a6fc8302cf2a269d624b41f87a5a41ad2cb6dfe35d47b841330d7abc2b`

```dockerfile
```

-	Layers:
	-	`sha256:8c9c5c03ca75bdd8f8ee981f0fddb2bd255c58dc8bb51dc58f0629ab67bef518`  
		Last Modified: Thu, 11 Jun 2026 02:21:56 GMT  
		Size: 3.2 MB (3174468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a5c8c55d54cfab33ac2c9896bcb4d6b37f209e60d508ca411fd15c92b13ae60`  
		Last Modified: Thu, 11 Jun 2026 02:21:55 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:73c90e03bc34e05af905e34ae1ec37cbd227ad84ac4d7de342c4773c1095f52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47796491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3e5f8f72f1339c733b23eda0280431cab67234153f666db13e14aae59c997e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:49:45 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e6afb0d9fe2fdfebacf2ccb9782fd129d9e416f637c13f72c2f0427e69c04c88`  
		Last Modified: Tue, 19 May 2026 23:49:54 GMT  
		Size: 47.8 MB (47796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb25929e6acc26dedc94e5d97820671e7bb55597a4f1c8652c1416cd246226b`  
		Last Modified: Wed, 20 May 2026 01:50:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d4b287ed5941b9a5c31b1e6f7be1f944fed234d7be49859c9dfe7f1dbbeda6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac99e35238f85c62d1d059fee4609f9851ddffaa8c8d45a9bf8fc02e96f57c3`

```dockerfile
```

-	Layers:
	-	`sha256:ea2c13043819d520b134c940f15d5ab55d63738e705e6a074808b977cf90290b`  
		Last Modified: Wed, 20 May 2026 01:50:39 GMT  
		Size: 3.2 MB (3163280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699747666d8049f07b6648cd6b76bbb0b0b8f7500881a14164b62406738a98f1`  
		Last Modified: Wed, 20 May 2026 01:50:39 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:022bf1b83ff1e52c0d7fc1e68680ddf72d95df17381dc572741fe79b96aca483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49386119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261a014fbbdc0b2869be751c2d3c55363f12326f2f0501b52d8747b2704a3f14`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:44 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c844125b053307d132340d17b9435583695111150b90553cd2092571685ae2`  
		Last Modified: Thu, 11 Jun 2026 00:15:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1794f75e448ba8c41e3dc27e750d947632b6afb388ad9bba1369365bae66d9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79a5f26aca5a26f9534cde8dea0174f568ca8c71e396e4183bfc4b890974688`

```dockerfile
```

-	Layers:
	-	`sha256:e5af1354d612aa321d07795aaee17f529c7edfeda5f4ce56b638b8130d14849b`  
		Last Modified: Thu, 11 Jun 2026 00:15:56 GMT  
		Size: 3.2 MB (3172402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cb6fab69cc1797c6d34f701e642656b80ff1481aa090496920b994cdee79ca6`  
		Last Modified: Thu, 11 Jun 2026 00:15:55 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json
