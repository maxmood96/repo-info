## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:8b3561998921cc7d9a3f6e476a49d8bf1ef421d78d96c05472c27694a3a30007
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:859579ef13b6a96d0fefccdf9bc0cce61e4810f6b151ce48969e65f89a415af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136922409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc35c93d8411c380d401d12872ba62b1931f1f55cf6efaa6611c7372b1c93a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:50c8952a20c5857ca1ca0f986f19c5d26579fe5c3b33a300ac341730c9ab45c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63681d0ef513defdf13c112062e8f1aef27c25c12c09790bbb2938d38b214d6f`

```dockerfile
```

-	Layers:
	-	`sha256:6a2a93997c8e5ff2ae66d480d29309291e8aeaf5dc9efd06e330725cc321fcf9`  
		Last Modified: Mon, 16 Mar 2026 23:25:03 GMT  
		Size: 8.0 MB (7966048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2e850b1439101cabbda47c5cdf933f5535681472a4b4849a4cc5b9e3f32599`  
		Last Modified: Mon, 16 Mar 2026 23:25:03 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:263049f5a0d2148d4f422921ea2f7dd7d6c80a82a39a577cbc3afe0b7abbe02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130744100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8478103f6e124c83c70123916a5405c92f97cfc5038829b33d5f98d56f9f900`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:16:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a889e82787049133d77ffad9b735ec4a592f071dd0e1873ff586ba91994e03fb`  
		Last Modified: Mon, 16 Mar 2026 21:51:55 GMT  
		Size: 46.0 MB (46021486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a2ee884acc42f13388cd68befd38ba7c8e48ff32ebffc04bc5ff13735cd047`  
		Last Modified: Mon, 16 Mar 2026 23:16:33 GMT  
		Size: 22.7 MB (22713788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a7ffdc9dcaed1952881119614bd002f2a5fee9ea4f873345f94e374aee1d1`  
		Last Modified: Tue, 17 Mar 2026 01:08:47 GMT  
		Size: 62.0 MB (62008826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:46fa77fe4410c4d08ef6f3af7d2874463b9878c5552149bbd31c0308ec2ab45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74eb7b379a436e4498d37401e197eec638f1fbd7503f1364bdb78d3b36c2fc71`

```dockerfile
```

-	Layers:
	-	`sha256:f1a2f2f125330bad69b48b72a9caf10c751914ef763e7cf26bf8959f61a359ed`  
		Last Modified: Tue, 17 Mar 2026 01:08:46 GMT  
		Size: 8.0 MB (7967906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:186e4665285fd4fb9b8b9db610dff474af50f4c9ac350ef832ed1906206f58a4`  
		Last Modified: Tue, 17 Mar 2026 01:08:45 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:92a73126be0cfcf542dcafc091a587a0ab71c9e88c6208c14cbe255c7ad3460b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125801712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e6d56d31dba610842a41a5bcd6d9e4e310c6b9de06bd6be408b0ecaaca7e54`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:51:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c259f98025fcc3d44333815b426fe9bea34608d38b537248297aff1482d389`  
		Last Modified: Tue, 17 Mar 2026 00:51:25 GMT  
		Size: 59.7 MB (59652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0cef628244786b17cf74aa7df771a3788f9e9170b4524a1edeb76623168f6bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73470fe3a7589c8241ddd6349b1b2215bc122d9e0a726ad2cddafdf5b79ddea7`

```dockerfile
```

-	Layers:
	-	`sha256:025907233f771b65bc642c450b8616b71322aaf667600375bf82f7954d5116a3`  
		Last Modified: Tue, 17 Mar 2026 00:51:24 GMT  
		Size: 8.0 MB (7967325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53780ab5cddf07ec72256fcb5972e9dde1f23eea1d99e01fff22df3ef8b91574`  
		Last Modified: Tue, 17 Mar 2026 00:51:24 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:419f058e71d03bfb7b29c7a5ab5a7beaf268aa60d9d813dd6c2e8a921f8c1f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136457175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad9fc538861fc686e6cdb00b1838d9fa63e0a99ce5757d9e0ef2f6ba82a9916`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c333bbb6bf6e347ec8d4e794e68112109389dc6cf98da06cb590c3d27c9d07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca95454a39d6567aa1a798feed487214a2296496be965ed2ec7d305e4f9366e`

```dockerfile
```

-	Layers:
	-	`sha256:77aa5d8f2886bc25c79e2eabce23bd1d0cc31aae1df01ca9ce265c6376e93953`  
		Last Modified: Mon, 16 Mar 2026 23:30:20 GMT  
		Size: 8.0 MB (7972441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f37c10aebe7f0702506435ad7f9c05b0fbf3a4bf7cb0ee6bdd0cc5184786b05e`  
		Last Modified: Mon, 16 Mar 2026 23:30:19 GMT  
		Size: 7.4 KB (7390 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a340d1c8eefae74f115e54e02ddcf8040b697f613ca00ae17d29fa2a3e80a302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140583953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0c09d4383dfdbf138730d6caffd2d36b6147aa7dbbc0cc2daa4fc2520e8bd9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:41:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7cf39578e27046e7ba7fa5d4d45df198790a004a9eb86583e977b3b055c88`  
		Last Modified: Mon, 16 Mar 2026 22:43:53 GMT  
		Size: 24.9 MB (24871994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9d2da3801adad27eefa73bb7b5ab6c0c94f46583823a923caa8e9b995a97b`  
		Last Modified: Mon, 16 Mar 2026 23:41:39 GMT  
		Size: 66.2 MB (66234305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c015caf18306ada5f706ccd4cae1b84e82c92670e7ca637364dc240f096d84d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66943aff6d80c4e4320583ddddfb39d3c83211cb386fa2590557709ee0ff698c`

```dockerfile
```

-	Layers:
	-	`sha256:b6ff5d1fc78c39b283ceb166a66eb8da3a3e7ebe9b9b07593053cc0be452c3e4`  
		Last Modified: Mon, 16 Mar 2026 23:41:37 GMT  
		Size: 8.0 MB (7962206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7600be157ff39e83fa479bce6d82e223273632a0baef833a2eeb2bafe789717b`  
		Last Modified: Mon, 16 Mar 2026 23:41:37 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8242e5f88cf12019c84731425495b8bf67a0c28499ee18026162c79834d0d85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135707598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12806cd449482851c416b19b2202bc56a8bdb0162e27a5284ce817b9eee6fe83`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 09:32:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 15:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:55bd01c42402ce77937fae9abfba9b351fd4b3fab7f1f58eccf5b2fcf0ac8978`  
		Last Modified: Mon, 16 Mar 2026 21:51:11 GMT  
		Size: 48.8 MB (48782288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a46874b19723e755d13ba2292477f479fd221937f5480b97990afd32f94b3d6`  
		Last Modified: Tue, 17 Mar 2026 09:32:54 GMT  
		Size: 23.6 MB (23615153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510757183cb1996fa93fc6110a5644d68f4a47cbb4c8f08c9a7376b57b6600e1`  
		Last Modified: Tue, 17 Mar 2026 15:10:46 GMT  
		Size: 63.3 MB (63310157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bbf79f59b3dd31266a8876fe21634e7487cf7e4b08f047a4561255c65bcc4f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b9618533f00e2b4661c2b37e387740ca639c5a019735a2b4aaf454d7c341f2`

```dockerfile
```

-	Layers:
	-	`sha256:0f356c461d423df37fcd9e1cd6b67069fb806fd113d981e9533d1c824d2ee9d0`  
		Last Modified: Tue, 17 Mar 2026 15:10:40 GMT  
		Size: 7.1 KB (7143 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cad95f297e923be18db15f573f655c42a3607feeefb4eb4dfe8b483f552ed50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147854425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b028098dcd9f217ec6828ab72797ccd75a68ff74751d80f6b8d3cc27c098caa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 06:03:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6053003aae760c21f129e32066714b891ab6bc6ec6abdf0f13ff20cb85ede`  
		Last Modified: Tue, 17 Mar 2026 01:49:00 GMT  
		Size: 25.7 MB (25671576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc763fa93abbd05d9932abad5e62ea754d4d526450c9517c9e5b75b5c914969`  
		Last Modified: Tue, 17 Mar 2026 06:04:00 GMT  
		Size: 69.8 MB (69846151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db9875dc6a0e1a07e50c354d76ca74e45888fc979393affb8cae4487fc00ec42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f37874d8a2b18ac487eb05ca5f6ffd3426e5ecc61a8472d41ca866bc3c98ce`

```dockerfile
```

-	Layers:
	-	`sha256:608668b5d0e60818f915854cb3839cf7eb0e9044a0f80a3ba854412598f0bf18`  
		Last Modified: Tue, 17 Mar 2026 06:03:58 GMT  
		Size: 8.0 MB (7973921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d06ce3090cb58922d31a9ccb258a8e6cdd84e84c480ec37b66fde514cc59af`  
		Last Modified: Tue, 17 Mar 2026 06:03:58 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ecf1551ffdcc523ba243fb96fc4f4de903689d0f66fcaa220c48723212b00467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134682999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77e1c702def42a8942bd8c7c92125ae3e044284471b8f2e1e857afca8918831`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d904b886f0656b8d9f7b2cc64089c6c03aa31b22b97fbf96b0bc6c4e3726e429`  
		Last Modified: Mon, 16 Mar 2026 23:44:29 GMT  
		Size: 24.0 MB (24033614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3244a56b42252330a5ec4502181ecac45b16d96de3113430b375f7d10e72bde6`  
		Last Modified: Tue, 17 Mar 2026 01:33:52 GMT  
		Size: 63.5 MB (63501466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e857a55f9adfbbb915eae3963cba2d595d14e80dd926c5958fae070c2fa61dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72adbc9928f94488b621822a781bfd546196a7c08fba43333bceb631ccbc9cd2`

```dockerfile
```

-	Layers:
	-	`sha256:c6a41abe9d503f464c8e4c7e40f10f14868c38b400abb3901ca0e27dd5290af9`  
		Last Modified: Tue, 17 Mar 2026 01:33:51 GMT  
		Size: 8.0 MB (7962361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39739033bca49cd85e427a762e44ff83ffdefa1eadf2711745af746f82537fd3`  
		Last Modified: Tue, 17 Mar 2026 01:33:51 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
