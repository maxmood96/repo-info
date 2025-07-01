## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:bce3d1c214e7bdc179b6b9a8caa42f9ed0b9adebb56eb5acd119df9ae7983834
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7bf2f0e26c1abc0687aa80885244d2ee8beb3f1d7e4e529dd0de1ca8132b586d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72514976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a75932823c7de703b2df11bfe23256fa75c001a615f191a89fa47a64098e78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e1bc5782eecba09f662ef11c429519a43dc26b0b928a1cc6ea3b3e3178335a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add32ba6d4444372f7db58f7e8a69a6db1e3a325f73d071225177ad3f87f23fe`

```dockerfile
```

-	Layers:
	-	`sha256:436cb3a9fe89cfb2e6467f882173ea4899d87bcea00ae238c6ea33a03dce0d6c`  
		Last Modified: Tue, 01 Jul 2025 04:09:18 GMT  
		Size: 4.5 MB (4507222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca04b504391ead8c6487b71eeff6eecc5c09c6fb55ed5a8d6491144bffa3961`  
		Last Modified: Tue, 01 Jul 2025 04:09:17 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ca35359ad88286afdce8c573d066da477eae76d179c1940811aacf361e706068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68720783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbb36335cf5cbf092c776dd6c15804c30cfaa13ca376e5697ea61421dfb5bd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fe4bc1cbdee9e4aabbc6c58a2156f300e4c3158cfb501698b1878215892a8763`  
		Last Modified: Wed, 11 Jun 2025 00:30:31 GMT  
		Size: 46.0 MB (46026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7973a0421a43933f783f2da8c4e6210bbcb63636694bdb47f5939d46f0cd8e74`  
		Last Modified: Wed, 11 Jun 2025 03:12:54 GMT  
		Size: 22.7 MB (22694196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:041b8ae0774fa79c29fbf2571a8e95fee40285b8be1a03b7b038d7c77f89ac0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4516922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a526f977e7bbe85908de4e61a8ff0391c488371a3b6b6ddb2ce092fd1e9b87b2`

```dockerfile
```

-	Layers:
	-	`sha256:4fe9e8e9a5bd814bf6a79058f46f525fe19e999b8accef704e7b05e91e86f4ab`  
		Last Modified: Wed, 11 Jun 2025 04:19:53 GMT  
		Size: 4.5 MB (4509690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01809453c3a77c79de870378829ce6aa8bd2f14c9a85313ef1086e1c9416c4c3`  
		Last Modified: Wed, 11 Jun 2025 04:19:54 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b1545be3918498f69c714b16ad8cd3ba507372bf445a38d9e11795906417d615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66132852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ebeba50c55b88ad3a9f99800983bf001c3b4ca4bb6997f56d76a103cebd290`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05d007b1a693a23681e1ede06f301048005c73ac2def08c3c891a4dbfd3517f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4515395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b6aabff89950175ba496df469a1c4fe1ab01d72162f61553f1f1d793008e9b`

```dockerfile
```

-	Layers:
	-	`sha256:dfc873905a1d321a76eb5a10d4c80e26050558eb3cb60eb33583aad3a1bf2083`  
		Last Modified: Wed, 11 Jun 2025 06:07:13 GMT  
		Size: 4.5 MB (4508163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e491e371a1e381488297874bffb4a5b244658261e37cffe691e0a50f568d8c62`  
		Last Modified: Wed, 11 Jun 2025 06:07:12 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1c008311b8cfc2194dcd740076096958c53e6e7a101afe909cb9ff9eb7eec39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71890409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f3702abeb7359d7e0dd8736475d99062fbe4c3d774a9c67d267fadc76d95a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:950d65b39140263dfff51d55a531b2871ba5e4bee33eb638aede1b1f59472131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4513395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d924f39433283ee461ad66011bbba7d5e40163eeec012127dcf4b944171be753`

```dockerfile
```

-	Layers:
	-	`sha256:8190f8965eacd816048887dcd6ab8d40400d964ede5fb3fcded38455cb0fe3f1`  
		Last Modified: Wed, 11 Jun 2025 04:06:53 GMT  
		Size: 4.5 MB (4506139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4505bc53657b95cc858eab1a64ca09e77398aa0231ae0bfa124f79c6b02acce`  
		Last Modified: Wed, 11 Jun 2025 04:06:53 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0d5d9039e97ebfb72bc9ff59af54c2ef27e683c0b293c7b7a037d3e3b6a2a872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74334354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3783bc1a5e4e2b535695dce3d6bb2b6bd73f2db0b2546c27c187a75aa7c46f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8a54ce59e0f5834e6f739421e0bc846fb58a9ee1605884c85e59a8d2424beac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4511479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89b6c6534500a113eefc758391a8c2bde50735277efa579e4266acc8aa31f34`

```dockerfile
```

-	Layers:
	-	`sha256:ea0ba44531886cee0bc2591e756d71388e0d670cebd2bd1144505783289117c6`  
		Last Modified: Tue, 01 Jul 2025 04:19:57 GMT  
		Size: 4.5 MB (4504342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af7ac18d88b096ae45f9209c3c24f37be200945f0e7dea4195bcb913154657c`  
		Last Modified: Tue, 01 Jul 2025 04:19:58 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d055d6ee47be487b7f4dc31e05ec05c20549b6a6c6e8c00454149cfab6f7011f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72374155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5131293c374f6185f23b044e10ad37ae446cf674048badb98ad8eaae64465799`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad14aceadbd8dec6fff454480e4e098f48c504f528663aa483f102aed68047`  
		Last Modified: Wed, 11 Jun 2025 13:00:39 GMT  
		Size: 23.6 MB (23598558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3f1d01814f8d9fd49c03a53d824d3245e364983b78d875b36ef41f5e4d30465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce1c190af0bf09816783e843826c5ca545f432d1db34e4bd08e2dd19d8cd89f`

```dockerfile
```

-	Layers:
	-	`sha256:5742aef8fc40d6f81ed357cbf643e62f50f51f3764ece0260c92fb96345753c5`  
		Last Modified: Wed, 11 Jun 2025 13:19:56 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d67727ec27ebc952f53d22ee2f238f77cddc3196e63ac99345ee4138bfdd6e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77994782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72c160b1e125cd24bd6e62430f3aaccba4345d0c27c9359b98fa1667bb6591b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f6f736caadf46080225440abfce28f1a2978e854a95a966ffa27a3c645e4e21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340e7c2ec9aba51b3c451f4c1d7773b6e20d5effc44dff3b708c3e221aa1cc89`

```dockerfile
```

-	Layers:
	-	`sha256:65a4e6bd197ca1a9ad2d3b508e85476a009c5d0bf8f91990c5e9daeb265ccee1`  
		Last Modified: Wed, 11 Jun 2025 19:20:01 GMT  
		Size: 4.5 MB (4510486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cd2b4e70ba2f70857ed269b8ada347485c527aee63824db277d3fbc0ae9201`  
		Last Modified: Wed, 11 Jun 2025 19:20:02 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e65dda7e81d457c8b75ac723fe0d5b8d41947ddb3cc0f3bcf1f17817250d4c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71164410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430105dee5421ef8dc3a703434d5a168e8b0059601dff29060a262c9e6edad94`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83030d8a694f635685bec1602230ad1d5fec4773d5158ddbd025887cae3655fe`  
		Last Modified: Wed, 11 Jun 2025 10:15:26 GMT  
		Size: 24.0 MB (24015002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cdca996b2b010162d6c2e78b1012c381004c6381277fe9ca2499f4ca6f08eed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4509833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe38c417688508a34020b99ed4beddf52b5b45ab20797bb33b36972972f08c7e`

```dockerfile
```

-	Layers:
	-	`sha256:275f212a8ea1e9207b1eade0cb0df828b2d3c93be46e32ac432ae253854b519c`  
		Last Modified: Wed, 11 Jun 2025 04:20:14 GMT  
		Size: 4.5 MB (4502670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8456b451d553ee0346ca0b43ba81418d0967278e9aec67052690e6941b3df8a`  
		Last Modified: Wed, 11 Jun 2025 04:20:15 GMT  
		Size: 7.2 KB (7163 bytes)  
		MIME: application/vnd.in-toto+json
