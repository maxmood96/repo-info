## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:b159246fa06674c7a64f1e1244ec3fb694292f255eaf8dd14c2da4e97bf31367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:ff78b09dee0b90b68a9263d13b8350bb4a753960b2775177ebdcc49c4a951a06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66679765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd101dbad321af8efd6976b2e659f4c1be93cadc61522907f5f6d73dbc5f3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:02:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:02:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:02:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ded3b2c2e2705491306395f08e76557f7e2f3651c3afef8d378b275b64072b`  
		Last Modified: Tue, 21 Nov 2023 09:04:00 GMT  
		Size: 11.3 MB (11311866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf6d0ca7d99eecd6a7cd31df4a5c04fcc54b7bc95fbc3519c85a9d94ea0b904`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8e54e234dff5f0348e5be547bb64b796452673f0bd183aa678099e28644718`  
		Last Modified: Tue, 21 Nov 2023 09:03:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b00d546a47901fba7ca367a3a5ddf441368999a84fd038f22d24edf494b1331`  
		Last Modified: Tue, 21 Nov 2023 09:03:59 GMT  
		Size: 308.0 KB (307980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:05ae47403683229c382942e9201cc80cec5f93aff3b92fa484586d3f493da6c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491b1d0b41e609f15065b67955fa1e9ad57896dfb61a7785345b6e12ee9a3ffa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:06:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 19 Dec 2023 03:06:06 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 19 Dec 2023 03:06:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a678807dec42582e887390c579155f2ff3f3c25b0fdfeb11854c487bfc0479`  
		Last Modified: Tue, 19 Dec 2023 03:07:34 GMT  
		Size: 11.3 MB (11313652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2434d66e0ac932afe623ab8fb9ddeaf97131cee80959a55990df31cdcbf946`  
		Last Modified: Tue, 19 Dec 2023 03:07:33 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8665dd0adc074adaedc5ecf6d1a9424f986359c007f4c36cbcae0e95056a940b`  
		Last Modified: Tue, 19 Dec 2023 03:07:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9cb0c2c79d2d93968c00288fda1bdc0a21e05ec517669fe68234be55ffd271`  
		Last Modified: Tue, 19 Dec 2023 03:07:33 GMT  
		Size: 307.9 KB (307878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:42bdac607d78c342b9d010ffbf4ab731014da1db8092747d0e8bd54e535e71ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68064908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92da83f63ff7256ee873cf328fac9c99a5068f62517bc346aa23821757a0b40b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:51:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:51:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 19 Dec 2023 03:51:11 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 19 Dec 2023 03:51:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0a042ddf885a246973867761eaeb7097c4ffba0155dc9ecd3c004dd567e6d6`  
		Last Modified: Tue, 19 Dec 2023 03:52:41 GMT  
		Size: 11.7 MB (11708784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b236339ceeaafd4e56a9404e9528b71ad8f45255c5f053e303f89715c4f09bd`  
		Last Modified: Tue, 19 Dec 2023 03:52:39 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92ca1d30df83fb1854dac8182f65566474d229cbccc4c7a4029273bddd4829d`  
		Last Modified: Tue, 19 Dec 2023 03:52:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c554dc1a2dd646999214a1df9a3c0747d1dfb49b0931fd602f90f37f7f2ba84`  
		Last Modified: Tue, 19 Dec 2023 03:52:39 GMT  
		Size: 307.8 KB (307775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
