## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:3608f2b7989e23e43ffe8636d93563f0f9266bbc46ebd56eb18168943f59391f
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

### `buildpack-deps:oldstable-curl` - linux; amd64

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4ab5eba144ea54e77571f7d080302ccdc744a7f5c7ffee354ffc4c7adbc1c8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66149902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9f06ffa497387bf1dcab1c72c50f499d8d8ec2f712918ab275b3c6bc698bf2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:857c29e6e25157da9322295da0f306ed0d3531bd12ddb3f2e57f4826c9d5c729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4523504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b3c70966c3316b859e1639ed3201218d13a32d6dcd912b798cb7930bc2c786`

```dockerfile
```

-	Layers:
	-	`sha256:93539304e38b96318810af2fe070aeb1dfc29179bcb9b1959d5ed804914b4855`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 4.5 MB (4516623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b74d3dc4c9de2102f57145cc92d8008e0ef17694ec6539c21c8df2c8cb3d112`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; 386

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; mips64le

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:557c9f46bbfc6f0258650a1dca3b323df0f8e9bab93b33ef77953d73c93e054d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78008196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b49131f5be8ff191f78767e6b19e9395dad7ea58ca70178bef67b635c40bd1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba53e63c4e3e4d88f0425bc79a37e364db9aabbff9c13ece5cecc63ec880f3`  
		Last Modified: Tue, 24 Feb 2026 21:19:17 GMT  
		Size: 25.7 MB (25671399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:26261ecfcaaab37318d05c9c71d3ccadbfa43df87999878b6edb84c4ff2c522a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6044ad4178486cc65cc99c3c58f4ceeea234beb82bac141f1529e3831041e4`

```dockerfile
```

-	Layers:
	-	`sha256:53c721ad3c72bdc25e4ac454b8c047ce4980a0f0333e80344fd8bbe98546662f`  
		Last Modified: Tue, 24 Feb 2026 21:19:17 GMT  
		Size: 4.5 MB (4518960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f606e5023f90a3dc560298d89905e29054b27bf29923076c083627b33b90379d`  
		Last Modified: Tue, 24 Feb 2026 21:19:16 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2786dd900ac737af64b29b0a0ded45c92d24163ced2a5511846b86edf6d672ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71181961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb415b89047d95e18ed4647c6844abc5fb59fac43fa40d9930846cac52c2be76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:56:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1490eda04f0dc8144e02f684cac28c2862b3a584dd3e8ad7e22b96b35409c89`  
		Last Modified: Tue, 24 Feb 2026 20:56:37 GMT  
		Size: 24.0 MB (24033874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5a7e521c94b254e246ec1a4f1f50308ffd42a7976c3eb25de6c6b4318780b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b443c83bd63911336cf8aba3251ad7740677269197a9abb8589d2cba904d8115`

```dockerfile
```

-	Layers:
	-	`sha256:8731012872d0007add5e4b16492d3b4d06a71a97b22177ad0bcbae321440536b`  
		Last Modified: Tue, 24 Feb 2026 20:56:36 GMT  
		Size: 4.5 MB (4511138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cd8d36777eb75f6d2e81e58b64960764d2f7f3928c4e695a57c2ba974324f02`  
		Last Modified: Tue, 24 Feb 2026 20:56:36 GMT  
		Size: 6.8 KB (6817 bytes)  
		MIME: application/vnd.in-toto+json
