## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:4f0cb8b6848b98e7f8edba17c7b5e844c65d78f961b6184767f867614c23fcf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1c94397e53817f930ed4d5e28caebf14cc5a22f115bb5603c2c37c4ba28c11f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60938512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556c644b0d54abf62f05f070dea827136fe1f6263c41bf651c1fd4be45f17138`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f9df759d1ff80892b96e37c8ecd4c2ac23e047895ce5f79659fae8e865e1e`  
		Last Modified: Thu, 13 Jun 2024 18:29:06 GMT  
		Size: 11.3 MB (11266600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d1d3dba503d96cd52c1861301a140c2726710a7493f0be87c73d759ba8559d`  
		Last Modified: Thu, 13 Jun 2024 18:29:06 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f26f9e4e062af5edcb1d37f838fcddb0104383e2a5e56abde2db45ba5b1dd6`  
		Last Modified: Thu, 13 Jun 2024 18:29:05 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22351756e8d8e6fa08a1c972549e165375bf3267b68e1d40a6d73943bd1dd898`  
		Last Modified: Thu, 13 Jun 2024 18:29:06 GMT  
		Size: 92.9 KB (92851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5fdb8b9151533c5ea333f1790783ff0f8ee64457b686ef031b420530af455`  
		Last Modified: Thu, 13 Jun 2024 18:29:06 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fe14b0a9e7fc574b4b22149d3227d2ab40e982018d532ebc85f9e7bb02d9c131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5941050f08a8b59609c7d511d916872bbe66e56e0a4f9b4f66fa6435196af3`

```dockerfile
```

-	Layers:
	-	`sha256:aff18923b6a02fe0cca6932278a0e3a6db26e5e03251058e7099ced06bce13eb`  
		Last Modified: Thu, 13 Jun 2024 18:29:06 GMT  
		Size: 3.9 MB (3901779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec30ba7ebdde5950308dbc2fb9bc96d413172c2558a9fe07d8525ce7c428e75`  
		Last Modified: Thu, 13 Jun 2024 18:29:05 GMT  
		Size: 15.5 KB (15510 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6fa28a591c36efdc1697f2072e65da35ce6a9551fed757e3a2ed4d7135961b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60940990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200a12411bb8a28718488fdb38ae529fcef480b2656df0f7ac4238633b8e1ad2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d270226c10537c5802a00393192c0fb6ce225995fd1e617b72cc8b1893001d0f`  
		Last Modified: Thu, 13 Jun 2024 19:37:03 GMT  
		Size: 11.2 MB (11232082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f500bf950058c46bfdb55354351159ba15cfddb415f8f49448974e74f3dc0d`  
		Last Modified: Thu, 13 Jun 2024 19:37:02 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ca1d40890bfea17cf04beac4b006a871d95f00185837a8cc9e24d7fefb182`  
		Last Modified: Thu, 13 Jun 2024 19:37:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463c4479285e39362d940bf891e8006803a23e9f3f4b04aee30ca790994aacf`  
		Last Modified: Thu, 13 Jun 2024 19:37:02 GMT  
		Size: 93.1 KB (93087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e3d2b9b0329bb6e0614407e1df9a443eda2071f3e8d43b812a53ba7ae8f5f`  
		Last Modified: Thu, 13 Jun 2024 19:37:22 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed5b28894e0645ab42d487355543e7fac3dbde20b0b67d804dafb177a5436796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b789835e8f82093cad8ab045bb188aaccaed72ccc706f04b9aa0faf46e929266`

```dockerfile
```

-	Layers:
	-	`sha256:496019fd4a72cfb21f73f8fabeebbba1da1bd34de313e7a033d9dc106e27bc56`  
		Last Modified: Thu, 13 Jun 2024 19:37:22 GMT  
		Size: 3.9 MB (3902020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccffe7f50b259da85d41485fd140c516cb19d622e45f65e57e0c277840bda6d`  
		Last Modified: Thu, 13 Jun 2024 19:37:22 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7d6c8b4235db55cc82515f58088ffe599c694475bf9a61ffdb1458c09c883ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62386687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4239d56f5279cdea7597ea3479ee0379a5db524731ffa3a8897d35c876429e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ffa67f849088d881ec1bd3050a216a615ede2edb4a511728ab5579a4fae22`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 11.7 MB (11688926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d8837ad2608097649f544d67a4577b1866865138f9e8a31b177912f5dce031`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161d8b08f6c9b9bd78b7414abdff21676319fc84d129807f18c1b8bfbe0305ce`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16fdac0c82ae1c1ccc8e105f8f96121d356b25ed71c9e2f32f7b680ee7841fb`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 92.9 KB (92895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad11b88e0c406f04ba1f7bfc5b1e04abf93bbd0bb16200a45f9560e4aa5c536`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:064e42db5fb916ae8be69bc1f8b43ddc7e644e625a376fa6d05eb362ccbf9310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00f6fa8bc6946b7ac2df2495e1bbb4e29e45525ca16dea8af7b9c0d71326442`

```dockerfile
```

-	Layers:
	-	`sha256:4791f9f5accce2cb9c311cea7d28bfda43d210e219ed131cb338a3a4195c767a`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 3.9 MB (3899700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432c1acfda6da922b96c421befb8a54378dbc7ca4b5d79bf4ffc808a14ddbca1`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 15.5 KB (15483 bytes)  
		MIME: application/vnd.in-toto+json
