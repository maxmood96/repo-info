## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:557ea045b7eee1aaacda673851a27799a5b0620333f6f4b80249c8d901a31767
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
$ docker pull neurodebian@sha256:2d73a121aa2a836fdd61c2caaa45f39a60d7135e9fea08a33bc74595a2c2f63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc4c075aa36307cec499d38e0967a31bb1177449a066237940379b201fe03dc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e3861fe7b114a17685588363e051556e829fd3ee46e28f62d884d28e74e55`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 11.3 MB (11266561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00ac0906fe55639580577bbd3dd60b722d4c59033a0c14446e5224830a05c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d085eb9d9ff2ee88dfca96061cefa20cf9c3d0a7bf1d9ab12247a6977664db72`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1ff7e0b7fca23cd7c1b39fa04005382442d07e9ce890af5fc59dcdf4f81278`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 93.1 KB (93128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44601798f4d155482adaf66f6cac064352d48cb3d7a9772da5500a7a213dcd`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d16d14974557a6a52b575d322f4fb464948fa19fe7409852ac281d2549fbe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853cf6b4a7404cb7dc08679bfe53a305752c9c1daf86c8db41da8b4019394c64`

```dockerfile
```

-	Layers:
	-	`sha256:3d1b519a35f33eaf08b368bda12cd36f3b6d20193425c489c53d1b4fb859221b`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26665f8ede534d5ee35159984cea4fb23139470098f78b030b8e872244fd4f73`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 15.9 KB (15858 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

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

### `neurodebian:nd120-non-free` - unknown; unknown

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

### `neurodebian:nd120-non-free` - linux; 386

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

### `neurodebian:nd120-non-free` - unknown; unknown

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
