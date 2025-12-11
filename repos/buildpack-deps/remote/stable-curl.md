## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:b3047b2fb059d4330e7e33f105bec95ad68af4c292c7e9168465719fcc8f9b2f
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
$ docker pull buildpack-deps@sha256:daca426f69aac2b126c035038d8789875c7d275b9387f15c72191c58e4dcdce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74903383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8461698e8d7218ac2020cdbccdb3965ccfaeb9486faabc3773a208da17806c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b7d40617cbd130291739190ad8e587027686694abef9cd230d578860feebc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fbff666bbdb94e5553b758cfea2132833b6a13c3c6a93e21b42f3b0a0d7725`

```dockerfile
```

-	Layers:
	-	`sha256:b683ec11d7e53fb3158b35632694cd235290a3d9ba221d6c1489e5cf0d5dd3c3`  
		Last Modified: Tue, 09 Dec 2025 02:21:33 GMT  
		Size: 4.1 MB (4118874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55278b57a1d9a167e9da0ebb906b9fc204cf5b70f8e71ce53b7a23ad718a01dd`  
		Last Modified: Tue, 09 Dec 2025 02:21:34 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ef927d27dbdd4f28986dbab7424a52dff5fce22c200e55008dac3930a14fa036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71794648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f4066ad71da5ba244b67d70b35c55fb8a6e25682ec835418b51abe9f4f92a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:123c232a33b986aeccb984e885244b48200c4eb4f9a811e3df109a416dc71f80`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 47.4 MB (47448721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaeb213e9fa41da55c6b895ce8273281464b3351c9fcf26aed8d0fc7484a18`  
		Last Modified: Mon, 08 Dec 2025 23:55:26 GMT  
		Size: 24.3 MB (24345927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd7bed8ac046d3272df081eb5c4b6b12a86ca3c0d2fa5d7fc4f0c753a897cb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fe07077ba004edff56cd2f66fd4483816c90578d8db072c25d8ecbce71e1e6`

```dockerfile
```

-	Layers:
	-	`sha256:840a856ad5eb897f4afe7b5b26274c920acfece9d28a5af48676135d5bca4598`  
		Last Modified: Tue, 09 Dec 2025 02:21:39 GMT  
		Size: 4.1 MB (4121864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e322f6dd2fbdc4858972a084d4a0fb2127b2ea005af7e4d41b1e0a1ad60294b0`  
		Last Modified: Tue, 09 Dec 2025 02:21:40 GMT  
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
$ docker pull buildpack-deps@sha256:37881ea294c5da39c55322eb7a3f03743cdd83a8ea527a38a829bde199c7314b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74671167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4cf2ad670718c6b942e2b72b69279744b9d63533fd1d6e2597c9368048f7dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a92ffcc8ce81c2f400e1b24efe1a84079f2c9a7bac54fc5639aa96340f8e4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883ef5fbd17403dca0667b09c73b0aa0eace3406e3162208e90723f72f5bbb48`

```dockerfile
```

-	Layers:
	-	`sha256:b67937de0ce5fd8b7631fcbf1ef7f0b6865f2320a55de163a9f3ab7aceaca422`  
		Last Modified: Tue, 09 Dec 2025 02:21:50 GMT  
		Size: 4.1 MB (4120416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1a2c8d07a23f632b45c7a6aa4167acad7872e4dac6a342c9ffab5e3a8cb46b`  
		Last Modified: Tue, 09 Dec 2025 02:21:51 GMT  
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
