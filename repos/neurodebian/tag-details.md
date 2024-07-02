<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:buster`](#neurodebianbuster)
-	[`neurodebian:buster-non-free`](#neurodebianbuster-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd100`](#neurodebiannd100)
-	[`neurodebian:nd100-non-free`](#neurodebiannd100-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd130`](#neurodebiannd130)
-	[`neurodebian:nd130-non-free`](#neurodebiannd130-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:5670bf67b386a7e47e9d98f3d7af5f8b0cc4f72a01053db1b62189698b37c065
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
$ docker pull neurodebian@sha256:bb45cc1847f9b911b39cc468b26256bd9ba3859cf8e3320692224fde2e0bc6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6e2c1137a6862e8b108290cdb4757d6147174a18a6501f3f1754cb39e5e710`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cfb6f5dfec97711feafb9c33a2590015ca328f9807711d4d3e62d326aba87c`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 11.3 MB (11266509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46570b27600cb554709fe9a2632cb10f3eebec4088ce4dce4ef9c423ba9f724`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c46ea3d00c2fc1da85fe97128d8fe4a12e9153c0e4a9148378ef722025f6400`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab0a3360f6162feec2879e7e3126049e0d0b21da41b1fed050840ab05d3a971`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 92.8 KB (92804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ba26c21433e511c53d54c5fb11575a7d72252d46be9fa7a5b650fd88f379d3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd38132509fc5b30ae7c308cbf1f8442fa563b2f0bc9c7afe73dcab320746298`

```dockerfile
```

-	Layers:
	-	`sha256:7e1d21b8d945efb0977e9eec36b810dfeef56db66eb730cdac739941e196188f`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 3.9 MB (3901274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da720ec897595af56343cd370a66c397c15083319a49739ecad621242f41de95`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7151133205f5e29a888d57d9cc3893ecf84ae45f66f16fd78a845f9c428182a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609e7edefa5d4ddcb00bc49aefba19a64d4d8a972c23b5517ba1197b01424d42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7927b2dcee59c324d2565fb954b8c435214f8fdeb6bea60c0852e4d9c1689b0`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28aec732af5c3c764498d4ea15c9e9a9cfb30997ac2e931477765f8163e09fa`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f03c91194fd4cd000dc5b677f57a4961e7bc5ff7d6c8815b8f729aa564467`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc847eb0d1afe5aebbfbb461b0caae9339fed614b6c35baac60aba3f7208c`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 93.1 KB (93075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a021c62427f5972c0c86aa895597e0677d3d861b13ea26f1c532d1cc6dc5e6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8912d78eb20420e18e6a15ed39490b62c05cf49060ecaf7d126556c59573e0e`

```dockerfile
```

-	Layers:
	-	`sha256:a60bff322a94b2e3f769e957abbef52371798c34b913d8ba518649cd27526a68`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 3.9 MB (3901527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9eee892cc06efb3b50aaf13462175fec88e9e61e07525711fd62537db8f0a7d`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:0f592d970d198131d771392be8f50cbe787bb485edcecb8e40e571cd28cc4715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533e5d8acc4a4f21d329a2f33b7e522189a199396c7a2b291c39b8a0a12d7294`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d923f2eb1e2154b3a147736c77c3edb48a60836f866c364d42a6cf55b3e26ec3`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 11.7 MB (11689061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44359970c511727c527231627e1a09e37e6c9a71b001ca66ba557b9e2463e4f8`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274bf96b1a4362e957c7cc72e7b8cdda7e48651d1d09242f397ddcd42a79502f`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eb787fa80bf1faea1fb470b9d01a2e6f09ba135d52bd822ded5a09d9553edf`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 92.9 KB (92881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee8acc3543e9a236ede8af78cb2a106f90e114816e2ef0de8a15e4ace80aa050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79ff3eab2a6aba6243ddc92d0a86a9d2d9e6183a76fdf54864e6b2e9b501ff2`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa8d521b076a3fb8f1abb5ee88865787bff8d6d911443d2e756ab6f0439f30`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 3.9 MB (3899191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ff17d585c3e7702667afd240ea49b31293c3f29e91adc86ad66fe608109df5`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:27e5d99204405da3882a3bc5af6b5c4ba65c23dc8e9ecf30dcb861db46a1984a
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
$ docker pull neurodebian@sha256:e3bf02662763b1d5eed34c1a4c1b8e3dce143794cabdca3c4be8d0c5dedba8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9633672d57a08f62cdbd025d79d06e31a9915fee95a82cd7fb7f32e772f5e3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e0953de06e1b01ff7d2055b9f20a3ba20a1b7c1b748c5529b5f072d20d5952`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 11.3 MB (11266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832603be935a7fa29c32943f55bb20bace3e68a72ea55d378d207ec681cfb62f`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffa9bb75d9bfce162acaee83c0a0c73659d5290224c0ce3c945a841f43c68b`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509d4b428934a9fbd54daa8f6a05ab55ccf6275ffcb89ff275bf65ad5d986886`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 92.8 KB (92820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677717d1fae198d1b12a8ad6dc403da87dc3837cac5902e3759b7650eac3a07f`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:05990838518fbc3b56779b4bd1c310b7a4ae5b704c480343c6da477fe6882894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f3904f777bef580a9c2b202de145686a8d49391d8146d08bc7a3c60d4df54`

```dockerfile
```

-	Layers:
	-	`sha256:56b145c5026738fafa379d7efd9615cbee2a070dc428efbc19ba0dbfcc4eeae4`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 3.9 MB (3901314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb50d3266d3f97f7c3f6c15944c6604256404fd2942bbeb309286e4dda2871df`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8e94f874f91854196e6076d6b2257915da8829a2dbb0c69fc71c69daf1b8ee7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fb5732480a63ed944bfc38838f7166af4d048cbc08d2e568a1b23dbacdaacf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7927b2dcee59c324d2565fb954b8c435214f8fdeb6bea60c0852e4d9c1689b0`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28aec732af5c3c764498d4ea15c9e9a9cfb30997ac2e931477765f8163e09fa`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f03c91194fd4cd000dc5b677f57a4961e7bc5ff7d6c8815b8f729aa564467`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc847eb0d1afe5aebbfbb461b0caae9339fed614b6c35baac60aba3f7208c`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 93.1 KB (93075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510daac82ff29d856863532c2947e9b7b4b8412958014b7e27b1021ea231433`  
		Last Modified: Tue, 02 Jul 2024 16:01:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8021e1296bb25306964451cdb5141166c468b34ae37368033bb8f1d65aed8ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5e58c1860b53852a190f8de888e8ee2d107ed81b36e6b278e6169323e6f620`

```dockerfile
```

-	Layers:
	-	`sha256:c5dfdeb03102caf3591bb716ffd684f322a5eea6d9de32d2b05adbe0f0760d99`  
		Last Modified: Tue, 02 Jul 2024 16:01:26 GMT  
		Size: 3.9 MB (3901567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb6da297076341b367ffa715a3be15c6b200ac589dfdbb604dcfb9da878c451`  
		Last Modified: Tue, 02 Jul 2024 16:01:25 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:efb49c63259515523fe8ccd10d2e69cccc919b28b7d019e9ec01ea54dcdf06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11abf557d49f8f62cb12bb0f00abbe6d2f11a5c5cdd67090adce1925c9de4da4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cf0ac242a3e8035e29b47f122d86973244dee2f1be303a17ff4b0938c482d5`  
		Last Modified: Tue, 02 Jul 2024 03:20:03 GMT  
		Size: 11.7 MB (11688947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4332763d9633e70311cf57bf761078910fc849e2a62e3e4ddff60d9b01c7009`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7a762c898e69a0d9a80b3d2b2a66524cf758c0814f0b0f1d26a28eb5e5103a`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764619c52a862d5c56b2e868e4f339f49c9456df8469c5f8e9f21f6ff7594e7`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 92.9 KB (92908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da9e058b6819c454d94409d52846b774b660804f0e4d95cb2370d94a3f56ee`  
		Last Modified: Tue, 02 Jul 2024 03:20:03 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b9fc7157c7288d7c94e2b56229184ddf05d77f7e6ac1a03a3e6e755e66805e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a603113a72528b543d99a038c8ae5cf497833a1667db080ece5b7db83a9d1`

```dockerfile
```

-	Layers:
	-	`sha256:f8cfbc339e6496e89b256cd214b6f00cb1703ffc7269a8d5064a68da0dfe20f2`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 3.9 MB (3899231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a0024b48cc8c7bca0377f145743883b2cce1a49c5c8b64afb30495c6131988`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:5b8a157f1fa4d153ecf8b59ddcefafc69a3a12c5e6b0a303a3cd2f05f9284957
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
$ docker pull neurodebian@sha256:e0bf514a0d34ecdc8b002e7b22cdd78068a509b97bb1cecc113fc3b4b8066a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33b8d06712b2ab86f0d1b6ee95c1732a91b184078d2afe46f52226a4c5dcee5`
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
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a181a4a3c4cf0bf326ca6d6ce4a6acde2cec0980c6164d6364aac4481ade0b0`  
		Last Modified: Tue, 02 Jul 2024 03:19:32 GMT  
		Size: 11.1 MB (11105038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21225520f7ff518fe183256cab94da710e68586dc6e8b7929b637e7ed0cf96b`  
		Last Modified: Tue, 02 Jul 2024 03:19:31 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2978eb695fe78a3741a7e22bb9251e99406a5d65c6e3d2e4904c9286bac48c8`  
		Last Modified: Tue, 02 Jul 2024 03:19:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e8221f8ce0d5a15c0fc3a0d7208cd3bec1bec51c813bf19b825decdb73bfbf`  
		Last Modified: Tue, 02 Jul 2024 03:19:31 GMT  
		Size: 100.8 KB (100761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2f4c9f413303bbc8b960824fbc95b20b625f2311edc3e98852fbb2bd66abd3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ba2645f04d3eb21b231fdf99e9586136f6ff3b2fe63b13f6dba135c7a861e3`

```dockerfile
```

-	Layers:
	-	`sha256:e44f79f1ace122ac207115246bfcfc9b02de8c6951a412ef5855f851599c1831`  
		Last Modified: Tue, 02 Jul 2024 03:19:32 GMT  
		Size: 4.2 MB (4198737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e12ba6b2875bec7706c65a98634ba58d08c1b93ea121457c42bfa95d58eb44`  
		Last Modified: Tue, 02 Jul 2024 03:19:32 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:27f7ce63a6f01e94271a444ec8f2373995dfe45b1d6c054f6a0d76a0d72cd7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64930188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dce8532ab51547b2329e74a8a014c54214e8a483a18c1f3ec68baef5ab81562`
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

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ebfc64feb504c89d3159e3cbced8c45b51e8ed2073e1bf012f7c31d2332e9295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1672e6d61b630c5c0f7e8a379fd15f7c2cf8d5275f7e5791bcc8958edaee064`

```dockerfile
```

-	Layers:
	-	`sha256:58d9b9f740475799a7fb732f54132ec98e9d19ee6c493533853d7b0744cddcbc`  
		Last Modified: Tue, 02 Jul 2024 16:00:10 GMT  
		Size: 4.2 MB (4198342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c240d8bbf66e950f232ede0ffd3e5cf89970d0db93a1c7eec79cdfdf40cc7c`  
		Last Modified: Tue, 02 Jul 2024 16:00:09 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:019cf6b18fa8d325c364835a127dd355233f0dd1667463a407b05e7d9f2a5e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67667751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c620322fd7504ee091a4c60dab413cb848763328a7919d1ab43d65fcd6a8fb4f`
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
```

-	Layers:
	-	`sha256:72a2b38d7f88bb9b0be6097180e8f8261c31815017cb512a158422c2bfba6973`  
		Last Modified: Tue, 02 Jul 2024 00:43:02 GMT  
		Size: 56.1 MB (56064975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313658cba670b69704c21bb3b6cd683cf6bb3d4ee71081c8254b350ce53ae86b`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 11.5 MB (11500171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be962056235be3484050152106eaef9d76a079efc4e0fb9f08c53e92a416b780`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d583c35d672ad69bc748fe666b938bb584c780453ed5b17549c6a4ac885221a`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bea244501331be599fdb702ea10f34d3bd162e65df75233b62c5f9fbe99bf91`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 100.6 KB (100620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ddd6924651e6101933be098f3d127561d6a42c9b386055efc3d0f6bbc0ac0630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7b1d3f3797a1c1f8b72c58e52c089ccbd17adaa20008d6171a072bdddef92a`

```dockerfile
```

-	Layers:
	-	`sha256:2df1b56ccd97b78fb638bf67ea0fefabef37e722fd606934f889c027be4686b1`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 4.2 MB (4195197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e8f5abb370649cfb19b1cc40973f4cd40ae43c2f5348990ae6f582df1c7ac6`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

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

### `neurodebian:bullseye-non-free` - unknown; unknown

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

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:edb263dc1066d7f87dd8711aa0800bf1e1580ab43d82f8bfc27aa45daceaa777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:ba6092bf310c54130b9f46a6f86691ba0c1d67ba1ed3d835a162baa99abe0e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61071084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff39e7247fcadbe53c1798f2d1814082cf109cd683049d792a2ce144c674a19`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b27899bf0a8d8b410efed70f01bf312669da6f68abdaa68e5f6c0f4be18b1fe`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 10.3 MB (10307522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6b00f76d19036c95d91763ba410da86a6b529388b6bc37c6918db191c4d98f`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a03af6c7ef2e49ec9931727bfe5db16be273bc730330e78b0fe95a71070db16`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290b61c7a7487f5ecd78e9e2fd987a6b8a7bed99b47685294a58073df804dac9`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 104.2 KB (104206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a7b5050bf51fee196fedf7681cf858ba20eaeb314b4931a22fa50118cd5627e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb76fec206f8dad74637c6e97e5eebcb910647b26689296a58a6bf127b86a09`

```dockerfile
```

-	Layers:
	-	`sha256:e707f48bd06ec7ba36328c123e2d6a1a423ada9711f1be26c6ff2247524bda5e`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 4.2 MB (4215066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79edcb763fb5445281cd87f8155755f08061719948117b2a9a5697f828961313`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 13.4 KB (13450 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fd746e2f8879adaad1070324be21cf059380912535c42573683deecfd8ddf612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da29b891493a9e7ecc596a7298090ddb62ec08f8f547608f6cac3a8570ad970`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b27aa5e3def1997c89f7bdc1f4e88d9b5b55f9828ac737b3c69360f3981256`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 10.3 MB (10313240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3b0287bdf89ea74e53a548aabae1fe03c0146c47bf2c0dc275edc30feed8`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033ef7f47caf7b9ec62046617a97459accb5b59a7cc2e9fd7d3befc1d3ff35c2`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a1bedd9437d691d7cf490e49ada31da729b4cc5bbff2f97af90bafbe84605`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 104.2 KB (104199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:91a424abc4307bf97a5eb20afe90834b1d3d40de0192a492e59dc8c0554765de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fe1a355bfdf96a96063cacd98766cfd9686624ce61eefcad52ce5c47d6ac77`

```dockerfile
```

-	Layers:
	-	`sha256:28d09605101094cf05fad8cffebe9f3f83debf8f039730924d4ab94b0a8a0b2f`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 4.2 MB (4215248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f11f26f2f2ec9fc71bd370d9282834fcbb5e9e7fcf66fa6a57b1a89c0a68c8f`  
		Last Modified: Thu, 13 Jun 2024 19:35:12 GMT  
		Size: 13.7 KB (13728 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:a76163b14df3412f9fea6b62101c8a3b3d81de779033ed78e753808b5d54691f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d280fa1db207ab1f86834891883d03e8cb9a15474e5d1b0a8e770440cb2201af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81eb6eaaa2db2f8610ccccd6bc1ba567a8f98b64e095fcaa6ba4dd344f99536`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 10.7 MB (10672362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e86184655aca75d86e8a7877fdb2ec9818923ae12e4ba8c8b6b6db64c0e816`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011c068dbed62dd0e7dca412001239f4d7843c04a22269387f161efac14a4e88`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3508b221dc7ad79957c24ad801f8116269b56190b332f04297e3cd58dbdaf239`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 104.1 KB (104134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6278e610ae8ff4f4069e330c959564104dc879c91f2848a3203547845a068740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0046e2e2e4e9ca91514877d1878562a0cd2e29ddd3d5ef59c27a594b325407`

```dockerfile
```

-	Layers:
	-	`sha256:a6e587ad4166f1ecbfdcb34af2443207d1ffb170307bc4619c3a3db05fd5eab3`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 4.2 MB (4212312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa44bf7d0ef4d049cb38b1d14a0405ee8ee349b6b306e47e1b41fc87ce50915`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 13.4 KB (13425 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:701901ea9ba548d62c21b720af5083e6062499f31f108e36e68150ae3dca74af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d982fb8a9ff6ead7d630eb1e851c615db56c391e38b3708fc7887baa66cdd5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61071453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9ae61b9794f926d1a6ee3c26201d26654f555379ce1431812687a5628dc7bc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bcf4dbcb1a4bfd2a81858b9d0d83395974965a1abb6d86a818466b8bcc263e`  
		Last Modified: Thu, 13 Jun 2024 18:29:11 GMT  
		Size: 10.3 MB (10307535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8015ad836afea9b24bdf6e4d2d35c74ef6272ece2dbfadb9774ea1cb29d2acf3`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b881f6ee9daf306c8cd344b4dc00f017523fadae7fe8f0de778dab6bf6c973`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497302dd2576f598d67b7d31d9a422f1378812f40f898affd47d36d58d2ee2b1`  
		Last Modified: Thu, 13 Jun 2024 18:29:11 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9f2707fd15ab253d9db738b3d975f5021efb2267fafc7a6916beebcac6f6f4`  
		Last Modified: Thu, 13 Jun 2024 18:29:12 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b6c5b0d9b9620f4fc891599ce914cc388e35e049e932ff5777435eb833a88f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225831fed7c66b8f267999a4d1ffaad4ab6a50e76e1f1c6c26a2620fabad195c`

```dockerfile
```

-	Layers:
	-	`sha256:eb630ba519836ed0aa82819eb99ecec395929a7071daaa953373c58c36455aee`  
		Last Modified: Thu, 13 Jun 2024 18:29:11 GMT  
		Size: 4.2 MB (4215102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152ab5892a0198a6f90c56d4066198b4bf3326f188ca2ddabbce43e600ca9b86`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:90042e51136c18b22f29bcde48518334d98b11d6f5e9ed074a739ad5e23e991d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59873044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fea009a5183136627105f96bf763f2edd3a34d9428abaf183d000e51db00c1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b27aa5e3def1997c89f7bdc1f4e88d9b5b55f9828ac737b3c69360f3981256`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 10.3 MB (10313240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3b0287bdf89ea74e53a548aabae1fe03c0146c47bf2c0dc275edc30feed8`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033ef7f47caf7b9ec62046617a97459accb5b59a7cc2e9fd7d3befc1d3ff35c2`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a1bedd9437d691d7cf490e49ada31da729b4cc5bbff2f97af90bafbe84605`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 104.2 KB (104199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959acd77c1ea6c0d19eb80bf589e44188fd4b4429b9fbeac6d124c223bb0581`  
		Last Modified: Thu, 13 Jun 2024 19:35:32 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b2a9fc60bc625ab54f74b550029a9867810040fd46d61454972136511b5f5942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4231046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c920c3450da6d14de1aec48284e0caf2f54d90a8190e8f36c06cdf9a1bee59cc`

```dockerfile
```

-	Layers:
	-	`sha256:462ecbaecbe3703701a1f75f4677a588b94bf3f47ea9288d8b865b26b36061f7`  
		Last Modified: Thu, 13 Jun 2024 19:35:32 GMT  
		Size: 4.2 MB (4215284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e19e467a6a4c52fc701ad217d5e512ab94a2d12923fb2f130572f9f740dbf8`  
		Last Modified: Thu, 13 Jun 2024 19:35:31 GMT  
		Size: 15.8 KB (15762 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:57f983e7f9f86acdfddb4d3f06279856dacc0db529dcdf3e7d9cfb75d9995c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8dd97f0a56db69579af7f6cb93a852bb53bc5231bd3d65066ca16225070f88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e86b3dc0faa0645c9c93e23b272579368c4be6a1dfa842fdaa79acf07923271`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 10.7 MB (10672417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763ff0412f0e24675a3c0094d231bb5d4e8e02027bf12f3b704a8d7af2450df`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d3a22329274128cc292bb8b17fbfa44e331807b81e2d773c7cb72f3eaa412d`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34750594939305441facfa5a6eefcd1cb932fb637d427e856e2d4fd8a40cb69`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 104.1 KB (104132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbb066394ae147de6d5ae62491985cfc67be643195f5d6cec344e2c6a9bfd20`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c6a7a766039d129b00d2cb80d7d5d41439aaf354b23075d1e7326ce2f8c304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1dc63b452c68125e8b1db6aac43ab686f120d7c6ac5815663e27bcdb864f93`

```dockerfile
```

-	Layers:
	-	`sha256:e2d563e3f4699cb1c3477375f76ac57e49733df27f30dc7ea01c8cbf4dd17229`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4212348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c16586447c4ba568049064444e9027010f79435b5b909d83ee830c6561b3bb`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 15.5 KB (15457 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:35696f693b6ef96260422b9091c766188a7983d82eb58b1eb04f6bd7b58ce84a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:8436872dff585d3f4fd9ba47de2a0c07d2c9601ea7683cd5d98156073fb3e61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c59f4bc1665f4125a9108a35f53ff8fd3c0f0db4bea3086ff4c0cb4117d2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aadfed4b17ce30257b1e83849176e62dda5f82aa6e95a8478f76eec14d065d`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 5.4 MB (5360246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad67a268cae8111d8fe8b7df873538bdf930ee3af83bddeae455228cf4b12a`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d727c6072b0d91a97e0e503910ae3a3875e0eb0f330dad37430449c5d538f6f1`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a1cbd18209d18420e1b340bb0af4bf1810b5523ee10e459833effca52500e`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 105.2 KB (105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af0c65cce1965a1a6b3c2b2975e967c195bd2eba5a033dfefc365029b377dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45da22baf7d2b89589eaf2d5f3e761d81c297d1c7034615e130e5031d2b182c1`

```dockerfile
```

-	Layers:
	-	`sha256:b358a4f2b71ae1fc1b775755876a2990c2755cb455ca4551f7204050603fd0fb`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 2.0 MB (1977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:543ad7176c91bae6840122d5e6913e1dabd6c77bfd53962ded0190dfc7eaffd4`  
		Last Modified: Wed, 05 Jun 2024 02:20:28 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0f5b1443b574b5ace2b0987cd1977e8210613ba725ed472573cfbe9c5cfe23ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b273064c8a6c81f5cacbef5005cb8661311bf23c477bd55a7c401646da2abe1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:284dd670c2b0916e7375fa296cc94b380cd5d78ea887f00690b52596df26c8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3a8fbbf35052ef29f84d07daf978d8d877ce6f9fcacb449acf1ffd0144aba`

```dockerfile
```

-	Layers:
	-	`sha256:813766013ab606a80d4443383a3397da61d8900db25f42772d29d6cf04b2bce7`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 2.0 MB (1978184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1bf415abcaaa1e6c9340665180fe32490ac956e54c13e38d2b031ff973533bb`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:69eea5eee69951a81433ff44e3a76d25374f43b5ede7e2be7991cafbb9ab8480
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2614cd1459a929df672f30c4de3ff5f4f423b10d0204439ea00b153fb35a4ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ba3c03399056b312baca33d2bef793afd92675c192b7d90af7db16bd0fe08b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab32168f62b0a56e9d1738ba27dd0e7b6b3b7c2e892a19527bf5495039d950`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 5.4 MB (5360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5f6a989efa6cf7d58ae9018a40243e81a4b1bdcb7a242de74e77d92f945db`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfefe3835ca69f4b947ebba8fa742346a61ebab4361ca98d383e7ba7489fb004`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc23cea86c9950d617b60a8e9e162dfa93280986c8e4ea3c9efc6450810bbd`  
		Last Modified: Wed, 05 Jun 2024 02:20:11 GMT  
		Size: 105.2 KB (105229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026d40b80d1375c0c978e08b9ee3768e5635a011dcf98d75ec8a728fea6461cb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8052d782c0e8c3437bea67acf4b2a22d79a7dffa5297317f4776bdc773d0701a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1993579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b545e88e893b1df4e4133705e4b3af666a09fa688c52562b97322c9c6d4c0099`

```dockerfile
```

-	Layers:
	-	`sha256:fa21014e2151b093cd2b0f181163b6be1985c8371a5cc2d7e52e4613433f80bb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 2.0 MB (1977992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15b3763a1a7a0714189ffe6046baae58c42e3ed9f083352e41a11ca77cd14e5`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a765833d6e8524c6babfed520f054ff84a6adea03bbc27c95574cb07aa8fa14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10519d9344ce22cf8b6dffbe4a09a105acf140f518107098b2c66a242582141f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5151156e9cc1c424bbecfc412c4effcbd14bdcecf53693bab61b678ae9ed5fd9`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d450bd9f532b807f700d228fe37fceb706c7960f3b87d06090658a57978a3d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1994083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e25fe54f10b92c153df2cdadaa8eb3efa03f0dee4e099174db24e3ac65946`

```dockerfile
```

-	Layers:
	-	`sha256:ed1c978d1833cda54dd5250213c0833f524702bb98f9f00a81505d89c5d1b173`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 2.0 MB (1978220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b63cad0b9de5d2bb91de6e7fb6616926fabbf2094cb6ffb471176092d3df97e`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 15.9 KB (15863 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:ec0ea51809c4a7caf3e84ace97c51774a2c4a8a756870b79c371406dbd1b71ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:50332ada0faa254b85fa3c99a2fb1022451d84260772392e0e6ae137e1769632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324940094fa472191de171a4ba863183350cf4d1a1e43ccc421a71b66e094cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d862268cca33b20dc33b79c6e362573fb742dcd42a2c8a20009493450369ddc5`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 3.6 MB (3622702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7004f9084ccb849430b7c98f8ef2eb567e8caa461377671d0ac1aba06db6d2`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f70324bbe5ab5ca9fd0e2cf5ea3b95c81703e6cd98a5b415809ceb4638987c`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ced8e730e6d5dd8769cd1bdbbdeb4d189659f419d807c42534b5d3654f8c48`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 110.1 KB (110097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f4826a37a310d849e4c83b7f084dee6af9a823f43d94d62ac6a708b6ec638e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f326f94e3b16867754bfd251636fdec9ac49e83e1e1cb329c204511c7e7ae1dc`

```dockerfile
```

-	Layers:
	-	`sha256:7246425b0d75d34d4e317919e463322149ad3be8c5ef7e9c58c8dc4712ece091`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 2.0 MB (2015659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ed2ec0795d1e6759f5395fa3f89dc5ecae1e9b4c754824dab0613aa1226807`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9bcf1392985d3afd0ecbc668940d0456f696bcdf4730bbe47f0cd4fa295bfaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31066446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d877dec38ef78dcb8000403d7491c4618ddf3d900efc02d7a784d5c1185d7e6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc16b23ee00d53f4adf324698b87c709e486e05c5b634739181bbce1d56c82`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 3.6 MB (3594186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f31c419c5921eb500e6bb4d1394cbc4cce89c991aa6ea0cb14769a2e4ceff8b`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4d5b48676456aba5e60bf7d682a9253b4301c3e43347c5f6b707ffe70669e`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d807b10b523db43ea06a66dc581da167eaaa97bc25dc203e08be033b9c646`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 110.2 KB (110240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14e7e743ccaae8dbbd8443016ed72061835e4425f075357bd75167779976b156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8170de6e72729ed20e70e4dc912f16558b929bdbc526e2c6a9fe606c149a8e1`

```dockerfile
```

-	Layers:
	-	`sha256:6a6fe57d1a82e58c192048c7cb131fdabb2a4364f02324a8fa100b681aa8356a`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 2.0 MB (2015918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5262a37a6988f6c82d7bcf44109f408b46c5d30de14569ccb3690d44371739`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:97f3c220574924fe964fa06d61fc892692bb1a6b009a039df7d5e66c78d35239
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2623a7c28522a7b25eb3fe44172632fc2b1c20a3ac1433aac85570c3d5a894af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69650e35f150a56a819ebf3c57f2723e3327461a3975bd8a64633add1bb9b27d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c600cd6d952702399348890ccb963cad1adb5d6098ffb092caec1a36545b59`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 3.6 MB (3622723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba852eb2127a816ea9594d23647541e8598c273234f40d074e70f717f2b363`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0f24912426a9bcca1a5e3ee9b310973b13df995b7565182f492ab021df7e2`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263c87d1b026352611e6b8267a292c541a135e3842177e774f5f9d5b91f64ef5`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 110.1 KB (110118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8772a37561b5fd83f6ab10e0506ed41d8922a4fd314dce23f19451b55a5d37ea`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dd1b06de41553a1c77638c8b54f222974b849d784be607edd211468735b0c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612275f45e18d0d569032ec2fc8952576023e24a60c792c2616ffa5aad12d4f1`

```dockerfile
```

-	Layers:
	-	`sha256:3447301f1f169b1f3acdd1f023f78fe04e8dd87a9de8dc89f3ef9b82fc18a35a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 2.0 MB (2015695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7244937c2399932fdc4026b34ea0785d361e1562807e9a3c5a205419dd4a72a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 15.6 KB (15635 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1933b2f19205647fc57be0a0ce1f60390d0ca130346609824d899c010635ee7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31066708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d41beebcdb80261bc322b441a2586ca83ceb3ebba450083e4795434e7bc28c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc16b23ee00d53f4adf324698b87c709e486e05c5b634739181bbce1d56c82`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 3.6 MB (3594186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f31c419c5921eb500e6bb4d1394cbc4cce89c991aa6ea0cb14769a2e4ceff8b`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4d5b48676456aba5e60bf7d682a9253b4301c3e43347c5f6b707ffe70669e`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d807b10b523db43ea06a66dc581da167eaaa97bc25dc203e08be033b9c646`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 110.2 KB (110240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ad070ba592bf4d760b4956a98ae70ec4651c7f5db0f4e2aabf5ac2bfe3b2c1`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:13f5ac4a8e9c0cef26a3377cc0f187b30ff2d40b24c8960944ec77b804232628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2acc579da0541db5b1806051198453ff0806569e736508bcf7c0c8876c064c5`

```dockerfile
```

-	Layers:
	-	`sha256:4fea70f73d3b08b467c57896ed29255771bb9295dba7ed13d1e55b6054cfb260`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 2.0 MB (2015954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b174930aea8ca924db6c39b0b1980d1d11b0b31e5eb7814b33f219112f583424`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:5670bf67b386a7e47e9d98f3d7af5f8b0cc4f72a01053db1b62189698b37c065
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
$ docker pull neurodebian@sha256:bb45cc1847f9b911b39cc468b26256bd9ba3859cf8e3320692224fde2e0bc6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6e2c1137a6862e8b108290cdb4757d6147174a18a6501f3f1754cb39e5e710`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cfb6f5dfec97711feafb9c33a2590015ca328f9807711d4d3e62d326aba87c`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 11.3 MB (11266509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46570b27600cb554709fe9a2632cb10f3eebec4088ce4dce4ef9c423ba9f724`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c46ea3d00c2fc1da85fe97128d8fe4a12e9153c0e4a9148378ef722025f6400`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab0a3360f6162feec2879e7e3126049e0d0b21da41b1fed050840ab05d3a971`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 92.8 KB (92804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ba26c21433e511c53d54c5fb11575a7d72252d46be9fa7a5b650fd88f379d3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd38132509fc5b30ae7c308cbf1f8442fa563b2f0bc9c7afe73dcab320746298`

```dockerfile
```

-	Layers:
	-	`sha256:7e1d21b8d945efb0977e9eec36b810dfeef56db66eb730cdac739941e196188f`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 3.9 MB (3901274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da720ec897595af56343cd370a66c397c15083319a49739ecad621242f41de95`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7151133205f5e29a888d57d9cc3893ecf84ae45f66f16fd78a845f9c428182a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609e7edefa5d4ddcb00bc49aefba19a64d4d8a972c23b5517ba1197b01424d42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7927b2dcee59c324d2565fb954b8c435214f8fdeb6bea60c0852e4d9c1689b0`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28aec732af5c3c764498d4ea15c9e9a9cfb30997ac2e931477765f8163e09fa`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f03c91194fd4cd000dc5b677f57a4961e7bc5ff7d6c8815b8f729aa564467`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc847eb0d1afe5aebbfbb461b0caae9339fed614b6c35baac60aba3f7208c`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 93.1 KB (93075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a021c62427f5972c0c86aa895597e0677d3d861b13ea26f1c532d1cc6dc5e6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8912d78eb20420e18e6a15ed39490b62c05cf49060ecaf7d126556c59573e0e`

```dockerfile
```

-	Layers:
	-	`sha256:a60bff322a94b2e3f769e957abbef52371798c34b913d8ba518649cd27526a68`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 3.9 MB (3901527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9eee892cc06efb3b50aaf13462175fec88e9e61e07525711fd62537db8f0a7d`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:0f592d970d198131d771392be8f50cbe787bb485edcecb8e40e571cd28cc4715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533e5d8acc4a4f21d329a2f33b7e522189a199396c7a2b291c39b8a0a12d7294`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d923f2eb1e2154b3a147736c77c3edb48a60836f866c364d42a6cf55b3e26ec3`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 11.7 MB (11689061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44359970c511727c527231627e1a09e37e6c9a71b001ca66ba557b9e2463e4f8`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274bf96b1a4362e957c7cc72e7b8cdda7e48651d1d09242f397ddcd42a79502f`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eb787fa80bf1faea1fb470b9d01a2e6f09ba135d52bd822ded5a09d9553edf`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 92.9 KB (92881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee8acc3543e9a236ede8af78cb2a106f90e114816e2ef0de8a15e4ace80aa050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79ff3eab2a6aba6243ddc92d0a86a9d2d9e6183a76fdf54864e6b2e9b501ff2`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa8d521b076a3fb8f1abb5ee88865787bff8d6d911443d2e756ab6f0439f30`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 3.9 MB (3899191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ff17d585c3e7702667afd240ea49b31293c3f29e91adc86ad66fe608109df5`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:ef536e667e844bef3f025a24f5383edb3acd8ba268e8ecec5d368a914330ea3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:fed4e2b3530c645d3e7f84cab37eae2b044203d0a63b5041fada474651435759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1f6f5d21c24fbd989fcb96724344eda0066e3348dcf06c8929fa5d5c6f83de`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c8a6a2c7c323b5f83d47d65d0855b9448b50e6b97cbef4bd5d73232f349fd`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 6.2 MB (6223751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490f9f972c2ac209587470895132421e429c467f7d29addd4040a25acb56cbfd`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07cd42cb9adf3ecf8f614512a7b6cae459af25dc79dc86de006f68132e9d45e`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb907ad1f19de4a554a7f21be16f71a92e5ce86f2ac6af4a9c84221b0b9479b`  
		Last Modified: Tue, 02 Jul 2024 03:20:01 GMT  
		Size: 90.0 KB (89951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:27b9f3644c9b309aa1a705e3d1fecc58292e8df3308051d0607aca64a23f0aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef885fe31425b485ef042622ab50eccae8d5e447adf219ea5996c50e1633d194`

```dockerfile
```

-	Layers:
	-	`sha256:f97fb27a9a48fc37dbb30f628f954e9883c25fb07c0f8413ceb17e10109b8d03`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 3.5 MB (3542968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ab7593e82d79e46a4371616d56822aa0bab981e2407fa488bd7038da7908d6`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:30fbaf2df2d18158454931946210929a898aac9a510b57a3de067dac3f31205d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59200815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ee26eeee82e9d2700b9e8a5ba5cfe2b0099fd78949a1e36b72fd50b835df89`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f682e5d0d35b6507170549e927b44fa72be309150cc766e8c567a6fff21d100`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 6.2 MB (6219470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1116df5d9885f9a9ff682c06a547c1709ba2c34e3e92865cc80ef986d89e795f`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2529b60acd15a8ed1a099809bf5493031c27bd7255a688091ce443bd422685a`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c43a6b60e4e33f946bea9f325fd364d2d5bd69f0848b7f74b24cbf2aa860681`  
		Last Modified: Tue, 02 Jul 2024 16:02:59 GMT  
		Size: 90.6 KB (90605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:310aee846defdfb760eca13b6fce5779b662d709ed3b6591cb5085bbeb1c75dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16c6093800c166d913f3cb72cced10e90a82d1ee69da07dbf4b58c9e05dafe0`

```dockerfile
```

-	Layers:
	-	`sha256:b191342d93b783e3a64d7a2bb642f2d37be02e8def34c8573eb81969a952317a`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 3.5 MB (3544010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e822a6477f51ada4b8a2b0db1d4d77bf3cbb576c54c263535d3d5d8fa2e38f12`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:a56df304eb1c86cff5dabf46e6ff9297bbb03f3ef255d7deaa00e0b8fdaa389c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60168574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6069e9b5bb86c23e89fd8dad23320f538af8540faf82b86dc52737c7034bb9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bae8a7e43bae044e98255a2206755c69c43385deb06ef20aa0b6503fa088d4`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 6.6 MB (6554390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e11be3bb587e64a347d31a346072a1d6e9ece33f4143863392162f16b3cd01`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f71b73e7356e07f5af8d54e2d18b1d85ecc857f950534783ef06835f22b8fa9`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7898530d420217d5444d31552e4c9f5342f0154e6f0d3ccef93978ec07cb807`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 89.8 KB (89812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:206fed867ae47592e453aab638ddf57f46de701b2e8f5d31586f00ae3e2805e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff168378fa483c4103d74c263824022ec0dcc5e2dec2fccd17229f8aedcf50c`

```dockerfile
```

-	Layers:
	-	`sha256:abd0719fa266c6eeddf8f85db3071c406ba6928ed8be544ffe69e049d85993a8`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 3.5 MB (3540064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263c2eec06e1535e540929dfabee362fe03001b2d54429cc4ced846840ab63f3`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:dd9da3972660d59d3362b8d0703c737d414e035a8cc655d86e4ba7528be89b27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:171d7790834ff2dace09d75d17fc095f5e0ddb5a64ab2f2c6c20e979b8283e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed02da4e0059860be250a87aa0f646a80a9a97405ef1de79b37b13c9eece8a43`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eeeaf4645947114337f3365b9e426c0269613f7bc3b5a498de5bfa2dc9f7d9`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 6.2 MB (6223730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bf23babadbd7e24e99d5f11987ac80999f65bba9925676b393344e7ee94208`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa10af556b8d2d97b814bc8adf79194667d8c4ce1a5024278442d4737439c5`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986345555fbfc0e18521aea6d42886d0b779a81cfe975e9eafc9ed31256d946`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 89.9 KB (89931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0757077789f6773bec41e3ee672f0542a27c2a763cadb11bcde5a56e46ba8dc1`  
		Last Modified: Tue, 02 Jul 2024 03:20:08 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73c2c384861f8818e86257a5bb7c489fe6c75e81009f7d36a5c4787a097dd6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be47e1f771cae7b74651749d34cb0056ec051866bf7e66c883ba536bab0438d7`

```dockerfile
```

-	Layers:
	-	`sha256:174f706621926c8028ac0797d12d9ea16ffd1a2a33d41ecd5081abc4d2df9679`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 3.5 MB (3543004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04024201415ee292c1e9d968a7e8f25fb4fa99f389a1ab14070d733a890e3448`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1d6ee16b19cca79b92541bb682a4c922cfe787ab167987a257b1cb41c69628da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59201205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61af8fb9eb88cbefe347add336cf5ddfdd03de1bbd8def9760ab1aac9ad011d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f682e5d0d35b6507170549e927b44fa72be309150cc766e8c567a6fff21d100`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 6.2 MB (6219470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1116df5d9885f9a9ff682c06a547c1709ba2c34e3e92865cc80ef986d89e795f`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2529b60acd15a8ed1a099809bf5493031c27bd7255a688091ce443bd422685a`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c43a6b60e4e33f946bea9f325fd364d2d5bd69f0848b7f74b24cbf2aa860681`  
		Last Modified: Tue, 02 Jul 2024 16:02:59 GMT  
		Size: 90.6 KB (90605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a830aa41d3e8d87799e4ca16d1813076416447501bca235a0651831bbeeab350`  
		Last Modified: Tue, 02 Jul 2024 16:03:19 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5aaa618816e5505ab338d006a538bd7aff3a3178b69f16b46b95f6d8f64338c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8b09ec1e0a532999060c6cb93a0d079d1073f63d48db887d7e839eff87c70b`

```dockerfile
```

-	Layers:
	-	`sha256:5c69f38169c1a9102899bbfa7a76dc58e3359ac9e4713d70a2f25ec4a7f28693`  
		Last Modified: Tue, 02 Jul 2024 16:03:19 GMT  
		Size: 3.5 MB (3544046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f627c118c0b71eab6eb5458d2d3a87f5691c5e6abee6be8be9f9c1eb4baf17`  
		Last Modified: Tue, 02 Jul 2024 16:03:18 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ccd33fe92961585e691320103b2d0f3466709f199056da460ca62cbe0d5470ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60169098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca223e31f2027f0bea7325055c5d03f33eb27502dddac3a3b4213eeb1fa81e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2067d5ad59a2a2d20bc80327b6f6ed28714940579539b9812e9e2f3157973cf`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 6.6 MB (6554505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc9e048603bc334e451f2a2ff1b8b689603b80171d863e44bdb12c8bc7a9d70`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5ed2c6d104afdf33dcc4ddf797b004d5933a8c960beb94d44ab97ea188f35d`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86bcc6164bd435f1f582154cd31a155f0749b0bfc6efc6e88c71e43f0a28937`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 89.8 KB (89832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b3440dcc43323d1971173e19bc352048910e85501abb4e5672519b888b9267`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e2c0308d75c24d63b042d64f6d4ff437b38ead191a1a197adc3d3dc0075bae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93a2eb119062ea2accb8a0e28abf2cae2a404016d635e3fea9a1e8d94f10085`

```dockerfile
```

-	Layers:
	-	`sha256:8de0478d7152d9c9a0cb48fdddef7ec88969d9806b1b0e61fd124ecbe855853f`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 3.5 MB (3540100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe08c161cbe93376c006e2d9a437eab0416700e73293e4b0d953bcef3d26d97`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 15.4 KB (15400 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:edb263dc1066d7f87dd8711aa0800bf1e1580ab43d82f8bfc27aa45daceaa777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:ba6092bf310c54130b9f46a6f86691ba0c1d67ba1ed3d835a162baa99abe0e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61071084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff39e7247fcadbe53c1798f2d1814082cf109cd683049d792a2ce144c674a19`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b27899bf0a8d8b410efed70f01bf312669da6f68abdaa68e5f6c0f4be18b1fe`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 10.3 MB (10307522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6b00f76d19036c95d91763ba410da86a6b529388b6bc37c6918db191c4d98f`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a03af6c7ef2e49ec9931727bfe5db16be273bc730330e78b0fe95a71070db16`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290b61c7a7487f5ecd78e9e2fd987a6b8a7bed99b47685294a58073df804dac9`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 104.2 KB (104206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a7b5050bf51fee196fedf7681cf858ba20eaeb314b4931a22fa50118cd5627e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb76fec206f8dad74637c6e97e5eebcb910647b26689296a58a6bf127b86a09`

```dockerfile
```

-	Layers:
	-	`sha256:e707f48bd06ec7ba36328c123e2d6a1a423ada9711f1be26c6ff2247524bda5e`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 4.2 MB (4215066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79edcb763fb5445281cd87f8155755f08061719948117b2a9a5697f828961313`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 13.4 KB (13450 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fd746e2f8879adaad1070324be21cf059380912535c42573683deecfd8ddf612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da29b891493a9e7ecc596a7298090ddb62ec08f8f547608f6cac3a8570ad970`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b27aa5e3def1997c89f7bdc1f4e88d9b5b55f9828ac737b3c69360f3981256`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 10.3 MB (10313240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3b0287bdf89ea74e53a548aabae1fe03c0146c47bf2c0dc275edc30feed8`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033ef7f47caf7b9ec62046617a97459accb5b59a7cc2e9fd7d3befc1d3ff35c2`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a1bedd9437d691d7cf490e49ada31da729b4cc5bbff2f97af90bafbe84605`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 104.2 KB (104199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100` - unknown; unknown

```console
$ docker pull neurodebian@sha256:91a424abc4307bf97a5eb20afe90834b1d3d40de0192a492e59dc8c0554765de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fe1a355bfdf96a96063cacd98766cfd9686624ce61eefcad52ce5c47d6ac77`

```dockerfile
```

-	Layers:
	-	`sha256:28d09605101094cf05fad8cffebe9f3f83debf8f039730924d4ab94b0a8a0b2f`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 4.2 MB (4215248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f11f26f2f2ec9fc71bd370d9282834fcbb5e9e7fcf66fa6a57b1a89c0a68c8f`  
		Last Modified: Thu, 13 Jun 2024 19:35:12 GMT  
		Size: 13.7 KB (13728 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100` - linux; 386

```console
$ docker pull neurodebian@sha256:a76163b14df3412f9fea6b62101c8a3b3d81de779033ed78e753808b5d54691f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d280fa1db207ab1f86834891883d03e8cb9a15474e5d1b0a8e770440cb2201af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81eb6eaaa2db2f8610ccccd6bc1ba567a8f98b64e095fcaa6ba4dd344f99536`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 10.7 MB (10672362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e86184655aca75d86e8a7877fdb2ec9818923ae12e4ba8c8b6b6db64c0e816`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011c068dbed62dd0e7dca412001239f4d7843c04a22269387f161efac14a4e88`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3508b221dc7ad79957c24ad801f8116269b56190b332f04297e3cd58dbdaf239`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 104.1 KB (104134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6278e610ae8ff4f4069e330c959564104dc879c91f2848a3203547845a068740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0046e2e2e4e9ca91514877d1878562a0cd2e29ddd3d5ef59c27a594b325407`

```dockerfile
```

-	Layers:
	-	`sha256:a6e587ad4166f1ecbfdcb34af2443207d1ffb170307bc4619c3a3db05fd5eab3`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 4.2 MB (4212312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa44bf7d0ef4d049cb38b1d14a0405ee8ee349b6b306e47e1b41fc87ce50915`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 13.4 KB (13425 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:701901ea9ba548d62c21b720af5083e6062499f31f108e36e68150ae3dca74af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d982fb8a9ff6ead7d630eb1e851c615db56c391e38b3708fc7887baa66cdd5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61071453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9ae61b9794f926d1a6ee3c26201d26654f555379ce1431812687a5628dc7bc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bcf4dbcb1a4bfd2a81858b9d0d83395974965a1abb6d86a818466b8bcc263e`  
		Last Modified: Thu, 13 Jun 2024 18:29:11 GMT  
		Size: 10.3 MB (10307535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8015ad836afea9b24bdf6e4d2d35c74ef6272ece2dbfadb9774ea1cb29d2acf3`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b881f6ee9daf306c8cd344b4dc00f017523fadae7fe8f0de778dab6bf6c973`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497302dd2576f598d67b7d31d9a422f1378812f40f898affd47d36d58d2ee2b1`  
		Last Modified: Thu, 13 Jun 2024 18:29:11 GMT  
		Size: 104.2 KB (104209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9f2707fd15ab253d9db738b3d975f5021efb2267fafc7a6916beebcac6f6f4`  
		Last Modified: Thu, 13 Jun 2024 18:29:12 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b6c5b0d9b9620f4fc891599ce914cc388e35e049e932ff5777435eb833a88f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225831fed7c66b8f267999a4d1ffaad4ab6a50e76e1f1c6c26a2620fabad195c`

```dockerfile
```

-	Layers:
	-	`sha256:eb630ba519836ed0aa82819eb99ecec395929a7071daaa953373c58c36455aee`  
		Last Modified: Thu, 13 Jun 2024 18:29:11 GMT  
		Size: 4.2 MB (4215102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152ab5892a0198a6f90c56d4066198b4bf3326f188ca2ddabbce43e600ca9b86`  
		Last Modified: Thu, 13 Jun 2024 18:29:10 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:90042e51136c18b22f29bcde48518334d98b11d6f5e9ed074a739ad5e23e991d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59873044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fea009a5183136627105f96bf763f2edd3a34d9428abaf183d000e51db00c1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b27aa5e3def1997c89f7bdc1f4e88d9b5b55f9828ac737b3c69360f3981256`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 10.3 MB (10313240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3b0287bdf89ea74e53a548aabae1fe03c0146c47bf2c0dc275edc30feed8`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033ef7f47caf7b9ec62046617a97459accb5b59a7cc2e9fd7d3befc1d3ff35c2`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a1bedd9437d691d7cf490e49ada31da729b4cc5bbff2f97af90bafbe84605`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 104.2 KB (104199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959acd77c1ea6c0d19eb80bf589e44188fd4b4429b9fbeac6d124c223bb0581`  
		Last Modified: Thu, 13 Jun 2024 19:35:32 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b2a9fc60bc625ab54f74b550029a9867810040fd46d61454972136511b5f5942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4231046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c920c3450da6d14de1aec48284e0caf2f54d90a8190e8f36c06cdf9a1bee59cc`

```dockerfile
```

-	Layers:
	-	`sha256:462ecbaecbe3703701a1f75f4677a588b94bf3f47ea9288d8b865b26b36061f7`  
		Last Modified: Thu, 13 Jun 2024 19:35:32 GMT  
		Size: 4.2 MB (4215284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e19e467a6a4c52fc701ad217d5e512ab94a2d12923fb2f130572f9f740dbf8`  
		Last Modified: Thu, 13 Jun 2024 19:35:31 GMT  
		Size: 15.8 KB (15762 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:57f983e7f9f86acdfddb4d3f06279856dacc0db529dcdf3e7d9cfb75d9995c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8dd97f0a56db69579af7f6cb93a852bb53bc5231bd3d65066ca16225070f88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e86b3dc0faa0645c9c93e23b272579368c4be6a1dfa842fdaa79acf07923271`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 10.7 MB (10672417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763ff0412f0e24675a3c0094d231bb5d4e8e02027bf12f3b704a8d7af2450df`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d3a22329274128cc292bb8b17fbfa44e331807b81e2d773c7cb72f3eaa412d`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34750594939305441facfa5a6eefcd1cb932fb637d427e856e2d4fd8a40cb69`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 104.1 KB (104132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbb066394ae147de6d5ae62491985cfc67be643195f5d6cec344e2c6a9bfd20`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c6a7a766039d129b00d2cb80d7d5d41439aaf354b23075d1e7326ce2f8c304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1dc63b452c68125e8b1db6aac43ab686f120d7c6ac5815663e27bcdb864f93`

```dockerfile
```

-	Layers:
	-	`sha256:e2d563e3f4699cb1c3477375f76ac57e49733df27f30dc7ea01c8cbf4dd17229`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4212348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c16586447c4ba568049064444e9027010f79435b5b909d83ee830c6561b3bb`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 15.5 KB (15457 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:5b8a157f1fa4d153ecf8b59ddcefafc69a3a12c5e6b0a303a3cd2f05f9284957
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
$ docker pull neurodebian@sha256:e0bf514a0d34ecdc8b002e7b22cdd78068a509b97bb1cecc113fc3b4b8066a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33b8d06712b2ab86f0d1b6ee95c1732a91b184078d2afe46f52226a4c5dcee5`
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
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a181a4a3c4cf0bf326ca6d6ce4a6acde2cec0980c6164d6364aac4481ade0b0`  
		Last Modified: Tue, 02 Jul 2024 03:19:32 GMT  
		Size: 11.1 MB (11105038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21225520f7ff518fe183256cab94da710e68586dc6e8b7929b637e7ed0cf96b`  
		Last Modified: Tue, 02 Jul 2024 03:19:31 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2978eb695fe78a3741a7e22bb9251e99406a5d65c6e3d2e4904c9286bac48c8`  
		Last Modified: Tue, 02 Jul 2024 03:19:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e8221f8ce0d5a15c0fc3a0d7208cd3bec1bec51c813bf19b825decdb73bfbf`  
		Last Modified: Tue, 02 Jul 2024 03:19:31 GMT  
		Size: 100.8 KB (100761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2f4c9f413303bbc8b960824fbc95b20b625f2311edc3e98852fbb2bd66abd3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ba2645f04d3eb21b231fdf99e9586136f6ff3b2fe63b13f6dba135c7a861e3`

```dockerfile
```

-	Layers:
	-	`sha256:e44f79f1ace122ac207115246bfcfc9b02de8c6951a412ef5855f851599c1831`  
		Last Modified: Tue, 02 Jul 2024 03:19:32 GMT  
		Size: 4.2 MB (4198737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e12ba6b2875bec7706c65a98634ba58d08c1b93ea121457c42bfa95d58eb44`  
		Last Modified: Tue, 02 Jul 2024 03:19:32 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:27f7ce63a6f01e94271a444ec8f2373995dfe45b1d6c054f6a0d76a0d72cd7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64930188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dce8532ab51547b2329e74a8a014c54214e8a483a18c1f3ec68baef5ab81562`
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

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ebfc64feb504c89d3159e3cbced8c45b51e8ed2073e1bf012f7c31d2332e9295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1672e6d61b630c5c0f7e8a379fd15f7c2cf8d5275f7e5791bcc8958edaee064`

```dockerfile
```

-	Layers:
	-	`sha256:58d9b9f740475799a7fb732f54132ec98e9d19ee6c493533853d7b0744cddcbc`  
		Last Modified: Tue, 02 Jul 2024 16:00:10 GMT  
		Size: 4.2 MB (4198342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c240d8bbf66e950f232ede0ffd3e5cf89970d0db93a1c7eec79cdfdf40cc7c`  
		Last Modified: Tue, 02 Jul 2024 16:00:09 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:019cf6b18fa8d325c364835a127dd355233f0dd1667463a407b05e7d9f2a5e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67667751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c620322fd7504ee091a4c60dab413cb848763328a7919d1ab43d65fcd6a8fb4f`
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
```

-	Layers:
	-	`sha256:72a2b38d7f88bb9b0be6097180e8f8261c31815017cb512a158422c2bfba6973`  
		Last Modified: Tue, 02 Jul 2024 00:43:02 GMT  
		Size: 56.1 MB (56064975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313658cba670b69704c21bb3b6cd683cf6bb3d4ee71081c8254b350ce53ae86b`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 11.5 MB (11500171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be962056235be3484050152106eaef9d76a079efc4e0fb9f08c53e92a416b780`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d583c35d672ad69bc748fe666b938bb584c780453ed5b17549c6a4ac885221a`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bea244501331be599fdb702ea10f34d3bd162e65df75233b62c5f9fbe99bf91`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 100.6 KB (100620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ddd6924651e6101933be098f3d127561d6a42c9b386055efc3d0f6bbc0ac0630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7b1d3f3797a1c1f8b72c58e52c089ccbd17adaa20008d6171a072bdddef92a`

```dockerfile
```

-	Layers:
	-	`sha256:2df1b56ccd97b78fb638bf67ea0fefabef37e722fd606934f889c027be4686b1`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 4.2 MB (4195197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e8f5abb370649cfb19b1cc40973f4cd40ae43c2f5348990ae6f582df1c7ac6`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

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

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:5670bf67b386a7e47e9d98f3d7af5f8b0cc4f72a01053db1b62189698b37c065
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
$ docker pull neurodebian@sha256:bb45cc1847f9b911b39cc468b26256bd9ba3859cf8e3320692224fde2e0bc6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6e2c1137a6862e8b108290cdb4757d6147174a18a6501f3f1754cb39e5e710`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cfb6f5dfec97711feafb9c33a2590015ca328f9807711d4d3e62d326aba87c`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 11.3 MB (11266509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46570b27600cb554709fe9a2632cb10f3eebec4088ce4dce4ef9c423ba9f724`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c46ea3d00c2fc1da85fe97128d8fe4a12e9153c0e4a9148378ef722025f6400`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab0a3360f6162feec2879e7e3126049e0d0b21da41b1fed050840ab05d3a971`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 92.8 KB (92804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ba26c21433e511c53d54c5fb11575a7d72252d46be9fa7a5b650fd88f379d3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd38132509fc5b30ae7c308cbf1f8442fa563b2f0bc9c7afe73dcab320746298`

```dockerfile
```

-	Layers:
	-	`sha256:7e1d21b8d945efb0977e9eec36b810dfeef56db66eb730cdac739941e196188f`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 3.9 MB (3901274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da720ec897595af56343cd370a66c397c15083319a49739ecad621242f41de95`  
		Last Modified: Tue, 02 Jul 2024 03:19:33 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7151133205f5e29a888d57d9cc3893ecf84ae45f66f16fd78a845f9c428182a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609e7edefa5d4ddcb00bc49aefba19a64d4d8a972c23b5517ba1197b01424d42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7927b2dcee59c324d2565fb954b8c435214f8fdeb6bea60c0852e4d9c1689b0`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28aec732af5c3c764498d4ea15c9e9a9cfb30997ac2e931477765f8163e09fa`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f03c91194fd4cd000dc5b677f57a4961e7bc5ff7d6c8815b8f729aa564467`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc847eb0d1afe5aebbfbb461b0caae9339fed614b6c35baac60aba3f7208c`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 93.1 KB (93075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a021c62427f5972c0c86aa895597e0677d3d861b13ea26f1c532d1cc6dc5e6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8912d78eb20420e18e6a15ed39490b62c05cf49060ecaf7d126556c59573e0e`

```dockerfile
```

-	Layers:
	-	`sha256:a60bff322a94b2e3f769e957abbef52371798c34b913d8ba518649cd27526a68`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 3.9 MB (3901527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9eee892cc06efb3b50aaf13462175fec88e9e61e07525711fd62537db8f0a7d`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:0f592d970d198131d771392be8f50cbe787bb485edcecb8e40e571cd28cc4715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533e5d8acc4a4f21d329a2f33b7e522189a199396c7a2b291c39b8a0a12d7294`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d923f2eb1e2154b3a147736c77c3edb48a60836f866c364d42a6cf55b3e26ec3`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 11.7 MB (11689061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44359970c511727c527231627e1a09e37e6c9a71b001ca66ba557b9e2463e4f8`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274bf96b1a4362e957c7cc72e7b8cdda7e48651d1d09242f397ddcd42a79502f`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eb787fa80bf1faea1fb470b9d01a2e6f09ba135d52bd822ded5a09d9553edf`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 92.9 KB (92881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee8acc3543e9a236ede8af78cb2a106f90e114816e2ef0de8a15e4ace80aa050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3912946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79ff3eab2a6aba6243ddc92d0a86a9d2d9e6183a76fdf54864e6b2e9b501ff2`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa8d521b076a3fb8f1abb5ee88865787bff8d6d911443d2e756ab6f0439f30`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 3.9 MB (3899191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ff17d585c3e7702667afd240ea49b31293c3f29e91adc86ad66fe608109df5`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:27e5d99204405da3882a3bc5af6b5c4ba65c23dc8e9ecf30dcb861db46a1984a
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
$ docker pull neurodebian@sha256:e3bf02662763b1d5eed34c1a4c1b8e3dce143794cabdca3c4be8d0c5dedba8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9633672d57a08f62cdbd025d79d06e31a9915fee95a82cd7fb7f32e772f5e3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e0953de06e1b01ff7d2055b9f20a3ba20a1b7c1b748c5529b5f072d20d5952`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 11.3 MB (11266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832603be935a7fa29c32943f55bb20bace3e68a72ea55d378d207ec681cfb62f`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffa9bb75d9bfce162acaee83c0a0c73659d5290224c0ce3c945a841f43c68b`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509d4b428934a9fbd54daa8f6a05ab55ccf6275ffcb89ff275bf65ad5d986886`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 92.8 KB (92820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677717d1fae198d1b12a8ad6dc403da87dc3837cac5902e3759b7650eac3a07f`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:05990838518fbc3b56779b4bd1c310b7a4ae5b704c480343c6da477fe6882894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f3904f777bef580a9c2b202de145686a8d49391d8146d08bc7a3c60d4df54`

```dockerfile
```

-	Layers:
	-	`sha256:56b145c5026738fafa379d7efd9615cbee2a070dc428efbc19ba0dbfcc4eeae4`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 3.9 MB (3901314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb50d3266d3f97f7c3f6c15944c6604256404fd2942bbeb309286e4dda2871df`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8e94f874f91854196e6076d6b2257915da8829a2dbb0c69fc71c69daf1b8ee7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fb5732480a63ed944bfc38838f7166af4d048cbc08d2e568a1b23dbacdaacf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7927b2dcee59c324d2565fb954b8c435214f8fdeb6bea60c0852e4d9c1689b0`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28aec732af5c3c764498d4ea15c9e9a9cfb30997ac2e931477765f8163e09fa`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f03c91194fd4cd000dc5b677f57a4961e7bc5ff7d6c8815b8f729aa564467`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc847eb0d1afe5aebbfbb461b0caae9339fed614b6c35baac60aba3f7208c`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 93.1 KB (93075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510daac82ff29d856863532c2947e9b7b4b8412958014b7e27b1021ea231433`  
		Last Modified: Tue, 02 Jul 2024 16:01:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8021e1296bb25306964451cdb5141166c468b34ae37368033bb8f1d65aed8ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5e58c1860b53852a190f8de888e8ee2d107ed81b36e6b278e6169323e6f620`

```dockerfile
```

-	Layers:
	-	`sha256:c5dfdeb03102caf3591bb716ffd684f322a5eea6d9de32d2b05adbe0f0760d99`  
		Last Modified: Tue, 02 Jul 2024 16:01:26 GMT  
		Size: 3.9 MB (3901567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb6da297076341b367ffa715a3be15c6b200ac589dfdbb604dcfb9da878c451`  
		Last Modified: Tue, 02 Jul 2024 16:01:25 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:efb49c63259515523fe8ccd10d2e69cccc919b28b7d019e9ec01ea54dcdf06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11abf557d49f8f62cb12bb0f00abbe6d2f11a5c5cdd67090adce1925c9de4da4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cf0ac242a3e8035e29b47f122d86973244dee2f1be303a17ff4b0938c482d5`  
		Last Modified: Tue, 02 Jul 2024 03:20:03 GMT  
		Size: 11.7 MB (11688947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4332763d9633e70311cf57bf761078910fc849e2a62e3e4ddff60d9b01c7009`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7a762c898e69a0d9a80b3d2b2a66524cf758c0814f0b0f1d26a28eb5e5103a`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764619c52a862d5c56b2e868e4f339f49c9456df8469c5f8e9f21f6ff7594e7`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 92.9 KB (92908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da9e058b6819c454d94409d52846b774b660804f0e4d95cb2370d94a3f56ee`  
		Last Modified: Tue, 02 Jul 2024 03:20:03 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b9fc7157c7288d7c94e2b56229184ddf05d77f7e6ac1a03a3e6e755e66805e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a603113a72528b543d99a038c8ae5cf497833a1667db080ece5b7db83a9d1`

```dockerfile
```

-	Layers:
	-	`sha256:f8cfbc339e6496e89b256cd214b6f00cb1703ffc7269a8d5064a68da0dfe20f2`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 3.9 MB (3899231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a0024b48cc8c7bca0377f145743883b2cce1a49c5c8b64afb30495c6131988`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:2701ee11ce003de748a8673f35592364c004c279b29561eeaf53d4dca9bace73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130` - linux; amd64

```console
$ docker pull neurodebian@sha256:86020420df0eb881ff092dc6370848df5fba8955c08c492c10c8ec8b85400a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58771613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b298dd02cf312117d40ae917c1da44edf9f73928a9f298d159763c5cfdbad330`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:90c4ad8b280b16131f305780a1f2721616642bd4d5b4a26256c760cd8ae98f27 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ca828e2fa86974a7bad5159e89a3c4f34921c624322a7fa71026f2a3933ab620`  
		Last Modified: Tue, 02 Jul 2024 01:31:45 GMT  
		Size: 52.5 MB (52458214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1022006ddf723b7769e7b09a86c825d0f39c97af210df7b7efa0ec35db3693`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 6.2 MB (6221865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efff9e871ba85c68cf52da4df7d44606485ee55c07e5696869a8736c738c5fb`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f13b507f2f38fd158c457d7a6004ca895e873a2738f2bf86bc2cb4d23f1a178`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59df4d655a842435892b91ada87ed87890c6e1eb78237c0b0fe575b22be0ad6`  
		Last Modified: Tue, 02 Jul 2024 03:19:29 GMT  
		Size: 89.6 KB (89551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2db6d78b5be1750f123569779318372c50ec40177ebf0d492c3bfa2bf843c26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206dc903c6cae6216105a228224595e74dfce8ac34981a81b87429c9732e787b`

```dockerfile
```

-	Layers:
	-	`sha256:af82b7215c2c96f47e852e3f56fca2ceb07957be45d22f7a5c95f3896fe64417`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 3.6 MB (3550053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1108c450e7df3e0e38ce9e9e191c53735ed188725412bbc405098f9d1ebfa2`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e2e6c2dad3e9c25d1ea3d8222756995cff380d4b07a735ce302ef9caa7923db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59005218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef771b1f9ab2d09bce49e0798ad3dd93430404bea3abbb996b1ab7fa7dfadf89`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37e4feb9b85ed81a0244ad32abf825fc3dcfa282fa2fbda1b573a8af3f9c66`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 6.2 MB (6219751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe324133caeef138406fb1d02d698bf04ae634950a378224cd67c28c8e16555a`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a395df2ca4da8df74e14bb8e822fddcd4499bf01353553400165ee04f5d153e5`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7299ee038b6c18a9f4e26e561aed03e451b34e861940756db261f8442b57ee`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 90.2 KB (90162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b1ee57b09d3fd6da3028ca30cab64722635764b475ec4a9abd08a7a839c9e99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a272f25b7a111c41cb3956571ce6bbf199816741392cee26c52c7b5887fa9c5`

```dockerfile
```

-	Layers:
	-	`sha256:353bb6b1a72e8745732e2dfd1dfdd3fbaa57e5a15452660ab3c31ce08d8d09d7`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 3.6 MB (3551094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c000a857e95c72571a967d744d0dc0377de066348a21f7435f849c2487c0a994`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:1b979e614b797a8e6b34dad7b4f04b675c9f817d136cae9d1e5cd5c6d2843c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59976885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8097c6780368356f0da76878203ccf56c2f6b468adfe12871c37587473375b59`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773778424cc9dd30f34b0dd99d912fdc8834e380ae80f2e3c094f79b333371eb`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 6.6 MB (6552263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03f370391c3e5d2a2c06f5c4e17ff675a2040a1785b48448847fd13640406d2`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0856b336a87b5b8ccce813aa69b8c8c6107b7ef7b2d1a7514f48079ea8879`  
		Last Modified: Tue, 02 Jul 2024 03:20:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26929505ada2c90ca7c24b4b14e04f9b75d63a1b49697b24ef448a887b7b876`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 89.5 KB (89458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ea8c51894f88b655386564b901f2bede4dda51a89f560f9dfcb72d562b780aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d1651ecf22805116196871bac4fc49400b60e97899802823523e5d88b4f5df`

```dockerfile
```

-	Layers:
	-	`sha256:942435d1b26d9543557c7ad883cb0f7222ff9d38610630a779a694428d5532e3`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 3.5 MB (3547152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54cef61444c589ba1dfabc4da40f457ede60d4586c9b8427e800e242c1bbe689`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:cbc3dd545d9b9b037c2fca20f1793ced8892493eb8ac076dca08a8c033bc4f64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ca2379877bd375136f0bebacc15725191bb411a53cf4085f66157875892ee4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58772271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353f68948093fbaa77025ded231eed6a7e3840a86d3b0e561d6e5044235db7b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:90c4ad8b280b16131f305780a1f2721616642bd4d5b4a26256c760cd8ae98f27 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ca828e2fa86974a7bad5159e89a3c4f34921c624322a7fa71026f2a3933ab620`  
		Last Modified: Tue, 02 Jul 2024 01:31:45 GMT  
		Size: 52.5 MB (52458214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94e3ccf5f5407de3eb05fa25f8e9c631fb1c59095bc2e61399ec9937cba2d3`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 6.2 MB (6222085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55ac663eeae01cec5106afb87e8ed79e49b5c2a7ca82dedd5e9d202d2761c1c`  
		Last Modified: Tue, 02 Jul 2024 03:19:46 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c35d22fc86197f71cf62047c3b9444dedefb03d49949ec9cc27cb11341a8750`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b3b39d2f3f9ebbd735f3955ccf42be6c60fc7c0673cc4d5c8194657c0b132b`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 89.6 KB (89564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830af931f363fe496bb2204c8b062340c0a5d696ce5e499e65abe96c6bb25443`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d1f5a12df29579d00f04b27c04671c9a4b46104c083c3ce51e009255e78c13a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26a3126ea213714cac4c2bf30e583440725b7bb70d9515a469e0e0143f1b868`

```dockerfile
```

-	Layers:
	-	`sha256:da24285cb8b8757dcdb2fb6b31c55cf2448b50fb093ed16348ffa0e5b6883b44`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 3.6 MB (3550089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b07cc3761be09ffa10b5dee6bfcb6afd6e6e5f2f6dacc8fd9d99879fd96290f`  
		Last Modified: Tue, 02 Jul 2024 03:19:46 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a79974208a0bb820954693531a9afb3afd106a32f2b757f3fc20227f0f4a0b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59005641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8c8eab87323d42fe26497f851c17fa6e0e5385d3882919e0dc57df605527ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37e4feb9b85ed81a0244ad32abf825fc3dcfa282fa2fbda1b573a8af3f9c66`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 6.2 MB (6219751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe324133caeef138406fb1d02d698bf04ae634950a378224cd67c28c8e16555a`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a395df2ca4da8df74e14bb8e822fddcd4499bf01353553400165ee04f5d153e5`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7299ee038b6c18a9f4e26e561aed03e451b34e861940756db261f8442b57ee`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 90.2 KB (90162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625e1ac3eae348163608b8585ba920626955440fe37f93e4d93ab97263de9118`  
		Last Modified: Tue, 02 Jul 2024 16:02:23 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e527ddb0e1c047facbe36e81204aae3cc538ed471e53e8cab806a22a6496f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44b20d48b8f68b1ab824177e21ae99b3a33f7070334edc4792d84a8cddd18f2`

```dockerfile
```

-	Layers:
	-	`sha256:3d2ab6e217ea6aebb7cb09a460fa739fa8e0af067bf6e31f73cd39f4ad9cea5d`  
		Last Modified: Tue, 02 Jul 2024 16:02:23 GMT  
		Size: 3.6 MB (3551130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a02f309059e7f55a807d43e326cc66a962c7f61273ded799a07347e31fa6cf1`  
		Last Modified: Tue, 02 Jul 2024 16:02:22 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6678b0abf7ce15b47e9fe6e10f34a869f8df78e0c6aa931ed483357ab28e3bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59977316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7f82e6b423e8ce366a692e0015506898918b77bcc79651abc0721a23d1cefb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572de5816e1dcea6e5d7bf1248df78c0a435de0efeef834dd9d0c38567570bd7`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 6.6 MB (6552258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a80c2c6d79e7c89ef04c1b1df81970b923505bad19e787301b1c53ed276e9e`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c830fb8727b7cc750190f85d23fc464ae943a3599eed6b6539911056e7eea3`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d978e8ef47f777662225ca0ad77f6faf928a037988e9242a9558de8a2829d531`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 89.5 KB (89475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bd4c6b10e884e1886dc9dc50e79503ccbac9653d743d726e5c1292b521da11`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:baeca2bd03a0194349bb44d0c311e1c6839f71fce257a6506bae904211aa7d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139e65b3a6189c99551bdf06fe0eb9a714c3c155ddcfb056e712b7011a72c9da`

```dockerfile
```

-	Layers:
	-	`sha256:ef6bdde65a79dcbbe926e238d768dce9b781bcabc19642a5647491d0d72a4332`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 3.5 MB (3547188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddb7644a264eff676c63c86ff6cea3f2e367692140d6e6493d4c3ead6803f4c`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 15.4 KB (15449 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:35696f693b6ef96260422b9091c766188a7983d82eb58b1eb04f6bd7b58ce84a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:8436872dff585d3f4fd9ba47de2a0c07d2c9601ea7683cd5d98156073fb3e61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c59f4bc1665f4125a9108a35f53ff8fd3c0f0db4bea3086ff4c0cb4117d2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aadfed4b17ce30257b1e83849176e62dda5f82aa6e95a8478f76eec14d065d`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 5.4 MB (5360246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad67a268cae8111d8fe8b7df873538bdf930ee3af83bddeae455228cf4b12a`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d727c6072b0d91a97e0e503910ae3a3875e0eb0f330dad37430449c5d538f6f1`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a1cbd18209d18420e1b340bb0af4bf1810b5523ee10e459833effca52500e`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 105.2 KB (105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af0c65cce1965a1a6b3c2b2975e967c195bd2eba5a033dfefc365029b377dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45da22baf7d2b89589eaf2d5f3e761d81c297d1c7034615e130e5031d2b182c1`

```dockerfile
```

-	Layers:
	-	`sha256:b358a4f2b71ae1fc1b775755876a2990c2755cb455ca4551f7204050603fd0fb`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 2.0 MB (1977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:543ad7176c91bae6840122d5e6913e1dabd6c77bfd53962ded0190dfc7eaffd4`  
		Last Modified: Wed, 05 Jun 2024 02:20:28 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0f5b1443b574b5ace2b0987cd1977e8210613ba725ed472573cfbe9c5cfe23ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b273064c8a6c81f5cacbef5005cb8661311bf23c477bd55a7c401646da2abe1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:284dd670c2b0916e7375fa296cc94b380cd5d78ea887f00690b52596df26c8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3a8fbbf35052ef29f84d07daf978d8d877ce6f9fcacb449acf1ffd0144aba`

```dockerfile
```

-	Layers:
	-	`sha256:813766013ab606a80d4443383a3397da61d8900db25f42772d29d6cf04b2bce7`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 2.0 MB (1978184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1bf415abcaaa1e6c9340665180fe32490ac956e54c13e38d2b031ff973533bb`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:69eea5eee69951a81433ff44e3a76d25374f43b5ede7e2be7991cafbb9ab8480
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2614cd1459a929df672f30c4de3ff5f4f423b10d0204439ea00b153fb35a4ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ba3c03399056b312baca33d2bef793afd92675c192b7d90af7db16bd0fe08b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab32168f62b0a56e9d1738ba27dd0e7b6b3b7c2e892a19527bf5495039d950`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 5.4 MB (5360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5f6a989efa6cf7d58ae9018a40243e81a4b1bdcb7a242de74e77d92f945db`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfefe3835ca69f4b947ebba8fa742346a61ebab4361ca98d383e7ba7489fb004`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc23cea86c9950d617b60a8e9e162dfa93280986c8e4ea3c9efc6450810bbd`  
		Last Modified: Wed, 05 Jun 2024 02:20:11 GMT  
		Size: 105.2 KB (105229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026d40b80d1375c0c978e08b9ee3768e5635a011dcf98d75ec8a728fea6461cb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8052d782c0e8c3437bea67acf4b2a22d79a7dffa5297317f4776bdc773d0701a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1993579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b545e88e893b1df4e4133705e4b3af666a09fa688c52562b97322c9c6d4c0099`

```dockerfile
```

-	Layers:
	-	`sha256:fa21014e2151b093cd2b0f181163b6be1985c8371a5cc2d7e52e4613433f80bb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 2.0 MB (1977992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15b3763a1a7a0714189ffe6046baae58c42e3ed9f083352e41a11ca77cd14e5`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a765833d6e8524c6babfed520f054ff84a6adea03bbc27c95574cb07aa8fa14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10519d9344ce22cf8b6dffbe4a09a105acf140f518107098b2c66a242582141f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5151156e9cc1c424bbecfc412c4effcbd14bdcecf53693bab61b678ae9ed5fd9`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d450bd9f532b807f700d228fe37fceb706c7960f3b87d06090658a57978a3d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1994083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e25fe54f10b92c153df2cdadaa8eb3efa03f0dee4e099174db24e3ac65946`

```dockerfile
```

-	Layers:
	-	`sha256:ed1c978d1833cda54dd5250213c0833f524702bb98f9f00a81505d89c5d1b173`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 2.0 MB (1978220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b63cad0b9de5d2bb91de6e7fb6616926fabbf2094cb6ffb471176092d3df97e`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 15.9 KB (15863 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:ec0ea51809c4a7caf3e84ace97c51774a2c4a8a756870b79c371406dbd1b71ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:50332ada0faa254b85fa3c99a2fb1022451d84260772392e0e6ae137e1769632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324940094fa472191de171a4ba863183350cf4d1a1e43ccc421a71b66e094cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d862268cca33b20dc33b79c6e362573fb742dcd42a2c8a20009493450369ddc5`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 3.6 MB (3622702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7004f9084ccb849430b7c98f8ef2eb567e8caa461377671d0ac1aba06db6d2`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f70324bbe5ab5ca9fd0e2cf5ea3b95c81703e6cd98a5b415809ceb4638987c`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ced8e730e6d5dd8769cd1bdbbdeb4d189659f419d807c42534b5d3654f8c48`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 110.1 KB (110097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f4826a37a310d849e4c83b7f084dee6af9a823f43d94d62ac6a708b6ec638e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f326f94e3b16867754bfd251636fdec9ac49e83e1e1cb329c204511c7e7ae1dc`

```dockerfile
```

-	Layers:
	-	`sha256:7246425b0d75d34d4e317919e463322149ad3be8c5ef7e9c58c8dc4712ece091`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 2.0 MB (2015659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ed2ec0795d1e6759f5395fa3f89dc5ecae1e9b4c754824dab0613aa1226807`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9bcf1392985d3afd0ecbc668940d0456f696bcdf4730bbe47f0cd4fa295bfaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31066446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d877dec38ef78dcb8000403d7491c4618ddf3d900efc02d7a784d5c1185d7e6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc16b23ee00d53f4adf324698b87c709e486e05c5b634739181bbce1d56c82`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 3.6 MB (3594186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f31c419c5921eb500e6bb4d1394cbc4cce89c991aa6ea0cb14769a2e4ceff8b`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4d5b48676456aba5e60bf7d682a9253b4301c3e43347c5f6b707ffe70669e`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d807b10b523db43ea06a66dc581da167eaaa97bc25dc203e08be033b9c646`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 110.2 KB (110240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14e7e743ccaae8dbbd8443016ed72061835e4425f075357bd75167779976b156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8170de6e72729ed20e70e4dc912f16558b929bdbc526e2c6a9fe606c149a8e1`

```dockerfile
```

-	Layers:
	-	`sha256:6a6fe57d1a82e58c192048c7cb131fdabb2a4364f02324a8fa100b681aa8356a`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 2.0 MB (2015918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5262a37a6988f6c82d7bcf44109f408b46c5d30de14569ccb3690d44371739`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:97f3c220574924fe964fa06d61fc892692bb1a6b009a039df7d5e66c78d35239
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2623a7c28522a7b25eb3fe44172632fc2b1c20a3ac1433aac85570c3d5a894af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69650e35f150a56a819ebf3c57f2723e3327461a3975bd8a64633add1bb9b27d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c600cd6d952702399348890ccb963cad1adb5d6098ffb092caec1a36545b59`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 3.6 MB (3622723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba852eb2127a816ea9594d23647541e8598c273234f40d074e70f717f2b363`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0f24912426a9bcca1a5e3ee9b310973b13df995b7565182f492ab021df7e2`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263c87d1b026352611e6b8267a292c541a135e3842177e774f5f9d5b91f64ef5`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 110.1 KB (110118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8772a37561b5fd83f6ab10e0506ed41d8922a4fd314dce23f19451b55a5d37ea`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dd1b06de41553a1c77638c8b54f222974b849d784be607edd211468735b0c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612275f45e18d0d569032ec2fc8952576023e24a60c792c2616ffa5aad12d4f1`

```dockerfile
```

-	Layers:
	-	`sha256:3447301f1f169b1f3acdd1f023f78fe04e8dd87a9de8dc89f3ef9b82fc18a35a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 2.0 MB (2015695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7244937c2399932fdc4026b34ea0785d361e1562807e9a3c5a205419dd4a72a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 15.6 KB (15635 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1933b2f19205647fc57be0a0ce1f60390d0ca130346609824d899c010635ee7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31066708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d41beebcdb80261bc322b441a2586ca83ceb3ebba450083e4795434e7bc28c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc16b23ee00d53f4adf324698b87c709e486e05c5b634739181bbce1d56c82`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 3.6 MB (3594186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f31c419c5921eb500e6bb4d1394cbc4cce89c991aa6ea0cb14769a2e4ceff8b`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4d5b48676456aba5e60bf7d682a9253b4301c3e43347c5f6b707ffe70669e`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d807b10b523db43ea06a66dc581da167eaaa97bc25dc203e08be033b9c646`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 110.2 KB (110240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ad070ba592bf4d760b4956a98ae70ec4651c7f5db0f4e2aabf5ac2bfe3b2c1`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:13f5ac4a8e9c0cef26a3377cc0f187b30ff2d40b24c8960944ec77b804232628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2acc579da0541db5b1806051198453ff0806569e736508bcf7c0c8876c064c5`

```dockerfile
```

-	Layers:
	-	`sha256:4fea70f73d3b08b467c57896ed29255771bb9295dba7ed13d1e55b6054cfb260`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 2.0 MB (2015954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b174930aea8ca924db6c39b0b1980d1d11b0b31e5eb7814b33f219112f583424`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:259b321a353852a396595fe3dccae3af14e80acea23b5fa253ccef9abe8d607f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:bc97960df24336fb9ab6ddba39cef28ad5b5981ee2a71c536fc3ecaa3c99c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33362900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cd2f3d101d99b8267c310b3a0379c5bac16f919035486b3add1b7b5ed6ffe5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045c8cfbb245c130721a6cce4ebaedd89b348c2f379bf11bbfeb3454b2c2c334`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 3.6 MB (3556375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d2d8a2f97d35ad8bfefe9e419c256552b427d8b6fd56f66298e27c6cab496c`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b2c472b41de28eb92dabae81984e17e4a3b31534b465f808ff43b6fb7a46a2`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75198d942de23473eb6ea13cc2747a0e564e3f96fdc80ae20291fa9f47bb56b3`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 99.4 KB (99380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:99d8189e975305f1f07e17ecd824dbe2680c00952af5ed50226095ed6c8491e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1960446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9a27a6f5a2270e273af05a7f37c7dafca9bb07e0f08356da7c2b5740bf397e`

```dockerfile
```

-	Layers:
	-	`sha256:05ec958be125c66bf2f39d91bcb27965f188147d7402585e574602d6da467f81`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 1.9 MB (1947044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f13b86b37031b1394e9d8e7c0089f611cfc72d136367e630b15a1dce9e470bbf`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 13.4 KB (13402 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c28c5692fdd8cb6094cf16f901ff1bb8eee7e085a2ef7da969264001f4810927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6375e1dd2dfd99a6f8b88dc59bb53c6a03f5d7ea6d2dcd700b7f3c7d8246f52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107d59261961bebfec87d95f4e1e558ce8e42798b8d28a75edc34fef7bf4b89c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 3.6 MB (3556246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26154957829f9bf3bb985a70068979a5c42aa97b39becd3512c54b7685a00f`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab8b90a3fe15e463e6f48c57d92b4fcf48bc4fc24903cd114dd8401e1ba8e8`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2435f75ec9c31dcdc86d4ec5a5f303baf23cf77f8a231e7aae021ee70f35b47e`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 100.8 KB (100832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71d5864e86f67f564aa0c3126aec7283f2e0f89a9e8ad42d6e31aa2ec7013e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1961771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b0f43f02531953bdb18ca8f475463223d5348b8f4e1feecd67d99f4e3bf3bf`

```dockerfile
```

-	Layers:
	-	`sha256:94eb2bd81873a92dec3252b19c382a0b2497df4ccf57fb01faecc941faed637d`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 1.9 MB (1948089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c43622364623d3bcb476f96cf74141e8cbaf957e54c79e57170d0097080807`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:b96be1088de53c9575d486ca8036410fca479c7e89c00858a8f591ce4fe833aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e8781cda6623406f20d46b9691666b81659a4bb104f1933ae9486ac8f5ec208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33363306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090fe7ce2dee91c02bb8858a9424b7e8a64e040c1558a8c999386a1d694dce5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5a806a7d10c69acfbf90844245f143b3482e6466c123a5c09da2efb8188a7`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 3.6 MB (3556384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60236668873eca6257c1fcfd556cab099eca2191d92cb29decd2e6ae3d9766ce`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1581a86dedda365c08b9c6cfd5bc95959519c98e884e1b639d663882c0146870`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b46e6f530a9a30413e06fa98a60210aaf8e3444d36977e30bcb74336afe08c7`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2be2c0f2bb018655be9a1d817db1ab59cb62c114bc229a444090561cae35e6`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e8eb2d7d6c97d6b4322fb5ff411dbf16c74e1963e2e9460a14c46ef017fe2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1962713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df8cccdcbb2218070b64b3b614767783aefb18cecf75a1baa7f1aaa113e3496`

```dockerfile
```

-	Layers:
	-	`sha256:1768075ff854355336a6a1efdf0e8f55279c7cbfe8476643fc4c349416b6b3ee`  
		Last Modified: Fri, 21 Jun 2024 22:54:25 GMT  
		Size: 1.9 MB (1947080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f1583b6e8effb98ce4b38e5aa71246f3f7849c8a8438e75fe964b1e93ad6d`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7f00f5a48b9b4249d216d59daf7211df3b18af80811ae01887340122eefa8e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c71a47d0235e4dc26f3c57266e0e1d4b92587c896fd20699c4040556bae931`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107d59261961bebfec87d95f4e1e558ce8e42798b8d28a75edc34fef7bf4b89c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 3.6 MB (3556246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26154957829f9bf3bb985a70068979a5c42aa97b39becd3512c54b7685a00f`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab8b90a3fe15e463e6f48c57d92b4fcf48bc4fc24903cd114dd8401e1ba8e8`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2435f75ec9c31dcdc86d4ec5a5f303baf23cf77f8a231e7aae021ee70f35b47e`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 100.8 KB (100832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14adb417e445e782b6c6f4c031353ab60033f483e74163ccdfb6602d3234a0e`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:abd941f9bb109976ae0f41cd5e1cce7c1c58d4cdf895851cbcba66a992e1df0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1964038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb75f98268d56b8ee8c7348c7cac0ff27ed25feb5634301eb1500990213c1b`

```dockerfile
```

-	Layers:
	-	`sha256:dc5a9652ff1195ae6074a02db46430f39cd20c384a53e978e8fee9fb923d411a`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 1.9 MB (1948125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8b3e52ef57e9ec95b816881052676acf6b01d9657ea900f954cf1c28c8a5a9`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:259b321a353852a396595fe3dccae3af14e80acea23b5fa253ccef9abe8d607f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:bc97960df24336fb9ab6ddba39cef28ad5b5981ee2a71c536fc3ecaa3c99c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33362900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cd2f3d101d99b8267c310b3a0379c5bac16f919035486b3add1b7b5ed6ffe5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045c8cfbb245c130721a6cce4ebaedd89b348c2f379bf11bbfeb3454b2c2c334`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 3.6 MB (3556375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d2d8a2f97d35ad8bfefe9e419c256552b427d8b6fd56f66298e27c6cab496c`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b2c472b41de28eb92dabae81984e17e4a3b31534b465f808ff43b6fb7a46a2`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75198d942de23473eb6ea13cc2747a0e564e3f96fdc80ae20291fa9f47bb56b3`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 99.4 KB (99380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:99d8189e975305f1f07e17ecd824dbe2680c00952af5ed50226095ed6c8491e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1960446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9a27a6f5a2270e273af05a7f37c7dafca9bb07e0f08356da7c2b5740bf397e`

```dockerfile
```

-	Layers:
	-	`sha256:05ec958be125c66bf2f39d91bcb27965f188147d7402585e574602d6da467f81`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 1.9 MB (1947044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f13b86b37031b1394e9d8e7c0089f611cfc72d136367e630b15a1dce9e470bbf`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 13.4 KB (13402 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c28c5692fdd8cb6094cf16f901ff1bb8eee7e085a2ef7da969264001f4810927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6375e1dd2dfd99a6f8b88dc59bb53c6a03f5d7ea6d2dcd700b7f3c7d8246f52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107d59261961bebfec87d95f4e1e558ce8e42798b8d28a75edc34fef7bf4b89c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 3.6 MB (3556246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26154957829f9bf3bb985a70068979a5c42aa97b39becd3512c54b7685a00f`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab8b90a3fe15e463e6f48c57d92b4fcf48bc4fc24903cd114dd8401e1ba8e8`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2435f75ec9c31dcdc86d4ec5a5f303baf23cf77f8a231e7aae021ee70f35b47e`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 100.8 KB (100832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71d5864e86f67f564aa0c3126aec7283f2e0f89a9e8ad42d6e31aa2ec7013e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1961771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b0f43f02531953bdb18ca8f475463223d5348b8f4e1feecd67d99f4e3bf3bf`

```dockerfile
```

-	Layers:
	-	`sha256:94eb2bd81873a92dec3252b19c382a0b2497df4ccf57fb01faecc941faed637d`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 1.9 MB (1948089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c43622364623d3bcb476f96cf74141e8cbaf957e54c79e57170d0097080807`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:b96be1088de53c9575d486ca8036410fca479c7e89c00858a8f591ce4fe833aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e8781cda6623406f20d46b9691666b81659a4bb104f1933ae9486ac8f5ec208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33363306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090fe7ce2dee91c02bb8858a9424b7e8a64e040c1558a8c999386a1d694dce5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5a806a7d10c69acfbf90844245f143b3482e6466c123a5c09da2efb8188a7`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 3.6 MB (3556384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60236668873eca6257c1fcfd556cab099eca2191d92cb29decd2e6ae3d9766ce`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1581a86dedda365c08b9c6cfd5bc95959519c98e884e1b639d663882c0146870`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b46e6f530a9a30413e06fa98a60210aaf8e3444d36977e30bcb74336afe08c7`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2be2c0f2bb018655be9a1d817db1ab59cb62c114bc229a444090561cae35e6`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e8eb2d7d6c97d6b4322fb5ff411dbf16c74e1963e2e9460a14c46ef017fe2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1962713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df8cccdcbb2218070b64b3b614767783aefb18cecf75a1baa7f1aaa113e3496`

```dockerfile
```

-	Layers:
	-	`sha256:1768075ff854355336a6a1efdf0e8f55279c7cbfe8476643fc4c349416b6b3ee`  
		Last Modified: Fri, 21 Jun 2024 22:54:25 GMT  
		Size: 1.9 MB (1947080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f1583b6e8effb98ce4b38e5aa71246f3f7849c8a8438e75fe964b1e93ad6d`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7f00f5a48b9b4249d216d59daf7211df3b18af80811ae01887340122eefa8e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c71a47d0235e4dc26f3c57266e0e1d4b92587c896fd20699c4040556bae931`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107d59261961bebfec87d95f4e1e558ce8e42798b8d28a75edc34fef7bf4b89c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 3.6 MB (3556246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26154957829f9bf3bb985a70068979a5c42aa97b39becd3512c54b7685a00f`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab8b90a3fe15e463e6f48c57d92b4fcf48bc4fc24903cd114dd8401e1ba8e8`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2435f75ec9c31dcdc86d4ec5a5f303baf23cf77f8a231e7aae021ee70f35b47e`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 100.8 KB (100832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14adb417e445e782b6c6f4c031353ab60033f483e74163ccdfb6602d3234a0e`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:abd941f9bb109976ae0f41cd5e1cce7c1c58d4cdf895851cbcba66a992e1df0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1964038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb75f98268d56b8ee8c7348c7cac0ff27ed25feb5634301eb1500990213c1b`

```dockerfile
```

-	Layers:
	-	`sha256:dc5a9652ff1195ae6074a02db46430f39cd20c384a53e978e8fee9fb923d411a`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 1.9 MB (1948125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8b3e52ef57e9ec95b816881052676acf6b01d9657ea900f954cf1c28c8a5a9`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:27e5d99204405da3882a3bc5af6b5c4ba65c23dc8e9ecf30dcb861db46a1984a
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
$ docker pull neurodebian@sha256:e3bf02662763b1d5eed34c1a4c1b8e3dce143794cabdca3c4be8d0c5dedba8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9633672d57a08f62cdbd025d79d06e31a9915fee95a82cd7fb7f32e772f5e3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e0953de06e1b01ff7d2055b9f20a3ba20a1b7c1b748c5529b5f072d20d5952`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 11.3 MB (11266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832603be935a7fa29c32943f55bb20bace3e68a72ea55d378d207ec681cfb62f`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffa9bb75d9bfce162acaee83c0a0c73659d5290224c0ce3c945a841f43c68b`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509d4b428934a9fbd54daa8f6a05ab55ccf6275ffcb89ff275bf65ad5d986886`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 92.8 KB (92820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677717d1fae198d1b12a8ad6dc403da87dc3837cac5902e3759b7650eac3a07f`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:05990838518fbc3b56779b4bd1c310b7a4ae5b704c480343c6da477fe6882894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f3904f777bef580a9c2b202de145686a8d49391d8146d08bc7a3c60d4df54`

```dockerfile
```

-	Layers:
	-	`sha256:56b145c5026738fafa379d7efd9615cbee2a070dc428efbc19ba0dbfcc4eeae4`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 3.9 MB (3901314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb50d3266d3f97f7c3f6c15944c6604256404fd2942bbeb309286e4dda2871df`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8e94f874f91854196e6076d6b2257915da8829a2dbb0c69fc71c69daf1b8ee7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fb5732480a63ed944bfc38838f7166af4d048cbc08d2e568a1b23dbacdaacf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7927b2dcee59c324d2565fb954b8c435214f8fdeb6bea60c0852e4d9c1689b0`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28aec732af5c3c764498d4ea15c9e9a9cfb30997ac2e931477765f8163e09fa`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f03c91194fd4cd000dc5b677f57a4961e7bc5ff7d6c8815b8f729aa564467`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc847eb0d1afe5aebbfbb461b0caae9339fed614b6c35baac60aba3f7208c`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 93.1 KB (93075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510daac82ff29d856863532c2947e9b7b4b8412958014b7e27b1021ea231433`  
		Last Modified: Tue, 02 Jul 2024 16:01:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8021e1296bb25306964451cdb5141166c468b34ae37368033bb8f1d65aed8ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5e58c1860b53852a190f8de888e8ee2d107ed81b36e6b278e6169323e6f620`

```dockerfile
```

-	Layers:
	-	`sha256:c5dfdeb03102caf3591bb716ffd684f322a5eea6d9de32d2b05adbe0f0760d99`  
		Last Modified: Tue, 02 Jul 2024 16:01:26 GMT  
		Size: 3.9 MB (3901567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb6da297076341b367ffa715a3be15c6b200ac589dfdbb604dcfb9da878c451`  
		Last Modified: Tue, 02 Jul 2024 16:01:25 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:efb49c63259515523fe8ccd10d2e69cccc919b28b7d019e9ec01ea54dcdf06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11abf557d49f8f62cb12bb0f00abbe6d2f11a5c5cdd67090adce1925c9de4da4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cf0ac242a3e8035e29b47f122d86973244dee2f1be303a17ff4b0938c482d5`  
		Last Modified: Tue, 02 Jul 2024 03:20:03 GMT  
		Size: 11.7 MB (11688947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4332763d9633e70311cf57bf761078910fc849e2a62e3e4ddff60d9b01c7009`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7a762c898e69a0d9a80b3d2b2a66524cf758c0814f0b0f1d26a28eb5e5103a`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764619c52a862d5c56b2e868e4f339f49c9456df8469c5f8e9f21f6ff7594e7`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 92.9 KB (92908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da9e058b6819c454d94409d52846b774b660804f0e4d95cb2370d94a3f56ee`  
		Last Modified: Tue, 02 Jul 2024 03:20:03 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b9fc7157c7288d7c94e2b56229184ddf05d77f7e6ac1a03a3e6e755e66805e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a603113a72528b543d99a038c8ae5cf497833a1667db080ece5b7db83a9d1`

```dockerfile
```

-	Layers:
	-	`sha256:f8cfbc339e6496e89b256cd214b6f00cb1703ffc7269a8d5064a68da0dfe20f2`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 3.9 MB (3899231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a0024b48cc8c7bca0377f145743883b2cce1a49c5c8b64afb30495c6131988`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:ef536e667e844bef3f025a24f5383edb3acd8ba268e8ecec5d368a914330ea3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:fed4e2b3530c645d3e7f84cab37eae2b044203d0a63b5041fada474651435759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1f6f5d21c24fbd989fcb96724344eda0066e3348dcf06c8929fa5d5c6f83de`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c8a6a2c7c323b5f83d47d65d0855b9448b50e6b97cbef4bd5d73232f349fd`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 6.2 MB (6223751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490f9f972c2ac209587470895132421e429c467f7d29addd4040a25acb56cbfd`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07cd42cb9adf3ecf8f614512a7b6cae459af25dc79dc86de006f68132e9d45e`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb907ad1f19de4a554a7f21be16f71a92e5ce86f2ac6af4a9c84221b0b9479b`  
		Last Modified: Tue, 02 Jul 2024 03:20:01 GMT  
		Size: 90.0 KB (89951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:27b9f3644c9b309aa1a705e3d1fecc58292e8df3308051d0607aca64a23f0aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef885fe31425b485ef042622ab50eccae8d5e447adf219ea5996c50e1633d194`

```dockerfile
```

-	Layers:
	-	`sha256:f97fb27a9a48fc37dbb30f628f954e9883c25fb07c0f8413ceb17e10109b8d03`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 3.5 MB (3542968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ab7593e82d79e46a4371616d56822aa0bab981e2407fa488bd7038da7908d6`  
		Last Modified: Tue, 02 Jul 2024 03:20:00 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:30fbaf2df2d18158454931946210929a898aac9a510b57a3de067dac3f31205d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59200815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ee26eeee82e9d2700b9e8a5ba5cfe2b0099fd78949a1e36b72fd50b835df89`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f682e5d0d35b6507170549e927b44fa72be309150cc766e8c567a6fff21d100`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 6.2 MB (6219470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1116df5d9885f9a9ff682c06a547c1709ba2c34e3e92865cc80ef986d89e795f`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2529b60acd15a8ed1a099809bf5493031c27bd7255a688091ce443bd422685a`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c43a6b60e4e33f946bea9f325fd364d2d5bd69f0848b7f74b24cbf2aa860681`  
		Last Modified: Tue, 02 Jul 2024 16:02:59 GMT  
		Size: 90.6 KB (90605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:310aee846defdfb760eca13b6fce5779b662d709ed3b6591cb5085bbeb1c75dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16c6093800c166d913f3cb72cced10e90a82d1ee69da07dbf4b58c9e05dafe0`

```dockerfile
```

-	Layers:
	-	`sha256:b191342d93b783e3a64d7a2bb642f2d37be02e8def34c8573eb81969a952317a`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 3.5 MB (3544010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e822a6477f51ada4b8a2b0db1d4d77bf3cbb576c54c263535d3d5d8fa2e38f12`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:a56df304eb1c86cff5dabf46e6ff9297bbb03f3ef255d7deaa00e0b8fdaa389c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60168574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6069e9b5bb86c23e89fd8dad23320f538af8540faf82b86dc52737c7034bb9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bae8a7e43bae044e98255a2206755c69c43385deb06ef20aa0b6503fa088d4`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 6.6 MB (6554390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e11be3bb587e64a347d31a346072a1d6e9ece33f4143863392162f16b3cd01`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f71b73e7356e07f5af8d54e2d18b1d85ecc857f950534783ef06835f22b8fa9`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7898530d420217d5444d31552e4c9f5342f0154e6f0d3ccef93978ec07cb807`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 89.8 KB (89812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:206fed867ae47592e453aab638ddf57f46de701b2e8f5d31586f00ae3e2805e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff168378fa483c4103d74c263824022ec0dcc5e2dec2fccd17229f8aedcf50c`

```dockerfile
```

-	Layers:
	-	`sha256:abd0719fa266c6eeddf8f85db3071c406ba6928ed8be544ffe69e049d85993a8`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 3.5 MB (3540064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263c2eec06e1535e540929dfabee362fe03001b2d54429cc4ced846840ab63f3`  
		Last Modified: Tue, 02 Jul 2024 03:19:56 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:dd9da3972660d59d3362b8d0703c737d414e035a8cc655d86e4ba7528be89b27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:171d7790834ff2dace09d75d17fc095f5e0ddb5a64ab2f2c6c20e979b8283e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed02da4e0059860be250a87aa0f646a80a9a97405ef1de79b37b13c9eece8a43`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eeeaf4645947114337f3365b9e426c0269613f7bc3b5a498de5bfa2dc9f7d9`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 6.2 MB (6223730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bf23babadbd7e24e99d5f11987ac80999f65bba9925676b393344e7ee94208`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa10af556b8d2d97b814bc8adf79194667d8c4ce1a5024278442d4737439c5`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986345555fbfc0e18521aea6d42886d0b779a81cfe975e9eafc9ed31256d946`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 89.9 KB (89931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0757077789f6773bec41e3ee672f0542a27c2a763cadb11bcde5a56e46ba8dc1`  
		Last Modified: Tue, 02 Jul 2024 03:20:08 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73c2c384861f8818e86257a5bb7c489fe6c75e81009f7d36a5c4787a097dd6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be47e1f771cae7b74651749d34cb0056ec051866bf7e66c883ba536bab0438d7`

```dockerfile
```

-	Layers:
	-	`sha256:174f706621926c8028ac0797d12d9ea16ffd1a2a33d41ecd5081abc4d2df9679`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 3.5 MB (3543004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04024201415ee292c1e9d968a7e8f25fb4fa99f389a1ab14070d733a890e3448`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1d6ee16b19cca79b92541bb682a4c922cfe787ab167987a257b1cb41c69628da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59201205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61af8fb9eb88cbefe347add336cf5ddfdd03de1bbd8def9760ab1aac9ad011d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f682e5d0d35b6507170549e927b44fa72be309150cc766e8c567a6fff21d100`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 6.2 MB (6219470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1116df5d9885f9a9ff682c06a547c1709ba2c34e3e92865cc80ef986d89e795f`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2529b60acd15a8ed1a099809bf5493031c27bd7255a688091ce443bd422685a`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c43a6b60e4e33f946bea9f325fd364d2d5bd69f0848b7f74b24cbf2aa860681`  
		Last Modified: Tue, 02 Jul 2024 16:02:59 GMT  
		Size: 90.6 KB (90605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a830aa41d3e8d87799e4ca16d1813076416447501bca235a0651831bbeeab350`  
		Last Modified: Tue, 02 Jul 2024 16:03:19 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5aaa618816e5505ab338d006a538bd7aff3a3178b69f16b46b95f6d8f64338c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8b09ec1e0a532999060c6cb93a0d079d1073f63d48db887d7e839eff87c70b`

```dockerfile
```

-	Layers:
	-	`sha256:5c69f38169c1a9102899bbfa7a76dc58e3359ac9e4713d70a2f25ec4a7f28693`  
		Last Modified: Tue, 02 Jul 2024 16:03:19 GMT  
		Size: 3.5 MB (3544046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f627c118c0b71eab6eb5458d2d3a87f5691c5e6abee6be8be9f9c1eb4baf17`  
		Last Modified: Tue, 02 Jul 2024 16:03:18 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ccd33fe92961585e691320103b2d0f3466709f199056da460ca62cbe0d5470ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60169098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca223e31f2027f0bea7325055c5d03f33eb27502dddac3a3b4213eeb1fa81e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2067d5ad59a2a2d20bc80327b6f6ed28714940579539b9812e9e2f3157973cf`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 6.6 MB (6554505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc9e048603bc334e451f2a2ff1b8b689603b80171d863e44bdb12c8bc7a9d70`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5ed2c6d104afdf33dcc4ddf797b004d5933a8c960beb94d44ab97ea188f35d`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86bcc6164bd435f1f582154cd31a155f0749b0bfc6efc6e88c71e43f0a28937`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 89.8 KB (89832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b3440dcc43323d1971173e19bc352048910e85501abb4e5672519b888b9267`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e2c0308d75c24d63b042d64f6d4ff437b38ead191a1a197adc3d3dc0075bae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93a2eb119062ea2accb8a0e28abf2cae2a404016d635e3fea9a1e8d94f10085`

```dockerfile
```

-	Layers:
	-	`sha256:8de0478d7152d9c9a0cb48fdddef7ec88969d9806b1b0e61fd124ecbe855853f`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 3.5 MB (3540100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe08c161cbe93376c006e2d9a437eab0416700e73293e4b0d953bcef3d26d97`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 15.4 KB (15400 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:2701ee11ce003de748a8673f35592364c004c279b29561eeaf53d4dca9bace73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:86020420df0eb881ff092dc6370848df5fba8955c08c492c10c8ec8b85400a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58771613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b298dd02cf312117d40ae917c1da44edf9f73928a9f298d159763c5cfdbad330`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:90c4ad8b280b16131f305780a1f2721616642bd4d5b4a26256c760cd8ae98f27 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ca828e2fa86974a7bad5159e89a3c4f34921c624322a7fa71026f2a3933ab620`  
		Last Modified: Tue, 02 Jul 2024 01:31:45 GMT  
		Size: 52.5 MB (52458214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1022006ddf723b7769e7b09a86c825d0f39c97af210df7b7efa0ec35db3693`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 6.2 MB (6221865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efff9e871ba85c68cf52da4df7d44606485ee55c07e5696869a8736c738c5fb`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f13b507f2f38fd158c457d7a6004ca895e873a2738f2bf86bc2cb4d23f1a178`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59df4d655a842435892b91ada87ed87890c6e1eb78237c0b0fe575b22be0ad6`  
		Last Modified: Tue, 02 Jul 2024 03:19:29 GMT  
		Size: 89.6 KB (89551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2db6d78b5be1750f123569779318372c50ec40177ebf0d492c3bfa2bf843c26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206dc903c6cae6216105a228224595e74dfce8ac34981a81b87429c9732e787b`

```dockerfile
```

-	Layers:
	-	`sha256:af82b7215c2c96f47e852e3f56fca2ceb07957be45d22f7a5c95f3896fe64417`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 3.6 MB (3550053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1108c450e7df3e0e38ce9e9e191c53735ed188725412bbc405098f9d1ebfa2`  
		Last Modified: Tue, 02 Jul 2024 03:19:28 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e2e6c2dad3e9c25d1ea3d8222756995cff380d4b07a735ce302ef9caa7923db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59005218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef771b1f9ab2d09bce49e0798ad3dd93430404bea3abbb996b1ab7fa7dfadf89`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37e4feb9b85ed81a0244ad32abf825fc3dcfa282fa2fbda1b573a8af3f9c66`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 6.2 MB (6219751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe324133caeef138406fb1d02d698bf04ae634950a378224cd67c28c8e16555a`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a395df2ca4da8df74e14bb8e822fddcd4499bf01353553400165ee04f5d153e5`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7299ee038b6c18a9f4e26e561aed03e451b34e861940756db261f8442b57ee`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 90.2 KB (90162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b1ee57b09d3fd6da3028ca30cab64722635764b475ec4a9abd08a7a839c9e99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a272f25b7a111c41cb3956571ce6bbf199816741392cee26c52c7b5887fa9c5`

```dockerfile
```

-	Layers:
	-	`sha256:353bb6b1a72e8745732e2dfd1dfdd3fbaa57e5a15452660ab3c31ce08d8d09d7`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 3.6 MB (3551094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c000a857e95c72571a967d744d0dc0377de066348a21f7435f849c2487c0a994`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:1b979e614b797a8e6b34dad7b4f04b675c9f817d136cae9d1e5cd5c6d2843c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59976885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8097c6780368356f0da76878203ccf56c2f6b468adfe12871c37587473375b59`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773778424cc9dd30f34b0dd99d912fdc8834e380ae80f2e3c094f79b333371eb`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 6.6 MB (6552263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03f370391c3e5d2a2c06f5c4e17ff675a2040a1785b48448847fd13640406d2`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0856b336a87b5b8ccce813aa69b8c8c6107b7ef7b2d1a7514f48079ea8879`  
		Last Modified: Tue, 02 Jul 2024 03:20:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26929505ada2c90ca7c24b4b14e04f9b75d63a1b49697b24ef448a887b7b876`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 89.5 KB (89458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ea8c51894f88b655386564b901f2bede4dda51a89f560f9dfcb72d562b780aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d1651ecf22805116196871bac4fc49400b60e97899802823523e5d88b4f5df`

```dockerfile
```

-	Layers:
	-	`sha256:942435d1b26d9543557c7ad883cb0f7222ff9d38610630a779a694428d5532e3`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 3.5 MB (3547152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54cef61444c589ba1dfabc4da40f457ede60d4586c9b8427e800e242c1bbe689`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:cbc3dd545d9b9b037c2fca20f1793ced8892493eb8ac076dca08a8c033bc4f64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ca2379877bd375136f0bebacc15725191bb411a53cf4085f66157875892ee4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58772271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353f68948093fbaa77025ded231eed6a7e3840a86d3b0e561d6e5044235db7b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:90c4ad8b280b16131f305780a1f2721616642bd4d5b4a26256c760cd8ae98f27 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ca828e2fa86974a7bad5159e89a3c4f34921c624322a7fa71026f2a3933ab620`  
		Last Modified: Tue, 02 Jul 2024 01:31:45 GMT  
		Size: 52.5 MB (52458214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94e3ccf5f5407de3eb05fa25f8e9c631fb1c59095bc2e61399ec9937cba2d3`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 6.2 MB (6222085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55ac663eeae01cec5106afb87e8ed79e49b5c2a7ca82dedd5e9d202d2761c1c`  
		Last Modified: Tue, 02 Jul 2024 03:19:46 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c35d22fc86197f71cf62047c3b9444dedefb03d49949ec9cc27cb11341a8750`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b3b39d2f3f9ebbd735f3955ccf42be6c60fc7c0673cc4d5c8194657c0b132b`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 89.6 KB (89564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830af931f363fe496bb2204c8b062340c0a5d696ce5e499e65abe96c6bb25443`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d1f5a12df29579d00f04b27c04671c9a4b46104c083c3ce51e009255e78c13a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26a3126ea213714cac4c2bf30e583440725b7bb70d9515a469e0e0143f1b868`

```dockerfile
```

-	Layers:
	-	`sha256:da24285cb8b8757dcdb2fb6b31c55cf2448b50fb093ed16348ffa0e5b6883b44`  
		Last Modified: Tue, 02 Jul 2024 03:19:47 GMT  
		Size: 3.6 MB (3550089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b07cc3761be09ffa10b5dee6bfcb6afd6e6e5f2f6dacc8fd9d99879fd96290f`  
		Last Modified: Tue, 02 Jul 2024 03:19:46 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a79974208a0bb820954693531a9afb3afd106a32f2b757f3fc20227f0f4a0b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59005641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8c8eab87323d42fe26497f851c17fa6e0e5385d3882919e0dc57df605527ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37e4feb9b85ed81a0244ad32abf825fc3dcfa282fa2fbda1b573a8af3f9c66`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 6.2 MB (6219751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe324133caeef138406fb1d02d698bf04ae634950a378224cd67c28c8e16555a`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a395df2ca4da8df74e14bb8e822fddcd4499bf01353553400165ee04f5d153e5`  
		Last Modified: Tue, 02 Jul 2024 16:02:02 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7299ee038b6c18a9f4e26e561aed03e451b34e861940756db261f8442b57ee`  
		Last Modified: Tue, 02 Jul 2024 16:02:03 GMT  
		Size: 90.2 KB (90162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625e1ac3eae348163608b8585ba920626955440fe37f93e4d93ab97263de9118`  
		Last Modified: Tue, 02 Jul 2024 16:02:23 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e527ddb0e1c047facbe36e81204aae3cc538ed471e53e8cab806a22a6496f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44b20d48b8f68b1ab824177e21ae99b3a33f7070334edc4792d84a8cddd18f2`

```dockerfile
```

-	Layers:
	-	`sha256:3d2ab6e217ea6aebb7cb09a460fa739fa8e0af067bf6e31f73cd39f4ad9cea5d`  
		Last Modified: Tue, 02 Jul 2024 16:02:23 GMT  
		Size: 3.6 MB (3551130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a02f309059e7f55a807d43e326cc66a962c7f61273ded799a07347e31fa6cf1`  
		Last Modified: Tue, 02 Jul 2024 16:02:22 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6678b0abf7ce15b47e9fe6e10f34a869f8df78e0c6aa931ed483357ab28e3bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59977316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7f82e6b423e8ce366a692e0015506898918b77bcc79651abc0721a23d1cefb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572de5816e1dcea6e5d7bf1248df78c0a435de0efeef834dd9d0c38567570bd7`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 6.6 MB (6552258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a80c2c6d79e7c89ef04c1b1df81970b923505bad19e787301b1c53ed276e9e`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c830fb8727b7cc750190f85d23fc464ae943a3599eed6b6539911056e7eea3`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d978e8ef47f777662225ca0ad77f6faf928a037988e9242a9558de8a2829d531`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 89.5 KB (89475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bd4c6b10e884e1886dc9dc50e79503ccbac9653d743d726e5c1292b521da11`  
		Last Modified: Tue, 02 Jul 2024 03:19:38 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:baeca2bd03a0194349bb44d0c311e1c6839f71fce257a6506bae904211aa7d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139e65b3a6189c99551bdf06fe0eb9a714c3c155ddcfb056e712b7011a72c9da`

```dockerfile
```

-	Layers:
	-	`sha256:ef6bdde65a79dcbbe926e238d768dce9b781bcabc19642a5647491d0d72a4332`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 3.5 MB (3547188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddb7644a264eff676c63c86ff6cea3f2e367692140d6e6493d4c3ead6803f4c`  
		Last Modified: Tue, 02 Jul 2024 03:19:37 GMT  
		Size: 15.4 KB (15449 bytes)  
		MIME: application/vnd.in-toto+json
