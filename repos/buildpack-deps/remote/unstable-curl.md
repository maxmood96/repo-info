## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:ac30cd05719d9dbedb9fa7ceacc98481053c704ef46b70195ba3778fec391a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:12348240e5db18afa70f6382420fb3e36194a640ffa7f21e5506ded546ce702b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73345043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801581c78b136e899df5cbff068467129f0d26f6e4add3126d2743694757cdae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:39 GMT
ADD file:0ded1ec762355d6c32b4a9f1eff5fbd5e60d15824d6bde678ef85cbdd03fe0ce in / 
# Tue, 23 Aug 2022 00:21:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:50:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 00:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6649fedb76d916c1041e321eca86994acdb4cd14cc61ef93b5d2a397c15af4ad`  
		Last Modified: Tue, 23 Aug 2022 00:26:41 GMT  
		Size: 52.8 MB (52768784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52383a4258951f21b40d1c18a5c708ecfd3cc7f76838fc8fbe3c1fa248f7b133`  
		Last Modified: Tue, 23 Aug 2022 00:57:51 GMT  
		Size: 9.3 MB (9302218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8bf82596b529ddf3a818d599c3bed1bef1e54925ac4df0a1a6bf6467ce1bd2`  
		Last Modified: Tue, 23 Aug 2022 00:57:51 GMT  
		Size: 11.3 MB (11274041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:71e2c01c10738a2393e1de893af0ba2af96f670e69ba1247ff4b341d90328bbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71709647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40fb8851f698beb9ffdb247f1c155484eab3e8768974b75caf70e82830d33b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:23 GMT
ADD file:2829a8dbc1e67454e67c0015efaaceadaa4b04330ed9e60cc8248246cac2aae2 in / 
# Tue, 02 Aug 2022 00:50:23 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:11a67d4cf31e6e9dc8797a5c01d3198f326d91410c372d1a490bf5592578d9b1`  
		Last Modified: Tue, 02 Aug 2022 00:58:37 GMT  
		Size: 52.0 MB (52021372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6833771528bea1307d56591db306804d9768947a466a60b5de4f6b545ab0cec5`  
		Last Modified: Tue, 02 Aug 2022 01:33:35 GMT  
		Size: 8.7 MB (8741294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2288f8703c485a4ea82b9d9a1de8905ae4f0e420ca4f317625f441977a31c0`  
		Last Modified: Tue, 02 Aug 2022 01:33:34 GMT  
		Size: 10.9 MB (10946981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6a1dc7cb1cfabd89e6d480fd7636b4982c9b8d7938703b686a3f106e6730956a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68748018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836d2baee2173e1ced99b95dbe1a7c3bfc11ee36f69245661672947313a3bcc2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:00:45 GMT
ADD file:a1d27fd37cd41b3026c10df50adfd5a93a40194548a87a372c97149f63b096b3 in / 
# Tue, 02 Aug 2022 01:00:46 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:50:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:23e34b183a37464e321571d2a75fa33fded0e5a8506066db5c4f20153a665c2c`  
		Last Modified: Tue, 02 Aug 2022 01:09:03 GMT  
		Size: 49.7 MB (49735351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af50b5c584586bbf2589138734167dd8e14560e75cd854cd9bca75019a3f530b`  
		Last Modified: Tue, 02 Aug 2022 02:12:03 GMT  
		Size: 8.4 MB (8423017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4818fead9ad7b4ed572aa86d08f341272cc2cbb418cbe22f7f7d71f2be3778d`  
		Last Modified: Tue, 02 Aug 2022 02:12:03 GMT  
		Size: 10.6 MB (10589650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:862e19141101ececdd8c8b4b921d9c66454cb29054c94150f924f060b9e1b670
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73524133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fb6c857675349da2e7836394fde759284d1652aa07a8511357c92c56779c68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:38 GMT
ADD file:477966410dd9e274b01740d7af857db5c024b4c4e53a5e83b5da6854d5b0c209 in / 
# Tue, 02 Aug 2022 00:41:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:27:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:17bcb8e39c7f35480d4c2e5b46b6c0a58dac180206453cc49052707aa8053632`  
		Last Modified: Tue, 02 Aug 2022 00:48:00 GMT  
		Size: 53.3 MB (53311787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040e49dab65b12b89c427063ea6eec0802e14801664648c428e5a774754f3e73`  
		Last Modified: Tue, 02 Aug 2022 01:47:00 GMT  
		Size: 9.2 MB (9150009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b71a9f562c782f5916aedb7846293c7057b9f5f32ac072f785d2b21839f530`  
		Last Modified: Tue, 02 Aug 2022 01:46:57 GMT  
		Size: 11.1 MB (11062337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b9972c98ff602f317e6304009068bc0bcfd55766be4faadef16a50f2e560ac0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75087575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be006906138be6be28f63d53b6777210491d213b2fd95065a1fd6ca582699aad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:03:44 GMT
ADD file:56a765ed5b9c59576a105c4e82da61f928406a2ef950e7cada80b5c269a1acda in / 
# Tue, 23 Aug 2022 01:03:44 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:35:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:35:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:05690d5133887cdda89e6ae4808c08e8a92acf2163ce992d8bacbed497b1ddd7`  
		Last Modified: Tue, 23 Aug 2022 01:10:25 GMT  
		Size: 54.1 MB (54133693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6de5521fae7f54e276230f1136f3c889618c53b37f387bcb06db2c09c9ea96`  
		Last Modified: Tue, 23 Aug 2022 01:42:35 GMT  
		Size: 9.5 MB (9480147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1ad46fde87250408a791d37517179cd6427cd46421e84e138f00437a005cc8`  
		Last Modified: Tue, 23 Aug 2022 01:42:35 GMT  
		Size: 11.5 MB (11473735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a066927b5ec09a3c745cdb27319b860af8d276f3d23efc2b091f4a9a10370066
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73007477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b88a966c0901785dc7b8096d2394d610676b405eebe695aac588ab352de1cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:13:16 GMT
ADD file:6165703835b4dbffafda027e272e21bf37cfc276085814fa1d03c1db0162e605 in / 
# Tue, 02 Aug 2022 01:13:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:11:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:11:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:71112f7b4dfd928d54aaa23ee1023fef50d2dc747bf6e2168afe69932ce8aa1a`  
		Last Modified: Tue, 02 Aug 2022 01:24:23 GMT  
		Size: 53.3 MB (53305987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523353756f561bdc5914e25ea1cfeda5bc330e894285664b88d8ce11aa594a29`  
		Last Modified: Tue, 02 Aug 2022 02:30:34 GMT  
		Size: 8.7 MB (8659688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258650534e83b3efae8fb3f1ce269322b09b63e553775a7c0b8c8104b2451b0`  
		Last Modified: Tue, 02 Aug 2022 02:30:34 GMT  
		Size: 11.0 MB (11041802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:06cdfa0e53f775de781a7ca8df696f077aa8d11900079078ba6d09ffa6afe1f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79414372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff993c0b06ebb20e22928ce3857f84fb8df00f14907bb609468fca58d3182c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:52 GMT
ADD file:6911368d0ae9ca029c373628ddb642f29cabf3f909e9a77f8931355843b8ea49 in / 
# Tue, 02 Aug 2022 01:18:54 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:35:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:35:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4a386a4ce4974e6c6fc3a96c6a7a96ce47fa8df11122fa0a4b856c23c5ccb46b`  
		Last Modified: Tue, 02 Aug 2022 01:27:09 GMT  
		Size: 57.4 MB (57440227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0eae2292d82f6824061d200408b3f0dfb525d1d5fcf719a2e4c01a7c4c82aea`  
		Last Modified: Tue, 02 Aug 2022 03:17:23 GMT  
		Size: 9.9 MB (9890501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465fd13cc41c21f92aad774503ecba5a1a350a8ee1c0affd0e437746ba26a774`  
		Last Modified: Tue, 02 Aug 2022 03:17:23 GMT  
		Size: 12.1 MB (12083644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7190f1576496c38d326bf20b45a9725d2c7888724774b79fa03f1ad5fdb68d29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68327170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbcd3644b4a571e4579adbe4eb08af38c965c5986789fdd1a493de8456457e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:12:03 GMT
ADD file:beb3c4d0f1887ccbbe2b266a156b7658d2e1d7d48cbcd416a0410554dfafdf12 in / 
# Tue, 23 Aug 2022 00:12:06 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:58:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 00:59:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:11998c1ffc96119253ef35ecbcfd66c2cb0d69f51a294f603a54496ec02d329c`  
		Last Modified: Tue, 23 Aug 2022 00:30:27 GMT  
		Size: 49.3 MB (49268189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237ee2e31cf68d3cd2675680cbf1e3c574c76f74440375dc1b8c1ad1d3d9768e`  
		Last Modified: Tue, 23 Aug 2022 01:41:12 GMT  
		Size: 8.4 MB (8399080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69eb487c5f4d1ba65732a0b11d3a69780177b7ed0357581fce4eb347813a643`  
		Last Modified: Tue, 23 Aug 2022 01:41:12 GMT  
		Size: 10.7 MB (10659901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e7c48a4d90ad2c746b43f0827ca881fc92ec57c70337fd9e24e589de09a2c2c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71862403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bfaae2997e205011a76eae3acb25d30ce8a2d7ee833c538bd2355a4dfcca40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:43:36 GMT
ADD file:19dee33de85aac92620de3bd92768833a889db0b60b7445419bccb4285c46f94 in / 
# Tue, 02 Aug 2022 00:43:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:12:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:12:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:31888e988211ae2cd4058438d0fd3d3420a26d35f21e97741527c1e85ad2d476`  
		Last Modified: Tue, 02 Aug 2022 00:49:29 GMT  
		Size: 51.7 MB (51734666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd60a4351ebe5fad9f32c09d0a6f7ec29b6c6dcb5ff8c29e6650149557447e2`  
		Last Modified: Tue, 02 Aug 2022 01:36:55 GMT  
		Size: 9.0 MB (8960873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0db795ce4385e2a159326c7d9ab52e109942607b82b1c377894e874e601d`  
		Last Modified: Tue, 02 Aug 2022 01:36:55 GMT  
		Size: 11.2 MB (11166864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
