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
$ docker pull neurodebian@sha256:d37ee95a3a4e97077a195f1618d2c8bd90b293f85744e2a7cf80ed4259962633
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
$ docker pull neurodebian@sha256:0da3e2d072a602fc6aedb65562b6c8eb2c9f32c62fce9fd7f31c95032970c379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4a360ac191d5d2dfa259dc87d446570b0d3c15baaef04491f0e4aed52377b3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad183c8b3e3a9f8871698df5673c23c35a92c4c0dbad82013ff7a7a9e91ae0e`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 11.3 MB (11266613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab9dd5bbb30c88662b92c8e56c3d34b5edb303dafc7f29ad99a7be171618c2d`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9ddf544f7b3442b8f4e09584b274a5782a6291b1e323ee48f2ef808bbdf45`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24e1a01d8b12dd36957fa1a2d368dd060fb013e1ab87cb997abca2f333d1651`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 93.1 KB (93125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9a54adf117975620ed244ee1f30b90073e8ec8ba56c2cd8db94953d6bcea290f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f329d7193c18aecca9a1cf6b27cfd7121b4d26db5c4bdefb596abdc52b939968`

```dockerfile
```

-	Layers:
	-	`sha256:81f432ff269dc1a78c67656daffb6eee212e88c40fdb327917ca6d36dcf2e40a`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130e5b11daf010f2e0029de0a5d4f9c3ee0e49c677d22e39e3ca1ab41fde0912`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
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
$ docker pull neurodebian@sha256:345bc7238b549e242190d82618dfc9f8e3d9b5d4eeb48d1f8f4c183b5ca39eb4
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
$ docker pull neurodebian@sha256:8bd6a40105820974efe39bacbacdda2abf45d9a2239a1ed59ed5cc08c8ba5924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68920c76da27386dc105718634961f0d847b5b71341d43ffa344575c779a5760`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f38856aca84fc144c0894b5583b4733c356542f9aabc617530a97da355e93`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 11.3 MB (11266599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bedb0642cb91b6008a3795412ad5527c9838485628cdb532f1abb601b3d56e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eec48808fb3af2793b868bdf881c68d54ffa9e36a78a84d6e0d6b296635ae1`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62c22daa22d6e4428a915ba7f39570fb94d04a461d6f66900ed31435bdc8520`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 93.1 KB (93113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b709e37690577434c0e98ed93efe2e947903baf6645ac5a17f97519f11a05c`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:18f6f19cb34871157480e0861fe447601f5dbf2c0b53bdef2fad3d7fbac6c7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92278b6032691d9a3cb503369fed1eeef86279c73860d6a32164e168f0591d0c`

```dockerfile
```

-	Layers:
	-	`sha256:da9593be6b0b5f94837cc43cb8a00a54beddedf81adcb710adf290ceca381181`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e17459c208fdfbf0ed14c8725db4eea4a2aedbed0bf0ec8dc704592a7e1ead4`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
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
$ docker pull neurodebian@sha256:fa4b70dad27813a8803e89a1e8cc5fa47b2d06259664664ca04e8d794edf6ddb
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
$ docker pull neurodebian@sha256:34b4a1e9f0fdacc26611a05ad1aa04e7aae7354b208d5b2f90284d0723bd8343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66292877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3520b073fa14e37b48cf5171678599407638fab2d1dd60963be91f361c01d12a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59f7861e33199bc85cce3c6dcc4f8014b0a185dff895c7361b35b262ce16638`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 11.1 MB (11105028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4174a9f0cbd87556668c13783915e131f9e70dcb1f616202f0e7a57eb3d1e84`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1815254f6f1e08ec804bced1771e936b243b47a8da7da36e34cd0890e2f3bb`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebca9645ccdf582bdf46081c9af04b0df590967aa2ec73c2285224b4aa718ac7`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 101.2 KB (101183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9bd23726d6e1d2758a3196ddcdd794fd5f31b2c24b598f593d65c2f1d734968c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e5eed48c915c3fcf0deea598b05dfabc8f84f50da6cfae8dfbb8b18b0f38fb`

```dockerfile
```

-	Layers:
	-	`sha256:e3ac75a08adb4bfa2e09937b3b5b87f277b2d1a16e4e208d354d2c59a4671d1e`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 4.2 MB (4223704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3189edf3ada0384fc5ae30ca3bf9cf065adcb7e44b4f52e5abb768ea376b1c61`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
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
$ docker pull neurodebian@sha256:8199b61b1a417e7ed51ca8f80672a46e758a4c8ced47ee34c31aafbe6fb46d18
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
$ docker pull neurodebian@sha256:ffc4b9f7508e242b9c69859a5d90b3cf612c06fc0ada1d8504b151d926aa7a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cec37c6d3e31136d0c85bbcf9c097ffbd9779f27e708ee6c92d484ba1b1ccc5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302351d91a1231ecbae76cb5918e1b4cc192e39df948aca28a41606f1a06b4e0`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 11.1 MB (11105040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe9b6f0fef964119f9408e111e03d80dc922a3a345387da6b73d909fa80b92c`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7445590a739b3a522581d8c7dc1ffaece3ac9e37098e8907cfb623047fa6d0`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6518ed1b8e70b81cfcd4f0d725be2b0ea9493750e3a879f9c5e805fa8a0db623`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 101.2 KB (101177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7335d3d5a67b1af26f9467d05864711f203d8717fdaf3b234633685a0d52763`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dafc26cdfdbf6bd3b827334c33c1c51a3589aeb2d4cc8fdfdfad72ce91a969f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ecc2700e13b73ae9acf43a5cc50f26177d75c2925a95ecd587e6c3007edcd`

```dockerfile
```

-	Layers:
	-	`sha256:7646adb8bf076c6f9cf65585d8ac71b400a62b06deea134f022bc9665a48b1ba`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 4.2 MB (4223740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c1b77c2882e500f5c0a132939374d17c22a90124b059be85680374d5521d83`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 15.5 KB (15510 bytes)  
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
$ docker pull neurodebian@sha256:d37ee95a3a4e97077a195f1618d2c8bd90b293f85744e2a7cf80ed4259962633
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
$ docker pull neurodebian@sha256:0da3e2d072a602fc6aedb65562b6c8eb2c9f32c62fce9fd7f31c95032970c379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4a360ac191d5d2dfa259dc87d446570b0d3c15baaef04491f0e4aed52377b3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad183c8b3e3a9f8871698df5673c23c35a92c4c0dbad82013ff7a7a9e91ae0e`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 11.3 MB (11266613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab9dd5bbb30c88662b92c8e56c3d34b5edb303dafc7f29ad99a7be171618c2d`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9ddf544f7b3442b8f4e09584b274a5782a6291b1e323ee48f2ef808bbdf45`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24e1a01d8b12dd36957fa1a2d368dd060fb013e1ab87cb997abca2f333d1651`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 93.1 KB (93125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9a54adf117975620ed244ee1f30b90073e8ec8ba56c2cd8db94953d6bcea290f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f329d7193c18aecca9a1cf6b27cfd7121b4d26db5c4bdefb596abdc52b939968`

```dockerfile
```

-	Layers:
	-	`sha256:81f432ff269dc1a78c67656daffb6eee212e88c40fdb327917ca6d36dcf2e40a`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130e5b11daf010f2e0029de0a5d4f9c3ee0e49c677d22e39e3ca1ab41fde0912`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
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
$ docker pull neurodebian@sha256:9f5b975b041bbf981dafdef3df85aa14153ee158381a5f178bcc7fc30f0e4223
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
$ docker pull neurodebian@sha256:0c49e4a33023f609f09584e01a96d87c68a121e96515944c5f3742046a1131d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59170126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcbf25b3d7e2dedf834db3c4f16a5666b581e8ef4a7b61bd7a2221053e84b07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
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
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89778f0cbe977174713de355013559ccca9aa08d5b5b559e431b5bd430fab4`  
		Last Modified: Tue, 13 Aug 2024 01:12:06 GMT  
		Size: 6.2 MB (6241198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e887a135a43718b8a55438286ebe39af3c8d90d51c7777702b9975eec68eb7`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f923e5ac6535fb231a908057bf7bf9c5a189cb99940d6b80b697a9197646b238`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858564bc043dfb29427bf2f3af58c4ccb39bf59727d42f4b231d5d1c591ce9e`  
		Last Modified: Tue, 13 Aug 2024 01:12:06 GMT  
		Size: 90.8 KB (90755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef82d2130935bb1c751f0ee18ba8240b2d6756d043b12ef03a7f10017b9d1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60949604cf8301350f811495e1b4a1c190193e428919143b5699ae94506c2ea`

```dockerfile
```

-	Layers:
	-	`sha256:c07e1a9590f3ec7c50f2087ca0e87be26394b0ea852bf7b6e99d665e12b9ef7f`  
		Last Modified: Tue, 13 Aug 2024 01:12:06 GMT  
		Size: 3.5 MB (3532398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:862a30da3b7805baa8efb3dd60a274fbaf4f01dc944ec7841862bcea4cad736a`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
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
$ docker pull neurodebian@sha256:e382f68d34a32f679268cb7b1e18311e274a206aed15f22ec975d0fcd72233b9
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
$ docker pull neurodebian@sha256:1425bd9e1aee2d8b829fe6f60c573976565e2db157ca795344af02a3318858b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59170368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabc5957637bf252746d4ee8fa3c9557c75872388cd662cc34a9041fe9c22949`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
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
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb951e649daac819b595ac587aaf218374e8b4c3bc3087ba695fac7b934eba45`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 6.2 MB (6241054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f038e90372847809ce4787019ffe2552665f1ee24e025408dae3af64a31ad5`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accfc3f0a6a00032ea0f0a0c663842971044c6aeac311d4125f722aa71a0389e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c314720cc1a281762827362053b361757ef353ecbf43d5087e73180343ea5ad`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 90.8 KB (90751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d58994bee8abc92b11ab4b444c3e25ac488693c2c7cb41084f5033169065270`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea1b48dadf464be5d8f7b5e22aa16d72f2f0dd37386de3115a688a21eb0b5d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd84b85cd11787fa38071e74cfc3c3bbaea4fb3b57cc4206f89bd741a77477c7`

```dockerfile
```

-	Layers:
	-	`sha256:18ec6a52cd24db235d9d5944f71ac133a2d011cc2b0ec5b78c4ab1476b15c740`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 3.5 MB (3532434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52e2080267d702efdcfb23a039482f22c00ce72808e220895ca7f265026ed8e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 15.4 KB (15429 bytes)  
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
$ docker pull neurodebian@sha256:fa4b70dad27813a8803e89a1e8cc5fa47b2d06259664664ca04e8d794edf6ddb
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
$ docker pull neurodebian@sha256:34b4a1e9f0fdacc26611a05ad1aa04e7aae7354b208d5b2f90284d0723bd8343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66292877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3520b073fa14e37b48cf5171678599407638fab2d1dd60963be91f361c01d12a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59f7861e33199bc85cce3c6dcc4f8014b0a185dff895c7361b35b262ce16638`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 11.1 MB (11105028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4174a9f0cbd87556668c13783915e131f9e70dcb1f616202f0e7a57eb3d1e84`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1815254f6f1e08ec804bced1771e936b243b47a8da7da36e34cd0890e2f3bb`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebca9645ccdf582bdf46081c9af04b0df590967aa2ec73c2285224b4aa718ac7`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 101.2 KB (101183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9bd23726d6e1d2758a3196ddcdd794fd5f31b2c24b598f593d65c2f1d734968c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e5eed48c915c3fcf0deea598b05dfabc8f84f50da6cfae8dfbb8b18b0f38fb`

```dockerfile
```

-	Layers:
	-	`sha256:e3ac75a08adb4bfa2e09937b3b5b87f277b2d1a16e4e208d354d2c59a4671d1e`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
		Size: 4.2 MB (4223704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3189edf3ada0384fc5ae30ca3bf9cf065adcb7e44b4f52e5abb768ea376b1c61`  
		Last Modified: Tue, 13 Aug 2024 01:11:59 GMT  
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
$ docker pull neurodebian@sha256:8199b61b1a417e7ed51ca8f80672a46e758a4c8ced47ee34c31aafbe6fb46d18
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
$ docker pull neurodebian@sha256:ffc4b9f7508e242b9c69859a5d90b3cf612c06fc0ada1d8504b151d926aa7a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cec37c6d3e31136d0c85bbcf9c097ffbd9779f27e708ee6c92d484ba1b1ccc5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302351d91a1231ecbae76cb5918e1b4cc192e39df948aca28a41606f1a06b4e0`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 11.1 MB (11105040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe9b6f0fef964119f9408e111e03d80dc922a3a345387da6b73d909fa80b92c`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7445590a739b3a522581d8c7dc1ffaece3ac9e37098e8907cfb623047fa6d0`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6518ed1b8e70b81cfcd4f0d725be2b0ea9493750e3a879f9c5e805fa8a0db623`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 101.2 KB (101177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7335d3d5a67b1af26f9467d05864711f203d8717fdaf3b234633685a0d52763`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dafc26cdfdbf6bd3b827334c33c1c51a3589aeb2d4cc8fdfdfad72ce91a969f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ecc2700e13b73ae9acf43a5cc50f26177d75c2925a95ecd587e6c3007edcd`

```dockerfile
```

-	Layers:
	-	`sha256:7646adb8bf076c6f9cf65585d8ac71b400a62b06deea134f022bc9665a48b1ba`  
		Last Modified: Tue, 13 Aug 2024 01:11:50 GMT  
		Size: 4.2 MB (4223740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c1b77c2882e500f5c0a132939374d17c22a90124b059be85680374d5521d83`  
		Last Modified: Tue, 13 Aug 2024 01:11:49 GMT  
		Size: 15.5 KB (15510 bytes)  
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
$ docker pull neurodebian@sha256:d37ee95a3a4e97077a195f1618d2c8bd90b293f85744e2a7cf80ed4259962633
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
$ docker pull neurodebian@sha256:0da3e2d072a602fc6aedb65562b6c8eb2c9f32c62fce9fd7f31c95032970c379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4a360ac191d5d2dfa259dc87d446570b0d3c15baaef04491f0e4aed52377b3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad183c8b3e3a9f8871698df5673c23c35a92c4c0dbad82013ff7a7a9e91ae0e`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 11.3 MB (11266613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab9dd5bbb30c88662b92c8e56c3d34b5edb303dafc7f29ad99a7be171618c2d`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9ddf544f7b3442b8f4e09584b274a5782a6291b1e323ee48f2ef808bbdf45`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24e1a01d8b12dd36957fa1a2d368dd060fb013e1ab87cb997abca2f333d1651`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 93.1 KB (93125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9a54adf117975620ed244ee1f30b90073e8ec8ba56c2cd8db94953d6bcea290f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f329d7193c18aecca9a1cf6b27cfd7121b4d26db5c4bdefb596abdc52b939968`

```dockerfile
```

-	Layers:
	-	`sha256:81f432ff269dc1a78c67656daffb6eee212e88c40fdb327917ca6d36dcf2e40a`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130e5b11daf010f2e0029de0a5d4f9c3ee0e49c677d22e39e3ca1ab41fde0912`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
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
$ docker pull neurodebian@sha256:345bc7238b549e242190d82618dfc9f8e3d9b5d4eeb48d1f8f4c183b5ca39eb4
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
$ docker pull neurodebian@sha256:8bd6a40105820974efe39bacbacdda2abf45d9a2239a1ed59ed5cc08c8ba5924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68920c76da27386dc105718634961f0d847b5b71341d43ffa344575c779a5760`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f38856aca84fc144c0894b5583b4733c356542f9aabc617530a97da355e93`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 11.3 MB (11266599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bedb0642cb91b6008a3795412ad5527c9838485628cdb532f1abb601b3d56e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eec48808fb3af2793b868bdf881c68d54ffa9e36a78a84d6e0d6b296635ae1`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62c22daa22d6e4428a915ba7f39570fb94d04a461d6f66900ed31435bdc8520`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 93.1 KB (93113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b709e37690577434c0e98ed93efe2e947903baf6645ac5a17f97519f11a05c`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:18f6f19cb34871157480e0861fe447601f5dbf2c0b53bdef2fad3d7fbac6c7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92278b6032691d9a3cb503369fed1eeef86279c73860d6a32164e168f0591d0c`

```dockerfile
```

-	Layers:
	-	`sha256:da9593be6b0b5f94837cc43cb8a00a54beddedf81adcb710adf290ceca381181`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e17459c208fdfbf0ed14c8725db4eea4a2aedbed0bf0ec8dc704592a7e1ead4`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
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
$ docker pull neurodebian@sha256:ad5cf2ec554fc3e9f6ca5e5fdc32967ec9d7de6904228c0e455fc6dd9886c0a5
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
$ docker pull neurodebian@sha256:6d762d79558c201d14a01e74573becee71d96b043ec7fea796724b17a3400d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59174533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4eefa4d71d13b7db1bbdfeaa1758a185409923e4363e732bed24ecf61cdf648`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
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
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f663abeab595413cca77c6f88a50322c4f80411702f17a711185b2c60333f2`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 6.2 MB (6240830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75ad9f7a649edb3af0b7b6cc8889cae322c6b55fa769f8f9b3d620286adeee7`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06429724a765681651790d014b72d30be34a6ffa16992333196ce8b6362a509`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7641817998246bf51a0c4699044a33146c720f1df0e311b5d1b69b46516619cc`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 90.5 KB (90530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:37505ae8aec723614f36f687b143b321cb7caa64244cf45e5965d1e762c5bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268d333f155cec535e6ef7351dd94a389f6929eae109a64f9245b9a7c04f3763`

```dockerfile
```

-	Layers:
	-	`sha256:7867a6667f51720c1d78329fb4253fa850c05a4d44cbc8ed22fbcf1189cbc955`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 3.6 MB (3560325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc61e695b0ad6b83c0b832255d79ef2b109598a3fa1c29b83829c2b835647de`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
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
$ docker pull neurodebian@sha256:c2c162da43785442e6e6a09f487d01de7be7123b324562732db9aa30c2786799
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
$ docker pull neurodebian@sha256:4599eb89d641c78f06330b5fc19e48023605af17a797465478d0b8be428f2ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59175044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d284eeb79e113b6e02d6ee672a6aa3520a83b5fa898a4bd2cb533ae8325e700`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
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
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce474f48ccd105d0617c09fe857f117a99e1e29a996b4320ba2b7de1979f59bb`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 6.2 MB (6240869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fd3a110ef4119373f628e087c16dbbb4bd28f06220d7389a705093d2b18012`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61497ddf2d4bb6a7077bc1d8b6a1c5424cc821e644b2c69433d9ffcb21547f7a`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a97170d3249a59394f70016aa80f45c6862354794bf973c6d159f12d2287cd`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 90.6 KB (90571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0706b3fa22fc07de6182303c357248f9a97b3e27b5e9035a4589d29413bda884`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:19841391167fc5f99fa73a705a1dad677fb273bf4bc43c9b9e4e22ef270c747a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a4734cebb22caa416a176e19399fcd71abfb92b38d0fbfbf918d39076f45a7`

```dockerfile
```

-	Layers:
	-	`sha256:864026c809e53aff40d228261d22b559ec0c43cd4a4acf3bd4461dc7344333df`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 3.6 MB (3560361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b82d259378640a9dbf9d00c545a02c4b92dc986e42188be54ef7e78503b091da`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 15.5 KB (15476 bytes)  
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
$ docker pull neurodebian@sha256:345bc7238b549e242190d82618dfc9f8e3d9b5d4eeb48d1f8f4c183b5ca39eb4
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
$ docker pull neurodebian@sha256:8bd6a40105820974efe39bacbacdda2abf45d9a2239a1ed59ed5cc08c8ba5924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68920c76da27386dc105718634961f0d847b5b71341d43ffa344575c779a5760`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f38856aca84fc144c0894b5583b4733c356542f9aabc617530a97da355e93`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 11.3 MB (11266599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bedb0642cb91b6008a3795412ad5527c9838485628cdb532f1abb601b3d56e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eec48808fb3af2793b868bdf881c68d54ffa9e36a78a84d6e0d6b296635ae1`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62c22daa22d6e4428a915ba7f39570fb94d04a461d6f66900ed31435bdc8520`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 93.1 KB (93113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b709e37690577434c0e98ed93efe2e947903baf6645ac5a17f97519f11a05c`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:18f6f19cb34871157480e0861fe447601f5dbf2c0b53bdef2fad3d7fbac6c7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92278b6032691d9a3cb503369fed1eeef86279c73860d6a32164e168f0591d0c`

```dockerfile
```

-	Layers:
	-	`sha256:da9593be6b0b5f94837cc43cb8a00a54beddedf81adcb710adf290ceca381181`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e17459c208fdfbf0ed14c8725db4eea4a2aedbed0bf0ec8dc704592a7e1ead4`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
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
$ docker pull neurodebian@sha256:9f5b975b041bbf981dafdef3df85aa14153ee158381a5f178bcc7fc30f0e4223
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
$ docker pull neurodebian@sha256:0c49e4a33023f609f09584e01a96d87c68a121e96515944c5f3742046a1131d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59170126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcbf25b3d7e2dedf834db3c4f16a5666b581e8ef4a7b61bd7a2221053e84b07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
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
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89778f0cbe977174713de355013559ccca9aa08d5b5b559e431b5bd430fab4`  
		Last Modified: Tue, 13 Aug 2024 01:12:06 GMT  
		Size: 6.2 MB (6241198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e887a135a43718b8a55438286ebe39af3c8d90d51c7777702b9975eec68eb7`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f923e5ac6535fb231a908057bf7bf9c5a189cb99940d6b80b697a9197646b238`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858564bc043dfb29427bf2f3af58c4ccb39bf59727d42f4b231d5d1c591ce9e`  
		Last Modified: Tue, 13 Aug 2024 01:12:06 GMT  
		Size: 90.8 KB (90755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef82d2130935bb1c751f0ee18ba8240b2d6756d043b12ef03a7f10017b9d1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60949604cf8301350f811495e1b4a1c190193e428919143b5699ae94506c2ea`

```dockerfile
```

-	Layers:
	-	`sha256:c07e1a9590f3ec7c50f2087ca0e87be26394b0ea852bf7b6e99d665e12b9ef7f`  
		Last Modified: Tue, 13 Aug 2024 01:12:06 GMT  
		Size: 3.5 MB (3532398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:862a30da3b7805baa8efb3dd60a274fbaf4f01dc944ec7841862bcea4cad736a`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
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
$ docker pull neurodebian@sha256:e382f68d34a32f679268cb7b1e18311e274a206aed15f22ec975d0fcd72233b9
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
$ docker pull neurodebian@sha256:1425bd9e1aee2d8b829fe6f60c573976565e2db157ca795344af02a3318858b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59170368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabc5957637bf252746d4ee8fa3c9557c75872388cd662cc34a9041fe9c22949`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
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
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb951e649daac819b595ac587aaf218374e8b4c3bc3087ba695fac7b934eba45`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 6.2 MB (6241054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f038e90372847809ce4787019ffe2552665f1ee24e025408dae3af64a31ad5`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accfc3f0a6a00032ea0f0a0c663842971044c6aeac311d4125f722aa71a0389e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c314720cc1a281762827362053b361757ef353ecbf43d5087e73180343ea5ad`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 90.8 KB (90751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d58994bee8abc92b11ab4b444c3e25ac488693c2c7cb41084f5033169065270`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea1b48dadf464be5d8f7b5e22aa16d72f2f0dd37386de3115a688a21eb0b5d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd84b85cd11787fa38071e74cfc3c3bbaea4fb3b57cc4206f89bd741a77477c7`

```dockerfile
```

-	Layers:
	-	`sha256:18ec6a52cd24db235d9d5944f71ac133a2d011cc2b0ec5b78c4ab1476b15c740`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 3.5 MB (3532434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52e2080267d702efdcfb23a039482f22c00ce72808e220895ca7f265026ed8e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 15.4 KB (15429 bytes)  
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
$ docker pull neurodebian@sha256:ad5cf2ec554fc3e9f6ca5e5fdc32967ec9d7de6904228c0e455fc6dd9886c0a5
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
$ docker pull neurodebian@sha256:6d762d79558c201d14a01e74573becee71d96b043ec7fea796724b17a3400d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59174533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4eefa4d71d13b7db1bbdfeaa1758a185409923e4363e732bed24ecf61cdf648`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
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
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f663abeab595413cca77c6f88a50322c4f80411702f17a711185b2c60333f2`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 6.2 MB (6240830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75ad9f7a649edb3af0b7b6cc8889cae322c6b55fa769f8f9b3d620286adeee7`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06429724a765681651790d014b72d30be34a6ffa16992333196ce8b6362a509`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7641817998246bf51a0c4699044a33146c720f1df0e311b5d1b69b46516619cc`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 90.5 KB (90530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:37505ae8aec723614f36f687b143b321cb7caa64244cf45e5965d1e762c5bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268d333f155cec535e6ef7351dd94a389f6929eae109a64f9245b9a7c04f3763`

```dockerfile
```

-	Layers:
	-	`sha256:7867a6667f51720c1d78329fb4253fa850c05a4d44cbc8ed22fbcf1189cbc955`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 3.6 MB (3560325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc61e695b0ad6b83c0b832255d79ef2b109598a3fa1c29b83829c2b835647de`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
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
$ docker pull neurodebian@sha256:c2c162da43785442e6e6a09f487d01de7be7123b324562732db9aa30c2786799
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
$ docker pull neurodebian@sha256:4599eb89d641c78f06330b5fc19e48023605af17a797465478d0b8be428f2ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59175044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d284eeb79e113b6e02d6ee672a6aa3520a83b5fa898a4bd2cb533ae8325e700`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
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
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce474f48ccd105d0617c09fe857f117a99e1e29a996b4320ba2b7de1979f59bb`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 6.2 MB (6240869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fd3a110ef4119373f628e087c16dbbb4bd28f06220d7389a705093d2b18012`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61497ddf2d4bb6a7077bc1d8b6a1c5424cc821e644b2c69433d9ffcb21547f7a`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a97170d3249a59394f70016aa80f45c6862354794bf973c6d159f12d2287cd`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 90.6 KB (90571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0706b3fa22fc07de6182303c357248f9a97b3e27b5e9035a4589d29413bda884`  
		Last Modified: Tue, 13 Aug 2024 01:11:52 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:19841391167fc5f99fa73a705a1dad677fb273bf4bc43c9b9e4e22ef270c747a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a4734cebb22caa416a176e19399fcd71abfb92b38d0fbfbf918d39076f45a7`

```dockerfile
```

-	Layers:
	-	`sha256:864026c809e53aff40d228261d22b559ec0c43cd4a4acf3bd4461dc7344333df`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 3.6 MB (3560361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b82d259378640a9dbf9d00c545a02c4b92dc986e42188be54ef7e78503b091da`  
		Last Modified: Tue, 13 Aug 2024 01:11:51 GMT  
		Size: 15.5 KB (15476 bytes)  
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
