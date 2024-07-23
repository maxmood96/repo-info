## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:25e58a5807c65f7ffa4516ccb2d47954af39a64ddbeaee70556493744958fb42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:8df25b7381b56e0c058ce85c9a33f671c6e1daf7f46efbcf14fd5528b3202b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59098051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246cb0db993b407cffde6493e242d3de06ae128cf87b2267b22a47439c4af6ed`
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
```

-	Layers:
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebedff2812269508116bdc4cfef008441e28a0371783e5d7858c4781c1feb07d`  
		Last Modified: Tue, 23 Jul 2024 06:16:50 GMT  
		Size: 6.2 MB (6224015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7a97239599a4e60b31be674f713a6b1e22c175b2c02845b61568d1db2fca0e`  
		Last Modified: Tue, 23 Jul 2024 06:16:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a545f13c4b3248136207595b0479eabda06be2625497db2580a1d192d0fb472`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5226c81f305bd3e0c716692aecb129ea31b38f0a17252ed8ce8074fdb8890d3`  
		Last Modified: Tue, 23 Jul 2024 06:16:49 GMT  
		Size: 90.1 KB (90093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44d15eaf8b16820042eb3da978d2cdae7052cb71a741d96ffe135242c6671f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc7595d4909f057493250e003bc9e2c5f3afa421c262c0372e83e6592bd1755`

```dockerfile
```

-	Layers:
	-	`sha256:2660976885a91f1b983c76bf298e1b3850a460a9a8529833488f454f140d5528`  
		Last Modified: Tue, 23 Jul 2024 06:16:50 GMT  
		Size: 3.6 MB (3560484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:542975e582d79cf3bd0666b614e52805ade397c7a5c3985cc1d0f1b0e27c7f6e`  
		Last Modified: Tue, 23 Jul 2024 06:16:49 GMT  
		Size: 13.4 KB (13395 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:30fbaf2df2d18158454931946210929a898aac9a510b57a3de067dac3f31205d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59200815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ee26eeee82e9d2700b9e8a5ba5cfe2b0099fd78949a1e36b72fd50b835df89`
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

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:310aee846defdfb760eca13b6fce5779b662d709ed3b6591cb5085bbeb1c75dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16c6093800c166d913f3cb72cced10e90a82d1ee69da07dbf4b58c9e05dafe0`

```dockerfile
```

-	Layers:
	-	`sha256:b191342d93b783e3a64d7a2bb642f2d37be02e8def34c8573eb81969a952317a`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 3.5 MB (3544010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e822a6477f51ada4b8a2b0db1d4d77bf3cbb576c54c263535d3d5d8fa2e38f12`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:3b372a54e1ce429917523e9c2859fb6720877ec0f30be7ed8ce8d07abe5109fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60347544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f950c70258e58d2a04cbaa96072681433773c05ea1973cfa4e9bdd4d5c609e6`
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
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82bec79dff3a3ed87ff22e886c5aafea0a550f124ca9f5991042ef6cc4c99aa`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 6.6 MB (6554808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd40d97447dd271777a17658fddd6e0adb18cb96c4c55d60d7b164ef5cf4fb8`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ed2f5ee74e882fbfb7a7ab0794df8358d83de25f763a8e085fc0ecabe76d2f`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f41dfdfe44562c08bf96630bed334529c1ebf002d479fc1d5930fb70cfe0859`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 90.0 KB (90008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb83ef00b339426a4d143411d85fa66511dcdc042a56a33803050d28f153a258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2b7a38b2f8a331c5bc8798fc52439dfc30869aa43d893ab5362e307440aad2`

```dockerfile
```

-	Layers:
	-	`sha256:f3e38412e47a224b162530825ddb5c0174967d282cb6b3bf7598e1ae9e09b248`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 3.6 MB (3557577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74437b60de29329d791d3af9660d31ba10f449b2fbb525da0626d417e2e6ccfd`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json
