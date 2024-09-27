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
$ docker pull neurodebian@sha256:76657de75d2774ad7dd62dafb1bbb46c79a8a1837c2c8b049f675d7aa4f4cad4
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
$ docker pull neurodebian@sha256:c8664a96795b166095b204fa54dbf0f48b5e6e4978643e8b763bb7c05b2dae1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0c3b1ce774b89533bd30de564feff9ba4dc520f740d46ae423bc2653ea8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffec6389bcbf6537d5f6a384d29b76f4fcfd4cc7522491bbc0e1e95e5c3eb722`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 11.3 MB (11266554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc93f4d62109e8a5d2f564ccd69d7bef7d80a32aa7a410bc6363888daa816a5`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d017be4b2180bbb56d6789d0382e398768bd1b3e8f19973efa1578db0296c75`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ced1a1a098fd13cc5a63fe69b80bbeb7435fa6bbdc8331b130d68a6b87ba8`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 93.1 KB (93127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f8466efd911fc1b98e6f430f3b1aab449dad4490a17f294deec380b6afab020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78075cb443a7999c807e8fb4699f6f1c0086f081b30c2d93be94680e05390300`

```dockerfile
```

-	Layers:
	-	`sha256:f1b4f0b3cc2badb64712a79a6915ffb632e856347854c52ff14ad2fe57846900`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69c5d58fafb7ead8986e2f8e1a098fcb901d06df3df04978588846236a6382f`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c345a247dacdd96d613b963e2e3fdeb72161e5c0f5a7740992bdb9e008a4ea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60913243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e470508b10c079f238639a81b1a0e47c435bf1a64e75213f6cfca87fc7ab16`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1407873c66503c0a93617924a56b4dd8e307ce2f1c2584c89a9fa1fdb32af2e5`  
		Last Modified: Thu, 05 Sep 2024 12:36:08 GMT  
		Size: 11.2 MB (11232270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71660075504871b9d383826ce5d80aeeafa0f24ef0d028e8c70c2106e2f40295`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920d93d230ac89732db5e1368e9288d33ab00280170ed41ef415abb19e20b71`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80251e079aed2b00cf9612399cb10176c8e0143d29001b61c7468a9dfb9ce708`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be69dbe480fdadcaf18fadf575c4e568b8081c443cb058d2a983ac699af38c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809742a0e06d624313d6f4f95410ae5632623b4128683f3d68bd1a3a3c84c0c4`

```dockerfile
```

-	Layers:
	-	`sha256:12b6df0c491b4c73165be2fc940f2b5c7fa177ece053843b76b2ed5eedd97450`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b2553d87c1a9b1095a1a7cb0019d4b6626d96f473703640f98ce7e46bc8ed3`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:1f762b90a16539d08e371cf9704aab60d8f8c3bd95c833c50e21668cf75d57ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62358760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ac852c496b2f0a3d2c1faf2f58f6de35195ce64fb3ff870ba31256f00ef489`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
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
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7919eb19b12c4b3fd8c8f9fcaef0c8c8df9e67b237eaf93ea5e98cebdde9abf4`  
		Last Modified: Thu, 05 Sep 2024 00:09:59 GMT  
		Size: 11.7 MB (11688944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba9b8b02a6740c4da8a43dfff05dd4473b4cb8ba489bfd5ba06c1dbd3285fc0`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fe05c6734e5dc50476e722cc57112d104c24e75fa204f8dd5066a7c29c59cb`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8c07cd6938f90cd62484a4e934e8fe7ade8182db8af02e6eb697cf53ad89f`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 93.2 KB (93222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4912857a7eec07b09ab0a4fa3da525e7f87d45f9af9f5eee2da079179c129abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23220b0a9fd93875caeee52955614a1b33f553ad4f6d378f2db9f8b784bb00a8`

```dockerfile
```

-	Layers:
	-	`sha256:9972c1ef7979b6a6373c836cb171ac20e39fe3638963c57848b4f6b0c138da8a`  
		Last Modified: Thu, 05 Sep 2024 00:09:59 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc254bb1124e09a0866605b00898566346278bdda14bb13896928fd3b65b85d7`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:de074c6477a033b628c052824d0419e3b0a90f13a2fb4073488b3c56fa7cfe59
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
$ docker pull neurodebian@sha256:b48d6272400457ab71668d983cf66e3677f8df417b405a16646a77398ba08d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f348d52d0a30c0875589c2a9119a552d0157a52592558ed41ab0bfd3e3c77a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9051ff7592ebdf57081bea4813d054f179c10baf88e8edb1b1eb0503dc57a398`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 11.3 MB (11266587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7d938f0d1f711b7744833ba75d25ef22f306b38fed3f791d43c283332c29d`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d8d64e9f86a243cadef1fab89c4bc283c6ab4b4d7acd3c713da0063cfbc7f8`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45240937643905b587fa479f7122727e4da480a63dc938c4d4e680049d4fd520`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca5c0ab742bba3e582138550e8f5870657e878200808229861aaeff5b17eddd`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8be6a251f01d60f7c79d8354d52a880631b39d9b5e7686fa2e26ec2df80aeac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcc537a8cec282d091e002e6f0a1e677c36051a6c61478e3e8eb0454c94a884`

```dockerfile
```

-	Layers:
	-	`sha256:11250ff6b4c7bc963acdf419c612cf7ee613254e2246c5b3d2a533583138de69`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bdef147161d65fa6df17b8f42d4d1bc566bd2ca0efeceae14bea0caf771bed`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:efbdeb8b5d814d3b0da4a167795648e3e251258aeec382a14937d4ed99826943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60913673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9576bbaf4ce331301262d1e6d4a9810bd99ef004b198a7126debd55b79b3c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1407873c66503c0a93617924a56b4dd8e307ce2f1c2584c89a9fa1fdb32af2e5`  
		Last Modified: Thu, 05 Sep 2024 12:36:08 GMT  
		Size: 11.2 MB (11232270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71660075504871b9d383826ce5d80aeeafa0f24ef0d028e8c70c2106e2f40295`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920d93d230ac89732db5e1368e9288d33ab00280170ed41ef415abb19e20b71`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80251e079aed2b00cf9612399cb10176c8e0143d29001b61c7468a9dfb9ce708`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367edb1c54966400c609652e755bfdb13b1f44403b415b6f36f5848b816ba7f6`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:900367b3a0829a3505f3df1874436aa29263efaaa70664454f5f91988cd4fb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c011ed8d1fce4e65e055582847acd29b56999057e60cb5495e989ee0817c7a6`

```dockerfile
```

-	Layers:
	-	`sha256:e570ced3443d64a24e17909c417b0370d5ee898bac3f1a6ea39f4a6086ccd8f1`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb42b2ae1c5cd926ed226f5811a5371c33caac652433e2252db8c9c75c3d08b4`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1a4afcecebe4bef4caaf6087619df118f6c1c292e033583195fe045694d78fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62359183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dca3b4e9e7222f5e5153b36ebf4f2d7fa9753edac38b779988e74015695147`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
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
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3007322a25966cabf21ac5571de68c821d72acd5af0bab7e29cc49bd24fcf4e2`  
		Last Modified: Thu, 05 Sep 2024 00:09:57 GMT  
		Size: 11.7 MB (11688959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912cbec8e3e3b83e3b0ae68456830d139a8152ca87a74445b5b043d0a407752`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf715249f2d007d220402bfe1d271f2fb1f0a5a7a038325c8da0c0d76071f4c`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c7b649709ff95ab124a63a5e85dd2d68406f923eb64ea2c070ee8e90efff4b`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 93.2 KB (93199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c39ccb9d688897f6f2f421e68d389039bf4d1bd0374f30abbfe71cdff28518`  
		Last Modified: Thu, 05 Sep 2024 00:09:57 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ada24163b1b4d1e3f839b8115b1ed0645c68b9ea55e24ca934727e37e763e815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ab804dbd14fe55a29132e33f7fb879710fe7e02062c17b40e05b75229a1d2`

```dockerfile
```

-	Layers:
	-	`sha256:92daa7227caa0f20eb908642d3589981a329d915032fbb483a7516baf3d45921`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992d1d344f322d643c83815f60fa24f872e11058f6f463a541ec529076a1f76c`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:3f297160a19ea8ec16f983d5ce3171d63da3045d1b991019f8fa553acef21112
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
$ docker pull neurodebian@sha256:74236c937c5b037ad60fc432ebc254c1e580993ab29f478a9b300daa626bb915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3adae40b3c213aa1ae0712e9060a41aaf499df6ccdbd746f19223f35ec6827e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb0a6060b8b0998db2e10892443ef142934b0ef2830beee3e3e7cfe4514bd9`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11104992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d5910828d32d02f070dba4e7945868769def79e0f9902c66830608d68aa481`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be85d64ab216d005b467f6308b5615d673e978f19c236082f992bdaf4ad93bc8`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 101.2 KB (101161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bc6eb256921208f76e8b28589cf11cc18adca9cfe24fed607071a4661686462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56e3b7a65d4bc869c344278645e4b1720f997dbd966ddf3e536b74e2805f59`

```dockerfile
```

-	Layers:
	-	`sha256:29d56d4669ef53c2f9a8c6678f2b9a0ae5aca6a32c1944ff8aec60b1b297320a`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 4.2 MB (4223717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2583fb1f95ef1984a58e4586f792e94a80ff50ed736cd3b33c28bfd5be697f3f`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f8213b6341b1bd416e1b73705a77c5227eb076fbda50c1b61fcd15c711751a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64940530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5805688720b5f4b15de238d4d61f07be3d1b0eefd9289054e89a2edea0cf0d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
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
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab2fdf0b58451a0c31951dc2a87a932deed77518e2a054bf1aeb38a5a7261e`  
		Last Modified: Thu, 05 Sep 2024 12:35:11 GMT  
		Size: 11.1 MB (11105823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3cce06e7960e8ba47689bbfb2de4f89c0f135a613080c0ecb2e1000bd16804`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23140bbd52963541dd8e0e8cda7d68393aea1804ac6bffb8fcec5940e65548c8`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1608e10ac25cd129bacc060a2fe424b11ed352acf6fbe6cf25636d78d881b`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:55bc3810d671d847ecc66841d51d017ec8540ed69cbe03815513d4d976f05b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad28e0a95f8254034c3f6e0f85bddea0f76763c2a1a9b2ad5aff778d69795b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d583b4965a88051bb19cd82140b6cdf8b6061f04c587e3a03729578e52f4acf`  
		Last Modified: Thu, 05 Sep 2024 12:35:11 GMT  
		Size: 4.2 MB (4223309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa866db050febfc23f2a557d0e06f92e5c9275ed20dee19a24ea3179a6343a3`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:96fe4aae67000ad6550f8e6838709416ceab4f74feb9a1a90cff0c1d77d09d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef01da747f6f76c43b94466e8820aed5df2c186c69932d123b5ada9592911e2a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
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
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a943fde0ebcc219ed5be7a65813a44fd9ae078d1b63ebf63c5da678c99be32`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 11.5 MB (11500208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13415e438d502909f21cbd42d54392b1c1305ef218c1e306f811304d6979e7e0`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c19e1db6c281b76dbd156756d08b252509adc87346da5e11d53521a449f86`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebf1edbb66dc5cf0ded190f867405852068a545f2611eeb6af9decaec8470f6`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 101.1 KB (101061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bbd87945b96ceeba117e56bb2f8cfa4a6ec9224ad3b8f7bcf9f3c092882b83f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b42e85f12377a98e9ea3ff307f1a0e95c144db6a4aaa4d2797138ac8df80f`

```dockerfile
```

-	Layers:
	-	`sha256:125cb6ca9c69dceaeaf638763b1dee8b881dbdaaff4d69680342af0d71b50954`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 4.2 MB (4220164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefe7ff2bc097e2bcb6e8df83f2a1f83fed570e02fdb005a542c2e15d0b65ad6`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:1d4be1129dc978e893ca7f1f912b58d26e066836afa98da72b6b6c77f9e09952
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
$ docker pull neurodebian@sha256:7f5088398c7f011e8097a29cd701f675a1080cc500196391c4b6794022b8a9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdfcd7ff9d894bb20277f777c30089d05e6bee15278a392b84be6561a744ef7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781057eafc4c33d419ac01788ae0f4708e6c8b9b42b4c0efa58265084ba5c337`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11105021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9f0b8cb73e5762cef8aad324e1ee6e0a020348d975fcf9a1b709b4c3fe925`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297557466a2385d9af17a8e5e0acc6b5876c310f8717e40aa3661b00dcd1149`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0755dc4a01fa569e141b166f027a20446a1bbb2e769b0548ef4ddb92083bae`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 101.2 KB (101182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a4483fab3e6ba8071f141c5125469123ab6dcbd2c5b2d7d419005489a71053`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2af657dc55a7ddc9f14035295ebd2f147736d2fb0fab02638830682adf4479ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49ad2aa5db65dc48910c228539fe3ce366263eeafc62176ba3c49fa58b7e06`

```dockerfile
```

-	Layers:
	-	`sha256:1c2d01c9aa9c1e38c274b4f75b13960fb53e6223ec48d13adfc84fb8419989a8`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 4.2 MB (4223753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad25678c39510df32b23c842ca8358063f7fc4eb6fc0befe7ae6135f725771ce`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a9b51a2e80948cac7bbee59ea1e13ba5369969893b5d5ceb0521eb696dacb9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64940892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bee63eae38e75bc7be7dffba041e7ca7e73cae2c0e713811bc6551db1d40bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
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
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab2fdf0b58451a0c31951dc2a87a932deed77518e2a054bf1aeb38a5a7261e`  
		Last Modified: Thu, 05 Sep 2024 12:35:11 GMT  
		Size: 11.1 MB (11105823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3cce06e7960e8ba47689bbfb2de4f89c0f135a613080c0ecb2e1000bd16804`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23140bbd52963541dd8e0e8cda7d68393aea1804ac6bffb8fcec5940e65548c8`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1608e10ac25cd129bacc060a2fe424b11ed352acf6fbe6cf25636d78d881b`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bd040d3118a6dc2176423c1d31a87a6a1e1e7e868f44fcced1e796200e04d5`  
		Last Modified: Thu, 05 Sep 2024 12:35:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8fe5ebf423951de559c47fa6d007a391c4d6a39842255620507e7a89643d3464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf0a49183496dd812d4c35815772ca7d8afa88030bef74f8c5b130d4ea65bf9`

```dockerfile
```

-	Layers:
	-	`sha256:c742219d6395bd95d2f014a16537d41f6ec98d39481f7a8126835bd2d634a6ed`  
		Last Modified: Thu, 05 Sep 2024 12:35:33 GMT  
		Size: 4.2 MB (4223345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce31a0ef62db38cb1b6a25769b3a8466fed5b6b6aa09a6baac7c73f3cede77a7`  
		Last Modified: Thu, 05 Sep 2024 12:35:32 GMT  
		Size: 15.8 KB (15791 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7616dceee5aefc521c248668cfe4a6ee06908cd2c688bde93d4e1c62fe1d90d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c8fa70d35b466b7488d6a8bbee5796d005eb095ecd6343839a909543ae790`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
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
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b13fceaf30837919c83ba0eaff4811346a54e9111e8609afa66847dddc498f`  
		Last Modified: Thu, 05 Sep 2024 00:07:30 GMT  
		Size: 11.5 MB (11500195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94822419f2eee106212fd1cfb61f612f5cbb4de0cff53b8b4346661dbd7d6dcf`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72cd6ea7780d9eb88dcbf6a60de043343c71c84b38a3fd593f7c4443e9841eb`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d79df17eae45ea840c3dd3047ee6d29f0238a4f93a9e4e5dfa6bb97776be06`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 101.1 KB (101052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfec050c8598da5da9fa965646f462272eb9bdfa7a27114a560c38e4aa697d3`  
		Last Modified: Thu, 05 Sep 2024 00:07:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f459330823492f170624e082686abd94b19b9855ca680cbc804070ed438cdbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a5abdbadfd2154a3bb12d0bfcaa4d4a86ff75310e4b6c11de2c608942a4f94`

```dockerfile
```

-	Layers:
	-	`sha256:9fe7cc4755190f18ca56b92e4c52d4545aa9e9a4a32a2c49d2ddda1dca821a47`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 4.2 MB (4220200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45de231496ead48cb3e03380acd101ff2b3b7fb3eec01e567cbe03aefdda1d3`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
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
$ docker pull neurodebian@sha256:8cd25968c7a8dda57e86f5f31179a392780c365d049c245f1563df254a345b6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:b5e2ad2679d21dfb98319132904ff13815643d741d29c2cbd61f795d2cfce2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03035b5fafec30a11ccaf9e676191d30bf2a93a2c961ae50bcdeae21ecee68c`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e5fc20939f49ca46aaa63fda94b740a46522034dd33a99dc846c2ab47da385`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 3.6 MB (3622683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d7c12d3dff8024cc7a65a06760eefef7523e92d4ab01561da2876474be6e25`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257f9b0966cd5484318ba1e2300bcf4102ad856d15cf79307d6575cb919be75d`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25429882efb06104ffa477fe41e22a29ad87a1b8b5a97eddc221fb3cfb85bc29`  
		Last Modified: Tue, 17 Sep 2024 00:58:50 GMT  
		Size: 110.0 KB (110041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d732e29d091ef7f0e630eef553f727bdf00995f77c7dcc07b0561d4792f4341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb4b42740c8b876bb56d509444cd2d22fd632ea9c6254cf4af8ef60cb72b5aa`

```dockerfile
```

-	Layers:
	-	`sha256:46449a2a17035de35151d0f04752a18008bd77cdb9bd76b7f1465ab848857267`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 2.0 MB (2041055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f62c1b512cec8166de552b1e0085eb7526f3474781a15c9cfadf62c2436da`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2e8ddba19dffa270b72c0c17efca5bea22c862945352f06ad9391ca69ae180ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64399ffc86a2a302a5f8b07efe84fa560a195e25878c4a52e8f5d97367769e`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:769792b0a9ae99abbe1b81296f09e1e53c2e662643848544f1a641d54f8b29bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ab15b050723ad8ecd0ff560efdd18d3d1451cbd92375f54cf16c418e647366`

```dockerfile
```

-	Layers:
	-	`sha256:2a92568efc9bccb357a48dc2f8cc5ef4f0d34112762744fc1408de6d45f8e34a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 2.0 MB (2041314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783fe908caebc3d7a05968a298b4c97dd56aff0cc5841272d2f31f8d0eac4efd`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:c35390a21d7dcdaa5248caedb0c2d1d3f2b9a31a1ccc6a5fd082bc8262ef35a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e45ad58f9dc146f7c58fee7c828c3c6831e76bdb9cf7020f9f7c9448d53671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4ea79fb23e81c99deef7e3da0330d8995389a5ed5528314613545bbc38a650`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e444df7ecce18d9b6a39b30f8f893e46de9a6c8393753ceb73f80be5147d5e`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 3.6 MB (3622684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eb688a315dc9dc281db41ae45a5e1651f96d5b6b93100b8f6b3604a1b7be90`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18efaf2abf8b145da9341e025a8599685148d724adf71187513efcefdc1eb92b`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c03e7463fe28779caf76a60210e080067f4e00e4a28d1ef22b5f71aab3511f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 110.0 KB (110044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a748ff3cbe6a5eed1e2b979d6648c667fb7a29be6b3e2bc14ea06d88519a0592`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49d3a7c89f96056348bc2f29c7aaab1b27bde7d7755e5cea5fe7102dbc63a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0141b248fd4a83635efee725ebffc6599bb6e48aedbb01287016be2df2e9e29d`

```dockerfile
```

-	Layers:
	-	`sha256:2aa3ae2b7c2d8c84a96d9dfae22e8bdbef344f1dea22754309dafd7d8ba3fa7f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 2.0 MB (2041091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48b6d14af7ecf44b9066d810db720df1078da0e69b612cc31771ef41b2957b4a`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4a2bedc35b23fd303d37b492a4dcd265b749cc561bed81266ef4fd4f072ca3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cc596bfd27c527f722fd0f60344b7c29c0ede0e0215ca28663dd6f7b11334d`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0571d1820815c6ffe6445310d6d56c0904985a7a40ce55ea60111c7ab14c14af`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15e423dc66f68b2fd18342bafd40c16c24df1ff2d5a105e3d23fe7a7b66e4859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14030ec66c96db8f89c291fc02780ff4e9dd29fbe18b7deeb19f1a70811d83`

```dockerfile
```

-	Layers:
	-	`sha256:b8a537c7762547e63f17b420cb0912f491db0829af8089494798ac00e311b1a7`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 2.0 MB (2041350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab7d3d2aaba018f1a288d03ac3c709c72564deb83d89ee6d4197767b31a448c9`  
		Last Modified: Tue, 17 Sep 2024 02:37:08 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:76657de75d2774ad7dd62dafb1bbb46c79a8a1837c2c8b049f675d7aa4f4cad4
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
$ docker pull neurodebian@sha256:c8664a96795b166095b204fa54dbf0f48b5e6e4978643e8b763bb7c05b2dae1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0c3b1ce774b89533bd30de564feff9ba4dc520f740d46ae423bc2653ea8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffec6389bcbf6537d5f6a384d29b76f4fcfd4cc7522491bbc0e1e95e5c3eb722`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 11.3 MB (11266554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc93f4d62109e8a5d2f564ccd69d7bef7d80a32aa7a410bc6363888daa816a5`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d017be4b2180bbb56d6789d0382e398768bd1b3e8f19973efa1578db0296c75`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ced1a1a098fd13cc5a63fe69b80bbeb7435fa6bbdc8331b130d68a6b87ba8`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 93.1 KB (93127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f8466efd911fc1b98e6f430f3b1aab449dad4490a17f294deec380b6afab020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78075cb443a7999c807e8fb4699f6f1c0086f081b30c2d93be94680e05390300`

```dockerfile
```

-	Layers:
	-	`sha256:f1b4f0b3cc2badb64712a79a6915ffb632e856347854c52ff14ad2fe57846900`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69c5d58fafb7ead8986e2f8e1a098fcb901d06df3df04978588846236a6382f`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c345a247dacdd96d613b963e2e3fdeb72161e5c0f5a7740992bdb9e008a4ea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60913243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e470508b10c079f238639a81b1a0e47c435bf1a64e75213f6cfca87fc7ab16`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1407873c66503c0a93617924a56b4dd8e307ce2f1c2584c89a9fa1fdb32af2e5`  
		Last Modified: Thu, 05 Sep 2024 12:36:08 GMT  
		Size: 11.2 MB (11232270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71660075504871b9d383826ce5d80aeeafa0f24ef0d028e8c70c2106e2f40295`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920d93d230ac89732db5e1368e9288d33ab00280170ed41ef415abb19e20b71`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80251e079aed2b00cf9612399cb10176c8e0143d29001b61c7468a9dfb9ce708`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be69dbe480fdadcaf18fadf575c4e568b8081c443cb058d2a983ac699af38c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809742a0e06d624313d6f4f95410ae5632623b4128683f3d68bd1a3a3c84c0c4`

```dockerfile
```

-	Layers:
	-	`sha256:12b6df0c491b4c73165be2fc940f2b5c7fa177ece053843b76b2ed5eedd97450`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b2553d87c1a9b1095a1a7cb0019d4b6626d96f473703640f98ce7e46bc8ed3`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:1f762b90a16539d08e371cf9704aab60d8f8c3bd95c833c50e21668cf75d57ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62358760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ac852c496b2f0a3d2c1faf2f58f6de35195ce64fb3ff870ba31256f00ef489`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
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
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7919eb19b12c4b3fd8c8f9fcaef0c8c8df9e67b237eaf93ea5e98cebdde9abf4`  
		Last Modified: Thu, 05 Sep 2024 00:09:59 GMT  
		Size: 11.7 MB (11688944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba9b8b02a6740c4da8a43dfff05dd4473b4cb8ba489bfd5ba06c1dbd3285fc0`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fe05c6734e5dc50476e722cc57112d104c24e75fa204f8dd5066a7c29c59cb`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8c07cd6938f90cd62484a4e934e8fe7ade8182db8af02e6eb697cf53ad89f`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 93.2 KB (93222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4912857a7eec07b09ab0a4fa3da525e7f87d45f9af9f5eee2da079179c129abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23220b0a9fd93875caeee52955614a1b33f553ad4f6d378f2db9f8b784bb00a8`

```dockerfile
```

-	Layers:
	-	`sha256:9972c1ef7979b6a6373c836cb171ac20e39fe3638963c57848b4f6b0c138da8a`  
		Last Modified: Thu, 05 Sep 2024 00:09:59 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc254bb1124e09a0866605b00898566346278bdda14bb13896928fd3b65b85d7`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:fbc54d1adf3df6d64fd4bf3fb9dadc8b58792b27f5b163fc227ebeec48ac94f3
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
$ docker pull neurodebian@sha256:b386e80e587d4c20ecf466054c921cfdc72aeb7e5502867ccdd6bac2d19048a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd3b8259795f4e2160852925aa7fbb7231a7e252c92696a27950f0303853dce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
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
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f475f97deaabc6193a3fa858337fe06184e11ad6b13315ab6c7f971b66a9bafc`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 6.3 MB (6287931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9fec776045441161388c757e0ad726b5ab7fbd3548e03d22fa42b727e9b782`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369688a9f2e20897b0342be14d8b6941a03ccb9fe3bb98dd6ddcfe4445ba29e`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 91.2 KB (91192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:822f4de5100bb1994064afb1cdd414af5247d0e87c51bb88c46ca6bed2dc05f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a37cb43875ddc7aa01e78a71637c84ed0a436c94162a5790e7bea0b07cc237`

```dockerfile
```

-	Layers:
	-	`sha256:8c16a39d93e2e784f37f3cbea84302594e573b2693f64b8b370f24ccf9d50237`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 3.5 MB (3542033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503cf70ae76d49b40790396ff4fbdf7b5f3daaf8b7ca72be3e759ad8e79bcacb`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1301c742eca91b58603a2667eff6b9eac6327001ed41f8a042f8618eae9c8662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b82c3e9dac515c8134f33569cc8a7c6cdaf0d6223e596d964073c16c9ffc04c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
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
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408855a53c5bbe2210b3acb92872348f336eed207c1fd565aa9a1894ae3360d7`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 6.2 MB (6248358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513957bcba9f74ca0a80d4f0d2a013c85dedaca9c3d7851562387b57f917f6d2`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b06fa225e64f5f4e0e613985a5fad9decc48bec4c0f6976a7c73a3096c5526`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda73a6bab6cbe0f0ae9577ec42d105d5e08ef05319ea5926169e01c3432901`  
		Last Modified: Thu, 05 Sep 2024 12:38:02 GMT  
		Size: 91.8 KB (91770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78765ff8458b22fec7849265d6db5e083ef24bd5997d278ca662573e4c2314fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27035daa77873055b6fe118538dab410d735292df50392b62c95dcce7efe76a`

```dockerfile
```

-	Layers:
	-	`sha256:83f31aa3a32586e88b0dd27a9dec574b3e8408e8b0e10dbc3ed2ed6c3916214c`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 3.5 MB (3533502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e375418842be8be11aa86a2f2bf098785a3774a084a21041582157fdf98117f`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:47e9bd51827b95feb3e89dafb8583ce8284ef80b888788217dd848b70dad7bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60713448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f4a1a27925112fe41435fa83cfd95c4928b7444cd5434e7dd4b8600b10bc5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
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
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be375743549e0e68564be0499e767c21b7af02c63b8ba6f9874033b7f6989ab3`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 6.6 MB (6587194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98205be1f0f5dea8ace51fc072e692d4ab82ba96a4fa4335fdebb86f2626de82`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf2c5a5226cfdbbcc8b7cf7d0fbc26605fb419d066536422b107cfcd038cac2`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bb3a2800a6b50bcbe14a55b7c4fd0b0ee771e18724d9c5161a7cf486e89064`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 91.0 KB (91010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb2ae32120e24d66fd2c6c77a0d0cb956f8efe63f86d9c563091a9e32530db17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aba443d0e9003cab1e91957153eaf624b50f534608f7beb882d2dc05b166e6`

```dockerfile
```

-	Layers:
	-	`sha256:5fc9f96a0b5046f5dc84f7d0af6bd76e7bb2feb421e41b5aa4a540df22a3fecc`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 3.5 MB (3529559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdfcc25e7f8ad25b6b9bc46f6d0ceba849c15760996ea088413aaffda4a06d4a`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:249efaf39c176e1ceefc0deb018a0690996e6e4a40886d53fb54fadaebc43e2c
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
$ docker pull neurodebian@sha256:d6385e1c5bb68d77f40e026ed12ce430380e0e470b79c3f5ccfcaefc931a7b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e776c45bc6971cf609f11e7627976f0cfe662728ec87d1d886c00188c57a3a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
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
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9932c03d465e07be767be6c6546a5fed0a8b713450009a5ae5548c52bc48a318`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 6.3 MB (6287955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa69fe5d2dbb347bcff9484d062465fb6e89f3a62b98b0ff196ed4d6799f673`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a23af6f8797bbef0455d9cd57276520bb04a5171c6203bc5a5ab3d4c88811a`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7138d16f6eeae6939426514f30129bb8016e17c4b9a24883b9440e1353b605`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 91.2 KB (91238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7203ca1b15919f54f52922c71b014e2624ac6f086d13bc8f501cb8858bbd344d`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:465aeca1f63b6dc525b5632ac6eea79aab7b6e34c2630a00249831526eda91d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4661d626714f88f865b4ae67b6b9f36d1602de01880fa1be9dfbfbd03c8d6cd`

```dockerfile
```

-	Layers:
	-	`sha256:e3e8d0820b5babfaf76c87b38d941bf58eb80d5250a65992b20ba00063fb637b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.5 MB (3542069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65c24b8306901ac0ef9a25e84ad3f7abf256dc28c444897f5eea6145f6e792b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:61b1335fe95c43cbba5331e564ed344d9a1117fadb9f2d8b7e9cda08ef005df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bb4b41d27fe8f8f38614f5f9d18334ac64546deb807d9c24f9a8bc2e7d6994`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
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
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408855a53c5bbe2210b3acb92872348f336eed207c1fd565aa9a1894ae3360d7`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 6.2 MB (6248358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513957bcba9f74ca0a80d4f0d2a013c85dedaca9c3d7851562387b57f917f6d2`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b06fa225e64f5f4e0e613985a5fad9decc48bec4c0f6976a7c73a3096c5526`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda73a6bab6cbe0f0ae9577ec42d105d5e08ef05319ea5926169e01c3432901`  
		Last Modified: Thu, 05 Sep 2024 12:38:02 GMT  
		Size: 91.8 KB (91770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f516d23c8c2424b41423a5203bfe7ee2dc27bf78f1d423bfaec155350b83b067`  
		Last Modified: Thu, 05 Sep 2024 12:38:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5abfd6e5ca6a2a3a60e3fc06b0a35c972fd31f3d60e35f3768dad4b3d718edaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b783683a14f28eebc05c5436416cd4da84c4587b6c3d69deb4e3b1e9e7997a`

```dockerfile
```

-	Layers:
	-	`sha256:cb59bdc05b436dafa348c7fe82a7d452321c84d9ae796567c4450919ca49b515`  
		Last Modified: Thu, 05 Sep 2024 12:38:23 GMT  
		Size: 3.5 MB (3533538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94fe3d7fc11ba1ba4aaafdb2d86aa83d27096203ad2c8924782d0df67b3d4a1`  
		Last Modified: Thu, 05 Sep 2024 12:38:22 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f262c8cff769b5b5310497956549cf54f5d9d71cfe7fa65799b481b869d6df13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60713808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a1dc652e1a803d21c1f7e3dfde6b5a2af5e9cebc49a802db06584b02ef4a7e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
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
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f53d49502772dd0bb2f4018a9034a0e325b9bd5f66244b738ad7515867ff34`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 6.6 MB (6587150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c740fedab1abb15223181bef8f90748bae271cea4d437f5c2f518598dae6edd7`  
		Last Modified: Thu, 05 Sep 2024 00:15:28 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823374c8ade17fe49d3c94df03cddf3b957757051a48a68d056d91a1fbdc2091`  
		Last Modified: Thu, 05 Sep 2024 00:15:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f993073d6e21d91c9082e35660a4a9afadf1ac920c59c5f3cf4c25232ba916`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 91.0 KB (91016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09943a1a6a592c8712c972bc5a4b91341501f19f6b14f36af6e8cf7dcda3ea2`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b1af0d66201c66bc02711ccfd849087130f60b5998ef91f7400a0607bbfa1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbecb14dbfbba53dea46422867f787375bcbe260c646f86cbc50b8da14a7827`

```dockerfile
```

-	Layers:
	-	`sha256:c6b7d3f4ce778effc987750d2dfd188f3f768d3db1b6ac2ccc8b8dcb95ce6af0`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 3.5 MB (3529595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bdcc3c9e286ab8883d59427bf8adfe9dc5aff9df257183bc8edfcdfa01a37a`  
		Last Modified: Thu, 05 Sep 2024 00:15:28 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:3f297160a19ea8ec16f983d5ce3171d63da3045d1b991019f8fa553acef21112
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
$ docker pull neurodebian@sha256:74236c937c5b037ad60fc432ebc254c1e580993ab29f478a9b300daa626bb915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3adae40b3c213aa1ae0712e9060a41aaf499df6ccdbd746f19223f35ec6827e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb0a6060b8b0998db2e10892443ef142934b0ef2830beee3e3e7cfe4514bd9`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11104992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d5910828d32d02f070dba4e7945868769def79e0f9902c66830608d68aa481`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be85d64ab216d005b467f6308b5615d673e978f19c236082f992bdaf4ad93bc8`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 101.2 KB (101161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bc6eb256921208f76e8b28589cf11cc18adca9cfe24fed607071a4661686462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56e3b7a65d4bc869c344278645e4b1720f997dbd966ddf3e536b74e2805f59`

```dockerfile
```

-	Layers:
	-	`sha256:29d56d4669ef53c2f9a8c6678f2b9a0ae5aca6a32c1944ff8aec60b1b297320a`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 4.2 MB (4223717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2583fb1f95ef1984a58e4586f792e94a80ff50ed736cd3b33c28bfd5be697f3f`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f8213b6341b1bd416e1b73705a77c5227eb076fbda50c1b61fcd15c711751a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64940530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5805688720b5f4b15de238d4d61f07be3d1b0eefd9289054e89a2edea0cf0d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
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
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab2fdf0b58451a0c31951dc2a87a932deed77518e2a054bf1aeb38a5a7261e`  
		Last Modified: Thu, 05 Sep 2024 12:35:11 GMT  
		Size: 11.1 MB (11105823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3cce06e7960e8ba47689bbfb2de4f89c0f135a613080c0ecb2e1000bd16804`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23140bbd52963541dd8e0e8cda7d68393aea1804ac6bffb8fcec5940e65548c8`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1608e10ac25cd129bacc060a2fe424b11ed352acf6fbe6cf25636d78d881b`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:55bc3810d671d847ecc66841d51d017ec8540ed69cbe03815513d4d976f05b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad28e0a95f8254034c3f6e0f85bddea0f76763c2a1a9b2ad5aff778d69795b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d583b4965a88051bb19cd82140b6cdf8b6061f04c587e3a03729578e52f4acf`  
		Last Modified: Thu, 05 Sep 2024 12:35:11 GMT  
		Size: 4.2 MB (4223309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa866db050febfc23f2a557d0e06f92e5c9275ed20dee19a24ea3179a6343a3`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:96fe4aae67000ad6550f8e6838709416ceab4f74feb9a1a90cff0c1d77d09d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef01da747f6f76c43b94466e8820aed5df2c186c69932d123b5ada9592911e2a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
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
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a943fde0ebcc219ed5be7a65813a44fd9ae078d1b63ebf63c5da678c99be32`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 11.5 MB (11500208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13415e438d502909f21cbd42d54392b1c1305ef218c1e306f811304d6979e7e0`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c19e1db6c281b76dbd156756d08b252509adc87346da5e11d53521a449f86`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebf1edbb66dc5cf0ded190f867405852068a545f2611eeb6af9decaec8470f6`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 101.1 KB (101061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bbd87945b96ceeba117e56bb2f8cfa4a6ec9224ad3b8f7bcf9f3c092882b83f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b42e85f12377a98e9ea3ff307f1a0e95c144db6a4aaa4d2797138ac8df80f`

```dockerfile
```

-	Layers:
	-	`sha256:125cb6ca9c69dceaeaf638763b1dee8b881dbdaaff4d69680342af0d71b50954`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 4.2 MB (4220164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefe7ff2bc097e2bcb6e8df83f2a1f83fed570e02fdb005a542c2e15d0b65ad6`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:1d4be1129dc978e893ca7f1f912b58d26e066836afa98da72b6b6c77f9e09952
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
$ docker pull neurodebian@sha256:7f5088398c7f011e8097a29cd701f675a1080cc500196391c4b6794022b8a9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdfcd7ff9d894bb20277f777c30089d05e6bee15278a392b84be6561a744ef7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781057eafc4c33d419ac01788ae0f4708e6c8b9b42b4c0efa58265084ba5c337`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11105021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9f0b8cb73e5762cef8aad324e1ee6e0a020348d975fcf9a1b709b4c3fe925`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297557466a2385d9af17a8e5e0acc6b5876c310f8717e40aa3661b00dcd1149`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0755dc4a01fa569e141b166f027a20446a1bbb2e769b0548ef4ddb92083bae`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 101.2 KB (101182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a4483fab3e6ba8071f141c5125469123ab6dcbd2c5b2d7d419005489a71053`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2af657dc55a7ddc9f14035295ebd2f147736d2fb0fab02638830682adf4479ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49ad2aa5db65dc48910c228539fe3ce366263eeafc62176ba3c49fa58b7e06`

```dockerfile
```

-	Layers:
	-	`sha256:1c2d01c9aa9c1e38c274b4f75b13960fb53e6223ec48d13adfc84fb8419989a8`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 4.2 MB (4223753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad25678c39510df32b23c842ca8358063f7fc4eb6fc0befe7ae6135f725771ce`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a9b51a2e80948cac7bbee59ea1e13ba5369969893b5d5ceb0521eb696dacb9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64940892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bee63eae38e75bc7be7dffba041e7ca7e73cae2c0e713811bc6551db1d40bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
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
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab2fdf0b58451a0c31951dc2a87a932deed77518e2a054bf1aeb38a5a7261e`  
		Last Modified: Thu, 05 Sep 2024 12:35:11 GMT  
		Size: 11.1 MB (11105823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3cce06e7960e8ba47689bbfb2de4f89c0f135a613080c0ecb2e1000bd16804`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23140bbd52963541dd8e0e8cda7d68393aea1804ac6bffb8fcec5940e65548c8`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1608e10ac25cd129bacc060a2fe424b11ed352acf6fbe6cf25636d78d881b`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bd040d3118a6dc2176423c1d31a87a6a1e1e7e868f44fcced1e796200e04d5`  
		Last Modified: Thu, 05 Sep 2024 12:35:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8fe5ebf423951de559c47fa6d007a391c4d6a39842255620507e7a89643d3464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf0a49183496dd812d4c35815772ca7d8afa88030bef74f8c5b130d4ea65bf9`

```dockerfile
```

-	Layers:
	-	`sha256:c742219d6395bd95d2f014a16537d41f6ec98d39481f7a8126835bd2d634a6ed`  
		Last Modified: Thu, 05 Sep 2024 12:35:33 GMT  
		Size: 4.2 MB (4223345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce31a0ef62db38cb1b6a25769b3a8466fed5b6b6aa09a6baac7c73f3cede77a7`  
		Last Modified: Thu, 05 Sep 2024 12:35:32 GMT  
		Size: 15.8 KB (15791 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7616dceee5aefc521c248668cfe4a6ee06908cd2c688bde93d4e1c62fe1d90d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c8fa70d35b466b7488d6a8bbee5796d005eb095ecd6343839a909543ae790`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
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
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b13fceaf30837919c83ba0eaff4811346a54e9111e8609afa66847dddc498f`  
		Last Modified: Thu, 05 Sep 2024 00:07:30 GMT  
		Size: 11.5 MB (11500195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94822419f2eee106212fd1cfb61f612f5cbb4de0cff53b8b4346661dbd7d6dcf`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72cd6ea7780d9eb88dcbf6a60de043343c71c84b38a3fd593f7c4443e9841eb`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d79df17eae45ea840c3dd3047ee6d29f0238a4f93a9e4e5dfa6bb97776be06`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 101.1 KB (101052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfec050c8598da5da9fa965646f462272eb9bdfa7a27114a560c38e4aa697d3`  
		Last Modified: Thu, 05 Sep 2024 00:07:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f459330823492f170624e082686abd94b19b9855ca680cbc804070ed438cdbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a5abdbadfd2154a3bb12d0bfcaa4d4a86ff75310e4b6c11de2c608942a4f94`

```dockerfile
```

-	Layers:
	-	`sha256:9fe7cc4755190f18ca56b92e4c52d4545aa9e9a4a32a2c49d2ddda1dca821a47`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 4.2 MB (4220200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45de231496ead48cb3e03380acd101ff2b3b7fb3eec01e567cbe03aefdda1d3`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:76657de75d2774ad7dd62dafb1bbb46c79a8a1837c2c8b049f675d7aa4f4cad4
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
$ docker pull neurodebian@sha256:c8664a96795b166095b204fa54dbf0f48b5e6e4978643e8b763bb7c05b2dae1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0c3b1ce774b89533bd30de564feff9ba4dc520f740d46ae423bc2653ea8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffec6389bcbf6537d5f6a384d29b76f4fcfd4cc7522491bbc0e1e95e5c3eb722`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 11.3 MB (11266554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc93f4d62109e8a5d2f564ccd69d7bef7d80a32aa7a410bc6363888daa816a5`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d017be4b2180bbb56d6789d0382e398768bd1b3e8f19973efa1578db0296c75`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ced1a1a098fd13cc5a63fe69b80bbeb7435fa6bbdc8331b130d68a6b87ba8`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 93.1 KB (93127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f8466efd911fc1b98e6f430f3b1aab449dad4490a17f294deec380b6afab020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78075cb443a7999c807e8fb4699f6f1c0086f081b30c2d93be94680e05390300`

```dockerfile
```

-	Layers:
	-	`sha256:f1b4f0b3cc2badb64712a79a6915ffb632e856347854c52ff14ad2fe57846900`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69c5d58fafb7ead8986e2f8e1a098fcb901d06df3df04978588846236a6382f`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c345a247dacdd96d613b963e2e3fdeb72161e5c0f5a7740992bdb9e008a4ea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60913243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e470508b10c079f238639a81b1a0e47c435bf1a64e75213f6cfca87fc7ab16`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1407873c66503c0a93617924a56b4dd8e307ce2f1c2584c89a9fa1fdb32af2e5`  
		Last Modified: Thu, 05 Sep 2024 12:36:08 GMT  
		Size: 11.2 MB (11232270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71660075504871b9d383826ce5d80aeeafa0f24ef0d028e8c70c2106e2f40295`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920d93d230ac89732db5e1368e9288d33ab00280170ed41ef415abb19e20b71`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80251e079aed2b00cf9612399cb10176c8e0143d29001b61c7468a9dfb9ce708`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be69dbe480fdadcaf18fadf575c4e568b8081c443cb058d2a983ac699af38c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809742a0e06d624313d6f4f95410ae5632623b4128683f3d68bd1a3a3c84c0c4`

```dockerfile
```

-	Layers:
	-	`sha256:12b6df0c491b4c73165be2fc940f2b5c7fa177ece053843b76b2ed5eedd97450`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b2553d87c1a9b1095a1a7cb0019d4b6626d96f473703640f98ce7e46bc8ed3`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:1f762b90a16539d08e371cf9704aab60d8f8c3bd95c833c50e21668cf75d57ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62358760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ac852c496b2f0a3d2c1faf2f58f6de35195ce64fb3ff870ba31256f00ef489`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
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
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7919eb19b12c4b3fd8c8f9fcaef0c8c8df9e67b237eaf93ea5e98cebdde9abf4`  
		Last Modified: Thu, 05 Sep 2024 00:09:59 GMT  
		Size: 11.7 MB (11688944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba9b8b02a6740c4da8a43dfff05dd4473b4cb8ba489bfd5ba06c1dbd3285fc0`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fe05c6734e5dc50476e722cc57112d104c24e75fa204f8dd5066a7c29c59cb`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8c07cd6938f90cd62484a4e934e8fe7ade8182db8af02e6eb697cf53ad89f`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 93.2 KB (93222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4912857a7eec07b09ab0a4fa3da525e7f87d45f9af9f5eee2da079179c129abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23220b0a9fd93875caeee52955614a1b33f553ad4f6d378f2db9f8b784bb00a8`

```dockerfile
```

-	Layers:
	-	`sha256:9972c1ef7979b6a6373c836cb171ac20e39fe3638963c57848b4f6b0c138da8a`  
		Last Modified: Thu, 05 Sep 2024 00:09:59 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc254bb1124e09a0866605b00898566346278bdda14bb13896928fd3b65b85d7`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:de074c6477a033b628c052824d0419e3b0a90f13a2fb4073488b3c56fa7cfe59
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
$ docker pull neurodebian@sha256:b48d6272400457ab71668d983cf66e3677f8df417b405a16646a77398ba08d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f348d52d0a30c0875589c2a9119a552d0157a52592558ed41ab0bfd3e3c77a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9051ff7592ebdf57081bea4813d054f179c10baf88e8edb1b1eb0503dc57a398`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 11.3 MB (11266587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7d938f0d1f711b7744833ba75d25ef22f306b38fed3f791d43c283332c29d`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d8d64e9f86a243cadef1fab89c4bc283c6ab4b4d7acd3c713da0063cfbc7f8`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45240937643905b587fa479f7122727e4da480a63dc938c4d4e680049d4fd520`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca5c0ab742bba3e582138550e8f5870657e878200808229861aaeff5b17eddd`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8be6a251f01d60f7c79d8354d52a880631b39d9b5e7686fa2e26ec2df80aeac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcc537a8cec282d091e002e6f0a1e677c36051a6c61478e3e8eb0454c94a884`

```dockerfile
```

-	Layers:
	-	`sha256:11250ff6b4c7bc963acdf419c612cf7ee613254e2246c5b3d2a533583138de69`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bdef147161d65fa6df17b8f42d4d1bc566bd2ca0efeceae14bea0caf771bed`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:efbdeb8b5d814d3b0da4a167795648e3e251258aeec382a14937d4ed99826943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60913673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9576bbaf4ce331301262d1e6d4a9810bd99ef004b198a7126debd55b79b3c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1407873c66503c0a93617924a56b4dd8e307ce2f1c2584c89a9fa1fdb32af2e5`  
		Last Modified: Thu, 05 Sep 2024 12:36:08 GMT  
		Size: 11.2 MB (11232270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71660075504871b9d383826ce5d80aeeafa0f24ef0d028e8c70c2106e2f40295`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920d93d230ac89732db5e1368e9288d33ab00280170ed41ef415abb19e20b71`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80251e079aed2b00cf9612399cb10176c8e0143d29001b61c7468a9dfb9ce708`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367edb1c54966400c609652e755bfdb13b1f44403b415b6f36f5848b816ba7f6`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:900367b3a0829a3505f3df1874436aa29263efaaa70664454f5f91988cd4fb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c011ed8d1fce4e65e055582847acd29b56999057e60cb5495e989ee0817c7a6`

```dockerfile
```

-	Layers:
	-	`sha256:e570ced3443d64a24e17909c417b0370d5ee898bac3f1a6ea39f4a6086ccd8f1`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb42b2ae1c5cd926ed226f5811a5371c33caac652433e2252db8c9c75c3d08b4`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1a4afcecebe4bef4caaf6087619df118f6c1c292e033583195fe045694d78fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62359183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dca3b4e9e7222f5e5153b36ebf4f2d7fa9753edac38b779988e74015695147`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
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
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3007322a25966cabf21ac5571de68c821d72acd5af0bab7e29cc49bd24fcf4e2`  
		Last Modified: Thu, 05 Sep 2024 00:09:57 GMT  
		Size: 11.7 MB (11688959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912cbec8e3e3b83e3b0ae68456830d139a8152ca87a74445b5b043d0a407752`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf715249f2d007d220402bfe1d271f2fb1f0a5a7a038325c8da0c0d76071f4c`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c7b649709ff95ab124a63a5e85dd2d68406f923eb64ea2c070ee8e90efff4b`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 93.2 KB (93199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c39ccb9d688897f6f2f421e68d389039bf4d1bd0374f30abbfe71cdff28518`  
		Last Modified: Thu, 05 Sep 2024 00:09:57 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ada24163b1b4d1e3f839b8115b1ed0645c68b9ea55e24ca934727e37e763e815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ab804dbd14fe55a29132e33f7fb879710fe7e02062c17b40e05b75229a1d2`

```dockerfile
```

-	Layers:
	-	`sha256:92daa7227caa0f20eb908642d3589981a329d915032fbb483a7516baf3d45921`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992d1d344f322d643c83815f60fa24f872e11058f6f463a541ec529076a1f76c`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:b0c1486a37f1209994f8d9bb515beac18e77554274d52a1c727a5793a95f4396
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
$ docker pull neurodebian@sha256:95b63a109fc48f08237b877fb7cffa77d61e8df22bf5a4d7791c6efd09c4ef8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe81e410768586b5492844badee22adc900027cdac5b1acf7b379c3a674edf9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
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
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267a7066a313165935bf4eaaa8b9aae312287191547d2809b4ad34773e828a5`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 6.3 MB (6280356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aafa6a0b3025fd4652316fc5e3fe6ea05e11344376a905017040b9b985cbf99`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5cb880e6abea22dd0197684015c78086ca2948c36925678e0bfe28e3465c00`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04bfec15b0903df67fad5cf467dc6eb0ca7d397677702389607bc4733e4fd4b`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 91.2 KB (91221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3320834de6354f493c1d82186351c117223665c2f4ead32bb77e28427b89eee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4e2f5a80b3b29afc74f04e8902b4b3c96a67b973d863de928e9726e32f9c8`

```dockerfile
```

-	Layers:
	-	`sha256:a20598f20436ee588f58c36585795a38adaac735394605a913cfb849c611cdeb`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 3.5 MB (3542857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1088db98014479771d8f0b3f7e94eab159c63f2a9e60f1ec223437d6c43cde04`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:24f342338693401867984d4213b28204174e6ccf76471ebfc022e3521c50aebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59929801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31656353606939c2c9507aee5d213b058e365d96868f1e632e95e19b0eb59275`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
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
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859f4127dbb6bd4852281e126959ee094bd68ff8be42d017e6a181f73ead3bb`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 6.2 MB (6241747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955f83e1df90f8ef2d13b780bebc31587035c53b36c3b3725fdf8080c96a672`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab66138a8cc3cda808f2ce60f4397ab57039ee7ec2d135069398bd4cb72b73c`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3975fb056504c89c026f526d8570509d6e32ba72d8a4328e7357324341d27d`  
		Last Modified: Thu, 05 Sep 2024 12:37:06 GMT  
		Size: 91.7 KB (91726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a42d885a5824bbca2af41d1a2297c2b7af5d711318c95b685208c3240a589104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e353a3f7f8b3be0323de7942e5bb14fe2ddfa0ad6711fe13e70d548621781655`

```dockerfile
```

-	Layers:
	-	`sha256:6c3ac198298f0c5bf1cf94953bcd4e554b44ee4a12c4b42b347d84692c2e45b7`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 3.5 MB (3534326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c738f9aa2fdecd457fd176654a9c5bc2ff542bb1a9f8d70983e0fc37d4045f`  
		Last Modified: Thu, 05 Sep 2024 12:37:04 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:8c6f454fc37a587a37624240f1acd6d8dbf71d5c92ac97f493552153d17fa9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60690275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9f707f5d52c73d7b0994b2358dbf7b4d9b644478517495c838e2051b32596c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
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
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1333c78cbfd9aa52271e569479d48c943ad9147e43a75caf4a8cae6c51a`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 6.6 MB (6572980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6b4321ab18ed6a12a8a49996eb7eaf67fc9fc9db20ba96a3214a3d80b865c8`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8051b1ddfe08bc83e829b01b93c1f7dfd61e675799ab4cf86d902006a595637`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc98573a9f3b01e547fed3a2007311d20d901fb130257ed478663d1c22c1dea`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 91.0 KB (91023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff488a69e1a4da2f2c98f8a1dbc2c21aff9925cd26db0669f340f7dcbb8ce9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301b4be982550abdc5bdbae672d097cd83368244bba2b73beae3c0a031a62287`

```dockerfile
```

-	Layers:
	-	`sha256:9659a39acdf1d37656ff78a42feb51c0465863f64de1cdd905cf0b9ae53cd6ab`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 3.5 MB (3530382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:303a1eb21faa30f54762d880b213c9b9a2fa67fbd348e157b296527b9310f4b8`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:70941b32ec07091db7972c1630ba676b5b8151a0a92357806b82a026350e4465
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
$ docker pull neurodebian@sha256:b1f199d03815d48bab11ecaeeacd81e4b2ac39a65aec462dfe763fb7529d3789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2893f89434279438492df27d6533582a320166e62af2248cf9c6b82914766bad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
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
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b19379603d098a671eb23697522873f6e76947ab42375d6822c5b0a4b6e809`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 6.3 MB (6280319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0c24d6a8e14e4685405a8aaf43a7ab30aa29e0e1f283aa98a3d7449868222`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b7a35dec8f5dd32abe5be6043a56585b31eede2c1645904e76cc3a0482af1a`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d57f109b0de41f938f7878759736faec767e84dac89736dbe1be92533a9acae`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 91.2 KB (91225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e14b1c01ac31d1c91fa43ae686e8efeb1145d926c79601a652e7726aae0434b`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15c88b06753416b8a2d15c8ec809ecbdb6754fdf950e7164e5fecc310c199b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d92db2beeb0a5cd44fee711408904a5286a853e7f5a750d1ad67c91a5b7482a`

```dockerfile
```

-	Layers:
	-	`sha256:413a52dce277246c096155463956e28af6833eaec6061b111fe35a78cd5126dc`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 3.5 MB (3542893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b06258c0c750ae4d23c85317f3cf98f715296d195230122d9ca927b48c27b20`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8a704ab2a66bedd6d545216d003cd9c9ecf32438627d95f7c047de9514cc09ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59930227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec7d8e42f5d698d453c52c0e3c5b95182ebe92ce4f3ff0d418bc8ee51cd21e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
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
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859f4127dbb6bd4852281e126959ee094bd68ff8be42d017e6a181f73ead3bb`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 6.2 MB (6241747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955f83e1df90f8ef2d13b780bebc31587035c53b36c3b3725fdf8080c96a672`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab66138a8cc3cda808f2ce60f4397ab57039ee7ec2d135069398bd4cb72b73c`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3975fb056504c89c026f526d8570509d6e32ba72d8a4328e7357324341d27d`  
		Last Modified: Thu, 05 Sep 2024 12:37:06 GMT  
		Size: 91.7 KB (91726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c6a231b4ae5e9400a3674313b29fa6bb199e56c37c44a7604322ec1dba65dc`  
		Last Modified: Thu, 05 Sep 2024 12:37:27 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7e548e1427eb6fc2d9a7a8feee437a55ff3ead5c3e8380688294479911ddce40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05445c5a5d254af676048b62bd4c259bac7cf7ee009c6a869ecd4663da883c6`

```dockerfile
```

-	Layers:
	-	`sha256:97b0afd3517a47d8760e79a48c134bbf27216a34c50cfdcf9f69ca816e61b898`  
		Last Modified: Thu, 05 Sep 2024 12:37:27 GMT  
		Size: 3.5 MB (3534362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d586a8f30275c37115efb6b53ccb770a331afdf2710b998e8c032b26fb202355`  
		Last Modified: Thu, 05 Sep 2024 12:37:27 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:68b54664e3866cc705204223f34e3b14687d203d5d8c4ccb41d48a81f93cedfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60690777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ecf48c44eeb66c35ca0c57c59bea6b4f55484c38154fdbe47d4f5a3a0da326`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
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
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6dbe168d1cbed58c86837c3c4e445deb7290ec698957ef32f5871b9708532c`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bba1583506d4cdbc507d7cc5fffa09a2d9182d563c6773b582cd5a11ddba1a6`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599299994105b13034a726b2027742dfa6c475364a0fb2af06e771388ee88540`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b8d36492ad7711b0cd10c10c8006d7288a6bbfc26cf33de3dbc6b4d8838fc0`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 91.1 KB (91064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048a377a5d58435f09efc2825d6314ff49bb86ccc8095cbdf3c9db7213d852b6`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78656ca2d10386314de4b1fce30ed2e6cbacbe7ef364b24e35c52c26191db06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdadccd02e0062c0e688529e7768b067ed807a1977bd6a231c79fc058c2637e`

```dockerfile
```

-	Layers:
	-	`sha256:e109f57e1ad3ea88bd73422a34f6383337b13ad53168635fa526b691ade511cf`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 3.5 MB (3530418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf143c4f772bceb5e893f350906929badd77d0929c34a2a5173497b82a00535`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
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
$ docker pull neurodebian@sha256:8cd25968c7a8dda57e86f5f31179a392780c365d049c245f1563df254a345b6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:b5e2ad2679d21dfb98319132904ff13815643d741d29c2cbd61f795d2cfce2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03035b5fafec30a11ccaf9e676191d30bf2a93a2c961ae50bcdeae21ecee68c`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e5fc20939f49ca46aaa63fda94b740a46522034dd33a99dc846c2ab47da385`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 3.6 MB (3622683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d7c12d3dff8024cc7a65a06760eefef7523e92d4ab01561da2876474be6e25`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257f9b0966cd5484318ba1e2300bcf4102ad856d15cf79307d6575cb919be75d`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25429882efb06104ffa477fe41e22a29ad87a1b8b5a97eddc221fb3cfb85bc29`  
		Last Modified: Tue, 17 Sep 2024 00:58:50 GMT  
		Size: 110.0 KB (110041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d732e29d091ef7f0e630eef553f727bdf00995f77c7dcc07b0561d4792f4341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb4b42740c8b876bb56d509444cd2d22fd632ea9c6254cf4af8ef60cb72b5aa`

```dockerfile
```

-	Layers:
	-	`sha256:46449a2a17035de35151d0f04752a18008bd77cdb9bd76b7f1465ab848857267`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 2.0 MB (2041055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f62c1b512cec8166de552b1e0085eb7526f3474781a15c9cfadf62c2436da`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2e8ddba19dffa270b72c0c17efca5bea22c862945352f06ad9391ca69ae180ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64399ffc86a2a302a5f8b07efe84fa560a195e25878c4a52e8f5d97367769e`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:769792b0a9ae99abbe1b81296f09e1e53c2e662643848544f1a641d54f8b29bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ab15b050723ad8ecd0ff560efdd18d3d1451cbd92375f54cf16c418e647366`

```dockerfile
```

-	Layers:
	-	`sha256:2a92568efc9bccb357a48dc2f8cc5ef4f0d34112762744fc1408de6d45f8e34a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 2.0 MB (2041314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783fe908caebc3d7a05968a298b4c97dd56aff0cc5841272d2f31f8d0eac4efd`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:c35390a21d7dcdaa5248caedb0c2d1d3f2b9a31a1ccc6a5fd082bc8262ef35a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e45ad58f9dc146f7c58fee7c828c3c6831e76bdb9cf7020f9f7c9448d53671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4ea79fb23e81c99deef7e3da0330d8995389a5ed5528314613545bbc38a650`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e444df7ecce18d9b6a39b30f8f893e46de9a6c8393753ceb73f80be5147d5e`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 3.6 MB (3622684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eb688a315dc9dc281db41ae45a5e1651f96d5b6b93100b8f6b3604a1b7be90`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18efaf2abf8b145da9341e025a8599685148d724adf71187513efcefdc1eb92b`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c03e7463fe28779caf76a60210e080067f4e00e4a28d1ef22b5f71aab3511f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 110.0 KB (110044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a748ff3cbe6a5eed1e2b979d6648c667fb7a29be6b3e2bc14ea06d88519a0592`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49d3a7c89f96056348bc2f29c7aaab1b27bde7d7755e5cea5fe7102dbc63a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0141b248fd4a83635efee725ebffc6599bb6e48aedbb01287016be2df2e9e29d`

```dockerfile
```

-	Layers:
	-	`sha256:2aa3ae2b7c2d8c84a96d9dfae22e8bdbef344f1dea22754309dafd7d8ba3fa7f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 2.0 MB (2041091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48b6d14af7ecf44b9066d810db720df1078da0e69b612cc31771ef41b2957b4a`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4a2bedc35b23fd303d37b492a4dcd265b749cc561bed81266ef4fd4f072ca3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cc596bfd27c527f722fd0f60344b7c29c0ede0e0215ca28663dd6f7b11334d`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0571d1820815c6ffe6445310d6d56c0904985a7a40ce55ea60111c7ab14c14af`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15e423dc66f68b2fd18342bafd40c16c24df1ff2d5a105e3d23fe7a7b66e4859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14030ec66c96db8f89c291fc02780ff4e9dd29fbe18b7deeb19f1a70811d83`

```dockerfile
```

-	Layers:
	-	`sha256:b8a537c7762547e63f17b420cb0912f491db0829af8089494798ac00e311b1a7`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 2.0 MB (2041350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab7d3d2aaba018f1a288d03ac3c709c72564deb83d89ee6d4197767b31a448c9`  
		Last Modified: Tue, 17 Sep 2024 02:37:08 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:ee18673f76356076cfcf2f447dc62ff644577cdd1227dc852c72b5f5d11dc753
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:cb400b6ceca5598c89e075235d9d97801bbc3dd3c1fd28e6b9e9f68ba9673bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57418e72bf3203e66f9ef72696a2311cbe51c6afd3f6ddbed74f77b91ca281ce`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df64aaba98e3e322c8854e81b959d56d16c0f7de70d6ffa765cb22a6dc49a1e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 3.6 MB (3557850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa49aeefd415b68360c4c5cef36758ff95c2fbe7e7105a4bc9569b0e3238e40a`  
		Last Modified: Tue, 17 Sep 2024 00:59:04 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9765a679a95113edbc79eea58c1fd72da3a6cf7b53b1f2a04a54375efb667bd`  
		Last Modified: Tue, 17 Sep 2024 00:59:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eab27635ea7dfa523ecf8850649efa560f95f35cd3f1142303acdcefcda360`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 100.8 KB (100783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:006134278094b57fbe8c2a16998d1c7dabbd0b62d919c12af997cba9788a07a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1985830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30944c1cd03b3e43ca215b7f0bccf4a4e1be93c239f59755bbea479aade17b56`

```dockerfile
```

-	Layers:
	-	`sha256:a9e318e1936b600f2a75e263d997c3017346ac59a39327ac8a3e8f9f00186325`  
		Last Modified: Tue, 17 Sep 2024 00:59:04 GMT  
		Size: 2.0 MB (1972424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b87cabc7984d7b38fa197436a89a25a4c0bcd0bad8a625f5b14d47aa9d2108`  
		Last Modified: Tue, 17 Sep 2024 00:59:04 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:65837f91add6c22c735706ad698ccb4a8842af6a6f804de4fcc8df8398636d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6552f557704928f464c1a4a90f46347f2442bdf4f1473f6b6408907b08a2f2d7`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c528017e91f5cc5b749ba6a5ec49b1489007f526dc76de4c0688bfd375bfe0`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 3.6 MB (3557058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c57f0202bd48996c76cfe8353658159a0b6dd4d6b5e6ddddb74d09f05c99d2c`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc219592e3ead1bb1eed844d765bf20908729bfc04fee856a3e634117a55775`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3184f62146b23536c694b0b1487ca2ca56d879fcdccd4ec791f4058c2dd3b1`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 101.5 KB (101455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e3e4d483c5c3161abfe6fae9031cc3e8abfe726b574234cdda9e1d8c4d140fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15757bf4144711c461ad3518a2397c679a0c60c5145db479c623f4409fe49c3d`

```dockerfile
```

-	Layers:
	-	`sha256:3e4624db212bd15f229bc43cf3171557de5603d7b3578c5ef817dc663ea4aaee`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 2.0 MB (1973469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55aaaa53afe2be43515f82621864734bed2479bf5db43e8b0ea80b7475575325`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:845fc301b50b3a4b33d732bf49776c2807a93443addebba44f5c7f4269984f07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:902584d42edb09004a9e5383f587fe24af4a1b858ee7605b41cb023748c7b235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f57abafa53d93a11fbefd1ea690e5f81b6f58a8e48d1b67dff4c6109122c8e7`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc75ff17550db8092fab7604c10c333e70e266250c3c6b5cd72078163d4f54f7`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 3.6 MB (3557848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef545aca17bc58d9ef369f44978f6e8f60e7957edd0b07720f1e3fc3ce9da6d2`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e911b14becd8d48a3394b3a7c3d008b0d39a665a6502940e4f90cc7f22daf722`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ad1ffad3d8688a24df2a5c36bd814db53aea8d81e55acf6d835f1d21854ff`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 100.8 KB (100792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf93a5f832a83fc1a9c58d63fc2acc8974ac31be816a46a9a5299f8455734885`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:de451eaf65788cb2cf6f6470bfd842f657606fc0a997767325734611e7d67024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb7c702d37d6e2a3b7ec989cfd751d64c90c79bbe5b73aab42d165ebd99dc45`

```dockerfile
```

-	Layers:
	-	`sha256:a4e2abdc14936826569b84a572f1d6118e38ae5bb3b3945147939208558c316c`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 2.0 MB (1972460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce2e7e7acb9ad9203d0df753d4faeaa1d69c7939bb23e8652b2a1b6e4007c609`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3e068103f646ddbaad20b5f20894956f2f5e4345dd1d595b07dec8569fd8e940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327e318c15a3ec8c08cd9ead5bc3f374cdc18b8f8b3146d9c9767653c57b999d`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c528017e91f5cc5b749ba6a5ec49b1489007f526dc76de4c0688bfd375bfe0`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 3.6 MB (3557058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c57f0202bd48996c76cfe8353658159a0b6dd4d6b5e6ddddb74d09f05c99d2c`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc219592e3ead1bb1eed844d765bf20908729bfc04fee856a3e634117a55775`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3184f62146b23536c694b0b1487ca2ca56d879fcdccd4ec791f4058c2dd3b1`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 101.5 KB (101455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68314c34f4fa65ac887a7a463599e146b0fb4c427d8220080ae58e0cbc4f5d8`  
		Last Modified: Tue, 17 Sep 2024 02:38:01 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0cf913ff9a905be7f50416b9e880c2b350910991bfcaef1d01911c3a5fd90421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4a6223227a7c54909df5d683305dbafa0d76769d93d888a4a35851fdf29b64`

```dockerfile
```

-	Layers:
	-	`sha256:85f43e35566d9283c13fceb5b831b128e4aaf4e9b030092671b58b0b1ea5a064`  
		Last Modified: Tue, 17 Sep 2024 02:38:01 GMT  
		Size: 2.0 MB (1973505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff155ee4650cb60df1a2ed11bfbb0354d610444f61bdca7ca8f7693025d11bf9`  
		Last Modified: Tue, 17 Sep 2024 02:38:00 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:ee18673f76356076cfcf2f447dc62ff644577cdd1227dc852c72b5f5d11dc753
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:cb400b6ceca5598c89e075235d9d97801bbc3dd3c1fd28e6b9e9f68ba9673bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57418e72bf3203e66f9ef72696a2311cbe51c6afd3f6ddbed74f77b91ca281ce`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df64aaba98e3e322c8854e81b959d56d16c0f7de70d6ffa765cb22a6dc49a1e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 3.6 MB (3557850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa49aeefd415b68360c4c5cef36758ff95c2fbe7e7105a4bc9569b0e3238e40a`  
		Last Modified: Tue, 17 Sep 2024 00:59:04 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9765a679a95113edbc79eea58c1fd72da3a6cf7b53b1f2a04a54375efb667bd`  
		Last Modified: Tue, 17 Sep 2024 00:59:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eab27635ea7dfa523ecf8850649efa560f95f35cd3f1142303acdcefcda360`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 100.8 KB (100783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:006134278094b57fbe8c2a16998d1c7dabbd0b62d919c12af997cba9788a07a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1985830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30944c1cd03b3e43ca215b7f0bccf4a4e1be93c239f59755bbea479aade17b56`

```dockerfile
```

-	Layers:
	-	`sha256:a9e318e1936b600f2a75e263d997c3017346ac59a39327ac8a3e8f9f00186325`  
		Last Modified: Tue, 17 Sep 2024 00:59:04 GMT  
		Size: 2.0 MB (1972424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b87cabc7984d7b38fa197436a89a25a4c0bcd0bad8a625f5b14d47aa9d2108`  
		Last Modified: Tue, 17 Sep 2024 00:59:04 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:65837f91add6c22c735706ad698ccb4a8842af6a6f804de4fcc8df8398636d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6552f557704928f464c1a4a90f46347f2442bdf4f1473f6b6408907b08a2f2d7`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c528017e91f5cc5b749ba6a5ec49b1489007f526dc76de4c0688bfd375bfe0`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 3.6 MB (3557058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c57f0202bd48996c76cfe8353658159a0b6dd4d6b5e6ddddb74d09f05c99d2c`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc219592e3ead1bb1eed844d765bf20908729bfc04fee856a3e634117a55775`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3184f62146b23536c694b0b1487ca2ca56d879fcdccd4ec791f4058c2dd3b1`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 101.5 KB (101455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e3e4d483c5c3161abfe6fae9031cc3e8abfe726b574234cdda9e1d8c4d140fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15757bf4144711c461ad3518a2397c679a0c60c5145db479c623f4409fe49c3d`

```dockerfile
```

-	Layers:
	-	`sha256:3e4624db212bd15f229bc43cf3171557de5603d7b3578c5ef817dc663ea4aaee`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 2.0 MB (1973469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55aaaa53afe2be43515f82621864734bed2479bf5db43e8b0ea80b7475575325`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:845fc301b50b3a4b33d732bf49776c2807a93443addebba44f5c7f4269984f07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:902584d42edb09004a9e5383f587fe24af4a1b858ee7605b41cb023748c7b235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f57abafa53d93a11fbefd1ea690e5f81b6f58a8e48d1b67dff4c6109122c8e7`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc75ff17550db8092fab7604c10c333e70e266250c3c6b5cd72078163d4f54f7`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 3.6 MB (3557848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef545aca17bc58d9ef369f44978f6e8f60e7957edd0b07720f1e3fc3ce9da6d2`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e911b14becd8d48a3394b3a7c3d008b0d39a665a6502940e4f90cc7f22daf722`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ad1ffad3d8688a24df2a5c36bd814db53aea8d81e55acf6d835f1d21854ff`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 100.8 KB (100792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf93a5f832a83fc1a9c58d63fc2acc8974ac31be816a46a9a5299f8455734885`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:de451eaf65788cb2cf6f6470bfd842f657606fc0a997767325734611e7d67024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb7c702d37d6e2a3b7ec989cfd751d64c90c79bbe5b73aab42d165ebd99dc45`

```dockerfile
```

-	Layers:
	-	`sha256:a4e2abdc14936826569b84a572f1d6118e38ae5bb3b3945147939208558c316c`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 2.0 MB (1972460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce2e7e7acb9ad9203d0df753d4faeaa1d69c7939bb23e8652b2a1b6e4007c609`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3e068103f646ddbaad20b5f20894956f2f5e4345dd1d595b07dec8569fd8e940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327e318c15a3ec8c08cd9ead5bc3f374cdc18b8f8b3146d9c9767653c57b999d`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c528017e91f5cc5b749ba6a5ec49b1489007f526dc76de4c0688bfd375bfe0`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 3.6 MB (3557058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c57f0202bd48996c76cfe8353658159a0b6dd4d6b5e6ddddb74d09f05c99d2c`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc219592e3ead1bb1eed844d765bf20908729bfc04fee856a3e634117a55775`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3184f62146b23536c694b0b1487ca2ca56d879fcdccd4ec791f4058c2dd3b1`  
		Last Modified: Tue, 17 Sep 2024 02:37:40 GMT  
		Size: 101.5 KB (101455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68314c34f4fa65ac887a7a463599e146b0fb4c427d8220080ae58e0cbc4f5d8`  
		Last Modified: Tue, 17 Sep 2024 02:38:01 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0cf913ff9a905be7f50416b9e880c2b350910991bfcaef1d01911c3a5fd90421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4a6223227a7c54909df5d683305dbafa0d76769d93d888a4a35851fdf29b64`

```dockerfile
```

-	Layers:
	-	`sha256:85f43e35566d9283c13fceb5b831b128e4aaf4e9b030092671b58b0b1ea5a064`  
		Last Modified: Tue, 17 Sep 2024 02:38:01 GMT  
		Size: 2.0 MB (1973505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff155ee4650cb60df1a2ed11bfbb0354d610444f61bdca7ca8f7693025d11bf9`  
		Last Modified: Tue, 17 Sep 2024 02:38:00 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:de074c6477a033b628c052824d0419e3b0a90f13a2fb4073488b3c56fa7cfe59
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
$ docker pull neurodebian@sha256:b48d6272400457ab71668d983cf66e3677f8df417b405a16646a77398ba08d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f348d52d0a30c0875589c2a9119a552d0157a52592558ed41ab0bfd3e3c77a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9051ff7592ebdf57081bea4813d054f179c10baf88e8edb1b1eb0503dc57a398`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 11.3 MB (11266587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7d938f0d1f711b7744833ba75d25ef22f306b38fed3f791d43c283332c29d`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d8d64e9f86a243cadef1fab89c4bc283c6ab4b4d7acd3c713da0063cfbc7f8`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45240937643905b587fa479f7122727e4da480a63dc938c4d4e680049d4fd520`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca5c0ab742bba3e582138550e8f5870657e878200808229861aaeff5b17eddd`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8be6a251f01d60f7c79d8354d52a880631b39d9b5e7686fa2e26ec2df80aeac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcc537a8cec282d091e002e6f0a1e677c36051a6c61478e3e8eb0454c94a884`

```dockerfile
```

-	Layers:
	-	`sha256:11250ff6b4c7bc963acdf419c612cf7ee613254e2246c5b3d2a533583138de69`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bdef147161d65fa6df17b8f42d4d1bc566bd2ca0efeceae14bea0caf771bed`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:efbdeb8b5d814d3b0da4a167795648e3e251258aeec382a14937d4ed99826943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60913673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9576bbaf4ce331301262d1e6d4a9810bd99ef004b198a7126debd55b79b3c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1407873c66503c0a93617924a56b4dd8e307ce2f1c2584c89a9fa1fdb32af2e5`  
		Last Modified: Thu, 05 Sep 2024 12:36:08 GMT  
		Size: 11.2 MB (11232270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71660075504871b9d383826ce5d80aeeafa0f24ef0d028e8c70c2106e2f40295`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920d93d230ac89732db5e1368e9288d33ab00280170ed41ef415abb19e20b71`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80251e079aed2b00cf9612399cb10176c8e0143d29001b61c7468a9dfb9ce708`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367edb1c54966400c609652e755bfdb13b1f44403b415b6f36f5848b816ba7f6`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:900367b3a0829a3505f3df1874436aa29263efaaa70664454f5f91988cd4fb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c011ed8d1fce4e65e055582847acd29b56999057e60cb5495e989ee0817c7a6`

```dockerfile
```

-	Layers:
	-	`sha256:e570ced3443d64a24e17909c417b0370d5ee898bac3f1a6ea39f4a6086ccd8f1`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb42b2ae1c5cd926ed226f5811a5371c33caac652433e2252db8c9c75c3d08b4`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1a4afcecebe4bef4caaf6087619df118f6c1c292e033583195fe045694d78fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62359183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dca3b4e9e7222f5e5153b36ebf4f2d7fa9753edac38b779988e74015695147`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
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
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3007322a25966cabf21ac5571de68c821d72acd5af0bab7e29cc49bd24fcf4e2`  
		Last Modified: Thu, 05 Sep 2024 00:09:57 GMT  
		Size: 11.7 MB (11688959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912cbec8e3e3b83e3b0ae68456830d139a8152ca87a74445b5b043d0a407752`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf715249f2d007d220402bfe1d271f2fb1f0a5a7a038325c8da0c0d76071f4c`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c7b649709ff95ab124a63a5e85dd2d68406f923eb64ea2c070ee8e90efff4b`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 93.2 KB (93199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c39ccb9d688897f6f2f421e68d389039bf4d1bd0374f30abbfe71cdff28518`  
		Last Modified: Thu, 05 Sep 2024 00:09:57 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ada24163b1b4d1e3f839b8115b1ed0645c68b9ea55e24ca934727e37e763e815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ab804dbd14fe55a29132e33f7fb879710fe7e02062c17b40e05b75229a1d2`

```dockerfile
```

-	Layers:
	-	`sha256:92daa7227caa0f20eb908642d3589981a329d915032fbb483a7516baf3d45921`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992d1d344f322d643c83815f60fa24f872e11058f6f463a541ec529076a1f76c`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:fbc54d1adf3df6d64fd4bf3fb9dadc8b58792b27f5b163fc227ebeec48ac94f3
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
$ docker pull neurodebian@sha256:b386e80e587d4c20ecf466054c921cfdc72aeb7e5502867ccdd6bac2d19048a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd3b8259795f4e2160852925aa7fbb7231a7e252c92696a27950f0303853dce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
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
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f475f97deaabc6193a3fa858337fe06184e11ad6b13315ab6c7f971b66a9bafc`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 6.3 MB (6287931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9fec776045441161388c757e0ad726b5ab7fbd3548e03d22fa42b727e9b782`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369688a9f2e20897b0342be14d8b6941a03ccb9fe3bb98dd6ddcfe4445ba29e`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 91.2 KB (91192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:822f4de5100bb1994064afb1cdd414af5247d0e87c51bb88c46ca6bed2dc05f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a37cb43875ddc7aa01e78a71637c84ed0a436c94162a5790e7bea0b07cc237`

```dockerfile
```

-	Layers:
	-	`sha256:8c16a39d93e2e784f37f3cbea84302594e573b2693f64b8b370f24ccf9d50237`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 3.5 MB (3542033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503cf70ae76d49b40790396ff4fbdf7b5f3daaf8b7ca72be3e759ad8e79bcacb`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1301c742eca91b58603a2667eff6b9eac6327001ed41f8a042f8618eae9c8662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b82c3e9dac515c8134f33569cc8a7c6cdaf0d6223e596d964073c16c9ffc04c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
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
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408855a53c5bbe2210b3acb92872348f336eed207c1fd565aa9a1894ae3360d7`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 6.2 MB (6248358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513957bcba9f74ca0a80d4f0d2a013c85dedaca9c3d7851562387b57f917f6d2`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b06fa225e64f5f4e0e613985a5fad9decc48bec4c0f6976a7c73a3096c5526`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda73a6bab6cbe0f0ae9577ec42d105d5e08ef05319ea5926169e01c3432901`  
		Last Modified: Thu, 05 Sep 2024 12:38:02 GMT  
		Size: 91.8 KB (91770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78765ff8458b22fec7849265d6db5e083ef24bd5997d278ca662573e4c2314fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27035daa77873055b6fe118538dab410d735292df50392b62c95dcce7efe76a`

```dockerfile
```

-	Layers:
	-	`sha256:83f31aa3a32586e88b0dd27a9dec574b3e8408e8b0e10dbc3ed2ed6c3916214c`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 3.5 MB (3533502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e375418842be8be11aa86a2f2bf098785a3774a084a21041582157fdf98117f`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:47e9bd51827b95feb3e89dafb8583ce8284ef80b888788217dd848b70dad7bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60713448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f4a1a27925112fe41435fa83cfd95c4928b7444cd5434e7dd4b8600b10bc5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
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
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be375743549e0e68564be0499e767c21b7af02c63b8ba6f9874033b7f6989ab3`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 6.6 MB (6587194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98205be1f0f5dea8ace51fc072e692d4ab82ba96a4fa4335fdebb86f2626de82`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf2c5a5226cfdbbcc8b7cf7d0fbc26605fb419d066536422b107cfcd038cac2`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bb3a2800a6b50bcbe14a55b7c4fd0b0ee771e18724d9c5161a7cf486e89064`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 91.0 KB (91010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb2ae32120e24d66fd2c6c77a0d0cb956f8efe63f86d9c563091a9e32530db17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aba443d0e9003cab1e91957153eaf624b50f534608f7beb882d2dc05b166e6`

```dockerfile
```

-	Layers:
	-	`sha256:5fc9f96a0b5046f5dc84f7d0af6bd76e7bb2feb421e41b5aa4a540df22a3fecc`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 3.5 MB (3529559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdfcc25e7f8ad25b6b9bc46f6d0ceba849c15760996ea088413aaffda4a06d4a`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:249efaf39c176e1ceefc0deb018a0690996e6e4a40886d53fb54fadaebc43e2c
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
$ docker pull neurodebian@sha256:d6385e1c5bb68d77f40e026ed12ce430380e0e470b79c3f5ccfcaefc931a7b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e776c45bc6971cf609f11e7627976f0cfe662728ec87d1d886c00188c57a3a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
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
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9932c03d465e07be767be6c6546a5fed0a8b713450009a5ae5548c52bc48a318`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 6.3 MB (6287955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa69fe5d2dbb347bcff9484d062465fb6e89f3a62b98b0ff196ed4d6799f673`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a23af6f8797bbef0455d9cd57276520bb04a5171c6203bc5a5ab3d4c88811a`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7138d16f6eeae6939426514f30129bb8016e17c4b9a24883b9440e1353b605`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 91.2 KB (91238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7203ca1b15919f54f52922c71b014e2624ac6f086d13bc8f501cb8858bbd344d`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:465aeca1f63b6dc525b5632ac6eea79aab7b6e34c2630a00249831526eda91d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4661d626714f88f865b4ae67b6b9f36d1602de01880fa1be9dfbfbd03c8d6cd`

```dockerfile
```

-	Layers:
	-	`sha256:e3e8d0820b5babfaf76c87b38d941bf58eb80d5250a65992b20ba00063fb637b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.5 MB (3542069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65c24b8306901ac0ef9a25e84ad3f7abf256dc28c444897f5eea6145f6e792b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:61b1335fe95c43cbba5331e564ed344d9a1117fadb9f2d8b7e9cda08ef005df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bb4b41d27fe8f8f38614f5f9d18334ac64546deb807d9c24f9a8bc2e7d6994`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
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
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408855a53c5bbe2210b3acb92872348f336eed207c1fd565aa9a1894ae3360d7`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 6.2 MB (6248358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513957bcba9f74ca0a80d4f0d2a013c85dedaca9c3d7851562387b57f917f6d2`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b06fa225e64f5f4e0e613985a5fad9decc48bec4c0f6976a7c73a3096c5526`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda73a6bab6cbe0f0ae9577ec42d105d5e08ef05319ea5926169e01c3432901`  
		Last Modified: Thu, 05 Sep 2024 12:38:02 GMT  
		Size: 91.8 KB (91770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f516d23c8c2424b41423a5203bfe7ee2dc27bf78f1d423bfaec155350b83b067`  
		Last Modified: Thu, 05 Sep 2024 12:38:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5abfd6e5ca6a2a3a60e3fc06b0a35c972fd31f3d60e35f3768dad4b3d718edaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b783683a14f28eebc05c5436416cd4da84c4587b6c3d69deb4e3b1e9e7997a`

```dockerfile
```

-	Layers:
	-	`sha256:cb59bdc05b436dafa348c7fe82a7d452321c84d9ae796567c4450919ca49b515`  
		Last Modified: Thu, 05 Sep 2024 12:38:23 GMT  
		Size: 3.5 MB (3533538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94fe3d7fc11ba1ba4aaafdb2d86aa83d27096203ad2c8924782d0df67b3d4a1`  
		Last Modified: Thu, 05 Sep 2024 12:38:22 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f262c8cff769b5b5310497956549cf54f5d9d71cfe7fa65799b481b869d6df13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60713808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a1dc652e1a803d21c1f7e3dfde6b5a2af5e9cebc49a802db06584b02ef4a7e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
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
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f53d49502772dd0bb2f4018a9034a0e325b9bd5f66244b738ad7515867ff34`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 6.6 MB (6587150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c740fedab1abb15223181bef8f90748bae271cea4d437f5c2f518598dae6edd7`  
		Last Modified: Thu, 05 Sep 2024 00:15:28 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823374c8ade17fe49d3c94df03cddf3b957757051a48a68d056d91a1fbdc2091`  
		Last Modified: Thu, 05 Sep 2024 00:15:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f993073d6e21d91c9082e35660a4a9afadf1ac920c59c5f3cf4c25232ba916`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 91.0 KB (91016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09943a1a6a592c8712c972bc5a4b91341501f19f6b14f36af6e8cf7dcda3ea2`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b1af0d66201c66bc02711ccfd849087130f60b5998ef91f7400a0607bbfa1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbecb14dbfbba53dea46422867f787375bcbe260c646f86cbc50b8da14a7827`

```dockerfile
```

-	Layers:
	-	`sha256:c6b7d3f4ce778effc987750d2dfd188f3f768d3db1b6ac2ccc8b8dcb95ce6af0`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 3.5 MB (3529595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bdcc3c9e286ab8883d59427bf8adfe9dc5aff9df257183bc8edfcdfa01a37a`  
		Last Modified: Thu, 05 Sep 2024 00:15:28 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:b0c1486a37f1209994f8d9bb515beac18e77554274d52a1c727a5793a95f4396
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
$ docker pull neurodebian@sha256:95b63a109fc48f08237b877fb7cffa77d61e8df22bf5a4d7791c6efd09c4ef8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe81e410768586b5492844badee22adc900027cdac5b1acf7b379c3a674edf9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
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
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267a7066a313165935bf4eaaa8b9aae312287191547d2809b4ad34773e828a5`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 6.3 MB (6280356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aafa6a0b3025fd4652316fc5e3fe6ea05e11344376a905017040b9b985cbf99`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5cb880e6abea22dd0197684015c78086ca2948c36925678e0bfe28e3465c00`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04bfec15b0903df67fad5cf467dc6eb0ca7d397677702389607bc4733e4fd4b`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 91.2 KB (91221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3320834de6354f493c1d82186351c117223665c2f4ead32bb77e28427b89eee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4e2f5a80b3b29afc74f04e8902b4b3c96a67b973d863de928e9726e32f9c8`

```dockerfile
```

-	Layers:
	-	`sha256:a20598f20436ee588f58c36585795a38adaac735394605a913cfb849c611cdeb`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 3.5 MB (3542857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1088db98014479771d8f0b3f7e94eab159c63f2a9e60f1ec223437d6c43cde04`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:24f342338693401867984d4213b28204174e6ccf76471ebfc022e3521c50aebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59929801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31656353606939c2c9507aee5d213b058e365d96868f1e632e95e19b0eb59275`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
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
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859f4127dbb6bd4852281e126959ee094bd68ff8be42d017e6a181f73ead3bb`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 6.2 MB (6241747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955f83e1df90f8ef2d13b780bebc31587035c53b36c3b3725fdf8080c96a672`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab66138a8cc3cda808f2ce60f4397ab57039ee7ec2d135069398bd4cb72b73c`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3975fb056504c89c026f526d8570509d6e32ba72d8a4328e7357324341d27d`  
		Last Modified: Thu, 05 Sep 2024 12:37:06 GMT  
		Size: 91.7 KB (91726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a42d885a5824bbca2af41d1a2297c2b7af5d711318c95b685208c3240a589104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e353a3f7f8b3be0323de7942e5bb14fe2ddfa0ad6711fe13e70d548621781655`

```dockerfile
```

-	Layers:
	-	`sha256:6c3ac198298f0c5bf1cf94953bcd4e554b44ee4a12c4b42b347d84692c2e45b7`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 3.5 MB (3534326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c738f9aa2fdecd457fd176654a9c5bc2ff542bb1a9f8d70983e0fc37d4045f`  
		Last Modified: Thu, 05 Sep 2024 12:37:04 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:8c6f454fc37a587a37624240f1acd6d8dbf71d5c92ac97f493552153d17fa9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60690275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9f707f5d52c73d7b0994b2358dbf7b4d9b644478517495c838e2051b32596c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
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
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e1333c78cbfd9aa52271e569479d48c943ad9147e43a75caf4a8cae6c51a`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 6.6 MB (6572980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6b4321ab18ed6a12a8a49996eb7eaf67fc9fc9db20ba96a3214a3d80b865c8`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8051b1ddfe08bc83e829b01b93c1f7dfd61e675799ab4cf86d902006a595637`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc98573a9f3b01e547fed3a2007311d20d901fb130257ed478663d1c22c1dea`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 91.0 KB (91023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff488a69e1a4da2f2c98f8a1dbc2c21aff9925cd26db0669f340f7dcbb8ce9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301b4be982550abdc5bdbae672d097cd83368244bba2b73beae3c0a031a62287`

```dockerfile
```

-	Layers:
	-	`sha256:9659a39acdf1d37656ff78a42feb51c0465863f64de1cdd905cf0b9ae53cd6ab`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 3.5 MB (3530382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:303a1eb21faa30f54762d880b213c9b9a2fa67fbd348e157b296527b9310f4b8`  
		Last Modified: Thu, 05 Sep 2024 02:09:42 GMT  
		Size: 13.4 KB (13419 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:70941b32ec07091db7972c1630ba676b5b8151a0a92357806b82a026350e4465
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
$ docker pull neurodebian@sha256:b1f199d03815d48bab11ecaeeacd81e4b2ac39a65aec462dfe763fb7529d3789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2893f89434279438492df27d6533582a320166e62af2248cf9c6b82914766bad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
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
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b19379603d098a671eb23697522873f6e76947ab42375d6822c5b0a4b6e809`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 6.3 MB (6280319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0c24d6a8e14e4685405a8aaf43a7ab30aa29e0e1f283aa98a3d7449868222`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b7a35dec8f5dd32abe5be6043a56585b31eede2c1645904e76cc3a0482af1a`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d57f109b0de41f938f7878759736faec767e84dac89736dbe1be92533a9acae`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 91.2 KB (91225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e14b1c01ac31d1c91fa43ae686e8efeb1145d926c79601a652e7726aae0434b`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15c88b06753416b8a2d15c8ec809ecbdb6754fdf950e7164e5fecc310c199b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d92db2beeb0a5cd44fee711408904a5286a853e7f5a750d1ad67c91a5b7482a`

```dockerfile
```

-	Layers:
	-	`sha256:413a52dce277246c096155463956e28af6833eaec6061b111fe35a78cd5126dc`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 3.5 MB (3542893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b06258c0c750ae4d23c85317f3cf98f715296d195230122d9ca927b48c27b20`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8a704ab2a66bedd6d545216d003cd9c9ecf32438627d95f7c047de9514cc09ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59930227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec7d8e42f5d698d453c52c0e3c5b95182ebe92ce4f3ff0d418bc8ee51cd21e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
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
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859f4127dbb6bd4852281e126959ee094bd68ff8be42d017e6a181f73ead3bb`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 6.2 MB (6241747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955f83e1df90f8ef2d13b780bebc31587035c53b36c3b3725fdf8080c96a672`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab66138a8cc3cda808f2ce60f4397ab57039ee7ec2d135069398bd4cb72b73c`  
		Last Modified: Thu, 05 Sep 2024 12:37:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3975fb056504c89c026f526d8570509d6e32ba72d8a4328e7357324341d27d`  
		Last Modified: Thu, 05 Sep 2024 12:37:06 GMT  
		Size: 91.7 KB (91726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c6a231b4ae5e9400a3674313b29fa6bb199e56c37c44a7604322ec1dba65dc`  
		Last Modified: Thu, 05 Sep 2024 12:37:27 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7e548e1427eb6fc2d9a7a8feee437a55ff3ead5c3e8380688294479911ddce40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05445c5a5d254af676048b62bd4c259bac7cf7ee009c6a869ecd4663da883c6`

```dockerfile
```

-	Layers:
	-	`sha256:97b0afd3517a47d8760e79a48c134bbf27216a34c50cfdcf9f69ca816e61b898`  
		Last Modified: Thu, 05 Sep 2024 12:37:27 GMT  
		Size: 3.5 MB (3534362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d586a8f30275c37115efb6b53ccb770a331afdf2710b998e8c032b26fb202355`  
		Last Modified: Thu, 05 Sep 2024 12:37:27 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:68b54664e3866cc705204223f34e3b14687d203d5d8c4ccb41d48a81f93cedfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60690777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ecf48c44eeb66c35ca0c57c59bea6b4f55484c38154fdbe47d4f5a3a0da326`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
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
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6dbe168d1cbed58c86837c3c4e445deb7290ec698957ef32f5871b9708532c`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bba1583506d4cdbc507d7cc5fffa09a2d9182d563c6773b582cd5a11ddba1a6`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599299994105b13034a726b2027742dfa6c475364a0fb2af06e771388ee88540`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b8d36492ad7711b0cd10c10c8006d7288a6bbfc26cf33de3dbc6b4d8838fc0`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 91.1 KB (91064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048a377a5d58435f09efc2825d6314ff49bb86ccc8095cbdf3c9db7213d852b6`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78656ca2d10386314de4b1fce30ed2e6cbacbe7ef364b24e35c52c26191db06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdadccd02e0062c0e688529e7768b067ed807a1977bd6a231c79fc058c2637e`

```dockerfile
```

-	Layers:
	-	`sha256:e109f57e1ad3ea88bd73422a34f6383337b13ad53168635fa526b691ade511cf`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 3.5 MB (3530418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf143c4f772bceb5e893f350906929badd77d0929c34a2a5173497b82a00535`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json
