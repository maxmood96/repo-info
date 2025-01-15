## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:104f8217967876111a4e8f72495f5f0989a2d6b9c2b91622ddf66e7371df6e36
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
$ docker pull buildpack-deps@sha256:c2259236a1d14d46119565d55257b0715e7ab73cd5c7c863ec2f404c9289d266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72538605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3007b535d306fef86c0cf0d3c7c44a7f867990e9a2d479a3d7b5971741414c6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e37c5777422e20e7c469c441ba5c4991906c4da72a0a0466e9c41e4980557e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284db7b0d69dbfe99276bea68955b71cddc38dc89f87dcd45995c217fccd78d9`

```dockerfile
```

-	Layers:
	-	`sha256:ba54796c42202ed410ebf206363219bb689790ae98fb378f6b6bc5c2fd917426`  
		Last Modified: Tue, 14 Jan 2025 21:00:27 GMT  
		Size: 4.4 MB (4359309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa09896476db9466bff04242a59ae1536d64728cab950a3d81dfaf67fb524059`  
		Last Modified: Tue, 14 Jan 2025 02:32:43 GMT  
		Size: 7.2 KB (7163 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a899961fa921dbc9e00cc78b4b1f62943c3023a5c6d6b3c7623f740aabc971f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68739962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c624ca24458a8a6c0a3366799073ee5fb16b77661fdfa84bfaddb487adcd152f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:237814a70d9f7e95f3568236c75036fcef22a88f1a76245129eca111484c0351`  
		Last Modified: Tue, 14 Jan 2025 01:33:00 GMT  
		Size: 46.0 MB (46006814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538440badda779e62c187f05746a171687a461254bcff139b6eb8551e262665b`  
		Last Modified: Tue, 14 Jan 2025 06:08:28 GMT  
		Size: 22.7 MB (22733148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb36206b1465a28110cd79f8f3404a69097a85250d568e1a18d8dcfae0fff068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7964f87a37fbd23d1aedb5c5ddbd291ec6797277d51450bc924a3e9bb8baca`

```dockerfile
```

-	Layers:
	-	`sha256:a4e1efb7dc43b13fe331d0797c2defc64c5ed66e81e5030746fab22c8429d676`  
		Last Modified: Tue, 14 Jan 2025 21:00:31 GMT  
		Size: 4.4 MB (4362825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327f27549dfe6dd95b57c323f539afe5ee5287a8e1a0223bd3f5a75b66c1ffac`  
		Last Modified: Tue, 14 Jan 2025 06:08:26 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4686f34a12b7ba65b4f11f4f131659a72ee77ecdb70b5596c62be906014be6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66144286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30954800b5d646115071f419da7a4c111bf22f177565bb1ae44c38febb936787`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 20:44:11 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 23:01:46 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:884a815c786e47e1cd19dd07d3261d1f7b536f2547ca8de3cfa09eae70c5e912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21e152f7b7663cff663d7efb1f39a029855e1cfd149ce8e1b73accf73ae3ffd`

```dockerfile
```

-	Layers:
	-	`sha256:6942b89164d7854c0121815e4775aad357aae3ef5d10f25c72a3c4db72aa4291`  
		Last Modified: Tue, 14 Jan 2025 21:00:33 GMT  
		Size: 4.4 MB (4361606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded1e1bc0636ed195390f4550ced44583fa533a4c2eb52778648b265ab9cb887`  
		Last Modified: Tue, 14 Jan 2025 08:58:06 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0170587e7fba0a3149589dca64146ca20fe18a7260ff36a4143c849b5e0c1307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71905121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f8888b0c36370bef73492e594fa7ad5a825f8d6da2b0965b7648ca54040c4d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 20:36:35 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e08021498b8290c438525fddcd4b8953869173ef430788c193508d4ee24a949f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3e846cb715fea407c0d60762543e21303c49af6602772750c058177add28ac`

```dockerfile
```

-	Layers:
	-	`sha256:b5211cf91856f76f82f7a27489bcaba10c9f96883d90c5f9b7a8c29c37cf875b`  
		Last Modified: Tue, 14 Jan 2025 21:00:37 GMT  
		Size: 4.4 MB (4359582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004281940275076a4be044fe1376d37bd10aad1332b721f440c32ec3706f0e3d`  
		Last Modified: Tue, 14 Jan 2025 06:59:52 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e6426ba9358123ac47fed618c108b0ca5636f728a9e9025491841cb6b57503fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74357104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4d68773b95eb52ed4a4f3d0be8f904adb808ff11cf219c8c7347aae7ecef83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 20:42:04 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 22:15:37 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c252c937970bca5420e0a2762f94e68e8c8ecaef4897973b6dc873fb9f6cc6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51201a0e8ced35cfd6c80d11446a91a362cf671f2126cb9a9782b8ce6a21ed2d`

```dockerfile
```

-	Layers:
	-	`sha256:5f4321c27cf36e6050544d9dcb28305a11d5ae10fe3fbc5ac41b71048ac3364c`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 4.4 MB (4356366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086ffe7057e8efcaefc2a2583a8e05fb94c8bc7d89b5307261454d5e3ac744e7`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 7.1 KB (7134 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7e82a0704e62d860a1aedcddb8d8649f97cf31831f64bc7cca3b3b57d143e5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72410267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93d76303f85bbe0d4d9125b1ba100a20c6c695a5ed02a407481017ce52c3617`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 20:45:22 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Wed, 15 Jan 2025 07:16:12 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:748b0707022a125c271b74edb18d3879dc9255eac8b1414f8c2ae6fd4c121716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762ff7a77a47447b52f9c5837805de7f8f22ee4d1be2cfde565f6d959f16523`

```dockerfile
```

-	Layers:
	-	`sha256:68a0baf3a618dcbd62663d3685d9fc7dbcc554f6503f61dc83b86d7a287f8558`  
		Last Modified: Tue, 14 Jan 2025 21:00:40 GMT  
		Size: 7.0 KB (7003 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8987d33853ae6dc6f6b0ca495edd4a85637a70ee1df067d15c236df592778274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78030576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a260cac16989b50445b080b51ce054a3a096d855680137f935a3826c3ae1ec6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fbde1cc8078e0a2194e570142da63331db259da0fcf3836628c919986eab0205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d4b16a9852b459b20ea04fe10df264fe5b252d3b79260dfdd787e191cb788c`

```dockerfile
```

-	Layers:
	-	`sha256:83728016b644299825d1c1a2f8a9d786922dddca0dc2bc6f4dabbdf4ed12a0e7`  
		Last Modified: Tue, 14 Jan 2025 05:30:14 GMT  
		Size: 4.4 MB (4363803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d1346c65e7137d27c09c60f9183400a4190da768cf74be764067acc47c3ae12`  
		Last Modified: Tue, 14 Jan 2025 05:30:14 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ad1cf495c4f9fea4a47ca350da915718e2644ca1f23bb298445e1397413cab1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71189536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2841b2e5474ab0b25d2daaaf452c2106c7f98f0be7e98f471612c3814f05326`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 20:37:18 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:198355f7e6b53ca2f59c5b26a36e145eaeeb6cf469178d9839c33aeee192e24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f5b026ea63701dfc4220b2ac331826dc20480b3283f988548bc3e5593c466a`

```dockerfile
```

-	Layers:
	-	`sha256:1f6bd970fc24f8946151021d85d0743b91f08493577216fbcb7ff9376bb29bac`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 4.4 MB (4359005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2ee96ff087310c83a2765c691333dc93c693b356220ed247121c5dcf62f1d5`  
		Last Modified: Tue, 14 Jan 2025 21:00:45 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json
