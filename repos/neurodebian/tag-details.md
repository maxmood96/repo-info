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
$ docker pull neurodebian@sha256:91d03c12c24727945c18a1d0698d199518d9e0dc379cae634172bb617cbc1e81
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
$ docker pull neurodebian@sha256:51870411e6cfb59409d593f72a2355e59ace517258dd08dcca5fc19b04e12f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e74521593afa5574af921754ef044568d01babe316919d0227ce0ee2ef2ab3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbc9b299160c1db312e7b95d297e3a72795f0e0cd3629f99ec0b5d5074f482`  
		Last Modified: Wed, 11 Jun 2025 01:26:55 GMT  
		Size: 11.3 MB (11266798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b92ffb97d1ab74a8c03abd5bf067a7db8b6a98535222d4198d2aedd42e704`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9905efb8849d4ad84769703bb6462b7fca532c145a9f3a617ccae66f5cd8178`  
		Last Modified: Wed, 11 Jun 2025 00:04:22 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5bccddef1ea7c90a3f83a629491790fd61738f12e0b059ffe29fed6947dca`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 93.2 KB (93159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7302e39b4a84ec236cc63f200ce5cd12b25857b6860d8aa9b4f2c630839d6f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac74c06d4f5af96295d348e5b88a26551309b48c3fd3aef828768699b17b3778`

```dockerfile
```

-	Layers:
	-	`sha256:330ba10e15b4eb2d882fe878e073c41b4621dba90fcb4a15242608a79e5a0d55`  
		Last Modified: Wed, 11 Jun 2025 01:07:21 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57969539b0d4a6d56f45d33a21186e47a269fe3eda38459de47c1bec3c4b99e2`  
		Last Modified: Wed, 11 Jun 2025 01:07:22 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c57b2f6a3d83e008a8374833294d64d7ea020d3897f07d9f96a317dc6fd4991a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59666969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4bbfb7b8a510cd8c1e4a88806bae413f872423387041274881d9013419584c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5c2d6b1d7d5d28d02e2f2cac517a8cdde90e21e5a6e67277ee7cfaad9cb254`  
		Last Modified: Wed, 11 Jun 2025 03:31:13 GMT  
		Size: 11.2 MB (11232526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765bba7a7ecb589546d86353bd0d94577c74fca3b7a96a17b6372db8a4d46d17`  
		Last Modified: Wed, 11 Jun 2025 03:35:42 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bea4e39b1faf52aa6e75eed7c4e67851e88e15f1bad433741dee64f21654ac`  
		Last Modified: Wed, 11 Jun 2025 03:35:46 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ff130ee2030768ccbdde40e0b0cc38a55d68706e2e115ed72ce1951bcdbe8`  
		Last Modified: Wed, 11 Jun 2025 03:35:49 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4679137c067a99ee683dafb2ae9637e8d984373475ba2b9a1e53a0348dc51f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4551441a3b710c67f67d9cc1bbb001da8d9eae63a4fd372983e21d1130db4563`

```dockerfile
```

-	Layers:
	-	`sha256:07e4af5e11e836ec2abd0aadb072181bddbbfb39c26ca8b3637d8dbf44a467a5`  
		Last Modified: Wed, 11 Jun 2025 07:07:22 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c617b20fd66a64f64960a9acd7ef713f9b71c70e48a8da4d309e9a240261359b`  
		Last Modified: Wed, 11 Jun 2025 07:07:22 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:aed52e4c3cf784e520efd607e8de956432f1649765ad50445d121a3edc376564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61261796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49497c214bc44fcc564f62c485f1aa0ebfc134858d7316f94b89ac733c9191a2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cec3206abae9af7504c3ecc6fc1d7ad93234636734cfd15d6641ce1fd2ef19`  
		Last Modified: Tue, 10 Jun 2025 23:36:46 GMT  
		Size: 11.7 MB (11688919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367740ef16aaa69f189736ee3e947d62834ff67146519987e1bcbb86e6eef45`  
		Last Modified: Tue, 10 Jun 2025 23:36:41 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2a82ec3d2e8e2d3698f3fd68d39a22f2192cc781a4413841252b837f3c5c52`  
		Last Modified: Tue, 10 Jun 2025 23:36:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3adf80d23972c5a2315ba281040ac8889bc1cb52b4052b7d3533d1941ee436a`  
		Last Modified: Tue, 10 Jun 2025 23:36:42 GMT  
		Size: 93.2 KB (93232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:16ecefc0b3d1030c4e5e61a12393de7a5d30cd21667f71b9a8c0c1c8db03acc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3d9b8214b88c9677b119d3d04eb71b7b2042ef0890334ab265f462ec690e20`

```dockerfile
```

-	Layers:
	-	`sha256:a0a953cc95bb74bbc501c537cde161432dba83f9bc9fdf30642cbbff4589ccdf`  
		Last Modified: Wed, 11 Jun 2025 01:07:34 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54b0972fbc6c4a305521a5c2070dba0fd26c33d2cd58ea932189117f34493c3`  
		Last Modified: Wed, 11 Jun 2025 01:07:35 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:66a5f9f387c84d65fa609ccf2e6e8e31a49e5694e3c0e18e29ffd1cffc27fcf4
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
$ docker pull neurodebian@sha256:df6f98d131c4b4bf650a51a1c7cb8ed75f6b077109089524861bcda54b09d0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e761c4b19cc195da8d2855cb566359243e2c2282c9d400eb4c1e84760f913924`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09446529b39b6e747011c65127756ea8c59f2b0b9dc3096e7f48c5de96ccc8`  
		Last Modified: Tue, 10 Jun 2025 23:39:47 GMT  
		Size: 11.3 MB (11266854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301fc755d8ade11aeed0a053875ca7bec42da40cb0a5d13ecb4b84d6c554fc5f`  
		Last Modified: Wed, 11 Jun 2025 00:04:20 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0288b274dd2c371bfab2859b2d1cde4581488f737485247c84dce92e4d2b7747`  
		Last Modified: Wed, 11 Jun 2025 00:04:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88f0c71750a0635a612ed508c265aec03154a9a165ac80f4d16644bb162d486`  
		Last Modified: Wed, 11 Jun 2025 00:04:31 GMT  
		Size: 93.2 KB (93182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b082f19682f2b486a0c80b855625ac837ca40d6474e312afe94d9358a943e0d9`  
		Last Modified: Wed, 11 Jun 2025 00:04:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a59d18ee99e44947f8786dc60e2eda4f1ad2dcb9e52f80b9ff75f6f0503c7b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dcbea1c292a0676d2e7427bad68077d67903db9500a9c57e829f6c4376720f`

```dockerfile
```

-	Layers:
	-	`sha256:190e185693c59b487307682a32db421010423d06f2d8afc82e125fd629a46f57`  
		Last Modified: Wed, 11 Jun 2025 01:07:29 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7352e7a8c0e8bdeb2fbdde263e76d108e097cf91c47f04aaa19d2bbeea69cda6`  
		Last Modified: Wed, 11 Jun 2025 01:07:30 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3f66b6cf9c777c7ee2675df679b3664db8db5bffb63e5f8aae246ebe7a13d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9605c535fd80e79ed800f02eabdf96798a756d9383b1767f72ab8c2604a49ff6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5c2d6b1d7d5d28d02e2f2cac517a8cdde90e21e5a6e67277ee7cfaad9cb254`  
		Last Modified: Wed, 11 Jun 2025 03:31:13 GMT  
		Size: 11.2 MB (11232526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765bba7a7ecb589546d86353bd0d94577c74fca3b7a96a17b6372db8a4d46d17`  
		Last Modified: Wed, 11 Jun 2025 03:35:42 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bea4e39b1faf52aa6e75eed7c4e67851e88e15f1bad433741dee64f21654ac`  
		Last Modified: Wed, 11 Jun 2025 03:35:46 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ff130ee2030768ccbdde40e0b0cc38a55d68706e2e115ed72ce1951bcdbe8`  
		Last Modified: Wed, 11 Jun 2025 03:35:49 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e5c12cb63606f72ac2d02d6c4454a55351dfa3a9d77fce2e7399bc1258ca27`  
		Last Modified: Wed, 11 Jun 2025 03:36:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c7e6a86aef74f4f3a8d6d667f461e989cbfab19d40cb90e57c7c188e15892bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2ec0e9052301c0bd49a05f5e70e49b8526e1e401d45da2f01932619441a4ba`

```dockerfile
```

-	Layers:
	-	`sha256:e78e5536cfdbd3ebd739c041c46391bcd6f46539462a2d07c4f2a1a0fc4632a4`  
		Last Modified: Wed, 11 Jun 2025 07:07:27 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd6c977ee13182fafe5148ade423f1ec36b61c08ccfaf59c11afed6705becd4`  
		Last Modified: Wed, 11 Jun 2025 07:07:28 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bcef4e130e048631d0384f4d3a205fbd025912b2c22c4ddb4b379b316643f789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4925bc3778b6b9c6a745172c48b31f0867a1d496d392da2e5e6cdbafb8a59ae9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3e3e6e2d9340b30d10be9677d2a91088a9651305d3e2814d24858a5d1767d`  
		Last Modified: Tue, 10 Jun 2025 23:36:55 GMT  
		Size: 11.7 MB (11688864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d2ad000b61b2f234b9980ea545edacb02cbd88ee3f3f90bf6fe2daeadb805`  
		Last Modified: Tue, 10 Jun 2025 23:36:53 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2994203a98e1d20fa0b1dd98832c1f6f178640a9cf5f3b357e7fc2dae27c25aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4912929dd01f693d2d50ccabad470fdf08e88e1602d5cc27d7edc7d2de7f05`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 93.2 KB (93219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33efd2b24711ab06b45a10963b4b06e468a842e81d32c38d9e6b08cbd957171b`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff720c8e4f114b36fb3ba27756e87d0525c45d132bfcdec8b951db47adfb27e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78957fdb65a2c4183db08aa3428de96e661ea300304ac4527d7c61ef279719cc`

```dockerfile
```

-	Layers:
	-	`sha256:8f7c40befd41400cd338eee56f9ab359489ae226cb16cba8f1a7265fece184b7`  
		Last Modified: Wed, 11 Jun 2025 01:07:42 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b39234998b303494b07caf4110461e1fe5a4a40b9aa15d920f390887c601e67`  
		Last Modified: Wed, 11 Jun 2025 01:07:43 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:4c1fb15e678211ecc7f8cd0c87172a93c86b5a48990f6ecb852a059f327874d1
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
$ docker pull neurodebian@sha256:fa8d0e64ddf2c1f1524b59c687262eb2f390dffce21e35e655a09cde8c897585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93a0c67e1f5a7d1e6579a77a17cf0f61e311848eec5f0fef8948e5888ddd6ef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12161ce65f3f2f3d708a045c4fa86915abb98817b1d113b48df410dbd607979`  
		Last Modified: Tue, 10 Jun 2025 23:39:48 GMT  
		Size: 11.1 MB (11105046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84c78d6484fd08234d24ffd44b1cf75253482d44f61de3b4d732c1a875f0482`  
		Last Modified: Wed, 11 Jun 2025 00:04:43 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfd68787eaab78b42c559ed7924a86222fd0f360803250914a6e3c1273bce86`  
		Last Modified: Wed, 11 Jun 2025 00:04:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d48b5c4c76458905e76732ba51f0d84c7705618ac8fb3edeb54cac29cb7cd85`  
		Last Modified: Wed, 11 Jun 2025 00:04:49 GMT  
		Size: 101.2 KB (101220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7a662ddfd8f8e1115e6dde91224cab8e49b8a35e368a288dcc5d02bbfd3bda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1cba6ed4f2a462bef52d228bfe3d825f7d55944b76eadf532a001b7e97a6c4`

```dockerfile
```

-	Layers:
	-	`sha256:d0979e886eef455999223006e6d1e1b32a15df13b9a2977627e6c89d85995bac`  
		Last Modified: Wed, 11 Jun 2025 01:07:37 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d06cb507a902e6a58d9b540dfd6b4044211fe8adcda2c8c7f5aaaa3ef804e53`  
		Last Modified: Wed, 11 Jun 2025 01:07:38 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6226c5d1bbcdbcdc4bfd2a736a30090d07676fc9f5183fcb03747c3dd45d7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dc659fb58bd17842f2b2b0c03ff062761bdb5aa47446d67cce71e8088094ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3704fbfd86a89305a8a4d0556a88966db2c9ae3b7731e49335164c93b49ba182`  
		Last Modified: Wed, 11 Jun 2025 03:31:02 GMT  
		Size: 11.1 MB (11106051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bcb90956441591df9a1f5f32b74f21a6fc4b2efa523a109f5c567befc57d05`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d5133fe164372190e333a26acb1669673c83c44225e9c4bcd48cdc24788087`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473514cac34b3a0a9d0a408fb13bb9096b3c088423448884d4944cb5a73eecaa`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f47c60feb71e1a24026ac69a15c67138420dae31da3c6ff87cd0acfd6383b01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e77babfb6209d17309a5a4dfefbc6ccfcf22478fbb4127264d046b98b027c01`

```dockerfile
```

-	Layers:
	-	`sha256:fac044c3fa4a5f3cd2da938d094a023035b08124113a81a01dde2d020ee655db`  
		Last Modified: Wed, 11 Jun 2025 07:07:30 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff065860ec4dcc9bc48e62a6fe3836c570b1852f1ed47af72b56cc3f6a4ddc1`  
		Last Modified: Wed, 11 Jun 2025 07:07:31 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:e7246e0a58c8da6ac9c975db63e6584dc267ff91c2094271417bf61cd6baff14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55d1972e505207c201182536b8203b6addb6ba7474d3f976cf07b1f8d8dd81f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74216023682d3b31d84de0ebaeff59619d56684e8f5c8c4a19cf9794f79c8d50`  
		Last Modified: Tue, 10 Jun 2025 23:36:26 GMT  
		Size: 11.5 MB (11500388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954648ca4b374873e27c6cb4db5fcac429b6cdb75d89592ace61f69f58265d84`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c27a1b518834de55ce4678d5c5ef7a81d8de304747378c297306ab52c279f94`  
		Last Modified: Wed, 11 Jun 2025 00:04:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ff93ddced19b93a0a2b7ca0ff36215d59f37be24b4512a0752abbbca5355cb`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 101.1 KB (101085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b51d0516f8e8ec87176aa063c2397f6ac06e922b0d2c3973b10de1c41e1b2c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf6fd4a2d7d454aaf3ca63f0c8db6452e0b510c18c1d1b6ce8f12187deaddff`

```dockerfile
```

-	Layers:
	-	`sha256:b8a880c26a89691b0df62c5aa9d221f823f338c4bd2ced185abd430b56b1cbc1`  
		Last Modified: Wed, 11 Jun 2025 01:07:50 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a5f114021b4fa20ebe17faa78be8de615a0e049329eac6a9ae8cf6c037477b`  
		Last Modified: Wed, 11 Jun 2025 01:07:51 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:b568765dda1c8f75d89bfb487c2b63706f9ec53b4371511f73183eacba1af1b6
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
$ docker pull neurodebian@sha256:132037d5bed6afc85087f1c3bceaea5ab38dc0a60d67bb18be0e5e541296be59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361a62c5d109622bcccf51c35ecd19608bba94d901620b44f78e05b6c87782f3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b46c6d980b5d149bfb3561d336408e77938927cf8e6738b9917903de0a079`  
		Last Modified: Tue, 10 Jun 2025 23:39:33 GMT  
		Size: 11.1 MB (11105048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2f38841dc3a9f76babfe13bec1e7c8864b9e924c522990e82854b1322a104`  
		Last Modified: Tue, 10 Jun 2025 23:39:32 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ceb617bc148dcaeeb9c7a28476263870764f4a8ba9f67604bc6e954049765`  
		Last Modified: Tue, 10 Jun 2025 23:39:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2346e301d767c129000931705ab6d325b8df9c5f195e2b0f08f4178fe75df535`  
		Last Modified: Tue, 10 Jun 2025 23:39:33 GMT  
		Size: 101.2 KB (101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90b48568a2a7d2b4e906c4a6b3e2c96037735cb20e535eedf64701a81c4ddf`  
		Last Modified: Tue, 10 Jun 2025 23:39:33 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:45cd4fc83e2fc6d43a0619c2da0d8edc2f4b32a2d52c577f84de394647dca198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fe5af5b67fd5a1a06f71075baa3cd42be3d9fb211fa8e2b3708ec835a69efe`

```dockerfile
```

-	Layers:
	-	`sha256:1c7082a4068c6d2d69a870eadb5707dfdd23ddbb1d2b29b42488162eef611fdc`  
		Last Modified: Wed, 11 Jun 2025 01:07:43 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c9377c89b97c6a0e6690269150a432dd5d3548de6f2ded453b3668bb8b0bca5`  
		Last Modified: Wed, 11 Jun 2025 01:07:44 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:487eb6af1477b472784d8ff181842faa9554c439e8997e85d856da04addd518c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3817313674aec263c667c7c0375e41545695a0ab47e0d412e0f5682d3364587e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3704fbfd86a89305a8a4d0556a88966db2c9ae3b7731e49335164c93b49ba182`  
		Last Modified: Wed, 11 Jun 2025 03:31:02 GMT  
		Size: 11.1 MB (11106051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bcb90956441591df9a1f5f32b74f21a6fc4b2efa523a109f5c567befc57d05`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d5133fe164372190e333a26acb1669673c83c44225e9c4bcd48cdc24788087`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473514cac34b3a0a9d0a408fb13bb9096b3c088423448884d4944cb5a73eecaa`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0188df129a5bf05e4b7d7533b4024832da46a201a61f52c17a0cf7d680e65239`  
		Last Modified: Wed, 11 Jun 2025 03:31:12 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a76706f966dc23953b81d64372eb98fe5052592f72e6e09b34695ccda17de03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61429672d72dd0b5732c11f9dc1438caa35574e43a6edb429b227ff111c4220`

```dockerfile
```

-	Layers:
	-	`sha256:1892fd921897d803750a68fa30929929b8dcb565c5e16832c11bc194850efcb9`  
		Last Modified: Wed, 11 Jun 2025 07:07:35 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b4ae33e10e8f64c34ada68d09ac7e25acbbfb8fafab8622bd0f9e79dacdb5d`  
		Last Modified: Wed, 11 Jun 2025 07:07:36 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:dab444ff3f8407e3d4de6e7464a4655ad875790900a34472f880d4e134da8956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c818ad8397b6c6f378b2abd3ddb05d8383ecf0f90ba3ae27456b4481924dbd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1090fea6e28262114514910f5324244b4e2120957a41ba4d90e810aa74026514`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 11.5 MB (11500323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2ca97cb02bfd5ce55cc8e7b0881b53d52e5f1d615486d799f6b98d796664ed`  
		Last Modified: Tue, 10 Jun 2025 23:36:42 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3de78fa3225601752ce238073a7a0ff14b28dfff3036bec8c45136582470c15`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ff5cb26b6544c857ea46597104ed49ec345e4f0d63ce5f67b479e813655a2`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 101.1 KB (101068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ced5d9c6980068de9c52da53fdd251cf15cb35439dcaa512d524e8f77d89107`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14b2a64479b6355d09d583b6c1972e5e67c6a0015dd49abed2d79161f5ea7749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964b7a6b0460dd581363d59d30987506200c3259cff7790f5317421e7a75d8c`

```dockerfile
```

-	Layers:
	-	`sha256:0954b888fba7569ad3f903df83458b3b1aca940dab61ad44ce1bef0f6fac2d2e`  
		Last Modified: Wed, 11 Jun 2025 01:07:55 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d416508ddb3b5096d6394d1850a38a6240edaee7625ef49cb254b80a5114d4a2`  
		Last Modified: Wed, 11 Jun 2025 01:07:56 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:a62ad433a27fe25a8de7f951e4212508ae8d406477c0b32dc47385b9799a5f1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:5c6093825b977242a0c5ce777463f22291467f3213ee9967d63ad853cad62b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0159f21b56dd611102fd38c93c9b9db6747ecff96ad393e3a308e6b9a27338be`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaae9adeb5784f217b1fccbfde587bde5f5a4eef001092646b8beb2b6083091`  
		Last Modified: Tue, 03 Jun 2025 15:33:13 GMT  
		Size: 3.6 MB (3624137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13bc798486b3ed6c830d97b2bbead94f4fba215db043fa3784384ab67490f7b`  
		Last Modified: Tue, 03 Jun 2025 15:33:12 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5403824352add24fb2c4ff3c15449271afc3ecff86b4c3ceaee1884051b6b38b`  
		Last Modified: Tue, 03 Jun 2025 15:33:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8cf2c0a6fd0753dac46ff04bd86d6df6b583a2e5e3255cf4a0a914a7af892`  
		Last Modified: Tue, 03 Jun 2025 15:33:14 GMT  
		Size: 110.6 KB (110554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cc4e8e5db5c9f889fe8af12a7c454a321cafb97ce2f6eb5726d0cf2334a61d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2094402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa173a2f1b0551b0755668bd7412967e18454e29d78df0e7fdc4eb9697d84f3`

```dockerfile
```

-	Layers:
	-	`sha256:d5df8adfd2250d8e942803d58a02b3042f130a0b08a3032e2f92fe6ebc663de0`  
		Last Modified: Tue, 10 Jun 2025 04:00:56 GMT  
		Size: 2.1 MB (2080426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8db84911c2b9570d62209aca26a6603452311f1d2675ca00a4d45b6e0e0e45`  
		Last Modified: Tue, 10 Jun 2025 04:18:45 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9d73162a14eddeaa42de80b66ebb46ce4058a34b7e8f278ebe76b01bdfe8218c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31063851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6641bfdb2031f8162a237d8747ec26d21147022b969270ac106464d19f1c9cd1`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Wed, 04 Jun 2025 23:53:21 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Wed, 04 Jun 2025 23:46:33 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Wed, 04 Jun 2025 23:58:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Wed, 04 Jun 2025 23:45:32 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e930d912712ee307694bc8edc2665e13ab5ffabd52de3c434ea3e9debd56da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2094787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da916fbb9e734f060ad2c0386b3dde6822474e043cccbcb4c4b5700a6eeeeb05`

```dockerfile
```

-	Layers:
	-	`sha256:55487635e34c1575a1c86ad1538db4eae8185f9b358bc3b2647c7b10c50a9639`  
		Last Modified: Tue, 10 Jun 2025 03:58:21 GMT  
		Size: 2.1 MB (2080686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6afd8ad60b0744690a9d8df1fdde507192154666dd867a3ca02ad6d8a4e9430`  
		Last Modified: Tue, 10 Jun 2025 03:59:20 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:7481cf83e704b3af7a5b48b3edcdaa6c8359604a90aee37431c2027bc8d9f36a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:106a157335593089bd9167471a43ac4e4a300c21bca0dfac7ab5e8ca330e11b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c425b94e9e05e94a3588a5ed5fa50798b770c5964ee80eb3108e2c2b854734`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833f05bf4a56287336922533369cb272b043579abea2c4588fb7a28586dccbb7`  
		Last Modified: Tue, 03 Jun 2025 17:31:23 GMT  
		Size: 3.6 MB (3624096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5f30655f789d9aaabd83e43e19fd42000e70a6d62d06ddf046576bfb3eb56`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b76c5daef076a6ef3131ece85a9ede4b5366f8b35563943c61f3ca36393de48`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b346a922dadb495203fa86390fce5ab7f4746b373ff8ee37ae89b1570fab89`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
		Size: 110.6 KB (110563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96bb241c37c54f5099c6ee4be792e3df22a12f314a81846062a58b160223e7a`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8aae46358cf11c3d67fb2b0bf9adbc7de24122f7bcae1bfe2c595b1a62233e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2096668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14479c1656b173c0100892f3c715ee08d6396fbbddd70f0eb6c7d400c28dc177`

```dockerfile
```

-	Layers:
	-	`sha256:1e817e7f07a5533079454f7b46be380fb1a89f65ee260bfd9d08395ebf6e86fa`  
		Last Modified: Tue, 10 Jun 2025 05:11:03 GMT  
		Size: 2.1 MB (2080462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb30aac33316b47ec98bca470a0a0a66269cdd7aa22f62d98e749d5c5e1c494`  
		Last Modified: Tue, 10 Jun 2025 05:12:32 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f069651f05d3e6c7a096a41a3242a53b7f5067e15c35b139bc0844d2c622254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b33835d3e532c457a861b46b17a2ecc210b0019baeec6bf4b85319109ae9d0`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Wed, 04 Jun 2025 23:53:21 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Wed, 04 Jun 2025 23:46:33 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Wed, 04 Jun 2025 23:58:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Wed, 04 Jun 2025 23:45:32 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc12a5156209348208485de93d3b89460edf23f23fdded16678f39a46448c25`  
		Last Modified: Wed, 04 Jun 2025 23:46:15 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2fb96a9daec1ce2a7e9ea4dd1144aa633c2bc1d97d73ba0bece51586ec46fc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2097068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25ae2c3ba2f40b6fa187203997315827f50c3c023a8f4ce4137f6b8994a5c1`

```dockerfile
```

-	Layers:
	-	`sha256:f8f474f858ffefa2d71ad93a00640e481fbbfd9d23b677cb8ee70750c1123694`  
		Last Modified: Tue, 10 Jun 2025 05:10:23 GMT  
		Size: 2.1 MB (2080722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09220ec00b43fe2a6638b49308e372f11987cceec9eefdf11f6781cec1b7a417`  
		Last Modified: Tue, 10 Jun 2025 05:09:48 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:91d03c12c24727945c18a1d0698d199518d9e0dc379cae634172bb617cbc1e81
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
$ docker pull neurodebian@sha256:51870411e6cfb59409d593f72a2355e59ace517258dd08dcca5fc19b04e12f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e74521593afa5574af921754ef044568d01babe316919d0227ce0ee2ef2ab3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbc9b299160c1db312e7b95d297e3a72795f0e0cd3629f99ec0b5d5074f482`  
		Last Modified: Wed, 11 Jun 2025 01:26:55 GMT  
		Size: 11.3 MB (11266798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b92ffb97d1ab74a8c03abd5bf067a7db8b6a98535222d4198d2aedd42e704`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9905efb8849d4ad84769703bb6462b7fca532c145a9f3a617ccae66f5cd8178`  
		Last Modified: Wed, 11 Jun 2025 00:04:22 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5bccddef1ea7c90a3f83a629491790fd61738f12e0b059ffe29fed6947dca`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 93.2 KB (93159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7302e39b4a84ec236cc63f200ce5cd12b25857b6860d8aa9b4f2c630839d6f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac74c06d4f5af96295d348e5b88a26551309b48c3fd3aef828768699b17b3778`

```dockerfile
```

-	Layers:
	-	`sha256:330ba10e15b4eb2d882fe878e073c41b4621dba90fcb4a15242608a79e5a0d55`  
		Last Modified: Wed, 11 Jun 2025 01:07:21 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57969539b0d4a6d56f45d33a21186e47a269fe3eda38459de47c1bec3c4b99e2`  
		Last Modified: Wed, 11 Jun 2025 01:07:22 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c57b2f6a3d83e008a8374833294d64d7ea020d3897f07d9f96a317dc6fd4991a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59666969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4bbfb7b8a510cd8c1e4a88806bae413f872423387041274881d9013419584c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5c2d6b1d7d5d28d02e2f2cac517a8cdde90e21e5a6e67277ee7cfaad9cb254`  
		Last Modified: Wed, 11 Jun 2025 03:31:13 GMT  
		Size: 11.2 MB (11232526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765bba7a7ecb589546d86353bd0d94577c74fca3b7a96a17b6372db8a4d46d17`  
		Last Modified: Wed, 11 Jun 2025 03:35:42 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bea4e39b1faf52aa6e75eed7c4e67851e88e15f1bad433741dee64f21654ac`  
		Last Modified: Wed, 11 Jun 2025 03:35:46 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ff130ee2030768ccbdde40e0b0cc38a55d68706e2e115ed72ce1951bcdbe8`  
		Last Modified: Wed, 11 Jun 2025 03:35:49 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4679137c067a99ee683dafb2ae9637e8d984373475ba2b9a1e53a0348dc51f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4551441a3b710c67f67d9cc1bbb001da8d9eae63a4fd372983e21d1130db4563`

```dockerfile
```

-	Layers:
	-	`sha256:07e4af5e11e836ec2abd0aadb072181bddbbfb39c26ca8b3637d8dbf44a467a5`  
		Last Modified: Wed, 11 Jun 2025 07:07:22 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c617b20fd66a64f64960a9acd7ef713f9b71c70e48a8da4d309e9a240261359b`  
		Last Modified: Wed, 11 Jun 2025 07:07:22 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:aed52e4c3cf784e520efd607e8de956432f1649765ad50445d121a3edc376564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61261796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49497c214bc44fcc564f62c485f1aa0ebfc134858d7316f94b89ac733c9191a2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cec3206abae9af7504c3ecc6fc1d7ad93234636734cfd15d6641ce1fd2ef19`  
		Last Modified: Tue, 10 Jun 2025 23:36:46 GMT  
		Size: 11.7 MB (11688919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367740ef16aaa69f189736ee3e947d62834ff67146519987e1bcbb86e6eef45`  
		Last Modified: Tue, 10 Jun 2025 23:36:41 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2a82ec3d2e8e2d3698f3fd68d39a22f2192cc781a4413841252b837f3c5c52`  
		Last Modified: Tue, 10 Jun 2025 23:36:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3adf80d23972c5a2315ba281040ac8889bc1cb52b4052b7d3533d1941ee436a`  
		Last Modified: Tue, 10 Jun 2025 23:36:42 GMT  
		Size: 93.2 KB (93232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:16ecefc0b3d1030c4e5e61a12393de7a5d30cd21667f71b9a8c0c1c8db03acc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3d9b8214b88c9677b119d3d04eb71b7b2042ef0890334ab265f462ec690e20`

```dockerfile
```

-	Layers:
	-	`sha256:a0a953cc95bb74bbc501c537cde161432dba83f9bc9fdf30642cbbff4589ccdf`  
		Last Modified: Wed, 11 Jun 2025 01:07:34 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54b0972fbc6c4a305521a5c2070dba0fd26c33d2cd58ea932189117f34493c3`  
		Last Modified: Wed, 11 Jun 2025 01:07:35 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:4c1fb15e678211ecc7f8cd0c87172a93c86b5a48990f6ecb852a059f327874d1
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
$ docker pull neurodebian@sha256:fa8d0e64ddf2c1f1524b59c687262eb2f390dffce21e35e655a09cde8c897585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93a0c67e1f5a7d1e6579a77a17cf0f61e311848eec5f0fef8948e5888ddd6ef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12161ce65f3f2f3d708a045c4fa86915abb98817b1d113b48df410dbd607979`  
		Last Modified: Tue, 10 Jun 2025 23:39:48 GMT  
		Size: 11.1 MB (11105046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84c78d6484fd08234d24ffd44b1cf75253482d44f61de3b4d732c1a875f0482`  
		Last Modified: Wed, 11 Jun 2025 00:04:43 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfd68787eaab78b42c559ed7924a86222fd0f360803250914a6e3c1273bce86`  
		Last Modified: Wed, 11 Jun 2025 00:04:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d48b5c4c76458905e76732ba51f0d84c7705618ac8fb3edeb54cac29cb7cd85`  
		Last Modified: Wed, 11 Jun 2025 00:04:49 GMT  
		Size: 101.2 KB (101220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7a662ddfd8f8e1115e6dde91224cab8e49b8a35e368a288dcc5d02bbfd3bda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1cba6ed4f2a462bef52d228bfe3d825f7d55944b76eadf532a001b7e97a6c4`

```dockerfile
```

-	Layers:
	-	`sha256:d0979e886eef455999223006e6d1e1b32a15df13b9a2977627e6c89d85995bac`  
		Last Modified: Wed, 11 Jun 2025 01:07:37 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d06cb507a902e6a58d9b540dfd6b4044211fe8adcda2c8c7f5aaaa3ef804e53`  
		Last Modified: Wed, 11 Jun 2025 01:07:38 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6226c5d1bbcdbcdc4bfd2a736a30090d07676fc9f5183fcb03747c3dd45d7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dc659fb58bd17842f2b2b0c03ff062761bdb5aa47446d67cce71e8088094ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3704fbfd86a89305a8a4d0556a88966db2c9ae3b7731e49335164c93b49ba182`  
		Last Modified: Wed, 11 Jun 2025 03:31:02 GMT  
		Size: 11.1 MB (11106051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bcb90956441591df9a1f5f32b74f21a6fc4b2efa523a109f5c567befc57d05`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d5133fe164372190e333a26acb1669673c83c44225e9c4bcd48cdc24788087`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473514cac34b3a0a9d0a408fb13bb9096b3c088423448884d4944cb5a73eecaa`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f47c60feb71e1a24026ac69a15c67138420dae31da3c6ff87cd0acfd6383b01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e77babfb6209d17309a5a4dfefbc6ccfcf22478fbb4127264d046b98b027c01`

```dockerfile
```

-	Layers:
	-	`sha256:fac044c3fa4a5f3cd2da938d094a023035b08124113a81a01dde2d020ee655db`  
		Last Modified: Wed, 11 Jun 2025 07:07:30 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff065860ec4dcc9bc48e62a6fe3836c570b1852f1ed47af72b56cc3f6a4ddc1`  
		Last Modified: Wed, 11 Jun 2025 07:07:31 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:e7246e0a58c8da6ac9c975db63e6584dc267ff91c2094271417bf61cd6baff14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55d1972e505207c201182536b8203b6addb6ba7474d3f976cf07b1f8d8dd81f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74216023682d3b31d84de0ebaeff59619d56684e8f5c8c4a19cf9794f79c8d50`  
		Last Modified: Tue, 10 Jun 2025 23:36:26 GMT  
		Size: 11.5 MB (11500388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954648ca4b374873e27c6cb4db5fcac429b6cdb75d89592ace61f69f58265d84`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c27a1b518834de55ce4678d5c5ef7a81d8de304747378c297306ab52c279f94`  
		Last Modified: Wed, 11 Jun 2025 00:04:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ff93ddced19b93a0a2b7ca0ff36215d59f37be24b4512a0752abbbca5355cb`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 101.1 KB (101085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b51d0516f8e8ec87176aa063c2397f6ac06e922b0d2c3973b10de1c41e1b2c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf6fd4a2d7d454aaf3ca63f0c8db6452e0b510c18c1d1b6ce8f12187deaddff`

```dockerfile
```

-	Layers:
	-	`sha256:b8a880c26a89691b0df62c5aa9d221f823f338c4bd2ced185abd430b56b1cbc1`  
		Last Modified: Wed, 11 Jun 2025 01:07:50 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a5f114021b4fa20ebe17faa78be8de615a0e049329eac6a9ae8cf6c037477b`  
		Last Modified: Wed, 11 Jun 2025 01:07:51 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:b568765dda1c8f75d89bfb487c2b63706f9ec53b4371511f73183eacba1af1b6
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
$ docker pull neurodebian@sha256:132037d5bed6afc85087f1c3bceaea5ab38dc0a60d67bb18be0e5e541296be59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361a62c5d109622bcccf51c35ecd19608bba94d901620b44f78e05b6c87782f3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b46c6d980b5d149bfb3561d336408e77938927cf8e6738b9917903de0a079`  
		Last Modified: Tue, 10 Jun 2025 23:39:33 GMT  
		Size: 11.1 MB (11105048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2f38841dc3a9f76babfe13bec1e7c8864b9e924c522990e82854b1322a104`  
		Last Modified: Tue, 10 Jun 2025 23:39:32 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ceb617bc148dcaeeb9c7a28476263870764f4a8ba9f67604bc6e954049765`  
		Last Modified: Tue, 10 Jun 2025 23:39:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2346e301d767c129000931705ab6d325b8df9c5f195e2b0f08f4178fe75df535`  
		Last Modified: Tue, 10 Jun 2025 23:39:33 GMT  
		Size: 101.2 KB (101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90b48568a2a7d2b4e906c4a6b3e2c96037735cb20e535eedf64701a81c4ddf`  
		Last Modified: Tue, 10 Jun 2025 23:39:33 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:45cd4fc83e2fc6d43a0619c2da0d8edc2f4b32a2d52c577f84de394647dca198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fe5af5b67fd5a1a06f71075baa3cd42be3d9fb211fa8e2b3708ec835a69efe`

```dockerfile
```

-	Layers:
	-	`sha256:1c7082a4068c6d2d69a870eadb5707dfdd23ddbb1d2b29b42488162eef611fdc`  
		Last Modified: Wed, 11 Jun 2025 01:07:43 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c9377c89b97c6a0e6690269150a432dd5d3548de6f2ded453b3668bb8b0bca5`  
		Last Modified: Wed, 11 Jun 2025 01:07:44 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:487eb6af1477b472784d8ff181842faa9554c439e8997e85d856da04addd518c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3817313674aec263c667c7c0375e41545695a0ab47e0d412e0f5682d3364587e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3704fbfd86a89305a8a4d0556a88966db2c9ae3b7731e49335164c93b49ba182`  
		Last Modified: Wed, 11 Jun 2025 03:31:02 GMT  
		Size: 11.1 MB (11106051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bcb90956441591df9a1f5f32b74f21a6fc4b2efa523a109f5c567befc57d05`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d5133fe164372190e333a26acb1669673c83c44225e9c4bcd48cdc24788087`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473514cac34b3a0a9d0a408fb13bb9096b3c088423448884d4944cb5a73eecaa`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0188df129a5bf05e4b7d7533b4024832da46a201a61f52c17a0cf7d680e65239`  
		Last Modified: Wed, 11 Jun 2025 03:31:12 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a76706f966dc23953b81d64372eb98fe5052592f72e6e09b34695ccda17de03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61429672d72dd0b5732c11f9dc1438caa35574e43a6edb429b227ff111c4220`

```dockerfile
```

-	Layers:
	-	`sha256:1892fd921897d803750a68fa30929929b8dcb565c5e16832c11bc194850efcb9`  
		Last Modified: Wed, 11 Jun 2025 07:07:35 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b4ae33e10e8f64c34ada68d09ac7e25acbbfb8fafab8622bd0f9e79dacdb5d`  
		Last Modified: Wed, 11 Jun 2025 07:07:36 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:dab444ff3f8407e3d4de6e7464a4655ad875790900a34472f880d4e134da8956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c818ad8397b6c6f378b2abd3ddb05d8383ecf0f90ba3ae27456b4481924dbd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1090fea6e28262114514910f5324244b4e2120957a41ba4d90e810aa74026514`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 11.5 MB (11500323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2ca97cb02bfd5ce55cc8e7b0881b53d52e5f1d615486d799f6b98d796664ed`  
		Last Modified: Tue, 10 Jun 2025 23:36:42 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3de78fa3225601752ce238073a7a0ff14b28dfff3036bec8c45136582470c15`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ff5cb26b6544c857ea46597104ed49ec345e4f0d63ce5f67b479e813655a2`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 101.1 KB (101068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ced5d9c6980068de9c52da53fdd251cf15cb35439dcaa512d524e8f77d89107`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14b2a64479b6355d09d583b6c1972e5e67c6a0015dd49abed2d79161f5ea7749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964b7a6b0460dd581363d59d30987506200c3259cff7790f5317421e7a75d8c`

```dockerfile
```

-	Layers:
	-	`sha256:0954b888fba7569ad3f903df83458b3b1aca940dab61ad44ce1bef0f6fac2d2e`  
		Last Modified: Wed, 11 Jun 2025 01:07:55 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d416508ddb3b5096d6394d1850a38a6240edaee7625ef49cb254b80a5114d4a2`  
		Last Modified: Wed, 11 Jun 2025 01:07:56 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:91d03c12c24727945c18a1d0698d199518d9e0dc379cae634172bb617cbc1e81
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
$ docker pull neurodebian@sha256:51870411e6cfb59409d593f72a2355e59ace517258dd08dcca5fc19b04e12f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e74521593afa5574af921754ef044568d01babe316919d0227ce0ee2ef2ab3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbc9b299160c1db312e7b95d297e3a72795f0e0cd3629f99ec0b5d5074f482`  
		Last Modified: Wed, 11 Jun 2025 01:26:55 GMT  
		Size: 11.3 MB (11266798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b92ffb97d1ab74a8c03abd5bf067a7db8b6a98535222d4198d2aedd42e704`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9905efb8849d4ad84769703bb6462b7fca532c145a9f3a617ccae66f5cd8178`  
		Last Modified: Wed, 11 Jun 2025 00:04:22 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5bccddef1ea7c90a3f83a629491790fd61738f12e0b059ffe29fed6947dca`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 93.2 KB (93159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7302e39b4a84ec236cc63f200ce5cd12b25857b6860d8aa9b4f2c630839d6f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac74c06d4f5af96295d348e5b88a26551309b48c3fd3aef828768699b17b3778`

```dockerfile
```

-	Layers:
	-	`sha256:330ba10e15b4eb2d882fe878e073c41b4621dba90fcb4a15242608a79e5a0d55`  
		Last Modified: Wed, 11 Jun 2025 01:07:21 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57969539b0d4a6d56f45d33a21186e47a269fe3eda38459de47c1bec3c4b99e2`  
		Last Modified: Wed, 11 Jun 2025 01:07:22 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c57b2f6a3d83e008a8374833294d64d7ea020d3897f07d9f96a317dc6fd4991a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59666969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4bbfb7b8a510cd8c1e4a88806bae413f872423387041274881d9013419584c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5c2d6b1d7d5d28d02e2f2cac517a8cdde90e21e5a6e67277ee7cfaad9cb254`  
		Last Modified: Wed, 11 Jun 2025 03:31:13 GMT  
		Size: 11.2 MB (11232526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765bba7a7ecb589546d86353bd0d94577c74fca3b7a96a17b6372db8a4d46d17`  
		Last Modified: Wed, 11 Jun 2025 03:35:42 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bea4e39b1faf52aa6e75eed7c4e67851e88e15f1bad433741dee64f21654ac`  
		Last Modified: Wed, 11 Jun 2025 03:35:46 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ff130ee2030768ccbdde40e0b0cc38a55d68706e2e115ed72ce1951bcdbe8`  
		Last Modified: Wed, 11 Jun 2025 03:35:49 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4679137c067a99ee683dafb2ae9637e8d984373475ba2b9a1e53a0348dc51f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4551441a3b710c67f67d9cc1bbb001da8d9eae63a4fd372983e21d1130db4563`

```dockerfile
```

-	Layers:
	-	`sha256:07e4af5e11e836ec2abd0aadb072181bddbbfb39c26ca8b3637d8dbf44a467a5`  
		Last Modified: Wed, 11 Jun 2025 07:07:22 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c617b20fd66a64f64960a9acd7ef713f9b71c70e48a8da4d309e9a240261359b`  
		Last Modified: Wed, 11 Jun 2025 07:07:22 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:aed52e4c3cf784e520efd607e8de956432f1649765ad50445d121a3edc376564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61261796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49497c214bc44fcc564f62c485f1aa0ebfc134858d7316f94b89ac733c9191a2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cec3206abae9af7504c3ecc6fc1d7ad93234636734cfd15d6641ce1fd2ef19`  
		Last Modified: Tue, 10 Jun 2025 23:36:46 GMT  
		Size: 11.7 MB (11688919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367740ef16aaa69f189736ee3e947d62834ff67146519987e1bcbb86e6eef45`  
		Last Modified: Tue, 10 Jun 2025 23:36:41 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2a82ec3d2e8e2d3698f3fd68d39a22f2192cc781a4413841252b837f3c5c52`  
		Last Modified: Tue, 10 Jun 2025 23:36:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3adf80d23972c5a2315ba281040ac8889bc1cb52b4052b7d3533d1941ee436a`  
		Last Modified: Tue, 10 Jun 2025 23:36:42 GMT  
		Size: 93.2 KB (93232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:16ecefc0b3d1030c4e5e61a12393de7a5d30cd21667f71b9a8c0c1c8db03acc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3d9b8214b88c9677b119d3d04eb71b7b2042ef0890334ab265f462ec690e20`

```dockerfile
```

-	Layers:
	-	`sha256:a0a953cc95bb74bbc501c537cde161432dba83f9bc9fdf30642cbbff4589ccdf`  
		Last Modified: Wed, 11 Jun 2025 01:07:34 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54b0972fbc6c4a305521a5c2070dba0fd26c33d2cd58ea932189117f34493c3`  
		Last Modified: Wed, 11 Jun 2025 01:07:35 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:66a5f9f387c84d65fa609ccf2e6e8e31a49e5694e3c0e18e29ffd1cffc27fcf4
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
$ docker pull neurodebian@sha256:df6f98d131c4b4bf650a51a1c7cb8ed75f6b077109089524861bcda54b09d0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e761c4b19cc195da8d2855cb566359243e2c2282c9d400eb4c1e84760f913924`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09446529b39b6e747011c65127756ea8c59f2b0b9dc3096e7f48c5de96ccc8`  
		Last Modified: Tue, 10 Jun 2025 23:39:47 GMT  
		Size: 11.3 MB (11266854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301fc755d8ade11aeed0a053875ca7bec42da40cb0a5d13ecb4b84d6c554fc5f`  
		Last Modified: Wed, 11 Jun 2025 00:04:20 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0288b274dd2c371bfab2859b2d1cde4581488f737485247c84dce92e4d2b7747`  
		Last Modified: Wed, 11 Jun 2025 00:04:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88f0c71750a0635a612ed508c265aec03154a9a165ac80f4d16644bb162d486`  
		Last Modified: Wed, 11 Jun 2025 00:04:31 GMT  
		Size: 93.2 KB (93182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b082f19682f2b486a0c80b855625ac837ca40d6474e312afe94d9358a943e0d9`  
		Last Modified: Wed, 11 Jun 2025 00:04:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a59d18ee99e44947f8786dc60e2eda4f1ad2dcb9e52f80b9ff75f6f0503c7b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dcbea1c292a0676d2e7427bad68077d67903db9500a9c57e829f6c4376720f`

```dockerfile
```

-	Layers:
	-	`sha256:190e185693c59b487307682a32db421010423d06f2d8afc82e125fd629a46f57`  
		Last Modified: Wed, 11 Jun 2025 01:07:29 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7352e7a8c0e8bdeb2fbdde263e76d108e097cf91c47f04aaa19d2bbeea69cda6`  
		Last Modified: Wed, 11 Jun 2025 01:07:30 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3f66b6cf9c777c7ee2675df679b3664db8db5bffb63e5f8aae246ebe7a13d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9605c535fd80e79ed800f02eabdf96798a756d9383b1767f72ab8c2604a49ff6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5c2d6b1d7d5d28d02e2f2cac517a8cdde90e21e5a6e67277ee7cfaad9cb254`  
		Last Modified: Wed, 11 Jun 2025 03:31:13 GMT  
		Size: 11.2 MB (11232526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765bba7a7ecb589546d86353bd0d94577c74fca3b7a96a17b6372db8a4d46d17`  
		Last Modified: Wed, 11 Jun 2025 03:35:42 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bea4e39b1faf52aa6e75eed7c4e67851e88e15f1bad433741dee64f21654ac`  
		Last Modified: Wed, 11 Jun 2025 03:35:46 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ff130ee2030768ccbdde40e0b0cc38a55d68706e2e115ed72ce1951bcdbe8`  
		Last Modified: Wed, 11 Jun 2025 03:35:49 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e5c12cb63606f72ac2d02d6c4454a55351dfa3a9d77fce2e7399bc1258ca27`  
		Last Modified: Wed, 11 Jun 2025 03:36:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c7e6a86aef74f4f3a8d6d667f461e989cbfab19d40cb90e57c7c188e15892bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2ec0e9052301c0bd49a05f5e70e49b8526e1e401d45da2f01932619441a4ba`

```dockerfile
```

-	Layers:
	-	`sha256:e78e5536cfdbd3ebd739c041c46391bcd6f46539462a2d07c4f2a1a0fc4632a4`  
		Last Modified: Wed, 11 Jun 2025 07:07:27 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd6c977ee13182fafe5148ade423f1ec36b61c08ccfaf59c11afed6705becd4`  
		Last Modified: Wed, 11 Jun 2025 07:07:28 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bcef4e130e048631d0384f4d3a205fbd025912b2c22c4ddb4b379b316643f789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4925bc3778b6b9c6a745172c48b31f0867a1d496d392da2e5e6cdbafb8a59ae9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3e3e6e2d9340b30d10be9677d2a91088a9651305d3e2814d24858a5d1767d`  
		Last Modified: Tue, 10 Jun 2025 23:36:55 GMT  
		Size: 11.7 MB (11688864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d2ad000b61b2f234b9980ea545edacb02cbd88ee3f3f90bf6fe2daeadb805`  
		Last Modified: Tue, 10 Jun 2025 23:36:53 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2994203a98e1d20fa0b1dd98832c1f6f178640a9cf5f3b357e7fc2dae27c25aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4912929dd01f693d2d50ccabad470fdf08e88e1602d5cc27d7edc7d2de7f05`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 93.2 KB (93219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33efd2b24711ab06b45a10963b4b06e468a842e81d32c38d9e6b08cbd957171b`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff720c8e4f114b36fb3ba27756e87d0525c45d132bfcdec8b951db47adfb27e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78957fdb65a2c4183db08aa3428de96e661ea300304ac4527d7c61ef279719cc`

```dockerfile
```

-	Layers:
	-	`sha256:8f7c40befd41400cd338eee56f9ab359489ae226cb16cba8f1a7265fece184b7`  
		Last Modified: Wed, 11 Jun 2025 01:07:42 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b39234998b303494b07caf4110461e1fe5a4a40b9aa15d920f390887c601e67`  
		Last Modified: Wed, 11 Jun 2025 01:07:43 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:a62ad433a27fe25a8de7f951e4212508ae8d406477c0b32dc47385b9799a5f1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:5c6093825b977242a0c5ce777463f22291467f3213ee9967d63ad853cad62b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0159f21b56dd611102fd38c93c9b9db6747ecff96ad393e3a308e6b9a27338be`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaae9adeb5784f217b1fccbfde587bde5f5a4eef001092646b8beb2b6083091`  
		Last Modified: Tue, 03 Jun 2025 15:33:13 GMT  
		Size: 3.6 MB (3624137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13bc798486b3ed6c830d97b2bbead94f4fba215db043fa3784384ab67490f7b`  
		Last Modified: Tue, 03 Jun 2025 15:33:12 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5403824352add24fb2c4ff3c15449271afc3ecff86b4c3ceaee1884051b6b38b`  
		Last Modified: Tue, 03 Jun 2025 15:33:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8cf2c0a6fd0753dac46ff04bd86d6df6b583a2e5e3255cf4a0a914a7af892`  
		Last Modified: Tue, 03 Jun 2025 15:33:14 GMT  
		Size: 110.6 KB (110554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cc4e8e5db5c9f889fe8af12a7c454a321cafb97ce2f6eb5726d0cf2334a61d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2094402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa173a2f1b0551b0755668bd7412967e18454e29d78df0e7fdc4eb9697d84f3`

```dockerfile
```

-	Layers:
	-	`sha256:d5df8adfd2250d8e942803d58a02b3042f130a0b08a3032e2f92fe6ebc663de0`  
		Last Modified: Tue, 10 Jun 2025 04:00:56 GMT  
		Size: 2.1 MB (2080426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8db84911c2b9570d62209aca26a6603452311f1d2675ca00a4d45b6e0e0e45`  
		Last Modified: Tue, 10 Jun 2025 04:18:45 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9d73162a14eddeaa42de80b66ebb46ce4058a34b7e8f278ebe76b01bdfe8218c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31063851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6641bfdb2031f8162a237d8747ec26d21147022b969270ac106464d19f1c9cd1`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Wed, 04 Jun 2025 23:53:21 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Wed, 04 Jun 2025 23:46:33 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Wed, 04 Jun 2025 23:58:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Wed, 04 Jun 2025 23:45:32 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e930d912712ee307694bc8edc2665e13ab5ffabd52de3c434ea3e9debd56da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2094787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da916fbb9e734f060ad2c0386b3dde6822474e043cccbcb4c4b5700a6eeeeb05`

```dockerfile
```

-	Layers:
	-	`sha256:55487635e34c1575a1c86ad1538db4eae8185f9b358bc3b2647c7b10c50a9639`  
		Last Modified: Tue, 10 Jun 2025 03:58:21 GMT  
		Size: 2.1 MB (2080686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6afd8ad60b0744690a9d8df1fdde507192154666dd867a3ca02ad6d8a4e9430`  
		Last Modified: Tue, 10 Jun 2025 03:59:20 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:7481cf83e704b3af7a5b48b3edcdaa6c8359604a90aee37431c2027bc8d9f36a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:106a157335593089bd9167471a43ac4e4a300c21bca0dfac7ab5e8ca330e11b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c425b94e9e05e94a3588a5ed5fa50798b770c5964ee80eb3108e2c2b854734`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833f05bf4a56287336922533369cb272b043579abea2c4588fb7a28586dccbb7`  
		Last Modified: Tue, 03 Jun 2025 17:31:23 GMT  
		Size: 3.6 MB (3624096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5f30655f789d9aaabd83e43e19fd42000e70a6d62d06ddf046576bfb3eb56`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b76c5daef076a6ef3131ece85a9ede4b5366f8b35563943c61f3ca36393de48`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b346a922dadb495203fa86390fce5ab7f4746b373ff8ee37ae89b1570fab89`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
		Size: 110.6 KB (110563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96bb241c37c54f5099c6ee4be792e3df22a12f314a81846062a58b160223e7a`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8aae46358cf11c3d67fb2b0bf9adbc7de24122f7bcae1bfe2c595b1a62233e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2096668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14479c1656b173c0100892f3c715ee08d6396fbbddd70f0eb6c7d400c28dc177`

```dockerfile
```

-	Layers:
	-	`sha256:1e817e7f07a5533079454f7b46be380fb1a89f65ee260bfd9d08395ebf6e86fa`  
		Last Modified: Tue, 10 Jun 2025 05:11:03 GMT  
		Size: 2.1 MB (2080462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb30aac33316b47ec98bca470a0a0a66269cdd7aa22f62d98e749d5c5e1c494`  
		Last Modified: Tue, 10 Jun 2025 05:12:32 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f069651f05d3e6c7a096a41a3242a53b7f5067e15c35b139bc0844d2c622254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b33835d3e532c457a861b46b17a2ecc210b0019baeec6bf4b85319109ae9d0`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Wed, 04 Jun 2025 23:53:21 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Wed, 04 Jun 2025 23:46:33 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Wed, 04 Jun 2025 23:58:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Wed, 04 Jun 2025 23:45:32 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc12a5156209348208485de93d3b89460edf23f23fdded16678f39a46448c25`  
		Last Modified: Wed, 04 Jun 2025 23:46:15 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2fb96a9daec1ce2a7e9ea4dd1144aa633c2bc1d97d73ba0bece51586ec46fc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2097068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25ae2c3ba2f40b6fa187203997315827f50c3c023a8f4ce4137f6b8994a5c1`

```dockerfile
```

-	Layers:
	-	`sha256:f8f474f858ffefa2d71ad93a00640e481fbbfd9d23b677cb8ee70750c1123694`  
		Last Modified: Tue, 10 Jun 2025 05:10:23 GMT  
		Size: 2.1 MB (2080722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09220ec00b43fe2a6638b49308e372f11987cceec9eefdf11f6781cec1b7a417`  
		Last Modified: Tue, 10 Jun 2025 05:09:48 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:66a5f9f387c84d65fa609ccf2e6e8e31a49e5694e3c0e18e29ffd1cffc27fcf4
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
$ docker pull neurodebian@sha256:df6f98d131c4b4bf650a51a1c7cb8ed75f6b077109089524861bcda54b09d0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e761c4b19cc195da8d2855cb566359243e2c2282c9d400eb4c1e84760f913924`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09446529b39b6e747011c65127756ea8c59f2b0b9dc3096e7f48c5de96ccc8`  
		Last Modified: Tue, 10 Jun 2025 23:39:47 GMT  
		Size: 11.3 MB (11266854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301fc755d8ade11aeed0a053875ca7bec42da40cb0a5d13ecb4b84d6c554fc5f`  
		Last Modified: Wed, 11 Jun 2025 00:04:20 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0288b274dd2c371bfab2859b2d1cde4581488f737485247c84dce92e4d2b7747`  
		Last Modified: Wed, 11 Jun 2025 00:04:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88f0c71750a0635a612ed508c265aec03154a9a165ac80f4d16644bb162d486`  
		Last Modified: Wed, 11 Jun 2025 00:04:31 GMT  
		Size: 93.2 KB (93182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b082f19682f2b486a0c80b855625ac837ca40d6474e312afe94d9358a943e0d9`  
		Last Modified: Wed, 11 Jun 2025 00:04:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a59d18ee99e44947f8786dc60e2eda4f1ad2dcb9e52f80b9ff75f6f0503c7b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dcbea1c292a0676d2e7427bad68077d67903db9500a9c57e829f6c4376720f`

```dockerfile
```

-	Layers:
	-	`sha256:190e185693c59b487307682a32db421010423d06f2d8afc82e125fd629a46f57`  
		Last Modified: Wed, 11 Jun 2025 01:07:29 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7352e7a8c0e8bdeb2fbdde263e76d108e097cf91c47f04aaa19d2bbeea69cda6`  
		Last Modified: Wed, 11 Jun 2025 01:07:30 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3f66b6cf9c777c7ee2675df679b3664db8db5bffb63e5f8aae246ebe7a13d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9605c535fd80e79ed800f02eabdf96798a756d9383b1767f72ab8c2604a49ff6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5c2d6b1d7d5d28d02e2f2cac517a8cdde90e21e5a6e67277ee7cfaad9cb254`  
		Last Modified: Wed, 11 Jun 2025 03:31:13 GMT  
		Size: 11.2 MB (11232526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765bba7a7ecb589546d86353bd0d94577c74fca3b7a96a17b6372db8a4d46d17`  
		Last Modified: Wed, 11 Jun 2025 03:35:42 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bea4e39b1faf52aa6e75eed7c4e67851e88e15f1bad433741dee64f21654ac`  
		Last Modified: Wed, 11 Jun 2025 03:35:46 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ff130ee2030768ccbdde40e0b0cc38a55d68706e2e115ed72ce1951bcdbe8`  
		Last Modified: Wed, 11 Jun 2025 03:35:49 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e5c12cb63606f72ac2d02d6c4454a55351dfa3a9d77fce2e7399bc1258ca27`  
		Last Modified: Wed, 11 Jun 2025 03:36:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c7e6a86aef74f4f3a8d6d667f461e989cbfab19d40cb90e57c7c188e15892bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2ec0e9052301c0bd49a05f5e70e49b8526e1e401d45da2f01932619441a4ba`

```dockerfile
```

-	Layers:
	-	`sha256:e78e5536cfdbd3ebd739c041c46391bcd6f46539462a2d07c4f2a1a0fc4632a4`  
		Last Modified: Wed, 11 Jun 2025 07:07:27 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd6c977ee13182fafe5148ade423f1ec36b61c08ccfaf59c11afed6705becd4`  
		Last Modified: Wed, 11 Jun 2025 07:07:28 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bcef4e130e048631d0384f4d3a205fbd025912b2c22c4ddb4b379b316643f789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4925bc3778b6b9c6a745172c48b31f0867a1d496d392da2e5e6cdbafb8a59ae9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3e3e6e2d9340b30d10be9677d2a91088a9651305d3e2814d24858a5d1767d`  
		Last Modified: Tue, 10 Jun 2025 23:36:55 GMT  
		Size: 11.7 MB (11688864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d2ad000b61b2f234b9980ea545edacb02cbd88ee3f3f90bf6fe2daeadb805`  
		Last Modified: Tue, 10 Jun 2025 23:36:53 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2994203a98e1d20fa0b1dd98832c1f6f178640a9cf5f3b357e7fc2dae27c25aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4912929dd01f693d2d50ccabad470fdf08e88e1602d5cc27d7edc7d2de7f05`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 93.2 KB (93219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33efd2b24711ab06b45a10963b4b06e468a842e81d32c38d9e6b08cbd957171b`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff720c8e4f114b36fb3ba27756e87d0525c45d132bfcdec8b951db47adfb27e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78957fdb65a2c4183db08aa3428de96e661ea300304ac4527d7c61ef279719cc`

```dockerfile
```

-	Layers:
	-	`sha256:8f7c40befd41400cd338eee56f9ab359489ae226cb16cba8f1a7265fece184b7`  
		Last Modified: Wed, 11 Jun 2025 01:07:42 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b39234998b303494b07caf4110461e1fe5a4a40b9aa15d920f390887c601e67`  
		Last Modified: Wed, 11 Jun 2025 01:07:43 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
