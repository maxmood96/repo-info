## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:7c96cd01b90e3cb6486bd313a8f01ff628b522070a013f02cd5bad89937d55b4
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
$ docker pull neurodebian@sha256:d1a43d2f25278216c1a9659bfb7c6ec44c80ccd5066649eaf2b0433519242cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ed153cb8527c84eaed449a92f0a656eee5b7d536a5a321c3461a15b862b1ec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f0102900c339db81394076194f5cabc70fd1bd5249b9e279c4c3dff279fa9a`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 11.1 MB (11105025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27e37472add233bbd47e458c8da9afa77fa6eb3b050d84b6a2344733ed9194c`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef3beccf4e525ee8ecb4d8fadaa6b201ac1d55f2e74262d65ae213b3e54144`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64a8c95417d848f4815e9a7b48787a5276ccc3ec7ba73faa304a009fb1d875`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 101.2 KB (101189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fe45998b41628fa647072b6cd3f22a62e5b9e2905f597f1b0a6932f4c4ee7c`  
		Last Modified: Thu, 17 Oct 2024 01:14:15 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f2422cad8533344783d8b8e9380271e3e9e2d273ad283d1e9c0e4d3a70559869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8ba2c3e63c2a0c16de87d27e28cc4d76d86339bba0163ab49426816a18fcff`

```dockerfile
```

-	Layers:
	-	`sha256:889e8208d5f5df28cee3850569bed5963b2617fc3fafa41ac08273dede19fdf4`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 4.2 MB (4223879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd2f394dbcd432364bb73783b3681f40544b3f30d1673fed9ffcea8ff18b60a`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 15.6 KB (15550 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cc787f8d6b0791659d572b06a5fa980290626e3bc3a421b9acb3f75d23234707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64943125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cccdc0177ad7abcdb5602cd2d8f3a5013b464ca19336c1f0bfa4ba7e2c0bf60`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fa9c49640a7a5333f3fea4cc6c5d10542a152ab8c5aa29cf3ce4e3238ef84`  
		Last Modified: Fri, 27 Sep 2024 15:27:29 GMT  
		Size: 11.1 MB (11105819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f59383dbb4959374257665f63dc2bbb1a4b567e04ad57c7117f913c3b10ff`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e727a822f540249948c259f1aa14d33f2495d123ea9d71a46ae031dad3f2dfa`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605ac67eae58773d4ea2de3dbfe0fcd786ceb75b482cf2659454fc879955761a`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b2d89999965d2abe6c3956d01d734a83db7ed22ad6c44fca949da5078f4f62`  
		Last Modified: Fri, 27 Sep 2024 15:27:50 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:21e3436984d7178e7def5e7e4340ac7bd783a5bb22e2932260859cfb022df1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01956dd7fe8e6a0fa7565f0faeb9c3a9e40c6dedb154aff74302501140fee8f`

```dockerfile
```

-	Layers:
	-	`sha256:739059f3f6be9798d36c6fb5e157680422f75fadd6056dda7b1d8c65264fe269`  
		Last Modified: Fri, 27 Sep 2024 15:27:51 GMT  
		Size: 4.2 MB (4223358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d13d210d4aedef2e5938d87c57ae119eea6ea34c896e00f27667ae499ba66f8d`  
		Last Modified: Fri, 27 Sep 2024 15:27:50 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e3be5a5c53975c91cbd979fd670794915bea99bd476d526a357ac2ed86967741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67681619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351ec6e66e29aef5a228977c44b8f85e3f12952fe4d8517681a201038797de6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
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
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79423534cf5965fe2f04fc5e975a694b4f8638b3320caa4c643e9ed24444bbb8`  
		Last Modified: Thu, 17 Oct 2024 01:14:28 GMT  
		Size: 11.5 MB (11500373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480013482db658c37a6c2ffea386ec2af1f1f4c4f5c2f5e2fff0dfbd003657cb`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce407a6bb2bfdc3323339b75bed14f72ccd45b312cc74e36d338dd1ec0ba424f`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8aa075707f8ed6aa84772b58aa32934020c09898ac7f66af7d51ffcd498d5c`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 101.1 KB (101074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ec9646e3b4d8c55e9ecdf6614030b3ed43d718ee92062ed8c317666411935`  
		Last Modified: Thu, 17 Oct 2024 01:14:28 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:447a2ef6cca5559abee275287989f394b1340cd5c1401eee08c935ca552bd6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccb8928053c0e11dca31752e4b544026893738954a0e0b3275e7e5f55121f0b`

```dockerfile
```

-	Layers:
	-	`sha256:ca8421cbbb10d45e2d2886e9f17bb470ba726da45075619590b1c0ce67f4a3b3`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 4.2 MB (4220339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c81157c4a2f79bca7249db43b05996ea04ea5426501cf870045d0eece9cbddf`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json
