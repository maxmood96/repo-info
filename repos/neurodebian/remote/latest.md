## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:e9a1fd26ea2baff00c1315608d739c61853882083e444ea056930ee89db09a2e
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
$ docker pull neurodebian@sha256:a9b6ea77fc0c2872c8c6c20d689263303c20c4bd67e1dbeda241260fff5ab67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60940562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6bcee8a2fc0e2a82690e94659d173b473d9bf8a092bad37e332016906695a0`
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

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:19c680d220366fa55bf59bc66fa95445868cb4e484ee050519dfeda38edcdb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036954c427e142a48e7593108d9b4b422ec7db72eb43421d9d568e58c68fabcd`

```dockerfile
```

-	Layers:
	-	`sha256:86ec47576f0a637284f28fe8f6f229eda89e3e133a8f9ad66a28b9fa7673a726`  
		Last Modified: Thu, 13 Jun 2024 19:37:02 GMT  
		Size: 3.9 MB (3901984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de38e2c23965eb130ce4a11586f826f4fc7dbdb97894fbd213b52ab144e35a10`  
		Last Modified: Thu, 13 Jun 2024 19:37:02 GMT  
		Size: 13.8 KB (13757 bytes)  
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
