## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:59eed0e0b9451ecf338d367e65b782b6064741cee8b7541a014012e7ea2c9d88
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a402fd948d62e1f1ae75d8a6a0559296213443a90f29500f23d9c6d729c510e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72509980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83445ea8dc0a615caddd520325738d8331e4b1e65aaee7d3a8c0959fe0d0342`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bba18db24014ba5bfcf65486d97507ea1dcd897186714dabdded994f639dc9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4513030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14e184c90dda6f9defee457af07d3556dba25ce1875f8e5d584800fd3696575`

```dockerfile
```

-	Layers:
	-	`sha256:9a6b0d8a0d8881e7182dca2ee0b5d64c57786b106ddcae2d501523044b62677e`  
		Last Modified: Wed, 11 Jun 2025 00:07:16 GMT  
		Size: 4.5 MB (4505866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f960db62a55ce9ce278a0c9f609ff6a0d4c80e22ce1877609039295afeed7247`  
		Last Modified: Wed, 11 Jun 2025 00:07:15 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

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

### `buildpack-deps:bookworm-curl` - unknown; unknown

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

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e0c8bbd81831c468bd34e8895d75caf2bd3d7d1753526ebc05dd7b27901b0fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74333180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe1e3de12fb61ab63fc1aa8a4fcc5977bda270874ee09a2512cf11a51d2e453`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c75f4bec42d705c7461dafeca15f760baded20b8c9c51e46af0486bae92b6d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ee2c18a14e2247535ad23558ffa27b90b3532c7b650247fb85ab76a48693b1`

```dockerfile
```

-	Layers:
	-	`sha256:229d236f7698edca5239178dfc367ac38618184e5685384c0b493b69b268f474`  
		Last Modified: Wed, 11 Jun 2025 01:20:13 GMT  
		Size: 4.5 MB (4502986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff30beb93213cb3822b0d65631703fbea63d5ca2bdbd9f9c65439fcd8e52b171`  
		Last Modified: Wed, 11 Jun 2025 01:20:14 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:bde0b234b62790a825c929bacf4e4fefe0fb0f3e16fa5db0663767f401068f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72368366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79eb836e49d6dd33e836fd0f277f58571c7e846c70521629bbec375c959e9085`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc05e2d1c7537a7663041b66446ee4a24f98e673290839931cdaf3c0b93f56`  
		Last Modified: Tue, 03 Jun 2025 14:36:17 GMT  
		Size: 23.6 MB (23598613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5969b50970c631564ddd670b0af2622f135fc52a0d7582e9980f536935283e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70de946090286097339c2692af0397f80ccd82314d0fe296bcd6cbe48fa09ba`

```dockerfile
```

-	Layers:
	-	`sha256:36fc14c9036ed037ab3d98c089ec73aee8ae37da2618d6ce536435277d59201f`  
		Last Modified: Thu, 05 Jun 2025 13:07:44 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2ed85b76397ecc3c35352ae354419a4a63cb6d200e90f55b4a33c43461e01cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77988916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884bbe6ff02f91883d58b5a423fdd84683a14829c57a44b7f578397a299cb4a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b76f20b7a6db2e5b39870d22db6b0bb21da6e4ec39811f3802a8cc5a1afde93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4395540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deda24d2f55caaa586123f573e42802b100e75c86198ebc758f125b215bf7002`

```dockerfile
```

-	Layers:
	-	`sha256:0d4bc0f9d7ae33da9fdb29b5ac68a4657327916008a8fea9ea00353cd8e2b452`  
		Last Modified: Thu, 05 Jun 2025 13:07:50 GMT  
		Size: 4.4 MB (4388338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b23babb05ffbbb217827ff8f988748256c3be4259614a786aac7bd35e4ca041`  
		Last Modified: Thu, 05 Jun 2025 13:07:52 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

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
		Last Modified: Wed, 11 Jun 2025 02:50:11 GMT  
		Size: 24.0 MB (24015002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

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
