## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:e2aede2250dabe0e0364449ac70e924ff0cb59a060037e547131b00439778803
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
$ docker pull buildpack-deps@sha256:c6062a1521167802af25cf8ede0d7ba70aeea57ceef1b37f555a81bdc381cc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72510071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb386bcad83fbb16854586fea362d14e516f12c4b414b993924fbe4001e3366a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ab8b91c2eaa0f65e85bd0dd0c6c5daf22b3cdbadb47c25e5dc3ee3f30fcf9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bdba855ec67daef696b8184be3f349ce9b806971d57a1ec9c738a7ad480212`

```dockerfile
```

-	Layers:
	-	`sha256:32fc78c11c5c107ff2c4f4ea01493b0fc550284bce02fc850772c9d7b588f2be`  
		Last Modified: Tue, 09 Dec 2025 00:08:33 GMT  
		Size: 4.5 MB (4513691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20999789646b3493fb4fb04dee853797ab6a2e222f43f89ca7b0d916606930d4`  
		Last Modified: Tue, 09 Dec 2025 00:08:32 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e8430cf6c4dc9673dc8983075bf6fd344b3dc409d968904e41a6bcabf898797a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68721546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec05af5d66625a61d805bc57160e2f9a39084172a995f60f2d5ef837270b254b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a635f54eaf3a9fce0549b1b49b875e73326ccbc501c3133d86c2ac8fd7828fb8`  
		Last Modified: Mon, 08 Dec 2025 22:16:16 GMT  
		Size: 46.0 MB (46015801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f70892cf40cf00afad948163124cb46c26422ae7a58c48384378f9afd91c3e5`  
		Last Modified: Mon, 08 Dec 2025 23:53:57 GMT  
		Size: 22.7 MB (22705745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:46a46d12c434f2a950d19e4b3a85575ec6077afeb97c8bcb144cfe07ff87a906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4581832b73dd8417b77ae11f68c80700d1f2cfcfb12b40aac87df5d9c70787`

```dockerfile
```

-	Layers:
	-	`sha256:27e38d70423687ac55206707d9e0c4088fb0a6f545d1fa16294fb19d56730154`  
		Last Modified: Tue, 09 Dec 2025 02:20:36 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c1dd2a87317f4054e996fa374cac546a5cf66e1b2a3b06148c925a21035094`  
		Last Modified: Tue, 09 Dec 2025 02:20:37 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c04efdb39d7e7fd3b02aa09c67efff096881a5834d67da718678987672592eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66130701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a15da94445baee12e6f70ef33cc7c6b34f62618b651645252fedfb021e902f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d09693cee7d7be5acfc877e846bb6954d05f57f6c45d1a641761ab312311e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5c9a42cc00a22c15eb56061e5b006acdbff17dd613ddfafb1c935e941cdf77`

```dockerfile
```

-	Layers:
	-	`sha256:3ea604319b56d5b1d3eb282d62554f1a301c236dcf6d2a10c66fa4090867b0cb`  
		Last Modified: Tue, 09 Dec 2025 00:18:09 GMT  
		Size: 4.5 MB (4515980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f2d2f628f388727a4ee41f7265866a4285e6edb06553ebc3e579fe1e79a787`  
		Last Modified: Tue, 09 Dec 2025 00:18:09 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3710e46de5d7401b9d5fd22a92a919cb0f171ece91d1df5c161ec610c90cfbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71957318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693d571b9e36aef3147316c9dcfed888848ea35305ed6b550ef144d1245f6083`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:122bc1c38a76a78e6d599eb7a6cd62a29894439d81b5098d6047e097af0d2afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5313acfd3f736a99a107841b309971a268228afd55f958e3a7a4c971961086e`

```dockerfile
```

-	Layers:
	-	`sha256:1eb74a6667919d893d99a84f6c5fc898c564f450246721796bbef97b3f40fdc4`  
		Last Modified: Tue, 09 Dec 2025 00:08:34 GMT  
		Size: 4.5 MB (4513952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07af5de3a53957a24faa74643dbf7439316a29fd85c10af7f41e29cb9cd9db1b`  
		Last Modified: Tue, 09 Dec 2025 00:08:33 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a3c882fba06e84aefa253cf37b4ba871d16e7d4473267c2c32506c2785df3e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74331158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b51c7f22cf7dd908ac40b5cffa855cff74ddf67a2d87d546302d76fef829077`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8c9cca3d9f455dde3fab1917d275b029f5f2978fcd1f8f1b757098b58abc9d`  
		Last Modified: Mon, 08 Dec 2025 23:14:28 GMT  
		Size: 24.9 MB (24864339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:91236a6ce1ea251e805212a6d7a14ac5bf9511b26ddde35056087272ca37345f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad14d3991a17e6d7b74b79ce4376946909b50189d2c0002ee8c9e14f580370a`

```dockerfile
```

-	Layers:
	-	`sha256:83338f0bc91a164a45e412f1e449959b88d9d6bd5ff1cc09c9fa6e4825a37d9e`  
		Last Modified: Tue, 09 Dec 2025 02:20:50 GMT  
		Size: 4.5 MB (4510811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27a02d795fa2e0ba6425079f1c025fd10ece105fec08fc0831939323cfdf3fe`  
		Last Modified: Tue, 09 Dec 2025 02:20:51 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:83ded9ef4968670a76f9d5e64355f969ee935dd462a6b0ad16adb78d9a0b7907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72374994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b109676039624d88643b6458a868a23ffe90d75d030f986bd85bf3babff22`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf41c56cb3beefc6b6211c26bdc048d41c337f12bc0bbfcfa89dfb5de99b7`  
		Last Modified: Tue, 18 Nov 2025 19:40:58 GMT  
		Size: 23.6 MB (23614038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:362dbe90e78bb2b9331fe7fca3eeb521e9def9f745a31a823f404552f3da461f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693a69024f6fb205b96ef575e57bf63efa845e8f64bab2912a53d1a21d770931`

```dockerfile
```

-	Layers:
	-	`sha256:9336f6ea30ae6e73fadb64634adbd532bac5df480f63499b2650e25a6eaef946`  
		Last Modified: Tue, 18 Nov 2025 20:20:03 GMT  
		Size: 6.6 KB (6649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:03f99cacfb91360ed7ec76b1b75026d8dd5c1c632cfb3e9a05b6e3f17ccc197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77999186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e11ae672aa5447473be4bd2d78f316e9747e2a870daa46948960fdc6799296`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4109a037ac4c69c3ce26e6d14e10c867842083c363485abd63db45502611991`  
		Last Modified: Mon, 08 Dec 2025 22:28:59 GMT  
		Size: 25.7 MB (25672209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ebfa39ab7894d5f4b841c629fb5c3f2b0da117a4dcbb01964874aab1315fc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbd29eaf4827b1eac12e9dbad001f698b164c8fecccaac33b8837b0774eb7c0`

```dockerfile
```

-	Layers:
	-	`sha256:4af00ae87070be83efb7bd600ee89b461ec0ff462853469941a84ed7f8b9c1e3`  
		Last Modified: Mon, 08 Dec 2025 23:21:04 GMT  
		Size: 4.5 MB (4518315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91fb456eb21cd2df615dd13ab307e6869e883301d67917a075843b568bde91e2`  
		Last Modified: Mon, 08 Dec 2025 23:21:09 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:166b3b250c2d1996da724ed913fcf6fa6130067f7f0aa4a2e083dd2dba4c7200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71164821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5eec6e9f686ea65ca29184e15ee52164b1860b0dabda12383db3f34565e625`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f16ae0686c09031c3054990cfc2d42dad5583f380c7afbc46985db44cb65c41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefd51f9802aa3775c5f41819fbe0782b3cd3c530930cbbb91718426c3686dec`

```dockerfile
```

-	Layers:
	-	`sha256:9b34964e5caebdee9e6ed20b8f79d47951350eecbc9264747514301c594f9963`  
		Last Modified: Tue, 18 Nov 2025 05:22:38 GMT  
		Size: 4.5 MB (4510495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf2257c81946ebc9660f67f3fc57992a6bf1cb03af326d735501a42a789c031`  
		Last Modified: Tue, 18 Nov 2025 05:22:39 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
