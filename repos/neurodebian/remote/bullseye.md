## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:21fc4e3c0cdf3d86d9153cba80384427527bfc2b483eeadd1e318ad6b34a81e5
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
$ docker pull neurodebian@sha256:4ecd9d1443e75181863e1b0a0427e8661fe92478615af709b630787153110c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03739d2be3885eea98c095c9c74a10e89108d70ea5b2d847b8bd4eff7a14a21`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:48:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5012d8636e02354fc754917a5033735462dd0859681a109ccc1d487ff5a0cbf`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 11.1 MB (11103507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958c347c1e407c069a4d2260fef1c8c469021a6e69859e324c4cc80a7ec71c79`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35c37d32450eca29c1869c861c8b6211f487e8459cb481d58bb785e689ccb2c`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59abc559ead350f7d45163c15a158239544ac872d73e287e28c62ec5d8d18573`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 101.5 KB (101459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:280100744d6de918a33f4507f434ad023c0711e4c6788351c5d3f00bb1fd15ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d5313ade697365c5833199af043d3c89e529d7424c8c2b152a0eebacb9eba8`

```dockerfile
```

-	Layers:
	-	`sha256:f1be9831e14fae35c899ab4f09a3310194c3a382bf28babcc9d58c730aced7a8`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ef553d164e1c42152cdab3a581c5a74ff6db0a28b1ed04399d3942e993e238`  
		Last Modified: Tue, 03 Feb 2026 02:48:41 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e4fd4b91cf6c647a708ace2299e986dc7ef6a91abb9d0a695b49b5a3f6cc738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e2e3ae2d52273247d84a145b8171c798a4f656f57f5c331d8bd618ed319110`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:33:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:33:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aab6a48aa93fb550f85c58ec26fc734421ede11574db26fe436f175d93a0ea2`  
		Last Modified: Tue, 13 Jan 2026 02:34:07 GMT  
		Size: 11.1 MB (11106068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e622165253aa4485269eef44e2cb409ad7f56c764352556e3867dcacf482d58`  
		Last Modified: Tue, 13 Jan 2026 02:34:06 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225fa2f91d12c286ee5049bcbe7503d76f6e1e7a49f8de853f55e92591550820`  
		Last Modified: Tue, 13 Jan 2026 02:34:06 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e5c12b682c631aed701dddac390de29596adf806c67edb4e6de8407aa3da66`  
		Last Modified: Tue, 13 Jan 2026 02:34:06 GMT  
		Size: 101.2 KB (101155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84d2b679fa2746129a39265e396826473cadf450533f37b0acc0c355655118e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1153ad8fc29d63a44673a778b5bd50bf49a62ae7c1ab6a44b7c125cbc9f9e532`

```dockerfile
```

-	Layers:
	-	`sha256:a3c9414a1efbe89640c08b0c1d558f51f1ce66935c259528de3494e6f17bb1d7`  
		Last Modified: Tue, 13 Jan 2026 02:34:06 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3faf9a02df783ce6a996ce711cea34004a4b5df6d6d944b25bd687f343a14327`  
		Last Modified: Tue, 13 Jan 2026 02:34:06 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:d7cb5a8fbbc3ea8e1194fcaf45cc7badfa3f0730ccd35325f197755cbc8954a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85d52f2b7022665b1d1a46274758515c4d183714f820014b22bea5269d404cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:07:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:07:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:07:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:07:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:26 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a4c7bbafeb19af44510a1c9ed09d1288e2b00066cf2400abbd52d8496f6973`  
		Last Modified: Tue, 13 Jan 2026 02:07:49 GMT  
		Size: 11.5 MB (11500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7969a91c7123c203a0161617f5ac9585f0cc1ac362c1ed2a5bf0352d26115c86`  
		Last Modified: Tue, 13 Jan 2026 02:07:48 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfffec129beccaf3232b2d81f28a8e34d4c30d953b665d5e2bc28e6567c5594`  
		Last Modified: Tue, 13 Jan 2026 02:07:48 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2979f85947831b281e65e892bb0d5f328429eab554aeb7e707ec9b89e68e82ab`  
		Last Modified: Tue, 13 Jan 2026 02:07:48 GMT  
		Size: 101.3 KB (101275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:494af68cb9f2a4a9930390c1380267acb858737bbf9c4597141f588bf022a01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe1ee7ed76b5ceb9e943e6aa3290edc6258aed2b09895c8276fdbb08737870d`

```dockerfile
```

-	Layers:
	-	`sha256:f9484de5b95c33464b0dcd885aca443208dd39bdfe3326356f0201537391bd67`  
		Last Modified: Tue, 13 Jan 2026 02:07:48 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed007e1dfa4dbba980b0fdb57d1753b165042c471883300a8335a420b0902907`  
		Last Modified: Tue, 13 Jan 2026 02:07:48 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json
