## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:5df24f56a6988d992fb159c10a1eadef5f941dd9f86d9a5804839909770c7d5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:23494218fcf4af676400f730f260d3496e45abeebb3643d4f2f6814e18804b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d7fab169b5c9cd9a6d29fd161d4333ea8b73868f7121cb26047d66a19f567f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c912f4f015c2c89eee9af3171573f750d3dc9de8e739f9252b3eb317387983`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 3.6 MB (3557868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c30851e6913a144d98698c661b2fec79c5b55153c2a7a9390eca093ac6f50`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b0875bf1f60a4462947264348c9dfe2c2f1e578d1a51e0986a1ea56fda4c5a`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8874b45bac9e590e59a39707917cd81534064618fa99b1d4a6831dc368f91958`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 100.8 KB (100783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1e41da67b4900e7f74072bebda6ad867d9a766ab22e16f0e7d6e74fcb7427b`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:487bbe2da69bd02307432a0294d70892a959eceb03e0a0870e6017fa3ca9b5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c7e2f11b539c1c880472ecb2113456958831d10e99a7db75e13458d8d64834`

```dockerfile
```

-	Layers:
	-	`sha256:7eea4b77cc0770574c9a48f2e102d138a8e32a2ee294f610f29b3bd66d90daee`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 2.0 MB (1972473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02f4c475e61277a148d2dc8f0843497b857e7d8ba0561c7e9012723fb526a07d`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3e068103f646ddbaad20b5f20894956f2f5e4345dd1d595b07dec8569fd8e940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327e318c15a3ec8c08cd9ead5bc3f374cdc18b8f8b3146d9c9767653c57b999d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c528017e91f5cc5b749ba6a5ec49b1489007f526dc76de4c0688bfd375bfe0`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 3.6 MB (3557058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c57f0202bd48996c76cfe8353658159a0b6dd4d6b5e6ddddb74d09f05c99d2c`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc219592e3ead1bb1eed844d765bf20908729bfc04fee856a3e634117a55775`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3184f62146b23536c694b0b1487ca2ca56d879fcdccd4ec791f4058c2dd3b1`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 101.5 KB (101455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68314c34f4fa65ac887a7a463599e146b0fb4c427d8220080ae58e0cbc4f5d8`  
		Last Modified: Tue, 17 Sep 2024 02:38:01 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0cf913ff9a905be7f50416b9e880c2b350910991bfcaef1d01911c3a5fd90421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4a6223227a7c54909df5d683305dbafa0d76769d93d888a4a35851fdf29b64`

```dockerfile
```

-	Layers:
	-	`sha256:85f43e35566d9283c13fceb5b831b128e4aaf4e9b030092671b58b0b1ea5a064`  
		Last Modified: Tue, 17 Sep 2024 02:38:01 GMT  
		Size: 2.0 MB (1973505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff155ee4650cb60df1a2ed11bfbb0354d610444f61bdca7ca8f7693025d11bf9`  
		Last Modified: Tue, 17 Sep 2024 02:38:00 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json
