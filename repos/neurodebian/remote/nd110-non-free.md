## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:441ca92c521bbbb0223318d0dbc85147fa5c79ff9ad65324689473eec3ac2f40
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

### `neurodebian:nd110-non-free` - unknown; unknown

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

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:433b10f63bc29bebf93cce594f70a709c333d58888f0c1dae59d8a38e917e917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64930548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e77dbdc7a26728e6fede307180c342d554ae1f60840118690b95095ce2d65b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
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
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea11fc4812146ee0406609bad9931ab449987942af4c11c63743088a1ed032`  
		Last Modified: Tue, 02 Jul 2024 16:00:10 GMT  
		Size: 11.1 MB (11105843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6adaa472f44d4e0fde1bfb9b6682772843d66b15ef7598b4558b66db050d49`  
		Last Modified: Tue, 02 Jul 2024 16:00:09 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff784185d6c577acbfea3c8f77c196ff0c53187329dfb35087fda392ed658b`  
		Last Modified: Tue, 02 Jul 2024 16:00:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f15342e6ff663e4aaa1146d7b0b3b61b678ae6c7a1195f429b23398d519ece0`  
		Last Modified: Tue, 02 Jul 2024 16:00:09 GMT  
		Size: 100.7 KB (100700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb0059251eb4e037e9330a461857c1cc659f97435a2477d29e0dc2f647a50af`  
		Last Modified: Tue, 02 Jul 2024 16:00:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65e2f672d7daed979af9224884286c87f5c60c11f2bf2509a68a7f504d7f3c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d913103204b84b8f9c9dc416cc1b1b59951988f873b2d8a172a315104d520e10`

```dockerfile
```

-	Layers:
	-	`sha256:2617cd894e45708e8ee0010408f0f4692854f007e86dbcaa5e6f16e67176df27`  
		Last Modified: Tue, 02 Jul 2024 16:00:29 GMT  
		Size: 4.2 MB (4198378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:817bfdfc005086a64389cd3a32b12a09ad41707adb504d8ccee86d41fa679320`  
		Last Modified: Tue, 02 Jul 2024 16:00:29 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

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

### `neurodebian:nd110-non-free` - unknown; unknown

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
