<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
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
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1479a7dfdd7bd71a331fb57263d63a48b18f362276a8d3507efc1dba468dc`  
		Last Modified: Tue, 03 Jun 2025 13:54:36 GMT  
		Size: 11.3 MB (11266844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3811163e1e52f20133f4a2f726f2743ad294c104a345c4ef4f4da69b9d078fd`  
		Last Modified: Tue, 03 Jun 2025 13:54:33 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df351ef0700f87809686368ec3b0cfb7da8af39ae9d31bc006aa2bd60ac1ed9f`  
		Last Modified: Tue, 03 Jun 2025 13:54:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1793f6f7307e57ec6794a674c75ce0ce2fd92331fdb2bc2df11fa0a20c8b713`  
		Last Modified: Tue, 03 Jun 2025 13:54:36 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Wed, 04 Jun 2025 16:16:03 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5e346146a229401e10471e4cbbe84a57931d3139ea0434147f07c663d432b`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 11.7 MB (11688893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1255468b95293fb1e60abbe6d77208b9625ac10eca1c246235c3ac7ddfb801f1`  
		Last Modified: Sat, 07 Jun 2025 07:18:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cd2e2bf1a80e558d1befccd7dc91728b49d1c244d7da9339a06a4d7ac3af14`  
		Last Modified: Sat, 07 Jun 2025 07:18:58 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb862dadada5fb7f5ae18bd37f410686a49ba21bf2d7c577bae16a2ef16ed6`  
		Last Modified: Sat, 07 Jun 2025 07:18:58 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682aa3f8a7a0c6b2c3f7e69082a7641b2f8a398db39cea59e30577ab2cd9545c`  
		Last Modified: Tue, 03 Jun 2025 17:44:19 GMT  
		Size: 11.3 MB (11266852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74fe3db0b2d5102c748c1dced6a2d654dcfe6325440f5ad12c7d15b9e2a4ca`  
		Last Modified: Tue, 03 Jun 2025 17:44:17 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b621e6e6f14028ed190e855d6f2b7332388d7d99f86177c0839d80572400cfb2`  
		Last Modified: Tue, 03 Jun 2025 17:44:17 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686d88df96b49bdf2c13c3a23f6cb8d645961840a556883c3cc5b79b9185eb01`  
		Last Modified: Tue, 03 Jun 2025 17:44:18 GMT  
		Size: 93.2 KB (93186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6586d320bf1e1e1821085a599b7260b177db8d637dffbc69299cb7848af335c`  
		Last Modified: Tue, 03 Jun 2025 17:44:19 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Wed, 04 Jun 2025 16:16:03 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470a16785ed0074295002c533632f65140ee1e5655c3e51026466bf8eb57fd4c`  
		Last Modified: Tue, 03 Jun 2025 17:39:15 GMT  
		Size: 11.1 MB (11105018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875f413f88db273081bdf04d81e663ec5201e9b626f42ec01033462ebe247351`  
		Last Modified: Tue, 03 Jun 2025 17:39:10 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc1e8d628fd6131dc4a548803f430ff460f19615a548d9abcf80c734137bb6`  
		Last Modified: Tue, 03 Jun 2025 17:39:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3239c21ef74426bcd266e0b79c4f3f8f0fee1a5b14829a0cb42ebf63bdf5e2`  
		Last Modified: Tue, 03 Jun 2025 17:39:12 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Tue, 03 Jun 2025 19:33:33 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Tue, 03 Jun 2025 19:33:36 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca25855464c362ff5b431ed1c58bcac1d3074d341dfbe0b69db0c4b7b06ddfb`  
		Last Modified: Tue, 03 Jun 2025 17:40:41 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bd852d80e3b0c678ae63bfb3948aaedb9a85ffee30335e3517dfdb5079959d`  
		Last Modified: Tue, 03 Jun 2025 17:40:40 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755cd40c0c29cc545f889321eb72bcbd161b6e91d0f0b1b7e45ff98558c28ca2`  
		Last Modified: Tue, 03 Jun 2025 17:40:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4067042efe9918fc632e3430f0139557b52b74d633b305ae3271d19e6436a4a6`  
		Last Modified: Tue, 03 Jun 2025 17:40:41 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762595f10379f52572d8fd283315b81ce1b9219d0093d67e34f012a23d953ce0`  
		Last Modified: Tue, 03 Jun 2025 17:40:41 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Tue, 03 Jun 2025 19:33:33 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Tue, 03 Jun 2025 19:33:36 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd4d56a7262cf9c7a1b114c72ceb3299228df837a1640a8ce90628bd5c963b1`  
		Last Modified: Wed, 04 Jun 2025 16:14:14 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaae9adeb5784f217b1fccbfde587bde5f5a4eef001092646b8beb2b6083091`  
		Last Modified: Tue, 03 Jun 2025 15:33:13 GMT  
		Size: 3.6 MB (3624137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13bc798486b3ed6c830d97b2bbead94f4fba215db043fa3784384ab67490f7b`  
		Last Modified: Tue, 03 Jun 2025 15:33:12 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5403824352add24fb2c4ff3c15449271afc3ecff86b4c3ceaee1884051b6b38b`  
		Last Modified: Tue, 03 Jun 2025 15:33:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8cf2c0a6fd0753dac46ff04bd86d6df6b583a2e5e3255cf4a0a914a7af892`  
		Last Modified: Tue, 03 Jun 2025 15:33:14 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Wed, 04 Jun 2025 23:53:21 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Wed, 04 Jun 2025 23:46:33 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Wed, 04 Jun 2025 23:58:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Wed, 04 Jun 2025 23:45:32 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833f05bf4a56287336922533369cb272b043579abea2c4588fb7a28586dccbb7`  
		Last Modified: Tue, 03 Jun 2025 17:31:23 GMT  
		Size: 3.6 MB (3624096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5f30655f789d9aaabd83e43e19fd42000e70a6d62d06ddf046576bfb3eb56`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b76c5daef076a6ef3131ece85a9ede4b5366f8b35563943c61f3ca36393de48`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b346a922dadb495203fa86390fce5ab7f4746b373ff8ee37ae89b1570fab89`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
		Size: 110.6 KB (110563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96bb241c37c54f5099c6ee4be792e3df22a12f314a81846062a58b160223e7a`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Wed, 04 Jun 2025 23:53:21 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Wed, 04 Jun 2025 23:46:33 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Wed, 04 Jun 2025 23:58:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Wed, 04 Jun 2025 23:45:32 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc12a5156209348208485de93d3b89460edf23f23fdded16678f39a46448c25`  
		Last Modified: Wed, 04 Jun 2025 23:46:15 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1479a7dfdd7bd71a331fb57263d63a48b18f362276a8d3507efc1dba468dc`  
		Last Modified: Tue, 03 Jun 2025 13:54:36 GMT  
		Size: 11.3 MB (11266844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3811163e1e52f20133f4a2f726f2743ad294c104a345c4ef4f4da69b9d078fd`  
		Last Modified: Tue, 03 Jun 2025 13:54:33 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df351ef0700f87809686368ec3b0cfb7da8af39ae9d31bc006aa2bd60ac1ed9f`  
		Last Modified: Tue, 03 Jun 2025 13:54:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1793f6f7307e57ec6794a674c75ce0ce2fd92331fdb2bc2df11fa0a20c8b713`  
		Last Modified: Tue, 03 Jun 2025 13:54:36 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Wed, 04 Jun 2025 16:16:03 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5e346146a229401e10471e4cbbe84a57931d3139ea0434147f07c663d432b`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 11.7 MB (11688893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1255468b95293fb1e60abbe6d77208b9625ac10eca1c246235c3ac7ddfb801f1`  
		Last Modified: Sat, 07 Jun 2025 07:18:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cd2e2bf1a80e558d1befccd7dc91728b49d1c244d7da9339a06a4d7ac3af14`  
		Last Modified: Sat, 07 Jun 2025 07:18:58 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb862dadada5fb7f5ae18bd37f410686a49ba21bf2d7c577bae16a2ef16ed6`  
		Last Modified: Sat, 07 Jun 2025 07:18:58 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470a16785ed0074295002c533632f65140ee1e5655c3e51026466bf8eb57fd4c`  
		Last Modified: Tue, 03 Jun 2025 17:39:15 GMT  
		Size: 11.1 MB (11105018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875f413f88db273081bdf04d81e663ec5201e9b626f42ec01033462ebe247351`  
		Last Modified: Tue, 03 Jun 2025 17:39:10 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc1e8d628fd6131dc4a548803f430ff460f19615a548d9abcf80c734137bb6`  
		Last Modified: Tue, 03 Jun 2025 17:39:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3239c21ef74426bcd266e0b79c4f3f8f0fee1a5b14829a0cb42ebf63bdf5e2`  
		Last Modified: Tue, 03 Jun 2025 17:39:12 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Tue, 03 Jun 2025 19:33:33 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Tue, 03 Jun 2025 19:33:36 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca25855464c362ff5b431ed1c58bcac1d3074d341dfbe0b69db0c4b7b06ddfb`  
		Last Modified: Tue, 03 Jun 2025 17:40:41 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bd852d80e3b0c678ae63bfb3948aaedb9a85ffee30335e3517dfdb5079959d`  
		Last Modified: Tue, 03 Jun 2025 17:40:40 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755cd40c0c29cc545f889321eb72bcbd161b6e91d0f0b1b7e45ff98558c28ca2`  
		Last Modified: Tue, 03 Jun 2025 17:40:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4067042efe9918fc632e3430f0139557b52b74d633b305ae3271d19e6436a4a6`  
		Last Modified: Tue, 03 Jun 2025 17:40:41 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762595f10379f52572d8fd283315b81ce1b9219d0093d67e34f012a23d953ce0`  
		Last Modified: Tue, 03 Jun 2025 17:40:41 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Tue, 03 Jun 2025 19:33:33 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Tue, 03 Jun 2025 19:33:36 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd4d56a7262cf9c7a1b114c72ceb3299228df837a1640a8ce90628bd5c963b1`  
		Last Modified: Wed, 04 Jun 2025 16:14:14 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d1479a7dfdd7bd71a331fb57263d63a48b18f362276a8d3507efc1dba468dc`  
		Last Modified: Tue, 03 Jun 2025 13:54:36 GMT  
		Size: 11.3 MB (11266844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3811163e1e52f20133f4a2f726f2743ad294c104a345c4ef4f4da69b9d078fd`  
		Last Modified: Tue, 03 Jun 2025 13:54:33 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df351ef0700f87809686368ec3b0cfb7da8af39ae9d31bc006aa2bd60ac1ed9f`  
		Last Modified: Tue, 03 Jun 2025 13:54:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1793f6f7307e57ec6794a674c75ce0ce2fd92331fdb2bc2df11fa0a20c8b713`  
		Last Modified: Tue, 03 Jun 2025 13:54:36 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Wed, 04 Jun 2025 16:16:03 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5e346146a229401e10471e4cbbe84a57931d3139ea0434147f07c663d432b`  
		Last Modified: Wed, 21 May 2025 23:20:18 GMT  
		Size: 11.7 MB (11688893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1255468b95293fb1e60abbe6d77208b9625ac10eca1c246235c3ac7ddfb801f1`  
		Last Modified: Sat, 07 Jun 2025 07:18:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cd2e2bf1a80e558d1befccd7dc91728b49d1c244d7da9339a06a4d7ac3af14`  
		Last Modified: Sat, 07 Jun 2025 07:18:58 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb862dadada5fb7f5ae18bd37f410686a49ba21bf2d7c577bae16a2ef16ed6`  
		Last Modified: Sat, 07 Jun 2025 07:18:58 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682aa3f8a7a0c6b2c3f7e69082a7641b2f8a398db39cea59e30577ab2cd9545c`  
		Last Modified: Tue, 03 Jun 2025 17:44:19 GMT  
		Size: 11.3 MB (11266852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74fe3db0b2d5102c748c1dced6a2d654dcfe6325440f5ad12c7d15b9e2a4ca`  
		Last Modified: Tue, 03 Jun 2025 17:44:17 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b621e6e6f14028ed190e855d6f2b7332388d7d99f86177c0839d80572400cfb2`  
		Last Modified: Tue, 03 Jun 2025 17:44:17 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686d88df96b49bdf2c13c3a23f6cb8d645961840a556883c3cc5b79b9185eb01`  
		Last Modified: Tue, 03 Jun 2025 17:44:18 GMT  
		Size: 93.2 KB (93186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6586d320bf1e1e1821085a599b7260b177db8d637dffbc69299cb7848af335c`  
		Last Modified: Tue, 03 Jun 2025 17:44:19 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Wed, 04 Jun 2025 16:16:03 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaae9adeb5784f217b1fccbfde587bde5f5a4eef001092646b8beb2b6083091`  
		Last Modified: Tue, 03 Jun 2025 15:33:13 GMT  
		Size: 3.6 MB (3624137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13bc798486b3ed6c830d97b2bbead94f4fba215db043fa3784384ab67490f7b`  
		Last Modified: Tue, 03 Jun 2025 15:33:12 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5403824352add24fb2c4ff3c15449271afc3ecff86b4c3ceaee1884051b6b38b`  
		Last Modified: Tue, 03 Jun 2025 15:33:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8cf2c0a6fd0753dac46ff04bd86d6df6b583a2e5e3255cf4a0a914a7af892`  
		Last Modified: Tue, 03 Jun 2025 15:33:14 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Wed, 04 Jun 2025 23:53:21 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Wed, 04 Jun 2025 23:46:33 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Wed, 04 Jun 2025 23:58:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Wed, 04 Jun 2025 23:45:32 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833f05bf4a56287336922533369cb272b043579abea2c4588fb7a28586dccbb7`  
		Last Modified: Tue, 03 Jun 2025 17:31:23 GMT  
		Size: 3.6 MB (3624096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd5f30655f789d9aaabd83e43e19fd42000e70a6d62d06ddf046576bfb3eb56`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b76c5daef076a6ef3131ece85a9ede4b5366f8b35563943c61f3ca36393de48`  
		Last Modified: Tue, 03 Jun 2025 17:31:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b346a922dadb495203fa86390fce5ab7f4746b373ff8ee37ae89b1570fab89`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
		Size: 110.6 KB (110563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96bb241c37c54f5099c6ee4be792e3df22a12f314a81846062a58b160223e7a`  
		Last Modified: Tue, 03 Jun 2025 17:31:24 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb392c94ac75bcd9a3d1c9227d1748af1accbe8187fbfc8c5d1775fec406ddf7`  
		Last Modified: Wed, 04 Jun 2025 23:53:21 GMT  
		Size: 3.6 MB (3595613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f75ee17aabcbf6b4cb401f1209ba36e9b65a6e79abf95f372b0962049a2f26`  
		Last Modified: Wed, 04 Jun 2025 23:46:33 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98432ecc9d6cca1469e31ff7f3a6d9ea401d199b788649c06c39bfc96c390eb5`  
		Last Modified: Wed, 04 Jun 2025 23:58:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff97a05d308956eaaf43302acc738b08bbc3ab11833a62a219be760d787277`  
		Last Modified: Wed, 04 Jun 2025 23:45:32 GMT  
		Size: 110.5 KB (110480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc12a5156209348208485de93d3b89460edf23f23fdded16678f39a46448c25`  
		Last Modified: Wed, 04 Jun 2025 23:46:15 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682aa3f8a7a0c6b2c3f7e69082a7641b2f8a398db39cea59e30577ab2cd9545c`  
		Last Modified: Tue, 03 Jun 2025 17:44:19 GMT  
		Size: 11.3 MB (11266852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74fe3db0b2d5102c748c1dced6a2d654dcfe6325440f5ad12c7d15b9e2a4ca`  
		Last Modified: Tue, 03 Jun 2025 17:44:17 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b621e6e6f14028ed190e855d6f2b7332388d7d99f86177c0839d80572400cfb2`  
		Last Modified: Tue, 03 Jun 2025 17:44:17 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686d88df96b49bdf2c13c3a23f6cb8d645961840a556883c3cc5b79b9185eb01`  
		Last Modified: Tue, 03 Jun 2025 17:44:18 GMT  
		Size: 93.2 KB (93186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6586d320bf1e1e1821085a599b7260b177db8d637dffbc69299cb7848af335c`  
		Last Modified: Tue, 03 Jun 2025 17:44:19 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Wed, 04 Jun 2025 16:16:03 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
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
