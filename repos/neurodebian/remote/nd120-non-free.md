## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:679da61d70db97a96f63d8c2b79d5f606aa70634346e133d14f7c46f447572e0
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
$ docker pull neurodebian@sha256:e89cb8491347c3793299b4609dc9f486e374e7e6b3871024cdaa52a242e8f889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea60233cd27143f98be7c617d34a2b7abccc6ff2aabcc29751782a270e795b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c45697feb00d0b63cd7fac2b980d8cb335c36bdc7ec19133c10ac21ea5e36fd`  
		Last Modified: Tue, 03 Feb 2026 02:48:58 GMT  
		Size: 11.3 MB (11273436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bba6c203b9ebf4afc38346aebc78ede9b2b21c6744a3a63f7fd29c95bbec92`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71877ab4d7a4f26899206a9f324de43293a354660fed1fd6bbc7313294974b4`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4479e797285f1f997594e3d4cf6214b8c6d464e7fafd77f8344aa65ae6180541`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 93.4 KB (93380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769627860e6b9788b55ff0f269633177f23ea77468d5f7e497b9b2a68e432c98`  
		Last Modified: Tue, 03 Feb 2026 02:48:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1aca7321e3f7be0a4a173952cd6e7d2f376d911b90eda28aed731f8858aa437a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5604db43735de04e2a0de391c3b42da87fa2823aa41080a13383d7db4ed34d7`

```dockerfile
```

-	Layers:
	-	`sha256:e014afc086f73ae28b94d4c5f55d120bf2c935b26fe4bfc6e4841a31381aeba3`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c58749e130661407c54b4f05e54b5e92070583915549b6dca5ee525921770f`  
		Last Modified: Tue, 03 Feb 2026 02:48:57 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f508fc569e9354103387cfcae965f96292ea8166c08fe93ed247bea719d39d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59715235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0062a10a83631d76fe541922a9ef608758f85d6ee77708c9a16924a2bd7e6b12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:35:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:35:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:35:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38115972cad477668bb850efc7c7ea6bfa4de7a2ac1e0f1018db51dfd95d9547`  
		Last Modified: Tue, 13 Jan 2026 02:35:16 GMT  
		Size: 11.3 MB (11252970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc14296655ddc474ca26d2749aca378c7c586988a59f9b7f87ae1e4c40a72538`  
		Last Modified: Tue, 13 Jan 2026 02:35:15 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b837d0d39f23fd8a5c5a1a72fb724de3fcb1eb99d3d209640d35949af0c564b2`  
		Last Modified: Tue, 13 Jan 2026 02:35:15 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3f790172ae50ed6b0d44cc64b97b6a4fd9ba186196dbce42bd5320f3432acd`  
		Last Modified: Tue, 13 Jan 2026 02:35:16 GMT  
		Size: 93.6 KB (93570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a291f115b418c28f66a9c6b7cc4094d759456e06301c7e417f249248d0b983`  
		Last Modified: Tue, 13 Jan 2026 02:35:16 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1d1e297bbc635e1c8ee1f84844827a692b1b41876641a231abe3b0e6c0030632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f96c4064af2337a4be93a3184c3aad06cc7e32518e9a2aa3690cf1cb5d613bc`

```dockerfile
```

-	Layers:
	-	`sha256:b1b0e53ce0e61f6f2fc32483eed6e1e0712259514181acc9b81a37ec762b08f6`  
		Last Modified: Tue, 13 Jan 2026 02:35:16 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ceab790878277f24c39bdb6887b7894b1836783e8bde9c2ef40ab4f7ae6a69`  
		Last Modified: Tue, 13 Jan 2026 02:35:15 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:67609dfabc9d67612c0a687ab32d3efc7642bf84bd38e368de7d697dab85a8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61257523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0279d1f771f4cb6863afc6fe0f714f786a52ed1f95c7b64ea570ec523bdeca1a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:09:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:09:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:09:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:09:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:09:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:41:57 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997c347d332a2c61c0fc360ad6eb7c79572de56f76687ff994021f55d5be5509`  
		Last Modified: Tue, 13 Jan 2026 02:10:06 GMT  
		Size: 11.7 MB (11692891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c32144be38bc3cdd35d34b179a53b857bd09030521b64e3b2ade8cfbe04682`  
		Last Modified: Tue, 13 Jan 2026 02:10:06 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b31d31d15813b4a718555d1d4e2460f1942473a1f45559c81acc8d3fa2e639`  
		Last Modified: Tue, 13 Jan 2026 02:10:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941714f5865663330ec0e001ad63079040334233d7b79e405bbcaa371ebdfc91`  
		Last Modified: Tue, 13 Jan 2026 02:10:05 GMT  
		Size: 93.4 KB (93411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83358d0a123b83f0bb86b0baa7411a9619ac366e0c8d8a761413fb6d2c44bb3`  
		Last Modified: Tue, 13 Jan 2026 02:10:07 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4247a7ea062c8b065187ce9d6f1d1eca09e1729d7ebf6eca88e1d9d3bc89a93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4032828511bde0fc105b8f486b7e39b0f33856ff273bc05683ee8fd3389dc12c`

```dockerfile
```

-	Layers:
	-	`sha256:7fe512b129d9da47649d446b267236f1dc7ca6f6c12d88985ad37acb18fde41c`  
		Last Modified: Tue, 13 Jan 2026 02:10:06 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd72de5be76ee258fd7bc91d339ad00dd77909b399889485157419880d2263b6`  
		Last Modified: Tue, 13 Jan 2026 02:10:05 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
