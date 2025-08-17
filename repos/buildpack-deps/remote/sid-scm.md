## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:07f43467ac6c593a3ae9ea6cb056d830f7157472d48a6b03edb09b42fa921a6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:29ad3aed8764e0f27c3664e9a11701d228ba50bbe2d8e24723f37c264cb80a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143140842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120d32a1461ad10036ac3ed5dfdafc21205d2e995dd08e54ad5703f4bab08d46`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:91617643e569834fa54ae3c641bfe51cb7c336b5d4c84459fe06ad34797a9b56`  
		Last Modified: Tue, 12 Aug 2025 20:45:04 GMT  
		Size: 49.3 MB (49311006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6147febc7eaaf987437ba1cec086fc417009e9ea749cf4a8e05425f6ae2ecd`  
		Last Modified: Tue, 12 Aug 2025 21:22:06 GMT  
		Size: 25.7 MB (25671763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5764333da2b14e2853ea365c029697a9b2d16d890203808413dd3e27a98c7bc`  
		Last Modified: Tue, 12 Aug 2025 22:15:01 GMT  
		Size: 68.2 MB (68158073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:731e445e52f5ef3c3b83592c4edb0368718de4cab71e317f30cf94984552500b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7786438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559468fe76405cc7956d7824870bec2f46890078d2c034ca8fbe65f21a893541`

```dockerfile
```

-	Layers:
	-	`sha256:57d7a8112d6acfd08def6a64fc2f745a997ea52babffc39142d4e49c0c8fe2bf`  
		Last Modified: Wed, 13 Aug 2025 01:22:26 GMT  
		Size: 7.8 MB (7779141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc788b02913e7d73cea0c7aad981313ab5cb8d0177d8e564490ac443e933b25b`  
		Last Modified: Wed, 13 Aug 2025 01:22:27 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:83ed8a889ed5dd97eaf91414ea42983cac7253154ae097fc9d298271c45bdb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137664797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bdd4aace181626f4e29bc1459053858873b10b722bb1d571ff2c6c71416a5a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5748e2c98ab94a513cbe6704d8aa158304698c52babb6c14538afdc0d2da4d79`  
		Last Modified: Tue, 12 Aug 2025 20:46:52 GMT  
		Size: 47.5 MB (47481153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8674f20f211a0a5df7e43fa4413500efffe4f69e9a5f53119c86c35ab3bfc85a`  
		Last Modified: Wed, 13 Aug 2025 00:00:46 GMT  
		Size: 24.4 MB (24409281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd16b6b97e2e3cd2021a0bcd7f18a25ab7c75e9e2a4a58e680359594cf2f951`  
		Last Modified: Wed, 13 Aug 2025 06:09:26 GMT  
		Size: 65.8 MB (65774363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:68fca14746ab13efe9651236f1367f778196e7ace1514d6d3318ac88444e0377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7787544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57414f0edb06da79ca97439ebe37181a49f39767e746a84772e48e70f8715969`

```dockerfile
```

-	Layers:
	-	`sha256:8f8c5577e5977899fa174d8d2e0a3b12297601b375c681c3bad99edbbf27b697`  
		Last Modified: Wed, 13 Aug 2025 07:21:19 GMT  
		Size: 7.8 MB (7780188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e04e05a5e797f8329738409df8c18c2b098c804160af427eedbf33bffb841d`  
		Last Modified: Wed, 13 Aug 2025 07:21:20 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e651680e656be523e2efc72d8de15fa0850c8840f702c5f3c5c318e90c88c7c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132607352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca868268ddcabe68063e50bd1c3f2f1f2ac93955c77b24aeece4f64638183f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51c05ed00e703a3cf5143ee59e5e4f274a1b80aa10078d7b24eafce226544dde`  
		Last Modified: Tue, 12 Aug 2025 20:49:45 GMT  
		Size: 45.7 MB (45743292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f4c6e871209c22d9147d58afa57aceed37d2c4246961ef6f33220a727e664c`  
		Last Modified: Wed, 13 Aug 2025 00:16:33 GMT  
		Size: 23.7 MB (23682193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31604b828c3328f78e4b41c62e665eed8e937b5c601513032185e28df4cf0ac8`  
		Last Modified: Wed, 13 Aug 2025 06:49:23 GMT  
		Size: 63.2 MB (63181867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dba0c9b0196f3e5fac20ab6deb9cbc9b997225a5330081f818a2ab50fffc7877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7786997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066c7847f4ec97398aba69ebd14630cfd18e45bf00d95cd67bf817d68a474bd0`

```dockerfile
```

-	Layers:
	-	`sha256:81e86b6723dedde56fcd48d31cb183f1dff83edc57d40c4b3d088cc72a759139`  
		Last Modified: Wed, 13 Aug 2025 07:21:26 GMT  
		Size: 7.8 MB (7779640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945f5e0f06c9c6986415f123ada0ecb2ce15136afda4b9a238494d2e07d2afb4`  
		Last Modified: Wed, 13 Aug 2025 07:21:27 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ede8a202f31198ac102f95cc671bc9a4fd3819d20a6dbb764dd9aa0e3fb2f4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142760468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba6c2ee379f512c56fc35ad832749b5f194f6a7addf873834574919cb0c28c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:406c75c505cd140952825ea55560dd596c3ac81bd28e8acd75409de77c63efed`  
		Last Modified: Tue, 12 Aug 2025 22:10:46 GMT  
		Size: 49.7 MB (49665758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42948f27bd259c3af4df8bb9642f9b13a961850fc18b0d0d704e4d8bd4184ce`  
		Last Modified: Wed, 13 Aug 2025 06:44:51 GMT  
		Size: 25.1 MB (25094159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37825ed6d653aa51fd40eb5d018e0ac28bfaaa55f25ee15e26fde25f0d23f94a`  
		Last Modified: Wed, 13 Aug 2025 21:41:14 GMT  
		Size: 68.0 MB (68000551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ae7d8521478e3225a63113a7e238ab8312a982047c1bdc9d45b69fee13e6b219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7794181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6616168dd65137522762f7fca7a85798d78e8ddd664191416758a702cebdbd8`

```dockerfile
```

-	Layers:
	-	`sha256:74f5946e90cb6eda5dfba054faac94db3a9f833e512a5debddb8a12704ce3e3e`  
		Last Modified: Wed, 13 Aug 2025 16:21:17 GMT  
		Size: 7.8 MB (7786804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6e01baf245e20a9b65fdce778b5b7aed93e61e0ea01f1bd59e5a4de6dc52ef`  
		Last Modified: Wed, 13 Aug 2025 16:21:18 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6c8813808963345904fd23720f91c930e20d8ef081d5c631a5089cfbd8c3f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147894251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88972b816d61ef1a7e039c5e1ceccceff5824d3c151f1a026aaafc963a2aa250`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b72ff759cae89a47c9827cbc3981a075f421742ace3eaf0d3c40f8d242d2eda8`  
		Last Modified: Tue, 12 Aug 2025 20:45:13 GMT  
		Size: 50.8 MB (50819082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3bb2ee090cfdfaa39c0d6ccc1bcda36a80f4080c6cc16e7b75c64cf990c8bf`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26837373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaaaf9e7098421af8e154d4b4462b5597c12f7d1e78455cd1a1c8a16f9966d1`  
		Last Modified: Tue, 12 Aug 2025 22:15:00 GMT  
		Size: 70.2 MB (70237796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:50cf42790d22b3133d3ee77f275f5ce62520df8a29df4458ad079e40277bf89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359f732ee994b168ceb7617f22db2b9e935e044a9e8a72ca63c97537868b15ec`

```dockerfile
```

-	Layers:
	-	`sha256:8ef495719dd38af39f0869587460c3dd981b5631cd5e327f3ce33b6dc679d0b9`  
		Last Modified: Wed, 13 Aug 2025 01:22:54 GMT  
		Size: 7.8 MB (7775288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5dabc94496a63637754077d7cb9c9554698f8f85262d12da1f889ed3f25979`  
		Last Modified: Wed, 13 Aug 2025 01:22:55 GMT  
		Size: 7.3 KB (7274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:57920e30e8e2a49e5614db78f182561763b0aa965b8cdfebaeeee2c2f0ffa34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145284256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d046964e84cc8b77c6ec59123a044bcaaa855d6a891f23fcbba44ac2157717`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5da413a3f50eb44f07bba0eecd786bf3efd93a4ca4c52ba8109a9b9ba14e688b`  
		Last Modified: Tue, 12 Aug 2025 21:13:15 GMT  
		Size: 49.6 MB (49562283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d257b869b2a60078b7a65964ab94a9b367c5ab49593e2c17c1f7845cf6eb2`  
		Last Modified: Wed, 13 Aug 2025 06:40:49 GMT  
		Size: 28.5 MB (28535525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86fe6006038239df0ed2d48c27073d2bc03b5547e42ef3e28ba6ae24c42e7f`  
		Last Modified: Wed, 13 Aug 2025 19:22:34 GMT  
		Size: 67.2 MB (67186448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ce64799ddb2db2a8ab4c5c16618193be88e29cebedea7c1369482dae9dc7030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6451494ede8156481ae8b4dc7bc9e9ec7792ba0809daa55f2117f83ac8873dc0`

```dockerfile
```

-	Layers:
	-	`sha256:258b8e74cd89877502fa2c82355303b369e97095ef8f0afe8ae2f0b2e1bcd14f`  
		Last Modified: Wed, 13 Aug 2025 19:20:59 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3ef7ec47659e0026d73e81028a2a84898cb822913df884b2041701b19b203e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153724344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f51005a38b0516dd464221116f8a63756e873727a7498678d04c43f46cb74e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ae7a451fcc7e9bebf7ef51b031f5ec2600e7c017efb66e1de76397538aff917`  
		Last Modified: Tue, 12 Aug 2025 23:09:05 GMT  
		Size: 53.1 MB (53147748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48ea27c6408465e04631c45f46084191d49262124cafc6550f5e911abd6374`  
		Last Modified: Wed, 13 Aug 2025 12:14:50 GMT  
		Size: 27.1 MB (27069254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca3385b479d65092a57bf9f294af41066b99dc31de27938a478b8d7dae4e82e`  
		Last Modified: Wed, 13 Aug 2025 21:22:30 GMT  
		Size: 73.5 MB (73507342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5fd5509dfba0fd4238f908b06f6b2001c0c87581e342b75d01beb79574934742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7793573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b4b0692f1da572640c2b3e5c7a01927c4af78b5cb8aac0c8b3983132acf882`

```dockerfile
```

-	Layers:
	-	`sha256:c0074d81b89cce6ba88a03eff5ea43547dae8bf4313966161b172e4d6f96f3fd`  
		Last Modified: Wed, 13 Aug 2025 22:21:46 GMT  
		Size: 7.8 MB (7786244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adb3071410bd40a9d534a82119f5afe987e2813e44ab56d324f173858b9e579f`  
		Last Modified: Wed, 13 Aug 2025 22:21:47 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9a984e3065d82cd534a7df44d5c55f68055509c51c3dbc901e27263b6effa08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139941891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fa80fa3b0ceed85fdbb84e2b85349b6bb6170291b2f5f4a2b8de5ecb59ab75`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a9e91ea2edc2d111f6a67eba934b0ebded0b74c51de6a807b73d07cbf965e132`  
		Last Modified: Wed, 13 Aug 2025 01:03:20 GMT  
		Size: 47.8 MB (47776559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64af9f489cd1777e5b300ee5ecaa1ee0eb257910fbeea3b4885aa18546f4677f`  
		Last Modified: Thu, 14 Aug 2025 14:45:40 GMT  
		Size: 25.0 MB (25043691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ca0dbc65f78a497c831d706ac3403d38aa6f98f2a4e700c685ca0e3cd72cd3`  
		Last Modified: Sun, 17 Aug 2025 07:42:58 GMT  
		Size: 67.1 MB (67121641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb9940a110035883ae07b786aa7d37fd2ca69184d9198b029abaa1236572c19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2209a09910b21f2d95c9cb3acb799305eabb2a800e94c8b45c5a5fdbed22c21e`

```dockerfile
```

-	Layers:
	-	`sha256:e0db5cee89cd9e0e4d0931dc4c4a69eb258c3e8177a88dcd08b144b079617d45`  
		Last Modified: Sun, 17 Aug 2025 10:20:50 GMT  
		Size: 7.8 MB (7768899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3635fce3bc436748988d18d58000aaf8b56a04bc69d639690367bfe9dd858bc`  
		Last Modified: Sun, 17 Aug 2025 10:20:51 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:762573ee2199b531686099bcfa928fdcd68e19141f895e98be16698bd4954cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148392538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c35b9e9058fccf18ede60a1fce97107f5500f47d7708d02394663241686cc3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4959d43b6e4e3bb883ad4324fbf3d2d46fc88486af520d990c753fc3a7ba0062`  
		Last Modified: Tue, 12 Aug 2025 20:56:23 GMT  
		Size: 49.4 MB (49380676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9f068820d21f743fb7a4899ffdac4cbb3c9018377c7ccd9ea60dfaa661d90`  
		Last Modified: Wed, 13 Aug 2025 11:02:14 GMT  
		Size: 30.0 MB (29993315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c726bc62e5513d157547977196ac5e96f4f6b0c75bcf55735caaa59100d378`  
		Last Modified: Wed, 13 Aug 2025 15:08:18 GMT  
		Size: 69.0 MB (69018547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:291b162545c0f204f9cc850c4750519210e2dc2b8daede0fe85536562932db41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7787351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddab23f277d94370377fd0690aef9fe4cd943cdc3bbfab427e9e834f275d842f`

```dockerfile
```

-	Layers:
	-	`sha256:470b1a787c2e551eca878357179c51809b90478054d80ee4980843767e561244`  
		Last Modified: Wed, 13 Aug 2025 16:21:43 GMT  
		Size: 7.8 MB (7780054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ceb38ab6ad008b63dd8035967cbc3bedd647868bd0c7b0b613ea085431600d`  
		Last Modified: Wed, 13 Aug 2025 16:21:44 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
