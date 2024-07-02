## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:ac2c3a509542e6ebf371da88b9cb4b240f87166315f94ce72db641575800465c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ca2379877bd375136f0bebacc15725191bb411a53cf4085f66157875892ee4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58772271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353f68948093fbaa77025ded231eed6a7e3840a86d3b0e561d6e5044235db7b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:90c4ad8b280b16131f305780a1f2721616642bd4d5b4a26256c760cd8ae98f27 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ca828e2fa86974a7bad5159e89a3c4f34921c624322a7fa71026f2a3933ab620`  
		Last Modified: Tue, 02 Jul 2024 01:31:45 GMT  
		Size: 52.5 MB (52458214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94e3ccf5f5407de3eb05fa25f8e9c631fb1c59095bc2e61399ec9937cba2d3`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 6.2 MB (6222085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55ac663eeae01cec5106afb87e8ed79e49b5c2a7ca82dedd5e9d202d2761c1c`  
		Last Modified: Tue, 02 Jul 2024 03:19:46 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c35d22fc86197f71cf62047c3b9444dedefb03d49949ec9cc27cb11341a8750`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b3b39d2f3f9ebbd735f3955ccf42be6c60fc7c0673cc4d5c8194657c0b132b`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 89.6 KB (89564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830af931f363fe496bb2204c8b062340c0a5d696ce5e499e65abe96c6bb25443`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d1f5a12df29579d00f04b27c04671c9a4b46104c083c3ce51e009255e78c13a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26a3126ea213714cac4c2bf30e583440725b7bb70d9515a469e0e0143f1b868`

```dockerfile
```

-	Layers:
	-	`sha256:da24285cb8b8757dcdb2fb6b31c55cf2448b50fb093ed16348ffa0e5b6883b44`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 3.6 MB (3550089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b07cc3761be09ffa10b5dee6bfcb6afd6e6e5f2f6dacc8fd9d99879fd96290f`  
		Last Modified: Tue, 02 Jul 2024 03:19:46 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f45065add2d0883b033a2583f09a8d0296d5b2745b1c2324e2c5a54ec3f82aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58826754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238b72f71b23c30823bcdb682d02953b3cc16a472ab5e249c0c188f6a4a9066c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf7f291b584d447470c53f740a381678ae64eb7277446eb7554834f38cd871e`  
		Last Modified: Fri, 21 Jun 2024 22:55:24 GMT  
		Size: 6.2 MB (6219741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ebd15e83f0eeb8343265465bc92b275299180a037a7280dddb86a897c405d`  
		Last Modified: Fri, 21 Jun 2024 22:55:24 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0cd3d386c4115201c955e348c507e250fe9f6c6a44c9d0ab6c06ea66413e79`  
		Last Modified: Fri, 21 Jun 2024 22:55:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ed7aec11adc4777ade35b4fd461be4e0547b4f74619300c17ffef4ef0e8f1c`  
		Last Modified: Fri, 21 Jun 2024 22:55:25 GMT  
		Size: 90.2 KB (90216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe6f6f2bb716bdc9373cc55c9e5072c4e88376485cc431a7381ab13af841cdd`  
		Last Modified: Fri, 21 Jun 2024 22:55:45 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5fab77562e73a66d222647794863678beefd6a97c7d1f883b4ace2ce2f721db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bcd5c33752d5a7f98b2bb1a14a605deb310cf4298096a9619d7aee5915d69d`

```dockerfile
```

-	Layers:
	-	`sha256:4660fa1d0cf408df5c0a2d80f668921651c39ee94bca9f66ce46e5d783962f46`  
		Last Modified: Fri, 21 Jun 2024 22:55:45 GMT  
		Size: 3.6 MB (3552342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b1005c43c33d6249bc872230389aab9c470d30ad6ea4c21af84e773033063d`  
		Last Modified: Fri, 21 Jun 2024 22:55:45 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6678b0abf7ce15b47e9fe6e10f34a869f8df78e0c6aa931ed483357ab28e3bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59977316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7f82e6b423e8ce366a692e0015506898918b77bcc79651abc0721a23d1cefb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572de5816e1dcea6e5d7bf1248df78c0a435de0efeef834dd9d0c38567570bd7`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 6.6 MB (6552258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a80c2c6d79e7c89ef04c1b1df81970b923505bad19e787301b1c53ed276e9e`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c830fb8727b7cc750190f85d23fc464ae943a3599eed6b6539911056e7eea3`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d978e8ef47f777662225ca0ad77f6faf928a037988e9242a9558de8a2829d531`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 89.5 KB (89475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bd4c6b10e884e1886dc9dc50e79503ccbac9653d743d726e5c1292b521da11`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:baeca2bd03a0194349bb44d0c311e1c6839f71fce257a6506bae904211aa7d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139e65b3a6189c99551bdf06fe0eb9a714c3c155ddcfb056e712b7011a72c9da`

```dockerfile
```

-	Layers:
	-	`sha256:ef6bdde65a79dcbbe926e238d768dce9b781bcabc19642a5647491d0d72a4332`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 3.5 MB (3547188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddb7644a264eff676c63c86ff6cea3f2e367692140d6e6493d4c3ead6803f4c`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 15.4 KB (15449 bytes)  
		MIME: application/vnd.in-toto+json
