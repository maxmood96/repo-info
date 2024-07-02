## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:a767f14018a2ce072d24009b8ba0e78a8a8b6034d76771dae27173c67e1b2f9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:855b77e694874955ad15bf85104b44640f63ba5bb8dec17f20d9fc7bfd39787e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1eae4b1672a293dce535b1ac9db634062cfba88b78bc06b19d5e728fd2f34a8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1604d756665359b6698357f64c36214cc702e053f91cbf48935cb378693bdbe3`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 11.1 MB (11105075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8142e6f550f471f5cfbb60299b5dadb1834c9990404cc1ebec041a40ee31ac32`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8d71f876104bb6419609a349cee3d6afa806fa540993fa175e15277145a10c`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c459269f889157c9a49a9149c17143e09cf412de837b6c261da9cd35f156d40`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 100.8 KB (100770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cda545515bbda09acdbf05c6937d140dbaa297b2352d4374cad1e5b492094f4`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d9d4d495667e632ccab51796f42e78de119e113d34ee5e3dc0285a0e6b1613fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26abba4f9868d5fdf876a1c5e9ee9de4d056dbb051aaa93acf0a915eb6f26889`

```dockerfile
```

-	Layers:
	-	`sha256:a9677d23cd2cccbb095f4c3567f007a43a728126da4d8d2a3fe95cc0b84a4237`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 4.2 MB (4198773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f03d36de37afdb28d38fc2bb23f3fa4516cafb6f80c447e836714da4139cb1cc`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 15.5 KB (15511 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f1e392da199b8dcca45f896a5cab373811b3aa702e8615419c65ddd7edfc74e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64948463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168acf79e5122f2c5e8a5c166e82192cf5852ec99f928fe129b530b1d79bf4b7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ef66b54f3529cd7df198490a60a02b9a4e099ea4456cbc230affa6271d7be`  
		Last Modified: Thu, 13 Jun 2024 19:36:08 GMT  
		Size: 11.1 MB (11105804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf9da50bd694d2938f66745014033d7f272e00c04af58b00384767df0a68779`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d1d085e2488d140f07257a03441112598facbad0671d3f6d3aca4474943da`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6ba47d152985a5fc3c5a383c539496f19f49199c0ba685819566962b387f7`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 100.7 KB (100727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea6100cf3e072ab362a57fe12dc0cbf09696721e80557e4b9e225c44b3cbfab`  
		Last Modified: Thu, 13 Jun 2024 19:36:26 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4da3bf242d095595bc989ae17d7609c596a0b91092deabe0e5f44a7226f92d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46662291b74b853620eac37118bd091db3450215860660763a774ef3e6c7a948`

```dockerfile
```

-	Layers:
	-	`sha256:bd2e2a297ec21ebdd927953ab988ea32549b9e3e2b03857c070c868ad1929315`  
		Last Modified: Thu, 13 Jun 2024 19:36:27 GMT  
		Size: 4.2 MB (4198699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f5aa795607d3ec33b9bbf4089b270c6af4bdd97c4778667c84578e7db6c552`  
		Last Modified: Thu, 13 Jun 2024 19:36:26 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:822b5eb81c6d88e75102be785011df8290a9529b4573e3f70d67556dff41b692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67668031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5091a35ac22ad436b6727f0b16788e507c1f88029353860c7260c138013adce1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e6fa59569d6234c463e39f7c2465f2984240a5e8cd613c1ffdc14ab3abb4a7ad in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:72a2b38d7f88bb9b0be6097180e8f8261c31815017cb512a158422c2bfba6973`  
		Last Modified: Tue, 02 Jul 2024 00:43:02 GMT  
		Size: 56.1 MB (56064975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e8cd48e9ca4cc4b0b2b562b18efdfb2b9c7305b0d2fc8276e9ca59fedca716`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 11.5 MB (11500091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84969a8bfce7a4bbcf743d3b8de90f73b6d07a65ceace905b317bf7c433a124`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206c38a43468a40f690f2dd342899fe8b93fe64c85819f526a846cdecb6f83ac`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c607b4e87b7854fbe117d3447e682ba44cd017ecb5d3e9e462478245de38cf7d`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 100.6 KB (100616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bdac2369935000e838fe374590db260340727edc9e818e7f381f4b358c1832`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:631e7cceacdf88f5852da95f29556d7aeb40ff92403d55affef74d1ac977c784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4210718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db227a06324e4e71ea58e8d1b30f4c42d9696944e73f554fdca355ec639d083`

```dockerfile
```

-	Layers:
	-	`sha256:08722eeb08778da567d8f4b84640b6bde3ba4d4b7235b764a22ab2daf93ba121`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 4.2 MB (4195233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5911ed9a294338206c61740ecc2f6bad0e17ecc5f39bf4ca08270741c2a64393`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json
