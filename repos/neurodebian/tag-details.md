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
$ docker pull neurodebian@sha256:975465318c2961a62e84945b66e3eb674c0cc276f3f1c79e9d775380ed7e2978
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3ce910a25e1ada8fb29113c427d363d0950df18f993942bb1e966b293c906fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc492e3e53cf64bb4f5f322e8772c61cb99e0627ce806d72563b7cd165fa6c0`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a4724a87526948a669d180182a6778e1e691c719838765abce4d01c46d3989`  
		Last Modified: Tue, 02 Sep 2025 00:23:48 GMT  
		Size: 3.6 MB (3625618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c380e33d94fb72232b49c8bc34ed7ec6d5fc476094360c374549509f46be63`  
		Last Modified: Tue, 02 Sep 2025 00:23:47 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5b8f40e27413a9ed04a139b53a2d27ad574119fb38e07573119b5f1ba2b7cb`  
		Last Modified: Tue, 02 Sep 2025 00:23:41 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f236e29b2af85abd6976a93143c874089cd671b6c9dce78ea9370ae33bedea`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 110.6 KB (110589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:34aff235caca5114ffe5988df3758c029134f3cfd79928f2b7b75e046d884177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35a861e1f8209aec3893a6055acb4e242ebe33c2703d85a893b48ff3b02363a`

```dockerfile
```

-	Layers:
	-	`sha256:7d41caedea004a5f24a35b74306fc2bb1a9a276bf38f155d55be744db8ac4a1e`  
		Last Modified: Tue, 02 Sep 2025 01:07:20 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09e2e050c9cb1cb84b85074083ff037333a48e8c7fdc30b0f24b2e72482d686`  
		Last Modified: Tue, 02 Sep 2025 01:07:21 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3d755067362f393c7585144595d3f2754010a5c721f206cd73de9f771bc93aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31072458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef546e0120c2e4950f832e3f1f63ea76331b4eddda9a60829a347bccc6d11f0`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b0329cf2a4a15a9bf4b14570d09ca06b3b9b031182d9d673722455466dea4`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 3.6 MB (3598206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b2c6c73f48a5205154bbeefdc3a62200f2912abd347eab19218d25884b59c6`  
		Last Modified: Tue, 02 Sep 2025 02:31:43 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6dd113705bb44b0596d44cfd3ff0395aac0b756dc8da44d1563df648bedfe`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02baa23e0d6f84b6310f25f56d9459f98c61c4ae69864e811e3f6d95714f90`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 110.6 KB (110605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50ea19520af7ff7bb17b1c87749b89c3d943ef0cd19a831bb8d497304d58d9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322e60f23e6672fb7149c0f864f30ec442e1b554da2264f5133d991f7e647c51`

```dockerfile
```

-	Layers:
	-	`sha256:5c2043d6adc338e426d3f82ccf4134905c4a04e1d8a86411801d898cb43d5ce9`  
		Last Modified: Tue, 02 Sep 2025 04:07:27 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1c964ae4683d90f63a5cbd6b78ef63792fd7523b7173d484e631d31afa51ba`  
		Last Modified: Tue, 02 Sep 2025 04:07:27 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:5a0fd02a955581821f5e1e61b232651e9eb3e9d8f5d112dd221a5079ab5a4655
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2fa15741085a7b9a111304f94de710a342d4003de42f96d7188ae76614ee49ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f3a6a8f1c8ad9cece02d2fe19baf080213cf7ed68cdb0ad98152ada06cb1f`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d350e6c4b05f6944ae006b8aab5488c91516ffd162cfaba7f84ac273d473b`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 3.6 MB (3625625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e43a114a27e26541cb1e85f4e91c965938ba1a97cae143d255897aff2129a`  
		Last Modified: Tue, 02 Sep 2025 00:23:44 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ac9ace5a9e24d09a5d74cfbef2b3423c8652f27e8f966bd9bc62e9113363ce`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32399516aec62d325145feb3435edfb7a8ae0199ff2cb6bbd66c90cccb4d2e3`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 110.6 KB (110617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7cb48d532455ee1f3cb8304abe4242d944151fed04590177b16c700f70b807`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c57cc66c296caefe8491e689ab76b85cfa5a28354db8fcaf6d4e285820860324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607be7f30cc779a1e17202a6d6c14b2ac08edabd49cd5703daef1c66963a2b95`

```dockerfile
```

-	Layers:
	-	`sha256:28344ea9cda64308e3f2beaec2b0f1ecf33f042627051ad839a05fbb550e8d2e`  
		Last Modified: Tue, 02 Sep 2025 01:07:24 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32e711bd76c0a3933a65639adf42f2367cc2f94d3e8d671098de1fec9256e73`  
		Last Modified: Tue, 02 Sep 2025 01:07:25 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:16c1487ee25e15abee9aa27c20c3bc91b9fa4c99bab65e7a742963d60666def6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31072747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6792b8f84d3304ef6e28de08173b87ae23cf5b542ae198b8bd962bf5b29b4a40`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b0329cf2a4a15a9bf4b14570d09ca06b3b9b031182d9d673722455466dea4`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 3.6 MB (3598206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b2c6c73f48a5205154bbeefdc3a62200f2912abd347eab19218d25884b59c6`  
		Last Modified: Tue, 02 Sep 2025 02:31:43 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6dd113705bb44b0596d44cfd3ff0395aac0b756dc8da44d1563df648bedfe`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02baa23e0d6f84b6310f25f56d9459f98c61c4ae69864e811e3f6d95714f90`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 110.6 KB (110605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b579638f5ad784db8571cf092a6ef4ab30b240756a48f6c38c0e8dc718d7610d`  
		Last Modified: Tue, 02 Sep 2025 02:31:46 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf925a26094fa612cb22d55b1e64484fb6c1683525aa871d37fd1df276896a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c790b7b9e0fe69d544874fceaebe8f92b6265deaed73d3e8ed48cec56061cf7`

```dockerfile
```

-	Layers:
	-	`sha256:b956c6cf699422639abaacca5984085ebbe4ef744fc698f2bc3ef106bba50906`  
		Last Modified: Tue, 02 Sep 2025 04:07:28 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42e7b9a80bb3eb37d02c02dc8ae979642d01e3d3644d30077268d4519deff36`  
		Last Modified: Tue, 02 Sep 2025 04:07:29 GMT  
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
$ docker pull neurodebian@sha256:975465318c2961a62e84945b66e3eb674c0cc276f3f1c79e9d775380ed7e2978
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3ce910a25e1ada8fb29113c427d363d0950df18f993942bb1e966b293c906fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc492e3e53cf64bb4f5f322e8772c61cb99e0627ce806d72563b7cd165fa6c0`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a4724a87526948a669d180182a6778e1e691c719838765abce4d01c46d3989`  
		Last Modified: Tue, 02 Sep 2025 00:23:48 GMT  
		Size: 3.6 MB (3625618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c380e33d94fb72232b49c8bc34ed7ec6d5fc476094360c374549509f46be63`  
		Last Modified: Tue, 02 Sep 2025 00:23:47 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5b8f40e27413a9ed04a139b53a2d27ad574119fb38e07573119b5f1ba2b7cb`  
		Last Modified: Tue, 02 Sep 2025 00:23:41 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f236e29b2af85abd6976a93143c874089cd671b6c9dce78ea9370ae33bedea`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 110.6 KB (110589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:34aff235caca5114ffe5988df3758c029134f3cfd79928f2b7b75e046d884177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35a861e1f8209aec3893a6055acb4e242ebe33c2703d85a893b48ff3b02363a`

```dockerfile
```

-	Layers:
	-	`sha256:7d41caedea004a5f24a35b74306fc2bb1a9a276bf38f155d55be744db8ac4a1e`  
		Last Modified: Tue, 02 Sep 2025 01:07:20 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09e2e050c9cb1cb84b85074083ff037333a48e8c7fdc30b0f24b2e72482d686`  
		Last Modified: Tue, 02 Sep 2025 01:07:21 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3d755067362f393c7585144595d3f2754010a5c721f206cd73de9f771bc93aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31072458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef546e0120c2e4950f832e3f1f63ea76331b4eddda9a60829a347bccc6d11f0`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b0329cf2a4a15a9bf4b14570d09ca06b3b9b031182d9d673722455466dea4`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 3.6 MB (3598206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b2c6c73f48a5205154bbeefdc3a62200f2912abd347eab19218d25884b59c6`  
		Last Modified: Tue, 02 Sep 2025 02:31:43 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6dd113705bb44b0596d44cfd3ff0395aac0b756dc8da44d1563df648bedfe`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02baa23e0d6f84b6310f25f56d9459f98c61c4ae69864e811e3f6d95714f90`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 110.6 KB (110605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50ea19520af7ff7bb17b1c87749b89c3d943ef0cd19a831bb8d497304d58d9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322e60f23e6672fb7149c0f864f30ec442e1b554da2264f5133d991f7e647c51`

```dockerfile
```

-	Layers:
	-	`sha256:5c2043d6adc338e426d3f82ccf4134905c4a04e1d8a86411801d898cb43d5ce9`  
		Last Modified: Tue, 02 Sep 2025 04:07:27 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1c964ae4683d90f63a5cbd6b78ef63792fd7523b7173d484e631d31afa51ba`  
		Last Modified: Tue, 02 Sep 2025 04:07:27 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:5a0fd02a955581821f5e1e61b232651e9eb3e9d8f5d112dd221a5079ab5a4655
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2fa15741085a7b9a111304f94de710a342d4003de42f96d7188ae76614ee49ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f3a6a8f1c8ad9cece02d2fe19baf080213cf7ed68cdb0ad98152ada06cb1f`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d350e6c4b05f6944ae006b8aab5488c91516ffd162cfaba7f84ac273d473b`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 3.6 MB (3625625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e43a114a27e26541cb1e85f4e91c965938ba1a97cae143d255897aff2129a`  
		Last Modified: Tue, 02 Sep 2025 00:23:44 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ac9ace5a9e24d09a5d74cfbef2b3423c8652f27e8f966bd9bc62e9113363ce`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32399516aec62d325145feb3435edfb7a8ae0199ff2cb6bbd66c90cccb4d2e3`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 110.6 KB (110617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7cb48d532455ee1f3cb8304abe4242d944151fed04590177b16c700f70b807`  
		Last Modified: Tue, 02 Sep 2025 00:23:45 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c57cc66c296caefe8491e689ab76b85cfa5a28354db8fcaf6d4e285820860324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607be7f30cc779a1e17202a6d6c14b2ac08edabd49cd5703daef1c66963a2b95`

```dockerfile
```

-	Layers:
	-	`sha256:28344ea9cda64308e3f2beaec2b0f1ecf33f042627051ad839a05fbb550e8d2e`  
		Last Modified: Tue, 02 Sep 2025 01:07:24 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32e711bd76c0a3933a65639adf42f2367cc2f94d3e8d671098de1fec9256e73`  
		Last Modified: Tue, 02 Sep 2025 01:07:25 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:16c1487ee25e15abee9aa27c20c3bc91b9fa4c99bab65e7a742963d60666def6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31072747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6792b8f84d3304ef6e28de08173b87ae23cf5b542ae198b8bd962bf5b29b4a40`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b0329cf2a4a15a9bf4b14570d09ca06b3b9b031182d9d673722455466dea4`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 3.6 MB (3598206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b2c6c73f48a5205154bbeefdc3a62200f2912abd347eab19218d25884b59c6`  
		Last Modified: Tue, 02 Sep 2025 02:31:43 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6dd113705bb44b0596d44cfd3ff0395aac0b756dc8da44d1563df648bedfe`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02baa23e0d6f84b6310f25f56d9459f98c61c4ae69864e811e3f6d95714f90`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 110.6 KB (110605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b579638f5ad784db8571cf092a6ef4ab30b240756a48f6c38c0e8dc718d7610d`  
		Last Modified: Tue, 02 Sep 2025 02:31:46 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf925a26094fa612cb22d55b1e64484fb6c1683525aa871d37fd1df276896a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c790b7b9e0fe69d544874fceaebe8f92b6265deaed73d3e8ed48cec56061cf7`

```dockerfile
```

-	Layers:
	-	`sha256:b956c6cf699422639abaacca5984085ebbe4ef744fc698f2bc3ef106bba50906`  
		Last Modified: Tue, 02 Sep 2025 04:07:28 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42e7b9a80bb3eb37d02c02dc8ae979642d01e3d3644d30077268d4519deff36`  
		Last Modified: Tue, 02 Sep 2025 04:07:29 GMT  
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
