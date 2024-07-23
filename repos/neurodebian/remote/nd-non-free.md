## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:bbe8995fd80f39593d8faa36d9304dafd35b5d33e1fceeb66759863ffb10447a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fe00f914907411d2718c1090b33671bd938acc75d18f6e9bd33915ae25007622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59098491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3329beaad1b7df1a274c23c124cf41b240f4974f192876230d1a238a6723945`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba78cc727fb8c4d6be3b81320c6cad029de3e21545cbd6ff7f5d3e24101f151a`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 6.2 MB (6224024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2d81607b27beb9a44d5a4417a9a035589e70b3b1ec2100391a8b57208c416f`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a545f13c4b3248136207595b0479eabda06be2625497db2580a1d192d0fb472`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca6000aeeffffc4a99aa4b2a506c1c37b60feaba0f4abbb0b0df48d71c168b3`  
		Last Modified: Tue, 23 Jul 2024 06:16:48 GMT  
		Size: 90.1 KB (90134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73252cba8a182a2d4e3711e7b3ca228fe88fc064566e9fca00041e6169eac54`  
		Last Modified: Tue, 23 Jul 2024 06:16:48 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f17ba763e3de97abf585a033972887d9566a765283b42b13e76d63a07fb6c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab996e76af23a9465feb34e25cf43c601f80837b9cb33fc4c9a699029842601b`

```dockerfile
```

-	Layers:
	-	`sha256:029906b62d9492d3fd7fcc7f30c42d40dbca591a8e4f4625452a132c7bb16237`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 3.6 MB (3560520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed57b663d769dc87ecba0f0d26f41a9774ef1d870b398bf12f681312a26ccec`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1d6ee16b19cca79b92541bb682a4c922cfe787ab167987a257b1cb41c69628da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59201205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61af8fb9eb88cbefe347add336cf5ddfdd03de1bbd8def9760ab1aac9ad011d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f682e5d0d35b6507170549e927b44fa72be309150cc766e8c567a6fff21d100`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 6.2 MB (6219470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1116df5d9885f9a9ff682c06a547c1709ba2c34e3e92865cc80ef986d89e795f`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2529b60acd15a8ed1a099809bf5493031c27bd7255a688091ce443bd422685a`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c43a6b60e4e33f946bea9f325fd364d2d5bd69f0848b7f74b24cbf2aa860681`  
		Last Modified: Tue, 02 Jul 2024 16:02:59 GMT  
		Size: 90.6 KB (90605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a830aa41d3e8d87799e4ca16d1813076416447501bca235a0651831bbeeab350`  
		Last Modified: Tue, 02 Jul 2024 16:03:19 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5aaa618816e5505ab338d006a538bd7aff3a3178b69f16b46b95f6d8f64338c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8b09ec1e0a532999060c6cb93a0d079d1073f63d48db887d7e839eff87c70b`

```dockerfile
```

-	Layers:
	-	`sha256:5c69f38169c1a9102899bbfa7a76dc58e3359ac9e4713d70a2f25ec4a7f28693`  
		Last Modified: Tue, 02 Jul 2024 16:03:19 GMT  
		Size: 3.5 MB (3544046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f627c118c0b71eab6eb5458d2d3a87f5691c5e6abee6be8be9f9c1eb4baf17`  
		Last Modified: Tue, 02 Jul 2024 16:03:18 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:573427ab2013d8649e8c77e0c43bc3c7b5b5f4fcde037e6c85a054575958da8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60347600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087f6bb71890c249e63439d7a260d4d4ff8b25d84f6ff76e84993a8400a9217c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5853df0c476cb6b47074aecdc44c8989de1742ae9f80314550a5b130cbd8cc93`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 6.6 MB (6554507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ea7f033db96bdba75250d4e1d338c9d502f3041c12b5d849f4b056c52135b1`  
		Last Modified: Tue, 23 Jul 2024 06:16:44 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2c54943a31f955045ec02343ddd94eac368955c1adf7e5c49bf9d15b245dcf`  
		Last Modified: Tue, 23 Jul 2024 06:16:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46257428d44167f3bc35b5e28d989e657f3ba1561445dc6279343bfbd3d6e182`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 90.0 KB (89966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325034bc80906c9ecd3452f092b7378c6ea12b3e022d1839bc4e2580c8ebed12`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:04eb5e30a4c547f455df66af4e1bdd2a670958758479b28c99da857edad49e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae053737de19f1e726412e8398493852de05747ad7b20e98595017394c240a00`

```dockerfile
```

-	Layers:
	-	`sha256:1c58c3cfa44d3b57862b1ac055d5022d978d6d2bd6781ffd4800c75fc04921d1`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 3.6 MB (3557613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c52f4ebd0b2d5e69e3a5681d4454b99743cca8d75a57d5175f3edb59fa3cf83e`  
		Last Modified: Tue, 23 Jul 2024 06:16:44 GMT  
		Size: 15.4 KB (15400 bytes)  
		MIME: application/vnd.in-toto+json
