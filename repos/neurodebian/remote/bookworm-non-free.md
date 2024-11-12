## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:a29ddff999331d8a84d57feb7604e07f98e15bb6d19fce6094e68a77bb3ec8f7
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
$ docker pull neurodebian@sha256:b8afb69da5b752b060806ec138fc3250abbedd6e6b123ec18579d284a0fa6498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60938060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e220ceb0b306f430cc776ed85f4e2a38f5b334e2fae14cce9cb5f8707630f5f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e875bcda0d24503a52645cf07fa8aa3dc1787e24f752990271aba967a9cfb2`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 11.3 MB (11266807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cca6a0f2fda1ef8ccfaeb511a82fcda80b6db7b91c345af7ea41dbe4f31e28`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6765a2eef3310ed643c9cbddd43e752a916e9ad1dcef70d89ef5dac93caba3f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f968c64ee180766d3e71944b655ff6d334e49b33b507c3daaccb449da7105`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 93.1 KB (93143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36ebc47b1d30568b2899589ba58430ac196cc8a733cfcbcb822f531251167de`  
		Last Modified: Tue, 12 Nov 2024 02:14:52 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6349e62c60180c5f04a0f88d011ad639c93e6ccecaea806de68713c6f69f1b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0450b5647d02f833f34a0f5672bfa7087713135811665f4bbd8444eb384d5347`

```dockerfile
```

-	Layers:
	-	`sha256:f5570f0790a0acacb7b300035ab5b7326e867a2ca3567c8e5523e787a4bfed04`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 3.9 MB (3938519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68a35dbd054a1e8d7907f5afc5da4b8de02e38190d41b7a811862d59a6edc98`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1de43f7b125dbbbfe5a310600098e8de1fbfd335184997e9cc609b4758231958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce5ba9d618002f94a38cff26b1170db170e99a36d546b12c1e2a5cc68717d50`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374b4f322cd89941e3a79c9bd26d1a5f1c6bc1cbada76ddcd1dc30f5e5cdba3`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 11.2 MB (11232560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c07a4424e486742d8557f51e2d6ea83c25c81a3fe1083cdc92f2aaabe53972`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76a820ff7756abf0046ae961df3ad5d2f997f1277bdb445d4f9ce1e548f3cc`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89406019c22729ee9e55b00384b15954a2694a0806199b7273eb34553edfd429`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6918a4974dfa238bbfdcb88f3d3f3458661a13de3a8be18203eff7defe143`  
		Last Modified: Tue, 12 Nov 2024 13:32:51 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:454165faeccb15f4aa5f0a212fc5218e227aa920fc5efa71800221a7aa824d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a29833a80483958f799c7ad16899b52498cf4e2f87262d5bfc5275cbe29c1a7`

```dockerfile
```

-	Layers:
	-	`sha256:c1010f6fd3eee44d87ebb438d3b23434a45fa4899ff9a6ae85965ce06845eda6`  
		Last Modified: Tue, 12 Nov 2024 13:32:51 GMT  
		Size: 3.9 MB (3938772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd8b5199518f821a024f414a90c2b37720a635f8bb8c6cc3c6cf2d1a5cf0fc9`  
		Last Modified: Tue, 12 Nov 2024 13:32:50 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f13d92e5211f97d59e114b6436138348667d7cc56920e67c081e941416adb094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150d422afc9147c5b81e217636b9324ce038c190cd5403829a80f8f38fdb8aad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b2bc7e2c4724e0d9cc99253b76322cead2324f1116c27c22e45882c20b73b`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 11.7 MB (11688981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a8acf27bb69d2d3bbfbaa534d4977b944e9f27fbdbea8956f2bc958022dae`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0ba9db146b8f5a4270e9de5dd5552b75471e8b8b207fcc3ed7a5074dfecf8e`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebee1da5e8ebfd36eea82726d73c31e81d1bd572d464a7c2e1735488895c79fb`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 93.2 KB (93224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8bcd17001bedce769ee0a613e4ff52e7a2324d77bef8e3ad6996ecd0f70ac`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:668fa7f722219a898de96bb7335edb634f3ae7fceb8edca2b504e43a6ab42ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f4bff819dd2497c5fc6382cc7ed783a292326d68e126067bd7a6ee1db7a6c`

```dockerfile
```

-	Layers:
	-	`sha256:fdaa6a6a15e6b4d89406be98109008f643f841b097fb21432b53f7c7520fec64`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 3.9 MB (3936436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79e84acf401893a2bcccb52bef19425ff82fc1e6122b7a32860ca01d7c2a473`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
