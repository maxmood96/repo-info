## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:ae54ad722627a0d4bf098ac7c90adde675b011691891a98ee549ed449f97550a
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
$ docker pull neurodebian@sha256:1bf2ad888a05ef807d67508a9f6926ad1786f54786c4acea708e393305d3e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f9c69de5373e2c9f69164910ff1d44257dc2596d2f0d7d3cfc67a0c584d68c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
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
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18398593d4c19c61fc775e0592d0d8a432ee6462e9a8f7b8810a361333b485d`  
		Last Modified: Fri, 27 Sep 2024 15:28:29 GMT  
		Size: 11.2 MB (11232110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621de790ca72d0c42672a6a2ac731249ca406772328f8c3edd3d594f1f53f616`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b740e3d498ccc528d88bab38ee97183e394cdd50200b197502891dfb79ad4d1`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5924f9901e2c8fcebcabc13a32cffd7e420213b1cf345f0e63ad1b70c157a`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c007be9f3baa091742dc1aebd0ae0a6e3cea7a4b810f0b8e43f15eb877896e70`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a5037ed0757501393c215f764e0ae006eb95c5b18a1b83e29856a21a86f904f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a21e19ca8c5ff905338308a88e40f5a3e1df607f032725531e296e5de2077dd`

```dockerfile
```

-	Layers:
	-	`sha256:b824964735f0d18f63657b8d91305ccedf77807feae3a5161f131d57be3295f5`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 3.9 MB (3924545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c864375c20088fe814094af1263b5d464fc676e095599494c207463caa2967`  
		Last Modified: Fri, 27 Sep 2024 15:28:51 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

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

### `neurodebian:nd120-non-free` - unknown; unknown

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
