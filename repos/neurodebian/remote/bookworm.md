## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:151dfcf608141bb4376a422c64a079d053379c6e3bce8d0c49a6d2a1f180eb4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:ccf643c66811d3f406fbdb7d21d61fb9de2d8868b54ed92124f3f43fa62ffcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f328af83b04a88c1894ef4a12cde84bcc28c15325cd2fadd257271ae82dfd348`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:13:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:13:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:13:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570c2f7b7f305f35333a98557b33dbc63cf367789ccebe11042da5774800e05b`  
		Last Modified: Mon, 08 Dec 2025 23:13:35 GMT  
		Size: 11.3 MB (11269734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b4d199b22bc024c53fe984e997f0167b8287262d3467699dcfed3a8fe1625e`  
		Last Modified: Mon, 08 Dec 2025 23:13:35 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db74b3efaa8ccfe41cb7c3dbf9cd53f3b462529d6b3bfba7372ecc6ef953272f`  
		Last Modified: Mon, 08 Dec 2025 23:13:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcf8f0a8586fbb2c7baefcb65560d4e48c6fd0113ad9ee232a2d7961f614069`  
		Last Modified: Mon, 08 Dec 2025 23:13:35 GMT  
		Size: 93.4 KB (93380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aee00c76cfa44edb21613ffa1788688147185b854bbae1bd1eb4806d5ec0461e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f867f42cf3831918f3c30444969ef82eda75a681eef6131654c1fb62e392e708`

```dockerfile
```

-	Layers:
	-	`sha256:4574437d8aed53ffa5dfe7e28dfb808151c47efb0756fe080b372bc0aa845679`  
		Last Modified: Tue, 09 Dec 2025 02:07:28 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958237f6b1f526a1d8af7c4aae5830cd69c120e35e7f36c960721d98c5be9cc9`  
		Last Modified: Tue, 09 Dec 2025 02:07:29 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:50a5a625b28c32c49bccd1b8d57923ee03ea30f76a7ac8f3389642470916bba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ac2181dd0537950d96d6b71f88ff00dd793b6457e2a1bc5e0d058cbb43684a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:51:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:51:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:51:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:51:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62390544d51e9e4e416e49b6d9beb1a6cc3c83979b1221df2a79f2ff23ea921f`  
		Last Modified: Tue, 18 Nov 2025 03:51:39 GMT  
		Size: 11.3 MB (11253505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bd7b45b845c00ce3b9f9b8550fd08ded78e3770e7b6b8c6594f1360627b697`  
		Last Modified: Tue, 18 Nov 2025 03:51:38 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1521afcc0a45d7d89d38fe3092052dab1c78fee7db3ab723626e2c7b2f37c3b`  
		Last Modified: Tue, 18 Nov 2025 03:51:38 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109959872cbd45e0cb947130faa31d3da05f5978e79bda669d4be8d31ae5d9cb`  
		Last Modified: Tue, 18 Nov 2025 03:51:38 GMT  
		Size: 93.5 KB (93539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f756360076a198bf499569584dd893dc71581cd8142f514a7fcae2b7f797f972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7320ee090c63c4ddbef1519e14e84705f7ca28c41758f1ebadd780630514b6`

```dockerfile
```

-	Layers:
	-	`sha256:7e1c5cdbbbea15f5fa8f04f34f1eafe471962d5b9f7d16a8a0240dd5c158c78f`  
		Last Modified: Tue, 18 Nov 2025 05:08:37 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f04f4ad24905c1c37df3cd350cc8d3cb49a3f52670111846504f97240995eb`  
		Last Modified: Tue, 18 Nov 2025 05:08:38 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:e541bd3d6e8c2e350585ff969178f5b1eb50d8c9ba616b7bdbf2f8399c5f14aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7d620a96142dcd3f186a6fe338504785161072efe1e215f5852fcfc5f84864`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f52798efde006ed1cd5f8b1568731b4e192bb8d42469448e91e101a0db4474`  
		Last Modified: Mon, 08 Dec 2025 23:15:29 GMT  
		Size: 11.7 MB (11690144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab9b17f9e8302b4007852306001a4fec79b4040b0206f90e41917f36c14aaf`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80fb5d370b48a0007fee996c5762d278fe813640bb9c94a63fb41e8d8b2e096`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b644a9afbba75e07f7cce8cdc7ddff087b8ce4f882d4922da7656fe6eae3e1cf`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 93.4 KB (93393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:682023088122f95448d674072ec064ed9c5f200510c386b7da9b9572a60dcf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb59ba0285827e553a3b085b7aa8dcc0cb47e214ae0b993a08817c9ad3cfb10`

```dockerfile
```

-	Layers:
	-	`sha256:ee7b2db1f021c38b521cae01de099d8549088a69985b97fdf1eae25474abc095`  
		Last Modified: Tue, 09 Dec 2025 02:07:38 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a489f0243008eccca8a2550085e9994ad5c7db757f3065e9cbac12ae22242e1d`  
		Last Modified: Tue, 09 Dec 2025 02:07:39 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json
