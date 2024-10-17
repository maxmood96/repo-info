## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:7e4840f6db5f0eafb9109b71b600b030c1d496111b609440225037c358b9144f
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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1360a324a787b80218de1b31e8a4bf1585aa0f4d8ca0632db9d4b1f1543510cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1324be94e3ec7d03a9cf2e35cb45480ac0a5381718eb771487a1f35f8dece4e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
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
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8e15811c104c2540eadcbc91d0ad8c420b9e7ed2ac33fc059533f236d22a34`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 11.7 MB (11688958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c913a60b2aea27736559d68f57b0c6af1fa233fec72e8e8d5c7c4c43199ae4ee`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72ec95c15f2bc5a6e5f16cc99197ac8aa491212630d4ba05e6289cff9722cef`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b72d6dd64c0de2b1a61e23af324c34b46bb76638afa8602a284cb0ae786c7c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 93.2 KB (93204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b092aabde6d4449b6ed80131da9e46d4b895bc88470d189cdccfa0ce75576069`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:007b4de94d8801338e3e7fbe3ec20314afdc0eb481e48bd4513d73b699b9acb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1461c367a715b910d400bca53db41530c86f17ef50c8272d365faef32c555115`

```dockerfile
```

-	Layers:
	-	`sha256:80806ecded92443b46c358114ef373cdefab1c787613403548a873b003328f3c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 3.9 MB (3922209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4b56190dbb02bcafb5596cfd93692a4b34dff5ee6b38ed1ef4f3c69444d232`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 15.8 KB (15827 bytes)  
		MIME: application/vnd.in-toto+json
