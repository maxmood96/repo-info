## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:4fe7b4ebd1745deb339dc7af9ba17ae5bb36fbed70b87d99a6cb584723c68207
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

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

### `neurodebian:nd` - unknown; unknown

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

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:060a7c0436faa46bd6a80640e5efe27a2fba2e87a2ec14ae3a194cbd1732a7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58995087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8d18c8ee4cc0fb6be602a515ae042e3a1c2e7fce195d4e9b83fba82b2567a2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012a9a0c6fc8e14dbae0dd211be74c76a40a0bdfe55e8fd25532fadc68dea49`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 6.2 MB (6219805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46829409c0895984dd0c82567ac3a739a6cf8e121453008052b2e558d75b2ab`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08328daef7cdf76f8df8778afcbc4c476fef35cd256705e6c768b9ce1033d6a5`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99980679ea6d0b863dc5d985d23bdce3df45e1f095ca22b3c2e45a70dbb5f47`  
		Last Modified: Thu, 13 Jun 2024 19:37:59 GMT  
		Size: 90.2 KB (90185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:43567836c2e3fbc3f88e6d669ec9fcea09c616929c8018cff46dc4cbb32ed3f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e656634f06db58f4ab04ef76d28bf2f9517e69b79fb6ed19dd970a964fe874`

```dockerfile
```

-	Layers:
	-	`sha256:0164ea5dfd6dc1d678da7b7547f4446613a7ee6e16627e3d591bfb6e89dc4ac1`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 3.6 MB (3551055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:078bd79380d023fc171fed9f97da85cf20d466f502004ad09885da2e0a4b9eb8`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

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

### `neurodebian:nd` - unknown; unknown

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
