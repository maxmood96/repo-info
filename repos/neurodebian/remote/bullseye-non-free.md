## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:852dea1d4002e43ae9d02ff5479ac320ee7af4774a6741c0905f5398d5023563
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
$ docker pull neurodebian@sha256:f026b68077b6f84a5f70a0db932046da05fc477b31afcd89b1e8768abbd8d44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb385ccca0c03c43e7b3c7f118f190067730298e8a5e19179ff774b507948e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9b1b5ada493789ac11ad992c547dc827bb57c7d3c2dfb205234aced9e75574`  
		Last Modified: Tue, 24 Dec 2024 22:29:06 GMT  
		Size: 11.1 MB (11105074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae2a398b323252c586599597dede20c9ace8fe379ed976241bd7b1b64e20fb`  
		Last Modified: Tue, 24 Dec 2024 22:29:05 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6424e356e1cedff118f02e0b63c3d648bf741a8f6f607e4d412c8c9268aa35b`  
		Last Modified: Tue, 24 Dec 2024 22:29:05 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2142e81fd44e109e4f3ef3072fd367a0c3b379f095a22c25860ac3bf431af7e6`  
		Last Modified: Tue, 24 Dec 2024 22:29:05 GMT  
		Size: 101.2 KB (101214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e2dfb09737221149dfcda587b66c35eb800a3c5c1f5dbaeb3df27119b073f7`  
		Last Modified: Tue, 24 Dec 2024 22:29:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e20de31d195d8f799417bc6cfecb296e11ead7bff8aba991a7564e07e6e1641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215d958958bb11b52bdfa845899239b4c42f6925fd61079dfef83a8d27fc29c`

```dockerfile
```

-	Layers:
	-	`sha256:7ff80167c4726c3126cdd5d3e9e89a16d517e8529b902f24f33a267c5ab46aaa`  
		Last Modified: Tue, 24 Dec 2024 22:29:05 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf070b4b5fa85c079041a14201b843f16f3e98d1f828bf160412c4a8c2e112f`  
		Last Modified: Tue, 24 Dec 2024 22:29:05 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:535963c32fcf93d0b7e6b596c82ad6961c27b36a7e41ff685482c464957d071f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362a4108e7a83cedf833a545ff08b6207e7ba08b6a3a0812d115741b25ec5c3b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3fd91d26138d9aaab80f425987de57628c24f81aca2727bcbbe870f7dd5c3a`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 11.1 MB (11105941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d41e172cd8c296857603d6eec38de1b1fcad65483cb5e3a5c165772ebbc188`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583285aa42d4ba42549ac2e4ea57d0849fc285d04fffe2155b702638dfda9ade`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2a8e49cbdd987bb7224891093e38a2baa58d5a5b27980b70b0c710e3e4f973`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 101.1 KB (101090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b911fff051384026d3a1ce7b93df92d04591d621e7a848ece543384bb43066a`  
		Last Modified: Wed, 25 Dec 2024 02:19:15 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:35f38aead4bfd0e832e06598f24f6017efb0e74754e494b9991587ded171bfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6843c473007509fab0df0a75cfef7c88886f907a7d220eb6eb6f9822e16a0c8`

```dockerfile
```

-	Layers:
	-	`sha256:0c3a437b2e81c9a759dc43a0fc0f0e1afa5ff8144b82fb661cb368f505d8edfd`  
		Last Modified: Wed, 25 Dec 2024 02:19:16 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5539bdd889e22e995e7c9aef5cc6581e5a103abc9a7919ac5176c493a543ae`  
		Last Modified: Wed, 25 Dec 2024 02:19:15 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d10c0b4884d2604ac5715286c9c86dda76b4a10da8581b6c2373abaea18ce2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105c929bec7b370b1bc4e83f152d1ff5f7c582f1dd08d4c3cb8a4bbe7a719b6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
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
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09eb6ab9cf21ae3899c220eecf18d28e644105fa7d7df46eb35ab9f69bf0513`  
		Last Modified: Tue, 24 Dec 2024 22:15:22 GMT  
		Size: 11.5 MB (11500240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbce1877f01872eca560a8eb40fbc4fdbb59e1708ce9ca25f1026ecc01727f8a`  
		Last Modified: Tue, 24 Dec 2024 22:15:22 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da97ec30e62f056a8ccd5aaf20b10a0f4b36f01bca1cafa52a7702de05ee97c`  
		Last Modified: Tue, 24 Dec 2024 22:15:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775a7a50b8c1b1f23baa3a794a3df6acca8177f16d166c05a48c58470613b6b4`  
		Last Modified: Tue, 24 Dec 2024 22:15:22 GMT  
		Size: 101.1 KB (101070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaf2b11a0e0d17a3a4b7df122c1a10264e28e4f3a08391297da0e36dc7b6182`  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:506cca5f967fb3fba711b97aa425f426efb3e861415d5c30b533fe98d32d2a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47d76687ffd7fad2b091aac1aee15874c6713a4a1b77ad19cfc0a2959b43ef4`

```dockerfile
```

-	Layers:
	-	`sha256:0d02cb9ac366c6794f1c91155e0aceb697f5cf481cf004b1ba27a8ead7565c2c`  
		Last Modified: Tue, 07 Jan 2025 23:51:18 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3d3c93a45aa2a165ceda8b0bb38cbc093e5f8aeb4b48aba78139889529b6f2`  
		Last Modified: Tue, 24 Dec 2024 22:15:22 GMT  
		Size: 15.7 KB (15691 bytes)  
		MIME: application/vnd.in-toto+json
