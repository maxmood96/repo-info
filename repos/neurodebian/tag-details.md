<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:2e568018d73892b21c1715a9e56e635e716350ac7b8cf61a8017981cee0916ef
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
$ docker pull neurodebian@sha256:ccfe6ca082745c97fa4ba00ac0fe25887b67c92d221e565744d35cf56c0a3625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed82c42a1fdc4026cc2c4ceeff7f950128e2011566e20783e15528b0668b750e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1479a7dfdd7bd71a331fb57263d63a48b18f362276a8d3507efc1dba468dc`  
		Last Modified: Wed, 21 May 2025 23:23:02 GMT  
		Size: 11.3 MB (11266844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3811163e1e52f20133f4a2f726f2743ad294c104a345c4ef4f4da69b9d078fd`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df351ef0700f87809686368ec3b0cfb7da8af39ae9d31bc006aa2bd60ac1ed9f`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1793f6f7307e57ec6794a674c75ce0ce2fd92331fdb2bc2df11fa0a20c8b713`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 93.2 KB (93191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e71bf24417e743e7203e3a4ed63b024a5503c29a6727c49b599ec8c813018f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd40900d4f9231c013ab72c0a9343ece65312a9276382d197774a7855aa9ccd`

```dockerfile
```

-	Layers:
	-	`sha256:e4f564ec6f91cac7f96d55a009199eaa0bb108fc7cd50780a733bf915c2fc0c1`  
		Last Modified: Wed, 21 May 2025 23:23:02 GMT  
		Size: 4.0 MB (3954822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895607a345c49ee9f2d34f2bd8ad0768f41e02c79dd16e5ce4b3c0005f3aecdf`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b99fc050dbe97fce7b2be84bbc74c98d5afa82adddac631d2d46606783d7dd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb89d84092ffa79c342c9d0ce96e517bb5e6f4c7740cb52c4308e59d29e7a39`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 93.4 KB (93443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:24a9982c45872ee44ad75c916770b6e54684d969af7c83f3976797a0f69b2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995ffd9cc5fdbc0dce9f2f9c92f5f9e09db94d23c707ed207103dea6e58ff697`

```dockerfile
```

-	Layers:
	-	`sha256:fe489f993345a9159847e68d85a3fff889d3bec20f51ae60371fdbabd7d6961b`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 4.0 MB (3955076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b54691e54bf95f0c8dac0cd29d7358fc539e3c85d5727d223011e9f57727b4`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:40b9766f674cbe18059a52d9132028b78d1d9732a101ffa3eacca866a11348b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61255830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52468f2219071593b803836c124a97455e373469ae1a6e9be7c13e5f895dfba0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5e346146a229401e10471e4cbbe84a57931d3139ea0434147f07c663d432b`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 11.7 MB (11688893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1255468b95293fb1e60abbe6d77208b9625ac10eca1c246235c3ac7ddfb801f1`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cd2e2bf1a80e558d1befccd7dc91728b49d1c244d7da9339a06a4d7ac3af14`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb862dadada5fb7f5ae18bd37f410686a49ba21bf2d7c577bae16a2ef16ed6`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 93.2 KB (93203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848686458fe8f432331e61cc40d34b67889f849657c2f6783f2a53c3a98753eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c148c8e5d098f166d5f6a24c1c83ec09679603cbbc8c6fd8c3efd9377a3b8bb`

```dockerfile
```

-	Layers:
	-	`sha256:5c09dd3adb1cb49760d6fb3a008b82184b82580e7331d7f6df9827955bfbfbe0`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 4.0 MB (3952790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915e7352977df39d05b78465ba9906fc5569734a50655cd7c22622a7105e20ae`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:b0fd02fb64867772094c3388f3fa12061f0b1641292c3eb9d4514f5c667eac4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:851e63864831469546085f6a457288bab67ac55db23fe8184195c000da461f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1140577c4fa48a7d165ccc461ad7e892f8c319ffc1838973c42f4cd47fbe908a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682aa3f8a7a0c6b2c3f7e69082a7641b2f8a398db39cea59e30577ab2cd9545c`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 11.3 MB (11266852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74fe3db0b2d5102c748c1dced6a2d654dcfe6325440f5ad12c7d15b9e2a4ca`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b621e6e6f14028ed190e855d6f2b7332388d7d99f86177c0839d80572400cfb2`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686d88df96b49bdf2c13c3a23f6cb8d645961840a556883c3cc5b79b9185eb01`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 93.2 KB (93186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6586d320bf1e1e1821085a599b7260b177db8d637dffbc69299cb7848af335c`  
		Last Modified: Wed, 21 May 2025 23:33:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa004cfcf0e1cb0d21a28babe2049d496a76da2dc5adddfdf974e2f8efad05d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061fdf2951dbc561a9c508a39236c8c3dd4a204b208530753faaa768e80ac32a`

```dockerfile
```

-	Layers:
	-	`sha256:305ee82f38619bafff21cca2294c2411ee720c40e0020e78825eeb6c523714a2`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 4.0 MB (3954862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b44bd6c10531f89f0b05cc959d4ead7f25c043efd5e5810173fa6bf75fb2de70`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f0b21e9a2b1d87e8e9d1cf617208198e10c617d9f80b1339ff54ce27ee66c91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36204bccfc429d1ecc0ab3e4cb4d125b9a3f7594aa42d97f2f51c173dce13323`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 93.4 KB (93443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89280029104abf21945b59b054a3eedf9f7b23e94999b1aca58011419c300a`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7e6da63402e4b1eef862b0d8a3f101017276aecf02c60186b794120fd687915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107dbd281f4baae96d89cf725ff834951638204a9503b9812136446b2ad9caf4`

```dockerfile
```

-	Layers:
	-	`sha256:b4f000b0ebc61fecbc86e06e322d07a3aca6d8fa3ed3c9d7d781d5c75cbcf560`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 4.0 MB (3955116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73550faaa5db727c23fdf4536980baf5f17f7a89739abf435a3879571e512a4`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bfa199662e75b2c37492367434358c210d8a355f2bb15868b5b769db9193be49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61256320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b532a8a00c0c0d7b9dd3f7f594b120af5664d70270ca19502f4e7bc233aace4c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2befdc47cd4cc9a43be4226914197171d517dbe40274f5b26c8088cdbcaa2b9c`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 11.7 MB (11688920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1bfa09a90b3a837330dd2a72b46dca98d510d8427fb5b9162ae3be7a83bba9`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18aa48402f14aa565c4a322fecbcc79be120249f1f6245662825df0b4a4d37a`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c2353a2d9dd0fffbf5018f9fc815a0ccef03054aee9386f0bfbb9f4d63b6d4`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 93.2 KB (93217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db8ce6f79b3373f6fdcacdddb049c597fb580b389a159ada0336d9dc29e05c`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc54ac074ea1a6afab79cac6dfcfab8d9003737aa056274f441cdf463fd1528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3920c7ac1fba6d508e7195907458fc78fa48d79d67c362e3e13a116d968ef667`

```dockerfile
```

-	Layers:
	-	`sha256:afa6979159e91d00fa568b799a399cc939346264429fe4419c17550b77367215`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 4.0 MB (3952830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b28f32383b18cc13b5a4e44e0a3ca98b957af3a8d6c2667e4b7ab8c4a5dd80`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:3315ee1a27832a89378e4f2636ef27f4efa4c0c3a94fd999daf9ce2382ea7e96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:96c1c951bca715e6d337f7cc2ef3dedd38bc2772dcb12d1c550040ab04ec1884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64958550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17eec14af4306dfdd475136b4bfafb95a2a76b37f1345c750e8cfcc4a98a5b1c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470a16785ed0074295002c533632f65140ee1e5655c3e51026466bf8eb57fd4c`  
		Last Modified: Wed, 21 May 2025 23:22:58 GMT  
		Size: 11.1 MB (11105018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875f413f88db273081bdf04d81e663ec5201e9b626f42ec01033462ebe247351`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc1e8d628fd6131dc4a548803f430ff460f19615a548d9abcf80c734137bb6`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3239c21ef74426bcd266e0b79c4f3f8f0fee1a5b14829a0cb42ebf63bdf5e2`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 101.2 KB (101179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6fdbd6d12faff6c8195287f01313c99394d360c36b2b7a032fa0688e4051de71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4273391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7314d6a9cffff62e824bd8e341e80824e8ab05582ae82a5762dc7e4c9fa17c05`

```dockerfile
```

-	Layers:
	-	`sha256:841ba6eaf618f16697cb76de46914854930cf747378312b3d3e6839f987dbe01`  
		Last Modified: Wed, 21 May 2025 23:22:58 GMT  
		Size: 4.3 MB (4259382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a1db1f9da357a617912bec9c5f859f648d382c2e3bb93ea9bb66051fb890c6`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f6ea5c2d91ef0725d4a5ad5cd7125f80b3fc78ff261238fa7c4d9f75b37e1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6873213ee173fc0021a00d8b7d220c1d2216db447ef3644e158f2a2b05e69a06`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Thu, 22 May 2025 03:19:19 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:61a931e647ad16337d4f09e239754e94547af9d7946cb1869572b5ca182da3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4273123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea337907d2f184a758c15db149c8c91fc3a44aec85d6a4ee0b8617add242f04`

```dockerfile
```

-	Layers:
	-	`sha256:33d48daca7db678746999e040dfd483fd2b62b4a311c170482f61deec548557d`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 4.3 MB (4258989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40dc3b54ca56f986bfc00993e3cf39fcb4d7301bcdcac2156bef0c4f29bd42dd`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:3bac0302ebc07dfe32953f6b8bde1779e8a4c934c1849b29f4f5b27f73b91a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e43515aec23d33e64eded42228a7e8916e6617658b8f5a0ec59f2be05534153`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d01ecfb2dd2080228a66d2fdf37f1ab66fed38adf6f82e03695c4117e495be`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 11.5 MB (11500350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60718ab3a6aeabd6508fd884c90aa6bdabf632cf06736d0b3cf7abe946afc77f`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca14452b5d0080f4c73b943509528a7ec1aba4f3a5efee283b88f7a9f6bac7a`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc2bd4f2d999d9d435921052461765c30b0b7288e9876cd6fa27b297ca2a021`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 101.1 KB (101064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7595abce688cc7ef89a5d5548b1c09500cd70abc10690152aaf06fd3c9c34c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4269882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9bc6369c18c99db3919c609b56a0557016c7367285c30ed8fd17da0150b9db`

```dockerfile
```

-	Layers:
	-	`sha256:9a126522203aa48571405dd8087773eeed31fae31cc354739cac1eaf97f342f2`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 4.3 MB (4255901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29409dbc3ce4091e1421562f90700ac344f7a0dbab890bf3e1c9451342a2a382`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:77c47c7668866764a9122387e7419916c7c8d85aff7f5a1ce83c1e3364195be9
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
$ docker pull neurodebian@sha256:246a6cea29bf1e53a63f2df1fa30567895cfdd762588b7a18d23e8f9ad82f454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64958971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e7f339bf19897ed357c21d32de33023e06c814327decd8cea75737758fc620`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca25855464c362ff5b431ed1c58bcac1d3074d341dfbe0b69db0c4b7b06ddfb`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bd852d80e3b0c678ae63bfb3948aaedb9a85ffee30335e3517dfdb5079959d`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755cd40c0c29cc545f889321eb72bcbd161b6e91d0f0b1b7e45ff98558c28ca2`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4067042efe9918fc632e3430f0139557b52b74d633b305ae3271d19e6436a4a6`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762595f10379f52572d8fd283315b81ce1b9219d0093d67e34f012a23d953ce0`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5c68454aa7e6353c94c501e6d14d0fee25f41e3af967fa9d7929a1fa53c2d33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4275455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00e6656fe42ba476e7319395892b61dd62ce9e32b70cc90b728550196d2864d`

```dockerfile
```

-	Layers:
	-	`sha256:f0af86d5157ce7d3378518d30607cc486e5a125dce2db026e7967a909b8826da`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 4.3 MB (4259418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d960478801780d84e84a55651c3c2b08d38fb5d627fa32b2e14ea9edb0c29`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:35cfa864205249d1d4e82504829a5f5aa992c2d184e55290bbb0d1af4dd05023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45c8b2299769ab81320368fa621d518caaa4dd7850a06661e4a8369452622c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Thu, 22 May 2025 03:19:19 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd4d56a7262cf9c7a1b114c72ceb3299228df837a1640a8ce90628bd5c963b1`  
		Last Modified: Thu, 22 May 2025 03:19:31 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7c666df1009a09dcd1bbba24ba9169ee5ff609d9945c900d9b868ca55e8fbbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4275202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f951394aedf3782b624e9bd05e62a2d1f23bf36f0a4d9531db99d61cdad249`

```dockerfile
```

-	Layers:
	-	`sha256:007a6fcd8d32772a7c49365a7cb79a2f7def3249337b36bbf7b5868f48c256bd`  
		Last Modified: Thu, 22 May 2025 03:19:32 GMT  
		Size: 4.3 MB (4259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec65fca109040eb81ff69488061cea5448ab551ff306c257491499a58e6bd282`  
		Last Modified: Thu, 22 May 2025 03:19:31 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:354b07db5d7f3f3ccf58d06ef3859976a429f941a35da01c12412d09a93f90ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5dfab42d2d147736ab665221a26bcb8c9cfb8de220dcd99ae2e231a180902eb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb82b38255af376127b720c3434c7588d795cf564324a00430b2e96651baa61`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 11.5 MB (11500246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829d9657d4d662f0da64ae1af4cf6886eff04007f3845ed03cf24b904192bd79`  
		Last Modified: Wed, 21 May 2025 23:20:16 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d687c2c1ddde860df043e0a7972ca660e64f07726254450e3b965eb4c222c8ed`  
		Last Modified: Wed, 21 May 2025 23:20:16 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3157e5a3bb34d5c229b87fe8a5f4cdbb169c5ab8176a02ad6a7b54f6cba873f`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 101.1 KB (101061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d80bac826a6ab24fbd286405cff47489bdf4673594316ec5e86c17c2c57e061`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b86338e7e377c60cdcb2dc43c9fa4b78c0f552887e78cc5b614313337dee915d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3d014f6e237e0cd1607930875f138176cf59c131019cd3fb2e0a02ef049b0c`

```dockerfile
```

-	Layers:
	-	`sha256:a64b7f8aae914ada58530ee812e30cb786ad7fadc5ede081b18a88a6fd946e85`  
		Last Modified: Wed, 21 May 2025 23:20:16 GMT  
		Size: 4.3 MB (4255937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92565edc49b85cf72d56f5a48654518b0c5ad31ce49b271befd3cbacbcc166e5`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:e68b01fb0dea971fa4cfd39d8feb687c3fe2aa4bd228ca5e72189d11d8c78908
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:ec026f26f90a1da8ffc3ba59281854c0bb1a0b5f166e58e75d57f34e8424bd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa3d04109e9bf85dbba55e27e2b0055d3c73ba8b1f21907acb2c7bdb223320`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabac9a159eac99d387c3b1a92d15536e78c12f6596c2dbd37f29d0b63d5dffe`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 5.4 MB (5362390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e9f035d7685c2fdb1e905a640424e5ad669ee2970a32cbec7f8d889e3625f1`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb125018a09465c3a7d0200be55fc6435a06fe742fd5a7a7ef39a0fb83cfbf6`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46b9b7320bd76241047fcf77910ba82992b5e91e204eefe5390b265739db65`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 105.4 KB (105439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed731be31bff11d448e1a27d734e900b2e674625af668b3f9b87ba45b1a8f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fb983f465508bd38f2970b20fcfd3052779b73f8d3b436c6ab4ff79915307d`

```dockerfile
```

-	Layers:
	-	`sha256:079d7ce90a22f0bd844b80ccfaee90ce51150b4f1244f3519448f12bf6c83630`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 2.0 MB (2017825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d275b201a8175e6493a6207f8e73ff2b18780007de8ef8e54adc086578431b8d`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:39c9bfd66371de386419abe34cd806357a534145fbce48504409d1f8f396a4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45aed6d0d9e4f56fcf7aaaad06b6a747462168128f4a0d1f3e2084772af72fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2952dad8358145d90322cccd4047ea733f93fc11fed56791f2817ddc6d99d545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0237cdae437eaedee949f6af64e985420e981a9dfa9474fce1bb2e9aa7fbb8fd`

```dockerfile
```

-	Layers:
	-	`sha256:f307ef0a8e38175dd6e3ceb807d756938a14b991426d356ef4e8432d33ab7e37`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 2.0 MB (2018054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8946cab190197295b0fd0de39d4d1f5d0e06793a5eb36d0073e79597d9fd10d1`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:4c1ed82e5488cc7a87a4035c84b91368bf439418f76c388be8923760e27cc034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5b5f12c95fa70eba84ed0d9a8cfd320ff1f928e0f4ecc665553188865bc1fdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77302996458a5ea42a30e362fe60a32b80399042312ed4461165057feaadc3a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09894bd673fc3443fa4aac9c04f3790e80821023e1b647cb36b0dbb3295685a1`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 5.4 MB (5362436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b567f68d429f42a824fdac7d380831ff3ee4e919d2c1f56ac4ba2d5c728dab9`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe211eff3c4623dbc046e34c08495b6c3665295d30178fc8053cd5baff9b469`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93ed51b316d633e53abd6403ccacb66bf2b80b807810d40df2342572077415`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 105.4 KB (105442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca65e65a74419b6f595b799268195de974952d7e1558d9a39092265337398f`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:451612c81608c2bebc8d3e36a6a521b28025afe8d027348134cdac02a7ec34d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e43683e94761e4cae4d1f50b39b3b1ced64f4fb773232eb29f20df0b386bb`

```dockerfile
```

-	Layers:
	-	`sha256:79b4a3ef3b60d9c20c2340237fe4236376a35581ce8f29f76d044ea8920b97d3`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 2.0 MB (2017861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd949e8f808ff83620701f51061d8dc60e04b6e7afc9a968a71e3ed0ef991e1`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b31849bda994a89ea1e43d1ee83490728e5c84d98e21bb02362919c0ee14a139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9884153e1d1e0355067632367672016383e04b73464a2d8661e4d01f7cf3d14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8215c91245c0463263d03909dc6267e663f8bc6ca035c5fa1478e3632affb97f`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e0dd953f78b0d8045d26f7afb42c726a2cc4e07a96a2b3b741316ca99534d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea7d3f1b864509ea868bded897bb9ca30f452582999b77e73c6bfc798dd9443`

```dockerfile
```

-	Layers:
	-	`sha256:1fcbe13a76f25efb5f459970d227c4628a1a8f71064188a5cd94ffb6874dd526`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 2.0 MB (2018090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dac00fd22e65ab791eda65319d76e0834a665f17c3cf1d1784f781fa3bcd68`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:a62ad433a27fe25a8de7f951e4212508ae8d406477c0b32dc47385b9799a5f1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:5c6093825b977242a0c5ce777463f22291467f3213ee9967d63ad853cad62b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0159f21b56dd611102fd38c93c9b9db6747ecff96ad393e3a308e6b9a27338be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaae9adeb5784f217b1fccbfde587bde5f5a4eef001092646b8beb2b6083091`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 3.6 MB (3624137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13bc798486b3ed6c830d97b2bbead94f4fba215db043fa3784384ab67490f7b`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5403824352add24fb2c4ff3c15449271afc3ecff86b4c3ceaee1884051b6b38b`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8cf2c0a6fd0753dac46ff04bd86d6df6b583a2e5e3255cf4a0a914a7af892`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 110.6 KB (110554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cc4e8e5db5c9f889fe8af12a7c454a321cafb97ce2f6eb5726d0cf2334a61d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2094402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa173a2f1b0551b0755668bd7412967e18454e29d78df0e7fdc4eb9697d84f3`

```dockerfile
```

-	Layers:
	-	`sha256:d5df8adfd2250d8e942803d58a02b3042f130a0b08a3032e2f92fe6ebc663de0`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 2.1 MB (2080426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8db84911c2b9570d62209aca26a6603452311f1d2675ca00a4d45b6e0e0e45`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9d73162a14eddeaa42de80b66ebb46ce4058a34b7e8f278ebe76b01bdfe8218c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31063851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6641bfdb2031f8162a237d8747ec26d21147022b969270ac106464d19f1c9cd1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Fri, 30 May 2025 23:34:51 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e930d912712ee307694bc8edc2665e13ab5ffabd52de3c434ea3e9debd56da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2094787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da916fbb9e734f060ad2c0386b3dde6822474e043cccbcb4c4b5700a6eeeeb05`

```dockerfile
```

-	Layers:
	-	`sha256:55487635e34c1575a1c86ad1538db4eae8185f9b358bc3b2647c7b10c50a9639`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 2.1 MB (2080686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6afd8ad60b0744690a9d8df1fdde507192154666dd867a3ca02ad6d8a4e9430`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:7481cf83e704b3af7a5b48b3edcdaa6c8359604a90aee37431c2027bc8d9f36a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:106a157335593089bd9167471a43ac4e4a300c21bca0dfac7ab5e8ca330e11b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c425b94e9e05e94a3588a5ed5fa50798b770c5964ee80eb3108e2c2b854734`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833f05bf4a56287336922533369cb272b043579abea2c4588fb7a28586dccbb7`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 3.6 MB (3624096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5f30655f789d9aaabd83e43e19fd42000e70a6d62d06ddf046576bfb3eb56`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b76c5daef076a6ef3131ece85a9ede4b5366f8b35563943c61f3ca36393de48`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b346a922dadb495203fa86390fce5ab7f4746b373ff8ee37ae89b1570fab89`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 110.6 KB (110563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96bb241c37c54f5099c6ee4be792e3df22a12f314a81846062a58b160223e7a`  
		Last Modified: Tue, 03 Jun 2025 04:16:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8aae46358cf11c3d67fb2b0bf9adbc7de24122f7bcae1bfe2c595b1a62233e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2096668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14479c1656b173c0100892f3c715ee08d6396fbbddd70f0eb6c7d400c28dc177`

```dockerfile
```

-	Layers:
	-	`sha256:1e817e7f07a5533079454f7b46be380fb1a89f65ee260bfd9d08395ebf6e86fa`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 2.1 MB (2080462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb30aac33316b47ec98bca470a0a0a66269cdd7aa22f62d98e749d5c5e1c494`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f069651f05d3e6c7a096a41a3242a53b7f5067e15c35b139bc0844d2c622254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b33835d3e532c457a861b46b17a2ecc210b0019baeec6bf4b85319109ae9d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Fri, 30 May 2025 23:34:51 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc12a5156209348208485de93d3b89460edf23f23fdded16678f39a46448c25`  
		Last Modified: Tue, 03 Jun 2025 05:19:07 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2fb96a9daec1ce2a7e9ea4dd1144aa633c2bc1d97d73ba0bece51586ec46fc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2097068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25ae2c3ba2f40b6fa187203997315827f50c3c023a8f4ce4137f6b8994a5c1`

```dockerfile
```

-	Layers:
	-	`sha256:f8f474f858ffefa2d71ad93a00640e481fbbfd9d23b677cb8ee70750c1123694`  
		Last Modified: Tue, 03 Jun 2025 05:19:07 GMT  
		Size: 2.1 MB (2080722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09220ec00b43fe2a6638b49308e372f11987cceec9eefdf11f6781cec1b7a417`  
		Last Modified: Tue, 03 Jun 2025 05:19:06 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:2e568018d73892b21c1715a9e56e635e716350ac7b8cf61a8017981cee0916ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:ccfe6ca082745c97fa4ba00ac0fe25887b67c92d221e565744d35cf56c0a3625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed82c42a1fdc4026cc2c4ceeff7f950128e2011566e20783e15528b0668b750e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1479a7dfdd7bd71a331fb57263d63a48b18f362276a8d3507efc1dba468dc`  
		Last Modified: Wed, 21 May 2025 23:23:02 GMT  
		Size: 11.3 MB (11266844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3811163e1e52f20133f4a2f726f2743ad294c104a345c4ef4f4da69b9d078fd`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df351ef0700f87809686368ec3b0cfb7da8af39ae9d31bc006aa2bd60ac1ed9f`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1793f6f7307e57ec6794a674c75ce0ce2fd92331fdb2bc2df11fa0a20c8b713`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 93.2 KB (93191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e71bf24417e743e7203e3a4ed63b024a5503c29a6727c49b599ec8c813018f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd40900d4f9231c013ab72c0a9343ece65312a9276382d197774a7855aa9ccd`

```dockerfile
```

-	Layers:
	-	`sha256:e4f564ec6f91cac7f96d55a009199eaa0bb108fc7cd50780a733bf915c2fc0c1`  
		Last Modified: Wed, 21 May 2025 23:23:02 GMT  
		Size: 4.0 MB (3954822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895607a345c49ee9f2d34f2bd8ad0768f41e02c79dd16e5ce4b3c0005f3aecdf`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b99fc050dbe97fce7b2be84bbc74c98d5afa82adddac631d2d46606783d7dd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb89d84092ffa79c342c9d0ce96e517bb5e6f4c7740cb52c4308e59d29e7a39`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 93.4 KB (93443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:24a9982c45872ee44ad75c916770b6e54684d969af7c83f3976797a0f69b2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995ffd9cc5fdbc0dce9f2f9c92f5f9e09db94d23c707ed207103dea6e58ff697`

```dockerfile
```

-	Layers:
	-	`sha256:fe489f993345a9159847e68d85a3fff889d3bec20f51ae60371fdbabd7d6961b`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 4.0 MB (3955076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b54691e54bf95f0c8dac0cd29d7358fc539e3c85d5727d223011e9f57727b4`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:40b9766f674cbe18059a52d9132028b78d1d9732a101ffa3eacca866a11348b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61255830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52468f2219071593b803836c124a97455e373469ae1a6e9be7c13e5f895dfba0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5e346146a229401e10471e4cbbe84a57931d3139ea0434147f07c663d432b`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 11.7 MB (11688893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1255468b95293fb1e60abbe6d77208b9625ac10eca1c246235c3ac7ddfb801f1`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cd2e2bf1a80e558d1befccd7dc91728b49d1c244d7da9339a06a4d7ac3af14`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb862dadada5fb7f5ae18bd37f410686a49ba21bf2d7c577bae16a2ef16ed6`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 93.2 KB (93203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848686458fe8f432331e61cc40d34b67889f849657c2f6783f2a53c3a98753eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c148c8e5d098f166d5f6a24c1c83ec09679603cbbc8c6fd8c3efd9377a3b8bb`

```dockerfile
```

-	Layers:
	-	`sha256:5c09dd3adb1cb49760d6fb3a008b82184b82580e7331d7f6df9827955bfbfbe0`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 4.0 MB (3952790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915e7352977df39d05b78465ba9906fc5569734a50655cd7c22622a7105e20ae`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:3315ee1a27832a89378e4f2636ef27f4efa4c0c3a94fd999daf9ce2382ea7e96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:96c1c951bca715e6d337f7cc2ef3dedd38bc2772dcb12d1c550040ab04ec1884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64958550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17eec14af4306dfdd475136b4bfafb95a2a76b37f1345c750e8cfcc4a98a5b1c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470a16785ed0074295002c533632f65140ee1e5655c3e51026466bf8eb57fd4c`  
		Last Modified: Wed, 21 May 2025 23:22:58 GMT  
		Size: 11.1 MB (11105018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875f413f88db273081bdf04d81e663ec5201e9b626f42ec01033462ebe247351`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc1e8d628fd6131dc4a548803f430ff460f19615a548d9abcf80c734137bb6`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3239c21ef74426bcd266e0b79c4f3f8f0fee1a5b14829a0cb42ebf63bdf5e2`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 101.2 KB (101179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6fdbd6d12faff6c8195287f01313c99394d360c36b2b7a032fa0688e4051de71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4273391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7314d6a9cffff62e824bd8e341e80824e8ab05582ae82a5762dc7e4c9fa17c05`

```dockerfile
```

-	Layers:
	-	`sha256:841ba6eaf618f16697cb76de46914854930cf747378312b3d3e6839f987dbe01`  
		Last Modified: Wed, 21 May 2025 23:22:58 GMT  
		Size: 4.3 MB (4259382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a1db1f9da357a617912bec9c5f859f648d382c2e3bb93ea9bb66051fb890c6`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f6ea5c2d91ef0725d4a5ad5cd7125f80b3fc78ff261238fa7c4d9f75b37e1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6873213ee173fc0021a00d8b7d220c1d2216db447ef3644e158f2a2b05e69a06`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Thu, 22 May 2025 03:19:19 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:61a931e647ad16337d4f09e239754e94547af9d7946cb1869572b5ca182da3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4273123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea337907d2f184a758c15db149c8c91fc3a44aec85d6a4ee0b8617add242f04`

```dockerfile
```

-	Layers:
	-	`sha256:33d48daca7db678746999e040dfd483fd2b62b4a311c170482f61deec548557d`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 4.3 MB (4258989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40dc3b54ca56f986bfc00993e3cf39fcb4d7301bcdcac2156bef0c4f29bd42dd`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:3bac0302ebc07dfe32953f6b8bde1779e8a4c934c1849b29f4f5b27f73b91a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e43515aec23d33e64eded42228a7e8916e6617658b8f5a0ec59f2be05534153`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d01ecfb2dd2080228a66d2fdf37f1ab66fed38adf6f82e03695c4117e495be`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 11.5 MB (11500350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60718ab3a6aeabd6508fd884c90aa6bdabf632cf06736d0b3cf7abe946afc77f`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca14452b5d0080f4c73b943509528a7ec1aba4f3a5efee283b88f7a9f6bac7a`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc2bd4f2d999d9d435921052461765c30b0b7288e9876cd6fa27b297ca2a021`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 101.1 KB (101064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7595abce688cc7ef89a5d5548b1c09500cd70abc10690152aaf06fd3c9c34c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4269882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9bc6369c18c99db3919c609b56a0557016c7367285c30ed8fd17da0150b9db`

```dockerfile
```

-	Layers:
	-	`sha256:9a126522203aa48571405dd8087773eeed31fae31cc354739cac1eaf97f342f2`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 4.3 MB (4255901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29409dbc3ce4091e1421562f90700ac344f7a0dbab890bf3e1c9451342a2a382`  
		Last Modified: Wed, 21 May 2025 23:20:15 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:77c47c7668866764a9122387e7419916c7c8d85aff7f5a1ce83c1e3364195be9
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
$ docker pull neurodebian@sha256:246a6cea29bf1e53a63f2df1fa30567895cfdd762588b7a18d23e8f9ad82f454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64958971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e7f339bf19897ed357c21d32de33023e06c814327decd8cea75737758fc620`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca25855464c362ff5b431ed1c58bcac1d3074d341dfbe0b69db0c4b7b06ddfb`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bd852d80e3b0c678ae63bfb3948aaedb9a85ffee30335e3517dfdb5079959d`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755cd40c0c29cc545f889321eb72bcbd161b6e91d0f0b1b7e45ff98558c28ca2`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4067042efe9918fc632e3430f0139557b52b74d633b305ae3271d19e6436a4a6`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762595f10379f52572d8fd283315b81ce1b9219d0093d67e34f012a23d953ce0`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5c68454aa7e6353c94c501e6d14d0fee25f41e3af967fa9d7929a1fa53c2d33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4275455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00e6656fe42ba476e7319395892b61dd62ce9e32b70cc90b728550196d2864d`

```dockerfile
```

-	Layers:
	-	`sha256:f0af86d5157ce7d3378518d30607cc486e5a125dce2db026e7967a909b8826da`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 4.3 MB (4259418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d960478801780d84e84a55651c3c2b08d38fb5d627fa32b2e14ea9edb0c29`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:35cfa864205249d1d4e82504829a5f5aa992c2d184e55290bbb0d1af4dd05023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45c8b2299769ab81320368fa621d518caaa4dd7850a06661e4a8369452622c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Thu, 22 May 2025 03:19:19 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Thu, 22 May 2025 03:19:18 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd4d56a7262cf9c7a1b114c72ceb3299228df837a1640a8ce90628bd5c963b1`  
		Last Modified: Thu, 22 May 2025 03:19:31 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7c666df1009a09dcd1bbba24ba9169ee5ff609d9945c900d9b868ca55e8fbbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4275202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f951394aedf3782b624e9bd05e62a2d1f23bf36f0a4d9531db99d61cdad249`

```dockerfile
```

-	Layers:
	-	`sha256:007a6fcd8d32772a7c49365a7cb79a2f7def3249337b36bbf7b5868f48c256bd`  
		Last Modified: Thu, 22 May 2025 03:19:32 GMT  
		Size: 4.3 MB (4259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec65fca109040eb81ff69488061cea5448ab551ff306c257491499a58e6bd282`  
		Last Modified: Thu, 22 May 2025 03:19:31 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:354b07db5d7f3f3ccf58d06ef3859976a429f941a35da01c12412d09a93f90ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5dfab42d2d147736ab665221a26bcb8c9cfb8de220dcd99ae2e231a180902eb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb82b38255af376127b720c3434c7588d795cf564324a00430b2e96651baa61`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 11.5 MB (11500246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829d9657d4d662f0da64ae1af4cf6886eff04007f3845ed03cf24b904192bd79`  
		Last Modified: Wed, 21 May 2025 23:20:16 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d687c2c1ddde860df043e0a7972ca660e64f07726254450e3b965eb4c222c8ed`  
		Last Modified: Wed, 21 May 2025 23:20:16 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3157e5a3bb34d5c229b87fe8a5f4cdbb169c5ab8176a02ad6a7b54f6cba873f`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 101.1 KB (101061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d80bac826a6ab24fbd286405cff47489bdf4673594316ec5e86c17c2c57e061`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b86338e7e377c60cdcb2dc43c9fa4b78c0f552887e78cc5b614313337dee915d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3d014f6e237e0cd1607930875f138176cf59c131019cd3fb2e0a02ef049b0c`

```dockerfile
```

-	Layers:
	-	`sha256:a64b7f8aae914ada58530ee812e30cb786ad7fadc5ede081b18a88a6fd946e85`  
		Last Modified: Wed, 21 May 2025 23:20:16 GMT  
		Size: 4.3 MB (4255937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92565edc49b85cf72d56f5a48654518b0c5ad31ce49b271befd3cbacbcc166e5`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:2e568018d73892b21c1715a9e56e635e716350ac7b8cf61a8017981cee0916ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:ccfe6ca082745c97fa4ba00ac0fe25887b67c92d221e565744d35cf56c0a3625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed82c42a1fdc4026cc2c4ceeff7f950128e2011566e20783e15528b0668b750e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1479a7dfdd7bd71a331fb57263d63a48b18f362276a8d3507efc1dba468dc`  
		Last Modified: Wed, 21 May 2025 23:23:02 GMT  
		Size: 11.3 MB (11266844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3811163e1e52f20133f4a2f726f2743ad294c104a345c4ef4f4da69b9d078fd`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df351ef0700f87809686368ec3b0cfb7da8af39ae9d31bc006aa2bd60ac1ed9f`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1793f6f7307e57ec6794a674c75ce0ce2fd92331fdb2bc2df11fa0a20c8b713`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 93.2 KB (93191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e71bf24417e743e7203e3a4ed63b024a5503c29a6727c49b599ec8c813018f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd40900d4f9231c013ab72c0a9343ece65312a9276382d197774a7855aa9ccd`

```dockerfile
```

-	Layers:
	-	`sha256:e4f564ec6f91cac7f96d55a009199eaa0bb108fc7cd50780a733bf915c2fc0c1`  
		Last Modified: Wed, 21 May 2025 23:23:02 GMT  
		Size: 4.0 MB (3954822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895607a345c49ee9f2d34f2bd8ad0768f41e02c79dd16e5ce4b3c0005f3aecdf`  
		Last Modified: Wed, 21 May 2025 23:23:01 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b99fc050dbe97fce7b2be84bbc74c98d5afa82adddac631d2d46606783d7dd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb89d84092ffa79c342c9d0ce96e517bb5e6f4c7740cb52c4308e59d29e7a39`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 93.4 KB (93443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:24a9982c45872ee44ad75c916770b6e54684d969af7c83f3976797a0f69b2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995ffd9cc5fdbc0dce9f2f9c92f5f9e09db94d23c707ed207103dea6e58ff697`

```dockerfile
```

-	Layers:
	-	`sha256:fe489f993345a9159847e68d85a3fff889d3bec20f51ae60371fdbabd7d6961b`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 4.0 MB (3955076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b54691e54bf95f0c8dac0cd29d7358fc539e3c85d5727d223011e9f57727b4`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:40b9766f674cbe18059a52d9132028b78d1d9732a101ffa3eacca866a11348b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61255830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52468f2219071593b803836c124a97455e373469ae1a6e9be7c13e5f895dfba0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5e346146a229401e10471e4cbbe84a57931d3139ea0434147f07c663d432b`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 11.7 MB (11688893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1255468b95293fb1e60abbe6d77208b9625ac10eca1c246235c3ac7ddfb801f1`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cd2e2bf1a80e558d1befccd7dc91728b49d1c244d7da9339a06a4d7ac3af14`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb862dadada5fb7f5ae18bd37f410686a49ba21bf2d7c577bae16a2ef16ed6`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 93.2 KB (93203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848686458fe8f432331e61cc40d34b67889f849657c2f6783f2a53c3a98753eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c148c8e5d098f166d5f6a24c1c83ec09679603cbbc8c6fd8c3efd9377a3b8bb`

```dockerfile
```

-	Layers:
	-	`sha256:5c09dd3adb1cb49760d6fb3a008b82184b82580e7331d7f6df9827955bfbfbe0`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 4.0 MB (3952790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915e7352977df39d05b78465ba9906fc5569734a50655cd7c22622a7105e20ae`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:b0fd02fb64867772094c3388f3fa12061f0b1641292c3eb9d4514f5c667eac4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:851e63864831469546085f6a457288bab67ac55db23fe8184195c000da461f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1140577c4fa48a7d165ccc461ad7e892f8c319ffc1838973c42f4cd47fbe908a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682aa3f8a7a0c6b2c3f7e69082a7641b2f8a398db39cea59e30577ab2cd9545c`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 11.3 MB (11266852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74fe3db0b2d5102c748c1dced6a2d654dcfe6325440f5ad12c7d15b9e2a4ca`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b621e6e6f14028ed190e855d6f2b7332388d7d99f86177c0839d80572400cfb2`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686d88df96b49bdf2c13c3a23f6cb8d645961840a556883c3cc5b79b9185eb01`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 93.2 KB (93186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6586d320bf1e1e1821085a599b7260b177db8d637dffbc69299cb7848af335c`  
		Last Modified: Wed, 21 May 2025 23:33:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa004cfcf0e1cb0d21a28babe2049d496a76da2dc5adddfdf974e2f8efad05d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061fdf2951dbc561a9c508a39236c8c3dd4a204b208530753faaa768e80ac32a`

```dockerfile
```

-	Layers:
	-	`sha256:305ee82f38619bafff21cca2294c2411ee720c40e0020e78825eeb6c523714a2`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 4.0 MB (3954862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b44bd6c10531f89f0b05cc959d4ead7f25c043efd5e5810173fa6bf75fb2de70`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f0b21e9a2b1d87e8e9d1cf617208198e10c617d9f80b1339ff54ce27ee66c91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36204bccfc429d1ecc0ab3e4cb4d125b9a3f7594aa42d97f2f51c173dce13323`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 93.4 KB (93443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89280029104abf21945b59b054a3eedf9f7b23e94999b1aca58011419c300a`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7e6da63402e4b1eef862b0d8a3f101017276aecf02c60186b794120fd687915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107dbd281f4baae96d89cf725ff834951638204a9503b9812136446b2ad9caf4`

```dockerfile
```

-	Layers:
	-	`sha256:b4f000b0ebc61fecbc86e06e322d07a3aca6d8fa3ed3c9d7d781d5c75cbcf560`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 4.0 MB (3955116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73550faaa5db727c23fdf4536980baf5f17f7a89739abf435a3879571e512a4`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bfa199662e75b2c37492367434358c210d8a355f2bb15868b5b769db9193be49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61256320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b532a8a00c0c0d7b9dd3f7f594b120af5664d70270ca19502f4e7bc233aace4c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2befdc47cd4cc9a43be4226914197171d517dbe40274f5b26c8088cdbcaa2b9c`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 11.7 MB (11688920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1bfa09a90b3a837330dd2a72b46dca98d510d8427fb5b9162ae3be7a83bba9`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18aa48402f14aa565c4a322fecbcc79be120249f1f6245662825df0b4a4d37a`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c2353a2d9dd0fffbf5018f9fc815a0ccef03054aee9386f0bfbb9f4d63b6d4`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 93.2 KB (93217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db8ce6f79b3373f6fdcacdddb049c597fb580b389a159ada0336d9dc29e05c`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc54ac074ea1a6afab79cac6dfcfab8d9003737aa056274f441cdf463fd1528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3920c7ac1fba6d508e7195907458fc78fa48d79d67c362e3e13a116d968ef667`

```dockerfile
```

-	Layers:
	-	`sha256:afa6979159e91d00fa568b799a399cc939346264429fe4419c17550b77367215`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 4.0 MB (3952830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b28f32383b18cc13b5a4e44e0a3ca98b957af3a8d6c2667e4b7ab8c4a5dd80`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:e68b01fb0dea971fa4cfd39d8feb687c3fe2aa4bd228ca5e72189d11d8c78908
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:ec026f26f90a1da8ffc3ba59281854c0bb1a0b5f166e58e75d57f34e8424bd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa3d04109e9bf85dbba55e27e2b0055d3c73ba8b1f21907acb2c7bdb223320`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabac9a159eac99d387c3b1a92d15536e78c12f6596c2dbd37f29d0b63d5dffe`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 5.4 MB (5362390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e9f035d7685c2fdb1e905a640424e5ad669ee2970a32cbec7f8d889e3625f1`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb125018a09465c3a7d0200be55fc6435a06fe742fd5a7a7ef39a0fb83cfbf6`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46b9b7320bd76241047fcf77910ba82992b5e91e204eefe5390b265739db65`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 105.4 KB (105439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed731be31bff11d448e1a27d734e900b2e674625af668b3f9b87ba45b1a8f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fb983f465508bd38f2970b20fcfd3052779b73f8d3b436c6ab4ff79915307d`

```dockerfile
```

-	Layers:
	-	`sha256:079d7ce90a22f0bd844b80ccfaee90ce51150b4f1244f3519448f12bf6c83630`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 2.0 MB (2017825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d275b201a8175e6493a6207f8e73ff2b18780007de8ef8e54adc086578431b8d`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:39c9bfd66371de386419abe34cd806357a534145fbce48504409d1f8f396a4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45aed6d0d9e4f56fcf7aaaad06b6a747462168128f4a0d1f3e2084772af72fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2952dad8358145d90322cccd4047ea733f93fc11fed56791f2817ddc6d99d545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0237cdae437eaedee949f6af64e985420e981a9dfa9474fce1bb2e9aa7fbb8fd`

```dockerfile
```

-	Layers:
	-	`sha256:f307ef0a8e38175dd6e3ceb807d756938a14b991426d356ef4e8432d33ab7e37`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 2.0 MB (2018054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8946cab190197295b0fd0de39d4d1f5d0e06793a5eb36d0073e79597d9fd10d1`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:4c1ed82e5488cc7a87a4035c84b91368bf439418f76c388be8923760e27cc034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5b5f12c95fa70eba84ed0d9a8cfd320ff1f928e0f4ecc665553188865bc1fdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77302996458a5ea42a30e362fe60a32b80399042312ed4461165057feaadc3a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09894bd673fc3443fa4aac9c04f3790e80821023e1b647cb36b0dbb3295685a1`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 5.4 MB (5362436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b567f68d429f42a824fdac7d380831ff3ee4e919d2c1f56ac4ba2d5c728dab9`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe211eff3c4623dbc046e34c08495b6c3665295d30178fc8053cd5baff9b469`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93ed51b316d633e53abd6403ccacb66bf2b80b807810d40df2342572077415`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 105.4 KB (105442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca65e65a74419b6f595b799268195de974952d7e1558d9a39092265337398f`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:451612c81608c2bebc8d3e36a6a521b28025afe8d027348134cdac02a7ec34d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e43683e94761e4cae4d1f50b39b3b1ced64f4fb773232eb29f20df0b386bb`

```dockerfile
```

-	Layers:
	-	`sha256:79b4a3ef3b60d9c20c2340237fe4236376a35581ce8f29f76d044ea8920b97d3`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 2.0 MB (2017861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd949e8f808ff83620701f51061d8dc60e04b6e7afc9a968a71e3ed0ef991e1`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b31849bda994a89ea1e43d1ee83490728e5c84d98e21bb02362919c0ee14a139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9884153e1d1e0355067632367672016383e04b73464a2d8661e4d01f7cf3d14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8215c91245c0463263d03909dc6267e663f8bc6ca035c5fa1478e3632affb97f`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e0dd953f78b0d8045d26f7afb42c726a2cc4e07a96a2b3b741316ca99534d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea7d3f1b864509ea868bded897bb9ca30f452582999b77e73c6bfc798dd9443`

```dockerfile
```

-	Layers:
	-	`sha256:1fcbe13a76f25efb5f459970d227c4628a1a8f71064188a5cd94ffb6874dd526`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 2.0 MB (2018090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dac00fd22e65ab791eda65319d76e0834a665f17c3cf1d1784f781fa3bcd68`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:a62ad433a27fe25a8de7f951e4212508ae8d406477c0b32dc47385b9799a5f1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:5c6093825b977242a0c5ce777463f22291467f3213ee9967d63ad853cad62b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0159f21b56dd611102fd38c93c9b9db6747ecff96ad393e3a308e6b9a27338be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaae9adeb5784f217b1fccbfde587bde5f5a4eef001092646b8beb2b6083091`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 3.6 MB (3624137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13bc798486b3ed6c830d97b2bbead94f4fba215db043fa3784384ab67490f7b`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5403824352add24fb2c4ff3c15449271afc3ecff86b4c3ceaee1884051b6b38b`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8cf2c0a6fd0753dac46ff04bd86d6df6b583a2e5e3255cf4a0a914a7af892`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 110.6 KB (110554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cc4e8e5db5c9f889fe8af12a7c454a321cafb97ce2f6eb5726d0cf2334a61d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2094402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa173a2f1b0551b0755668bd7412967e18454e29d78df0e7fdc4eb9697d84f3`

```dockerfile
```

-	Layers:
	-	`sha256:d5df8adfd2250d8e942803d58a02b3042f130a0b08a3032e2f92fe6ebc663de0`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 2.1 MB (2080426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8db84911c2b9570d62209aca26a6603452311f1d2675ca00a4d45b6e0e0e45`  
		Last Modified: Tue, 03 Jun 2025 04:17:15 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9d73162a14eddeaa42de80b66ebb46ce4058a34b7e8f278ebe76b01bdfe8218c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31063851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6641bfdb2031f8162a237d8747ec26d21147022b969270ac106464d19f1c9cd1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Fri, 30 May 2025 23:34:51 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e930d912712ee307694bc8edc2665e13ab5ffabd52de3c434ea3e9debd56da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2094787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da916fbb9e734f060ad2c0386b3dde6822474e043cccbcb4c4b5700a6eeeeb05`

```dockerfile
```

-	Layers:
	-	`sha256:55487635e34c1575a1c86ad1538db4eae8185f9b358bc3b2647c7b10c50a9639`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 2.1 MB (2080686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6afd8ad60b0744690a9d8df1fdde507192154666dd867a3ca02ad6d8a4e9430`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:7481cf83e704b3af7a5b48b3edcdaa6c8359604a90aee37431c2027bc8d9f36a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:106a157335593089bd9167471a43ac4e4a300c21bca0dfac7ab5e8ca330e11b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c425b94e9e05e94a3588a5ed5fa50798b770c5964ee80eb3108e2c2b854734`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833f05bf4a56287336922533369cb272b043579abea2c4588fb7a28586dccbb7`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 3.6 MB (3624096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5f30655f789d9aaabd83e43e19fd42000e70a6d62d06ddf046576bfb3eb56`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b76c5daef076a6ef3131ece85a9ede4b5366f8b35563943c61f3ca36393de48`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b346a922dadb495203fa86390fce5ab7f4746b373ff8ee37ae89b1570fab89`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 110.6 KB (110563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96bb241c37c54f5099c6ee4be792e3df22a12f314a81846062a58b160223e7a`  
		Last Modified: Tue, 03 Jun 2025 04:16:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8aae46358cf11c3d67fb2b0bf9adbc7de24122f7bcae1bfe2c595b1a62233e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2096668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14479c1656b173c0100892f3c715ee08d6396fbbddd70f0eb6c7d400c28dc177`

```dockerfile
```

-	Layers:
	-	`sha256:1e817e7f07a5533079454f7b46be380fb1a89f65ee260bfd9d08395ebf6e86fa`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 2.1 MB (2080462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb30aac33316b47ec98bca470a0a0a66269cdd7aa22f62d98e749d5c5e1c494`  
		Last Modified: Tue, 03 Jun 2025 04:16:58 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f069651f05d3e6c7a096a41a3242a53b7f5067e15c35b139bc0844d2c622254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b33835d3e532c457a861b46b17a2ecc210b0019baeec6bf4b85319109ae9d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Fri, 30 May 2025 23:34:51 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Tue, 03 Jun 2025 05:18:54 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc12a5156209348208485de93d3b89460edf23f23fdded16678f39a46448c25`  
		Last Modified: Tue, 03 Jun 2025 05:19:07 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2fb96a9daec1ce2a7e9ea4dd1144aa633c2bc1d97d73ba0bece51586ec46fc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2097068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25ae2c3ba2f40b6fa187203997315827f50c3c023a8f4ce4137f6b8994a5c1`

```dockerfile
```

-	Layers:
	-	`sha256:f8f474f858ffefa2d71ad93a00640e481fbbfd9d23b677cb8ee70750c1123694`  
		Last Modified: Tue, 03 Jun 2025 05:19:07 GMT  
		Size: 2.1 MB (2080722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09220ec00b43fe2a6638b49308e372f11987cceec9eefdf11f6781cec1b7a417`  
		Last Modified: Tue, 03 Jun 2025 05:19:06 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:f95676da88045789e619860caeb6a3ecad7e5735e7fe3cba9bc0245f6499fa2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:d38770387a1f54d95d0d558099909093e51c2a541d725a169a3ab440228ce641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e059b96cc5ab2387c1bb2485d9de3fe3aa2dab08159f4e56de08657ed279f9`
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
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aae2be978b6887ba33cc355eb60849e9a4b6494da48dbc2025ec215fc048bbd`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 3.6 MB (3561550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214a87e3f5642da384965dace0ef6f6fe356aeebd976cea08d1deb25cc5b17cc`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 1.9 KB (1907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c2ffabb65505adc1a9bd197602a784b5362d2bf73c24ab87ff05d5de31986b`  
		Last Modified: Mon, 05 May 2025 16:36:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418af0f32ee06323cc96c6ebd9014c231ad3deaa60e018b922a41d15df29cd9e`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 102.8 KB (102849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d05f6938da9aeb0879b1fe995f7e53f824b9806df54a2cf758869d5a75b9fd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3bb6b2ab29942ba9926b585f6a9f2762e3332b5b0917f6c506a00cb07af85`

```dockerfile
```

-	Layers:
	-	`sha256:db5db1fcebc99c5ee245340feaabb7749eaa8dd62337d6b75728edd76c2e33a1`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 2.0 MB (1988007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae603c4f8c4fdbb75e2ff13d822ac64719e2cc5269f96c64fbd4e9433d674d53`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ff983cae8fa779ca9d445f0e2e30c9c0c03e867cff63e93ec397123b526af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9506d7bae42cf7450aa75eaeb8571087a3a9d4066fc59a980c2149e19578d`
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
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
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

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:222ce1225e4552dab3c723682de0a2272dd746e75ef288a430f54e46046c4985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de3d7a56bd63248962b3eb96296da8be24233a5f3739114ca94981c5ccecf8a`

```dockerfile
```

-	Layers:
	-	`sha256:691e9a8ce459d8732c2d0bfe0a5462ebd479d481a963330437c6d61ca42d888c`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 2.0 MB (1989052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c66f9e1f8f25f8e1de91b113698830913584ff5a51823d5484ec6d26a10084`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:69ce90ed413297d173afe360aad6f52bb5176e84eca7931478cd30ca79a58961
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

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
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5d60262949712c1e9b418187e3cc8bd5f8d0cd29eb97c9e363914cedaa63b`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 3.6 MB (3561531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4ccf25a7e89dd343d5f776bf03085f2ba18bbad5a4100ece345624e0a595c`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53011f9a2cfb2befb053a53ab616fbc8cdc2c34c7c16c3d64268caf75936a28d`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d8f4ff9e91fa0098e89a942d5178c56e58307eeddb25322eb98cb14237292c`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 102.8 KB (102845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f18bdc3a399429a3003a5facfc548c193056b9f8a3c92159a30cdc1478fdfc`  
		Last Modified: Mon, 05 May 2025 16:35:50 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

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

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

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
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
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

### `neurodebian:nd24.04-non-free` - unknown; unknown

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

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:f95676da88045789e619860caeb6a3ecad7e5735e7fe3cba9bc0245f6499fa2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:d38770387a1f54d95d0d558099909093e51c2a541d725a169a3ab440228ce641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e059b96cc5ab2387c1bb2485d9de3fe3aa2dab08159f4e56de08657ed279f9`
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
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aae2be978b6887ba33cc355eb60849e9a4b6494da48dbc2025ec215fc048bbd`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 3.6 MB (3561550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214a87e3f5642da384965dace0ef6f6fe356aeebd976cea08d1deb25cc5b17cc`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 1.9 KB (1907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c2ffabb65505adc1a9bd197602a784b5362d2bf73c24ab87ff05d5de31986b`  
		Last Modified: Mon, 05 May 2025 16:36:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418af0f32ee06323cc96c6ebd9014c231ad3deaa60e018b922a41d15df29cd9e`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 102.8 KB (102849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d05f6938da9aeb0879b1fe995f7e53f824b9806df54a2cf758869d5a75b9fd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3bb6b2ab29942ba9926b585f6a9f2762e3332b5b0917f6c506a00cb07af85`

```dockerfile
```

-	Layers:
	-	`sha256:db5db1fcebc99c5ee245340feaabb7749eaa8dd62337d6b75728edd76c2e33a1`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 2.0 MB (1988007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae603c4f8c4fdbb75e2ff13d822ac64719e2cc5269f96c64fbd4e9433d674d53`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ff983cae8fa779ca9d445f0e2e30c9c0c03e867cff63e93ec397123b526af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9506d7bae42cf7450aa75eaeb8571087a3a9d4066fc59a980c2149e19578d`
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
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
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

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:222ce1225e4552dab3c723682de0a2272dd746e75ef288a430f54e46046c4985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de3d7a56bd63248962b3eb96296da8be24233a5f3739114ca94981c5ccecf8a`

```dockerfile
```

-	Layers:
	-	`sha256:691e9a8ce459d8732c2d0bfe0a5462ebd479d481a963330437c6d61ca42d888c`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 2.0 MB (1989052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c66f9e1f8f25f8e1de91b113698830913584ff5a51823d5484ec6d26a10084`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

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
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5d60262949712c1e9b418187e3cc8bd5f8d0cd29eb97c9e363914cedaa63b`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 3.6 MB (3561531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4ccf25a7e89dd343d5f776bf03085f2ba18bbad5a4100ece345624e0a595c`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53011f9a2cfb2befb053a53ab616fbc8cdc2c34c7c16c3d64268caf75936a28d`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d8f4ff9e91fa0098e89a942d5178c56e58307eeddb25322eb98cb14237292c`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 102.8 KB (102845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f18bdc3a399429a3003a5facfc548c193056b9f8a3c92159a30cdc1478fdfc`  
		Last Modified: Mon, 05 May 2025 16:35:50 GMT  
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
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
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

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:b0fd02fb64867772094c3388f3fa12061f0b1641292c3eb9d4514f5c667eac4a
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
$ docker pull neurodebian@sha256:851e63864831469546085f6a457288bab67ac55db23fe8184195c000da461f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1140577c4fa48a7d165ccc461ad7e892f8c319ffc1838973c42f4cd47fbe908a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682aa3f8a7a0c6b2c3f7e69082a7641b2f8a398db39cea59e30577ab2cd9545c`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 11.3 MB (11266852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74fe3db0b2d5102c748c1dced6a2d654dcfe6325440f5ad12c7d15b9e2a4ca`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b621e6e6f14028ed190e855d6f2b7332388d7d99f86177c0839d80572400cfb2`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686d88df96b49bdf2c13c3a23f6cb8d645961840a556883c3cc5b79b9185eb01`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 93.2 KB (93186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6586d320bf1e1e1821085a599b7260b177db8d637dffbc69299cb7848af335c`  
		Last Modified: Wed, 21 May 2025 23:33:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa004cfcf0e1cb0d21a28babe2049d496a76da2dc5adddfdf974e2f8efad05d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061fdf2951dbc561a9c508a39236c8c3dd4a204b208530753faaa768e80ac32a`

```dockerfile
```

-	Layers:
	-	`sha256:305ee82f38619bafff21cca2294c2411ee720c40e0020e78825eeb6c523714a2`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 4.0 MB (3954862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b44bd6c10531f89f0b05cc959d4ead7f25c043efd5e5810173fa6bf75fb2de70`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f0b21e9a2b1d87e8e9d1cf617208198e10c617d9f80b1339ff54ce27ee66c91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36204bccfc429d1ecc0ab3e4cb4d125b9a3f7594aa42d97f2f51c173dce13323`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 93.4 KB (93443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89280029104abf21945b59b054a3eedf9f7b23e94999b1aca58011419c300a`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7e6da63402e4b1eef862b0d8a3f101017276aecf02c60186b794120fd687915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107dbd281f4baae96d89cf725ff834951638204a9503b9812136446b2ad9caf4`

```dockerfile
```

-	Layers:
	-	`sha256:b4f000b0ebc61fecbc86e06e322d07a3aca6d8fa3ed3c9d7d781d5c75cbcf560`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 4.0 MB (3955116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73550faaa5db727c23fdf4536980baf5f17f7a89739abf435a3879571e512a4`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bfa199662e75b2c37492367434358c210d8a355f2bb15868b5b769db9193be49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61256320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b532a8a00c0c0d7b9dd3f7f594b120af5664d70270ca19502f4e7bc233aace4c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2befdc47cd4cc9a43be4226914197171d517dbe40274f5b26c8088cdbcaa2b9c`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 11.7 MB (11688920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1bfa09a90b3a837330dd2a72b46dca98d510d8427fb5b9162ae3be7a83bba9`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18aa48402f14aa565c4a322fecbcc79be120249f1f6245662825df0b4a4d37a`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c2353a2d9dd0fffbf5018f9fc815a0ccef03054aee9386f0bfbb9f4d63b6d4`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 93.2 KB (93217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db8ce6f79b3373f6fdcacdddb049c597fb580b389a159ada0336d9dc29e05c`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc54ac074ea1a6afab79cac6dfcfab8d9003737aa056274f441cdf463fd1528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3920c7ac1fba6d508e7195907458fc78fa48d79d67c362e3e13a116d968ef667`

```dockerfile
```

-	Layers:
	-	`sha256:afa6979159e91d00fa568b799a399cc939346264429fe4419c17550b77367215`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 4.0 MB (3952830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b28f32383b18cc13b5a4e44e0a3ca98b957af3a8d6c2667e4b7ab8c4a5dd80`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
