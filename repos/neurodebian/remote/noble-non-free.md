## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:845fc301b50b3a4b33d732bf49776c2807a93443addebba44f5c7f4269984f07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:902584d42edb09004a9e5383f587fe24af4a1b858ee7605b41cb023748c7b235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f57abafa53d93a11fbefd1ea690e5f81b6f58a8e48d1b67dff4c6109122c8e7`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc75ff17550db8092fab7604c10c333e70e266250c3c6b5cd72078163d4f54f7`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 3.6 MB (3557848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef545aca17bc58d9ef369f44978f6e8f60e7957edd0b07720f1e3fc3ce9da6d2`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e911b14becd8d48a3394b3a7c3d008b0d39a665a6502940e4f90cc7f22daf722`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ad1ffad3d8688a24df2a5c36bd814db53aea8d81e55acf6d835f1d21854ff`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 100.8 KB (100792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf93a5f832a83fc1a9c58d63fc2acc8974ac31be816a46a9a5299f8455734885`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:de451eaf65788cb2cf6f6470bfd842f657606fc0a997767325734611e7d67024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb7c702d37d6e2a3b7ec989cfd751d64c90c79bbe5b73aab42d165ebd99dc45`

```dockerfile
```

-	Layers:
	-	`sha256:a4e2abdc14936826569b84a572f1d6118e38ae5bb3b3945147939208558c316c`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 2.0 MB (1972460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce2e7e7acb9ad9203d0df753d4faeaa1d69c7939bb23e8652b2a1b6e4007c609`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 15.6 KB (15636 bytes)  
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
