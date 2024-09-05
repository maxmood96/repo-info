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
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
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
$ docker pull neurodebian@sha256:86bf16ea341131b94834b82b1fad1be2a4e2c758bdebf6269fb81005493e1440
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
$ docker pull neurodebian@sha256:baca0af0e600d4eb5673968b51b81e3c01dfbd4afc281940ff7d7c6d78ed741e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60918412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f5f8734b677aa4409e1fdaeb2596287562419a627a2047c28b218798897870`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8553aac5ada3d57fa02485752729b218183e391f256b8f556021e4da979429`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 11.3 MB (11266596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0920907450c5815ca556bc9418b43897f0a1b433d9c94fbc6a8f34fc477cf`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bfc646f22c7d6b23dfd43f1fd9e959530e4cdd2d7cc1466d873115d272717e`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000c71c1b18acc1de1ce7d26b6d2e3b79868d9d487afef3e6c1fdba6610178a`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 93.1 KB (93124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b8934708ecf6bbb786c047f9cbd663c371f1bc651676f2255113e3098c85c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c8695a09f10ad91087d1b0ee82aba1f221b3092ada8d8c9f9448a07dcb75e2`

```dockerfile
```

-	Layers:
	-	`sha256:c4d3094a41db65375f15c2e76db9bc8bc482af824a6a9a64abb0222a0ba0ce98`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4124a58a47fb482e249defb5e353787cf657769d362036433e95e912192179ca`  
		Last Modified: Wed, 04 Sep 2024 23:10:40 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a1cb3b5b67cf0e33740eab0262c450d59e72b86b395d24c8d3a9f168a289b6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffdbe3d5fa71ad63f7f9ce991223af396c40a9156a0e8c62e855b7bcf88d251`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
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
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6516de16487e13fd76db87360111809c44b836a1dd673fa8de93b983583728c`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 11.2 MB (11232114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6108c7a663d245cb0932ddfae87f92ca3e1de7fecebcc1c63ff8508adf4e6db8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08a498a3c3c4bf8a5ccf542b868e62921588d0f25c6cc09bac0d6a005711aa2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e20e8cb909fb4d46a63b2053a3a0c458af529d893341a678b2c4b75796cb9b2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cb795a0975baf1f75ee1ce62b377c40aac3dde2c15d9e5c6b8970685714a2510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0fba90f7da7dcd6b439e7ba720e8ab181de5d8193ac16bd8c915f30d4e63f2`

```dockerfile
```

-	Layers:
	-	`sha256:f48d7ad43d43e6852e3cd4b617ff75b9f95e9ec8c998d37041fe7d0e955140a6`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb0c8dfdbaf13211fbc6bbf2d1f5e6a0992ef2ef16cb8a437b676e1d54898c8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 14.1 KB (14076 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:d91ae7a8e8e0a9cd1ffb1fdb782e80cfd9da956bc72f78806584839aec880e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb593a6077e15e3e59d1eeb6e935ed129fded0fb46fe5d39199cd3652ccb7d7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
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
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a474c2633397aa8306d1b46ed39eb7746779e75412486f5a38cf877780594f5`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 11.7 MB (11688978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54facb93fbe5b8f9909d31756bba5f2ded7ec557a297888397bb38450bc1eb8f`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fce3b83199534f3d75365cc5b58bc55d368f2ec44856cc75b30160bdd1d8`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5f31329f83d69533edc23d6eeae9ff2fb069d68a6cce9838698cd524b8c568`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8897ff5043a7750fd4373550d72fc68d1b6d3d82d162871168d1f00796c311f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbe09b244eb3ae159769ad770a0dafc5091e558adfebaa8d5fb67510a9d6014`

```dockerfile
```

-	Layers:
	-	`sha256:fc84cae9d8bf21b3eb9bd59bdc787ae4b071c0b38d8be46234d7420219476b7e`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2e799e06efa1c383ee2a950c88b8103826599d4c0e5fb804093db0855c2bcd`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:92b6eb86e62a3a40e533bddba7e6ba36aed887e0ac522a884548625d92be5637
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
$ docker pull neurodebian@sha256:847fa5b5f7cf1bccaca954bf29c9760f6e50b0d341c1fc9922e71b16a107dcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60918838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d8b68cc7b03f4463b38a4b84766e653af6f629425f8dc9da21a01905f86c41`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cff9496b0f02716173380ea8121b9e078fc273f6d7523b800d9fe735b5dd1b`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 11.3 MB (11266595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5983ad1294ee53f6d8da2393360eac5f051d3bc0b588717c0d4cd3e142217c`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf285c1642ebca0cc13aac597170ef3a5c579a105f0f92629069f4832450ad61`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed44b93503e6a3d93bdb96a16f03e2b54bd73a19da0bab6380ba0ea3510e5cd8`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 93.1 KB (93123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fac7a70a3b2ea3f16e625c5ce0fedc502786c081db5610946a45da1b8ab44c2`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e24effabf132ff5cdc935ff05cd29e117b0bf3205036161440b7bbed70d99ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52f163fc775a474972895d85969b53cfac0fff58bcd49825409af99d1bef98b`

```dockerfile
```

-	Layers:
	-	`sha256:398cb201c6629b1fc0c304b57e8d35385ba361d53e29d7c558217a80617152e3`  
		Last Modified: Wed, 04 Sep 2024 23:10:44 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223b164f125eb0ef2acf8dfaff4c3934e24cfec268650cb9bef3c76614f46ab9`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:761fa3220c10853beea131741907ee20e70ec4521ac8bb053ed3102cc2c2f107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c6a24608f1cf51881701b2548227ae1a0c126c6ad59c7c32ae3e326410aa0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
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
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6516de16487e13fd76db87360111809c44b836a1dd673fa8de93b983583728c`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 11.2 MB (11232114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6108c7a663d245cb0932ddfae87f92ca3e1de7fecebcc1c63ff8508adf4e6db8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08a498a3c3c4bf8a5ccf542b868e62921588d0f25c6cc09bac0d6a005711aa2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e20e8cb909fb4d46a63b2053a3a0c458af529d893341a678b2c4b75796cb9b2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce457b9d5bc4664f2ee4fea10d635db111976ec6879c1d1b65c5f2583dbe5583`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:faf07f81a060067adb199891ec5a55de7b6b552d9e1425f1af3d811264f4ad67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b630765608bbb9375212b2673d9d41627e2f3fdad5f8105e334bc40f372814b6`

```dockerfile
```

-	Layers:
	-	`sha256:b5b0a3582701ba2dfcab416b724d504cf731b6eba018c782d7f8f980f48d5880`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2796e687428634d360ff415826bf00c056a4a1fd7916d81eca260088e413ab5a`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6dda59b69a60752417dc53a7da8941269d242b1e51024eefe430dc3c8678535b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62364011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6544912638a3d685fb71af9ef012ae48702e550f4eacecadc34616be26b1ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
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
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96a775276b452d08188a5c8cefb2671c2351befe343f1b71ec2831ff494f794`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 11.7 MB (11688976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cba750c7d48374c4a665b3aa6dbc0d35907c8f5351297534109e7710fb5c1f`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f40691f5b23aab625dedc59cb84165c3346c956f411c37faab61829e98875`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f559b7b520cf1d9f632d590f4a76abef8d20d19ee766429dd08dfd1c710e99d`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3984a8ad3a3a24cb4c87f0a2b5e7d680ee45cfce31b1e5cd4e4f20f1155943c`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ef44f9fdf0ade8b16b042df566cce5c0d994e196038e8dc7afac19802fe5532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132b918c3187bacdd483261bb47116c101b17645636f69910a6307417710fc41`

```dockerfile
```

-	Layers:
	-	`sha256:46ddedcbc2ee5bb19f1be63bafb03eb6792a0d36311f43bdc4abca7f7d714bba`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b55d3c3b9f45b61d2f39e46bd54d2650bf8f8a7462f64277466dd89f98889a4`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:623f88f24b9ae0b8a922939a2b76e884e1e60ddeacd3c078ba3498eab2362b53
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
$ docker pull neurodebian@sha256:ef96f4ffd60228e64dd4357acf6bb4f1f7d1a683e563095ae5497bdfb12ab6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604cb8f24240d11a65cdc5cc10ba42ad769af0fdbc4687d40c0842c04b1cfc87`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
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
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8229cd5767c1fe3ccf97dc241f9775c959e3a2f3ff08b32d367d68ed890c2463`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 11.1 MB (11104998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a8f94d7e2ff63aff6b5aa019f3edfa8b21cb30905458ccc1bd9dbbdde9f7fd`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76998563fe66245924cbad91c3a4e926d33b00a1b07a82beee9a57b4ad2c0451`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704c0a9181147f709d4f6496cdf26505b3048b62468a58abd66402203892757d`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 101.2 KB (101189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb7fb9c8cae32f8ae1fc059f4f408e429acb616fd20bace226275bd99a48f2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df983365605673ccef6006f76ec41783d05efdad0b4a23227064d28cf8c142a5`

```dockerfile
```

-	Layers:
	-	`sha256:f6e9e0a46a41eaeb5600fb3f15855752c1f5c7e9fbe5cdd3e0fbff0ea3eed8f3`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 4.2 MB (4223704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93094f619548a5cd2b8be5a544aebb5e90632b2ac494ac5cd9ab290fe2cd5dfb`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:aeff8d220de591bb51be66b1509ac7ddba972d21b8ba2722877b78b494200cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64938906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d8f04d5762a59bac48f71e1dd82a7d959c727dcb13fd712b1df8d452ad673`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c1837712cd740a7b87a314d41272c401ded8ce6df66684b504dd48894e92b`  
		Last Modified: Tue, 13 Aug 2024 07:39:38 GMT  
		Size: 11.1 MB (11105879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300cf65bc9beca57bc7882230779a6aa040b842f40c72404d5c06e5dadf718f7`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3d9476d60842d9d913502642dcba44aa76828cfb14cbaecfb739e21aa465a0`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb0f25f8fac8aa2b0b2671c3c902f209d41aa33455bb202bf968ebef99f92d`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4be26975a18f80aaabd7590cd69e0f346907cd5fcafe423ceaf798289704efea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2787943a12315c16c2baf17c53051758e4ca1973bdfc16f70971e55f09b97f`

```dockerfile
```

-	Layers:
	-	`sha256:728dadeef62652439001ed5cabf16e60c4d4bf704479452e7732bc9c0e12f289`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 4.2 MB (4223309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccbf9ee9c6d729099509d11ee7884bf64e5a1aca2a4ede7c21b4f44ba19e7ca5`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:d6442aaf411f6b7317fb029bdab3b397873436e024cdd67f8aef85e2e6b04f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab815b1d7bdb4ccefbe5ccd5f6d4a166c3499b8539f5103f349cd796af54a47`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
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
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fb4eb6f62cdeba31e6d69cfb84d444cf628b43ce8002eb68b122365e12ba40`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 11.5 MB (11500076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d529280f6a6a918ad676a325f6c19b0ca78d98839c022497e74193579fc99634`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bbbf843f82657df2505db1accc5e4028926b7a5ba7e2617955928e74594645`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8f6c624c0ea5365eac6c105ff32abf1ace893ef3564c444c7acbe11a1c5adb`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 101.0 KB (101035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:154e3e036b4ace281d2534c1865c6df071c7f2f55a763557ee0164c988bc95c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5e1b29d6f8687b416c2b88ecd885495ed77390e347b54b2697a2c867480ab4`

```dockerfile
```

-	Layers:
	-	`sha256:95cd5a6b87e46d9955ec52378adf03f93125f5c49562a3453041f5c5804f389d`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 4.2 MB (4220164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2268d0e3d6467811593dde30efe7a163fc6128557e98221180fb0d524126af63`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:6d2974fe43af719acd5fe2f15ed2b7ea3cefc0e1a0fadc31ccbb1fafd1ae2b7d
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
$ docker pull neurodebian@sha256:37742f33147749a7cf8493b1c57e513137caf3a39237ff5fd69d05e9741843d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198e3b59f16736e7d1b4a215fb775f60a8db597df22072c3d4e56b031dbb14cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
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
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498f1488fe0ce4f68ba65588e42a509359c780aa37830c58b5bc532049f3df06`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 11.1 MB (11105001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48078c64027e315d16c3372a517ad0c996c3cf427cc76e93e09b8930683d4a89`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6ab9cca1215b9e090b5fd61f543c95516ad130be26f239a6350ddcbcb06643`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a912325e1f8f7ad2107b3ed37ccfb31fd6cf24f60f829b87f710ce0e7285083`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 101.2 KB (101204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1377c99ace9afbc4b630d2ad13a2ad54f2797a1ad5b02d255712c5274cabbfc`  
		Last Modified: Wed, 04 Sep 2024 23:10:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:02560e1e69409480316a22e0c128252d8158e8447af63065e8ba0dc7661e4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3a370621af6b03463d135102fdc5b70dd52233d202435895b030bfad0fd63`

```dockerfile
```

-	Layers:
	-	`sha256:fb9f5d0bf90cf2c36528627b064a061e2884c4b8ce20b8725eca76988de7c219`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 4.2 MB (4223740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc908c641f6d66494192e645327f8e109f089102893e1f99551a0b8a7cb6b20`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:76612f82bb19d492cda557ef4ca7e5e12aa89fe10533f9f802f660f932860e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64939265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19fcb6b90a409e53d91791ce566f2dbb2995ad53426d99769cad48f62dcdec0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c1837712cd740a7b87a314d41272c401ded8ce6df66684b504dd48894e92b`  
		Last Modified: Tue, 13 Aug 2024 07:39:38 GMT  
		Size: 11.1 MB (11105879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300cf65bc9beca57bc7882230779a6aa040b842f40c72404d5c06e5dadf718f7`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3d9476d60842d9d913502642dcba44aa76828cfb14cbaecfb739e21aa465a0`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb0f25f8fac8aa2b0b2671c3c902f209d41aa33455bb202bf968ebef99f92d`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba89ecc911f902ffdc68ce05b8a946d4c9dfe6834b0badbe843453dbe61e05c9`  
		Last Modified: Tue, 13 Aug 2024 07:39:57 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0344d9075d2b5e7102ee9ba7d47f4389ccbb2dd959b2258492790012b7ea4849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad05d8e8a9822138efd10511df029b10ff7963e2cfe6ff10fe1991e116738c`

```dockerfile
```

-	Layers:
	-	`sha256:3df23917d59aa302a0ed7bc885013174a9738e685b109c0cd41abf30d16a1398`  
		Last Modified: Tue, 13 Aug 2024 07:39:57 GMT  
		Size: 4.2 MB (4223345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8386cba83bbea8f238f4918e8b5f8d5d1d74d9d730390b0e7bc812850de98719`  
		Last Modified: Tue, 13 Aug 2024 07:39:57 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fc86b4be57cf117a0ca4558a7fb4b3dcaab78a2875da39c098636ce4d1fd6228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33961755717a6e4df1dccbf4721ed678520139dae487a163f29d22126c291cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
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
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a32a7663886dda98b3e982992ab7412bbe79dc2e558114930a6f85414704f`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 11.5 MB (11500159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97530f82c868f8106a7554a67bb6753fe0c9c16b172aa5ecc328fbfd935fe9`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7445590a739b3a522581d8c7dc1ffaece3ac9e37098e8907cfb623047fa6d0`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0630285d079475ca95c222ddec6d833d65d6eb2863881d078e45b8e086a19b1`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 101.0 KB (101039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ad846a8b84c1d32ae4fb5beb9b88fa142a72c6639a7ca617de7ac53da474f5`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c0ac5f568dcc5d1672b7658c6b3217b4286fd142b6e8b1aabcb19f4c99d5f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5804d6f0911db6c145a1be84d4149cdf5167f83f17d08b3c0ca9b1a4a57c0173`

```dockerfile
```

-	Layers:
	-	`sha256:54232af2ad07f640f95a2b03db33f7ad7c5507e91a07d9237d6e753d7d0f20a8`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 4.2 MB (4220200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a75c8cedde283c2362dcc1352ca8b9371bef2c1e4fda66ef1e0186d0a32eb5b`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:8df4e760190f3184795b360080280ad5a9275765869d679e984ad3a1c798e6f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:835645ff640e0142a0d70b8be3ba4638a382ac72c67226aec4e8588ce4ec7c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390b61ad47378182770a2a820747040d768ff99bf0939b198a7bcbf4f0bf8a7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5889d68f1c611652a413d65837ee20352e00c59841d2e5610ea3b191b17edd7`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 5.4 MB (5360097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25867322675a948e12a50cceab4e3300713f994744099d783b76f2bcdd39e433`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4220848f077408718e98ccc6eb67e4ff521ec7a6b8ac1a5c1a5e7ca67120067`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6c8a677ce3bff8a9a3b154e868b1784552773f214318e5e082d655f2fbd1ac`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 105.2 KB (105183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:09d06e052405a63123040c809e203e9d109b16a84e402292d52bdc7b0a9cdef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d2f3d10af80443a7fa61073ec0bbca0f9204569ca94bf6755608efda7a9a5`

```dockerfile
```

-	Layers:
	-	`sha256:8390bd5dd97a5116688396231b0a1182a18e98fd8ca998f6d264b4887a7fd5a8`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 2.0 MB (2002638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8b174df4e6b1276ca0d9b68a50bf1f8929847cedeece4ea19afc63fcdfe78c`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c4f9d85053aa89e9a36ce96d6f32bcb36ebf1d565cf38f7e4350dfbc540bfaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b09eae5c93db890c880b065697968d7411fd7169e3f75e153dcd61251ed72bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0639d72092b592b944940eaba5264bbabebedc923c867d5cef204e3869370ef7`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 5.3 MB (5340388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e7d1c2d83050467ab223500a26d141bdd407ae0e6e93886431805ca3d5c22`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f6e4e6a296c9284d095ca5915669b150327bff81a93c81da40429350457fa4`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6afbc297c547eebfdff6b788637e32acc191d56ab28e1b571477510a8ca5b`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 105.2 KB (105231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f55c5bdee82b1c011271c0c624cd82b39488db7acde45dacbf7146869d0eea3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb2f2b3d0e9dcfe27d3b5ae0242c59d59b5c410d29417b2bf2602ee21d9fa8f`

```dockerfile
```

-	Layers:
	-	`sha256:9c7deba42a44262b8779a5b289447570c109ba28094ec8dd6ee5b71e08203334`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 2.0 MB (2002866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4db5f9492ef8ce64fd0b1771dd024422ff8201a3607ccd5adacb6fc086eac4`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:3656f68829b2a5609535626496a1f55d42f92f6ad8471692486fd8334d870e22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:77fb9130fe78863108f7f501050ece1197ec6cf54602ff9569dd579ec57a995d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4287e443009a9cf9c2c9cfa86bc4745d2830cc3142226f9126a0bbf43aaa68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378948ec170b4d8a3013772e2b302e397bab4c44a11f0249dede601a785f45d`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 5.4 MB (5360101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee4f8a5435dcf4efe8aacde9bf929bc80f51622561ec15161b5d4c39394aca`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64d92368b359bd4d2c8c5c9a1192171b7b95942fbdf86d66157667501827e00`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e974ec6725aeedacccfdc674af6fa00d862b362ac3de6d22e82ca6bf916d81a`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 105.2 KB (105186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0057b985c6f43e1e74cae2ce0577e1ad0efe4aeb67f205e93d151a20eac4ed03`  
		Last Modified: Sat, 17 Aug 2024 02:01:34 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14cd61596e92f159e820332529cdb62730d33f911883b4e531f9e077d0774eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e6bbd7493a8f0b17e450b95e56e5c0278a13b6bf21b0844d5ae3659ba50029`

```dockerfile
```

-	Layers:
	-	`sha256:5aa75864d011ddfe1d301412abd7aef31ee304f67b8490199d6b10e8c4a3e67e`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 2.0 MB (2002674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf80141cecef2fdf0bce1f92a0b845f40570df4d34b50dc495bc6a80235db9a`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d11bf39deaf7de11ad41c96cf537df477ed85d0488ffa697612bb126b5d753e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdae2cf2d82494d1a3621947569a205d1774d1d85071b3844ba1efabb720655b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0639d72092b592b944940eaba5264bbabebedc923c867d5cef204e3869370ef7`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 5.3 MB (5340388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e7d1c2d83050467ab223500a26d141bdd407ae0e6e93886431805ca3d5c22`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f6e4e6a296c9284d095ca5915669b150327bff81a93c81da40429350457fa4`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6afbc297c547eebfdff6b788637e32acc191d56ab28e1b571477510a8ca5b`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 105.2 KB (105231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c21685943f244b1d8bc574a86763d24baf01d135736926254f4bf33003932ab`  
		Last Modified: Sat, 17 Aug 2024 03:26:54 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd4d294f2b44f3421f9a91359180bad3483318ab42326f1f3d80b7b49255005e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2060d6c33f98e63c1d617787975ff356a667c174713e3c991f12be90bd367`

```dockerfile
```

-	Layers:
	-	`sha256:87d77a954395223ffbab79c701033297186c31614e438db57959086ac47e7690`  
		Last Modified: Sat, 17 Aug 2024 03:26:54 GMT  
		Size: 2.0 MB (2002902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250b5817ba7362a6358206761a137e7ef32ace96b20f593c8fbc72b107287182`  
		Last Modified: Sat, 17 Aug 2024 03:26:54 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:c76cdb697e932bd1ae56b61482e6d88224ac8b9a88378a4b86ffae71b7371ebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:eb6c223a4a1a531b8bf95075d38c51152a0ff2e2a2bb81abb345135f64cfd25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bf875c9a9f9ccf9291fd353336bc8786a19878fac26ac669a87ba3f3dfb484`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a52ad96cf081ad99e55f0ae7da8287d3ab9e67b73b6a19de653dd1f36a1b43`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 3.6 MB (3622800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3243246bb56a63815d22e9ade9a0587c7e1d13022048e8499dc45f5571c6c905`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e820e921f70036b4093f941d63cb1544549093de2b85c8e4cb082b1bf63066ea`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343e179ce49c74fdc934bfbb8a6a84b0f0d5341974248fb92fe7bca3ef25c970`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 110.2 KB (110155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52c3b54434ac146657c5403d09bf482796ab6ba9a4f0a2b37144a53e6ea26041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa3cf2bbeb0b8167478ff916145f77e3296a568b8e70e6b866711d184d05c9e`

```dockerfile
```

-	Layers:
	-	`sha256:c051b4ac90a6dee339f319c6b8ffda7f8091567918686d946831aed82bf1045d`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 2.0 MB (2041055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45466d6ee69840024e3f90d1ff6914bd5dfdbab1d6746091fdcc8fdc5ad00617`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c0be1982387e329151c748e23b1d3b432adddfadf32f4894ef963ae2eee02ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed49370c0d1c5ff9d6ac073942dbfbcd7f2955aa3bf492a590ad95c39fccb81`
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
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ff02d894ad8e635c681df9ab272273ee6ef6fc2de761dac177e4b08a7996e5`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 3.6 MB (3594216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbff8da0ddd5b0063079b89cf8dea9d21d2d6039ad2dc20c8077cecb4a6982c`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce958e839238ae37a8145b798126f2f38ac17755e85d50b2cf84ed1743fcff9b`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5492c71801d75cd5ec1c6a42e5e6a93410815c737e19793eba12356e09ea3f5a`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 110.2 KB (110195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c3f7d9652103e03397e3c9d96e94b427eb2fd796ea3bee960a4e4ea1f5607f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536afe5b7b22b4796509887811eb8360adffdec15e902c171354c65c5d49ab9a`

```dockerfile
```

-	Layers:
	-	`sha256:ca275407384afacf5f4c06700c6fb1e1400710c24ba43331cb43ed803af825aa`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 2.0 MB (2041314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a3deb8f03cf9268d0c4a1571d227c850fed332c63e7ed8c63963349199ec26`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:69000b4b82130c86111e2d6f2154e383374ca25200434d36c35649a4e5559d0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:56bd533555c24b1a0e33d8715b923991f52a2390e718cad615e3bff0515609e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33271295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3566d261905df20f6cb67de2e2b0f1a5e5c36a0a5d60904a443b38395ad9a`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cc7342a9101f7bd65ee11e85877b5167401a573496bc13b0254de69412ecc9`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 3.6 MB (3622828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698948cbfdbdb47f46cfa18f153db97f0d4185b2ed0b0ffa4ed7241dd111275b`  
		Last Modified: Sat, 17 Aug 2024 02:01:54 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562faec9eff170ec13a317ec590e7fc5d2465196653271ad94727e25bc8311b7`  
		Last Modified: Sat, 17 Aug 2024 02:01:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1412ebcbb56620affa88dd6fbb7e39dcb76e6bce53dbfd670137f69d3f2c974a`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 110.2 KB (110191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438eebc3143823b29528449def844b428375d64ee9196d47b83fb4c4122f9bd8`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6614b7ddcb99ae1b7fa0467afc9700f61781c0689f09b79056afdbbf11d8bb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f79af39f0b140321d5d479f607c4990268d1a5ab84e40cd385f7604fcdff53c`

```dockerfile
```

-	Layers:
	-	`sha256:a6325c5e50dcd50ef9cfaea30ddc8a7cdb33eef4646621328bb6e914d10778b8`  
		Last Modified: Sat, 17 Aug 2024 02:01:54 GMT  
		Size: 2.0 MB (2041091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e92bff7835cd7b5a49eaf89dcfdfd1235e8355f81c4e637cf643075199c3c8`  
		Last Modified: Sat, 17 Aug 2024 02:01:54 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ab895a10b5c2a35700955e7ad688cb39c99dd1fcb1ea8906d533b55001376066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b09dbdd8f2ca864eb51b667cf425f880a87f413fc2e08b365de111f19009bb`
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
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ff02d894ad8e635c681df9ab272273ee6ef6fc2de761dac177e4b08a7996e5`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 3.6 MB (3594216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbff8da0ddd5b0063079b89cf8dea9d21d2d6039ad2dc20c8077cecb4a6982c`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce958e839238ae37a8145b798126f2f38ac17755e85d50b2cf84ed1743fcff9b`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5492c71801d75cd5ec1c6a42e5e6a93410815c737e19793eba12356e09ea3f5a`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 110.2 KB (110195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5169b924b8deb541b69bbd51bcd176c029d87d47bdf518075b1d5cc550920da`  
		Last Modified: Sat, 17 Aug 2024 03:27:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4256e963e77ea1a32c5205e91bbf733bba06be857f47f92aaec98fddfd81b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6d8b3d855e98e05ceb76c4bba59772e02bec8429df2ce8ad73eaeb061688d4`

```dockerfile
```

-	Layers:
	-	`sha256:bd47fc093378bbd2d7d030d9958582ca469738dbb00b645373f2e8614f9330e0`  
		Last Modified: Sat, 17 Aug 2024 03:27:44 GMT  
		Size: 2.0 MB (2041350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e288de02dab95dfcf208aec0315505ec789648e1f296f5c8442a717a72536d1`  
		Last Modified: Sat, 17 Aug 2024 03:27:44 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:86bf16ea341131b94834b82b1fad1be2a4e2c758bdebf6269fb81005493e1440
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
$ docker pull neurodebian@sha256:baca0af0e600d4eb5673968b51b81e3c01dfbd4afc281940ff7d7c6d78ed741e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60918412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f5f8734b677aa4409e1fdaeb2596287562419a627a2047c28b218798897870`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8553aac5ada3d57fa02485752729b218183e391f256b8f556021e4da979429`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 11.3 MB (11266596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0920907450c5815ca556bc9418b43897f0a1b433d9c94fbc6a8f34fc477cf`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bfc646f22c7d6b23dfd43f1fd9e959530e4cdd2d7cc1466d873115d272717e`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000c71c1b18acc1de1ce7d26b6d2e3b79868d9d487afef3e6c1fdba6610178a`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 93.1 KB (93124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b8934708ecf6bbb786c047f9cbd663c371f1bc651676f2255113e3098c85c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c8695a09f10ad91087d1b0ee82aba1f221b3092ada8d8c9f9448a07dcb75e2`

```dockerfile
```

-	Layers:
	-	`sha256:c4d3094a41db65375f15c2e76db9bc8bc482af824a6a9a64abb0222a0ba0ce98`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4124a58a47fb482e249defb5e353787cf657769d362036433e95e912192179ca`  
		Last Modified: Wed, 04 Sep 2024 23:10:40 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a1cb3b5b67cf0e33740eab0262c450d59e72b86b395d24c8d3a9f168a289b6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffdbe3d5fa71ad63f7f9ce991223af396c40a9156a0e8c62e855b7bcf88d251`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
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
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6516de16487e13fd76db87360111809c44b836a1dd673fa8de93b983583728c`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 11.2 MB (11232114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6108c7a663d245cb0932ddfae87f92ca3e1de7fecebcc1c63ff8508adf4e6db8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08a498a3c3c4bf8a5ccf542b868e62921588d0f25c6cc09bac0d6a005711aa2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e20e8cb909fb4d46a63b2053a3a0c458af529d893341a678b2c4b75796cb9b2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cb795a0975baf1f75ee1ce62b377c40aac3dde2c15d9e5c6b8970685714a2510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0fba90f7da7dcd6b439e7ba720e8ab181de5d8193ac16bd8c915f30d4e63f2`

```dockerfile
```

-	Layers:
	-	`sha256:f48d7ad43d43e6852e3cd4b617ff75b9f95e9ec8c998d37041fe7d0e955140a6`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb0c8dfdbaf13211fbc6bbf2d1f5e6a0992ef2ef16cb8a437b676e1d54898c8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 14.1 KB (14076 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:d91ae7a8e8e0a9cd1ffb1fdb782e80cfd9da956bc72f78806584839aec880e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb593a6077e15e3e59d1eeb6e935ed129fded0fb46fe5d39199cd3652ccb7d7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
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
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a474c2633397aa8306d1b46ed39eb7746779e75412486f5a38cf877780594f5`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 11.7 MB (11688978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54facb93fbe5b8f9909d31756bba5f2ded7ec557a297888397bb38450bc1eb8f`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fce3b83199534f3d75365cc5b58bc55d368f2ec44856cc75b30160bdd1d8`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5f31329f83d69533edc23d6eeae9ff2fb069d68a6cce9838698cd524b8c568`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8897ff5043a7750fd4373550d72fc68d1b6d3d82d162871168d1f00796c311f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbe09b244eb3ae159769ad770a0dafc5091e558adfebaa8d5fb67510a9d6014`

```dockerfile
```

-	Layers:
	-	`sha256:fc84cae9d8bf21b3eb9bd59bdc787ae4b071c0b38d8be46234d7420219476b7e`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2e799e06efa1c383ee2a950c88b8103826599d4c0e5fb804093db0855c2bcd`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:9e085870cb694cf3b669663a1b243a092c0b330bbafd92c3d7c01682ba8ca0d1
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
$ docker pull neurodebian@sha256:d5b072a5141a86dd1d2500e0c66407e895b6a7cd02772fca2ad2953e01036964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59510892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986472010412306b6437bd6a1fb9bdce5785924d8b5f20a8a1208d6c5635ee52`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
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
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034bc937277199ec164847356d05777d74634f8f5f05723bd208cb3eb6138b78`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 6.3 MB (6260893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b77db3a43cb43615e3531865bc65936809125b4da8289276926163d9c2d30d4`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f157f39a62fa798f416a12a4fbcc54c4d50bd039d2428ab32c79c125e0c5874`  
		Last Modified: Wed, 04 Sep 2024 23:11:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f02174b8243c9482bc3bd0e6ee8f3ee77adf56b32417414cddb12cce0e13f62`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 91.2 KB (91162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1717a43a3dd14a94d30142710e223970593b56d0f5309f2ee6294f49cda02ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26637a4026d86d363cc068a6499ad746ffd2cbb35b7e93097653df757a8a92b0`

```dockerfile
```

-	Layers:
	-	`sha256:9c5747490dd0983fcbe9f53c25f5f90cfa0b682f70fd6b32283a230b556d8b4a`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 3.5 MB (3532460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8625fdd4ee91d417fb4bb1b9f41a818c610a6e5b6b07f6806186a3aa72e0def`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 13.4 KB (13397 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c24554d2b03c88038671f7dd363e185920cb2c3d56fe292a23a6b5316ca9e5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59483897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25afc236d3afba5d4a0961256a2b5fbfcd0bc83d16154e306ed3f4ca8f718d7c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d3aa31e5e33290bb28cfd74e2b2a88ce7e4415dc0d995c3c39d36c332bdbfcf in / 
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
	-	`sha256:543c0d8816b61b146fc103b18d6ec335253cba7bad9fa7f1cb3e794a6b9e450c`  
		Last Modified: Tue, 13 Aug 2024 00:44:13 GMT  
		Size: 53.2 MB (53155250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02191b116647481476d52030a803e28ba5e68be75a6620aa17907059437da993`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 6.2 MB (6235299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49fc1a3149682d8a81b651e3c53dcdbb45d3ae5b19c1abed966b8e7ff9ec25`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f53b0fdfbf88451067600990b58000941f44e8fb25d7f56a2040f4c02e5f88`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab9ebaf49832bc2e70ff76ed23a0cd70d02d5b8c5853db5f86181077c727f6`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 91.4 KB (91368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:565ddfc6af473f19ecdd32e26652054091c8686db3a9e305d6c86b6dbfee0622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8188b1f100e1b01a87195c48287ad47b85c7865a2ce5a2a8226ff6f5ddd1f6af`

```dockerfile
```

-	Layers:
	-	`sha256:06f04d1df7ab382a4d8f77d2d144bf4aeba6c4ab3fafe199d4e33a6bd92251ed`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 3.5 MB (3533440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b4482dded10009090fd2f781e3e4583a565934f8b5e80fcdd3e3a36123f242`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:2d7295e78c1f93e93a2fafe3cf5d6578c9bd04ba3e70aeb1ac00e4ab6a423853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98da68791e8c85b2337b5ace3354f2cf5c2661f1890b36c48faa684596d1a893`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
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
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0659bfc4fa78a1d35cc72364a5ae98ac8f4d07bd69d5519d26f5a17cb400a074`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 6.6 MB (6566071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8727d0f61d96321e8ca009fce720e24d7cc8b2eef994ca6bc4de03fca1eec706`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a36b20258ae61eb5dcc9eb1db3b6f8b4cc8dd1758e38b36d1ba0854ca92f`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08afb7bac914d3affff0a203687d081a71dfea865fb144968f617538c675d23`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 90.7 KB (90690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a550bba3856e784dc5634debe1d9eaa3713a572c52b7a21ec54d73e0c2cf13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab79690e1cadf319dd8b38d9a493570fc9e9c614dacf0dae87dbb78b2feacbdf`

```dockerfile
```

-	Layers:
	-	`sha256:1a0d28cdbf8efae3239dea7c48eb32f819b4f35eaba78d926a86bda35ae7add8`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 3.5 MB (3530303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c286a639d57592fa8d3072963de485396b9c4aab261687c908e99b643ae588`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:299a54ccfcf4ed7b643740603c1abf80e811c5ee8215e3065b305e8fb0ec9dcf
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
$ docker pull neurodebian@sha256:26a59f612ed56a4697f366a60a77194f5641af54e9a1664a020ed586da6d71f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59511253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f2ad76884e7f344ab5b0e055a2b96cca37774aef8be383075916292182c8af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
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
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2c007c64da352ec00a7c770959f382104c4122028f01d19283f85f7c5196e5`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 6.3 MB (6260869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e19ed26657edb9a90abf530ae502f28e31e1fcceca1c8faa0c42eca3a5984c`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d3b2c132c8026f38909d51e7a45f40fa7d65bfad4af42b8ff1cd3cae31b32`  
		Last Modified: Wed, 04 Sep 2024 23:10:59 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5389944352d641fbf5d89602026b8119d8cf060cbdac213da804dbba99554b2`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 91.2 KB (91154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a05ede3e7172d449e69bd39da700fee287c4bfcf237b04a327d7c64236ff83e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bc86531131eff71b8b0308bd0c49133fb6956878d87c78527fb4d8c92332daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c70794af3101644cfd9922da9e9cf1d6e31f20c36f21ce04b23f581344a9ef`

```dockerfile
```

-	Layers:
	-	`sha256:2dfae5164f018ebc1798d623dbc99edff836f35311794491eaf4a62521db0c5b`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 3.5 MB (3532496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155d36edcf9182b5d9cd047985eadbb745b640d0e8d69fb82d6ffba6986d16e1`  
		Last Modified: Wed, 04 Sep 2024 23:10:59 GMT  
		Size: 15.4 KB (15428 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7f830e4e2c2d4d6fe4727b5f3c67cef86820ab5773bf9fefac3d72d524451a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a40f7d644f46a12c3166e7f144ef587ae0b9d775bf582804a5923c9540f11c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d3aa31e5e33290bb28cfd74e2b2a88ce7e4415dc0d995c3c39d36c332bdbfcf in / 
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
	-	`sha256:543c0d8816b61b146fc103b18d6ec335253cba7bad9fa7f1cb3e794a6b9e450c`  
		Last Modified: Tue, 13 Aug 2024 00:44:13 GMT  
		Size: 53.2 MB (53155250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02191b116647481476d52030a803e28ba5e68be75a6620aa17907059437da993`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 6.2 MB (6235299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49fc1a3149682d8a81b651e3c53dcdbb45d3ae5b19c1abed966b8e7ff9ec25`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f53b0fdfbf88451067600990b58000941f44e8fb25d7f56a2040f4c02e5f88`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab9ebaf49832bc2e70ff76ed23a0cd70d02d5b8c5853db5f86181077c727f6`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 91.4 KB (91368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c01f4db884a7e9e5e03a2c3a4f148b5eae1fd576626b29c6eb6ec84ab7abcb`  
		Last Modified: Tue, 13 Aug 2024 07:42:44 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f7a4d4e88328b2a38b7d20e94dc0f3436ca1ad4f9d60b0c983d6c2f136e7ed18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97881e2fcfabb0b2c1d5bbdf55f7996e98f77c400d6e133a047a29729f74e0e6`

```dockerfile
```

-	Layers:
	-	`sha256:346da81b252618de9c218de26e73488c09966414f4b1c0e07c5e8b3c58bba1bd`  
		Last Modified: Tue, 13 Aug 2024 07:42:44 GMT  
		Size: 3.5 MB (3533476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52f58fee8fab48fa3131808e449368a6cda85d7f168728764bbfdedbf9d3ee`  
		Last Modified: Tue, 13 Aug 2024 07:42:43 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3879645d8248e19c7cecc51e81e443dd2244460b4f358cfeb57cb286852c04a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb0d7cc60a97195c40904e7573f816efef7d6f12cc2155af4cfb3e20b788da`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
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
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b71d132a4344bb16e2e09fd83117250f48d572c643b3a712f89502bd494932f`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 6.6 MB (6566180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b92d44337ab2e36cf50dbb0e5f5a982aedb8ea031edfd566ea77794b8600db`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83d54a7d8728387f810ef105293ffd3ecdbe46c909d35465dd6ac692a203a66`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c86223c48237f67a081fdc1da5b575bca1e0b24ca39b18348f604b229ec46a`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 90.7 KB (90739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c730d96f05d4551706957182b16dc3e0b695f848bc18e53ac8a87794f7bc71b5`  
		Last Modified: Tue, 13 Aug 2024 01:12:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:afa48e552f3090b92141c3f16761ea91ebd9c37674b87f9131690f18413b23a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc69503183698682084ccc15450c076f8942d02054a333aa86200e39f668a11`

```dockerfile
```

-	Layers:
	-	`sha256:d17136678b054f4bbd69c0d37627fc779e2d83be22dc0d59ec71ef570984beac`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 3.5 MB (3530339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1d4f4372fabf850ce1ffa73ac663ea1660175de7920a8b704f09006156321a`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:623f88f24b9ae0b8a922939a2b76e884e1e60ddeacd3c078ba3498eab2362b53
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
$ docker pull neurodebian@sha256:ef96f4ffd60228e64dd4357acf6bb4f1f7d1a683e563095ae5497bdfb12ab6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604cb8f24240d11a65cdc5cc10ba42ad769af0fdbc4687d40c0842c04b1cfc87`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
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
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8229cd5767c1fe3ccf97dc241f9775c959e3a2f3ff08b32d367d68ed890c2463`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 11.1 MB (11104998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a8f94d7e2ff63aff6b5aa019f3edfa8b21cb30905458ccc1bd9dbbdde9f7fd`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76998563fe66245924cbad91c3a4e926d33b00a1b07a82beee9a57b4ad2c0451`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704c0a9181147f709d4f6496cdf26505b3048b62468a58abd66402203892757d`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 101.2 KB (101189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb7fb9c8cae32f8ae1fc059f4f408e429acb616fd20bace226275bd99a48f2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df983365605673ccef6006f76ec41783d05efdad0b4a23227064d28cf8c142a5`

```dockerfile
```

-	Layers:
	-	`sha256:f6e9e0a46a41eaeb5600fb3f15855752c1f5c7e9fbe5cdd3e0fbff0ea3eed8f3`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 4.2 MB (4223704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93094f619548a5cd2b8be5a544aebb5e90632b2ac494ac5cd9ab290fe2cd5dfb`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:aeff8d220de591bb51be66b1509ac7ddba972d21b8ba2722877b78b494200cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64938906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d8f04d5762a59bac48f71e1dd82a7d959c727dcb13fd712b1df8d452ad673`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c1837712cd740a7b87a314d41272c401ded8ce6df66684b504dd48894e92b`  
		Last Modified: Tue, 13 Aug 2024 07:39:38 GMT  
		Size: 11.1 MB (11105879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300cf65bc9beca57bc7882230779a6aa040b842f40c72404d5c06e5dadf718f7`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3d9476d60842d9d913502642dcba44aa76828cfb14cbaecfb739e21aa465a0`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb0f25f8fac8aa2b0b2671c3c902f209d41aa33455bb202bf968ebef99f92d`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4be26975a18f80aaabd7590cd69e0f346907cd5fcafe423ceaf798289704efea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2787943a12315c16c2baf17c53051758e4ca1973bdfc16f70971e55f09b97f`

```dockerfile
```

-	Layers:
	-	`sha256:728dadeef62652439001ed5cabf16e60c4d4bf704479452e7732bc9c0e12f289`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 4.2 MB (4223309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccbf9ee9c6d729099509d11ee7884bf64e5a1aca2a4ede7c21b4f44ba19e7ca5`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:d6442aaf411f6b7317fb029bdab3b397873436e024cdd67f8aef85e2e6b04f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab815b1d7bdb4ccefbe5ccd5f6d4a166c3499b8539f5103f349cd796af54a47`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
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
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fb4eb6f62cdeba31e6d69cfb84d444cf628b43ce8002eb68b122365e12ba40`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 11.5 MB (11500076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d529280f6a6a918ad676a325f6c19b0ca78d98839c022497e74193579fc99634`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bbbf843f82657df2505db1accc5e4028926b7a5ba7e2617955928e74594645`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8f6c624c0ea5365eac6c105ff32abf1ace893ef3564c444c7acbe11a1c5adb`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 101.0 KB (101035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:154e3e036b4ace281d2534c1865c6df071c7f2f55a763557ee0164c988bc95c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5e1b29d6f8687b416c2b88ecd885495ed77390e347b54b2697a2c867480ab4`

```dockerfile
```

-	Layers:
	-	`sha256:95cd5a6b87e46d9955ec52378adf03f93125f5c49562a3453041f5c5804f389d`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 4.2 MB (4220164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2268d0e3d6467811593dde30efe7a163fc6128557e98221180fb0d524126af63`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:6d2974fe43af719acd5fe2f15ed2b7ea3cefc0e1a0fadc31ccbb1fafd1ae2b7d
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
$ docker pull neurodebian@sha256:37742f33147749a7cf8493b1c57e513137caf3a39237ff5fd69d05e9741843d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198e3b59f16736e7d1b4a215fb775f60a8db597df22072c3d4e56b031dbb14cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
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
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498f1488fe0ce4f68ba65588e42a509359c780aa37830c58b5bc532049f3df06`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 11.1 MB (11105001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48078c64027e315d16c3372a517ad0c996c3cf427cc76e93e09b8930683d4a89`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6ab9cca1215b9e090b5fd61f543c95516ad130be26f239a6350ddcbcb06643`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a912325e1f8f7ad2107b3ed37ccfb31fd6cf24f60f829b87f710ce0e7285083`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 101.2 KB (101204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1377c99ace9afbc4b630d2ad13a2ad54f2797a1ad5b02d255712c5274cabbfc`  
		Last Modified: Wed, 04 Sep 2024 23:10:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:02560e1e69409480316a22e0c128252d8158e8447af63065e8ba0dc7661e4c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3a370621af6b03463d135102fdc5b70dd52233d202435895b030bfad0fd63`

```dockerfile
```

-	Layers:
	-	`sha256:fb9f5d0bf90cf2c36528627b064a061e2884c4b8ce20b8725eca76988de7c219`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 4.2 MB (4223740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc908c641f6d66494192e645327f8e109f089102893e1f99551a0b8a7cb6b20`  
		Last Modified: Wed, 04 Sep 2024 23:10:31 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:76612f82bb19d492cda557ef4ca7e5e12aa89fe10533f9f802f660f932860e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64939265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19fcb6b90a409e53d91791ce566f2dbb2995ad53426d99769cad48f62dcdec0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c1837712cd740a7b87a314d41272c401ded8ce6df66684b504dd48894e92b`  
		Last Modified: Tue, 13 Aug 2024 07:39:38 GMT  
		Size: 11.1 MB (11105879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300cf65bc9beca57bc7882230779a6aa040b842f40c72404d5c06e5dadf718f7`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3d9476d60842d9d913502642dcba44aa76828cfb14cbaecfb739e21aa465a0`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb0f25f8fac8aa2b0b2671c3c902f209d41aa33455bb202bf968ebef99f92d`  
		Last Modified: Tue, 13 Aug 2024 07:39:37 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba89ecc911f902ffdc68ce05b8a946d4c9dfe6834b0badbe843453dbe61e05c9`  
		Last Modified: Tue, 13 Aug 2024 07:39:57 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0344d9075d2b5e7102ee9ba7d47f4389ccbb2dd959b2258492790012b7ea4849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad05d8e8a9822138efd10511df029b10ff7963e2cfe6ff10fe1991e116738c`

```dockerfile
```

-	Layers:
	-	`sha256:3df23917d59aa302a0ed7bc885013174a9738e685b109c0cd41abf30d16a1398`  
		Last Modified: Tue, 13 Aug 2024 07:39:57 GMT  
		Size: 4.2 MB (4223345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8386cba83bbea8f238f4918e8b5f8d5d1d74d9d730390b0e7bc812850de98719`  
		Last Modified: Tue, 13 Aug 2024 07:39:57 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fc86b4be57cf117a0ca4558a7fb4b3dcaab78a2875da39c098636ce4d1fd6228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33961755717a6e4df1dccbf4721ed678520139dae487a163f29d22126c291cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
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
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a32a7663886dda98b3e982992ab7412bbe79dc2e558114930a6f85414704f`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 11.5 MB (11500159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e97530f82c868f8106a7554a67bb6753fe0c9c16b172aa5ecc328fbfd935fe9`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7445590a739b3a522581d8c7dc1ffaece3ac9e37098e8907cfb623047fa6d0`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0630285d079475ca95c222ddec6d833d65d6eb2863881d078e45b8e086a19b1`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 101.0 KB (101039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ad846a8b84c1d32ae4fb5beb9b88fa142a72c6639a7ca617de7ac53da474f5`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c0ac5f568dcc5d1672b7658c6b3217b4286fd142b6e8b1aabcb19f4c99d5f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5804d6f0911db6c145a1be84d4149cdf5167f83f17d08b3c0ca9b1a4a57c0173`

```dockerfile
```

-	Layers:
	-	`sha256:54232af2ad07f640f95a2b03db33f7ad7c5507e91a07d9237d6e753d7d0f20a8`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 4.2 MB (4220200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a75c8cedde283c2362dcc1352ca8b9371bef2c1e4fda66ef1e0186d0a32eb5b`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:86bf16ea341131b94834b82b1fad1be2a4e2c758bdebf6269fb81005493e1440
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
$ docker pull neurodebian@sha256:baca0af0e600d4eb5673968b51b81e3c01dfbd4afc281940ff7d7c6d78ed741e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60918412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f5f8734b677aa4409e1fdaeb2596287562419a627a2047c28b218798897870`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8553aac5ada3d57fa02485752729b218183e391f256b8f556021e4da979429`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 11.3 MB (11266596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0920907450c5815ca556bc9418b43897f0a1b433d9c94fbc6a8f34fc477cf`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bfc646f22c7d6b23dfd43f1fd9e959530e4cdd2d7cc1466d873115d272717e`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000c71c1b18acc1de1ce7d26b6d2e3b79868d9d487afef3e6c1fdba6610178a`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 93.1 KB (93124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b8934708ecf6bbb786c047f9cbd663c371f1bc651676f2255113e3098c85c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c8695a09f10ad91087d1b0ee82aba1f221b3092ada8d8c9f9448a07dcb75e2`

```dockerfile
```

-	Layers:
	-	`sha256:c4d3094a41db65375f15c2e76db9bc8bc482af824a6a9a64abb0222a0ba0ce98`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4124a58a47fb482e249defb5e353787cf657769d362036433e95e912192179ca`  
		Last Modified: Wed, 04 Sep 2024 23:10:40 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a1cb3b5b67cf0e33740eab0262c450d59e72b86b395d24c8d3a9f168a289b6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffdbe3d5fa71ad63f7f9ce991223af396c40a9156a0e8c62e855b7bcf88d251`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
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
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6516de16487e13fd76db87360111809c44b836a1dd673fa8de93b983583728c`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 11.2 MB (11232114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6108c7a663d245cb0932ddfae87f92ca3e1de7fecebcc1c63ff8508adf4e6db8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08a498a3c3c4bf8a5ccf542b868e62921588d0f25c6cc09bac0d6a005711aa2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e20e8cb909fb4d46a63b2053a3a0c458af529d893341a678b2c4b75796cb9b2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cb795a0975baf1f75ee1ce62b377c40aac3dde2c15d9e5c6b8970685714a2510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0fba90f7da7dcd6b439e7ba720e8ab181de5d8193ac16bd8c915f30d4e63f2`

```dockerfile
```

-	Layers:
	-	`sha256:f48d7ad43d43e6852e3cd4b617ff75b9f95e9ec8c998d37041fe7d0e955140a6`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb0c8dfdbaf13211fbc6bbf2d1f5e6a0992ef2ef16cb8a437b676e1d54898c8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 14.1 KB (14076 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:d91ae7a8e8e0a9cd1ffb1fdb782e80cfd9da956bc72f78806584839aec880e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb593a6077e15e3e59d1eeb6e935ed129fded0fb46fe5d39199cd3652ccb7d7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
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
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a474c2633397aa8306d1b46ed39eb7746779e75412486f5a38cf877780594f5`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 11.7 MB (11688978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54facb93fbe5b8f9909d31756bba5f2ded7ec557a297888397bb38450bc1eb8f`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fce3b83199534f3d75365cc5b58bc55d368f2ec44856cc75b30160bdd1d8`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5f31329f83d69533edc23d6eeae9ff2fb069d68a6cce9838698cd524b8c568`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8897ff5043a7750fd4373550d72fc68d1b6d3d82d162871168d1f00796c311f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbe09b244eb3ae159769ad770a0dafc5091e558adfebaa8d5fb67510a9d6014`

```dockerfile
```

-	Layers:
	-	`sha256:fc84cae9d8bf21b3eb9bd59bdc787ae4b071c0b38d8be46234d7420219476b7e`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2e799e06efa1c383ee2a950c88b8103826599d4c0e5fb804093db0855c2bcd`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:92b6eb86e62a3a40e533bddba7e6ba36aed887e0ac522a884548625d92be5637
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
$ docker pull neurodebian@sha256:847fa5b5f7cf1bccaca954bf29c9760f6e50b0d341c1fc9922e71b16a107dcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60918838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d8b68cc7b03f4463b38a4b84766e653af6f629425f8dc9da21a01905f86c41`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cff9496b0f02716173380ea8121b9e078fc273f6d7523b800d9fe735b5dd1b`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 11.3 MB (11266595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5983ad1294ee53f6d8da2393360eac5f051d3bc0b588717c0d4cd3e142217c`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf285c1642ebca0cc13aac597170ef3a5c579a105f0f92629069f4832450ad61`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed44b93503e6a3d93bdb96a16f03e2b54bd73a19da0bab6380ba0ea3510e5cd8`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 93.1 KB (93123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fac7a70a3b2ea3f16e625c5ce0fedc502786c081db5610946a45da1b8ab44c2`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e24effabf132ff5cdc935ff05cd29e117b0bf3205036161440b7bbed70d99ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52f163fc775a474972895d85969b53cfac0fff58bcd49825409af99d1bef98b`

```dockerfile
```

-	Layers:
	-	`sha256:398cb201c6629b1fc0c304b57e8d35385ba361d53e29d7c558217a80617152e3`  
		Last Modified: Wed, 04 Sep 2024 23:10:44 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223b164f125eb0ef2acf8dfaff4c3934e24cfec268650cb9bef3c76614f46ab9`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:761fa3220c10853beea131741907ee20e70ec4521ac8bb053ed3102cc2c2f107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c6a24608f1cf51881701b2548227ae1a0c126c6ad59c7c32ae3e326410aa0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
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
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6516de16487e13fd76db87360111809c44b836a1dd673fa8de93b983583728c`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 11.2 MB (11232114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6108c7a663d245cb0932ddfae87f92ca3e1de7fecebcc1c63ff8508adf4e6db8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08a498a3c3c4bf8a5ccf542b868e62921588d0f25c6cc09bac0d6a005711aa2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e20e8cb909fb4d46a63b2053a3a0c458af529d893341a678b2c4b75796cb9b2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce457b9d5bc4664f2ee4fea10d635db111976ec6879c1d1b65c5f2583dbe5583`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:faf07f81a060067adb199891ec5a55de7b6b552d9e1425f1af3d811264f4ad67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b630765608bbb9375212b2673d9d41627e2f3fdad5f8105e334bc40f372814b6`

```dockerfile
```

-	Layers:
	-	`sha256:b5b0a3582701ba2dfcab416b724d504cf731b6eba018c782d7f8f980f48d5880`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2796e687428634d360ff415826bf00c056a4a1fd7916d81eca260088e413ab5a`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6dda59b69a60752417dc53a7da8941269d242b1e51024eefe430dc3c8678535b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62364011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6544912638a3d685fb71af9ef012ae48702e550f4eacecadc34616be26b1ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
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
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96a775276b452d08188a5c8cefb2671c2351befe343f1b71ec2831ff494f794`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 11.7 MB (11688976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cba750c7d48374c4a665b3aa6dbc0d35907c8f5351297534109e7710fb5c1f`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f40691f5b23aab625dedc59cb84165c3346c956f411c37faab61829e98875`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f559b7b520cf1d9f632d590f4a76abef8d20d19ee766429dd08dfd1c710e99d`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3984a8ad3a3a24cb4c87f0a2b5e7d680ee45cfce31b1e5cd4e4f20f1155943c`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ef44f9fdf0ade8b16b042df566cce5c0d994e196038e8dc7afac19802fe5532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132b918c3187bacdd483261bb47116c101b17645636f69910a6307417710fc41`

```dockerfile
```

-	Layers:
	-	`sha256:46ddedcbc2ee5bb19f1be63bafb03eb6792a0d36311f43bdc4abca7f7d714bba`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b55d3c3b9f45b61d2f39e46bd54d2650bf8f8a7462f64277466dd89f98889a4`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:5d3129afaf9a1323fe20f7229e24f8d783577c51d4a4efee558a2fde23f60936
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
$ docker pull neurodebian@sha256:a546d8ed9ffe1cf9bfaa5f41e6990494d4161f32f71c2912d6ff8a323fd891d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59491484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf42119ac53bfcf848e5c69c4b517bd04ed962dfe730d51ec7ae87855959ee1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
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
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb4d57c723071fab9db60a4db2147e17aa66dc83d2eb2eaa6d6579487ee0405`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 6.2 MB (6245441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5983ad1294ee53f6d8da2393360eac5f051d3bc0b588717c0d4cd3e142217c`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f5e26a0664131c25e2eec527fbcf80640e1dc3a81b7a9f1070f1b76dbfc976`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f414c1a656a41c98a86a7e5ab714d0c744b0d0e057887321cef5c818745e553`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 91.1 KB (91108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:90095457c2c3217e470366efd9f555dc4106a4f43a068b16fda1a15a50cfe397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1dd60de3b0104390f365e269fc3dc0c0f82664e1ce82ddb3bc0504bdf434f0`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3bd20bfbe30fc6feb1760c58ab8f8348ba270666600d2970d9d6f00bf0e47`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 3.5 MB (3533284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f3317280d884cdafb352868dd83567052bbb80f73737cf10ca00dbbff1c8a0`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4902d30efab700e1e0e7523ad44858bd58a9039c36ac78d7c66275ab9b3cee2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59480755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daccafc1f00787667713fbdf34071b12f94780c42ed253bb68afc7b749d22869`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
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
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb7ace09fdfd476fb95d4fd5a8a2edd7a9fdf7565c943ea7c1ee453011b5697`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 6.2 MB (6235166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af976523b1ff0ed7a6ea2d97619433f9e2ed6a36abcae442c116f36141f7c5`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe64922d76d36467a2655a19d8f70ca78b033cbb756a63287ef0050ee43aff9f`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ce3529f0b82b4882db3aa1ee50dd070dbe6994cf2242d75819e76f0acfed4`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 91.2 KB (91163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:89a4a17aa7e58a5b71aa52e99a139b5b58f4b64bb4d7f6232dc569fccfc738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9ebefda3efecdb73baeba3204318196ebce232572ff0bc926c70b78d5354c0`

```dockerfile
```

-	Layers:
	-	`sha256:844f178c4ab0992a80f84dca8dbb6ce33a4411dc7b869065ab23976c51f13e50`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 3.6 MB (3561367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdfd21adf8224349c32874c3825d25d8472c8564d30be72e731e594e359c63b3`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:2917d3afeb3fb636e12940beb6791076a7cca7bcc9323f0d210d2eb049517a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60435962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162543759a640728d99080bc6821ca27f669e5e6d2f194830250fa18d7d5ab66`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
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
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07041f7523e0901d7c47895945c0bd1cacb4692d4614b1ffdbe05fa57e01e4df`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 6.6 MB (6565982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca643e5a596b37baa07257045ef13923dcb3596dba7f1d83275b23371f8122c8`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248be0caa7517a9fa8f3ceae041a4a546ee6ffcb5a8e17da61311b64cef0f39b`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465fec9852b0db92fca39606004e3da1bff74c315b4ba1a49ae6f98bd4ce588c`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 90.5 KB (90497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:194159e51e60e4cd446bc9871b2b9dcc9c1939ec0cb8ae4a5be2d10f5da5b5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da11e8ea5815e2cc0c24e8b7a74d6610b60031b2503f72b6a45eaead60b0e0d`

```dockerfile
```

-	Layers:
	-	`sha256:214c5fbd9973ffc5415fc3aeb6b5c3f3dfccbd6b98cc07ce869780e51832b773`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 3.6 MB (3557418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b25cf0ea84c2e63b9d10044e8b28a910dd9082e4e5f6fa9c44c115d782f698f`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:fade21252c86f3a8878c4435f1307a63b1ed258def3b7fb11f01a6d2b8fb2cbe
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
$ docker pull neurodebian@sha256:82e474c2ae8e21c50a816ca8623bd88bf10f268ef4546821dfabcf820e0bf1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59491933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fec2a1fcc57d10ea266a88d73ea6e17c9ecd09671b8c84fff39ae6cf7a2f9fa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
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
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb091556b81f4904845d65b2153884d581ad6cbbdac107a2f862a6707fc5218e`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 6.2 MB (6245445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4580af063012cf07a90f4c4deb394f146cdf7a02a156056e6bdfc9c42840ea5`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d6de5a32ceb96497a82ed7c607b87555825b7a60056bada7560264dde688fb`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea057aed6cb485a17c4bc68bdcc1a81cb4787ac1e05596faf20d1bfb1b86802c`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 91.1 KB (91127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f784639f20b4c216890d379aa5486b23ba801d021777b1a6cc9c39255a331eaa`  
		Last Modified: Wed, 04 Sep 2024 23:10:49 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eace15c747f6d6ffced917962585b4c110fbc7fb653d9b6c85a0e23f34046b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe746e3f282968ed6262d9350bcbac0318a90f681615ceff1ad8f1a1694be9a`

```dockerfile
```

-	Layers:
	-	`sha256:01346c0147987859ad6490f74cf8d191bc6fbcb44bcc43313726df86733bf3df`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 3.5 MB (3533320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:390a341ebc9b73743d3a5a6e4b1534734c72b485ad249e8411fd2931a60e476c`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e0fccdebbb4c3e1a4c51702d3bcfc7b8ef28c1fdba127fb501398b54b9d97be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59481178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078b3ce0bc1dd7b36af04ddc5cad250a918b6391f24707db77d6c92c9b0d3553`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
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
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb7ace09fdfd476fb95d4fd5a8a2edd7a9fdf7565c943ea7c1ee453011b5697`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 6.2 MB (6235166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af976523b1ff0ed7a6ea2d97619433f9e2ed6a36abcae442c116f36141f7c5`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe64922d76d36467a2655a19d8f70ca78b033cbb756a63287ef0050ee43aff9f`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ce3529f0b82b4882db3aa1ee50dd070dbe6994cf2242d75819e76f0acfed4`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 91.2 KB (91163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab7094a272c5f55af989aed29e9331e322fde90bcc6e6310d1f9cecf4f1bcd3`  
		Last Modified: Tue, 13 Aug 2024 07:41:48 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f7bc75943597ccf63423e01147b4cd0be252e263339ae1466d4530d5bf245fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311ff9447377aa2faf72ae51c9a8a6cdba678c8bf81924249c2ca218cae908a4`

```dockerfile
```

-	Layers:
	-	`sha256:60ef82002dc4188c276c967733bf3f7dfe6ed10afb436761e28b05f01c47748d`  
		Last Modified: Tue, 13 Aug 2024 07:41:48 GMT  
		Size: 3.6 MB (3561403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b732592ee34b5f02ad33eed797d157f745cb26004c31735bb1a7c10c88fb8e63`  
		Last Modified: Tue, 13 Aug 2024 07:41:47 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:549b82d1b0e5cd9c2ce9a9baf648b680a14c782c8f611235c31aca17cd419869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60436291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1bc6a4d38957fdfd69ea50f09f3ea43d9787658cdca31544d4d0141f6606cf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
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
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09f0177e0d45ab1a69528ede56e30ac3e58bde63bf62f2c1bf78711aec1b92e`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 6.6 MB (6565895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bedb0642cb91b6008a3795412ad5527c9838485628cdb532f1abb601b3d56e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a53b8f72283931b8920c07e7c2c39098475ff9658352fde012ed25e5ad75471`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a7d0317b5178d23dcf6d127c9d0af7c859e20d4bf21fb593b37a0621ab74a2`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 90.5 KB (90485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faf6db1b44baed2d5b9bb7695613c6daf5549c5f18f80473d873e346ffb47b7`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:969eb3d41b3528ee2d9433a5a63c75104060be0657ff8b63cacb1e505c8c89ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f8c1efe704d408b169c6fcfa592a13d6a9472f0e7b2e27b298560a24ff6281`

```dockerfile
```

-	Layers:
	-	`sha256:30e99b0a09798c571353fbc370f6f4dc9cec56ea7091480e8cad466438192439`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 3.6 MB (3557454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d0c3b412bb34261435220faf454f44ac6f6b3120cf906986b821f2d2229cb`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:8df4e760190f3184795b360080280ad5a9275765869d679e984ad3a1c798e6f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:835645ff640e0142a0d70b8be3ba4638a382ac72c67226aec4e8588ce4ec7c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390b61ad47378182770a2a820747040d768ff99bf0939b198a7bcbf4f0bf8a7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5889d68f1c611652a413d65837ee20352e00c59841d2e5610ea3b191b17edd7`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 5.4 MB (5360097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25867322675a948e12a50cceab4e3300713f994744099d783b76f2bcdd39e433`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4220848f077408718e98ccc6eb67e4ff521ec7a6b8ac1a5c1a5e7ca67120067`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6c8a677ce3bff8a9a3b154e868b1784552773f214318e5e082d655f2fbd1ac`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 105.2 KB (105183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:09d06e052405a63123040c809e203e9d109b16a84e402292d52bdc7b0a9cdef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d2f3d10af80443a7fa61073ec0bbca0f9204569ca94bf6755608efda7a9a5`

```dockerfile
```

-	Layers:
	-	`sha256:8390bd5dd97a5116688396231b0a1182a18e98fd8ca998f6d264b4887a7fd5a8`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 2.0 MB (2002638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8b174df4e6b1276ca0d9b68a50bf1f8929847cedeece4ea19afc63fcdfe78c`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c4f9d85053aa89e9a36ce96d6f32bcb36ebf1d565cf38f7e4350dfbc540bfaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b09eae5c93db890c880b065697968d7411fd7169e3f75e153dcd61251ed72bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0639d72092b592b944940eaba5264bbabebedc923c867d5cef204e3869370ef7`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 5.3 MB (5340388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e7d1c2d83050467ab223500a26d141bdd407ae0e6e93886431805ca3d5c22`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f6e4e6a296c9284d095ca5915669b150327bff81a93c81da40429350457fa4`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6afbc297c547eebfdff6b788637e32acc191d56ab28e1b571477510a8ca5b`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 105.2 KB (105231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f55c5bdee82b1c011271c0c624cd82b39488db7acde45dacbf7146869d0eea3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb2f2b3d0e9dcfe27d3b5ae0242c59d59b5c410d29417b2bf2602ee21d9fa8f`

```dockerfile
```

-	Layers:
	-	`sha256:9c7deba42a44262b8779a5b289447570c109ba28094ec8dd6ee5b71e08203334`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 2.0 MB (2002866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4db5f9492ef8ce64fd0b1771dd024422ff8201a3607ccd5adacb6fc086eac4`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:3656f68829b2a5609535626496a1f55d42f92f6ad8471692486fd8334d870e22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:77fb9130fe78863108f7f501050ece1197ec6cf54602ff9569dd579ec57a995d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4287e443009a9cf9c2c9cfa86bc4745d2830cc3142226f9126a0bbf43aaa68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378948ec170b4d8a3013772e2b302e397bab4c44a11f0249dede601a785f45d`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 5.4 MB (5360101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee4f8a5435dcf4efe8aacde9bf929bc80f51622561ec15161b5d4c39394aca`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64d92368b359bd4d2c8c5c9a1192171b7b95942fbdf86d66157667501827e00`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e974ec6725aeedacccfdc674af6fa00d862b362ac3de6d22e82ca6bf916d81a`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 105.2 KB (105186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0057b985c6f43e1e74cae2ce0577e1ad0efe4aeb67f205e93d151a20eac4ed03`  
		Last Modified: Sat, 17 Aug 2024 02:01:34 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14cd61596e92f159e820332529cdb62730d33f911883b4e531f9e077d0774eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e6bbd7493a8f0b17e450b95e56e5c0278a13b6bf21b0844d5ae3659ba50029`

```dockerfile
```

-	Layers:
	-	`sha256:5aa75864d011ddfe1d301412abd7aef31ee304f67b8490199d6b10e8c4a3e67e`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 2.0 MB (2002674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf80141cecef2fdf0bce1f92a0b845f40570df4d34b50dc495bc6a80235db9a`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d11bf39deaf7de11ad41c96cf537df477ed85d0488ffa697612bb126b5d753e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdae2cf2d82494d1a3621947569a205d1774d1d85071b3844ba1efabb720655b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0639d72092b592b944940eaba5264bbabebedc923c867d5cef204e3869370ef7`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 5.3 MB (5340388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e7d1c2d83050467ab223500a26d141bdd407ae0e6e93886431805ca3d5c22`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f6e4e6a296c9284d095ca5915669b150327bff81a93c81da40429350457fa4`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6afbc297c547eebfdff6b788637e32acc191d56ab28e1b571477510a8ca5b`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 105.2 KB (105231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c21685943f244b1d8bc574a86763d24baf01d135736926254f4bf33003932ab`  
		Last Modified: Sat, 17 Aug 2024 03:26:54 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd4d294f2b44f3421f9a91359180bad3483318ab42326f1f3d80b7b49255005e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2060d6c33f98e63c1d617787975ff356a667c174713e3c991f12be90bd367`

```dockerfile
```

-	Layers:
	-	`sha256:87d77a954395223ffbab79c701033297186c31614e438db57959086ac47e7690`  
		Last Modified: Sat, 17 Aug 2024 03:26:54 GMT  
		Size: 2.0 MB (2002902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250b5817ba7362a6358206761a137e7ef32ace96b20f593c8fbc72b107287182`  
		Last Modified: Sat, 17 Aug 2024 03:26:54 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:c76cdb697e932bd1ae56b61482e6d88224ac8b9a88378a4b86ffae71b7371ebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:eb6c223a4a1a531b8bf95075d38c51152a0ff2e2a2bb81abb345135f64cfd25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bf875c9a9f9ccf9291fd353336bc8786a19878fac26ac669a87ba3f3dfb484`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a52ad96cf081ad99e55f0ae7da8287d3ab9e67b73b6a19de653dd1f36a1b43`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 3.6 MB (3622800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3243246bb56a63815d22e9ade9a0587c7e1d13022048e8499dc45f5571c6c905`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e820e921f70036b4093f941d63cb1544549093de2b85c8e4cb082b1bf63066ea`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343e179ce49c74fdc934bfbb8a6a84b0f0d5341974248fb92fe7bca3ef25c970`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 110.2 KB (110155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52c3b54434ac146657c5403d09bf482796ab6ba9a4f0a2b37144a53e6ea26041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa3cf2bbeb0b8167478ff916145f77e3296a568b8e70e6b866711d184d05c9e`

```dockerfile
```

-	Layers:
	-	`sha256:c051b4ac90a6dee339f319c6b8ffda7f8091567918686d946831aed82bf1045d`  
		Last Modified: Sat, 17 Aug 2024 02:01:45 GMT  
		Size: 2.0 MB (2041055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45466d6ee69840024e3f90d1ff6914bd5dfdbab1d6746091fdcc8fdc5ad00617`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c0be1982387e329151c748e23b1d3b432adddfadf32f4894ef963ae2eee02ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed49370c0d1c5ff9d6ac073942dbfbcd7f2955aa3bf492a590ad95c39fccb81`
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
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ff02d894ad8e635c681df9ab272273ee6ef6fc2de761dac177e4b08a7996e5`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 3.6 MB (3594216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbff8da0ddd5b0063079b89cf8dea9d21d2d6039ad2dc20c8077cecb4a6982c`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce958e839238ae37a8145b798126f2f38ac17755e85d50b2cf84ed1743fcff9b`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5492c71801d75cd5ec1c6a42e5e6a93410815c737e19793eba12356e09ea3f5a`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 110.2 KB (110195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c3f7d9652103e03397e3c9d96e94b427eb2fd796ea3bee960a4e4ea1f5607f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536afe5b7b22b4796509887811eb8360adffdec15e902c171354c65c5d49ab9a`

```dockerfile
```

-	Layers:
	-	`sha256:ca275407384afacf5f4c06700c6fb1e1400710c24ba43331cb43ed803af825aa`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 2.0 MB (2041314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a3deb8f03cf9268d0c4a1571d227c850fed332c63e7ed8c63963349199ec26`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:69000b4b82130c86111e2d6f2154e383374ca25200434d36c35649a4e5559d0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:56bd533555c24b1a0e33d8715b923991f52a2390e718cad615e3bff0515609e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33271295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3566d261905df20f6cb67de2e2b0f1a5e5c36a0a5d60904a443b38395ad9a`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cc7342a9101f7bd65ee11e85877b5167401a573496bc13b0254de69412ecc9`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 3.6 MB (3622828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698948cbfdbdb47f46cfa18f153db97f0d4185b2ed0b0ffa4ed7241dd111275b`  
		Last Modified: Sat, 17 Aug 2024 02:01:54 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562faec9eff170ec13a317ec590e7fc5d2465196653271ad94727e25bc8311b7`  
		Last Modified: Sat, 17 Aug 2024 02:01:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1412ebcbb56620affa88dd6fbb7e39dcb76e6bce53dbfd670137f69d3f2c974a`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 110.2 KB (110191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438eebc3143823b29528449def844b428375d64ee9196d47b83fb4c4122f9bd8`  
		Last Modified: Sat, 17 Aug 2024 02:01:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6614b7ddcb99ae1b7fa0467afc9700f61781c0689f09b79056afdbbf11d8bb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f79af39f0b140321d5d479f607c4990268d1a5ab84e40cd385f7604fcdff53c`

```dockerfile
```

-	Layers:
	-	`sha256:a6325c5e50dcd50ef9cfaea30ddc8a7cdb33eef4646621328bb6e914d10778b8`  
		Last Modified: Sat, 17 Aug 2024 02:01:54 GMT  
		Size: 2.0 MB (2041091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e92bff7835cd7b5a49eaf89dcfdfd1235e8355f81c4e637cf643075199c3c8`  
		Last Modified: Sat, 17 Aug 2024 02:01:54 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ab895a10b5c2a35700955e7ad688cb39c99dd1fcb1ea8906d533b55001376066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b09dbdd8f2ca864eb51b667cf425f880a87f413fc2e08b365de111f19009bb`
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
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ff02d894ad8e635c681df9ab272273ee6ef6fc2de761dac177e4b08a7996e5`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 3.6 MB (3594216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbff8da0ddd5b0063079b89cf8dea9d21d2d6039ad2dc20c8077cecb4a6982c`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce958e839238ae37a8145b798126f2f38ac17755e85d50b2cf84ed1743fcff9b`  
		Last Modified: Sat, 17 Aug 2024 03:27:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5492c71801d75cd5ec1c6a42e5e6a93410815c737e19793eba12356e09ea3f5a`  
		Last Modified: Sat, 17 Aug 2024 03:27:25 GMT  
		Size: 110.2 KB (110195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5169b924b8deb541b69bbd51bcd176c029d87d47bdf518075b1d5cc550920da`  
		Last Modified: Sat, 17 Aug 2024 03:27:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4256e963e77ea1a32c5205e91bbf733bba06be857f47f92aaec98fddfd81b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6d8b3d855e98e05ceb76c4bba59772e02bec8429df2ce8ad73eaeb061688d4`

```dockerfile
```

-	Layers:
	-	`sha256:bd47fc093378bbd2d7d030d9958582ca469738dbb00b645373f2e8614f9330e0`  
		Last Modified: Sat, 17 Aug 2024 03:27:44 GMT  
		Size: 2.0 MB (2041350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e288de02dab95dfcf208aec0315505ec789648e1f296f5c8442a717a72536d1`  
		Last Modified: Sat, 17 Aug 2024 03:27:44 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:a908af3ab83cc5d9c73ca04238c205dacfa345725fd39407d05ffd0f2862bdb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:65a5e2974b0aaa455cd8086522e85ca0a75d8172eb709171124a006808075dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33364069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aa938c91a54d1af641aefe5ab65eeb9969bffa515852163ec1f1813f4b824e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Fri, 21 Jun 2024 21:57:43 GMT
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb8807969871b2c4b743c77f4912b4b21dc86097dc565259c30af63d927a991`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 3.6 MB (3556392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c985848f8839ae6a5165d0492e3943f69a02bdb43947aff82815c86e5268e5b`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09ae3303e9e268919e3dea174637e2415ad4260b94a0686c104212c7311448`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206c0e1406b7821b74ce08bf2d21539b2f923b77885dc92d0cf6e68f69c7e6a5`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 99.4 KB (99387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7f8abf19ccf794b476b9cc9235a3d5353ed9f26401fd60b4c4daf0f30a47ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1983271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71f7b998fbff639771bbcb71893061e445002631210e1c0473b5cdf980d1e2d`

```dockerfile
```

-	Layers:
	-	`sha256:f97efb5f6d79399921e66ee5562d4013736b8ca73dfb3ac07e83f12f0e9cb8d9`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 2.0 MB (1969866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5544deea3282c14e3460c150698a2711e9af96697d5e0cb03183aa6db8275cb5`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 13.4 KB (13405 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:86a3e2d223356960b9952d6a86808c281327c2977ddcc2623b8383255af4a902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061747c12250a93fe68c0429f37e2e4fed5df6135cc5d60b3d7e11daee0e2a07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c4e01a43dbc7c416a9b731fa8f8bef88fdfc1df080891d0652278f413d6af1`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 3.6 MB (3556261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d895792661c41dae2383215cbcff1f49b37e1c60169903b6857813e7aae358c5`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715c1819824070a2de32ff43c09f4f54855f57bed50f1a23950b315f213a2cb`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eceb2198dc6b8c608265e9db97ab61c4fccb468c896eeeb53acae5013f8012c`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 100.8 KB (100804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cb46cc29c8712b8fe60376d736e46fe5a9b351ef3c4f329995ae47470f85e08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1984594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1aa0a641079880321ed2bd5401af6beb2a9d217290367858789210729129a5f`

```dockerfile
```

-	Layers:
	-	`sha256:24d4c15573fa35d52017d8f45ef6fd47bec3dfe64e09af71435434a7b0d1b346`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 2.0 MB (1970911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29306a825e41f71e4df2dae831dc0994d951ea31cb9dd42aa4645b042c4feff3`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:04b003e94882fc0d57a121d3a99043e54136f58bb3ed3c08f6d0c4a3506b50ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d0f6dfe87bbf8ff3295f2d135423c44eabfb1c4b392d6ada2059c0a45b81e7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33364503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047f55e55f45f90056bf1c191035119e95b8a947a36111ea84cd40486235b18c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Fri, 21 Jun 2024 21:57:43 GMT
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253a770aa0fc4016ae1d0aedb821108155cb121ba2904ee0cbe1a59270ea7b6`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 3.6 MB (3556420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97354b5ce0775796dd2556e209a2be2c064e05c08ce8c0689753ce114b7f249`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d70d49474507b5a745b369f6eb1308de52532d725ade76270bda595f5b2ab2`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0546cd37d40811ea9d1b41251d7450551d20bd67b010734b2ebfd999fb62e53e`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd391e5835bd5c8c86c1ff6a15a6945f9f5eb054e79d208fad6da084c130cba`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:499fe167d207a9f2462b61c96c635673ddca40546760f1b6e302cbbf46a3718d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1985536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cf56198fb469d7486a3228975922b4a4c876b15517113e726ab87c503632c2`

```dockerfile
```

-	Layers:
	-	`sha256:a90baeb8a1f9fbd63a1e77933ae75c90ddee8f43449eaae163d112828a30fb2a`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 2.0 MB (1969902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cfe40256999ad436b928bfb8935f5a01ccc87d2e84c36d9d6f9b3802ac8c0f2`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 15.6 KB (15634 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:12e5fd4eccd8be6c8ff17ccb83f60d4899f69f18b87d6bb7e994ea8a8b5e6160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32503146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9da95c355c644183351c4bbf5babd41bb03e09c8e6a1ff0687e4a2fe974e74e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c4e01a43dbc7c416a9b731fa8f8bef88fdfc1df080891d0652278f413d6af1`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 3.6 MB (3556261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d895792661c41dae2383215cbcff1f49b37e1c60169903b6857813e7aae358c5`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715c1819824070a2de32ff43c09f4f54855f57bed50f1a23950b315f213a2cb`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eceb2198dc6b8c608265e9db97ab61c4fccb468c896eeeb53acae5013f8012c`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 100.8 KB (100804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e7e0833c61fae1324c79ab32b990e9e29fa9951223bb911ce4e472b1f01228`  
		Last Modified: Sat, 17 Aug 2024 03:28:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:03b10c26fa149acdf00d9712df4691c9fc361f59db6f82da757a681c7ea514d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1986860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4409bb785dc79c9abd78fdd0e26497d7d202302a79268a662eb23b5832635bcc`

```dockerfile
```

-	Layers:
	-	`sha256:417e1857fab43db3a8f9f3c2d1fc22abbe629c9856b33904701b61325b787ed6`  
		Last Modified: Sat, 17 Aug 2024 03:28:36 GMT  
		Size: 2.0 MB (1970947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87fafe055ed3126f285391c8078da181ef1135026442bf4b3f1cbc1b9daf793`  
		Last Modified: Sat, 17 Aug 2024 03:28:36 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:a908af3ab83cc5d9c73ca04238c205dacfa345725fd39407d05ffd0f2862bdb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:65a5e2974b0aaa455cd8086522e85ca0a75d8172eb709171124a006808075dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33364069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aa938c91a54d1af641aefe5ab65eeb9969bffa515852163ec1f1813f4b824e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Fri, 21 Jun 2024 21:57:43 GMT
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb8807969871b2c4b743c77f4912b4b21dc86097dc565259c30af63d927a991`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 3.6 MB (3556392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c985848f8839ae6a5165d0492e3943f69a02bdb43947aff82815c86e5268e5b`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09ae3303e9e268919e3dea174637e2415ad4260b94a0686c104212c7311448`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206c0e1406b7821b74ce08bf2d21539b2f923b77885dc92d0cf6e68f69c7e6a5`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 99.4 KB (99387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7f8abf19ccf794b476b9cc9235a3d5353ed9f26401fd60b4c4daf0f30a47ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1983271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71f7b998fbff639771bbcb71893061e445002631210e1c0473b5cdf980d1e2d`

```dockerfile
```

-	Layers:
	-	`sha256:f97efb5f6d79399921e66ee5562d4013736b8ca73dfb3ac07e83f12f0e9cb8d9`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 2.0 MB (1969866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5544deea3282c14e3460c150698a2711e9af96697d5e0cb03183aa6db8275cb5`  
		Last Modified: Sat, 17 Aug 2024 02:05:20 GMT  
		Size: 13.4 KB (13405 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:86a3e2d223356960b9952d6a86808c281327c2977ddcc2623b8383255af4a902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061747c12250a93fe68c0429f37e2e4fed5df6135cc5d60b3d7e11daee0e2a07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c4e01a43dbc7c416a9b731fa8f8bef88fdfc1df080891d0652278f413d6af1`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 3.6 MB (3556261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d895792661c41dae2383215cbcff1f49b37e1c60169903b6857813e7aae358c5`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715c1819824070a2de32ff43c09f4f54855f57bed50f1a23950b315f213a2cb`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eceb2198dc6b8c608265e9db97ab61c4fccb468c896eeeb53acae5013f8012c`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 100.8 KB (100804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cb46cc29c8712b8fe60376d736e46fe5a9b351ef3c4f329995ae47470f85e08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1984594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1aa0a641079880321ed2bd5401af6beb2a9d217290367858789210729129a5f`

```dockerfile
```

-	Layers:
	-	`sha256:24d4c15573fa35d52017d8f45ef6fd47bec3dfe64e09af71435434a7b0d1b346`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 2.0 MB (1970911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29306a825e41f71e4df2dae831dc0994d951ea31cb9dd42aa4645b042c4feff3`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:04b003e94882fc0d57a121d3a99043e54136f58bb3ed3c08f6d0c4a3506b50ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d0f6dfe87bbf8ff3295f2d135423c44eabfb1c4b392d6ada2059c0a45b81e7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33364503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047f55e55f45f90056bf1c191035119e95b8a947a36111ea84cd40486235b18c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Fri, 21 Jun 2024 21:57:43 GMT
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253a770aa0fc4016ae1d0aedb821108155cb121ba2904ee0cbe1a59270ea7b6`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 3.6 MB (3556420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97354b5ce0775796dd2556e209a2be2c064e05c08ce8c0689753ce114b7f249`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d70d49474507b5a745b369f6eb1308de52532d725ade76270bda595f5b2ab2`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0546cd37d40811ea9d1b41251d7450551d20bd67b010734b2ebfd999fb62e53e`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd391e5835bd5c8c86c1ff6a15a6945f9f5eb054e79d208fad6da084c130cba`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:499fe167d207a9f2462b61c96c635673ddca40546760f1b6e302cbbf46a3718d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1985536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cf56198fb469d7486a3228975922b4a4c876b15517113e726ab87c503632c2`

```dockerfile
```

-	Layers:
	-	`sha256:a90baeb8a1f9fbd63a1e77933ae75c90ddee8f43449eaae163d112828a30fb2a`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 2.0 MB (1969902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cfe40256999ad436b928bfb8935f5a01ccc87d2e84c36d9d6f9b3802ac8c0f2`  
		Last Modified: Sat, 17 Aug 2024 02:01:37 GMT  
		Size: 15.6 KB (15634 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:12e5fd4eccd8be6c8ff17ccb83f60d4899f69f18b87d6bb7e994ea8a8b5e6160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32503146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9da95c355c644183351c4bbf5babd41bb03e09c8e6a1ff0687e4a2fe974e74e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c4e01a43dbc7c416a9b731fa8f8bef88fdfc1df080891d0652278f413d6af1`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 3.6 MB (3556261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d895792661c41dae2383215cbcff1f49b37e1c60169903b6857813e7aae358c5`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715c1819824070a2de32ff43c09f4f54855f57bed50f1a23950b315f213a2cb`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eceb2198dc6b8c608265e9db97ab61c4fccb468c896eeeb53acae5013f8012c`  
		Last Modified: Sat, 17 Aug 2024 03:28:14 GMT  
		Size: 100.8 KB (100804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e7e0833c61fae1324c79ab32b990e9e29fa9951223bb911ce4e472b1f01228`  
		Last Modified: Sat, 17 Aug 2024 03:28:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:03b10c26fa149acdf00d9712df4691c9fc361f59db6f82da757a681c7ea514d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1986860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4409bb785dc79c9abd78fdd0e26497d7d202302a79268a662eb23b5832635bcc`

```dockerfile
```

-	Layers:
	-	`sha256:417e1857fab43db3a8f9f3c2d1fc22abbe629c9856b33904701b61325b787ed6`  
		Last Modified: Sat, 17 Aug 2024 03:28:36 GMT  
		Size: 2.0 MB (1970947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87fafe055ed3126f285391c8078da181ef1135026442bf4b3f1cbc1b9daf793`  
		Last Modified: Sat, 17 Aug 2024 03:28:36 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:92b6eb86e62a3a40e533bddba7e6ba36aed887e0ac522a884548625d92be5637
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
$ docker pull neurodebian@sha256:847fa5b5f7cf1bccaca954bf29c9760f6e50b0d341c1fc9922e71b16a107dcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60918838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d8b68cc7b03f4463b38a4b84766e653af6f629425f8dc9da21a01905f86c41`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cff9496b0f02716173380ea8121b9e078fc273f6d7523b800d9fe735b5dd1b`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 11.3 MB (11266595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5983ad1294ee53f6d8da2393360eac5f051d3bc0b588717c0d4cd3e142217c`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf285c1642ebca0cc13aac597170ef3a5c579a105f0f92629069f4832450ad61`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed44b93503e6a3d93bdb96a16f03e2b54bd73a19da0bab6380ba0ea3510e5cd8`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 93.1 KB (93123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fac7a70a3b2ea3f16e625c5ce0fedc502786c081db5610946a45da1b8ab44c2`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e24effabf132ff5cdc935ff05cd29e117b0bf3205036161440b7bbed70d99ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52f163fc775a474972895d85969b53cfac0fff58bcd49825409af99d1bef98b`

```dockerfile
```

-	Layers:
	-	`sha256:398cb201c6629b1fc0c304b57e8d35385ba361d53e29d7c558217a80617152e3`  
		Last Modified: Wed, 04 Sep 2024 23:10:44 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223b164f125eb0ef2acf8dfaff4c3934e24cfec268650cb9bef3c76614f46ab9`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:761fa3220c10853beea131741907ee20e70ec4521ac8bb053ed3102cc2c2f107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c6a24608f1cf51881701b2548227ae1a0c126c6ad59c7c32ae3e326410aa0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
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
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6516de16487e13fd76db87360111809c44b836a1dd673fa8de93b983583728c`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 11.2 MB (11232114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6108c7a663d245cb0932ddfae87f92ca3e1de7fecebcc1c63ff8508adf4e6db8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08a498a3c3c4bf8a5ccf542b868e62921588d0f25c6cc09bac0d6a005711aa2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e20e8cb909fb4d46a63b2053a3a0c458af529d893341a678b2c4b75796cb9b2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce457b9d5bc4664f2ee4fea10d635db111976ec6879c1d1b65c5f2583dbe5583`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:faf07f81a060067adb199891ec5a55de7b6b552d9e1425f1af3d811264f4ad67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b630765608bbb9375212b2673d9d41627e2f3fdad5f8105e334bc40f372814b6`

```dockerfile
```

-	Layers:
	-	`sha256:b5b0a3582701ba2dfcab416b724d504cf731b6eba018c782d7f8f980f48d5880`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2796e687428634d360ff415826bf00c056a4a1fd7916d81eca260088e413ab5a`  
		Last Modified: Tue, 13 Aug 2024 07:40:53 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6dda59b69a60752417dc53a7da8941269d242b1e51024eefe430dc3c8678535b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62364011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6544912638a3d685fb71af9ef012ae48702e550f4eacecadc34616be26b1ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
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
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96a775276b452d08188a5c8cefb2671c2351befe343f1b71ec2831ff494f794`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 11.7 MB (11688976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cba750c7d48374c4a665b3aa6dbc0d35907c8f5351297534109e7710fb5c1f`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f40691f5b23aab625dedc59cb84165c3346c956f411c37faab61829e98875`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f559b7b520cf1d9f632d590f4a76abef8d20d19ee766429dd08dfd1c710e99d`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3984a8ad3a3a24cb4c87f0a2b5e7d680ee45cfce31b1e5cd4e4f20f1155943c`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ef44f9fdf0ade8b16b042df566cce5c0d994e196038e8dc7afac19802fe5532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132b918c3187bacdd483261bb47116c101b17645636f69910a6307417710fc41`

```dockerfile
```

-	Layers:
	-	`sha256:46ddedcbc2ee5bb19f1be63bafb03eb6792a0d36311f43bdc4abca7f7d714bba`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b55d3c3b9f45b61d2f39e46bd54d2650bf8f8a7462f64277466dd89f98889a4`  
		Last Modified: Tue, 13 Aug 2024 01:12:04 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:9e085870cb694cf3b669663a1b243a092c0b330bbafd92c3d7c01682ba8ca0d1
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
$ docker pull neurodebian@sha256:d5b072a5141a86dd1d2500e0c66407e895b6a7cd02772fca2ad2953e01036964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59510892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986472010412306b6437bd6a1fb9bdce5785924d8b5f20a8a1208d6c5635ee52`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
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
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034bc937277199ec164847356d05777d74634f8f5f05723bd208cb3eb6138b78`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 6.3 MB (6260893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b77db3a43cb43615e3531865bc65936809125b4da8289276926163d9c2d30d4`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f157f39a62fa798f416a12a4fbcc54c4d50bd039d2428ab32c79c125e0c5874`  
		Last Modified: Wed, 04 Sep 2024 23:11:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f02174b8243c9482bc3bd0e6ee8f3ee77adf56b32417414cddb12cce0e13f62`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 91.2 KB (91162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1717a43a3dd14a94d30142710e223970593b56d0f5309f2ee6294f49cda02ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26637a4026d86d363cc068a6499ad746ffd2cbb35b7e93097653df757a8a92b0`

```dockerfile
```

-	Layers:
	-	`sha256:9c5747490dd0983fcbe9f53c25f5f90cfa0b682f70fd6b32283a230b556d8b4a`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 3.5 MB (3532460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8625fdd4ee91d417fb4bb1b9f41a818c610a6e5b6b07f6806186a3aa72e0def`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 13.4 KB (13397 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c24554d2b03c88038671f7dd363e185920cb2c3d56fe292a23a6b5316ca9e5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59483897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25afc236d3afba5d4a0961256a2b5fbfcd0bc83d16154e306ed3f4ca8f718d7c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d3aa31e5e33290bb28cfd74e2b2a88ce7e4415dc0d995c3c39d36c332bdbfcf in / 
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
	-	`sha256:543c0d8816b61b146fc103b18d6ec335253cba7bad9fa7f1cb3e794a6b9e450c`  
		Last Modified: Tue, 13 Aug 2024 00:44:13 GMT  
		Size: 53.2 MB (53155250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02191b116647481476d52030a803e28ba5e68be75a6620aa17907059437da993`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 6.2 MB (6235299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49fc1a3149682d8a81b651e3c53dcdbb45d3ae5b19c1abed966b8e7ff9ec25`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f53b0fdfbf88451067600990b58000941f44e8fb25d7f56a2040f4c02e5f88`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab9ebaf49832bc2e70ff76ed23a0cd70d02d5b8c5853db5f86181077c727f6`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 91.4 KB (91368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:565ddfc6af473f19ecdd32e26652054091c8686db3a9e305d6c86b6dbfee0622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8188b1f100e1b01a87195c48287ad47b85c7865a2ce5a2a8226ff6f5ddd1f6af`

```dockerfile
```

-	Layers:
	-	`sha256:06f04d1df7ab382a4d8f77d2d144bf4aeba6c4ab3fafe199d4e33a6bd92251ed`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 3.5 MB (3533440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b4482dded10009090fd2f781e3e4583a565934f8b5e80fcdd3e3a36123f242`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:2d7295e78c1f93e93a2fafe3cf5d6578c9bd04ba3e70aeb1ac00e4ab6a423853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98da68791e8c85b2337b5ace3354f2cf5c2661f1890b36c48faa684596d1a893`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
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
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0659bfc4fa78a1d35cc72364a5ae98ac8f4d07bd69d5519d26f5a17cb400a074`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 6.6 MB (6566071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8727d0f61d96321e8ca009fce720e24d7cc8b2eef994ca6bc4de03fca1eec706`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a36b20258ae61eb5dcc9eb1db3b6f8b4cc8dd1758e38b36d1ba0854ca92f`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08afb7bac914d3affff0a203687d081a71dfea865fb144968f617538c675d23`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 90.7 KB (90690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a550bba3856e784dc5634debe1d9eaa3713a572c52b7a21ec54d73e0c2cf13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab79690e1cadf319dd8b38d9a493570fc9e9c614dacf0dae87dbb78b2feacbdf`

```dockerfile
```

-	Layers:
	-	`sha256:1a0d28cdbf8efae3239dea7c48eb32f819b4f35eaba78d926a86bda35ae7add8`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 3.5 MB (3530303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c286a639d57592fa8d3072963de485396b9c4aab261687c908e99b643ae588`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:299a54ccfcf4ed7b643740603c1abf80e811c5ee8215e3065b305e8fb0ec9dcf
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
$ docker pull neurodebian@sha256:26a59f612ed56a4697f366a60a77194f5641af54e9a1664a020ed586da6d71f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59511253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f2ad76884e7f344ab5b0e055a2b96cca37774aef8be383075916292182c8af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
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
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2c007c64da352ec00a7c770959f382104c4122028f01d19283f85f7c5196e5`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 6.3 MB (6260869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e19ed26657edb9a90abf530ae502f28e31e1fcceca1c8faa0c42eca3a5984c`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d3b2c132c8026f38909d51e7a45f40fa7d65bfad4af42b8ff1cd3cae31b32`  
		Last Modified: Wed, 04 Sep 2024 23:10:59 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5389944352d641fbf5d89602026b8119d8cf060cbdac213da804dbba99554b2`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 91.2 KB (91154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a05ede3e7172d449e69bd39da700fee287c4bfcf237b04a327d7c64236ff83e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bc86531131eff71b8b0308bd0c49133fb6956878d87c78527fb4d8c92332daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c70794af3101644cfd9922da9e9cf1d6e31f20c36f21ce04b23f581344a9ef`

```dockerfile
```

-	Layers:
	-	`sha256:2dfae5164f018ebc1798d623dbc99edff836f35311794491eaf4a62521db0c5b`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 3.5 MB (3532496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155d36edcf9182b5d9cd047985eadbb745b640d0e8d69fb82d6ffba6986d16e1`  
		Last Modified: Wed, 04 Sep 2024 23:10:59 GMT  
		Size: 15.4 KB (15428 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7f830e4e2c2d4d6fe4727b5f3c67cef86820ab5773bf9fefac3d72d524451a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a40f7d644f46a12c3166e7f144ef587ae0b9d775bf582804a5923c9540f11c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d3aa31e5e33290bb28cfd74e2b2a88ce7e4415dc0d995c3c39d36c332bdbfcf in / 
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
	-	`sha256:543c0d8816b61b146fc103b18d6ec335253cba7bad9fa7f1cb3e794a6b9e450c`  
		Last Modified: Tue, 13 Aug 2024 00:44:13 GMT  
		Size: 53.2 MB (53155250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02191b116647481476d52030a803e28ba5e68be75a6620aa17907059437da993`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 6.2 MB (6235299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49fc1a3149682d8a81b651e3c53dcdbb45d3ae5b19c1abed966b8e7ff9ec25`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f53b0fdfbf88451067600990b58000941f44e8fb25d7f56a2040f4c02e5f88`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab9ebaf49832bc2e70ff76ed23a0cd70d02d5b8c5853db5f86181077c727f6`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 91.4 KB (91368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c01f4db884a7e9e5e03a2c3a4f148b5eae1fd576626b29c6eb6ec84ab7abcb`  
		Last Modified: Tue, 13 Aug 2024 07:42:44 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f7a4d4e88328b2a38b7d20e94dc0f3436ca1ad4f9d60b0c983d6c2f136e7ed18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97881e2fcfabb0b2c1d5bbdf55f7996e98f77c400d6e133a047a29729f74e0e6`

```dockerfile
```

-	Layers:
	-	`sha256:346da81b252618de9c218de26e73488c09966414f4b1c0e07c5e8b3c58bba1bd`  
		Last Modified: Tue, 13 Aug 2024 07:42:44 GMT  
		Size: 3.5 MB (3533476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52f58fee8fab48fa3131808e449368a6cda85d7f168728764bbfdedbf9d3ee`  
		Last Modified: Tue, 13 Aug 2024 07:42:43 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3879645d8248e19c7cecc51e81e443dd2244460b4f358cfeb57cb286852c04a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb0d7cc60a97195c40904e7573f816efef7d6f12cc2155af4cfb3e20b788da`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
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
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b71d132a4344bb16e2e09fd83117250f48d572c643b3a712f89502bd494932f`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 6.6 MB (6566180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b92d44337ab2e36cf50dbb0e5f5a982aedb8ea031edfd566ea77794b8600db`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83d54a7d8728387f810ef105293ffd3ecdbe46c909d35465dd6ac692a203a66`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c86223c48237f67a081fdc1da5b575bca1e0b24ca39b18348f604b229ec46a`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 90.7 KB (90739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c730d96f05d4551706957182b16dc3e0b695f848bc18e53ac8a87794f7bc71b5`  
		Last Modified: Tue, 13 Aug 2024 01:12:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:afa48e552f3090b92141c3f16761ea91ebd9c37674b87f9131690f18413b23a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc69503183698682084ccc15450c076f8942d02054a333aa86200e39f668a11`

```dockerfile
```

-	Layers:
	-	`sha256:d17136678b054f4bbd69c0d37627fc779e2d83be22dc0d59ec71ef570984beac`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 3.5 MB (3530339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1d4f4372fabf850ce1ffa73ac663ea1660175de7920a8b704f09006156321a`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:5d3129afaf9a1323fe20f7229e24f8d783577c51d4a4efee558a2fde23f60936
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
$ docker pull neurodebian@sha256:a546d8ed9ffe1cf9bfaa5f41e6990494d4161f32f71c2912d6ff8a323fd891d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59491484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf42119ac53bfcf848e5c69c4b517bd04ed962dfe730d51ec7ae87855959ee1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
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
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb4d57c723071fab9db60a4db2147e17aa66dc83d2eb2eaa6d6579487ee0405`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 6.2 MB (6245441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5983ad1294ee53f6d8da2393360eac5f051d3bc0b588717c0d4cd3e142217c`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f5e26a0664131c25e2eec527fbcf80640e1dc3a81b7a9f1070f1b76dbfc976`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f414c1a656a41c98a86a7e5ab714d0c744b0d0e057887321cef5c818745e553`  
		Last Modified: Wed, 04 Sep 2024 23:10:43 GMT  
		Size: 91.1 KB (91108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:90095457c2c3217e470366efd9f555dc4106a4f43a068b16fda1a15a50cfe397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1dd60de3b0104390f365e269fc3dc0c0f82664e1ce82ddb3bc0504bdf434f0`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3bd20bfbe30fc6feb1760c58ab8f8348ba270666600d2970d9d6f00bf0e47`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 3.5 MB (3533284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f3317280d884cdafb352868dd83567052bbb80f73737cf10ca00dbbff1c8a0`  
		Last Modified: Wed, 04 Sep 2024 23:10:42 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4902d30efab700e1e0e7523ad44858bd58a9039c36ac78d7c66275ab9b3cee2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59480755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daccafc1f00787667713fbdf34071b12f94780c42ed253bb68afc7b749d22869`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
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
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb7ace09fdfd476fb95d4fd5a8a2edd7a9fdf7565c943ea7c1ee453011b5697`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 6.2 MB (6235166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af976523b1ff0ed7a6ea2d97619433f9e2ed6a36abcae442c116f36141f7c5`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe64922d76d36467a2655a19d8f70ca78b033cbb756a63287ef0050ee43aff9f`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ce3529f0b82b4882db3aa1ee50dd070dbe6994cf2242d75819e76f0acfed4`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 91.2 KB (91163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:89a4a17aa7e58a5b71aa52e99a139b5b58f4b64bb4d7f6232dc569fccfc738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9ebefda3efecdb73baeba3204318196ebce232572ff0bc926c70b78d5354c0`

```dockerfile
```

-	Layers:
	-	`sha256:844f178c4ab0992a80f84dca8dbb6ce33a4411dc7b869065ab23976c51f13e50`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 3.6 MB (3561367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdfd21adf8224349c32874c3825d25d8472c8564d30be72e731e594e359c63b3`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:2917d3afeb3fb636e12940beb6791076a7cca7bcc9323f0d210d2eb049517a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60435962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162543759a640728d99080bc6821ca27f669e5e6d2f194830250fa18d7d5ab66`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
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
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07041f7523e0901d7c47895945c0bd1cacb4692d4614b1ffdbe05fa57e01e4df`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 6.6 MB (6565982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca643e5a596b37baa07257045ef13923dcb3596dba7f1d83275b23371f8122c8`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248be0caa7517a9fa8f3ceae041a4a546ee6ffcb5a8e17da61311b64cef0f39b`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465fec9852b0db92fca39606004e3da1bff74c315b4ba1a49ae6f98bd4ce588c`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 90.5 KB (90497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:194159e51e60e4cd446bc9871b2b9dcc9c1939ec0cb8ae4a5be2d10f5da5b5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da11e8ea5815e2cc0c24e8b7a74d6610b60031b2503f72b6a45eaead60b0e0d`

```dockerfile
```

-	Layers:
	-	`sha256:214c5fbd9973ffc5415fc3aeb6b5c3f3dfccbd6b98cc07ce869780e51832b773`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 3.6 MB (3557418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b25cf0ea84c2e63b9d10044e8b28a910dd9082e4e5f6fa9c44c115d782f698f`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:fade21252c86f3a8878c4435f1307a63b1ed258def3b7fb11f01a6d2b8fb2cbe
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
$ docker pull neurodebian@sha256:82e474c2ae8e21c50a816ca8623bd88bf10f268ef4546821dfabcf820e0bf1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59491933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fec2a1fcc57d10ea266a88d73ea6e17c9ecd09671b8c84fff39ae6cf7a2f9fa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
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
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb091556b81f4904845d65b2153884d581ad6cbbdac107a2f862a6707fc5218e`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 6.2 MB (6245445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4580af063012cf07a90f4c4deb394f146cdf7a02a156056e6bdfc9c42840ea5`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d6de5a32ceb96497a82ed7c607b87555825b7a60056bada7560264dde688fb`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea057aed6cb485a17c4bc68bdcc1a81cb4787ac1e05596faf20d1bfb1b86802c`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 91.1 KB (91127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f784639f20b4c216890d379aa5486b23ba801d021777b1a6cc9c39255a331eaa`  
		Last Modified: Wed, 04 Sep 2024 23:10:49 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eace15c747f6d6ffced917962585b4c110fbc7fb653d9b6c85a0e23f34046b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe746e3f282968ed6262d9350bcbac0318a90f681615ceff1ad8f1a1694be9a`

```dockerfile
```

-	Layers:
	-	`sha256:01346c0147987859ad6490f74cf8d191bc6fbcb44bcc43313726df86733bf3df`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 3.5 MB (3533320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:390a341ebc9b73743d3a5a6e4b1534734c72b485ad249e8411fd2931a60e476c`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e0fccdebbb4c3e1a4c51702d3bcfc7b8ef28c1fdba127fb501398b54b9d97be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59481178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078b3ce0bc1dd7b36af04ddc5cad250a918b6391f24707db77d6c92c9b0d3553`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
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
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb7ace09fdfd476fb95d4fd5a8a2edd7a9fdf7565c943ea7c1ee453011b5697`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 6.2 MB (6235166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af976523b1ff0ed7a6ea2d97619433f9e2ed6a36abcae442c116f36141f7c5`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe64922d76d36467a2655a19d8f70ca78b033cbb756a63287ef0050ee43aff9f`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ce3529f0b82b4882db3aa1ee50dd070dbe6994cf2242d75819e76f0acfed4`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 91.2 KB (91163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab7094a272c5f55af989aed29e9331e322fde90bcc6e6310d1f9cecf4f1bcd3`  
		Last Modified: Tue, 13 Aug 2024 07:41:48 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f7bc75943597ccf63423e01147b4cd0be252e263339ae1466d4530d5bf245fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311ff9447377aa2faf72ae51c9a8a6cdba678c8bf81924249c2ca218cae908a4`

```dockerfile
```

-	Layers:
	-	`sha256:60ef82002dc4188c276c967733bf3f7dfe6ed10afb436761e28b05f01c47748d`  
		Last Modified: Tue, 13 Aug 2024 07:41:48 GMT  
		Size: 3.6 MB (3561403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b732592ee34b5f02ad33eed797d157f745cb26004c31735bb1a7c10c88fb8e63`  
		Last Modified: Tue, 13 Aug 2024 07:41:47 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:549b82d1b0e5cd9c2ce9a9baf648b680a14c782c8f611235c31aca17cd419869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60436291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1bc6a4d38957fdfd69ea50f09f3ea43d9787658cdca31544d4d0141f6606cf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
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
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09f0177e0d45ab1a69528ede56e30ac3e58bde63bf62f2c1bf78711aec1b92e`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 6.6 MB (6565895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bedb0642cb91b6008a3795412ad5527c9838485628cdb532f1abb601b3d56e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a53b8f72283931b8920c07e7c2c39098475ff9658352fde012ed25e5ad75471`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a7d0317b5178d23dcf6d127c9d0af7c859e20d4bf21fb593b37a0621ab74a2`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 90.5 KB (90485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faf6db1b44baed2d5b9bb7695613c6daf5549c5f18f80473d873e346ffb47b7`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:969eb3d41b3528ee2d9433a5a63c75104060be0657ff8b63cacb1e505c8c89ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f8c1efe704d408b169c6fcfa592a13d6a9472f0e7b2e27b298560a24ff6281`

```dockerfile
```

-	Layers:
	-	`sha256:30e99b0a09798c571353fbc370f6f4dc9cec56ea7091480e8cad466438192439`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 3.6 MB (3557454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d0c3b412bb34261435220faf454f44ac6f6b3120cf906986b821f2d2229cb`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json
