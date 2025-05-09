## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:69ce90ed413297d173afe360aad6f52bb5176e84eca7931478cd30ca79a58961
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:13066bdb3f041d79fea341879cf32fc99e1501130aba61e38b5bb537e26c6d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e766d4c7c665af01ecdf3c7f5ebacdb666da09a8f6a3fc562abc8135cc5e5b1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5d60262949712c1e9b418187e3cc8bd5f8d0cd29eb97c9e363914cedaa63b`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 3.6 MB (3561531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4ccf25a7e89dd343d5f776bf03085f2ba18bbad5a4100ece345624e0a595c`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53011f9a2cfb2befb053a53ab616fbc8cdc2c34c7c16c3d64268caf75936a28d`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d8f4ff9e91fa0098e89a942d5178c56e58307eeddb25322eb98cb14237292c`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 102.8 KB (102845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f18bdc3a399429a3003a5facfc548c193056b9f8a3c92159a30cdc1478fdfc`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c63cacdcdeb7eb72ae8539221ee0ebcb57c3925d98bbc09a2a6ec531638dff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c783b424c09b07cd1ef4bfbe1afb9b6a360e746ed91c3589067e70bcefa6ac7a`

```dockerfile
```

-	Layers:
	-	`sha256:0e6a2844b7765ed34907f15e7585e8bdebc12f3faadefd03864a0f5d02a826d0`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 2.0 MB (1988043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314f1c1506cd318e08789d785bcc4374c81b8056d15a4514197f223b08c7268a`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a790631dcdafe28f015c5c0479912489674be9f8f6443c5baa269296a9aac686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6ad30b4f18c93b1b8b0d5ab83d85d1a12a4e4200c5a5b3d74087d39e1af734`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac21e8e96238695c860d38f337d7bc1fc8004ea7c02420374175bd455adc01`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 3.6 MB (3560024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc1ea305697372c2857b25e00b899c927cb6bc69155e067e49c0a9bba9402a`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b43beb4a469f9bf1d5fbbde21ed17e9307737945bc57d9f78fc561d40e08ea`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861dc62479460407739b1ccc0c1b1ed34a4710f546a7bb95fdfa45af3b8efd3c`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 103.3 KB (103339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c89c90922ffd5d5f4ad5e74b112d2030c727ce2904398c5ceef67660d3c259`  
		Last Modified: Mon, 05 May 2025 17:47:55 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f372e8ab37fe59a92e06d06cc943b4f987a2b0248f30c3165bfed88b8836e189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc218ebea555829040d03a4a15c0f5df5da7efb29ac615a2891b238c37f82455`

```dockerfile
```

-	Layers:
	-	`sha256:acbad4c4e58f95388548674e8a027f84744a36ba854c40bcfe075c25f9afc1c0`  
		Last Modified: Mon, 05 May 2025 17:47:55 GMT  
		Size: 2.0 MB (1989088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d3aee94659ed4646a4d848ec65ba5ffaaf28e5be2b04557c641715a24f788f`  
		Last Modified: Mon, 05 May 2025 17:47:55 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json
