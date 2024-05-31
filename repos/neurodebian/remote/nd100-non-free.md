## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:afc8b3335d916afeae7db67b7b15a0929030baff5a369d2f0ba2de71de83494b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a40a455e224e378e6c1ba53e49e80d54529f414ccade581cfdb22793781a5cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61070980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef3d76eacecaf0406c82147a394f54794bf4b700f87d152f5020f712da7a5a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728c2a274152156adae707afd4c7acff7c3cda876d9f29783c874f87c6aa6d3`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 10.3 MB (10307527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314584b23585792203e4a076400bf81f382d644fcb124e3f4ddf4f81afd551b8`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d822bf0f40147d3330203054210369cf3c5dc3a52c16fc1726e82cfc84284616`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da49aa44fbf6acccb4122c994c67ba81c4a6140f03fb144120bd4253a6780cf`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf89c183f941a66ae90604d83e0ac30aee3197b51ab7e74b363a9999914ee77`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee6ec2e169249fac98fe23df8d0c1eb252e19df7a7ff3b364d8f3f4fbee094e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf9ffef60121c1ac26664f0439c64670b139b6aeaa957af6334c6f9a79f540f`

```dockerfile
```

-	Layers:
	-	`sha256:1832a42524e696b8e542d88ce1fce9959d42d5e7148a1e06a6c337d4a32540bf`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 4.2 MB (4215102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3614377f3b59450f10c8124c7df977ab039c86c05526e2f7ad95c529a4408f`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 15.4 KB (15433 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c88056a47dc5318043679e57676a23e583df1c718e7983a3b57d31f2e4a093f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024422e05673ba9016411a9080801a2e926b1283e23186b85469a2b625cf8fbb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd9c59acf204c0d81aff8b7e5da56cc3b76c258fa40d482df9e225cd533596`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 10.3 MB (10313209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cc3300b9846c0e9c7dba482c8c981db848d2eeb56f74c62c65a1debee89e29`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60fd2e75c963791cd3b0929bb3c01c7671ec64f140a3ac83cf1212b4a5b5c4b`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e238e2f4604a403218d3037f6bf35bb3d8d7e071f2dba1a6a88fbe012a1abb1`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 104.2 KB (104250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b85b4e240f80a499a71af86f86bb3a75a46bc47a84a841fdc6cec3b6fb75e4`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60e9beea383de0d520744c632f02662cfb2ea54b541ff3608e4cd6c258ed5daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c823c4fb2948cba2750dda96dbc5bd93d2fd769c9b0aa6c4fb1a87091d8bfe5`

```dockerfile
```

-	Layers:
	-	`sha256:c502212cb34e8b56ae978bc283f847c2d4d457e1f762d554516348d43afbceef`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 4.2 MB (4215284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78431dc615efd921d0ece65d407291dd8c193f19e87e47543b1a2e182523b064`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 15.7 KB (15713 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:79f43e09c8bd942a74f73573bacb1941fbd78ff7eeba55462743997bdc4f7d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1874d6c59d2e5026b1e028e02ac1eb5817249b3aed4e7dd6e7b9f0905ccfe10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:5e59addfe8663b7c16cce40874c2a3c8601e20e80f5a0897c86b64ba463c10e9 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1a892f56e4b10aaecbb51b3219d90bd0d8a1e955acd0624a6ef27ed086ba168c`  
		Last Modified: Tue, 14 May 2024 00:53:06 GMT  
		Size: 51.4 MB (51419713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bacd369dce408b68c7726056e592b1f17f7578941f3de2d8f76b6d3ca8d7e4`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 10.7 MB (10672378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2308c349457295ab95fe2575055110d1ade8a54a480a6e0f2a743eca4e5e9e`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e324ca101e0ea13d957f5a45d94621cb084dffaf4547471dd53b306ab98f49e6`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ace760e484c0fe839a5e3c34af4575df20dd5f0ffaac9bf46b706d335b755`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 104.2 KB (104163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e842e392f924c6e1b42d7161bf79b0f7ec7f4b8887a3ebcab0ea5087f9c59e`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c8004ea08b3b304828350dce215b80ecaab283c3852ab7e9d3ec04592a3432a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bd370ac7a1d31953052df464acca8b87f29cbe37951062d4ebcc7cb54c8e48`

```dockerfile
```

-	Layers:
	-	`sha256:af2b7c7773f2524a1ca066f7c7b8c8ec3a4519c506699522ae7df07c5665effa`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 4.2 MB (4212348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e547be5d9e6bcfb7dec9a08796d5188e6f44f613a6ac2632e1db0a760b953b`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 15.4 KB (15408 bytes)  
		MIME: application/vnd.in-toto+json
