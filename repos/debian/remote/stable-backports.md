## `debian:stable-backports`

```console
$ docker pull debian@sha256:695f5632b530d08e5a5b6a796f8187b874dbd20e1ba5ffed1c37c48a3b9a50e5
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
$ docker pull debian@sha256:adc358414278341afbae62d772b5ade0f25d4f4517753fce4252acc3e2f4f5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49317342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4717c4180f8a2debedf876bfa23f91780acb2f6b3077b59e560f00069dafcec4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:15:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:76c1b568d783b0a559a2770aaeab50f23c7b7f3dd90364c64fba1639cd29c86d`  
		Last Modified: Wed, 10 Jun 2026 23:40:43 GMT  
		Size: 49.3 MB (49317120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b6ff084a7483c4db14a2315ae6dec0128b37205730bd5629f6df1df7754276`  
		Last Modified: Thu, 11 Jun 2026 00:15:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:998d0159a9ac6d987a20681f3a0b73d22f324985381540a99f3afbfae91a8f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a245ae97f4b28d3dee6fbea8cd4f8aef313290c5aaf592909c7571b168b93d13`

```dockerfile
```

-	Layers:
	-	`sha256:d5ec64458f85e9794e908a5b75a7cae83f5aeffda6acf7e6de4d425246e43353`  
		Last Modified: Thu, 11 Jun 2026 00:16:00 GMT  
		Size: 3.2 MB (3170955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45350d579edc56a0a82bb6c7dc8cafa10006b95a4784afcaf0588288e36da56e`  
		Last Modified: Thu, 11 Jun 2026 00:16:00 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:bdb3faffa6b3c4a419fcac0dbb62e62313f6337120b3fea328f2cfb777067864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47495032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfba61f014d28092ff605eabaa7c18bc728552f62c3726eb6de2fee2b9a6bb2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:15:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bb365e18e4a59d04337d032f20a4472965f1e2eee516ab699795c01ba82765df`  
		Last Modified: Wed, 10 Jun 2026 23:39:14 GMT  
		Size: 47.5 MB (47494812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb88decfb9149bffbd421d315e137396534dfe725a8138bef468bdc211fe144`  
		Last Modified: Thu, 11 Jun 2026 00:15:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ab6a4003887923c302864d59c5094e8f21e0ed7973c28a4b681cc316376519f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1037c1e8e296d510f86a9977d79afe7d936542be942e949815e6ffbf83231abc`

```dockerfile
```

-	Layers:
	-	`sha256:a7f49de777203be76460497080dc08901281d27634604e3982702dce04ea730b`  
		Last Modified: Thu, 11 Jun 2026 00:15:51 GMT  
		Size: 3.2 MB (3173892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7115e252cad6943d6213bb718bdc5c6efcc9f46088e7420e825a9f9c92d61ce8`  
		Last Modified: Thu, 11 Jun 2026 00:15:51 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ff1825e7bb08e0f43b8e26c29f729bb722b51a8350b3b44efa611f85ecf7844a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45748861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6508ae31f474c16f44a8c7a24961ccb46a2ddfb9c08fedfa2c521d383e2ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:15:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1465566b8e00c1e1105244e8396fdd6c02b3b7747ce3bdbf2176503872c00e05`  
		Last Modified: Wed, 10 Jun 2026 23:43:10 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8017d91ca9b91e6d3a29caa200ebf154d02ae7f6d71a003111d0b6d1cd030a2`  
		Last Modified: Thu, 11 Jun 2026 00:15:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5184a3714f66748712f92f5118643c7690219e0928b85dfe4533e5cb071aa91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ebacbd723507ac5256554ff057e7171bfc8ed407f01177d5e79c153f2247a7`

```dockerfile
```

-	Layers:
	-	`sha256:522a4e02324f704fda58967dbabdc847ce488c89898998175008e150b9560e27`  
		Last Modified: Thu, 11 Jun 2026 00:15:52 GMT  
		Size: 3.2 MB (3172329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8163f66e6be8f00177a495404c5401b5c883d7413ecb6956eeb93b5b08b28278`  
		Last Modified: Thu, 11 Jun 2026 00:15:52 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:906fe8cca4086c0e155c64df90e0599fed8e7970b2cb5595d1ceaf3374935a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49678390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6580d03e174fd964bdf941f5b747852fce719d18d03921e56ff55237f924ee4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1781049600'
# Thu, 11 Jun 2026 00:14:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:982e76ff0ff5fd68cde264ba90670e342dd29a01ef9d0559a2e682f70d2053aa`  
		Last Modified: Wed, 10 Jun 2026 23:40:14 GMT  
		Size: 49.7 MB (49678170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3425d0203c3d7c78e54b94659f07d2ef5a91fc57ce63bf07b5a61b24b4dd586d`  
		Last Modified: Thu, 11 Jun 2026 00:15:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c94294aba4824646f9630da336a6df5a12c8987e76bd4c204914f153e2847a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bd703657f176ee05f149c9d81f65ee2a60d05084de62e3bb9e7326474c641e`

```dockerfile
```

-	Layers:
	-	`sha256:6b0865deabae9f0a54bd86ab342d7a60cc5f5fc0f0dfc53f422634ed4ba4b273`  
		Last Modified: Thu, 11 Jun 2026 00:15:00 GMT  
		Size: 3.2 MB (3171799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6b53c9af198ba80e74fa8fc470f829e00dbb03d248791024973cb02c0d67cd`  
		Last Modified: Thu, 11 Jun 2026 00:15:00 GMT  
		Size: 5.9 KB (5852 bytes)  
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
