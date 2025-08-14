<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:d5fbbf1d3617d563d782bf01503fbd1fef4355c1b7bea10d576e7596406234e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:809c477909cf0fd18862b329bcdd4e87adafffe89bcc78c78595b136288209bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a248704bde343620eff25ad63058e527698b855779e7f60b33c85dbe46976cb4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba70e2e27460d417e9bafe489b7e8aecbfee3ab542cf46506db9e6933daf424`  
		Last Modified: Wed, 13 Aug 2025 00:19:31 GMT  
		Size: 11.3 MB (11266801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63dbb5cfed31f01ce53848be77e54f1b827372f4f336a7c17220a0682a3465b`  
		Last Modified: Tue, 12 Aug 2025 21:27:08 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51e6585eff85a1a04cb4dcd11ea131bf89d28182a044176afb364ae99f1025`  
		Last Modified: Tue, 12 Aug 2025 21:27:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7d1b4818e582a5e2b6e1bdf16e516015dfdcdb7942a5bc6f77e835fc94a109`  
		Last Modified: Tue, 12 Aug 2025 21:27:14 GMT  
		Size: 93.2 KB (93176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2873c836c1cf047a037ddbcb4567dea2943db0b58175712744910b6ce7dae032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2e783ce35e1e95e612539402f6e4ea65d2e012e60536da62a6b0cc44bc9188`

```dockerfile
```

-	Layers:
	-	`sha256:e3a460b4d5d0a3f95c812400f1f36520eaac5ac80142b4917b38bf49dc39c2ec`  
		Last Modified: Wed, 13 Aug 2025 01:07:20 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f05668a5ab1c144345b5041d39371123218559d76cf9a2a838e95fcf44290c3`  
		Last Modified: Wed, 13 Aug 2025 01:07:21 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c8475a51e84b66e3ce6821ff7ceb84eac7fc1f82c048e7e402cc67f417f8d8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59670712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ced994f26f2b092eb62ea23fe3fe8a513dbed97dbe77e57534e99512f27578`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398157a4590ac7aadba659d655fa1e00f8f05a8ab0784529d0099545f337bc03`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 11.2 MB (11232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e01fcd5942424056ba8f0b9a313ff0dde95202c4e3440076fc637b0813c64d`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405e7c25660e800db97c97594d0a4f9b537b1a9fc32793315de1592d0bcfdb9`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2527f69d856843d89ea49d0ee163b7a03c78ceaa2f858c3cbaddacefb732357`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 93.4 KB (93433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:95aa20c2049cfb33598e143e3edd5dc301fed6cc15d10b15e12b05d5fecef4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95975f3930829ee9652fca1f4c3fab3c5ab20a4725720748de2d91c7d54024e9`

```dockerfile
```

-	Layers:
	-	`sha256:6924f68a66edcd1f5082dd813dc5a36f4913133252276abcde4364e8df649299`  
		Last Modified: Wed, 13 Aug 2025 10:09:27 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d38ebd5108b733f20fdcc43249cf599fddb52780aa4f43dfc91df35dc80cfe4`  
		Last Modified: Wed, 13 Aug 2025 10:09:28 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:f84316ff8d8b3ae225ad8c0d7e7e45491b919bb56181dbca5ba1385f3e635cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1819902dbe75b0cccf9bab3c758cf24bbc4c18b666d86310ac25e446f66a16ff`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0557245a4233d6ed0a813738d93888d73d43eb684d18ea929937431c9702`  
		Last Modified: Tue, 12 Aug 2025 21:21:37 GMT  
		Size: 11.7 MB (11688898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73e78c8ed688b9fec478bd057658df7aa8c559e4b5bf882be1c175cd08163b`  
		Last Modified: Tue, 12 Aug 2025 21:21:35 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9193997ad9c823abe8f7d1c1f448e6230c212498a20cdb047aa0dfeff48e673a`  
		Last Modified: Tue, 12 Aug 2025 21:21:34 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7d9601317c4ff1f530caa3ac9c137a87432186a6f634f0acce8c4aadac4c01`  
		Last Modified: Tue, 12 Aug 2025 21:21:32 GMT  
		Size: 93.3 KB (93261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d80795b60339edcebddf5fd87fc6f61602d687c266d903a8b56456a56d0dcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415d1bbbfd7acae7f60115ce66fac55d6a6b2e5f2cab7a30a0363cf67f53b124`

```dockerfile
```

-	Layers:
	-	`sha256:046403f77b477f1e3e1a5f4c7ab21e86bfac80b32b641e05560f049f6b3f4b2b`  
		Last Modified: Wed, 13 Aug 2025 01:07:30 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021a0daf0fa67e89ec9b08cb19b9fa33fe27b477bb7fb2afc77ab8732d68b0fb`  
		Last Modified: Wed, 13 Aug 2025 01:07:31 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:f1700f710fb3a7a7ffd7accf0a37c4009bceb1d2017a8205c6c60109fc57db29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e1e23c85e5bbd51fe50d63418e35e66134c2ffe2f0645c7a4fb95a55f915f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fab33cac0afcc8955f876e9f2516b2593e2071b93bdd8fcdcfdc67b5bd7eb4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca7f8441975b558ca0ef283f56f08f77825f779c076f6de3575109057618921`  
		Last Modified: Tue, 12 Aug 2025 21:25:50 GMT  
		Size: 11.3 MB (11266802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515da2cae6f4e931c65953b83787a4ed52b06f8970245c8033c02dbe26d32d52`  
		Last Modified: Tue, 12 Aug 2025 21:25:49 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05313306ba9a3a0b254f27c2009f9fcf26e25872e146ec58b68f3f122e9e0c4a`  
		Last Modified: Tue, 12 Aug 2025 21:25:49 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61c2a6c5996ede28c75d6706f475897d1f12b8f2741dc359bf1d5337e64abce`  
		Last Modified: Tue, 12 Aug 2025 21:25:51 GMT  
		Size: 93.2 KB (93166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15131243c0bc8e7238da0779914743d971ccbb6a4c7278acaa41b925dbde7af6`  
		Last Modified: Tue, 12 Aug 2025 21:25:50 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56136ee322b43713bfcef696875cb804c977177bdeeb15ab5ec769eba7ba62af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c4db29c0f03c077b176a86f738264f0994c8af0b9181fa2d8b02f3273fc49a`

```dockerfile
```

-	Layers:
	-	`sha256:90d172a22a1a332971f73b7920c30fab0bb63a4644d128ebb0ae1439329a6a1a`  
		Last Modified: Wed, 13 Aug 2025 01:07:28 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ba733a68ceeec254a0fd4c848d419e069030e5403e7a0277c33ac4f6b24dfc`  
		Last Modified: Wed, 13 Aug 2025 01:07:29 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ba4f5c9d0d8e3e88067449edae8ab672eb4b606fa9dcfc9bbe53120ed06b3fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cc5e8120b309a808b8b17384338da1db82b3ea82dadecfd2ace44069dd3bdb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398157a4590ac7aadba659d655fa1e00f8f05a8ab0784529d0099545f337bc03`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 11.2 MB (11232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e01fcd5942424056ba8f0b9a313ff0dde95202c4e3440076fc637b0813c64d`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405e7c25660e800db97c97594d0a4f9b537b1a9fc32793315de1592d0bcfdb9`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2527f69d856843d89ea49d0ee163b7a03c78ceaa2f858c3cbaddacefb732357`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 93.4 KB (93433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f77e7ba9063abd80126010a77ce29596d5e4ba6c0dee2bafae62978e16d71df`  
		Last Modified: Wed, 13 Aug 2025 08:24:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cced9e2b54e8933202292fb68c6cd3012a6e3b144d28f849eb9f3461833ea802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8929676cc0ef7a9617249ccd15b195901245d06533ca9e718ab60f88e10ddec5`

```dockerfile
```

-	Layers:
	-	`sha256:a2f476cc4360921349bb63f66510650c7ae8c83cb34b75346b64ded471694c9e`  
		Last Modified: Wed, 13 Aug 2025 10:09:32 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc458f66151a39b80f39079ebb5ead336f86564387a23c18609431aff638ef3`  
		Last Modified: Wed, 13 Aug 2025 10:09:33 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:01e8d00045f91fb4738ddefff5ce32ca1be6209de1c09736dbf43c5370751b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16b3729e307a1bf3bd90822470070fee8025ff7fff664dcde64d0fc71908edf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5394d0fd08e540a301e3b5f99b64f94f1ba947c5bbe47e0d84a2339afa6c994c`  
		Last Modified: Tue, 12 Aug 2025 21:21:53 GMT  
		Size: 11.7 MB (11688885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e663a91a0aa6dacdc64c684bf82d797030d47adcbff357a5cf069460c1197d`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45030c4feb33187c49f2fd35da69d2b0a7ae3af8dda4972d933421611e48d5`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a397d8483559f951b63a3b5852d5066f8d70d659c67795b7972d016edcf480a`  
		Last Modified: Tue, 12 Aug 2025 21:21:51 GMT  
		Size: 93.2 KB (93211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ff42e5d40a326607d815eb58689a4a20fa2e74ee8668f764f746eadf40a2ad`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bdeeddf6ecca857b4fb89f5b698b4675a355670b44cee651810417717e91070f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73276fe5c06baf891d0fa4cebc9ca03db4c8538c244f9f88efe7831ba61ca6fb`

```dockerfile
```

-	Layers:
	-	`sha256:7528113e7f1996421b92ce6c09b20a6971bc66a7884394ec37d5edb8d1c0a25f`  
		Last Modified: Wed, 13 Aug 2025 01:07:38 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f7f08ce14ba39a229be1a13e27219db34478e744420cca8df3c9878a15d1e31`  
		Last Modified: Wed, 13 Aug 2025 01:07:39 GMT  
		Size: 16.3 KB (16311 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:4fcfe4cc9a359cd5ff6897c80268f988158f7dec262742681f066fadcbc1da21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:73359f39ac469b399641045f30993cfb1211e665c14be5d1be3acee4e7e6c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d22f295b20bd63d92e469a3aaaed3cafa6fa21e068930c1c9e32c3062f9b135`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f1341f5b046e45d8141cbcd596aeb5bc9e20d1e772a9ff8c5383c022fcef98`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 11.1 MB (11105055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde9ea5ac798c1e0bae96acc06a9584dd91340b414ab660442644c94a89ef88`  
		Last Modified: Tue, 12 Aug 2025 21:24:54 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959cabf2060cde6a56e23db3803fca3e12d2fba962b3e7fd543fa595528edb9e`  
		Last Modified: Tue, 12 Aug 2025 21:24:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ba63842ce77c124769a83ad2d9f4800bd8ac6ffd41c15e2fd340e76fef3b0e`  
		Last Modified: Tue, 12 Aug 2025 21:24:53 GMT  
		Size: 101.2 KB (101208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ba9e50898a1c5e35cca4388544d0a2e1719f890e357f6f28860c5d91e8c2331e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd631cb693e276a66445ec7ccdd248112b40f621f77658d840a970a06b7aba0`

```dockerfile
```

-	Layers:
	-	`sha256:64570b92741ba52b33cc885a02c68e29729aed2542df7184b65ba4171d288590`  
		Last Modified: Wed, 13 Aug 2025 01:07:36 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b53f8613bb665bdad8ff512be081aea8fab517622d6d961fc62841839bfb2f9`  
		Last Modified: Wed, 13 Aug 2025 01:07:37 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0512689f3cfbe199ee48b6431b2dd258c6955e2f62187e5e56f3492ea6025d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73a205559c030d50be1f5e59a273a1cd3312c2164151863187294443c88500c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c18e7907793e86e4c9b4f54afbc7f041f620e9915aeae582feba6910c5d3fe`  
		Last Modified: Wed, 13 Aug 2025 09:16:44 GMT  
		Size: 11.1 MB (11106133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeec47a0ab1423984373ae0303d9919cdf61e21c670ff1f3ccb7f6c5a0384a17`  
		Last Modified: Wed, 13 Aug 2025 08:24:53 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ecf4827c1fb509243c0b166ea022847afa5b20921aa447345b6e9d65d78e26`  
		Last Modified: Wed, 13 Aug 2025 08:24:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb37c179c91e7838b6ea61418deb0216abf359de05ab1705f97a3867b180e376`  
		Last Modified: Wed, 13 Aug 2025 08:25:00 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f81a4edae06c09f4a2e3056bac594b088a60586c8695c680c071a968795672a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca203384088fa052de72c03bd7c7ed433bc4cdbf05826dc23942abfb219f4f1d`

```dockerfile
```

-	Layers:
	-	`sha256:0ffb42e8aefce766748d6942b3295332b477e981dcaecda86bf239903e0e1d3e`  
		Last Modified: Wed, 13 Aug 2025 10:09:38 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c105b04a40af2902e00525259dced98e10358a646c041d729301d3fdef42df5b`  
		Last Modified: Wed, 13 Aug 2025 10:09:39 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:545a320c35566a388f6be80f1e52cea27a8e1e2c37c04ef3f3cba5cf7980f30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66294246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74816509a8a58a4184fa1436229bac424666f7a54e88b1bb15d18559a5299a3f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b148e76c29cc0ae2d2cf6449d62900f5cf24990640523768d8221eafa133979a`  
		Last Modified: Tue, 12 Aug 2025 20:44:54 GMT  
		Size: 54.7 MB (54690594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017e1a7b0b50fcd0e466a61f7a7b4d4a44997caf469d94b03e7f2aee7e60d844`  
		Last Modified: Tue, 12 Aug 2025 21:21:05 GMT  
		Size: 11.5 MB (11500388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1045fefbcd8ea997c7d117781f2b9b047731bc82cca186a8828f2b890c6c8f`  
		Last Modified: Tue, 12 Aug 2025 21:21:02 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9fdb56429033d88ca09cb3a5efccb8795a9853cf8fda42dd8c0dba2f5e6e97`  
		Last Modified: Tue, 12 Aug 2025 21:21:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558427f9783dfc4dd7d0c4fa214ca7c5dead3b2fc07a136d8fe80f6cfc873969`  
		Last Modified: Tue, 12 Aug 2025 21:21:02 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6471951e91cd6844a74b6ad78c16ced99ecb938d41b140a5fad91093adfaf059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c338bcf7d1b135dc0e9a37708d9f9f49adfabb59550a1248cd9d393867735b9`

```dockerfile
```

-	Layers:
	-	`sha256:7f29d7bc133c6847669f72eae2ead5f121d1809686d86a4ddbed7862cab1e23d`  
		Last Modified: Wed, 13 Aug 2025 01:07:46 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7b428175076bfcdef56cd8244e4c727bee57bbfe6370955d357d32a95f6802`  
		Last Modified: Wed, 13 Aug 2025 01:07:47 GMT  
		Size: 14.0 KB (13980 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:155c29125c400ee13f6fec8dbe6dfa246e1311faf0e6c33892b97808e0c8274d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:02507ebf5d57f47f1b112cb7825b808c282b8641303941b416ad481e3f84249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64964240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec86a76c5124b01b613fa4648d840a716d35e11a3b53f5b4eeba2d9e79e396b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56452c566b05783df56f9874c82e121f7b219cc55904ac3e2cde9e809f452dfe`  
		Last Modified: Tue, 12 Aug 2025 21:24:54 GMT  
		Size: 11.1 MB (11105132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8bdce4c27174c77ff6183f6ba1e81af52e9a4b93b296e0aa009264d4c39f0c`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b37bcd9134c001294bb6da14d07d349587f33bf8e580897d0c71430184e4981`  
		Last Modified: Tue, 12 Aug 2025 21:24:54 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d44848add8ae2fdc771f6ddc3a1eff4da476a6723975fa33bd017040f1920c1`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 101.2 KB (101218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfa28a2b94b36327f0c5e1beded20f79a23c09f35064e2eacf4e34de8f970ae`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:92f5c73422f4deb334d5ee1a9dcca384e09c930be1c70972d51c05e4ec9cac39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508bb03017fa4c443a9b25a24458910f55725e17b4034a11d4d95651984463e8`

```dockerfile
```

-	Layers:
	-	`sha256:28189c4fb78f00fb45e71990411333f5f7a5cdccf479bf3a843892d15227d66d`  
		Last Modified: Wed, 13 Aug 2025 01:07:43 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d0c8b6bb4257c9505f0edf5bc41dad19a95984c1fd1883e29d7dd3da097956b`  
		Last Modified: Wed, 13 Aug 2025 01:07:44 GMT  
		Size: 16.0 KB (16036 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7531687f9a55eb38fa9a57f951c32708eafa91dae542e6ce99c7848eb32fd738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b704f97f81260e70e92442cd850cdc47a70af45f906d8d99f15d308f1d81e459`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c18e7907793e86e4c9b4f54afbc7f041f620e9915aeae582feba6910c5d3fe`  
		Last Modified: Wed, 13 Aug 2025 09:16:44 GMT  
		Size: 11.1 MB (11106133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeec47a0ab1423984373ae0303d9919cdf61e21c670ff1f3ccb7f6c5a0384a17`  
		Last Modified: Wed, 13 Aug 2025 08:24:53 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ecf4827c1fb509243c0b166ea022847afa5b20921aa447345b6e9d65d78e26`  
		Last Modified: Wed, 13 Aug 2025 08:24:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb37c179c91e7838b6ea61418deb0216abf359de05ab1705f97a3867b180e376`  
		Last Modified: Wed, 13 Aug 2025 08:25:00 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6a5ad58b3cf14e85a71406affbc9683e40e971affe910495a5602577325341`  
		Last Modified: Wed, 13 Aug 2025 07:32:00 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:169c4aa7a53a671d42b5b5166dcb9d805d822edc2945d199803132aba88fda68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115dd6064340ce703e49ad848f7a4df120d50ea029203cf0a2462f29bc34321c`

```dockerfile
```

-	Layers:
	-	`sha256:17f0f32b25d0c477303152533c22c840902ff1d883e3b2480e78a2a20ec95b64`  
		Last Modified: Wed, 13 Aug 2025 10:09:46 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73aabf6e5b624a43ff25ecc279fd680b09e41a11ef3b1eb9f5e079e8b979d614`  
		Last Modified: Wed, 13 Aug 2025 10:09:47 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a2af00e78356ee88f4937f88a0d6f306f501a2baf22eb32420d94714b75ea449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66294649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd21727bb33d618865ae7f1282fb5ca4221dab751012395fe0694e7a1330cae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b148e76c29cc0ae2d2cf6449d62900f5cf24990640523768d8221eafa133979a`  
		Last Modified: Tue, 12 Aug 2025 20:44:54 GMT  
		Size: 54.7 MB (54690594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7e296ebfd94a8bca878ba21b15e1ab045111e0fc6d0e44fcf88e573490090c`  
		Last Modified: Tue, 12 Aug 2025 21:21:47 GMT  
		Size: 11.5 MB (11500405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace1d316ad4599513644e81d66a50f4dca455844e90e781a1594c08ca34d14c`  
		Last Modified: Tue, 12 Aug 2025 21:21:43 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e2efd9b9bd875962c66f91baee4e221c510f2f3d33d4a68693c6ee5ab3997`  
		Last Modified: Tue, 12 Aug 2025 21:21:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec63648871ede6f519bc355b034b8ee7c40c436b269c8c338a8c469e0cd414d1`  
		Last Modified: Tue, 12 Aug 2025 21:21:45 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d915e8d6bae0b17698f6970f49ec08899b2d183b84fe840d4b8e62c9c2db1b37`  
		Last Modified: Tue, 12 Aug 2025 21:21:44 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d2b224a1e6bd3f3afb9074c9a6a88d0a776c1703ace227b7fec0a8936aa671ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901ac69988a39855673c6b3fd08a86e9d43358dd3587740b41d94e04747472d6`

```dockerfile
```

-	Layers:
	-	`sha256:966bc8efd074c44a14b255bbf6956fc34c54ad06dd123d14b0ec9e5a3190ab28`  
		Last Modified: Wed, 13 Aug 2025 01:07:54 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6463bb395e36dc25f6cf2e8cc683b477c52fd885636b0b29bd9c00ff054d5e`  
		Last Modified: Wed, 13 Aug 2025 01:07:55 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:fb871a2d8fde538e46722f1e75d46d124cea1e6c72513d06f9ed06a9e5458f8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f66d98e37bd9b1b373e4258e71504a2f3a3a68f03ce20f6fd41fdf63bb24e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a665154f4cb20d708fa9e806acd4e60846f799df5e96fa2b4173310f638dd9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819d80a80d1bc605dd86075007bd922bd88bc5009783c33e1d4d876db036fdd5`  
		Last Modified: Tue, 12 Aug 2025 18:03:36 GMT  
		Size: 3.6 MB (3625636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961221e682123699cb13c4b32b1b59be8e45b19b85b5bb6b3b72c1cf4c0b157e`  
		Last Modified: Tue, 12 Aug 2025 18:03:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77ed8ef883d94bd4dda60d905819ac30337cac0bebe911d145ac01359a8cdd1`  
		Last Modified: Tue, 12 Aug 2025 18:03:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf73720cfe8f314d366a14999f98a227e3ab288053c6e19e88e061094264bce0`  
		Last Modified: Tue, 12 Aug 2025 18:03:34 GMT  
		Size: 110.6 KB (110616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65cc19c39e1764337b32baa695a8e6e9629c009c99dff6326fc1346b0ae8e428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e00bb3f56e229c3ee2848975d7ac28ca30da08b08477c5e41895cf8dfe35cf`

```dockerfile
```

-	Layers:
	-	`sha256:1c88acb96ddac777b1cc908561d1554c3d648ba86762ef09583cf19cb078bc38`  
		Last Modified: Tue, 12 Aug 2025 19:07:24 GMT  
		Size: 2.2 MB (2198304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2116374dfd5c325bcb5ac95aced49e39a419f4f87764743d188907effb33ddca`  
		Last Modified: Tue, 12 Aug 2025 19:07:24 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ad8b5021080af09840051d598a139cc1c51c5efd96106321e1c90e24d044331b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31070053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffecd0a6844d208ea0f4506ccde69a244b06ffa5e778636e6460a540b30e23fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c79060279f7aa5b518a13677c95296260b1886a9f06c0e227470f215e83ade0`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 3.6 MB (3598083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b131986ef9be15153a34c64bfff28f038121b1c7c30140d9bd1989ac1bc8e1b`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172ce265d02bd87f8e4121afa9fcae149080ac766bda336aed21bb4709d2c93a`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffdd963c92937ca675977e8fc095b7dc1053938bd089842f31e5a5b575a3445`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 110.5 KB (110546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a5e7e4f3b165d34fb2b0551c78a2ff2ac49e39100f1fdc4ec8ea55cbb11a4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e172ac10e0efc41d919cdddd439714cc3a31ce8e2402d91a16378065109184ca`

```dockerfile
```

-	Layers:
	-	`sha256:845a10a1ee83d7027ba8904d7ae03bb1741ff736c904e2aa0a744f5a41812511`  
		Last Modified: Tue, 12 Aug 2025 22:07:25 GMT  
		Size: 2.2 MB (2198564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017a69c5cc0e714fad05106e616c4c380eda5a105290ccc493961416fc91c597`  
		Last Modified: Tue, 12 Aug 2025 22:07:26 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:f3531b70ccbb5a1e18fdb9361e24539d6f6fe8027b6b45ab2dfb637cb866a9b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:908228cbe32ea3d752263f6fd21da848264d885dbf5b5656426884c1f565e295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafc71b275477c6affdc1517faa1f59cda1c5ac1a36c53257d66c0985942091f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb48825ce554bbe3027d028453d69dd46ef5d8b50bb4c9287b75647e3cb2099`  
		Last Modified: Tue, 12 Aug 2025 18:05:03 GMT  
		Size: 3.6 MB (3625601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcfca81afaca970229467729e50e6163ef60b6eaee157ac493aa239af0b4b74`  
		Last Modified: Tue, 12 Aug 2025 18:05:04 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a42426227ce62eabff708b791d83e5fcd26b40077d6a81a366d8fec6c22b5b`  
		Last Modified: Tue, 12 Aug 2025 18:05:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e30728f9a0b3ab3734e7260515c187e0f846c79c438862e511a1ce7c0b3e1b`  
		Last Modified: Tue, 12 Aug 2025 18:05:04 GMT  
		Size: 110.6 KB (110587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cef03f6976b1160cb439d7c91e7e8f1bbff1ac5aacb49434f38b27e34224cfc`  
		Last Modified: Tue, 12 Aug 2025 18:05:03 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ae87f68c14795dfefdde5c7ecb0c0bb3bbb2a30dc3fde958fd5b2ba716a26bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd0e642ddac08a209e7207f0783c30b01c176ec2176cb56d842f2f03f415901`

```dockerfile
```

-	Layers:
	-	`sha256:01cf68b8b517ef0701718303d099a205427904859372f7d57f9dca1adae38e56`  
		Last Modified: Tue, 12 Aug 2025 19:07:25 GMT  
		Size: 2.2 MB (2198340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23614dcd0ab080f0f8954209631320770a55c6c0b3357b111df052ab0995555c`  
		Last Modified: Tue, 12 Aug 2025 19:07:26 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8897c16b790c4dc0fcd920cc05936cdc4533f438af65fcb6c85f1c450428bf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31070341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c495e389b1cc5f153ea965230aaedba5e8398c38dae443edb65f9ba1175b985`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c79060279f7aa5b518a13677c95296260b1886a9f06c0e227470f215e83ade0`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 3.6 MB (3598083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b131986ef9be15153a34c64bfff28f038121b1c7c30140d9bd1989ac1bc8e1b`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172ce265d02bd87f8e4121afa9fcae149080ac766bda336aed21bb4709d2c93a`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffdd963c92937ca675977e8fc095b7dc1053938bd089842f31e5a5b575a3445`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 110.5 KB (110546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662cc4df201faf13345eaa1b94eb51b586ccea3c628ebe5a4623011fd38c412`  
		Last Modified: Tue, 12 Aug 2025 20:33:09 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:32dcb98668b4f9472c37f3298bc9adf3f65803cbd1a6a15922cc9348c3b74375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2bc4732af00fc8c561a45dcb420d7a96a9ca0ec08b48ad576e0f564478eff7`

```dockerfile
```

-	Layers:
	-	`sha256:2f1fba23883a59282ebd7c03d6997a7179a39ed09117dc7c53bfa85a20a1ee01`  
		Last Modified: Tue, 12 Aug 2025 22:07:30 GMT  
		Size: 2.2 MB (2198600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72566b98014e79d881c5b56a29fd8207b1b9c1e15cc2cc910bf0b4cc9210391f`  
		Last Modified: Tue, 12 Aug 2025 22:07:31 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:d5fbbf1d3617d563d782bf01503fbd1fef4355c1b7bea10d576e7596406234e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:809c477909cf0fd18862b329bcdd4e87adafffe89bcc78c78595b136288209bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a248704bde343620eff25ad63058e527698b855779e7f60b33c85dbe46976cb4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba70e2e27460d417e9bafe489b7e8aecbfee3ab542cf46506db9e6933daf424`  
		Last Modified: Wed, 13 Aug 2025 00:19:31 GMT  
		Size: 11.3 MB (11266801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63dbb5cfed31f01ce53848be77e54f1b827372f4f336a7c17220a0682a3465b`  
		Last Modified: Tue, 12 Aug 2025 21:27:08 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51e6585eff85a1a04cb4dcd11ea131bf89d28182a044176afb364ae99f1025`  
		Last Modified: Tue, 12 Aug 2025 21:27:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7d1b4818e582a5e2b6e1bdf16e516015dfdcdb7942a5bc6f77e835fc94a109`  
		Last Modified: Tue, 12 Aug 2025 21:27:14 GMT  
		Size: 93.2 KB (93176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2873c836c1cf047a037ddbcb4567dea2943db0b58175712744910b6ce7dae032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2e783ce35e1e95e612539402f6e4ea65d2e012e60536da62a6b0cc44bc9188`

```dockerfile
```

-	Layers:
	-	`sha256:e3a460b4d5d0a3f95c812400f1f36520eaac5ac80142b4917b38bf49dc39c2ec`  
		Last Modified: Wed, 13 Aug 2025 01:07:20 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f05668a5ab1c144345b5041d39371123218559d76cf9a2a838e95fcf44290c3`  
		Last Modified: Wed, 13 Aug 2025 01:07:21 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c8475a51e84b66e3ce6821ff7ceb84eac7fc1f82c048e7e402cc67f417f8d8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59670712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ced994f26f2b092eb62ea23fe3fe8a513dbed97dbe77e57534e99512f27578`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398157a4590ac7aadba659d655fa1e00f8f05a8ab0784529d0099545f337bc03`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 11.2 MB (11232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e01fcd5942424056ba8f0b9a313ff0dde95202c4e3440076fc637b0813c64d`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405e7c25660e800db97c97594d0a4f9b537b1a9fc32793315de1592d0bcfdb9`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2527f69d856843d89ea49d0ee163b7a03c78ceaa2f858c3cbaddacefb732357`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 93.4 KB (93433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:95aa20c2049cfb33598e143e3edd5dc301fed6cc15d10b15e12b05d5fecef4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95975f3930829ee9652fca1f4c3fab3c5ab20a4725720748de2d91c7d54024e9`

```dockerfile
```

-	Layers:
	-	`sha256:6924f68a66edcd1f5082dd813dc5a36f4913133252276abcde4364e8df649299`  
		Last Modified: Wed, 13 Aug 2025 10:09:27 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d38ebd5108b733f20fdcc43249cf599fddb52780aa4f43dfc91df35dc80cfe4`  
		Last Modified: Wed, 13 Aug 2025 10:09:28 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:f84316ff8d8b3ae225ad8c0d7e7e45491b919bb56181dbca5ba1385f3e635cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1819902dbe75b0cccf9bab3c758cf24bbc4c18b666d86310ac25e446f66a16ff`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0557245a4233d6ed0a813738d93888d73d43eb684d18ea929937431c9702`  
		Last Modified: Tue, 12 Aug 2025 21:21:37 GMT  
		Size: 11.7 MB (11688898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73e78c8ed688b9fec478bd057658df7aa8c559e4b5bf882be1c175cd08163b`  
		Last Modified: Tue, 12 Aug 2025 21:21:35 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9193997ad9c823abe8f7d1c1f448e6230c212498a20cdb047aa0dfeff48e673a`  
		Last Modified: Tue, 12 Aug 2025 21:21:34 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7d9601317c4ff1f530caa3ac9c137a87432186a6f634f0acce8c4aadac4c01`  
		Last Modified: Tue, 12 Aug 2025 21:21:32 GMT  
		Size: 93.3 KB (93261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d80795b60339edcebddf5fd87fc6f61602d687c266d903a8b56456a56d0dcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415d1bbbfd7acae7f60115ce66fac55d6a6b2e5f2cab7a30a0363cf67f53b124`

```dockerfile
```

-	Layers:
	-	`sha256:046403f77b477f1e3e1a5f4c7ab21e86bfac80b32b641e05560f049f6b3f4b2b`  
		Last Modified: Wed, 13 Aug 2025 01:07:30 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021a0daf0fa67e89ec9b08cb19b9fa33fe27b477bb7fb2afc77ab8732d68b0fb`  
		Last Modified: Wed, 13 Aug 2025 01:07:31 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:4fcfe4cc9a359cd5ff6897c80268f988158f7dec262742681f066fadcbc1da21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:73359f39ac469b399641045f30993cfb1211e665c14be5d1be3acee4e7e6c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d22f295b20bd63d92e469a3aaaed3cafa6fa21e068930c1c9e32c3062f9b135`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f1341f5b046e45d8141cbcd596aeb5bc9e20d1e772a9ff8c5383c022fcef98`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 11.1 MB (11105055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde9ea5ac798c1e0bae96acc06a9584dd91340b414ab660442644c94a89ef88`  
		Last Modified: Tue, 12 Aug 2025 21:24:54 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959cabf2060cde6a56e23db3803fca3e12d2fba962b3e7fd543fa595528edb9e`  
		Last Modified: Tue, 12 Aug 2025 21:24:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ba63842ce77c124769a83ad2d9f4800bd8ac6ffd41c15e2fd340e76fef3b0e`  
		Last Modified: Tue, 12 Aug 2025 21:24:53 GMT  
		Size: 101.2 KB (101208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ba9e50898a1c5e35cca4388544d0a2e1719f890e357f6f28860c5d91e8c2331e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd631cb693e276a66445ec7ccdd248112b40f621f77658d840a970a06b7aba0`

```dockerfile
```

-	Layers:
	-	`sha256:64570b92741ba52b33cc885a02c68e29729aed2542df7184b65ba4171d288590`  
		Last Modified: Wed, 13 Aug 2025 01:07:36 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b53f8613bb665bdad8ff512be081aea8fab517622d6d961fc62841839bfb2f9`  
		Last Modified: Wed, 13 Aug 2025 01:07:37 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0512689f3cfbe199ee48b6431b2dd258c6955e2f62187e5e56f3492ea6025d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73a205559c030d50be1f5e59a273a1cd3312c2164151863187294443c88500c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c18e7907793e86e4c9b4f54afbc7f041f620e9915aeae582feba6910c5d3fe`  
		Last Modified: Wed, 13 Aug 2025 09:16:44 GMT  
		Size: 11.1 MB (11106133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeec47a0ab1423984373ae0303d9919cdf61e21c670ff1f3ccb7f6c5a0384a17`  
		Last Modified: Wed, 13 Aug 2025 08:24:53 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ecf4827c1fb509243c0b166ea022847afa5b20921aa447345b6e9d65d78e26`  
		Last Modified: Wed, 13 Aug 2025 08:24:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb37c179c91e7838b6ea61418deb0216abf359de05ab1705f97a3867b180e376`  
		Last Modified: Wed, 13 Aug 2025 08:25:00 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f81a4edae06c09f4a2e3056bac594b088a60586c8695c680c071a968795672a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca203384088fa052de72c03bd7c7ed433bc4cdbf05826dc23942abfb219f4f1d`

```dockerfile
```

-	Layers:
	-	`sha256:0ffb42e8aefce766748d6942b3295332b477e981dcaecda86bf239903e0e1d3e`  
		Last Modified: Wed, 13 Aug 2025 10:09:38 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c105b04a40af2902e00525259dced98e10358a646c041d729301d3fdef42df5b`  
		Last Modified: Wed, 13 Aug 2025 10:09:39 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:545a320c35566a388f6be80f1e52cea27a8e1e2c37c04ef3f3cba5cf7980f30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66294246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74816509a8a58a4184fa1436229bac424666f7a54e88b1bb15d18559a5299a3f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b148e76c29cc0ae2d2cf6449d62900f5cf24990640523768d8221eafa133979a`  
		Last Modified: Tue, 12 Aug 2025 20:44:54 GMT  
		Size: 54.7 MB (54690594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017e1a7b0b50fcd0e466a61f7a7b4d4a44997caf469d94b03e7f2aee7e60d844`  
		Last Modified: Tue, 12 Aug 2025 21:21:05 GMT  
		Size: 11.5 MB (11500388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1045fefbcd8ea997c7d117781f2b9b047731bc82cca186a8828f2b890c6c8f`  
		Last Modified: Tue, 12 Aug 2025 21:21:02 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9fdb56429033d88ca09cb3a5efccb8795a9853cf8fda42dd8c0dba2f5e6e97`  
		Last Modified: Tue, 12 Aug 2025 21:21:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558427f9783dfc4dd7d0c4fa214ca7c5dead3b2fc07a136d8fe80f6cfc873969`  
		Last Modified: Tue, 12 Aug 2025 21:21:02 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6471951e91cd6844a74b6ad78c16ced99ecb938d41b140a5fad91093adfaf059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c338bcf7d1b135dc0e9a37708d9f9f49adfabb59550a1248cd9d393867735b9`

```dockerfile
```

-	Layers:
	-	`sha256:7f29d7bc133c6847669f72eae2ead5f121d1809686d86a4ddbed7862cab1e23d`  
		Last Modified: Wed, 13 Aug 2025 01:07:46 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7b428175076bfcdef56cd8244e4c727bee57bbfe6370955d357d32a95f6802`  
		Last Modified: Wed, 13 Aug 2025 01:07:47 GMT  
		Size: 14.0 KB (13980 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:155c29125c400ee13f6fec8dbe6dfa246e1311faf0e6c33892b97808e0c8274d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:02507ebf5d57f47f1b112cb7825b808c282b8641303941b416ad481e3f84249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64964240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec86a76c5124b01b613fa4648d840a716d35e11a3b53f5b4eeba2d9e79e396b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56452c566b05783df56f9874c82e121f7b219cc55904ac3e2cde9e809f452dfe`  
		Last Modified: Tue, 12 Aug 2025 21:24:54 GMT  
		Size: 11.1 MB (11105132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8bdce4c27174c77ff6183f6ba1e81af52e9a4b93b296e0aa009264d4c39f0c`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b37bcd9134c001294bb6da14d07d349587f33bf8e580897d0c71430184e4981`  
		Last Modified: Tue, 12 Aug 2025 21:24:54 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d44848add8ae2fdc771f6ddc3a1eff4da476a6723975fa33bd017040f1920c1`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 101.2 KB (101218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfa28a2b94b36327f0c5e1beded20f79a23c09f35064e2eacf4e34de8f970ae`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:92f5c73422f4deb334d5ee1a9dcca384e09c930be1c70972d51c05e4ec9cac39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508bb03017fa4c443a9b25a24458910f55725e17b4034a11d4d95651984463e8`

```dockerfile
```

-	Layers:
	-	`sha256:28189c4fb78f00fb45e71990411333f5f7a5cdccf479bf3a843892d15227d66d`  
		Last Modified: Wed, 13 Aug 2025 01:07:43 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d0c8b6bb4257c9505f0edf5bc41dad19a95984c1fd1883e29d7dd3da097956b`  
		Last Modified: Wed, 13 Aug 2025 01:07:44 GMT  
		Size: 16.0 KB (16036 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7531687f9a55eb38fa9a57f951c32708eafa91dae542e6ce99c7848eb32fd738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b704f97f81260e70e92442cd850cdc47a70af45f906d8d99f15d308f1d81e459`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c18e7907793e86e4c9b4f54afbc7f041f620e9915aeae582feba6910c5d3fe`  
		Last Modified: Wed, 13 Aug 2025 09:16:44 GMT  
		Size: 11.1 MB (11106133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeec47a0ab1423984373ae0303d9919cdf61e21c670ff1f3ccb7f6c5a0384a17`  
		Last Modified: Wed, 13 Aug 2025 08:24:53 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ecf4827c1fb509243c0b166ea022847afa5b20921aa447345b6e9d65d78e26`  
		Last Modified: Wed, 13 Aug 2025 08:24:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb37c179c91e7838b6ea61418deb0216abf359de05ab1705f97a3867b180e376`  
		Last Modified: Wed, 13 Aug 2025 08:25:00 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6a5ad58b3cf14e85a71406affbc9683e40e971affe910495a5602577325341`  
		Last Modified: Wed, 13 Aug 2025 07:32:00 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:169c4aa7a53a671d42b5b5166dcb9d805d822edc2945d199803132aba88fda68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115dd6064340ce703e49ad848f7a4df120d50ea029203cf0a2462f29bc34321c`

```dockerfile
```

-	Layers:
	-	`sha256:17f0f32b25d0c477303152533c22c840902ff1d883e3b2480e78a2a20ec95b64`  
		Last Modified: Wed, 13 Aug 2025 10:09:46 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73aabf6e5b624a43ff25ecc279fd680b09e41a11ef3b1eb9f5e079e8b979d614`  
		Last Modified: Wed, 13 Aug 2025 10:09:47 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a2af00e78356ee88f4937f88a0d6f306f501a2baf22eb32420d94714b75ea449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66294649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd21727bb33d618865ae7f1282fb5ca4221dab751012395fe0694e7a1330cae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b148e76c29cc0ae2d2cf6449d62900f5cf24990640523768d8221eafa133979a`  
		Last Modified: Tue, 12 Aug 2025 20:44:54 GMT  
		Size: 54.7 MB (54690594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7e296ebfd94a8bca878ba21b15e1ab045111e0fc6d0e44fcf88e573490090c`  
		Last Modified: Tue, 12 Aug 2025 21:21:47 GMT  
		Size: 11.5 MB (11500405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace1d316ad4599513644e81d66a50f4dca455844e90e781a1594c08ca34d14c`  
		Last Modified: Tue, 12 Aug 2025 21:21:43 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e2efd9b9bd875962c66f91baee4e221c510f2f3d33d4a68693c6ee5ab3997`  
		Last Modified: Tue, 12 Aug 2025 21:21:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec63648871ede6f519bc355b034b8ee7c40c436b269c8c338a8c469e0cd414d1`  
		Last Modified: Tue, 12 Aug 2025 21:21:45 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d915e8d6bae0b17698f6970f49ec08899b2d183b84fe840d4b8e62c9c2db1b37`  
		Last Modified: Tue, 12 Aug 2025 21:21:44 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d2b224a1e6bd3f3afb9074c9a6a88d0a776c1703ace227b7fec0a8936aa671ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901ac69988a39855673c6b3fd08a86e9d43358dd3587740b41d94e04747472d6`

```dockerfile
```

-	Layers:
	-	`sha256:966bc8efd074c44a14b255bbf6956fc34c54ad06dd123d14b0ec9e5a3190ab28`  
		Last Modified: Wed, 13 Aug 2025 01:07:54 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6463bb395e36dc25f6cf2e8cc683b477c52fd885636b0b29bd9c00ff054d5e`  
		Last Modified: Wed, 13 Aug 2025 01:07:55 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:d5fbbf1d3617d563d782bf01503fbd1fef4355c1b7bea10d576e7596406234e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:809c477909cf0fd18862b329bcdd4e87adafffe89bcc78c78595b136288209bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a248704bde343620eff25ad63058e527698b855779e7f60b33c85dbe46976cb4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba70e2e27460d417e9bafe489b7e8aecbfee3ab542cf46506db9e6933daf424`  
		Last Modified: Wed, 13 Aug 2025 00:19:31 GMT  
		Size: 11.3 MB (11266801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63dbb5cfed31f01ce53848be77e54f1b827372f4f336a7c17220a0682a3465b`  
		Last Modified: Tue, 12 Aug 2025 21:27:08 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51e6585eff85a1a04cb4dcd11ea131bf89d28182a044176afb364ae99f1025`  
		Last Modified: Tue, 12 Aug 2025 21:27:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7d1b4818e582a5e2b6e1bdf16e516015dfdcdb7942a5bc6f77e835fc94a109`  
		Last Modified: Tue, 12 Aug 2025 21:27:14 GMT  
		Size: 93.2 KB (93176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2873c836c1cf047a037ddbcb4567dea2943db0b58175712744910b6ce7dae032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2e783ce35e1e95e612539402f6e4ea65d2e012e60536da62a6b0cc44bc9188`

```dockerfile
```

-	Layers:
	-	`sha256:e3a460b4d5d0a3f95c812400f1f36520eaac5ac80142b4917b38bf49dc39c2ec`  
		Last Modified: Wed, 13 Aug 2025 01:07:20 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f05668a5ab1c144345b5041d39371123218559d76cf9a2a838e95fcf44290c3`  
		Last Modified: Wed, 13 Aug 2025 01:07:21 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c8475a51e84b66e3ce6821ff7ceb84eac7fc1f82c048e7e402cc67f417f8d8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59670712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ced994f26f2b092eb62ea23fe3fe8a513dbed97dbe77e57534e99512f27578`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398157a4590ac7aadba659d655fa1e00f8f05a8ab0784529d0099545f337bc03`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 11.2 MB (11232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e01fcd5942424056ba8f0b9a313ff0dde95202c4e3440076fc637b0813c64d`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405e7c25660e800db97c97594d0a4f9b537b1a9fc32793315de1592d0bcfdb9`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2527f69d856843d89ea49d0ee163b7a03c78ceaa2f858c3cbaddacefb732357`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 93.4 KB (93433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:95aa20c2049cfb33598e143e3edd5dc301fed6cc15d10b15e12b05d5fecef4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95975f3930829ee9652fca1f4c3fab3c5ab20a4725720748de2d91c7d54024e9`

```dockerfile
```

-	Layers:
	-	`sha256:6924f68a66edcd1f5082dd813dc5a36f4913133252276abcde4364e8df649299`  
		Last Modified: Wed, 13 Aug 2025 10:09:27 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d38ebd5108b733f20fdcc43249cf599fddb52780aa4f43dfc91df35dc80cfe4`  
		Last Modified: Wed, 13 Aug 2025 10:09:28 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:f84316ff8d8b3ae225ad8c0d7e7e45491b919bb56181dbca5ba1385f3e635cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1819902dbe75b0cccf9bab3c758cf24bbc4c18b666d86310ac25e446f66a16ff`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0557245a4233d6ed0a813738d93888d73d43eb684d18ea929937431c9702`  
		Last Modified: Tue, 12 Aug 2025 21:21:37 GMT  
		Size: 11.7 MB (11688898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73e78c8ed688b9fec478bd057658df7aa8c559e4b5bf882be1c175cd08163b`  
		Last Modified: Tue, 12 Aug 2025 21:21:35 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9193997ad9c823abe8f7d1c1f448e6230c212498a20cdb047aa0dfeff48e673a`  
		Last Modified: Tue, 12 Aug 2025 21:21:34 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7d9601317c4ff1f530caa3ac9c137a87432186a6f634f0acce8c4aadac4c01`  
		Last Modified: Tue, 12 Aug 2025 21:21:32 GMT  
		Size: 93.3 KB (93261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d80795b60339edcebddf5fd87fc6f61602d687c266d903a8b56456a56d0dcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415d1bbbfd7acae7f60115ce66fac55d6a6b2e5f2cab7a30a0363cf67f53b124`

```dockerfile
```

-	Layers:
	-	`sha256:046403f77b477f1e3e1a5f4c7ab21e86bfac80b32b641e05560f049f6b3f4b2b`  
		Last Modified: Wed, 13 Aug 2025 01:07:30 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021a0daf0fa67e89ec9b08cb19b9fa33fe27b477bb7fb2afc77ab8732d68b0fb`  
		Last Modified: Wed, 13 Aug 2025 01:07:31 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:f1700f710fb3a7a7ffd7accf0a37c4009bceb1d2017a8205c6c60109fc57db29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e1e23c85e5bbd51fe50d63418e35e66134c2ffe2f0645c7a4fb95a55f915f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fab33cac0afcc8955f876e9f2516b2593e2071b93bdd8fcdcfdc67b5bd7eb4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca7f8441975b558ca0ef283f56f08f77825f779c076f6de3575109057618921`  
		Last Modified: Tue, 12 Aug 2025 21:25:50 GMT  
		Size: 11.3 MB (11266802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515da2cae6f4e931c65953b83787a4ed52b06f8970245c8033c02dbe26d32d52`  
		Last Modified: Tue, 12 Aug 2025 21:25:49 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05313306ba9a3a0b254f27c2009f9fcf26e25872e146ec58b68f3f122e9e0c4a`  
		Last Modified: Tue, 12 Aug 2025 21:25:49 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61c2a6c5996ede28c75d6706f475897d1f12b8f2741dc359bf1d5337e64abce`  
		Last Modified: Tue, 12 Aug 2025 21:25:51 GMT  
		Size: 93.2 KB (93166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15131243c0bc8e7238da0779914743d971ccbb6a4c7278acaa41b925dbde7af6`  
		Last Modified: Tue, 12 Aug 2025 21:25:50 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56136ee322b43713bfcef696875cb804c977177bdeeb15ab5ec769eba7ba62af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c4db29c0f03c077b176a86f738264f0994c8af0b9181fa2d8b02f3273fc49a`

```dockerfile
```

-	Layers:
	-	`sha256:90d172a22a1a332971f73b7920c30fab0bb63a4644d128ebb0ae1439329a6a1a`  
		Last Modified: Wed, 13 Aug 2025 01:07:28 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ba733a68ceeec254a0fd4c848d419e069030e5403e7a0277c33ac4f6b24dfc`  
		Last Modified: Wed, 13 Aug 2025 01:07:29 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ba4f5c9d0d8e3e88067449edae8ab672eb4b606fa9dcfc9bbe53120ed06b3fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cc5e8120b309a808b8b17384338da1db82b3ea82dadecfd2ace44069dd3bdb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398157a4590ac7aadba659d655fa1e00f8f05a8ab0784529d0099545f337bc03`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 11.2 MB (11232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e01fcd5942424056ba8f0b9a313ff0dde95202c4e3440076fc637b0813c64d`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405e7c25660e800db97c97594d0a4f9b537b1a9fc32793315de1592d0bcfdb9`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2527f69d856843d89ea49d0ee163b7a03c78ceaa2f858c3cbaddacefb732357`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 93.4 KB (93433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f77e7ba9063abd80126010a77ce29596d5e4ba6c0dee2bafae62978e16d71df`  
		Last Modified: Wed, 13 Aug 2025 08:24:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cced9e2b54e8933202292fb68c6cd3012a6e3b144d28f849eb9f3461833ea802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8929676cc0ef7a9617249ccd15b195901245d06533ca9e718ab60f88e10ddec5`

```dockerfile
```

-	Layers:
	-	`sha256:a2f476cc4360921349bb63f66510650c7ae8c83cb34b75346b64ded471694c9e`  
		Last Modified: Wed, 13 Aug 2025 10:09:32 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc458f66151a39b80f39079ebb5ead336f86564387a23c18609431aff638ef3`  
		Last Modified: Wed, 13 Aug 2025 10:09:33 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:01e8d00045f91fb4738ddefff5ce32ca1be6209de1c09736dbf43c5370751b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16b3729e307a1bf3bd90822470070fee8025ff7fff664dcde64d0fc71908edf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5394d0fd08e540a301e3b5f99b64f94f1ba947c5bbe47e0d84a2339afa6c994c`  
		Last Modified: Tue, 12 Aug 2025 21:21:53 GMT  
		Size: 11.7 MB (11688885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e663a91a0aa6dacdc64c684bf82d797030d47adcbff357a5cf069460c1197d`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45030c4feb33187c49f2fd35da69d2b0a7ae3af8dda4972d933421611e48d5`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a397d8483559f951b63a3b5852d5066f8d70d659c67795b7972d016edcf480a`  
		Last Modified: Tue, 12 Aug 2025 21:21:51 GMT  
		Size: 93.2 KB (93211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ff42e5d40a326607d815eb58689a4a20fa2e74ee8668f764f746eadf40a2ad`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bdeeddf6ecca857b4fb89f5b698b4675a355670b44cee651810417717e91070f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73276fe5c06baf891d0fa4cebc9ca03db4c8538c244f9f88efe7831ba61ca6fb`

```dockerfile
```

-	Layers:
	-	`sha256:7528113e7f1996421b92ce6c09b20a6971bc66a7884394ec37d5edb8d1c0a25f`  
		Last Modified: Wed, 13 Aug 2025 01:07:38 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f7f08ce14ba39a229be1a13e27219db34478e744420cca8df3c9878a15d1e31`  
		Last Modified: Wed, 13 Aug 2025 01:07:39 GMT  
		Size: 16.3 KB (16311 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:fb871a2d8fde538e46722f1e75d46d124cea1e6c72513d06f9ed06a9e5458f8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f66d98e37bd9b1b373e4258e71504a2f3a3a68f03ce20f6fd41fdf63bb24e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a665154f4cb20d708fa9e806acd4e60846f799df5e96fa2b4173310f638dd9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819d80a80d1bc605dd86075007bd922bd88bc5009783c33e1d4d876db036fdd5`  
		Last Modified: Tue, 12 Aug 2025 18:03:36 GMT  
		Size: 3.6 MB (3625636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961221e682123699cb13c4b32b1b59be8e45b19b85b5bb6b3b72c1cf4c0b157e`  
		Last Modified: Tue, 12 Aug 2025 18:03:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77ed8ef883d94bd4dda60d905819ac30337cac0bebe911d145ac01359a8cdd1`  
		Last Modified: Tue, 12 Aug 2025 18:03:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf73720cfe8f314d366a14999f98a227e3ab288053c6e19e88e061094264bce0`  
		Last Modified: Tue, 12 Aug 2025 18:03:34 GMT  
		Size: 110.6 KB (110616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65cc19c39e1764337b32baa695a8e6e9629c009c99dff6326fc1346b0ae8e428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e00bb3f56e229c3ee2848975d7ac28ca30da08b08477c5e41895cf8dfe35cf`

```dockerfile
```

-	Layers:
	-	`sha256:1c88acb96ddac777b1cc908561d1554c3d648ba86762ef09583cf19cb078bc38`  
		Last Modified: Tue, 12 Aug 2025 19:07:24 GMT  
		Size: 2.2 MB (2198304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2116374dfd5c325bcb5ac95aced49e39a419f4f87764743d188907effb33ddca`  
		Last Modified: Tue, 12 Aug 2025 19:07:24 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ad8b5021080af09840051d598a139cc1c51c5efd96106321e1c90e24d044331b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31070053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffecd0a6844d208ea0f4506ccde69a244b06ffa5e778636e6460a540b30e23fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c79060279f7aa5b518a13677c95296260b1886a9f06c0e227470f215e83ade0`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 3.6 MB (3598083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b131986ef9be15153a34c64bfff28f038121b1c7c30140d9bd1989ac1bc8e1b`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172ce265d02bd87f8e4121afa9fcae149080ac766bda336aed21bb4709d2c93a`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffdd963c92937ca675977e8fc095b7dc1053938bd089842f31e5a5b575a3445`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 110.5 KB (110546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a5e7e4f3b165d34fb2b0551c78a2ff2ac49e39100f1fdc4ec8ea55cbb11a4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e172ac10e0efc41d919cdddd439714cc3a31ce8e2402d91a16378065109184ca`

```dockerfile
```

-	Layers:
	-	`sha256:845a10a1ee83d7027ba8904d7ae03bb1741ff736c904e2aa0a744f5a41812511`  
		Last Modified: Tue, 12 Aug 2025 22:07:25 GMT  
		Size: 2.2 MB (2198564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017a69c5cc0e714fad05106e616c4c380eda5a105290ccc493961416fc91c597`  
		Last Modified: Tue, 12 Aug 2025 22:07:26 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:f3531b70ccbb5a1e18fdb9361e24539d6f6fe8027b6b45ab2dfb637cb866a9b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:908228cbe32ea3d752263f6fd21da848264d885dbf5b5656426884c1f565e295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafc71b275477c6affdc1517faa1f59cda1c5ac1a36c53257d66c0985942091f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb48825ce554bbe3027d028453d69dd46ef5d8b50bb4c9287b75647e3cb2099`  
		Last Modified: Tue, 12 Aug 2025 18:05:03 GMT  
		Size: 3.6 MB (3625601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcfca81afaca970229467729e50e6163ef60b6eaee157ac493aa239af0b4b74`  
		Last Modified: Tue, 12 Aug 2025 18:05:04 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a42426227ce62eabff708b791d83e5fcd26b40077d6a81a366d8fec6c22b5b`  
		Last Modified: Tue, 12 Aug 2025 18:05:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e30728f9a0b3ab3734e7260515c187e0f846c79c438862e511a1ce7c0b3e1b`  
		Last Modified: Tue, 12 Aug 2025 18:05:04 GMT  
		Size: 110.6 KB (110587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cef03f6976b1160cb439d7c91e7e8f1bbff1ac5aacb49434f38b27e34224cfc`  
		Last Modified: Tue, 12 Aug 2025 18:05:03 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ae87f68c14795dfefdde5c7ecb0c0bb3bbb2a30dc3fde958fd5b2ba716a26bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd0e642ddac08a209e7207f0783c30b01c176ec2176cb56d842f2f03f415901`

```dockerfile
```

-	Layers:
	-	`sha256:01cf68b8b517ef0701718303d099a205427904859372f7d57f9dca1adae38e56`  
		Last Modified: Tue, 12 Aug 2025 19:07:25 GMT  
		Size: 2.2 MB (2198340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23614dcd0ab080f0f8954209631320770a55c6c0b3357b111df052ab0995555c`  
		Last Modified: Tue, 12 Aug 2025 19:07:26 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8897c16b790c4dc0fcd920cc05936cdc4533f438af65fcb6c85f1c450428bf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31070341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c495e389b1cc5f153ea965230aaedba5e8398c38dae443edb65f9ba1175b985`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c79060279f7aa5b518a13677c95296260b1886a9f06c0e227470f215e83ade0`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 3.6 MB (3598083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b131986ef9be15153a34c64bfff28f038121b1c7c30140d9bd1989ac1bc8e1b`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172ce265d02bd87f8e4121afa9fcae149080ac766bda336aed21bb4709d2c93a`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffdd963c92937ca675977e8fc095b7dc1053938bd089842f31e5a5b575a3445`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 110.5 KB (110546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662cc4df201faf13345eaa1b94eb51b586ccea3c628ebe5a4623011fd38c412`  
		Last Modified: Tue, 12 Aug 2025 20:33:09 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:32dcb98668b4f9472c37f3298bc9adf3f65803cbd1a6a15922cc9348c3b74375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2bc4732af00fc8c561a45dcb420d7a96a9ca0ec08b48ad576e0f564478eff7`

```dockerfile
```

-	Layers:
	-	`sha256:2f1fba23883a59282ebd7c03d6997a7179a39ed09117dc7c53bfa85a20a1ee01`  
		Last Modified: Tue, 12 Aug 2025 22:07:30 GMT  
		Size: 2.2 MB (2198600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72566b98014e79d881c5b56a29fd8207b1b9c1e15cc2cc910bf0b4cc9210391f`  
		Last Modified: Tue, 12 Aug 2025 22:07:31 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:f1700f710fb3a7a7ffd7accf0a37c4009bceb1d2017a8205c6c60109fc57db29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e1e23c85e5bbd51fe50d63418e35e66134c2ffe2f0645c7a4fb95a55f915f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fab33cac0afcc8955f876e9f2516b2593e2071b93bdd8fcdcfdc67b5bd7eb4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca7f8441975b558ca0ef283f56f08f77825f779c076f6de3575109057618921`  
		Last Modified: Tue, 12 Aug 2025 21:25:50 GMT  
		Size: 11.3 MB (11266802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515da2cae6f4e931c65953b83787a4ed52b06f8970245c8033c02dbe26d32d52`  
		Last Modified: Tue, 12 Aug 2025 21:25:49 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05313306ba9a3a0b254f27c2009f9fcf26e25872e146ec58b68f3f122e9e0c4a`  
		Last Modified: Tue, 12 Aug 2025 21:25:49 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61c2a6c5996ede28c75d6706f475897d1f12b8f2741dc359bf1d5337e64abce`  
		Last Modified: Tue, 12 Aug 2025 21:25:51 GMT  
		Size: 93.2 KB (93166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15131243c0bc8e7238da0779914743d971ccbb6a4c7278acaa41b925dbde7af6`  
		Last Modified: Tue, 12 Aug 2025 21:25:50 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56136ee322b43713bfcef696875cb804c977177bdeeb15ab5ec769eba7ba62af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c4db29c0f03c077b176a86f738264f0994c8af0b9181fa2d8b02f3273fc49a`

```dockerfile
```

-	Layers:
	-	`sha256:90d172a22a1a332971f73b7920c30fab0bb63a4644d128ebb0ae1439329a6a1a`  
		Last Modified: Wed, 13 Aug 2025 01:07:28 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ba733a68ceeec254a0fd4c848d419e069030e5403e7a0277c33ac4f6b24dfc`  
		Last Modified: Wed, 13 Aug 2025 01:07:29 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ba4f5c9d0d8e3e88067449edae8ab672eb4b606fa9dcfc9bbe53120ed06b3fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cc5e8120b309a808b8b17384338da1db82b3ea82dadecfd2ace44069dd3bdb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398157a4590ac7aadba659d655fa1e00f8f05a8ab0784529d0099545f337bc03`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 11.2 MB (11232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e01fcd5942424056ba8f0b9a313ff0dde95202c4e3440076fc637b0813c64d`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405e7c25660e800db97c97594d0a4f9b537b1a9fc32793315de1592d0bcfdb9`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2527f69d856843d89ea49d0ee163b7a03c78ceaa2f858c3cbaddacefb732357`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 93.4 KB (93433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f77e7ba9063abd80126010a77ce29596d5e4ba6c0dee2bafae62978e16d71df`  
		Last Modified: Wed, 13 Aug 2025 08:24:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cced9e2b54e8933202292fb68c6cd3012a6e3b144d28f849eb9f3461833ea802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8929676cc0ef7a9617249ccd15b195901245d06533ca9e718ab60f88e10ddec5`

```dockerfile
```

-	Layers:
	-	`sha256:a2f476cc4360921349bb63f66510650c7ae8c83cb34b75346b64ded471694c9e`  
		Last Modified: Wed, 13 Aug 2025 10:09:32 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc458f66151a39b80f39079ebb5ead336f86564387a23c18609431aff638ef3`  
		Last Modified: Wed, 13 Aug 2025 10:09:33 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:01e8d00045f91fb4738ddefff5ce32ca1be6209de1c09736dbf43c5370751b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16b3729e307a1bf3bd90822470070fee8025ff7fff664dcde64d0fc71908edf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5394d0fd08e540a301e3b5f99b64f94f1ba947c5bbe47e0d84a2339afa6c994c`  
		Last Modified: Tue, 12 Aug 2025 21:21:53 GMT  
		Size: 11.7 MB (11688885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e663a91a0aa6dacdc64c684bf82d797030d47adcbff357a5cf069460c1197d`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45030c4feb33187c49f2fd35da69d2b0a7ae3af8dda4972d933421611e48d5`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a397d8483559f951b63a3b5852d5066f8d70d659c67795b7972d016edcf480a`  
		Last Modified: Tue, 12 Aug 2025 21:21:51 GMT  
		Size: 93.2 KB (93211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ff42e5d40a326607d815eb58689a4a20fa2e74ee8668f764f746eadf40a2ad`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bdeeddf6ecca857b4fb89f5b698b4675a355670b44cee651810417717e91070f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73276fe5c06baf891d0fa4cebc9ca03db4c8538c244f9f88efe7831ba61ca6fb`

```dockerfile
```

-	Layers:
	-	`sha256:7528113e7f1996421b92ce6c09b20a6971bc66a7884394ec37d5edb8d1c0a25f`  
		Last Modified: Wed, 13 Aug 2025 01:07:38 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f7f08ce14ba39a229be1a13e27219db34478e744420cca8df3c9878a15d1e31`  
		Last Modified: Wed, 13 Aug 2025 01:07:39 GMT  
		Size: 16.3 KB (16311 bytes)  
		MIME: application/vnd.in-toto+json
