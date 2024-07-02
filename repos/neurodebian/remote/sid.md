## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:ef536e667e844bef3f025a24f5383edb3acd8ba268e8ecec5d368a914330ea3c
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
$ docker pull neurodebian@sha256:fed4e2b3530c645d3e7f84cab37eae2b044203d0a63b5041fada474651435759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1f6f5d21c24fbd989fcb96724344eda0066e3348dcf06c8929fa5d5c6f83de`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
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
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c8a6a2c7c323b5f83d47d65d0855b9448b50e6b97cbef4bd5d73232f349fd`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 6.2 MB (6223751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490f9f972c2ac209587470895132421e429c467f7d29addd4040a25acb56cbfd`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07cd42cb9adf3ecf8f614512a7b6cae459af25dc79dc86de006f68132e9d45e`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb907ad1f19de4a554a7f21be16f71a92e5ce86f2ac6af4a9c84221b0b9479b`  
		Last Modified: Tue, 02 Jul 2024 03:20:01 GMT  
		Size: 90.0 KB (89951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:27b9f3644c9b309aa1a705e3d1fecc58292e8df3308051d0607aca64a23f0aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef885fe31425b485ef042622ab50eccae8d5e447adf219ea5996c50e1633d194`

```dockerfile
```

-	Layers:
	-	`sha256:f97fb27a9a48fc37dbb30f628f954e9883c25fb07c0f8413ceb17e10109b8d03`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 3.5 MB (3542968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ab7593e82d79e46a4371616d56822aa0bab981e2407fa488bd7038da7908d6`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 13.4 KB (13396 bytes)  
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
$ docker pull neurodebian@sha256:a56df304eb1c86cff5dabf46e6ff9297bbb03f3ef255d7deaa00e0b8fdaa389c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60168574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6069e9b5bb86c23e89fd8dad23320f538af8540faf82b86dc52737c7034bb9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
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
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bae8a7e43bae044e98255a2206755c69c43385deb06ef20aa0b6503fa088d4`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 6.6 MB (6554390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e11be3bb587e64a347d31a346072a1d6e9ece33f4143863392162f16b3cd01`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f71b73e7356e07f5af8d54e2d18b1d85ecc857f950534783ef06835f22b8fa9`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7898530d420217d5444d31552e4c9f5342f0154e6f0d3ccef93978ec07cb807`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 89.8 KB (89812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:206fed867ae47592e453aab638ddf57f46de701b2e8f5d31586f00ae3e2805e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff168378fa483c4103d74c263824022ec0dcc5e2dec2fccd17229f8aedcf50c`

```dockerfile
```

-	Layers:
	-	`sha256:abd0719fa266c6eeddf8f85db3071c406ba6928ed8be544ffe69e049d85993a8`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 3.5 MB (3540064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263c2eec06e1535e540929dfabee362fe03001b2d54429cc4ced846840ab63f3`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json
