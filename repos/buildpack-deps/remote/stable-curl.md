## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:68118d60d8b0b2f639c8a644e677d3d79c9179b21b8e0f09c50ba0974c1a5536
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e0fe68c4b061a8ffafddb203973e4b66b91cc1de3cf300788e50dfc035cdcf0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74903576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7852ecdf1490acb07acca731d201ea37fab7538d3292046e16cbb6536fc1b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:316ca827b517ca613365384ac440544ba0cad1d4fc83eeba6f204034372122a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a84a9deb205b5f7f8740cbbcae1dce6a9354616a76f426f2aac68e642cd2ae`

```dockerfile
```

-	Layers:
	-	`sha256:8b08444225b26fcda576b91b707b3384399f3efef48ed60ce91cfbef1ee2521a`  
		Last Modified: Tue, 30 Dec 2025 02:21:04 GMT  
		Size: 4.1 MB (4118874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402534085c27735c33a107f0cae6087af5c6b30f7300516ec76504967f485ae0`  
		Last Modified: Tue, 30 Dec 2025 02:21:05 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cc3a30d2ce8f4aad9eab821b8f4df82581e4573c72ad6bb41c2c2610e1305f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71794499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4c54f18b631695f1d72462aee2318905abb08fa54a8815d22c0fc69edafa3a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34295e8c92d32055cf38cee5aec380c4d26fb9f87d9d69deffe81403a9d5a203`  
		Last Modified: Mon, 29 Dec 2025 22:26:50 GMT  
		Size: 47.4 MB (47448770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cf1b0fd719c142e9016b7b007d0d982443d9aeedfc75f9de33d17efc3342d9`  
		Last Modified: Tue, 30 Dec 2025 00:29:32 GMT  
		Size: 24.3 MB (24345729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60114465c3e0cf3a57c2ba855b30f25a516b406a989b70616fecb9b820579441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a984fccb9ecde034961d34f2bdfa61b5415852d6535b82c20a90b969224789f7`

```dockerfile
```

-	Layers:
	-	`sha256:5b788229f8a19a9e5505dbf17bfbb3c68b5427eb700c63a0f5ec043b86447b49`  
		Last Modified: Tue, 30 Dec 2025 02:21:09 GMT  
		Size: 4.1 MB (4121864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f91a4298e610d4aa2c0ba62f8180c23641c04e4e03d20dbfaf734c4ce6dd60`  
		Last Modified: Tue, 30 Dec 2025 02:21:10 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:999dea1dbcb816ef058cddf4ee6eceb427004e449ec036cb3a4c0d017b3d1412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69338453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e71fbafed7acf027c585ecf7ed91003f418670bc8acd4cab4ea5d3622a6a15f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4eba7a08ba9825cabd599d8641314a004d500b627e05a38640b9d3c0bf389ef`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.7 MB (45718282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ad1d8bb6e8d2c91990f13409d4d822c19a3b9fb5463aa9033cd860aaa4822`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 23.6 MB (23620171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7422d5ecf3c771aed663d3d1d53a7af8dc1b4c509f04ba1a30a7f2a93cd72b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979e12bd18a85eeb123d02627025e9505e2449d9a61ec3d7a7c980dc11727e46`

```dockerfile
```

-	Layers:
	-	`sha256:9111da1fadb4e469e50ddbbfa1e54a52e2960f8b8a18f24165e6ab7ab4415715`  
		Last Modified: Tue, 09 Dec 2025 02:21:44 GMT  
		Size: 4.1 MB (4120375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc67fd4dc690daa65e0b11868b6c71e4c3d268320d4e9c9ae265353656fe0e4`  
		Last Modified: Tue, 09 Dec 2025 02:21:45 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a65ca32c6bec847c737c9b3afae4e787aeb54468f4ab50d1e0a8b8a16beeb97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74671238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22c0f7cc70fd16dad8e81ce06ec9b8303d532a768193cd41680645877f96f57`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7c3d81b5c4e9b21a8ff0107f35a479e9363288903fd7f4fba449382521d630e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac076e799a0906a4664ee567bee395decabd360a6c9d2fe396caf5d4ab93bfb3`

```dockerfile
```

-	Layers:
	-	`sha256:69aeb4f8d80db4061f8e2dc3ffbfe02af0062b949e3d2bf75ecd142b88d79baf`  
		Last Modified: Tue, 30 Dec 2025 02:21:18 GMT  
		Size: 4.1 MB (4120416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d72bd8f8298480da03de4e8fb985f40f3914a05366ac9d766e1545525f080d4`  
		Last Modified: Tue, 30 Dec 2025 02:21:19 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:26f14eacace0a571aa341cfe1f9eb139937ea05303c2545e193fda0d4be39921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5ebb28d415a716492daf8d9c113b71d78a76e3bccafb086fc6e0d308e806b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798fea9bbf98ef639c9ca23d745bec44c0d7b28fbd93792d4578fc5b43e7569`  
		Last Modified: Mon, 08 Dec 2025 23:14:38 GMT  
		Size: 26.8 MB (26776300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ad8f45a79baac25224fb6b9146e9495c47e20e64ba3641d6fbc00ebe0cf9ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3192f646d56254f648f6683cb377cd992d6180ed5e85f5f3d2b7d5c8c9ce919`

```dockerfile
```

-	Layers:
	-	`sha256:1100848e57e7e47a2dde9edcbed59dd17347bcba9ce16e13314792303f5c7f4e`  
		Last Modified: Tue, 09 Dec 2025 02:21:55 GMT  
		Size: 4.1 MB (4115982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309a31b562fc2d9ddbbba3d117c1404b9c2343ee8a7679976053f02f231edb84`  
		Last Modified: Tue, 09 Dec 2025 02:21:56 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:145afbc84ce22abb46497ae44085319285c2a1155f810485c7efbad6303a4e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80105253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a723a386dcdc60b2219bbc98d219a843999ae7c721b2eefbbe62947459a14d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0ebb153c297256cfdb50591ed7a3cf6337f95b71869a46655b0b36d632168e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3123ba241d5fd3c42f8ca5f93261d7210227089e76d1e26f05c6803b85724be1`

```dockerfile
```

-	Layers:
	-	`sha256:0ea0af9f4322a03f43a807947c1a6d6f5256b06531ac4719f9d63130a55c7891`  
		Last Modified: Tue, 09 Dec 2025 02:22:01 GMT  
		Size: 4.1 MB (4122720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939bd3625fd59501aebd42e9a62cec5da4e12417df059543bee9835061c31fef`  
		Last Modified: Tue, 09 Dec 2025 02:22:02 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:83c85ff470842004aa6cbaf5abf68015f2f15a8c126f46096fe05e8aff1acc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72724969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e93866111ee1ac5f0c26aef6ff1170e1485cde7744e17a9237c59457f1d5b0f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088c9d98910c38f13b1907a28647a9e78cc7ea821df93ab45af07ce2813dcab`  
		Last Modified: Thu, 11 Dec 2025 08:40:59 GMT  
		Size: 25.0 MB (24953834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de712ec543db6fd967330163900fe52edba74667819383a664b1c0aeb6d545ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332ec010d941d3e2aebc8a9c93e602555609f94ab581b12a60ff178b9b95643d`

```dockerfile
```

-	Layers:
	-	`sha256:e62f8fd460ec46fa5de2d42b43611fa8a0c55f25b81ac66a0e303cf419525383`  
		Last Modified: Thu, 11 Dec 2025 11:20:09 GMT  
		Size: 4.1 MB (4111384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:799b29e57395307f8cad88fbfa4b437a7677490e4636dbac0aa23a4099e530ec`  
		Last Modified: Thu, 11 Dec 2025 11:20:09 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:03d32b4f5e3f4f69261bfb129fe96a3cfc3a8b8d3e86f59199036e2af5d0e9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76132424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f11d4fa9734dc32bb99e19e6b172a19f65a99756275a1ef5def7dcc840bc01`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:78f6af9df8e55837379eae385038776d2a452e376e9108fb6a5a41d811da20b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1ef73ed5a2045e83189ff845bdf8a1453c38dd2b04ef566caa4e5a0252e5b6`

```dockerfile
```

-	Layers:
	-	`sha256:fe0625efe1384be6a242cdf42c8914f82f5605841e1a6fa17b0470e428b6ec04`  
		Last Modified: Tue, 09 Dec 2025 02:24:09 GMT  
		Size: 4.1 MB (4120284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17e1f87fd19e4973eefe777538f115109678d0cea8cff78dd6b8b5fc4d4bd0c`  
		Last Modified: Tue, 09 Dec 2025 02:24:10 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
