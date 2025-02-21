## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:06fa1016d5b778c6aa1f05aa80acaf572138699158582a8751a772733ae08029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d412efc95c809788873dbd59e3cc152b4a29bd511883b353b4c4799417edb33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9ab0393d07a0c127fa6858fc228df28615460ec5bc8bab2620ef50b9c41f0b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fbae250e7e198cb32987f465dac3fd166cf277a544d44493717b32964a9952`  
		Last Modified: Tue, 04 Feb 2025 04:25:13 GMT  
		Size: 11.1 MB (11105098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e60cfdc9ab5b0c2d9afe8eabed1742eac024e6214c3cbda2064224bb775400b`  
		Last Modified: Tue, 04 Feb 2025 04:25:13 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69314e81b8a3f1eb8ef4b48b5fb5ec3ca0a6fc116cdb2c17c83a5da42339ca45`  
		Last Modified: Tue, 04 Feb 2025 04:25:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62177c1dd85fc5249c70ceed9dbeac60b00932dabff93e7c7c89a37b898eb1ad`  
		Last Modified: Tue, 04 Feb 2025 04:25:13 GMT  
		Size: 101.2 KB (101216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701c2c06da71a36f562e6cbd9c7e0222f4f7d1adcc810d47acb45e205a6d4d31`  
		Last Modified: Tue, 04 Feb 2025 04:25:14 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0e482a6e96f681f39841c18e076a5bb87bfac61e0d96595a5da9cb79fe1a74ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc55ca476022589322a51298a9e4bf6f14d75e5fa99b6ed2642bd876619af033`

```dockerfile
```

-	Layers:
	-	`sha256:e21f6820aa5c242f31c5fa53013f952b7bcb420cf63d3d7c3aabc47a644a891d`  
		Last Modified: Tue, 04 Feb 2025 04:25:13 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22fb13b36aea793ab8c20bbd8b3a869294a0a4ae341ed990742b8f45da7af92`  
		Last Modified: Tue, 04 Feb 2025 04:25:13 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:adeffd7d7b4876d93490b45f1bf7db0a31ebe2c91fe557a5ed33e7dcd95afd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e9bc24d7d988dbc1b420003629bdab58a106a6a0f17ca197d784887859b9d3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e95529282fe4b2c53926ffa260e910ca2e7edbe840ec6045501427c2b0fcc2`  
		Last Modified: Tue, 04 Feb 2025 10:14:11 GMT  
		Size: 11.1 MB (11105949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3498b7aa8199bc97f275a3b6d10573f41165c0eb35ce7ff70f2f3ddd65a4f5`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af64b7d26c87753053c75134052452ee120a3493c4d975102854f002f29f65c`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628b5ae84a5cd3de98a4de2b27f64955e4e5e004721258979acdb6b183904370`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 101.1 KB (101102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df83d3c23da0b5df36bdc784ddee25b91909ea0340f81b77341cbd0e75147f18`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b1c2a555a093d89edb798b9c41eec081c742e59307253be2f5bd4a5899147d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9bb42f0dc95e2bf94c144e676c423415a7b1442a83ede8afbd5847ddeea66`

```dockerfile
```

-	Layers:
	-	`sha256:dfae46ead578e6973908c1a2c813a24d46fc554aba3026407ed83cee0b4ddc46`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5c6fe5fa24a9bafc7f0d161f4b11d10f8578478a0e160fe998a3ec5ac64941`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bc4ea7fba92d1e46b8937630fdf7d51c94c052959ad6a6c75f6ab7bc1af6ec08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9669c22464450cd2c1bd3eebecfdcec9a022c2055c248f2bf1236abd9b6ae2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c7d26bfc7a95bb8e1f4dde8a29c174109c237cef20b71a17db258506497871`  
		Last Modified: Tue, 04 Feb 2025 04:37:17 GMT  
		Size: 11.5 MB (11500283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac148139275341abf288eb339ef9be649b924ef1b7419f340f39336983de2fa`  
		Last Modified: Tue, 04 Feb 2025 04:37:17 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5faf29a1de6ba86aad1e315233ed69033548fc77ba65420681265981d9aac7`  
		Last Modified: Tue, 04 Feb 2025 04:37:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e27c3bec56cb39253aaa2da26ef7e8a77aff335cc243b1e00d498180699a34`  
		Last Modified: Tue, 04 Feb 2025 04:37:17 GMT  
		Size: 101.1 KB (101058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11318dbb304a8f515097f73e1a43630f60c6319cce9baf2395e940efd54f9ae`  
		Last Modified: Tue, 04 Feb 2025 04:37:18 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c715f8ea954a803d4b54900d921738ec275c7c0a3b97e4cd22031b41473815ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aa79bf6f033bafd79c6c918e157f33e8ebc207985626f29a9cc45713eb81e1`

```dockerfile
```

-	Layers:
	-	`sha256:2b9be95efb996ff68cd72826dbfc9e322180f7849c2ef0fa58f0589475541d0d`  
		Last Modified: Tue, 04 Feb 2025 04:37:17 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94d00a1b7376996108e8b2ba058acf7184a4f64dcf96407d4fce258d7305c19`  
		Last Modified: Tue, 04 Feb 2025 04:37:17 GMT  
		Size: 15.7 KB (15691 bytes)  
		MIME: application/vnd.in-toto+json
