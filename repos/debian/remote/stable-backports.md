## `debian:stable-backports`

```console
$ docker pull debian@sha256:ae546eb50c22addc654ed6a96eade9f5c4e69215d7bcb3643409cbff98f5d557
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:99b507759401f63fd66ed9765c9799f414308aea07aa361f77ba6fc36bcc2313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49317477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6066884817f971f73d7cc337cf571ee7af6e416815be8000db0be4ff9a93ab95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1782172800'
# Wed, 24 Jun 2026 01:15:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0175edf8aedd0f204848248c24be4f601a41e3ff33fe804beb0ad78a40d3a242`  
		Last Modified: Wed, 24 Jun 2026 00:28:22 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274fead83b3fd32b2c075e903ca372ee36fa80484efb5a794a1714264d100967`  
		Last Modified: Wed, 24 Jun 2026 01:15:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:46601307b7d7dce9a7d007418b61e10dac81dd0d72e12a3984b913d4628a69df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22120b433aba917db14ad5c4a03b2c36c3c9c31bb8789dd74124ac3ae147be22`

```dockerfile
```

-	Layers:
	-	`sha256:153c82f93da458b749e32a37f8848acf5815312ac1ae411ff5ad0d23fb5b9953`  
		Last Modified: Wed, 24 Jun 2026 01:15:27 GMT  
		Size: 3.2 MB (3170955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ed6062dda1c0dba36a4ab9dc531513bda0dce2b787a98d07c627147c0e2aaa`  
		Last Modified: Wed, 24 Jun 2026 01:15:26 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:807fafd20b01a1d7e342e27d2c8db733ddcca73067ddbe1588156e08a7ebe62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47495190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8176686dfd7728c135064ebc4b8ee8cbb1d1e07d6b04f3d466a9bd502456ba8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1782172800'
# Wed, 24 Jun 2026 01:15:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6a0abc3b1f622c876bccec80db9003ab655980e925dc450af1aeb29ead46273d`  
		Last Modified: Wed, 24 Jun 2026 00:28:49 GMT  
		Size: 47.5 MB (47494968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6bca35506b2c5dd4332fe10aeb141c442baf3a3effbd9a40c18f314edc158b`  
		Last Modified: Wed, 24 Jun 2026 01:15:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ee2fbda0e319ccb0d6fdec1f9c24b62dedf91a07150627327cb6631e92b3905a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa363d49132489d4d672aa4ccb04e536abeb7966d632bfeb2ced4c6a4bb8078f`

```dockerfile
```

-	Layers:
	-	`sha256:16e69c0600ae8303e4e3cc230fd05134f75498fbb440eaeff62c290595a0c6b3`  
		Last Modified: Wed, 24 Jun 2026 01:15:09 GMT  
		Size: 3.2 MB (3173892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87a30a4935d65dce5a48e3bb267219d778aaaa557db897f0402bc7855010d7c`  
		Last Modified: Wed, 24 Jun 2026 01:15:08 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e867d5efd8345b49c7f6e480380ffff23f9c53375e5b4e1d8987165ea88c5fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45748941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6481fed0484ad79e54cbd5959c9eca9cb122e4c28538a23dd6b29243071cfa50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1782172800'
# Wed, 24 Jun 2026 01:14:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a20eda36629b93120d38d96687fdfb964e182420fd3f77e1dd24e1ec4445d0fa`  
		Last Modified: Wed, 24 Jun 2026 00:28:26 GMT  
		Size: 45.7 MB (45748719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4add62baffe607aa407fdfbf7f912b6fad51ab66065c4ac4328284c24dbdde`  
		Last Modified: Wed, 24 Jun 2026 01:14:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e653981d5f53389f098ceee64e7e13e90d9d8d70e14fb3779f45493e0ce3b119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa6e97d21acc8dcaeba8ae73b82be0625af79dee8a98afe5ca2cb9984ca24bc`

```dockerfile
```

-	Layers:
	-	`sha256:ae4d15c9aeb55b68f4f5449f1edb0949946b81b95b8a0813c14f0b7267e542f9`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 3.2 MB (3172329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1d5117ee5186d8171c0f212affead2eb1bdbe0b96e3be0dc02b47463937359`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e92a08a049f7dae660be0fed5f14068b75dd1e5078ae3f219313c0d2812af866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49678615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76b0bb88536d24919d7abd7c931279d83c999191595488e8108f755e92b9c50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1782172800'
# Wed, 24 Jun 2026 01:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:98f023cbf349ace3ea3a02dcd5f98a707a369c17e008607e5d4f7d8fc588d8c2`  
		Last Modified: Wed, 24 Jun 2026 00:28:37 GMT  
		Size: 49.7 MB (49678393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f8f38af4e76623f1a4d7b53a16117f19cdb9728d4c494ccab3f4b49b607cf0`  
		Last Modified: Wed, 24 Jun 2026 01:15:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1461c395fd121c942e48c72e8d77f16127260d6a4488a5eeff3556975bc54dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872c12f614d9f8ebaa6f308f782ef87a46797c18d8064a01c9c7032a0576c83b`

```dockerfile
```

-	Layers:
	-	`sha256:ae55981b918c70936f35118dbf135b80d97eb59eab67562c8c9a5cf8a1a83b82`  
		Last Modified: Wed, 24 Jun 2026 01:15:14 GMT  
		Size: 3.2 MB (3171799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5688bbe7cc8088ae57cd3b8a836b7ee555b6f1f01fe3399faf44eba6fe1c10b8`  
		Last Modified: Wed, 24 Jun 2026 01:15:14 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:d3d53bf269c1241105b7e48a7e05b6da2dfce5f0cfb25b0deb123b6aee7476a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50835878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e264fbb40f6a822f692ce0d1aa9e50e919394799245fe0235de473b2f4328fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1782172800'
# Wed, 24 Jun 2026 01:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3173584128605dba40001b373c97b4d1f865681b3b3096c43780ad0489fbe9af`  
		Last Modified: Wed, 24 Jun 2026 00:28:24 GMT  
		Size: 50.8 MB (50835655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674f3b9941e4d9de02b85ee47bc12000ba59678e24782fe74612ca1a8b088fd8`  
		Last Modified: Wed, 24 Jun 2026 01:15:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:181fca2ccc5d19eb725fa7fa9bea3fe5929149ad1b4496af781811c7ab1c830c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff93dfba117c3c644c4cbd23c3903305c2cd68a8cde31529a671f0f683fb13d`

```dockerfile
```

-	Layers:
	-	`sha256:62c66851234e00c87828c5e6601d4a3a2df08fa485ce2446dbf30d02e00d2ee0`  
		Last Modified: Wed, 24 Jun 2026 01:15:19 GMT  
		Size: 3.2 MB (3168157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd0e54951ddfa654e148f5054d6a8a877f8c6065a7b8522735b1b90f10e8c4a`  
		Last Modified: Wed, 24 Jun 2026 01:15:19 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f623a763793471a39350fc8b6f90dda1c0c3c19edfe7993ed03c7bf652c8b450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53138292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbc1c605396b117442b52fe32447f8d8647bbb7a8fe1145c2454b6b20e7b694`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1782172800'
# Wed, 24 Jun 2026 01:14:17 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f6ca872a6509bdff9ed4d2a17e7401c77a212fe8a0b3f25dd74f231b88c4ac31`  
		Last Modified: Wed, 24 Jun 2026 00:29:30 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70aadbd80b5dc07f7c48a37d4f6d7ee16ea32d1bc2ad1ab8997fb36e9a2f79f`  
		Last Modified: Wed, 24 Jun 2026 01:14:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a05e671158c9d4608e541316dba98dd5085509200ca4a57de957f28fd94c91b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dcca47a9617204b631a8d0bd7683bc3b7b033484550945de1b3e3dc1007200`

```dockerfile
```

-	Layers:
	-	`sha256:dc0592a1aef46297db4e8889ab452d312800a22fa8116a819c4dbee5131c3681`  
		Last Modified: Wed, 24 Jun 2026 01:14:32 GMT  
		Size: 3.2 MB (3174468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69031f520d74f950c2c844b26388d9a2294c4077a94b355f3e3de22fa4fc9d9f`  
		Last Modified: Wed, 24 Jun 2026 01:14:31 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:2e0e08497acd1ebb0cec21ac2db1cf99f531b283c10154fcf182265638a9c79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47802755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310c1230a94f0340140abf318c4961dca37aa7f0d418349a489f21fd53f606ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 22:08:26 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8e8587ba31c7d2366e168db6284a9bad01ffdd923354b652e256b3c1d990522a`  
		Last Modified: Thu, 11 Jun 2026 02:52:24 GMT  
		Size: 47.8 MB (47802535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df6665c8fb6a2355bc7de96b354f90774e09697016ce72a9cf9e76804661cb3`  
		Last Modified: Thu, 11 Jun 2026 22:09:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:58d86f2a29f89e9e52fa251af6d6fd7c07cca6685803c5342835bcf09ebf6541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4a4008ffdc3ffed6345b8de72eaa34c91ac31433a6b64b973a71f010f42352`

```dockerfile
```

-	Layers:
	-	`sha256:a71645650f65b9e132e1b466d325b8f63861dfbed80652098f6471eca23b3209`  
		Last Modified: Thu, 11 Jun 2026 22:09:21 GMT  
		Size: 3.2 MB (3163280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4ab347d0852ac18d16e92fb8a29ff04a9a0b35fff88bdbc1559b1560bac523`  
		Last Modified: Thu, 11 Jun 2026 22:09:21 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:de7e6b4d980b4134f078b2e30993405c4bab98dbd5e4b576146310c554edbbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49386282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b27c50552daae6c81a5cba0854bc6e0b556ff211aab89e8eb0c8d154fd728d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1782172800'
# Wed, 24 Jun 2026 01:13:56 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7dd3ac5a4d6cc02991d8abeefdbdb83784a38fc243a75f4b2585b5ac5670bc13`  
		Last Modified: Wed, 24 Jun 2026 00:28:11 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e65fc378b34dcde4a42d104be30c148d42d514952f06c17cf465edc66b4c8b3`  
		Last Modified: Wed, 24 Jun 2026 01:14:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2f2dd4deddc18f5d0e3fbd46b8d6cc4889cc09e01d0e8f17213702b5820ab493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07560928ac0b321c753403fd4f90eda8e3e80c3562abb839a0ea6a23cfddc36d`

```dockerfile
```

-	Layers:
	-	`sha256:dafea8f9d570e429dee9ea25307c8b747db6e178515586ab7fce49d7ff9c686f`  
		Last Modified: Wed, 24 Jun 2026 01:14:07 GMT  
		Size: 3.2 MB (3172402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024c13c4d8f02416ff477f4f838c560265098f66dbd8468099e1b427ea0db0f0`  
		Last Modified: Wed, 24 Jun 2026 01:14:07 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
