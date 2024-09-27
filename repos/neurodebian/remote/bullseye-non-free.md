## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:dd06c71912068499b62ddd2f8d1c48c8aa05aec07878fb276f79252feba79ac2
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
$ docker pull neurodebian@sha256:cc787f8d6b0791659d572b06a5fa980290626e3bc3a421b9acb3f75d23234707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64943125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cccdc0177ad7abcdb5602cd2d8f3a5013b464ca19336c1f0bfa4ba7e2c0bf60`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fa9c49640a7a5333f3fea4cc6c5d10542a152ab8c5aa29cf3ce4e3238ef84`  
		Last Modified: Fri, 27 Sep 2024 15:27:29 GMT  
		Size: 11.1 MB (11105819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f59383dbb4959374257665f63dc2bbb1a4b567e04ad57c7117f913c3b10ff`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e727a822f540249948c259f1aa14d33f2495d123ea9d71a46ae031dad3f2dfa`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605ac67eae58773d4ea2de3dbfe0fcd786ceb75b482cf2659454fc879955761a`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b2d89999965d2abe6c3956d01d734a83db7ed22ad6c44fca949da5078f4f62`  
		Last Modified: Fri, 27 Sep 2024 15:27:50 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:21e3436984d7178e7def5e7e4340ac7bd783a5bb22e2932260859cfb022df1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01956dd7fe8e6a0fa7565f0faeb9c3a9e40c6dedb154aff74302501140fee8f`

```dockerfile
```

-	Layers:
	-	`sha256:739059f3f6be9798d36c6fb5e157680422f75fadd6056dda7b1d8c65264fe269`  
		Last Modified: Fri, 27 Sep 2024 15:27:51 GMT  
		Size: 4.2 MB (4223358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d13d210d4aedef2e5938d87c57ae119eea6ea34c896e00f27667ae499ba66f8d`  
		Last Modified: Fri, 27 Sep 2024 15:27:50 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a847974e93e911586570ee1d7e8f6254ae6933e4ff60a5a4eafc0a59e752e40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67680032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76250fa78ef11613685bfbfcd9362128fbf96968b7ef1346163d86c43dba7967`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
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
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef6e128fe253e9e92df878bdf6679d19c4c795a0ad5b4e2763d98dc38d52397`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 11.5 MB (11500106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ec30e15c8071ee1dd2c285d9e9180cbd765125f72712cde12b1e30609cd7d`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3df436804194d27d1205da4b1b5b92b11b5e9dd37789901d1bb7054b49941e`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec155c5566b8bfd54cb4ff20ed3df4ebe932bc0414cdb7a5a1686c9f2943d4c4`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 101.1 KB (101076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f013ea1ffa93929d5f3fc804f87adaa36164ab369bb17de0daf168773747c7e`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0b8a94eaa507d01e918eb51c1691cc17c03ac6f5f39042bdd87316f86c7f4526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f97f8b8941aa00985d47d71e1ca26088ec2cf233814c1fcca8257344690427`

```dockerfile
```

-	Layers:
	-	`sha256:c13ac2c7f8d63495afdaca68139efd3b9e9e5363a3043024ca9ad151326111ac`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 4.2 MB (4220213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44468e83d9ce5d88b4eb7b5dc138e35d4e8586e0dddd16c82cdd5f9c45b443fb`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json
