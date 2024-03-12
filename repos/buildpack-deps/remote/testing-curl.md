## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:353427e1953f3f736b62d0b255c6f40743e8181edff733a00af35ebac8acaf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bf7c5e7df1344c29825cecf0b13a48e3542d9076344bb488f886f9dfce534e05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76521533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab18b0139243de95245640eb86079cfec9ad31042c78135b8277e778e58b183`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:23:42 GMT
ADD file:93e647bfd891e82156d7a13e0f0b194003855008967ec51e962ea0d70fc59ff6 in / 
# Tue, 12 Mar 2024 01:23:43 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:59:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6fbaa46799c378c8b00a06cb5a2319bdd5ab7abe194cd97bbc9aec2daf476e9c`  
		Last Modified: Tue, 12 Mar 2024 01:29:57 GMT  
		Size: 52.4 MB (52360823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1767d006c9347102620ba4282bc383135a85f2d494cc82af4568dbaa79a48972`  
		Last Modified: Tue, 12 Mar 2024 06:08:15 GMT  
		Size: 24.2 MB (24160710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fd0a14ae856254c098859eec38bafaf87e9474e0d817958dc4b89726aa5aa0fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72458820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717c04e5eab3c7c08ebdbcddf4383b81f31a07eb15d7c81d1d2370a21b5aa91c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:49:56 GMT
ADD file:3e60918b2fc6eb291458158f2b94b782320f758effe373fd6d0a5c58dd3e2319 in / 
# Tue, 12 Mar 2024 00:49:56 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d768e5bf180c947f8692477b575df3498b64f65e904bac933d0260cd957c8aa`  
		Last Modified: Tue, 12 Mar 2024 00:55:26 GMT  
		Size: 49.4 MB (49418029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb2336dddcb338dd0f592faca75df5ec1dcd20bf4a99dac4ce09223036087fc`  
		Last Modified: Tue, 12 Mar 2024 01:45:26 GMT  
		Size: 23.0 MB (23040791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dc80403c991f09bb5bfe602ed086e1baabb2e0d82f85668dca99ea4e166f2187
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69273994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc3fadc2c9f0f321da6f8c5f8c7cd37b5a05bf21eb9a8b5d657b2bc02af01c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:01:42 GMT
ADD file:653b30d78a37c262fc23750e2a51b4c22f86c5a03a005268cedcb42011759039 in / 
# Tue, 12 Mar 2024 01:01:45 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:15:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84940e63db1cf18d5cf1aa5d0b2d913f1cfeaf6d1392975ee4542b2b21627246`  
		Last Modified: Tue, 12 Mar 2024 01:08:19 GMT  
		Size: 46.9 MB (46919137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f950b5c77433bb7df3cf43f999646d938e0afeca45ad4123d681d5aa08f1576`  
		Last Modified: Tue, 12 Mar 2024 02:23:27 GMT  
		Size: 22.4 MB (22354857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:64b7ff72b7d47330d2407edd07ee6ddd8762882093629c0ea442921448fc2ca9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76070350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03235140c06be132c58c0cdeadaa865e344ba6a78e9c1fc9243154a73c0b272d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:47:23 GMT
ADD file:822f8ebf81dcb8d0c3abe6092460eb4cd185e7a4b5b794a9ebc4221cc30518c9 in / 
# Tue, 12 Mar 2024 00:47:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:abb8ff6184544bf5d189fbbab4286e594f2b7adc7d1feb51af49c007cff0e2c6`  
		Last Modified: Tue, 12 Mar 2024 00:53:00 GMT  
		Size: 52.2 MB (52191351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f6a2f77ef2eb04a7b071796c5ec48f48d3cc5f0577048728b1f064cfc42453`  
		Last Modified: Tue, 12 Mar 2024 01:38:42 GMT  
		Size: 23.9 MB (23878999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a5d8d263eeaa0072bc8cf7b2d1eb4c2e0ad8d7e9cf9683ee8082f2a1f6f8fc58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78451889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23290d867c742631003184db5d9b699c20aed43d86814da331ecdd70e94d83fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:00:45 GMT
ADD file:37f9337bf11dc9e80356b325a83e455996065eb5a0bb7e34196dd3ab715908c3 in / 
# Tue, 12 Mar 2024 01:00:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:50:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d38fd1f357db42e901e77bda285b7bc07b7f9c002000df3fbd114813ff6b7831`  
		Last Modified: Tue, 12 Mar 2024 01:07:51 GMT  
		Size: 53.2 MB (53172667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b95670c35235fad2d1e368da26e5ba78fff048eab444dc410d559b74309288`  
		Last Modified: Tue, 12 Mar 2024 07:58:54 GMT  
		Size: 25.3 MB (25279222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:321afc0cb40d301bfd0ad74c630c32138941c3107825567211b1678f80e127be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76032490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b0443104203e1c9bfc980e6c1309403c070444758c3dd09e1d6d3476d6b2d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:54 GMT
ADD file:b1a1fd9e7f874d3dc6cae10f09e49e08335ad86924ba543f9ff6c777d93c7314 in / 
# Tue, 12 Mar 2024 01:12:59 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9b0712382998885f6ab26afd04e80c46f04069a2491aab0d33d167a8539090c2`  
		Last Modified: Tue, 12 Mar 2024 01:25:01 GMT  
		Size: 51.4 MB (51407725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f9dba4bf2ad9240436865bb873640b08db96046b128861417790bef43c9163`  
		Last Modified: Tue, 12 Mar 2024 02:52:06 GMT  
		Size: 24.6 MB (24624765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1fe68362aafea9b2f64fb88db7ea32b2bf09152acc8292adce727344497263b7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82497169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d667898b8391e3b97ea9fc844c269c8c9f9bc3c6d73dfb761960fe84590ef4d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:34:27 GMT
ADD file:ee3f9725c5da5d09634af5073dc8d63c0cf10c6ece6c7b0084a82d44eeaa487e in / 
# Tue, 12 Mar 2024 00:34:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df0d8d793e684337100029abc1076242a4e60e57c67bb9ee5002155393dd3737`  
		Last Modified: Tue, 12 Mar 2024 00:41:55 GMT  
		Size: 56.2 MB (56240791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0231f2ef2e18927b6d6939bd530fca98be4ea26cbda154232692c64973723b7c`  
		Last Modified: Tue, 12 Mar 2024 02:23:59 GMT  
		Size: 26.3 MB (26256378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:83f705be493e94d0f9dc88d3ee5b6ed40435cb2c2fc2d3f80bf6fab9ee228443
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77035318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1b4ae5479896b2c5ee8df61f53aa58a57a6f09cff15b2c8a20903b75650393`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:17 GMT
ADD file:a763a87b7a749afb8ffcbc72555a671734dd9d842834384eebb8dd784135bfc9 in / 
# Tue, 12 Mar 2024 01:12:19 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:26:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2f13ce6fc956957d2abf0abd272bd88a159c9cdf4a731647c572eb2581973c57`  
		Last Modified: Tue, 12 Mar 2024 01:23:47 GMT  
		Size: 51.7 MB (51738519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4953941dae1a90e29387e6e32120bb7c2ebca24adab5d68977c75cbd85a709bf`  
		Last Modified: Tue, 12 Mar 2024 02:50:10 GMT  
		Size: 25.3 MB (25296799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
