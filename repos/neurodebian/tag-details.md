<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:forky`](#neurodebianforky)
-	[`neurodebian:forky-non-free`](#neurodebianforky-non-free)
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
-	[`neurodebian:nd140`](#neurodebiannd140)
-	[`neurodebian:nd140-non-free`](#neurodebiannd140-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:nd25.04`](#neurodebiannd2504)
-	[`neurodebian:nd25.04-non-free`](#neurodebiannd2504-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:plucky`](#neurodebianplucky)
-	[`neurodebian:plucky-non-free`](#neurodebianplucky-non-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:f5ad6f9d35d36b0e4546739cc2cc2b0715dcaad10c252c1d731b93ba99e7ca61
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
$ docker pull neurodebian@sha256:c1242f1ae926b10fac848bae44a495dccd66a1f230b6b7fed29b1f6a0d61b415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ffe9ae6a0219a6a9bb417e0807677106ca2fdd75bfa7c85c32f6b7b19a61d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2076e118117aaae08d4043f950fcfaf533cbf38d422320c2d3e4e79fd1cb42e0`  
		Last Modified: Tue, 03 Feb 2026 02:48:56 GMT  
		Size: 11.3 MB (11273502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adaf593435563a325b4e351870a254d93ace4a6f6e07a0076246d00cb5465a4`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9b8967af24b7aecf27b7cce202956704c3b50f82c4085ecce2a9a7160bd959`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b33b63666fc4fd13332f7b20b6bdbe9ca7b0a7ffa3038bb9e9fff447c9777c9`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 93.4 KB (93407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0d1ebd5434d67fae166a6c83a948abf5b042772ba034630f0f2f66f59f73ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19eff2aa6afd5c085e13f1a2dd7f58dc001e6100f286fe390bd5ba170a02014`

```dockerfile
```

-	Layers:
	-	`sha256:c8bca7e18d0064b9ef958dc8aca15d79c44717eef437552691266c3fc08cb082`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cca950dd7c438bcf4a08ac81d7d99a6ee39835a490ee62f3eb322f3b651ec73`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f4d165b202ae7cf889cebfb2f8890f5a1b1e3ac7383ce00db73956bb2a57ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59714711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b050b86537ad67bb9a59f72c77683b3c499dee86aa68bec598ef623163fb7d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:34:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:34:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5bac5984f021a1cb1ca749e027c45de7e53293b1625c4988634a4daa8acc9c`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 11.3 MB (11252918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dc8f152c1cf266e173daf7a4a919546ee4a9897b2895bb2832bd1f63404ebc`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c75f7dce09f41ce9bb54cfdcf8fc08fcd6a07d50774a65eb285da7fcd95322`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3504a75e5c40c7856f2d2967e8709ddc3ace746bdc156afbbf077d0ccf63396d`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 93.5 KB (93548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50d1b24cd28126b28a8bc7059cc7aec5bbb328f9577aa0b3467612494ddfe8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b50357eebb778298a3ccd6d4d853257b9c8d1b9e1706a66cd4955ff44f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:a9db612e110a8920702e1d47ac0556074c76c777a5a4f34c6e716b2c48187888`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b441564c50d329324650274898a7074bd1b3099aab493b5dc71971a097f1d21`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:67812d5d9ba451d131e6983c080b6648e35510efaca0de5b1f1048058abad6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61257184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab86506df32c3e9caffe0560f3b197a28c2c7c8fbd0e56495b0ad5ffa07be1ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:08:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:08:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:41:57 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a556fc2754d9f044d1662e4d79eac9e4915ce45406c40cf4e34e0b2b98dd0626`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 11.7 MB (11693011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9cb7a9c880a28c145c0be772f574008d4916e91293035f33747c3ddb4f2d68`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167d0a94399112121b938a46fdcecfced399b318f44230eee634ec27d131632e`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331905edb01f14a56fae50e349444847e3bec8fb9dad97125063c168acdf007`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 93.4 KB (93404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e572b62f187127281c4838b3299293489b0a40b901a9a475fc139531f066fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a320d9dff56836018043dfef369561d75d7d2e35a73b7d9b938c8019818bad6`

```dockerfile
```

-	Layers:
	-	`sha256:712c971f0cd3f560638800376e5c3dfd18579579a9bf58f9575cc4581e212b34`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d499e215431beed2308372294ba048f2ef1a48797946500f2ced622d31e60cf9`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

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

### `neurodebian:bookworm-non-free` - linux; amd64

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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

### `neurodebian:bookworm-non-free` - linux; 386

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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:6fa71149b39566a9b40b3e31620da4b02316e38d01a7c2f408f94252367bdf46
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
$ docker pull neurodebian@sha256:c6fe056761bf624c48323aa68b1a0f5d713c4d0b61832e061ca1ea7ecda933c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21627ce4e7ec3d7e88f1abe7fa4bc41c147db83695ed04258bda3a7b6dc4445b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1d633e2bc91aea90973516b45752d540db2ea3cedbfabefc881c030ae1e19f`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 11.1 MB (11103524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c5bcd939835f01a3b851bb6cd334c3fdaceae44dc5ad0b2ff9983495d88ad0`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0cc5228ca7eca77a2a40283d1d9ae0330aa87b2d01ff8cf386e2e04e296e29`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b465d2202f2a38722e786a7c0e5bd9671a551c9ebbcc46d3929a4bce2970a3`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 101.4 KB (101429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9cdf47e555c97d954a83f3afa5500cf5b0c917f7db57b2737a13e136b200a8`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fff433a0c16911f96bb25b6fb337a61b0a4c392e54d963c253c382e94f961fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6144505b81e88e04ceec7346c279a36e30e6c8747e2c29b4a53bcccf0a4224`

```dockerfile
```

-	Layers:
	-	`sha256:83904257f196bddf92b45b7631562668036000f57c2d47b653b38066e4e63f45`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf75af788ef139571dc1aa51a678c8b24d5627b132e55c158d9d084f744edd4e`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f5f7312c945b60990fbeb6fa3ac154b799bf2d959560ac8209d2695e35608669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e996b679012531510d226df25700fee8ee8d09cb53e5037c113b5b6eef393ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:33:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:33:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e852e98585e0086932c28bd104c90762c999c879f6bff631b9dfd3e5e027ad8`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 11.1 MB (11106067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2012f775c3a0b7db8ad8b6a741fce6bf1a3bd9e7285301af6bb8c74aa205a210`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ebf6dae5f8f124e7deca8a99d38275f3c415952230053da6203eada6d23fb4`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198ebede9dec6dff5f729071cee117718742f091332b36e1a24dc261bb2f4460`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cbc978f4e18f291d148dd2e8b50e3720b87f256894ab7ca9ee5548ec476ec8`  
		Last Modified: Tue, 13 Jan 2026 02:34:06 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c162acbfd1be1a7b6057738ee3e0f7eeed018cbbfe6384cde8bd6a7aa2fd6ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26227bb96753fc94da015678725c714ca85ed6bcae28e4cb9e8efa8f62ca3f2d`

```dockerfile
```

-	Layers:
	-	`sha256:fa0ebbfca159885e51eeec2aa8d9a49786b1ca5cb94a7e95879a740e9c917d61`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3c2220f93de37bff4c79e226a29ae34c67448e82152cfb4700a608af0f01c27`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b4387c5264e12a316b565ed6d7b792e8b38229f38956eeb5c8b8f7deb44931e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d488196570b9678d5d15398ea3a5a56144e7e2fc7f6b24ff3e53a9760cc2b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:08:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:08:53 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:08:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:26 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84f7876b97c9cc558e3b682faffaa05ced369d3a1daf0097395a92379a1e56e`  
		Last Modified: Tue, 13 Jan 2026 02:09:04 GMT  
		Size: 11.5 MB (11500374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0706ef71ceb0b289ae294621e19630c33b44b79fd2a4700c9bfe91af88f5e09`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93d15594c1a09687f963a46a767fd98814ce5068a9a92bee4d01761a2547e5`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685f5a198b5049eb844e3225fc405d497e7a828788b0b2d3a99315e1c89872d`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 101.3 KB (101277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2935e4ff248fbeb6449435fe4391367a3ec04a837788d04f2a5c950f94815f39`  
		Last Modified: Tue, 13 Jan 2026 02:09:04 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ccdbc0018d01f9e14a406dc7bfa3d3e22843a63b2183a16fb9268e2b2f13f988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b44cf07798c40a6ce78dbafc09692d3ecfb06394249c498e5874b19421d30a4`

```dockerfile
```

-	Layers:
	-	`sha256:d08560fbc054319e24e443e931ae6376f40ec35a6650d0c9a827ecfcbefe1fe4`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de584fcc7e6273fc33f29b39b5ea37d0141365526c22b1438baebc0dfcc34719`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 16.0 KB (15963 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:2d03b1d3fbee2907a38c3b5446d553cae3791503718072be575fd80bf58e538b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:62557098c459de418b2e59e2e0374ded8453839c8dc8a8a635e934e25b272fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60289672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e09429446df5077bffdd30968e77332ee3dbad06f3b3bea0d5d4e95d262872`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2730c822ebcac3a15d3d766e879e3429b4f9adf6fe76271ccfc76c249537f502`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc7445e516a5d581aed9ea2f12b0eaeed7fb0988a1b7763124e12ff75af87a`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.6 KB (90648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6aed34d51bd5ea07823221ec742d4e2d9232789220b79efe8f13368675e3040f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3787c78d5c00b60dd7bf2b7563d0ab9a1f311b1efe8e20720192ef75f7123075`

```dockerfile
```

-	Layers:
	-	`sha256:5b86a2fd5679538630a28183b3b3ba91097d7d8705bb17616d47cf9348996af0`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d480378322cf7188821388658920d0bdc152a426690dd4aca8e70b9eb5cd12aa`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:20110e381f6b004aa11f066beb696aeca0000b8124cffac7191c4cf7022c6010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60198955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c078fc2e2f1689540c190a5373f9ca68722470fab192a2bd957f460ab642ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:36:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:36:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:36:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9b4ae41d7233f89c118d44c566dbbb0830c66fb38efc746d17d7d8173a4882`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 11.3 MB (11284159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6245f8367a76c48a8d8d1f80c4b50d14bc2990b1511aa41472f5da8ce96dcc06`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865c6f91c38ef38d5b6ce69fc2f8327da1da6f39b1c6117b3cdd7009653db137`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dd28e59e9c284ee6ea9cd526634ccd93547489875f216d845eadcacd04c1ac`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 91.1 KB (91081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:88cff5449f9b674dfddf81f0ae1030542280eae60026af309ba965c62c3fae35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3d45e5e795a9de5b54de388dda9d9e8a9dd64086e65bd23593c7c589264a1f`

```dockerfile
```

-	Layers:
	-	`sha256:e29b98130b6dc6e456541688ff5b568dc4f6ccd4d3030133e5a4ac315d808cae`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 3.6 MB (3593356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630d99390d48575bc5839357287f4463cd0de213f9cbb7150049c3656c5f1a7a`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:1be3593202c67933b0299654e15c40a1f5f79745d476a49e0c57d40fbef93e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61816076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6906c266a1c4fcbea80e2940b2bc77724f1b671ab54ba960695b5a85da2ddff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:12:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:12:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6cfe728e8ad2478120bdf56f46f6e29d6f196368ee72600cf4cf563f852d0c`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 11.8 MB (11777884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b758bbfaadc4750b38dd2d7a2eed37620b79d23adad813edbadf9b54190aadad`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f53ad6cf16dbd5f68bc9d9322dbb7cf4cdc0b91cd81817c248463451194c32f`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f6d2e23e75837861e27bcb5f7a138da1aafb97f4d81476f5435b4f15a01e0`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 90.7 KB (90744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:68d058ecda648f3359c973d9e0cb54d24bf63c92d5ebb84d7583b7d42502e083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1f93b265c195fd17e70d6c5296f6e03fded2d2628ada0e80b976c5b095c0eb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b335683b09ca022d562f726c22c173d84b01acbd67aed48073df04de9fd807`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 3.6 MB (3590438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1f2b647f16426bffab845d28d772f826717c5d3650bc9437f5b6cbb3f22628`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:288ab70606798fce0b498ad955d5dc54bb03ec0c0832d582d137cd79772d001c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a163bb449af86570efbb2c848f4a56b0a9f75e2c9bab460fac75b282e0ee9659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60290217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ebf1e005f416f00f58c9265e914c41d744ca6aa1cfbeee885ba91c67104b69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbb37aa9daedccd57c940309ed43a39d7248abc940a23204d466caa4499871f`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035ddd951380f76413ebc0059b6934df85dc73f566840fbe23db460cfcd656e9`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.7 KB (90675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef19c1eb6c1cbf32f075f42496b94816b18968b15c0f0b69876955199b6719`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14a013c4124a4a318ef9462fba9ce8e7d4f7ade0f5398b9583274cdf91689f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f2134a5a1a99b81c7e83acec3a0283963987a07471c68c3cdf183c9f72d260`

```dockerfile
```

-	Layers:
	-	`sha256:2164015860c8679b1861e5dd23a57a9c9cf4dfe0487d529174fcf93b3b40604d`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cff4e739dd29e441abfa38f38ab0d7eff091449c92875d8627eed5ac223629`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:311f95d8c09f720583c8bf71fe7f6a89b4dda12c1383d28957ad4189fae03e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60199406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee76e1175122295cf681eed5d09471821de89695b8dbdc0203f5375abc37a83e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:37:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:37:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:37:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:37:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:37:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840a5ae9b27a3ace79b3cf0fdb2bddc6e0106d136b74b66d524377fecce1c8ee`  
		Last Modified: Tue, 13 Jan 2026 02:37:21 GMT  
		Size: 11.3 MB (11284159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b04b69ed7b0dc312198ad357b2412c074128f959f7293aed12772b8024660ef`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ff9f4d2e3110d267b69e9306e4a2c646baa86f11542e5890a5a610a3d81b20`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624da5a767e899231c0f32b59b33cb218d6cd91826a2f6983521bf73ce77dca`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 91.1 KB (91090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b7c6b056e0df9d0635f7da4ff9b04e3ae4d6bba65d77282f987483a0af1b94`  
		Last Modified: Tue, 13 Jan 2026 02:37:21 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af4aa92e279c4915e30df6e7cd29dd117fdacc453c824e0a90fe24c7b6d57a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32574c6ac80df83065fa624f2b51be56590164d0a5cd3bb7ae01b53b0c76a077`

```dockerfile
```

-	Layers:
	-	`sha256:b7dd2f04643444f2e93834bcaf87bfba2f61ffde30c642adee29597f4ed07e2f`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 3.6 MB (3593392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958c23f7a6c9a93a6fc9cf4709b5056222a686e1d725659fcc9f3c9ad5383603`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4e99c3c6e5582d78c9e78cf02a431906f358c74b00f4f0194cceadef329c0811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61816562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b1b6bb9725c2c422ea1ff4e255221a0d3b6cc81e7d5b5bfd1509bab991daeb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:13:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:13:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:13:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:14:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf06d6cadb4b597f7d41ef40aa97534c966810a7be12ffa98ba0c62d0b6d87a`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 11.8 MB (11777905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b17d2a39e5656e48ba83c086e5b2cc1bcf80b3fa2bd447dedcd331732869dbb`  
		Last Modified: Tue, 13 Jan 2026 02:14:09 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c37104f12b85966a7ba54059613e4fb6cee349b2e91746262d8151289c2b0b`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667de473d81a94e4ead18b60fd01798a848e3638b2f0aca250844c57926eda`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 90.8 KB (90763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1be9d3fa61a9e252b493065fac5b67a71bd9f7acb6ee3d71de5a31fa1e7bb4`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a83992b948f52e474ce13a2d7219f483a042dba1531fa41ad79976890dbb9bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf46cf6dd92a6377c617e5a247502d0f0d0faa3552ddd363c849b3c85277b7b`

```dockerfile
```

-	Layers:
	-	`sha256:d99390adbd9fc049478e9f3b542594c7912a0d5b18a72b084290199625a8d438`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 3.6 MB (3590474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3fb5f51573288a20fa8174e7c6f3d3943d5d35eaeeba105e823e4cbfab7236f`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:19ec59ed4b51fae27dd278d0bf11380b21edf2718a14a056b71c205ea984a184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:e497487cf2720a736bacbaedac3ae2436433d09e6ad0bd8a65c86d41f4d063a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33274380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43de36e1bb01c325b9bcc5b3aa2750460e5d3413af9817fb57aff5043948e09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c31a1de4315e0b58b79ce211ded98e483a09dfdc7f9a6499a9a7ce21a39391`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 3.6 MB (3624300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ba782c854a068481cc1d19b2b885bc3941b0f687797867734b959977f68bcb`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b50cebc4c825ee52a417c7198f1be150abccfd99fab7124120dc49208d23b3`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ddc7f4be458215b98db1adbbcdd655a576940b797584f026f194d25aea142`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 111.2 KB (111235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:25d21931ef63fecca937fa9c226d4b9c972c6a07ab7b12d6cd472e98c2f391b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bf0f83a34f3cf53098c7ebd08efc3892d2749a28113b59f8b7fae1fc13e58c`

```dockerfile
```

-	Layers:
	-	`sha256:11dd9334d128520572ee5d6644d929c8e386a02ca3d2ec2ff0bcf28cf4bda108`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07dbb8c42e97f3cbb99e13a0cce5eaeb2908125d20a39eb7a012208555bb6be0`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:de8c6e985f8ebfc9f9818ad855d16fa99573bd46e0e9f4dd84d73e19618c9a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31098806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fd5b3ddc77a114383c7ee36112f4540c8891c057f8e7a8cc490ac45e5716fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:36:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:36:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a4ea43c440ed4c5c6940006aeb234cf69c04ad0392d10b84fd9766e4a34f8`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 3.6 MB (3602633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae0723c728afe1d94014082337ee6c2c149eac4aa6f8373a264ae6ef9d99e8f`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7101abc79e23d3f25054e865a814a95478cc4e41c4b4ccbee0cc361e535cc37d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c3cd39c7b72b92ef079ad69cd3630b8af83c92b6ffe3230be891653be676b`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 110.5 KB (110499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:886473be4217eaa0f6c8744ebd3176ca4d06f19d1a76302fb19c67bd0726beaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468d90fb319d993524a4713f622cc2c3e500cd78f13f40e5551c0563785618fd`

```dockerfile
```

-	Layers:
	-	`sha256:58f1ed8735b4542a9a1bea99b6f344ded0a424a110de890d71fa473bc53b359d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d01ecd9429deb21559e16c32c9f4e387c8f8033115397f07ceae09f9725024d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:f8a04f8a8dc04df731f84789fcb71e800edabbf6bb1aebd975bbca1fa8f1c3a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2cd764c7884ab25b110fddde83cf33834467579766c56cb1ab549e9a3ea90470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33274712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc3af720234bde69d207e0f9fdc641e991f2697f3fee5ae0aec4cf34d6223c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b59d1ef943d834ee1a50db8acc83df82aaf8bb732bc303a4d9ac314ca79ada8`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 3.6 MB (3624349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903068be00a686117d5126046cccd885353091e8878694caf04fcdb458f28010`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7436405aa87ebd15250cc5d262e3a512295411df4ec41ab2b7a149be703da`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09c2a0a07d862cba86e9245a3f5fc8b54ab7bc332077758a597ebd129314c71`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 111.2 KB (111237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb3eba37faf714db0851cc8861baaa63273442a84287700b6607cbf7e50d4d2`  
		Last Modified: Thu, 15 Jan 2026 22:34:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93e9d3bcff981b6bdaebb3818c9abfdf384cfce638b89d07c9d9da38979e63c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d61845c72e5e377c08f2a586fe8d061339c3f115497261045d09f1c31a2058e`

```dockerfile
```

-	Layers:
	-	`sha256:5fb780292168a3a5dbe5f8ce395b7bf5beb0798a6ebe2dc57020d67f10741c2e`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd6a705adf1df71c78ac76d86175ef0b0fa0cde1b1b6ec1f5a5a5337153629e`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:741ddf278e88035b94dc004a4c6a12f141ac542d2e852ecc9b064c70994cbadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31099022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af2062e8549cae074e26beb662b0eb5efc3f3383962c6318a236bb569173e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39623f164b7c134bd7c870258397b9ae29b76f658821cd89c872006781773a07`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 3.6 MB (3602582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc84ee017cfa97d082301a68c097692ea26fbf238220f31788ab3777fb0915`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62e658825b155b9da439360822a1b71de7886aa64a9f6b2ed952f31379c285f`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf949af04af6e2380e6e33215d31850a1aaf11a41caf3df6b222373f2d115b`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 110.5 KB (110485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ade6120433a2a5a27b1949103586f6bea98efdfbdcde54a84ec40fc4703e39`  
		Last Modified: Thu, 15 Jan 2026 22:37:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2f764bf523306b0471b6acd75e196f3491fa44291dc40435483f27e5d5637037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b21632db7bd9623230cd92a59777549d877ad4ed24e036f4a1ca309c4a29973`

```dockerfile
```

-	Layers:
	-	`sha256:09017ddbca29fb71dcab82dce0807d3653f2cca9f0d865f7a27c96666e61c0b9`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd1544fac022fe23da5e4aa065119ee55176834cec20f0c37704625726caef3`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:ffef758c80ceabbba337660d9965eb402f9211965a7659511c9648332d2c09a1
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
$ docker pull neurodebian@sha256:da3b9227f84c0e82c2a1cd4cb5e96ec28789730085a1ac4652b6bb91620d43a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59678819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8b026c74f7c723c4dd8ef3d34903dbf19b1ec0bcfb0356313abfeee3f0d4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae41ec031155c98b455bb78067eba48a17546176cae679a09109c6f40044b853`  
		Last Modified: Tue, 03 Feb 2026 02:49:08 GMT  
		Size: 10.3 MB (10292604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c456de52ce89d78c3e11be3ed11cac3ff2a3bbf1b5b7acbcc34864caa6ed1b`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c3f547274c1b9aba5a4c1dca0de6439e3641e2927b7ff0e29ba10f2598771`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e44b0ddaace5231fb0277c41a8f1dd1b9a803222537517cf5fc0faf0163b35`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 90.4 KB (90356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af8d1c9f950620612b890e7e6a4d8c5e0b2b9f2e5fdfb0bced7707c0f81c1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a741a8c1833792cc9553aecb085450cdb9f1664685ce094c1941eda5289f656`

```dockerfile
```

-	Layers:
	-	`sha256:e40985eb60787ad8aa5df064ec78906a87d592650d3cb7bd4e4d35fef41aeff0`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c276c637f8dbb8e68f06bb64f124d7e82ae5dde2c17bdf3085ab2d27b05e7a9`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:07e1a111cf7db99a4e8da7b30d05dbe05ce582c3e60c621b8dddf3f1d7fb85e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6958c992473c935b57387a0074e6ff9d5c8d8f25f4000cddbad2a4da7337e949`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:35:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:35:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:35:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7684c225310a7186686d90420bff2204e00d1da54ed64629dd5c3e06bedb11`  
		Last Modified: Tue, 13 Jan 2026 02:35:51 GMT  
		Size: 10.1 MB (10073782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6a425fa7aac586d22520ac0e48d6b900e2d7650c99f069fc369de3faad44f9`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b744125fe7f349b2dca35775678901252ef655baabbabf00e0581e5db35f4d0`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ec7811cc5fffb4d35b28f25ffe926c9d946a0287fc98559205e5ee8aad5d7`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 91.0 KB (91029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4f8ea8e151623c0726e2b1d500eadf97f81d9185d53345068d8a5310be376250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d3f945473a1378792d3153caab159049530a28c11f85defc0c8257070900d`

```dockerfile
```

-	Layers:
	-	`sha256:9036dfeefff31d7ac9375bcbcaa30955c898c61f27f40e393540a89d7cae685f`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 3.6 MB (3615595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69148b190dc58c8fbc910cf582b627d0d34da0969ae22d538922ec69e3487bd`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:1c485a7ec0ef76060f194fc63ade360521156d06352d21ba7e55c5678263b4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61359266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3405de0f825036ef97723d3ffeaf81ee462ad3c0bdef73f83566138b62c01017`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:11:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:11:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f9978ca299f165c197622edd759b69b3cf32899ccbb3854492744e5131a0d`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 10.5 MB (10466724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdffb0278580783eda7f81d2d70ad20bf0b440ee7b7590e521dc0aa44d3eff2`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d29a632dda1a11016736a63fec3296211533322f93651cd5c2f440ed3ea8f04`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f369e3c2508700e6055a1900113ae937b42ec7d8683d5ef29fc8b48f14b44a`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 90.8 KB (90766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1147e07d7974976c8157d340cbacd2696887d306fdb7a9521442243eee0bd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93d8778ceb78ab3c09d834438ad8647adc746cb80d84fc2b182f923c0d074b0`

```dockerfile
```

-	Layers:
	-	`sha256:a32e0b1b72a70a565da4eddb3e9eee98754724c4b9777ad9defe87db52ffbf4e`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 3.6 MB (3612016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd6ffeb7dffa3512f65e180c61eb1ffa3c36f0545d4818f3ec30607974a2b26`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:86a955a6da2fd6e49310005ddd799d6d0c1b03e61ec3a26bf798c7e17fb2dd88
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
$ docker pull neurodebian@sha256:742f81326d6458fc4835788d8fe3317f77b687290629fc738389f12c4814df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d9d256c1ca3e4c144c863cc2281316c3cc3eb45088369a88aea3a40a0914ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911d1558a1b3010131d47ee741db0963c889273e31e2a95035fd6cfb9f17c1`  
		Last Modified: Tue, 03 Feb 2026 02:49:21 GMT  
		Size: 11.5 MB (11540410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6309d0a7b6729391c7f1314a74b6b06b07c4646ed52a3d9e7ce4cb11daa5bc`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0740384dd13f89422fe1f4638c08fb758dc33e4f5c9810aa0b1d0a69d7fae0bb`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 90.5 KB (90457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e1ba3408ddc3dfef56dc25b1915ff61fc917b613ede0a431592467c4b4864a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba3eb40824aca52a92259785bc8cb173186a6bb1ccb406742f34f2f6ebfec74`

```dockerfile
```

-	Layers:
	-	`sha256:7d69e622a5bfed66bf691b20cdf1aa82f53f6f580b821ab40aec94be47d4d4b1`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 3.6 MB (3607661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7e7edca04a0e1aa36eebfdd3e3f3946a1ce7603207a77681ec83592f931e12`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fa0ba41b4e84d980cdefd58691824eb67a3c89e5ce751baafa6676d27374880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60202507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98d5b725f75bacf9154914537830dad7da7c50305e6a09d608433860d4f0361`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:38:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:38:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:38:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:38:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da01bcf829ac0481e16c259eb82b33f353df66d362cf4da5276683b0b2b9319`  
		Last Modified: Tue, 13 Jan 2026 02:38:20 GMT  
		Size: 11.3 MB (11283991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b508d27ae81a583413ba342757fe3a8e81b34b43dcaf3cada42f01296b880433`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb85291bd22f4f2d342b547834f90db0ef1315dc5b3db25f80d522429c600b6`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0758f88b1ad03441d33efc0759464c7090116fd1b6225e6bb3549fba6af4c928`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 90.9 KB (90900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fd4287db1c80d84718a24bbf7b419272c01514b21c14f2017321173cfbaf6ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6178646fb591280a4322dda9041233d675f14ba891bcf3c3cdb42b6669a33488`

```dockerfile
```

-	Layers:
	-	`sha256:0827d76799ed2ee2ffd22bb96db6c785e7ab0c7910d70e72af72764c15894510`  
		Last Modified: Tue, 13 Jan 2026 02:38:20 GMT  
		Size: 3.6 MB (3594069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079930c725e760d95d23f7f8d75cf0c97b6bb6f92cd6ee6185135a9359b10eb9`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:75cfaf1c6b7dc32eea6e9ad0986a93ef5eeaa1ad62b6eb7b9b92c50a27cf5a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61815161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619842c0a344cd4cc323e6bce0195b699ffcec1e1e11d144aa7ba65e03ae8e4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:14:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:14:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:14:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37772ef8b09ff9ece288ef28843ba2b28651580cfaaa82c9376253b633ebec17`  
		Last Modified: Tue, 13 Jan 2026 02:14:57 GMT  
		Size: 11.8 MB (11777889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b62c15fbf7ad5a88504652ccc590c41168dd750ad796ee00cb146201e51d41a`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572d1ccf01b56f7a38834164db204119048dc7f9118850e151ee844646faa2d7`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc6d97bb71fa9592ffbe96f2e81728683ccd72aff6a26e2a3dd0b3342b417a`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 90.6 KB (90557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:86bbfdaf6aa29318b32ef02597c6614d32d58e53aba363eaa8a6c80a860a36fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109185c65d9918c90b219c20784cc9ff1d784bd8e3c7eb098dd0571837b25969`

```dockerfile
```

-	Layers:
	-	`sha256:b48b602aa44be33ca0546314de063837fef65f8f602a6f9a01c8ec2a16fe31a9`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 3.6 MB (3591151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8768990e2a7177e584c19848ea859a7128c68a9856c85d9b11594e75f37bada0`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:3f7505cd2a98c7b65a1686ec9196357a8c77b8f9e87d476ac19a198abfe87cbd
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
$ docker pull neurodebian@sha256:a34bd5c63c5d4d902f50950efd6ce5dca64b1addf6060d5cb0d1249f0cbee543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308f8f8e8e8be830f406d62dc791fd094ace9d9714082e5a38b94de80c022113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7002f3da964c57bd455c7ea9aea032a614f96ad162a44a4e3be7f438517c9a`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 11.5 MB (11540369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfae06b9f53d369e6035db2bb25acc88db5141f15668b9c187df731a53d6330`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0675e38a13a9ae911bed6a859416965f3afb652c0c0bde63d3aa4b7c256fd8`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 90.4 KB (90432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a622e4dd49c0b33475fbc290bee154d0d2fa0f6b39499fc01581d935969bf0`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e40dd2e539b3db456883132b1b1edd605a481e44ded2b819881cb3566719049d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a040ca843f8191579ffafa4b24724273fd39a8d8db116dbf48cb294a674d25ac`

```dockerfile
```

-	Layers:
	-	`sha256:80d0cd2e330fc9bf7aa1ae15a2864ea8ed86232bb2bdabd6bdfc79ab09150396`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 3.6 MB (3607697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44da38342d0de406e284f67ea9541752f7cdaec248b21cc9996fbba57ab3770`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0c396589891d3c617ca0410ea2ff3ef8c48ab233cd8826d253a933bd2501b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60202796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427aa2ced9486bd12be502f9419345de174c5654292a3ce2ff4d35ea097d7a95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:38:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:38:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:38:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:38:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:38:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a5edd52237009e0cac583b17514f638b5d8f08eedc3930a2e812e893bd6c7`  
		Last Modified: Tue, 13 Jan 2026 02:38:53 GMT  
		Size: 11.3 MB (11283894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc58c09ec95440415b943959da0113ae578e6d378ab910c68074397ee96024d`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3e2db745e5179dd8918931028318ac50146b5c7f4ed70102c02afdf323fabe`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d8c2ee79391cf1b2076de818d699484239f70dab0332479d0eb6876eb76d24`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 90.9 KB (90868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7407bf616dbd5929f5d38b6b8161c64ea318bef988d826e2db12e1c7bdfa6b3b`  
		Last Modified: Tue, 13 Jan 2026 02:38:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c40f5ce3cfbbb278253579b56d9308fe52a4d1238982cb42d68d999e8e92b88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3610176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d60536309a11b855e32b84990e0453efdfe7827f3a33e9562615a2ea3d04f5`

```dockerfile
```

-	Layers:
	-	`sha256:9690eb218fc781102f03827a207ea0cff9fff756f8122a35552468f93250a736`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 3.6 MB (3594105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fdaae74eb9cff639961a564fad50873ac2bf56d2c0ea39128352527d6b9e666`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:29c6f2d2701bc0d15ab7aecb27bd6a46db79c8e5a7816d1289882bfa328a0cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61815677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c093d6a9a0e2ddba9eb0857a20960b123f24417c1896d87284b76f837efa073`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:15:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:15:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:15:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca115bc00d353cad320bbfd72a4e71bd2d894f06113dcb9a17030fb18e14aa4`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 11.8 MB (11777974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109172636f5d8d15495a86c47640b8833da31afa49dac51dc788d331d51b4194`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabaf41752bbfa6fc79aa7258daafcea5cd5ad20b4ad9da0d86b1e88d1a8bedb`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d143b59110518f6bd31d6dd22cb9813ce4fcc6f91f1241d926ef3b57c95d4`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 90.6 KB (90564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d2cf67c8b76bf197f0430f4758d401b3dce448aa47698c1733eaf18167b00e`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:304666b92baad6e4035e011a329a7d8bbd4352a94a1bbb7dddd27d4dceb391f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c456b6dd20574b34e286d508e125f0c53668b0932f7c6882109698912166b43`

```dockerfile
```

-	Layers:
	-	`sha256:0a44ae40c2d9af50ce8fb40c7a0100941164bfd8490f4e7115b2766a546e667a`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 3.6 MB (3591187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c08d2228b8f636f2a594f5106ad6f754469e440be86a8eb81b47366aad1557`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

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

### `neurodebian:nd110` - linux; amd64

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

### `neurodebian:nd110` - unknown; unknown

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

### `neurodebian:nd110` - linux; arm64 variant v8

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

### `neurodebian:nd110` - unknown; unknown

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

### `neurodebian:nd110` - linux; 386

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

### `neurodebian:nd110` - unknown; unknown

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

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:6fa71149b39566a9b40b3e31620da4b02316e38d01a7c2f408f94252367bdf46
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
$ docker pull neurodebian@sha256:c6fe056761bf624c48323aa68b1a0f5d713c4d0b61832e061ca1ea7ecda933c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21627ce4e7ec3d7e88f1abe7fa4bc41c147db83695ed04258bda3a7b6dc4445b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1d633e2bc91aea90973516b45752d540db2ea3cedbfabefc881c030ae1e19f`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 11.1 MB (11103524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c5bcd939835f01a3b851bb6cd334c3fdaceae44dc5ad0b2ff9983495d88ad0`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0cc5228ca7eca77a2a40283d1d9ae0330aa87b2d01ff8cf386e2e04e296e29`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b465d2202f2a38722e786a7c0e5bd9671a551c9ebbcc46d3929a4bce2970a3`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 101.4 KB (101429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9cdf47e555c97d954a83f3afa5500cf5b0c917f7db57b2737a13e136b200a8`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fff433a0c16911f96bb25b6fb337a61b0a4c392e54d963c253c382e94f961fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6144505b81e88e04ceec7346c279a36e30e6c8747e2c29b4a53bcccf0a4224`

```dockerfile
```

-	Layers:
	-	`sha256:83904257f196bddf92b45b7631562668036000f57c2d47b653b38066e4e63f45`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf75af788ef139571dc1aa51a678c8b24d5627b132e55c158d9d084f744edd4e`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f5f7312c945b60990fbeb6fa3ac154b799bf2d959560ac8209d2695e35608669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e996b679012531510d226df25700fee8ee8d09cb53e5037c113b5b6eef393ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:33:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:33:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e852e98585e0086932c28bd104c90762c999c879f6bff631b9dfd3e5e027ad8`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 11.1 MB (11106067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2012f775c3a0b7db8ad8b6a741fce6bf1a3bd9e7285301af6bb8c74aa205a210`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ebf6dae5f8f124e7deca8a99d38275f3c415952230053da6203eada6d23fb4`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198ebede9dec6dff5f729071cee117718742f091332b36e1a24dc261bb2f4460`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cbc978f4e18f291d148dd2e8b50e3720b87f256894ab7ca9ee5548ec476ec8`  
		Last Modified: Tue, 13 Jan 2026 02:34:06 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c162acbfd1be1a7b6057738ee3e0f7eeed018cbbfe6384cde8bd6a7aa2fd6ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26227bb96753fc94da015678725c714ca85ed6bcae28e4cb9e8efa8f62ca3f2d`

```dockerfile
```

-	Layers:
	-	`sha256:fa0ebbfca159885e51eeec2aa8d9a49786b1ca5cb94a7e95879a740e9c917d61`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3c2220f93de37bff4c79e226a29ae34c67448e82152cfb4700a608af0f01c27`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b4387c5264e12a316b565ed6d7b792e8b38229f38956eeb5c8b8f7deb44931e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d488196570b9678d5d15398ea3a5a56144e7e2fc7f6b24ff3e53a9760cc2b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:08:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:08:53 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:08:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:26 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84f7876b97c9cc558e3b682faffaa05ced369d3a1daf0097395a92379a1e56e`  
		Last Modified: Tue, 13 Jan 2026 02:09:04 GMT  
		Size: 11.5 MB (11500374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0706ef71ceb0b289ae294621e19630c33b44b79fd2a4700c9bfe91af88f5e09`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93d15594c1a09687f963a46a767fd98814ce5068a9a92bee4d01761a2547e5`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685f5a198b5049eb844e3225fc405d497e7a828788b0b2d3a99315e1c89872d`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 101.3 KB (101277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2935e4ff248fbeb6449435fe4391367a3ec04a837788d04f2a5c950f94815f39`  
		Last Modified: Tue, 13 Jan 2026 02:09:04 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ccdbc0018d01f9e14a406dc7bfa3d3e22843a63b2183a16fb9268e2b2f13f988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b44cf07798c40a6ce78dbafc09692d3ecfb06394249c498e5874b19421d30a4`

```dockerfile
```

-	Layers:
	-	`sha256:d08560fbc054319e24e443e931ae6376f40ec35a6650d0c9a827ecfcbefe1fe4`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de584fcc7e6273fc33f29b39b5ea37d0141365526c22b1438baebc0dfcc34719`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 16.0 KB (15963 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:f5ad6f9d35d36b0e4546739cc2cc2b0715dcaad10c252c1d731b93ba99e7ca61
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
$ docker pull neurodebian@sha256:c1242f1ae926b10fac848bae44a495dccd66a1f230b6b7fed29b1f6a0d61b415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90ffe9ae6a0219a6a9bb417e0807677106ca2fdd75bfa7c85c32f6b7b19a61d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:48:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2076e118117aaae08d4043f950fcfaf533cbf38d422320c2d3e4e79fd1cb42e0`  
		Last Modified: Tue, 03 Feb 2026 02:48:56 GMT  
		Size: 11.3 MB (11273502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adaf593435563a325b4e351870a254d93ace4a6f6e07a0076246d00cb5465a4`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9b8967af24b7aecf27b7cce202956704c3b50f82c4085ecce2a9a7160bd959`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b33b63666fc4fd13332f7b20b6bdbe9ca7b0a7ffa3038bb9e9fff447c9777c9`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 93.4 KB (93407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a0d1ebd5434d67fae166a6c83a948abf5b042772ba034630f0f2f66f59f73ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19eff2aa6afd5c085e13f1a2dd7f58dc001e6100f286fe390bd5ba170a02014`

```dockerfile
```

-	Layers:
	-	`sha256:c8bca7e18d0064b9ef958dc8aca15d79c44717eef437552691266c3fc08cb082`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cca950dd7c438bcf4a08ac81d7d99a6ee39835a490ee62f3eb322f3b651ec73`  
		Last Modified: Tue, 03 Feb 2026 02:48:55 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f4d165b202ae7cf889cebfb2f8890f5a1b1e3ac7383ce00db73956bb2a57ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59714711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b050b86537ad67bb9a59f72c77683b3c499dee86aa68bec598ef623163fb7d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:34:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:34:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5bac5984f021a1cb1ca749e027c45de7e53293b1625c4988634a4daa8acc9c`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 11.3 MB (11252918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dc8f152c1cf266e173daf7a4a919546ee4a9897b2895bb2832bd1f63404ebc`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c75f7dce09f41ce9bb54cfdcf8fc08fcd6a07d50774a65eb285da7fcd95322`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3504a75e5c40c7856f2d2967e8709ddc3ace746bdc156afbbf077d0ccf63396d`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 93.5 KB (93548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50d1b24cd28126b28a8bc7059cc7aec5bbb328f9577aa0b3467612494ddfe8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b50357eebb778298a3ccd6d4d853257b9c8d1b9e1706a66cd4955ff44f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:a9db612e110a8920702e1d47ac0556074c76c777a5a4f34c6e716b2c48187888`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b441564c50d329324650274898a7074bd1b3099aab493b5dc71971a097f1d21`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:67812d5d9ba451d131e6983c080b6648e35510efaca0de5b1f1048058abad6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61257184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab86506df32c3e9caffe0560f3b197a28c2c7c8fbd0e56495b0ad5ffa07be1ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:08:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:08:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:41:57 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a556fc2754d9f044d1662e4d79eac9e4915ce45406c40cf4e34e0b2b98dd0626`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 11.7 MB (11693011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9cb7a9c880a28c145c0be772f574008d4916e91293035f33747c3ddb4f2d68`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167d0a94399112121b938a46fdcecfced399b318f44230eee634ec27d131632e`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331905edb01f14a56fae50e349444847e3bec8fb9dad97125063c168acdf007`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 93.4 KB (93404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e572b62f187127281c4838b3299293489b0a40b901a9a475fc139531f066fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a320d9dff56836018043dfef369561d75d7d2e35a73b7d9b938c8019818bad6`

```dockerfile
```

-	Layers:
	-	`sha256:712c971f0cd3f560638800376e5c3dfd18579579a9bf58f9575cc4581e212b34`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d499e215431beed2308372294ba048f2ef1a48797946500f2ced622d31e60cf9`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

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

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:ffef758c80ceabbba337660d9965eb402f9211965a7659511c9648332d2c09a1
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
$ docker pull neurodebian@sha256:da3b9227f84c0e82c2a1cd4cb5e96ec28789730085a1ac4652b6bb91620d43a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59678819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8b026c74f7c723c4dd8ef3d34903dbf19b1ec0bcfb0356313abfeee3f0d4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae41ec031155c98b455bb78067eba48a17546176cae679a09109c6f40044b853`  
		Last Modified: Tue, 03 Feb 2026 02:49:08 GMT  
		Size: 10.3 MB (10292604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c456de52ce89d78c3e11be3ed11cac3ff2a3bbf1b5b7acbcc34864caa6ed1b`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c3f547274c1b9aba5a4c1dca0de6439e3641e2927b7ff0e29ba10f2598771`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e44b0ddaace5231fb0277c41a8f1dd1b9a803222537517cf5fc0faf0163b35`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 90.4 KB (90356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af8d1c9f950620612b890e7e6a4d8c5e0b2b9f2e5fdfb0bced7707c0f81c1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a741a8c1833792cc9553aecb085450cdb9f1664685ce094c1941eda5289f656`

```dockerfile
```

-	Layers:
	-	`sha256:e40985eb60787ad8aa5df064ec78906a87d592650d3cb7bd4e4d35fef41aeff0`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c276c637f8dbb8e68f06bb64f124d7e82ae5dde2c17bdf3085ab2d27b05e7a9`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:07e1a111cf7db99a4e8da7b30d05dbe05ce582c3e60c621b8dddf3f1d7fb85e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6958c992473c935b57387a0074e6ff9d5c8d8f25f4000cddbad2a4da7337e949`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:35:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:35:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:35:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7684c225310a7186686d90420bff2204e00d1da54ed64629dd5c3e06bedb11`  
		Last Modified: Tue, 13 Jan 2026 02:35:51 GMT  
		Size: 10.1 MB (10073782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6a425fa7aac586d22520ac0e48d6b900e2d7650c99f069fc369de3faad44f9`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b744125fe7f349b2dca35775678901252ef655baabbabf00e0581e5db35f4d0`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ec7811cc5fffb4d35b28f25ffe926c9d946a0287fc98559205e5ee8aad5d7`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 91.0 KB (91029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4f8ea8e151623c0726e2b1d500eadf97f81d9185d53345068d8a5310be376250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d3f945473a1378792d3153caab159049530a28c11f85defc0c8257070900d`

```dockerfile
```

-	Layers:
	-	`sha256:9036dfeefff31d7ac9375bcbcaa30955c898c61f27f40e393540a89d7cae685f`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 3.6 MB (3615595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69148b190dc58c8fbc910cf582b627d0d34da0969ae22d538922ec69e3487bd`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:1c485a7ec0ef76060f194fc63ade360521156d06352d21ba7e55c5678263b4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61359266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3405de0f825036ef97723d3ffeaf81ee462ad3c0bdef73f83566138b62c01017`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:11:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:11:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f9978ca299f165c197622edd759b69b3cf32899ccbb3854492744e5131a0d`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 10.5 MB (10466724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdffb0278580783eda7f81d2d70ad20bf0b440ee7b7590e521dc0aa44d3eff2`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d29a632dda1a11016736a63fec3296211533322f93651cd5c2f440ed3ea8f04`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f369e3c2508700e6055a1900113ae937b42ec7d8683d5ef29fc8b48f14b44a`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 90.8 KB (90766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1147e07d7974976c8157d340cbacd2696887d306fdb7a9521442243eee0bd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93d8778ceb78ab3c09d834438ad8647adc746cb80d84fc2b182f923c0d074b0`

```dockerfile
```

-	Layers:
	-	`sha256:a32e0b1b72a70a565da4eddb3e9eee98754724c4b9777ad9defe87db52ffbf4e`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 3.6 MB (3612016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd6ffeb7dffa3512f65e180c61eb1ffa3c36f0545d4818f3ec30607974a2b26`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:4bf6259209bc214c61d034c1dc11a5f99f24c56694fc40cebf1fa4e991e82640
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
$ docker pull neurodebian@sha256:bfe6f18aa6a74c90c1bef54a8ecbfd1554d462da56f4431077902cee7e35743f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59679073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734174826d480fd0ca4221a27524fe98e871a54a19c068307ec6b8d151189d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f763d27f0cca3eca63d032df25da1781edc10ad21bb6ec6472a87765b5d494`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 10.3 MB (10292413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2193d3bb29390a43b5fe3cf6ef36f5d049269591f33a3f65f1c3ebf33ea628`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f82edf0cab6319880f6003cb047a9679b2b534d136feeba495550f279df6cb9`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae03b3a868a98138feda4a04a1f015e865a3599f8231275cde4e2d3ab18157`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 90.4 KB (90354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f2df40ce739fcaf54c09cdf8f844f97b7b89ddd3a009cf66056798e7a816d`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fbf95673c18f9bfa0a30481eb45b538fec3995c608702a1c1d90e08da42446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9f83b2f6643450c6e9f512971c820c8345c704dcd2e8cc7a8756a02e736f86`

```dockerfile
```

-	Layers:
	-	`sha256:6c76910ec532300ba0ac33261e0fa300df86a2a7236c44063bcf717e3999b372`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48dd7f90c47288d683499a84f5abe7001a411496c218e1bd8e77b25b0888176`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3e8b1aee676dde93acde9fac58fa3ab60f76be22359149b15a158f66571828b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59816200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16820c26affbce98ddae6fa99af774b35f36fa48f83f0175f7cc280513d9df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:36:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:36:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:36:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ed602a8d82e45752b42458f6c6cf735a34652ba4dde594e695631d834d59b`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 10.1 MB (10073712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8fc00822d28ca96ab3b0a281c9f30f594ddc2a1097c1d118b5a8d327ade838`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8209c0e736639a6f4be8dbb64c8eebcf8f0660d2bfc6801b3c25864d8deee2`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850c1d0537909467bd63adc7a9f8b6c380009301140d89edfcf9e56b6a682db`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 91.1 KB (91057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f820caede12aa6a0a73d704ba9b536c2a46a1c60230cf73b319c81ab1626f30`  
		Last Modified: Tue, 13 Jan 2026 02:36:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9e27486911deee56ba88782a368ea64fb2d4cfebf43f5046a845fd248bd042d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ee1f59febf6225a8b47ae664b8af048babe29a052e8afed5aacf201038bfa7`

```dockerfile
```

-	Layers:
	-	`sha256:f6eed23b2bfe38aa7cbef27424d9b0bedeef111763c3f9036af89d8ad36602c2`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 3.6 MB (3615635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df7281df837c359d65967773d79bc4901995aad5084db01a47562adb7c7d61c`  
		Last Modified: Tue, 13 Jan 2026 02:36:36 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:0e960ee0faa42f6bdd57961fff7557121bcaf8613b82e9b199d40d7a0261d96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61359689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571fe39bf716fc3e4014c560ab9d7be66fbb4dc330c7f227e15b9de763fbdf3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:12:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:12:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6161421471c9fb8d6e355616caf09b7087ac27ca53984bcd4134a0b0d7e111`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 10.5 MB (10466725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ebcc0e9e4361a538531fdba9070f9175a771b5bb299631b4e6ba78b8981ae3`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895adfd9029fe52f402919d58a03065389e5be8bff8acbf6465d5a18b525fef2`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7e6cefa33611a70c52fbfc73b63e42b2cdfc1fba6226f458dc3f5c739c142`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 90.7 KB (90740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3130aa08749bed8751f83a3a79d2ab7115ab45e908a1b0fffbdd9f80014cee1`  
		Last Modified: Tue, 13 Jan 2026 02:12:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e78e25dbca6377a9c55bca652f94e0e9be3780e215df940fb294f1d5d86968c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f5b3a6f545f0eba153876fc40fb4cce27fea22fc5fc61617969ef489152f6c`

```dockerfile
```

-	Layers:
	-	`sha256:847768114c721eaa57ed7d191df816ead0fde24426576323ca0caead4f71653a`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34278bc983bca66a2b8695d2725d6c0031354a486b9d39d322df70ee7d8ffc6`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:2d03b1d3fbee2907a38c3b5446d553cae3791503718072be575fd80bf58e538b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140` - linux; amd64

```console
$ docker pull neurodebian@sha256:62557098c459de418b2e59e2e0374ded8453839c8dc8a8a635e934e25b272fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60289672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e09429446df5077bffdd30968e77332ee3dbad06f3b3bea0d5d4e95d262872`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2730c822ebcac3a15d3d766e879e3429b4f9adf6fe76271ccfc76c249537f502`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc7445e516a5d581aed9ea2f12b0eaeed7fb0988a1b7763124e12ff75af87a`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.6 KB (90648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6aed34d51bd5ea07823221ec742d4e2d9232789220b79efe8f13368675e3040f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3787c78d5c00b60dd7bf2b7563d0ab9a1f311b1efe8e20720192ef75f7123075`

```dockerfile
```

-	Layers:
	-	`sha256:5b86a2fd5679538630a28183b3b3ba91097d7d8705bb17616d47cf9348996af0`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d480378322cf7188821388658920d0bdc152a426690dd4aca8e70b9eb5cd12aa`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:20110e381f6b004aa11f066beb696aeca0000b8124cffac7191c4cf7022c6010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60198955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c078fc2e2f1689540c190a5373f9ca68722470fab192a2bd957f460ab642ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:36:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:36:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:36:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9b4ae41d7233f89c118d44c566dbbb0830c66fb38efc746d17d7d8173a4882`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 11.3 MB (11284159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6245f8367a76c48a8d8d1f80c4b50d14bc2990b1511aa41472f5da8ce96dcc06`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865c6f91c38ef38d5b6ce69fc2f8327da1da6f39b1c6117b3cdd7009653db137`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dd28e59e9c284ee6ea9cd526634ccd93547489875f216d845eadcacd04c1ac`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 91.1 KB (91081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:88cff5449f9b674dfddf81f0ae1030542280eae60026af309ba965c62c3fae35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3d45e5e795a9de5b54de388dda9d9e8a9dd64086e65bd23593c7c589264a1f`

```dockerfile
```

-	Layers:
	-	`sha256:e29b98130b6dc6e456541688ff5b568dc4f6ccd4d3030133e5a4ac315d808cae`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 3.6 MB (3593356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630d99390d48575bc5839357287f4463cd0de213f9cbb7150049c3656c5f1a7a`  
		Last Modified: Tue, 13 Jan 2026 02:36:56 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:1be3593202c67933b0299654e15c40a1f5f79745d476a49e0c57d40fbef93e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61816076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6906c266a1c4fcbea80e2940b2bc77724f1b671ab54ba960695b5a85da2ddff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:12:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:12:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:12:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6cfe728e8ad2478120bdf56f46f6e29d6f196368ee72600cf4cf563f852d0c`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 11.8 MB (11777884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b758bbfaadc4750b38dd2d7a2eed37620b79d23adad813edbadf9b54190aadad`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f53ad6cf16dbd5f68bc9d9322dbb7cf4cdc0b91cd81817c248463451194c32f`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f6d2e23e75837861e27bcb5f7a138da1aafb97f4d81476f5435b4f15a01e0`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 90.7 KB (90744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:68d058ecda648f3359c973d9e0cb54d24bf63c92d5ebb84d7583b7d42502e083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1f93b265c195fd17e70d6c5296f6e03fded2d2628ada0e80b976c5b095c0eb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b335683b09ca022d562f726c22c173d84b01acbd67aed48073df04de9fd807`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 3.6 MB (3590438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1f2b647f16426bffab845d28d772f826717c5d3650bc9437f5b6cbb3f22628`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:288ab70606798fce0b498ad955d5dc54bb03ec0c0832d582d137cd79772d001c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a163bb449af86570efbb2c848f4a56b0a9f75e2c9bab460fac75b282e0ee9659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60290217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ebf1e005f416f00f58c9265e914c41d744ca6aa1cfbeee885ba91c67104b69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1769990400'
# Tue, 03 Feb 2026 02:49:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e7ee730174f13176a4a2ca706f251743bedcb5459da1b8f275d5b6bcc67c0aef`  
		Last Modified: Tue, 03 Feb 2026 01:14:19 GMT  
		Size: 48.7 MB (48655735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbb37aa9daedccd57c940309ed43a39d7248abc940a23204d466caa4499871f`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 11.5 MB (11540452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1930f996b21f85d26d813979c448b5cc33d9133a8314e6eec99d3e973f6035c`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a47c885c79a443813591c82a08a80cadd63adef2c8d39f9547d22badfcacb`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035ddd951380f76413ebc0059b6934df85dc73f566840fbe23db460cfcd656e9`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 90.7 KB (90675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef19c1eb6c1cbf32f075f42496b94816b18968b15c0f0b69876955199b6719`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14a013c4124a4a318ef9462fba9ce8e7d4f7ade0f5398b9583274cdf91689f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f2134a5a1a99b81c7e83acec3a0283963987a07471c68c3cdf183c9f72d260`

```dockerfile
```

-	Layers:
	-	`sha256:2164015860c8679b1861e5dd23a57a9c9cf4dfe0487d529174fcf93b3b40604d`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 3.6 MB (3608579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cff4e739dd29e441abfa38f38ab0d7eff091449c92875d8627eed5ac223629`  
		Last Modified: Tue, 03 Feb 2026 02:49:17 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:311f95d8c09f720583c8bf71fe7f6a89b4dda12c1383d28957ad4189fae03e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60199406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee76e1175122295cf681eed5d09471821de89695b8dbdc0203f5375abc37a83e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:37:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:37:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:37:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:37:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:37:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840a5ae9b27a3ace79b3cf0fdb2bddc6e0106d136b74b66d524377fecce1c8ee`  
		Last Modified: Tue, 13 Jan 2026 02:37:21 GMT  
		Size: 11.3 MB (11284159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b04b69ed7b0dc312198ad357b2412c074128f959f7293aed12772b8024660ef`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ff9f4d2e3110d267b69e9306e4a2c646baa86f11542e5890a5a610a3d81b20`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624da5a767e899231c0f32b59b33cb218d6cd91826a2f6983521bf73ce77dca`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 91.1 KB (91090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b7c6b056e0df9d0635f7da4ff9b04e3ae4d6bba65d77282f987483a0af1b94`  
		Last Modified: Tue, 13 Jan 2026 02:37:21 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af4aa92e279c4915e30df6e7cd29dd117fdacc453c824e0a90fe24c7b6d57a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32574c6ac80df83065fa624f2b51be56590164d0a5cd3bb7ae01b53b0c76a077`

```dockerfile
```

-	Layers:
	-	`sha256:b7dd2f04643444f2e93834bcaf87bfba2f61ffde30c642adee29597f4ed07e2f`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 3.6 MB (3593392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958c23f7a6c9a93a6fc9cf4709b5056222a686e1d725659fcc9f3c9ad5383603`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4e99c3c6e5582d78c9e78cf02a431906f358c74b00f4f0194cceadef329c0811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61816562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b1b6bb9725c2c422ea1ff4e255221a0d3b6cc81e7d5b5bfd1509bab991daeb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:13:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:13:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:13:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:14:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf06d6cadb4b597f7d41ef40aa97534c966810a7be12ffa98ba0c62d0b6d87a`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 11.8 MB (11777905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b17d2a39e5656e48ba83c086e5b2cc1bcf80b3fa2bd447dedcd331732869dbb`  
		Last Modified: Tue, 13 Jan 2026 02:14:09 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c37104f12b85966a7ba54059613e4fb6cee349b2e91746262d8151289c2b0b`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667de473d81a94e4ead18b60fd01798a848e3638b2f0aca250844c57926eda`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 90.8 KB (90763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1be9d3fa61a9e252b493065fac5b67a71bd9f7acb6ee3d71de5a31fa1e7bb4`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a83992b948f52e474ce13a2d7219f483a042dba1531fa41ad79976890dbb9bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf46cf6dd92a6377c617e5a247502d0f0d0faa3552ddd363c849b3c85277b7b`

```dockerfile
```

-	Layers:
	-	`sha256:d99390adbd9fc049478e9f3b542594c7912a0d5b18a72b084290199625a8d438`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 3.6 MB (3590474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3fb5f51573288a20fa8174e7c6f3d3943d5d35eaeeba105e823e4cbfab7236f`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:19ec59ed4b51fae27dd278d0bf11380b21edf2718a14a056b71c205ea984a184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:e497487cf2720a736bacbaedac3ae2436433d09e6ad0bd8a65c86d41f4d063a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33274380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43de36e1bb01c325b9bcc5b3aa2750460e5d3413af9817fb57aff5043948e09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c31a1de4315e0b58b79ce211ded98e483a09dfdc7f9a6499a9a7ce21a39391`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 3.6 MB (3624300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ba782c854a068481cc1d19b2b885bc3941b0f687797867734b959977f68bcb`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b50cebc4c825ee52a417c7198f1be150abccfd99fab7124120dc49208d23b3`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ddc7f4be458215b98db1adbbcdd655a576940b797584f026f194d25aea142`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 111.2 KB (111235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:25d21931ef63fecca937fa9c226d4b9c972c6a07ab7b12d6cd472e98c2f391b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bf0f83a34f3cf53098c7ebd08efc3892d2749a28113b59f8b7fae1fc13e58c`

```dockerfile
```

-	Layers:
	-	`sha256:11dd9334d128520572ee5d6644d929c8e386a02ca3d2ec2ff0bcf28cf4bda108`  
		Last Modified: Thu, 15 Jan 2026 22:34:24 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07dbb8c42e97f3cbb99e13a0cce5eaeb2908125d20a39eb7a012208555bb6be0`  
		Last Modified: Thu, 15 Jan 2026 22:34:23 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:de8c6e985f8ebfc9f9818ad855d16fa99573bd46e0e9f4dd84d73e19618c9a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31098806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fd5b3ddc77a114383c7ee36112f4540c8891c057f8e7a8cc490ac45e5716fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:36:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:36:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a4ea43c440ed4c5c6940006aeb234cf69c04ad0392d10b84fd9766e4a34f8`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 3.6 MB (3602633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae0723c728afe1d94014082337ee6c2c149eac4aa6f8373a264ae6ef9d99e8f`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7101abc79e23d3f25054e865a814a95478cc4e41c4b4ccbee0cc361e535cc37d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c3cd39c7b72b92ef079ad69cd3630b8af83c92b6ffe3230be891653be676b`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 110.5 KB (110499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:886473be4217eaa0f6c8744ebd3176ca4d06f19d1a76302fb19c67bd0726beaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468d90fb319d993524a4713f622cc2c3e500cd78f13f40e5551c0563785618fd`

```dockerfile
```

-	Layers:
	-	`sha256:58f1ed8735b4542a9a1bea99b6f344ded0a424a110de890d71fa473bc53b359d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d01ecd9429deb21559e16c32c9f4e387c8f8033115397f07ceae09f9725024d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:f8a04f8a8dc04df731f84789fcb71e800edabbf6bb1aebd975bbca1fa8f1c3a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2cd764c7884ab25b110fddde83cf33834467579766c56cb1ab549e9a3ea90470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33274712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc3af720234bde69d207e0f9fdc641e991f2697f3fee5ae0aec4cf34d6223c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b59d1ef943d834ee1a50db8acc83df82aaf8bb732bc303a4d9ac314ca79ada8`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 3.6 MB (3624349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903068be00a686117d5126046cccd885353091e8878694caf04fcdb458f28010`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7436405aa87ebd15250cc5d262e3a512295411df4ec41ab2b7a149be703da`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09c2a0a07d862cba86e9245a3f5fc8b54ab7bc332077758a597ebd129314c71`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 111.2 KB (111237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb3eba37faf714db0851cc8861baaa63273442a84287700b6607cbf7e50d4d2`  
		Last Modified: Thu, 15 Jan 2026 22:34:35 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93e9d3bcff981b6bdaebb3818c9abfdf384cfce638b89d07c9d9da38979e63c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d61845c72e5e377c08f2a586fe8d061339c3f115497261045d09f1c31a2058e`

```dockerfile
```

-	Layers:
	-	`sha256:5fb780292168a3a5dbe5f8ce395b7bf5beb0798a6ebe2dc57020d67f10741c2e`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd6a705adf1df71c78ac76d86175ef0b0fa0cde1b1b6ec1f5a5a5337153629e`  
		Last Modified: Thu, 15 Jan 2026 22:34:34 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:741ddf278e88035b94dc004a4c6a12f141ac542d2e852ecc9b064c70994cbadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31099022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af2062e8549cae074e26beb662b0eb5efc3f3383962c6318a236bb569173e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39623f164b7c134bd7c870258397b9ae29b76f658821cd89c872006781773a07`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 3.6 MB (3602582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc84ee017cfa97d082301a68c097692ea26fbf238220f31788ab3777fb0915`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62e658825b155b9da439360822a1b71de7886aa64a9f6b2ed952f31379c285f`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf949af04af6e2380e6e33215d31850a1aaf11a41caf3df6b222373f2d115b`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 110.5 KB (110485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ade6120433a2a5a27b1949103586f6bea98efdfbdcde54a84ec40fc4703e39`  
		Last Modified: Thu, 15 Jan 2026 22:37:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2f764bf523306b0471b6acd75e196f3491fa44291dc40435483f27e5d5637037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b21632db7bd9623230cd92a59777549d877ad4ed24e036f4a1ca309c4a29973`

```dockerfile
```

-	Layers:
	-	`sha256:09017ddbca29fb71dcab82dce0807d3653f2cca9f0d865f7a27c96666e61c0b9`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd1544fac022fe23da5e4aa065119ee55176834cec20f0c37704625726caef3`  
		Last Modified: Thu, 15 Jan 2026 22:37:14 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:3b1ea9866549892bcfb5deacf0a8f1dadf9c2f98bc63ce01b622f7745ea46c65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:39dab19ea0056fea381a2e3081c573bfd689d2656f5cc81fd3aa41ae0aafcc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a7aa252972df966e8bf224240d541b7d88ce8370c9fa313cc2adeea313cf30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febb96c351dc6c0d19a074b7bf0a980146f228694ed515a5e6e4776348b5d83`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 3.6 MB (3563150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baad77fe67014a99e49ccbb36bfa471550dbfe256c0a7997b77cc92db588b238`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d558af79b48a1dc1eba2fd55a45ab5177f557780a20b8afd5fecaf034f577cb`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c341089aea08830c751d3756d07510e12c782bb60ddc69ebaab8ffa5029a30bc`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 104.6 KB (104575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a7b83fa45a2ec02faf249af7419c07420383708eb87fda857dbfe98bdaed5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3607dff0dabf71a31ae8a8d3b3a75f55737f7a69e1d3dc070f88269b85f1486`

```dockerfile
```

-	Layers:
	-	`sha256:d9ff96588e736f2de78e48e58e17efe725819c5302f84fabc2e05fe87cbe845e`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d4dd02fcbaa60ee0e870849b37cadc44a2fc95004b2b0c366e2b4f9fd44b22`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bbd6e0261957f20c46d34962987746d93400c15e314c81f6a64419c91b7b065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32532687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24eca9e911f1ef800afe0cd19724f336ae82260d50c9f4b9f782df0356d4b3c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11d827e327f828ef515a5ee3828fc7df7429f4b6fbac0be158005236e186fe`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 3.6 MB (3560792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e9075292abfb37049926dd278eaa023c87947273bac27af654d465972b0ca`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a28cca6467154fa487391fafc9c46ab2569d2510dcce267c204dcd1149a12f`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7e1041691204d39dc1e2e6b9a0d184d8a90b0de7386c680d0babf4b584849`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 105.2 KB (105161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:48009258df992087de7fb120477a38bf8c9e7890ce32c805c7f253896db012ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e121faf012875be8415caaaa95813bfc205ab8f562b254334d16b738816f0f13`

```dockerfile
```

-	Layers:
	-	`sha256:f1c64391a4650e5d5a17196f03e5b2562ea6d98a2f0c2f9a560cefef58af1128`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bda8fe80c01c55cfd927fcb6b54d5213dc934c85a38e089a1945a03b8baf762`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:1ceedf2a318dba40426fe2f72e01fafa822b183fa308fcf3c39c012ee18a5443
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:29bd654a9dd78b6a5e66e56203ea411102c7f500bedb3be6946505c041958f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33397014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220675f233145f83f0cc39ac185b91891302544e001f10d936298294ccdccb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:35:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:35:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:35:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:35:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:35:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a548ca73cf3c853fcef8cc5fc4e37b42dcc57abd2ed979e56815d39fb4d2e1d`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 3.6 MB (3563186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43697b196e8d2c4b0a8ba22dda06c60a2720d7ecbb327195ef4a733a9a9199a8`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf22aeb3829fe498fa19c16c5fdb441e50cdd85738b65a2d38355b2322d1bb`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e67f0420cd35a361f4bcd7f5637294ec870f6249ac769578cb2b697880c549`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 104.5 KB (104478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f6e8a4dba4124fe5efdf1962988721ec07e6fc6878bcc80a9a379f9253e849`  
		Last Modified: Thu, 15 Jan 2026 22:35:22 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72734c10c1cf995c81e4a91d122677f146d6e2563af5405a01fa095d936b2f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83569a852db661e4bb3cb966fcca962060a4d94573ed0f50ec5830ef247bd5b7`

```dockerfile
```

-	Layers:
	-	`sha256:b7b9ddbe9fe86bcbffdd90e2ac87f34033401026b3ffa5b30b988156ead4f9c5`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f23e802c7e970c3e019b577b1c7691e1f9475949ceaf9b3b66a265ad188d36`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:337e0094efc3a087b25a981421b53f1d439b30ff45c4b8cbe2de4afcaca9a9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32533146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992ff80c45aa201e62f7f3f62e219a102100fd5f4f2888527233f9f87206a02b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2aea097a4bbb9d5bdaded81482eedf9b99f3c5f026ca55b6e403563c587b66`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 3.6 MB (3560842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76004830fcab5147953ec62120e9188a61c12121f2327a2de3b15e88d02b19d`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33a41e6ec1c2b8fe89edb69a4ffd926bd25296f84ed1cd3c94a95975d23a25`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f32872c3ae902f9b9f8f6512093ee79fa4f3b288d84103139a75f0a04a60e`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 105.1 KB (105142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d33c20ca018680f26d1c2204d39af5752691853971325601cd21bee5c51074`  
		Last Modified: Thu, 15 Jan 2026 22:38:03 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:96427596211b20b4819332d643f7cc48057a7e9d68628988529c08c48fee0d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673f5866c150a6e4fdeaf156ee392d4569b2e7ef22f87585d60ab6552fdde497`

```dockerfile
```

-	Layers:
	-	`sha256:8892abf0464711dd694b127d86ae7fbe36a931d3c3786f23ca2bec3f10d2ea55`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e09ac7a089e43b83ed3c810459f514467750bce8124e594af9e8ae6471226a`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04`

```console
$ docker pull neurodebian@sha256:ab139e2ef8b811558941eff017d1f467deaa77fcebcdf3189633727ef717dc92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdc67ac4dd0d651097ba75d3f513b34e66af0bdfa85db80045d15880faf9ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36682742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc9a62b14ecbd0c50b253059091a66a5c95e0809527bce9cdece2619b81e21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Thu, 02 Oct 2025 22:51:56 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 103.6 KB (103644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87fb8fcdc3533806d68ebce00bcfcf60c95a4fd2ca27173aa2131f4e12b9a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7aa5c68eb77711d7c5504ea0dd43319dc6ba5a495e2a39b29e42dd4613450`

```dockerfile
```

-	Layers:
	-	`sha256:34e86114d346aa4146ae590dee647494234ddff44dc9bf93ed557394aed25887`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d0215dbda4b85ac69b750d98f8f3eb9aba18829cafe490ef6c04e7f1b5d3575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34803835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6196b8372a58dd339a5cd7b297736021c12b067eaa196975ee6481a581ec22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Thu, 02 Oct 2025 22:52:03 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 09 Oct 2025 21:21:53 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b6e0e2468e055fd3994fdd22716a6516ca822a0b893af378cfe9b7c8c92ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b634830ed4e5ae3eba300cf243790465b87b6d976898e0bdc93781f17d3473b`

```dockerfile
```

-	Layers:
	-	`sha256:73f73f1097d47935c4c36115e56c20ae5811fee70906bb8d0100cacf857414df`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04-non-free`

```console
$ docker pull neurodebian@sha256:843d307ce6bc09a7cd1b57e44466adef4c4764ea1c793ae5816c4c23f5fd2e42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e3b0aa3a1e9664cb5a8951141d1855604212beb174f638ffd32f46742ed4bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635066dc43129e20e37c95f2235d3e316b7d3b9c2aba40f0ffde2b54e2e6e2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Thu, 02 Oct 2025 22:51:56 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 09 Oct 2025 21:20:58 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b03d30cc46e85e007f546cd2c4a415622d8016571f0fcd74004ece8a9d69a9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b1b3d34374f9d8719267a2de2de8be8524966deb0e192f3a0d0b9e95bbf7e6`

```dockerfile
```

-	Layers:
	-	`sha256:75abe1e107a33427871261a37ffd5362e38bd76021a38d45be8b8ecfd67cf1a7`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8bb52949ffdc66d1b1c45b166770d0321d7082209a408f0dde0ce50355c437d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6029e77c7f8a48311858bca5d16c501aebcd7dbababb443b3c892392f8506a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Thu, 02 Oct 2025 22:52:03 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 09 Oct 2025 21:22:07 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29ea36baad60d33ffbfb5fd8152d415e121532b4008b174a68251c71851548a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5656dffee277d964d7af531bee03d767b53dc21bddc33bbedf5b7d1e0c3a1668`

```dockerfile
```

-	Layers:
	-	`sha256:a897c9f03a98ed8cc43baa74786f9234dccd6f6c51fe452db7dab397fb9c66a0`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:3b1ea9866549892bcfb5deacf0a8f1dadf9c2f98bc63ce01b622f7745ea46c65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:39dab19ea0056fea381a2e3081c573bfd689d2656f5cc81fd3aa41ae0aafcc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a7aa252972df966e8bf224240d541b7d88ce8370c9fa313cc2adeea313cf30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:34:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:34:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:34:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febb96c351dc6c0d19a074b7bf0a980146f228694ed515a5e6e4776348b5d83`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 3.6 MB (3563150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baad77fe67014a99e49ccbb36bfa471550dbfe256c0a7997b77cc92db588b238`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d558af79b48a1dc1eba2fd55a45ab5177f557780a20b8afd5fecaf034f577cb`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c341089aea08830c751d3756d07510e12c782bb60ddc69ebaab8ffa5029a30bc`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 104.6 KB (104575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a7b83fa45a2ec02faf249af7419c07420383708eb87fda857dbfe98bdaed5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3607dff0dabf71a31ae8a8d3b3a75f55737f7a69e1d3dc070f88269b85f1486`

```dockerfile
```

-	Layers:
	-	`sha256:d9ff96588e736f2de78e48e58e17efe725819c5302f84fabc2e05fe87cbe845e`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d4dd02fcbaa60ee0e870849b37cadc44a2fc95004b2b0c366e2b4f9fd44b22`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bbd6e0261957f20c46d34962987746d93400c15e314c81f6a64419c91b7b065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32532687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24eca9e911f1ef800afe0cd19724f336ae82260d50c9f4b9f782df0356d4b3c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11d827e327f828ef515a5ee3828fc7df7429f4b6fbac0be158005236e186fe`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 3.6 MB (3560792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e9075292abfb37049926dd278eaa023c87947273bac27af654d465972b0ca`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a28cca6467154fa487391fafc9c46ab2569d2510dcce267c204dcd1149a12f`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7e1041691204d39dc1e2e6b9a0d184d8a90b0de7386c680d0babf4b584849`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 105.2 KB (105161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:48009258df992087de7fb120477a38bf8c9e7890ce32c805c7f253896db012ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e121faf012875be8415caaaa95813bfc205ab8f562b254334d16b738816f0f13`

```dockerfile
```

-	Layers:
	-	`sha256:f1c64391a4650e5d5a17196f03e5b2562ea6d98a2f0c2f9a560cefef58af1128`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bda8fe80c01c55cfd927fcb6b54d5213dc934c85a38e089a1945a03b8baf762`  
		Last Modified: Thu, 15 Jan 2026 22:37:43 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:1ceedf2a318dba40426fe2f72e01fafa822b183fa308fcf3c39c012ee18a5443
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:29bd654a9dd78b6a5e66e56203ea411102c7f500bedb3be6946505c041958f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33397014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220675f233145f83f0cc39ac185b91891302544e001f10d936298294ccdccb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:35:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:35:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:35:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:35:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:35:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a548ca73cf3c853fcef8cc5fc4e37b42dcc57abd2ed979e56815d39fb4d2e1d`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 3.6 MB (3563186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43697b196e8d2c4b0a8ba22dda06c60a2720d7ecbb327195ef4a733a9a9199a8`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf22aeb3829fe498fa19c16c5fdb441e50cdd85738b65a2d38355b2322d1bb`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e67f0420cd35a361f4bcd7f5637294ec870f6249ac769578cb2b697880c549`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 104.5 KB (104478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f6e8a4dba4124fe5efdf1962988721ec07e6fc6878bcc80a9a379f9253e849`  
		Last Modified: Thu, 15 Jan 2026 22:35:22 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72734c10c1cf995c81e4a91d122677f146d6e2563af5405a01fa095d936b2f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83569a852db661e4bb3cb966fcca962060a4d94573ed0f50ec5830ef247bd5b7`

```dockerfile
```

-	Layers:
	-	`sha256:b7b9ddbe9fe86bcbffdd90e2ac87f34033401026b3ffa5b30b988156ead4f9c5`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f23e802c7e970c3e019b577b1c7691e1f9475949ceaf9b3b66a265ad188d36`  
		Last Modified: Thu, 15 Jan 2026 22:35:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:337e0094efc3a087b25a981421b53f1d439b30ff45c4b8cbe2de4afcaca9a9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32533146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992ff80c45aa201e62f7f3f62e219a102100fd5f4f2888527233f9f87206a02b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:37:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 15 Jan 2026 22:37:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 15 Jan 2026 22:37:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:37:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2aea097a4bbb9d5bdaded81482eedf9b99f3c5f026ca55b6e403563c587b66`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 3.6 MB (3560842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76004830fcab5147953ec62120e9188a61c12121f2327a2de3b15e88d02b19d`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33a41e6ec1c2b8fe89edb69a4ffd926bd25296f84ed1cd3c94a95975d23a25`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f32872c3ae902f9b9f8f6512093ee79fa4f3b288d84103139a75f0a04a60e`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 105.1 KB (105142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d33c20ca018680f26d1c2204d39af5752691853971325601cd21bee5c51074`  
		Last Modified: Thu, 15 Jan 2026 22:38:03 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:96427596211b20b4819332d643f7cc48057a7e9d68628988529c08c48fee0d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673f5866c150a6e4fdeaf156ee392d4569b2e7ef22f87585d60ab6552fdde497`

```dockerfile
```

-	Layers:
	-	`sha256:8892abf0464711dd694b127d86ae7fbe36a931d3c3786f23ca2bec3f10d2ea55`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e09ac7a089e43b83ed3c810459f514467750bce8124e594af9e8ae6471226a`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:4bf6259209bc214c61d034c1dc11a5f99f24c56694fc40cebf1fa4e991e82640
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
$ docker pull neurodebian@sha256:bfe6f18aa6a74c90c1bef54a8ecbfd1554d462da56f4431077902cee7e35743f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59679073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734174826d480fd0ca4221a27524fe98e871a54a19c068307ec6b8d151189d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f763d27f0cca3eca63d032df25da1781edc10ad21bb6ec6472a87765b5d494`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 10.3 MB (10292413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2193d3bb29390a43b5fe3cf6ef36f5d049269591f33a3f65f1c3ebf33ea628`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f82edf0cab6319880f6003cb047a9679b2b534d136feeba495550f279df6cb9`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae03b3a868a98138feda4a04a1f015e865a3599f8231275cde4e2d3ab18157`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 90.4 KB (90354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f2df40ce739fcaf54c09cdf8f844f97b7b89ddd3a009cf66056798e7a816d`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fbf95673c18f9bfa0a30481eb45b538fec3995c608702a1c1d90e08da42446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9f83b2f6643450c6e9f512971c820c8345c704dcd2e8cc7a8756a02e736f86`

```dockerfile
```

-	Layers:
	-	`sha256:6c76910ec532300ba0ac33261e0fa300df86a2a7236c44063bcf717e3999b372`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48dd7f90c47288d683499a84f5abe7001a411496c218e1bd8e77b25b0888176`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3e8b1aee676dde93acde9fac58fa3ab60f76be22359149b15a158f66571828b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59816200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16820c26affbce98ddae6fa99af774b35f36fa48f83f0175f7cc280513d9df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:36:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:36:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:36:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ed602a8d82e45752b42458f6c6cf735a34652ba4dde594e695631d834d59b`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 10.1 MB (10073712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8fc00822d28ca96ab3b0a281c9f30f594ddc2a1097c1d118b5a8d327ade838`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8209c0e736639a6f4be8dbb64c8eebcf8f0660d2bfc6801b3c25864d8deee2`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850c1d0537909467bd63adc7a9f8b6c380009301140d89edfcf9e56b6a682db`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 91.1 KB (91057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f820caede12aa6a0a73d704ba9b536c2a46a1c60230cf73b319c81ab1626f30`  
		Last Modified: Tue, 13 Jan 2026 02:36:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9e27486911deee56ba88782a368ea64fb2d4cfebf43f5046a845fd248bd042d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ee1f59febf6225a8b47ae664b8af048babe29a052e8afed5aacf201038bfa7`

```dockerfile
```

-	Layers:
	-	`sha256:f6eed23b2bfe38aa7cbef27424d9b0bedeef111763c3f9036af89d8ad36602c2`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 3.6 MB (3615635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df7281df837c359d65967773d79bc4901995aad5084db01a47562adb7c7d61c`  
		Last Modified: Tue, 13 Jan 2026 02:36:36 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:0e960ee0faa42f6bdd57961fff7557121bcaf8613b82e9b199d40d7a0261d96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61359689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571fe39bf716fc3e4014c560ab9d7be66fbb4dc330c7f227e15b9de763fbdf3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:12:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:12:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6161421471c9fb8d6e355616caf09b7087ac27ca53984bcd4134a0b0d7e111`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 10.5 MB (10466725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ebcc0e9e4361a538531fdba9070f9175a771b5bb299631b4e6ba78b8981ae3`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895adfd9029fe52f402919d58a03065389e5be8bff8acbf6465d5a18b525fef2`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7e6cefa33611a70c52fbfc73b63e42b2cdfc1fba6226f458dc3f5c739c142`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 90.7 KB (90740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3130aa08749bed8751f83a3a79d2ab7115ab45e908a1b0fffbdd9f80014cee1`  
		Last Modified: Tue, 13 Jan 2026 02:12:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e78e25dbca6377a9c55bca652f94e0e9be3780e215df940fb294f1d5d86968c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f5b3a6f545f0eba153876fc40fb4cce27fea22fc5fc61617969ef489152f6c`

```dockerfile
```

-	Layers:
	-	`sha256:847768114c721eaa57ed7d191df816ead0fde24426576323ca0caead4f71653a`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34278bc983bca66a2b8695d2725d6c0031354a486b9d39d322df70ee7d8ffc6`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky`

```console
$ docker pull neurodebian@sha256:ab139e2ef8b811558941eff017d1f467deaa77fcebcdf3189633727ef717dc92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdc67ac4dd0d651097ba75d3f513b34e66af0bdfa85db80045d15880faf9ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36682742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc9a62b14ecbd0c50b253059091a66a5c95e0809527bce9cdece2619b81e21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Thu, 02 Oct 2025 22:51:56 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 103.6 KB (103644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87fb8fcdc3533806d68ebce00bcfcf60c95a4fd2ca27173aa2131f4e12b9a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7aa5c68eb77711d7c5504ea0dd43319dc6ba5a495e2a39b29e42dd4613450`

```dockerfile
```

-	Layers:
	-	`sha256:34e86114d346aa4146ae590dee647494234ddff44dc9bf93ed557394aed25887`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d0215dbda4b85ac69b750d98f8f3eb9aba18829cafe490ef6c04e7f1b5d3575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34803835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6196b8372a58dd339a5cd7b297736021c12b067eaa196975ee6481a581ec22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Thu, 02 Oct 2025 22:52:03 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 09 Oct 2025 21:21:53 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b6e0e2468e055fd3994fdd22716a6516ca822a0b893af378cfe9b7c8c92ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b634830ed4e5ae3eba300cf243790465b87b6d976898e0bdc93781f17d3473b`

```dockerfile
```

-	Layers:
	-	`sha256:73f73f1097d47935c4c36115e56c20ae5811fee70906bb8d0100cacf857414df`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky-non-free`

```console
$ docker pull neurodebian@sha256:843d307ce6bc09a7cd1b57e44466adef4c4764ea1c793ae5816c4c23f5fd2e42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e3b0aa3a1e9664cb5a8951141d1855604212beb174f638ffd32f46742ed4bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635066dc43129e20e37c95f2235d3e316b7d3b9c2aba40f0ffde2b54e2e6e2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Thu, 02 Oct 2025 22:51:56 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 09 Oct 2025 21:20:58 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b03d30cc46e85e007f546cd2c4a415622d8016571f0fcd74004ece8a9d69a9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b1b3d34374f9d8719267a2de2de8be8524966deb0e192f3a0d0b9e95bbf7e6`

```dockerfile
```

-	Layers:
	-	`sha256:75abe1e107a33427871261a37ffd5362e38bd76021a38d45be8b8ecfd67cf1a7`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8bb52949ffdc66d1b1c45b166770d0321d7082209a408f0dde0ce50355c437d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6029e77c7f8a48311858bca5d16c501aebcd7dbababb443b3c892392f8506a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Thu, 02 Oct 2025 22:52:03 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 09 Oct 2025 21:22:07 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29ea36baad60d33ffbfb5fd8152d415e121532b4008b174a68251c71851548a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5656dffee277d964d7af531bee03d767b53dc21bddc33bbedf5b7d1e0c3a1668`

```dockerfile
```

-	Layers:
	-	`sha256:a897c9f03a98ed8cc43baa74786f9234dccd6f6c51fe452db7dab397fb9c66a0`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:86a955a6da2fd6e49310005ddd799d6d0c1b03e61ec3a26bf798c7e17fb2dd88
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
$ docker pull neurodebian@sha256:742f81326d6458fc4835788d8fe3317f77b687290629fc738389f12c4814df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d9d256c1ca3e4c144c863cc2281316c3cc3eb45088369a88aea3a40a0914ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911d1558a1b3010131d47ee741db0963c889273e31e2a95035fd6cfb9f17c1`  
		Last Modified: Tue, 03 Feb 2026 02:49:21 GMT  
		Size: 11.5 MB (11540410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6309d0a7b6729391c7f1314a74b6b06b07c4646ed52a3d9e7ce4cb11daa5bc`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0740384dd13f89422fe1f4638c08fb758dc33e4f5c9810aa0b1d0a69d7fae0bb`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 90.5 KB (90457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e1ba3408ddc3dfef56dc25b1915ff61fc917b613ede0a431592467c4b4864a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba3eb40824aca52a92259785bc8cb173186a6bb1ccb406742f34f2f6ebfec74`

```dockerfile
```

-	Layers:
	-	`sha256:7d69e622a5bfed66bf691b20cdf1aa82f53f6f580b821ab40aec94be47d4d4b1`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 3.6 MB (3607661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7e7edca04a0e1aa36eebfdd3e3f3946a1ce7603207a77681ec83592f931e12`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fa0ba41b4e84d980cdefd58691824eb67a3c89e5ce751baafa6676d27374880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60202507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98d5b725f75bacf9154914537830dad7da7c50305e6a09d608433860d4f0361`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:38:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:38:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:38:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:38:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da01bcf829ac0481e16c259eb82b33f353df66d362cf4da5276683b0b2b9319`  
		Last Modified: Tue, 13 Jan 2026 02:38:20 GMT  
		Size: 11.3 MB (11283991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b508d27ae81a583413ba342757fe3a8e81b34b43dcaf3cada42f01296b880433`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb85291bd22f4f2d342b547834f90db0ef1315dc5b3db25f80d522429c600b6`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0758f88b1ad03441d33efc0759464c7090116fd1b6225e6bb3549fba6af4c928`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 90.9 KB (90900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fd4287db1c80d84718a24bbf7b419272c01514b21c14f2017321173cfbaf6ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6178646fb591280a4322dda9041233d675f14ba891bcf3c3cdb42b6669a33488`

```dockerfile
```

-	Layers:
	-	`sha256:0827d76799ed2ee2ffd22bb96db6c785e7ab0c7910d70e72af72764c15894510`  
		Last Modified: Tue, 13 Jan 2026 02:38:20 GMT  
		Size: 3.6 MB (3594069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079930c725e760d95d23f7f8d75cf0c97b6bb6f92cd6ee6185135a9359b10eb9`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:75cfaf1c6b7dc32eea6e9ad0986a93ef5eeaa1ad62b6eb7b9b92c50a27cf5a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61815161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619842c0a344cd4cc323e6bce0195b699ffcec1e1e11d144aa7ba65e03ae8e4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:14:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:14:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:14:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37772ef8b09ff9ece288ef28843ba2b28651580cfaaa82c9376253b633ebec17`  
		Last Modified: Tue, 13 Jan 2026 02:14:57 GMT  
		Size: 11.8 MB (11777889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b62c15fbf7ad5a88504652ccc590c41168dd750ad796ee00cb146201e51d41a`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572d1ccf01b56f7a38834164db204119048dc7f9118850e151ee844646faa2d7`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc6d97bb71fa9592ffbe96f2e81728683ccd72aff6a26e2a3dd0b3342b417a`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 90.6 KB (90557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:86bbfdaf6aa29318b32ef02597c6614d32d58e53aba363eaa8a6c80a860a36fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109185c65d9918c90b219c20784cc9ff1d784bd8e3c7eb098dd0571837b25969`

```dockerfile
```

-	Layers:
	-	`sha256:b48b602aa44be33ca0546314de063837fef65f8f602a6f9a01c8ec2a16fe31a9`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 3.6 MB (3591151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8768990e2a7177e584c19848ea859a7128c68a9856c85d9b11594e75f37bada0`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:3f7505cd2a98c7b65a1686ec9196357a8c77b8f9e87d476ac19a198abfe87cbd
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
$ docker pull neurodebian@sha256:a34bd5c63c5d4d902f50950efd6ce5dca64b1addf6060d5cb0d1249f0cbee543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308f8f8e8e8be830f406d62dc791fd094ace9d9714082e5a38b94de80c022113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7002f3da964c57bd455c7ea9aea032a614f96ad162a44a4e3be7f438517c9a`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 11.5 MB (11540369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfae06b9f53d369e6035db2bb25acc88db5141f15668b9c187df731a53d6330`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0675e38a13a9ae911bed6a859416965f3afb652c0c0bde63d3aa4b7c256fd8`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 90.4 KB (90432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a622e4dd49c0b33475fbc290bee154d0d2fa0f6b39499fc01581d935969bf0`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e40dd2e539b3db456883132b1b1edd605a481e44ded2b819881cb3566719049d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a040ca843f8191579ffafa4b24724273fd39a8d8db116dbf48cb294a674d25ac`

```dockerfile
```

-	Layers:
	-	`sha256:80d0cd2e330fc9bf7aa1ae15a2864ea8ed86232bb2bdabd6bdfc79ab09150396`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 3.6 MB (3607697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44da38342d0de406e284f67ea9541752f7cdaec248b21cc9996fbba57ab3770`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0c396589891d3c617ca0410ea2ff3ef8c48ab233cd8826d253a933bd2501b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60202796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427aa2ced9486bd12be502f9419345de174c5654292a3ce2ff4d35ea097d7a95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:38:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:38:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:38:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:38:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:38:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a5edd52237009e0cac583b17514f638b5d8f08eedc3930a2e812e893bd6c7`  
		Last Modified: Tue, 13 Jan 2026 02:38:53 GMT  
		Size: 11.3 MB (11283894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc58c09ec95440415b943959da0113ae578e6d378ab910c68074397ee96024d`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3e2db745e5179dd8918931028318ac50146b5c7f4ed70102c02afdf323fabe`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d8c2ee79391cf1b2076de818d699484239f70dab0332479d0eb6876eb76d24`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 90.9 KB (90868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7407bf616dbd5929f5d38b6b8161c64ea318bef988d826e2db12e1c7bdfa6b3b`  
		Last Modified: Tue, 13 Jan 2026 02:38:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c40f5ce3cfbbb278253579b56d9308fe52a4d1238982cb42d68d999e8e92b88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3610176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d60536309a11b855e32b84990e0453efdfe7827f3a33e9562615a2ea3d04f5`

```dockerfile
```

-	Layers:
	-	`sha256:9690eb218fc781102f03827a207ea0cff9fff756f8122a35552468f93250a736`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 3.6 MB (3594105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fdaae74eb9cff639961a564fad50873ac2bf56d2c0ea39128352527d6b9e666`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:29c6f2d2701bc0d15ab7aecb27bd6a46db79c8e5a7816d1289882bfa328a0cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61815677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c093d6a9a0e2ddba9eb0857a20960b123f24417c1896d87284b76f837efa073`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:15:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:15:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:15:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:15:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca115bc00d353cad320bbfd72a4e71bd2d894f06113dcb9a17030fb18e14aa4`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 11.8 MB (11777974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109172636f5d8d15495a86c47640b8833da31afa49dac51dc788d331d51b4194`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabaf41752bbfa6fc79aa7258daafcea5cd5ad20b4ad9da0d86b1e88d1a8bedb`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d143b59110518f6bd31d6dd22cb9813ce4fcc6f91f1241d926ef3b57c95d4`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 90.6 KB (90564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d2cf67c8b76bf197f0430f4758d401b3dce448aa47698c1733eaf18167b00e`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:304666b92baad6e4035e011a329a7d8bbd4352a94a1bbb7dddd27d4dceb391f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c456b6dd20574b34e286d508e125f0c53668b0932f7c6882109698912166b43`

```dockerfile
```

-	Layers:
	-	`sha256:0a44ae40c2d9af50ce8fb40c7a0100941164bfd8490f4e7115b2766a546e667a`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 3.6 MB (3591187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c08d2228b8f636f2a594f5106ad6f754469e440be86a8eb81b47366aad1557`  
		Last Modified: Tue, 13 Jan 2026 02:15:35 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:ffef758c80ceabbba337660d9965eb402f9211965a7659511c9648332d2c09a1
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
$ docker pull neurodebian@sha256:da3b9227f84c0e82c2a1cd4cb5e96ec28789730085a1ac4652b6bb91620d43a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59678819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8b026c74f7c723c4dd8ef3d34903dbf19b1ec0bcfb0356313abfeee3f0d4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae41ec031155c98b455bb78067eba48a17546176cae679a09109c6f40044b853`  
		Last Modified: Tue, 03 Feb 2026 02:49:08 GMT  
		Size: 10.3 MB (10292604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c456de52ce89d78c3e11be3ed11cac3ff2a3bbf1b5b7acbcc34864caa6ed1b`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c3f547274c1b9aba5a4c1dca0de6439e3641e2927b7ff0e29ba10f2598771`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e44b0ddaace5231fb0277c41a8f1dd1b9a803222537517cf5fc0faf0163b35`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 90.4 KB (90356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af8d1c9f950620612b890e7e6a4d8c5e0b2b9f2e5fdfb0bced7707c0f81c1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a741a8c1833792cc9553aecb085450cdb9f1664685ce094c1941eda5289f656`

```dockerfile
```

-	Layers:
	-	`sha256:e40985eb60787ad8aa5df064ec78906a87d592650d3cb7bd4e4d35fef41aeff0`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c276c637f8dbb8e68f06bb64f124d7e82ae5dde2c17bdf3085ab2d27b05e7a9`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:07e1a111cf7db99a4e8da7b30d05dbe05ce582c3e60c621b8dddf3f1d7fb85e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6958c992473c935b57387a0074e6ff9d5c8d8f25f4000cddbad2a4da7337e949`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:35:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:35:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:35:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7684c225310a7186686d90420bff2204e00d1da54ed64629dd5c3e06bedb11`  
		Last Modified: Tue, 13 Jan 2026 02:35:51 GMT  
		Size: 10.1 MB (10073782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6a425fa7aac586d22520ac0e48d6b900e2d7650c99f069fc369de3faad44f9`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b744125fe7f349b2dca35775678901252ef655baabbabf00e0581e5db35f4d0`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ec7811cc5fffb4d35b28f25ffe926c9d946a0287fc98559205e5ee8aad5d7`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 91.0 KB (91029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4f8ea8e151623c0726e2b1d500eadf97f81d9185d53345068d8a5310be376250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d3f945473a1378792d3153caab159049530a28c11f85defc0c8257070900d`

```dockerfile
```

-	Layers:
	-	`sha256:9036dfeefff31d7ac9375bcbcaa30955c898c61f27f40e393540a89d7cae685f`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 3.6 MB (3615595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69148b190dc58c8fbc910cf582b627d0d34da0969ae22d538922ec69e3487bd`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:1c485a7ec0ef76060f194fc63ade360521156d06352d21ba7e55c5678263b4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61359266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3405de0f825036ef97723d3ffeaf81ee462ad3c0bdef73f83566138b62c01017`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:11:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:11:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f9978ca299f165c197622edd759b69b3cf32899ccbb3854492744e5131a0d`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 10.5 MB (10466724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdffb0278580783eda7f81d2d70ad20bf0b440ee7b7590e521dc0aa44d3eff2`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d29a632dda1a11016736a63fec3296211533322f93651cd5c2f440ed3ea8f04`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f369e3c2508700e6055a1900113ae937b42ec7d8683d5ef29fc8b48f14b44a`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 90.8 KB (90766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1147e07d7974976c8157d340cbacd2696887d306fdb7a9521442243eee0bd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93d8778ceb78ab3c09d834438ad8647adc746cb80d84fc2b182f923c0d074b0`

```dockerfile
```

-	Layers:
	-	`sha256:a32e0b1b72a70a565da4eddb3e9eee98754724c4b9777ad9defe87db52ffbf4e`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 3.6 MB (3612016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd6ffeb7dffa3512f65e180c61eb1ffa3c36f0545d4818f3ec30607974a2b26`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:4bf6259209bc214c61d034c1dc11a5f99f24c56694fc40cebf1fa4e991e82640
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
$ docker pull neurodebian@sha256:bfe6f18aa6a74c90c1bef54a8ecbfd1554d462da56f4431077902cee7e35743f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59679073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734174826d480fd0ca4221a27524fe98e871a54a19c068307ec6b8d151189d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f763d27f0cca3eca63d032df25da1781edc10ad21bb6ec6472a87765b5d494`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 10.3 MB (10292413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2193d3bb29390a43b5fe3cf6ef36f5d049269591f33a3f65f1c3ebf33ea628`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f82edf0cab6319880f6003cb047a9679b2b534d136feeba495550f279df6cb9`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae03b3a868a98138feda4a04a1f015e865a3599f8231275cde4e2d3ab18157`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 90.4 KB (90354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f2df40ce739fcaf54c09cdf8f844f97b7b89ddd3a009cf66056798e7a816d`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fbf95673c18f9bfa0a30481eb45b538fec3995c608702a1c1d90e08da42446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9f83b2f6643450c6e9f512971c820c8345c704dcd2e8cc7a8756a02e736f86`

```dockerfile
```

-	Layers:
	-	`sha256:6c76910ec532300ba0ac33261e0fa300df86a2a7236c44063bcf717e3999b372`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48dd7f90c47288d683499a84f5abe7001a411496c218e1bd8e77b25b0888176`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3e8b1aee676dde93acde9fac58fa3ab60f76be22359149b15a158f66571828b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59816200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16820c26affbce98ddae6fa99af774b35f36fa48f83f0175f7cc280513d9df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:36:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:36:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:36:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ed602a8d82e45752b42458f6c6cf735a34652ba4dde594e695631d834d59b`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 10.1 MB (10073712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8fc00822d28ca96ab3b0a281c9f30f594ddc2a1097c1d118b5a8d327ade838`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8209c0e736639a6f4be8dbb64c8eebcf8f0660d2bfc6801b3c25864d8deee2`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850c1d0537909467bd63adc7a9f8b6c380009301140d89edfcf9e56b6a682db`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 91.1 KB (91057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f820caede12aa6a0a73d704ba9b536c2a46a1c60230cf73b319c81ab1626f30`  
		Last Modified: Tue, 13 Jan 2026 02:36:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9e27486911deee56ba88782a368ea64fb2d4cfebf43f5046a845fd248bd042d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ee1f59febf6225a8b47ae664b8af048babe29a052e8afed5aacf201038bfa7`

```dockerfile
```

-	Layers:
	-	`sha256:f6eed23b2bfe38aa7cbef27424d9b0bedeef111763c3f9036af89d8ad36602c2`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 3.6 MB (3615635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df7281df837c359d65967773d79bc4901995aad5084db01a47562adb7c7d61c`  
		Last Modified: Tue, 13 Jan 2026 02:36:36 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:0e960ee0faa42f6bdd57961fff7557121bcaf8613b82e9b199d40d7a0261d96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61359689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571fe39bf716fc3e4014c560ab9d7be66fbb4dc330c7f227e15b9de763fbdf3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:12:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:12:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6161421471c9fb8d6e355616caf09b7087ac27ca53984bcd4134a0b0d7e111`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 10.5 MB (10466725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ebcc0e9e4361a538531fdba9070f9175a771b5bb299631b4e6ba78b8981ae3`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895adfd9029fe52f402919d58a03065389e5be8bff8acbf6465d5a18b525fef2`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7e6cefa33611a70c52fbfc73b63e42b2cdfc1fba6226f458dc3f5c739c142`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 90.7 KB (90740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3130aa08749bed8751f83a3a79d2ab7115ab45e908a1b0fffbdd9f80014cee1`  
		Last Modified: Tue, 13 Jan 2026 02:12:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e78e25dbca6377a9c55bca652f94e0e9be3780e215df940fb294f1d5d86968c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f5b3a6f545f0eba153876fc40fb4cce27fea22fc5fc61617969ef489152f6c`

```dockerfile
```

-	Layers:
	-	`sha256:847768114c721eaa57ed7d191df816ead0fde24426576323ca0caead4f71653a`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34278bc983bca66a2b8695d2725d6c0031354a486b9d39d322df70ee7d8ffc6`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
