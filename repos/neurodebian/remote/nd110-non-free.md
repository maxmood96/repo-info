## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:7a88b422cc7e629d2e07257a7fb87dc7c6b6cca5a77c07f6877d40f942db272d
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
$ docker pull neurodebian@sha256:8d4d9a19b705b077eade31b70d52d3b982967423ff556880290833b85f4e12bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ab99c915493086850178980a96c566577b1bf790d140039d5576db9652c7ae`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0f09be120d28122f57d6c89d78d28c5996838af2639d5885c1c072c740ea29`  
		Last Modified: Tue, 14 Jan 2025 07:29:21 GMT  
		Size: 11.1 MB (11106108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11af011f5e8ec6d00e9f3d357d221728137686e62c7f8a14db20b6d886e7689a`  
		Last Modified: Tue, 14 Jan 2025 07:29:21 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761f1fb7ef56305ad67f0eeef85482cc669d802403ef5cb5181fb75bc1d9a894`  
		Last Modified: Tue, 14 Jan 2025 07:29:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec557fa53bda8927e6b8d4fb855a2e16482a8a712c8ee806de23d1260a88f2e`  
		Last Modified: Tue, 14 Jan 2025 07:29:21 GMT  
		Size: 101.1 KB (101128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07640740ca64cffb2679e6e9ebbcbd52716fbe274dcbb27cb21abf70998043c4`  
		Last Modified: Tue, 14 Jan 2025 07:29:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c205f62b8e84faf25003c1cfd05961f1889afb7413b510b55edee6deb835befa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40eafd7cdf6d8079f9a5e86f49b0348154f9ec46ac419011e13cd19cde4ab2f`

```dockerfile
```

-	Layers:
	-	`sha256:fc405f97a4a1c5e299b8951da1b2573407c4cf59ce29d8fd7cee6ca300389a77`  
		Last Modified: Tue, 14 Jan 2025 07:29:36 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1a632f7abed180e4cc8c5d50168d5461cee4446fa604020ccd8fd4a9a957e59`  
		Last Modified: Tue, 14 Jan 2025 07:29:35 GMT  
		Size: 15.9 KB (15861 bytes)  
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
