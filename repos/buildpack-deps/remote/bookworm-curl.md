## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:564d382283087968a92798708e25fd527fead26654e55e9d415f9797af45329a
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
$ docker pull buildpack-deps@sha256:6b0499c08572def03e11c6828fcacc21d5132b66b6c09fa53586d4c6b67396ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72526888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edca950e82d122aa7751208bc5bc2fbd558f6259924ef47fd3903ee5f394039f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc33f8c500d431774cac22572d65c047945f044e7d7b7ea16f83166c24dc1834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a874983bbaa014083921cfda21bb0d991c08788b342d06dda6947679b281192`

```dockerfile
```

-	Layers:
	-	`sha256:3d846f01748a47c73612bf5538fc2009704bdec71bad325e76540897e3b8431a`  
		Last Modified: Mon, 16 Mar 2026 22:37:08 GMT  
		Size: 4.5 MB (4514334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e063a39f4bf7ac35d6b86ae610bff04dc2044e18134164bbc418b51e731101`  
		Last Modified: Mon, 16 Mar 2026 22:37:08 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9beab4cefe56053e5c0237bd6284c22c30d27052e6077cddfcf84f26c2f4c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68735274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3a33cff20f7b53ef8182588859f0139ecb0c1e06d8d5eca32cf8fc6376a4b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:16:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7632810deba3af8046303a85fdb48062d8c548d9b9314414a3fbfef53996799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fb4ef9d66dee52a7fc069f04082e4d2e207f87756107834e4b034bf5a0a2b0`

```dockerfile
```

-	Layers:
	-	`sha256:3c99bbf20bd689c39f5c69982dc514c03546a517552d481d62a5ae8e04897f2c`  
		Last Modified: Mon, 16 Mar 2026 23:16:32 GMT  
		Size: 4.5 MB (4518150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5574d56ec6f50fff95c7fa7135d30f05ef3b32922b83d7d2394ea4c5e765fbe`  
		Last Modified: Mon, 16 Mar 2026 23:16:32 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9d18ad1869c3c26e8711b61b7b527edbf55887e5d952c22577169ddf69d9adac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66149624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b34607edd09aa4200517ae920f7f54a5d1f21cb646a99dea29cb1ec2fe96d97`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9253b0e0001be88b853635fb56e583b098d5f023d069cdd2d43ed6330b6929d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354a8cadab8812af7ade4f7254f13dd131c56ded66f19a5e00585e19b56c7563`

```dockerfile
```

-	Layers:
	-	`sha256:e19d236b1c00e4de303103a50b3f46475582a833c5b7dec0410e9b4247b4dc29`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 4.5 MB (4516623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ec181984be2dd8837622c894bf8e9c447e5a785724399a42f94d4c15751f79`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9eafa40700ce9b3cf4d33c73a2a89f1247704130524041732e43c3c6d8cc2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71977733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9101edd0b8a43da601ba351cdd655fdb2a3bf6f2b833c10a2f65ef6c409402c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:73b2d4620d9bd3936f6c5302c64bfd88ed9c096943e49c7d67c20517b27eafbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db007cc2a4d4516129a71cecc80b38210a5a3b2a4f1f650376464b5ef185037a`

```dockerfile
```

-	Layers:
	-	`sha256:d89b7baf73989bfe18a90e02e920b0024c7d10a9147b84f4a25a9dc5a14a1630`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 4.5 MB (4514595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc5ef16a62f2c52b42e8dd3f191b84f100151bbceb8c3759f99c2b71f8c9f3fa`  
		Last Modified: Mon, 16 Mar 2026 22:39:27 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a6788b3576e9f5cc76e8eff73fceb4000a55c4e35ca573de0365c3cf33aa6097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74349648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d427b0d5eff0926e48aee13a27d4a8541697f960b96ab6a49f3627572b620a83`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e9edaa547320d994252bc3aeb50f777e7bcdcd17bbb5ab746a6f3ab5b84fb2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31bbe8813a192cf2a6b9967a0453a501c2b74c9c867640c98c837d3c4088a3f`

```dockerfile
```

-	Layers:
	-	`sha256:18fe30783ca6374adea6ec7ac24bf78796469317b697e4f3d9dd1fd40d23466c`  
		Last Modified: Mon, 16 Mar 2026 22:43:52 GMT  
		Size: 4.5 MB (4511453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a9cec2c57028a887b553d36240aed492de78a0e1a9d00ceaef0c1968dd49d3`  
		Last Modified: Mon, 16 Mar 2026 22:43:52 GMT  
		Size: 6.8 KB (6794 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2fcfdd55b67414f47c6e2828bd34f58db36e03dd1c5429da07095f9c7e954743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72397825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700b08f303388efb3f58605e5549202d0e94ee371b37fd109d5c9ae78ba10ba5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 06:07:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6ec71ee94fb878725e70f6a21c20349985b89066361ee1f753b3854cfa2c839a`  
		Last Modified: Tue, 24 Feb 2026 18:41:37 GMT  
		Size: 48.8 MB (48782510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2283ea3597dab73b85bc0ebe9635f3297b9d6d4b8ff5df7913003859ba369`  
		Last Modified: Wed, 25 Feb 2026 06:07:50 GMT  
		Size: 23.6 MB (23615315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de26e783cd42b9c1ed6ad0b28c0216acc2531f0996f8a8e1c3ecf8964593a17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995032aabe93554570504956c6220a25154e8ac10791100e0a0b200e95a40148`

```dockerfile
```

-	Layers:
	-	`sha256:4539e0770e01b48655f4fdb2f40e1a425ab55e0a01ca8332ab0378429b4958d0`  
		Last Modified: Wed, 25 Feb 2026 06:07:48 GMT  
		Size: 6.6 KB (6649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d92309f39a71b1f2b7a2854ff15bbddb2aa99613fe884af58eb14873d29b19b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78008274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adb03bb1fa315f6e5a3ba40687f630c3a16c1ef2178ae8ce0e6d9889fd9047f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c93b562a2c36911d83922a6588d2108eaaeecbecba958a685dcd85098f20981a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024a148a0bab1d82df93c31df2f9024b4864fa19588c406959a10a2b26e8d6e6`

```dockerfile
```

-	Layers:
	-	`sha256:e700615bddb8b504402806dc302b96d038427bfe6f9b0953829b2490bfcb2396`  
		Last Modified: Tue, 17 Mar 2026 01:49:00 GMT  
		Size: 4.5 MB (4518960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c2b9e7546995700bd8b6a2cf0552b3c09d00391c7390d3e017d02958a31210`  
		Last Modified: Tue, 17 Mar 2026 01:48:59 GMT  
		Size: 6.8 KB (6848 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b206bedbf1f60f7f8da0383f43bfa1cb7c32eb60e1029bd85efc4bf871acc1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71181533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcf700ecf4c5ae2fb17c3ecbdd193267095bec0c9ed4bd9c4976cc4c313e05c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:40de86fab2c129c7cb30def55aee47be72f4e049b978fe542932862c5a6dbee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538d1637f7283373351f89cf4cd73f8133663e5955528dc69ee468977b47bff`

```dockerfile
```

-	Layers:
	-	`sha256:a5535ab1e93be84fcfa46a31f549e7c0715f077bb45c753babc09f501fa20bcb`  
		Last Modified: Mon, 16 Mar 2026 23:44:28 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de8284b95036920a9b978111621374ad5076f626f90f6f4ce6422e0b82adabc`  
		Last Modified: Mon, 16 Mar 2026 23:44:28 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
