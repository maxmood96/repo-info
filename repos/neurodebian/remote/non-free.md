## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:e9ddccb875a17aa345ca669154d40457f3de1e6196e359e147dbbc52b912b2b1
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

### `neurodebian:non-free` - unknown; unknown

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

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2cadf68a2031eb58f9fc6f1ffe6aef4ed02a17e61fb6e899e162e11be19e5924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23adc07773d4924502532239ca86fe971d4c52473ddaf831a0ad2f4c5e2875d3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b222ea27d3a13a628f27fb485c2c8953c435cf879ad43c99108ae24a1a8538`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa7c14ee96487976b1787f395d3da08538e6eb4bc1212666ffac800202f10b`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103fbbaf04667aeef928e69b2b8457085af18a4894f429dfb4cd0ec52dfca876`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370293ac9e0cd3f1e79e181dd7401ddcfc4d9579c4bcc066993cb19373d455b1`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 93.4 KB (93360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d034187a5238f4ac144d3f26372ba2a244669cc6d057318d3f60129559b396`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cff90856eaa4cfe55cef01efb7e4a7d6ad9fc13743ac77d3ec2d1b4411602090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6784a5fa44f5349ac857cc8fa34504dc72bdc0c73d227e8c76e86459bd2d1df5`

```dockerfile
```

-	Layers:
	-	`sha256:04944ff3646cbb8d2c015a187bb9f8c4707d4a241a5c5ded62e171f60402f190`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 3.9 MB (3924545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cfff78c55d81b9986af70e9de4c9acb0d6a646de7805f6f542277ce9e81bf6`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

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

### `neurodebian:non-free` - unknown; unknown

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
