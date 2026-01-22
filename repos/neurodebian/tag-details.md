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
$ docker pull neurodebian@sha256:50378acdd71781752e7024676a8bd328382efcfdfd93b6b5c6a62ee4121d9b38
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
$ docker pull neurodebian@sha256:07b453c92cf64ff48e660dd4618cdb5d70b3731bacb8d66e1d8c82c3118846f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2175dda30d850351a8e7c6dcc6a7e321f1f1a792e0a9984968fdf5f6bc26d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:30:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:30:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:30:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:30:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e627397f0fd5d6ba6dc03a13cdb205b2250c665910adbb60908d94813855ed5`  
		Last Modified: Tue, 13 Jan 2026 02:31:10 GMT  
		Size: 11.3 MB (11273362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f47af5f478c211e4a8db978b66053d892e42844fbc976ff37bf72419cc3d75e`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211023c1e941ddaa629f23af6b7c6096fa82f8009a3cb6d29440097cbbd881dd`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316013a6629ad2d6b021e7d8b44572a86dba4a10a499a15c30e5364945a35d74`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
		Size: 93.4 KB (93419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a76145fec1c345e159dd624403d49f620294a155772313dda1e70ee8720c1301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd924562edf0dbe314e41f14c3e17d3c90eced47af97d807df05d0a2841f5499`

```dockerfile
```

-	Layers:
	-	`sha256:2a89848c7cf3c7209079b048fadd0ea9311760fe46f7743c17c7a288e7e1b34b`  
		Last Modified: Tue, 13 Jan 2026 05:07:40 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df5bc6e443be9b2df1e1fbb9dd364ae7ece7e2a5d4f06ba9325617ba7c049c6`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5bac5984f021a1cb1ca749e027c45de7e53293b1625c4988634a4daa8acc9c`  
		Last Modified: Tue, 13 Jan 2026 02:34:51 GMT  
		Size: 11.3 MB (11252918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dc8f152c1cf266e173daf7a4a919546ee4a9897b2895bb2832bd1f63404ebc`  
		Last Modified: Tue, 13 Jan 2026 02:34:50 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c75f7dce09f41ce9bb54cfdcf8fc08fcd6a07d50774a65eb285da7fcd95322`  
		Last Modified: Tue, 13 Jan 2026 02:34:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3504a75e5c40c7856f2d2967e8709ddc3ace746bdc156afbbf077d0ccf63396d`  
		Last Modified: Tue, 13 Jan 2026 02:34:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:07:52 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a556fc2754d9f044d1662e4d79eac9e4915ce45406c40cf4e34e0b2b98dd0626`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 11.7 MB (11693011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9cb7a9c880a28c145c0be772f574008d4916e91293035f33747c3ddb4f2d68`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167d0a94399112121b938a46fdcecfced399b318f44230eee634ec27d131632e`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331905edb01f14a56fae50e349444847e3bec8fb9dad97125063c168acdf007`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
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
$ docker pull neurodebian@sha256:d459313dbf8f242095f6799b3d08a48d4fa198ca6ab156afa98b321581f4b4be
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
$ docker pull neurodebian@sha256:9e25a18b8687b88181786cfaa3df892f3ef84bad424fa3b0b47ea46cc7974706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7541202e00f508ada8da0eb293554e9715e6696fefa0b7a459cb7ab2ad7a6c0d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:31:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:31:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:31:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:31:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:31:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a380485364df6e63b13402a903b34109d5097c83c5e6202702b77ededcf0007`  
		Last Modified: Tue, 13 Jan 2026 02:31:44 GMT  
		Size: 11.3 MB (11273398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87cc627bbee9f85f59ce85ad8b6c9bb38a86d270fb0c689361b52a3300a6845`  
		Last Modified: Tue, 13 Jan 2026 02:31:44 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287937d4284b4c7a671b9a6adfb3d23f42e046275717a029afcbaa4350078163`  
		Last Modified: Tue, 13 Jan 2026 02:31:44 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f415e37a6e21f7f0a4498e40eaad2baf1a18230ce45da1d5916c4a49ca5e1e`  
		Last Modified: Tue, 13 Jan 2026 02:31:50 GMT  
		Size: 93.4 KB (93421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d3895aaca248c03b1834cd018d5f88b1397ac9973f1d257beef6ee2bafa5d6`  
		Last Modified: Tue, 13 Jan 2026 02:31:45 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a58c7bc25a43d3ebeee6033bed58ac7eb9dc4f1b61fd3ca3e2a0d30c934bc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662deddc5385803c285c955a1ddd5e525718e26e97079849fba302a3416831ed`

```dockerfile
```

-	Layers:
	-	`sha256:0d4f9639a8725ad7defd4b4824e9b637cbb8b6d68a8f8e06b3e31b562adf658d`  
		Last Modified: Tue, 13 Jan 2026 05:07:51 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00d8dc7be10eaa89858f96552bda58bff01d756e62ab8999a47eb8af56a67d0`  
		Last Modified: Tue, 13 Jan 2026 02:31:44 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:07:57 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ceab790878277f24c39bdb6887b7894b1836783e8bde9c2ef40ab4f7ae6a69`  
		Last Modified: Tue, 13 Jan 2026 05:07:58 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997c347d332a2c61c0fc360ad6eb7c79572de56f76687ff994021f55d5be5509`  
		Last Modified: Tue, 13 Jan 2026 02:10:06 GMT  
		Size: 11.7 MB (11692891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c32144be38bc3cdd35d34b179a53b857bd09030521b64e3b2ade8cfbe04682`  
		Last Modified: Tue, 13 Jan 2026 02:10:11 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b31d31d15813b4a718555d1d4e2460f1942473a1f45559c81acc8d3fa2e639`  
		Last Modified: Tue, 13 Jan 2026 02:10:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941714f5865663330ec0e001ad63079040334233d7b79e405bbcaa371ebdfc91`  
		Last Modified: Tue, 13 Jan 2026 02:10:05 GMT  
		Size: 93.4 KB (93411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83358d0a123b83f0bb86b0baa7411a9619ac366e0c8d8a761413fb6d2c44bb3`  
		Last Modified: Tue, 13 Jan 2026 02:10:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:03 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd72de5be76ee258fd7bc91d339ad00dd77909b399889485157419880d2263b6`  
		Last Modified: Tue, 13 Jan 2026 05:08:39 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:1d44c2db080f9108728a50380ca07654a90a1434f2c5c318eac1727162358b9f
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
$ docker pull neurodebian@sha256:02ea9a776547501550df356a94602114da53e5d74c0d920c53eb5ce81f418625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd9b4ff42af0ae0c5856fc44b09a6413aaefca1fa9a5e1c8ba4da3a5df13824`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:29:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:29:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:29:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c452d2d759110d65f3c976abd4d5e6d76ed19fe9c50ef329abca12452bf6e`  
		Last Modified: Tue, 13 Jan 2026 02:29:40 GMT  
		Size: 11.1 MB (11105041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187e9c7cdfc2b7e6b917de9ba5cf39afdb080e9b78da403c11de1bd80de7e1c`  
		Last Modified: Tue, 13 Jan 2026 02:29:45 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bc3d927b511e66959acf04eedab9f4807a4c33a5da9ba48a944e65e8fb38d6`  
		Last Modified: Tue, 13 Jan 2026 02:29:45 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64881b8183c10bfac8be8293d5d4dbda32ff69a2f0efab95998befac450b1954`  
		Last Modified: Tue, 13 Jan 2026 02:29:39 GMT  
		Size: 101.4 KB (101360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56c3fc171c915be5d66e35763f837d88af6c103774e55b6e4d343e70019a9f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6a3f8c47f2b58ac893dcfe3be942bfb66228c9d0cb78da8ffc1f411ead86e7`

```dockerfile
```

-	Layers:
	-	`sha256:a73edb5d7647df0129e383c8e666ee2f0e87a4543ae45c02a18a02f4ee4682fa`  
		Last Modified: Tue, 13 Jan 2026 05:08:03 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c85c9e55df51cf8c9a71e2ba0d3abb4ee5a1a8ac3cff18efd8b8c5d214963e9`  
		Last Modified: Tue, 13 Jan 2026 02:29:39 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:34:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e5c12b682c631aed701dddac390de29596adf806c67edb4e6de8407aa3da66`  
		Last Modified: Tue, 13 Jan 2026 02:34:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:07:54 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:07:53 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:15 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed007e1dfa4dbba980b0fdb57d1753b165042c471883300a8335a420b0902907`  
		Last Modified: Tue, 13 Jan 2026 05:08:16 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:8441c97a8e198199f07e5a76d645e70806fff1908f494ff3ddec0d444f7ebe52
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
$ docker pull neurodebian@sha256:43852c13486094023492093d1debf80eb35c72d63a9ece7e046323c60a5e227d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557567cb0aa131beb5a5004ca576ca408d37ff2ac4aa19205bf4b5b2c0db17d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:29:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:29:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:29:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60469e509d0db0a8b229a64c66febb355a8cf43de76e0ce7b698340166607f1e`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 11.1 MB (11105087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d9c9f86602982491d439e62a677afb463694c0b1bc57e50d08347d6ef88e3a`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5043a9fff3300da9bb6e22abdfda0cfa3de5a76ed7c68608348c68b7c634101`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2364ed7d3cbbdc21509804a526b9d7357b52c813e5a0f97fdd14aa5f803f30f`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 101.4 KB (101367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183f5f0fd07e138f2d622e5e46a79e3681174f26740a24f3dcc6ba9b9c9c6ea1`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6f6c0ff5acbdeb75814a080ef01605770da928414eaa93d21149e8d166889fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660955ade71b3e4a77be848bf34643f837a7c771f0b78fb67a80467ea0f3527e`

```dockerfile
```

-	Layers:
	-	`sha256:18ad11d013327db0cfeb37cf2958c48784e34c9161110ebb3cbff0070cb04ea7`  
		Last Modified: Tue, 13 Jan 2026 02:29:52 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3c5af0c09bfdb2cad7723af5a5dc2497ad97bfdd9dcd6c0137b68e30daedc5`  
		Last Modified: Tue, 13 Jan 2026 02:29:52 GMT  
		Size: 16.0 KB (15993 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:34:15 GMT  
		Size: 11.1 MB (11106067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2012f775c3a0b7db8ad8b6a741fce6bf1a3bd9e7285301af6bb8c74aa205a210`  
		Last Modified: Tue, 13 Jan 2026 02:34:14 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ebf6dae5f8f124e7deca8a99d38275f3c415952230053da6203eada6d23fb4`  
		Last Modified: Tue, 13 Jan 2026 02:34:14 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198ebede9dec6dff5f729071cee117718742f091332b36e1a24dc261bb2f4460`  
		Last Modified: Tue, 13 Jan 2026 02:34:14 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:09:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:03 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de584fcc7e6273fc33f29b39b5ea37d0141365526c22b1438baebc0dfcc34719`  
		Last Modified: Tue, 13 Jan 2026 05:09:04 GMT  
		Size: 16.0 KB (15963 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:242ac2f0e752a3fa7a584047c08e28d832a04c5a40a17e4c69d26bd567402769
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
$ docker pull neurodebian@sha256:9f2cb282ff890f651cc8008a6f1322bc8bf837e45160babfca8ad4352a1306da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60561989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19e777a68b926864e3f4b314232ad008444addba9776e875f2c5970ada1b6cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:33:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:743b991b49b557d24658aa3fd7faa6c90234b4433dabd04078e1e4904b8e483b`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 48.8 MB (48836497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feaa04165ca0cd6010b515b453a1bf9f7a4711e3a08ed8ece5c9543bef1f6ec`  
		Last Modified: Tue, 13 Jan 2026 02:34:17 GMT  
		Size: 11.6 MB (11632219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43963a84add649e811aa4f38c6fb2ec2cdb5904fa655a5eae05ec726ab8e7d4`  
		Last Modified: Tue, 13 Jan 2026 02:34:09 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbe6ea98b303791a0937b0dff6387400d847fcca0018908eed03d6285560f44`  
		Last Modified: Tue, 13 Jan 2026 02:34:09 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08972a25fb6dd26ec80ec4b858db54de047c63f20db5db4ecbc991a6043023f2`  
		Last Modified: Tue, 13 Jan 2026 02:34:16 GMT  
		Size: 90.4 KB (90368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1607ddf77ce1b14227bdfa821a39ac52062ac4e8906c8eaf26e5cfdeaf009d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a5e5fded2b480df07bd87a5b6a8f53190990a926ad6efe1c153ed84f7068a0`

```dockerfile
```

-	Layers:
	-	`sha256:95ccb7119fcc93e995601230e06931d20f6b09ba6d6a8e3fa004d4623604cf6a`  
		Last Modified: Tue, 13 Jan 2026 05:08:34 GMT  
		Size: 3.6 MB (3592480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b0db80dc0ed008545f1dbf219d476c3a90c30aa23037b1eaba5e87ef155ccf2`  
		Last Modified: Tue, 13 Jan 2026 02:34:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:37:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:13:13 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f53ad6cf16dbd5f68bc9d9322dbb7cf4cdc0b91cd81817c248463451194c32f`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f6d2e23e75837861e27bcb5f7a138da1aafb97f4d81476f5435b4f15a01e0`  
		Last Modified: Tue, 13 Jan 2026 02:13:13 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:46 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:d1a3754b493305398f325ea3a6592d5dda3b5504d2c56e650caedb603b7d0066
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
$ docker pull neurodebian@sha256:3a9843542adba90737d65b1d0cbff2e65ebc3cc6115b888a9f62bca64c61c078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60562386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2a3b5c2fbbe39e2c2b707c7f008b15b58b7e36ba37cecf4be273c9037508dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:34:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:34:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:743b991b49b557d24658aa3fd7faa6c90234b4433dabd04078e1e4904b8e483b`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 48.8 MB (48836497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55492b41b4a9f1fb29f9a699f2bdb4ab3567a04da18e53990fac8ee9a5067fe`  
		Last Modified: Tue, 13 Jan 2026 02:34:37 GMT  
		Size: 11.6 MB (11632195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71003c85ea10f480bbb3572783de51413eda378dc9d0c08c05aec0a84be02f7a`  
		Last Modified: Tue, 13 Jan 2026 02:34:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d42b2d1ed754afaf35635f0d655e1ef533470f8e9407b3bde73984bf77ecb`  
		Last Modified: Tue, 13 Jan 2026 02:34:42 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3302faea5aae0cc4ae334839e449b071eedf8fe2027cc204e87ec6b6875d53a4`  
		Last Modified: Tue, 13 Jan 2026 02:34:42 GMT  
		Size: 90.3 KB (90346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db05db04376f8dcb0185846c487862ff8f945ce3bcb30a123a22c98fb07b7da`  
		Last Modified: Tue, 13 Jan 2026 02:34:42 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8867b289e3c3d47d9a3a1170f86568a18de42083acc96a6f44a2e354088311c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406a671b2eb198d3e70ec2cc3d0d6f82f86b98ed1472463bba0fa84492e0cf55`

```dockerfile
```

-	Layers:
	-	`sha256:481b24813c55a95c43ed835dbc9612dbfe3043d76ed1423bb19f49560baeb7a0`  
		Last Modified: Tue, 13 Jan 2026 02:34:37 GMT  
		Size: 3.6 MB (3592516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e0beae277cf0606ac0bd78a66fda9481dc7a527009e3542e06b59031c7ff6ae`  
		Last Modified: Tue, 13 Jan 2026 02:34:36 GMT  
		Size: 16.0 KB (15957 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:37:27 GMT  
		Size: 11.3 MB (11284159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b04b69ed7b0dc312198ad357b2412c074128f959f7293aed12772b8024660ef`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ff9f4d2e3110d267b69e9306e4a2c646baa86f11542e5890a5a610a3d81b20`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624da5a767e899231c0f32b59b33cb218d6cd91826a2f6983521bf73ce77dca`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:52 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:14:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:58 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:32 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:32 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:08:47 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07dbb8c42e97f3cbb99e13a0cce5eaeb2908125d20a39eb7a012208555bb6be0`  
		Last Modified: Fri, 16 Jan 2026 02:08:48 GMT  
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
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a4ea43c440ed4c5c6940006aeb234cf69c04ad0392d10b84fd9766e4a34f8`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 3.6 MB (3602633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae0723c728afe1d94014082337ee6c2c149eac4aa6f8373a264ae6ef9d99e8f`  
		Last Modified: Thu, 15 Jan 2026 22:37:02 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7101abc79e23d3f25054e865a814a95478cc4e41c4b4ccbee0cc361e535cc37d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c3cd39c7b72b92ef079ad69cd3630b8af83c92b6ffe3230be891653be676b`  
		Last Modified: Thu, 15 Jan 2026 22:37:03 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:08:52 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d01ecd9429deb21559e16c32c9f4e387c8f8033115397f07ceae09f9725024d`  
		Last Modified: Fri, 16 Jan 2026 02:08:53 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:40 GMT  
		Size: 3.6 MB (3624349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903068be00a686117d5126046cccd885353091e8878694caf04fcdb458f28010`  
		Last Modified: Thu, 15 Jan 2026 22:34:39 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:39 GMT  
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
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:37:20 GMT  
		Size: 110.5 KB (110485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ade6120433a2a5a27b1949103586f6bea98efdfbdcde54a84ec40fc4703e39`  
		Last Modified: Thu, 15 Jan 2026 22:37:20 GMT  
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
$ docker pull neurodebian@sha256:47b754108f2c8ddefe5d13697f941d76f494c994d47b20499fc5fe223716d447
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
$ docker pull neurodebian@sha256:22e37f2603d1ed32821a0cad6512380fa6fabfd53b42aaaa9c5e19c73d718cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9f574a764af442ccf4f0d76ada28a5f05f3e50f49afa75eccb8787883c149`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:32:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:32:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:32:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:32:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc68761723983fb9c260913503a6009ba5a2f08483a876479840bb380f2427da`  
		Last Modified: Tue, 13 Jan 2026 02:32:38 GMT  
		Size: 10.3 MB (10292369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2967f103d4ce45b19792a2ecbff3632e03fea3edc3be61f563e7e43c118f700d`  
		Last Modified: Tue, 13 Jan 2026 02:32:38 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5c85078c373f5db9b4ecc974fafd99fb82e5714a93447ad8b6776458449a4c`  
		Last Modified: Tue, 13 Jan 2026 02:32:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e2e17fc67e8d7c08da7a7f77f3f7db097444f2ffa6707ed5ebc5601fef6a19`  
		Last Modified: Tue, 13 Jan 2026 02:32:43 GMT  
		Size: 90.4 KB (90377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbfc8e24d44e4c71f66017bcedf813c4a42d2b360c8c787a5e10d2f2565e273b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4551d97a664bb0fcd7504cf5e0c293b1e5c69a721fbf18673d1e31805110b45e`

```dockerfile
```

-	Layers:
	-	`sha256:1fbd881cc4c6cabc9c47af353e71736e06885a3d4b903a46fa14e91e66772841`  
		Last Modified: Tue, 13 Jan 2026 05:08:57 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f00b2e3933218e49feba543ae9da5f9a99e694fa143a0b369f3b1dc6d0d0fbd`  
		Last Modified: Tue, 13 Jan 2026 02:32:38 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7684c225310a7186686d90420bff2204e00d1da54ed64629dd5c3e06bedb11`  
		Last Modified: Tue, 13 Jan 2026 02:35:57 GMT  
		Size: 10.1 MB (10073782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6a425fa7aac586d22520ac0e48d6b900e2d7650c99f069fc369de3faad44f9`  
		Last Modified: Tue, 13 Jan 2026 02:35:56 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:03 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f9978ca299f165c197622edd759b69b3cf32899ccbb3854492744e5131a0d`  
		Last Modified: Tue, 13 Jan 2026 02:11:38 GMT  
		Size: 10.5 MB (10466724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdffb0278580783eda7f81d2d70ad20bf0b440ee7b7590e521dc0aa44d3eff2`  
		Last Modified: Tue, 13 Jan 2026 02:11:38 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d29a632dda1a11016736a63fec3296211533322f93651cd5c2f440ed3ea8f04`  
		Last Modified: Tue, 13 Jan 2026 02:11:46 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f369e3c2508700e6055a1900113ae937b42ec7d8683d5ef29fc8b48f14b44a`  
		Last Modified: Tue, 13 Jan 2026 02:11:38 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:09 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:64535a2da97c53d7fa7f0f0defaa69da44c5052f8a631c84398d72611d48587b
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
$ docker pull neurodebian@sha256:92487a8aebe98c1c9d388be4905fe1bf1527c1e8c0d4a4cf4030b6fa82f2104b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60567318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc202592d736a492ae1c4a4ba82b22f07e9fea13e8052395c5165dd75760d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:34:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:34:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2184fb6462644b6acf50283df065d3d00ff827c80b1fe7de520944b5c1333b4`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48841950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8a6faf80ecfccce4104b9e268fbed126849120ca36bea68c5394d5c76d9e0b`  
		Last Modified: Tue, 13 Jan 2026 02:35:06 GMT  
		Size: 11.6 MB (11632231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466355a210dbc03ea43136ff8fdd8a5ae5afcf0615e60d30047cfd37efbe4b21`  
		Last Modified: Tue, 13 Jan 2026 02:35:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1779d0fa4495e3d2a0a0b68128d9ef9e82565361d68729bbb5a5885aace097`  
		Last Modified: Tue, 13 Jan 2026 02:35:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f8660c0e79c11d5bbbfff390099d07ced013275c9b7979904bf16339975a7`  
		Last Modified: Tue, 13 Jan 2026 02:35:12 GMT  
		Size: 90.2 KB (90232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:da1774bcfc71603d4d1872cc31f042122eba5b6ba59dc1b50aa749fabb984990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c431dfccbdcb32a1a4cfb4e9d18507058f7eed38cf6ed1103e2e8a03aa0766e6`

```dockerfile
```

-	Layers:
	-	`sha256:b8b556cb0c2448de7f6d828c1c6ee56d88287cefa3f5b4eec41c4c392dd19359`  
		Last Modified: Tue, 13 Jan 2026 05:09:10 GMT  
		Size: 3.6 MB (3593193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74376fbea860e23a42f23513b84b3a49d6803d2a36b913b516096b3fe541aa7`  
		Last Modified: Tue, 13 Jan 2026 02:35:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:38:26 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:06 GMT  
		Size: 11.8 MB (11777889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b62c15fbf7ad5a88504652ccc590c41168dd750ad796ee00cb146201e51d41a`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572d1ccf01b56f7a38834164db204119048dc7f9118850e151ee844646faa2d7`  
		Last Modified: Tue, 13 Jan 2026 02:15:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:23 GMT  
		Size: 3.6 MB (3591151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8768990e2a7177e584c19848ea859a7128c68a9856c85d9b11594e75f37bada0`  
		Last Modified: Tue, 13 Jan 2026 05:09:23 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:0b630c00c5070bf23631871f269b8293c6027e2f30a895ea73746f2ed9b4b936
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
$ docker pull neurodebian@sha256:883eb0b954b83d7480c8a3678cbc8ae5d0acb09156daa78de63f88d0c7be2215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60567727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f103c35caa70fa2e598bbf9b8e5d389f44a144527d5ae15a2ec8e3bbc2b1be6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:35:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:35:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:35:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b2184fb6462644b6acf50283df065d3d00ff827c80b1fe7de520944b5c1333b4`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48841950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa19ca8127c7609765102d825c06a722be6aa2a704ad10ba538de570a72b6c7e`  
		Last Modified: Tue, 13 Jan 2026 02:35:54 GMT  
		Size: 11.6 MB (11632256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78ad8f8ce96a8a0161687f8d72d7ce31047f9e79c01cc6d465e0f2520459fd7`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2174da5053e56df9335e9b85f225136e8dc9397d0594a3c1fd6850ee2f8bbb7`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220bbb1b36941bb7f746471dbd6af8c3dd4662bade8d99d05f24f13912b51c8f`  
		Last Modified: Tue, 13 Jan 2026 02:35:53 GMT  
		Size: 90.2 KB (90201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181a2da67b8e3991dcb1f417001cfa2694d49106dcc0c91c375c094c1af0bc27`  
		Last Modified: Tue, 13 Jan 2026 02:35:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ceb7efd5cc791e93223c656e87687a09bb780e06359f7b203d71b3883af59a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4898b9290d6b9bc8ce40cdde772e085e81442a757a7a24bab3635b2cd8aa9744`

```dockerfile
```

-	Layers:
	-	`sha256:86e4d90f97512714d41888dd2c03de4c8d3dfe00af68c592810d378d4c23225d`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
		Size: 3.6 MB (3593229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25234269e6f4b00858be9f4f0c989c43f66a8e3594d8bc59f42bf51e559e473c`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:38:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d8c2ee79391cf1b2076de818d699484239f70dab0332479d0eb6876eb76d24`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 90.9 KB (90868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7407bf616dbd5929f5d38b6b8161c64ea318bef988d826e2db12e1c7bdfa6b3b`  
		Last Modified: Tue, 13 Jan 2026 02:38:58 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:43 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:42 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:40 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:1d44c2db080f9108728a50380ca07654a90a1434f2c5c318eac1727162358b9f
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
$ docker pull neurodebian@sha256:02ea9a776547501550df356a94602114da53e5d74c0d920c53eb5ce81f418625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd9b4ff42af0ae0c5856fc44b09a6413aaefca1fa9a5e1c8ba4da3a5df13824`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:29:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:29:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:29:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6c452d2d759110d65f3c976abd4d5e6d76ed19fe9c50ef329abca12452bf6e`  
		Last Modified: Tue, 13 Jan 2026 02:29:40 GMT  
		Size: 11.1 MB (11105041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187e9c7cdfc2b7e6b917de9ba5cf39afdb080e9b78da403c11de1bd80de7e1c`  
		Last Modified: Tue, 13 Jan 2026 02:29:45 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bc3d927b511e66959acf04eedab9f4807a4c33a5da9ba48a944e65e8fb38d6`  
		Last Modified: Tue, 13 Jan 2026 02:29:45 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64881b8183c10bfac8be8293d5d4dbda32ff69a2f0efab95998befac450b1954`  
		Last Modified: Tue, 13 Jan 2026 02:29:39 GMT  
		Size: 101.4 KB (101360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56c3fc171c915be5d66e35763f837d88af6c103774e55b6e4d343e70019a9f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6a3f8c47f2b58ac893dcfe3be942bfb66228c9d0cb78da8ffc1f411ead86e7`

```dockerfile
```

-	Layers:
	-	`sha256:a73edb5d7647df0129e383c8e666ee2f0e87a4543ae45c02a18a02f4ee4682fa`  
		Last Modified: Tue, 13 Jan 2026 05:08:03 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c85c9e55df51cf8c9a71e2ba0d3abb4ee5a1a8ac3cff18efd8b8c5d214963e9`  
		Last Modified: Tue, 13 Jan 2026 02:29:39 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:34:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e5c12b682c631aed701dddac390de29596adf806c67edb4e6de8407aa3da66`  
		Last Modified: Tue, 13 Jan 2026 02:34:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:07:54 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:07:53 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:15 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed007e1dfa4dbba980b0fdb57d1753b165042c471883300a8335a420b0902907`  
		Last Modified: Tue, 13 Jan 2026 05:08:16 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:8441c97a8e198199f07e5a76d645e70806fff1908f494ff3ddec0d444f7ebe52
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
$ docker pull neurodebian@sha256:43852c13486094023492093d1debf80eb35c72d63a9ece7e046323c60a5e227d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557567cb0aa131beb5a5004ca576ca408d37ff2ac4aa19205bf4b5b2c0db17d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:29:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:29:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:29:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60469e509d0db0a8b229a64c66febb355a8cf43de76e0ce7b698340166607f1e`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 11.1 MB (11105087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d9c9f86602982491d439e62a677afb463694c0b1bc57e50d08347d6ef88e3a`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5043a9fff3300da9bb6e22abdfda0cfa3de5a76ed7c68608348c68b7c634101`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2364ed7d3cbbdc21509804a526b9d7357b52c813e5a0f97fdd14aa5f803f30f`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 101.4 KB (101367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183f5f0fd07e138f2d622e5e46a79e3681174f26740a24f3dcc6ba9b9c9c6ea1`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6f6c0ff5acbdeb75814a080ef01605770da928414eaa93d21149e8d166889fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660955ade71b3e4a77be848bf34643f837a7c771f0b78fb67a80467ea0f3527e`

```dockerfile
```

-	Layers:
	-	`sha256:18ad11d013327db0cfeb37cf2958c48784e34c9161110ebb3cbff0070cb04ea7`  
		Last Modified: Tue, 13 Jan 2026 02:29:52 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3c5af0c09bfdb2cad7723af5a5dc2497ad97bfdd9dcd6c0137b68e30daedc5`  
		Last Modified: Tue, 13 Jan 2026 02:29:52 GMT  
		Size: 16.0 KB (15993 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:34:15 GMT  
		Size: 11.1 MB (11106067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2012f775c3a0b7db8ad8b6a741fce6bf1a3bd9e7285301af6bb8c74aa205a210`  
		Last Modified: Tue, 13 Jan 2026 02:34:14 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ebf6dae5f8f124e7deca8a99d38275f3c415952230053da6203eada6d23fb4`  
		Last Modified: Tue, 13 Jan 2026 02:34:14 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198ebede9dec6dff5f729071cee117718742f091332b36e1a24dc261bb2f4460`  
		Last Modified: Tue, 13 Jan 2026 02:34:14 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:09:10 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:03 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de584fcc7e6273fc33f29b39b5ea37d0141365526c22b1438baebc0dfcc34719`  
		Last Modified: Tue, 13 Jan 2026 05:09:04 GMT  
		Size: 16.0 KB (15963 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:50378acdd71781752e7024676a8bd328382efcfdfd93b6b5c6a62ee4121d9b38
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
$ docker pull neurodebian@sha256:07b453c92cf64ff48e660dd4618cdb5d70b3731bacb8d66e1d8c82c3118846f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2175dda30d850351a8e7c6dcc6a7e321f1f1a792e0a9984968fdf5f6bc26d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:30:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:30:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:30:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:30:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e627397f0fd5d6ba6dc03a13cdb205b2250c665910adbb60908d94813855ed5`  
		Last Modified: Tue, 13 Jan 2026 02:31:10 GMT  
		Size: 11.3 MB (11273362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f47af5f478c211e4a8db978b66053d892e42844fbc976ff37bf72419cc3d75e`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211023c1e941ddaa629f23af6b7c6096fa82f8009a3cb6d29440097cbbd881dd`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316013a6629ad2d6b021e7d8b44572a86dba4a10a499a15c30e5364945a35d74`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
		Size: 93.4 KB (93419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a76145fec1c345e159dd624403d49f620294a155772313dda1e70ee8720c1301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd924562edf0dbe314e41f14c3e17d3c90eced47af97d807df05d0a2841f5499`

```dockerfile
```

-	Layers:
	-	`sha256:2a89848c7cf3c7209079b048fadd0ea9311760fe46f7743c17c7a288e7e1b34b`  
		Last Modified: Tue, 13 Jan 2026 05:07:40 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df5bc6e443be9b2df1e1fbb9dd364ae7ece7e2a5d4f06ba9325617ba7c049c6`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5bac5984f021a1cb1ca749e027c45de7e53293b1625c4988634a4daa8acc9c`  
		Last Modified: Tue, 13 Jan 2026 02:34:51 GMT  
		Size: 11.3 MB (11252918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dc8f152c1cf266e173daf7a4a919546ee4a9897b2895bb2832bd1f63404ebc`  
		Last Modified: Tue, 13 Jan 2026 02:34:50 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c75f7dce09f41ce9bb54cfdcf8fc08fcd6a07d50774a65eb285da7fcd95322`  
		Last Modified: Tue, 13 Jan 2026 02:34:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3504a75e5c40c7856f2d2967e8709ddc3ace746bdc156afbbf077d0ccf63396d`  
		Last Modified: Tue, 13 Jan 2026 02:34:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:07:52 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a556fc2754d9f044d1662e4d79eac9e4915ce45406c40cf4e34e0b2b98dd0626`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 11.7 MB (11693011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9cb7a9c880a28c145c0be772f574008d4916e91293035f33747c3ddb4f2d68`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167d0a94399112121b938a46fdcecfced399b318f44230eee634ec27d131632e`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331905edb01f14a56fae50e349444847e3bec8fb9dad97125063c168acdf007`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
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
$ docker pull neurodebian@sha256:d459313dbf8f242095f6799b3d08a48d4fa198ca6ab156afa98b321581f4b4be
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
$ docker pull neurodebian@sha256:9e25a18b8687b88181786cfaa3df892f3ef84bad424fa3b0b47ea46cc7974706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7541202e00f508ada8da0eb293554e9715e6696fefa0b7a459cb7ab2ad7a6c0d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:31:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:31:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:31:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:31:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:31:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a380485364df6e63b13402a903b34109d5097c83c5e6202702b77ededcf0007`  
		Last Modified: Tue, 13 Jan 2026 02:31:44 GMT  
		Size: 11.3 MB (11273398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87cc627bbee9f85f59ce85ad8b6c9bb38a86d270fb0c689361b52a3300a6845`  
		Last Modified: Tue, 13 Jan 2026 02:31:44 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287937d4284b4c7a671b9a6adfb3d23f42e046275717a029afcbaa4350078163`  
		Last Modified: Tue, 13 Jan 2026 02:31:44 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f415e37a6e21f7f0a4498e40eaad2baf1a18230ce45da1d5916c4a49ca5e1e`  
		Last Modified: Tue, 13 Jan 2026 02:31:50 GMT  
		Size: 93.4 KB (93421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d3895aaca248c03b1834cd018d5f88b1397ac9973f1d257beef6ee2bafa5d6`  
		Last Modified: Tue, 13 Jan 2026 02:31:45 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a58c7bc25a43d3ebeee6033bed58ac7eb9dc4f1b61fd3ca3e2a0d30c934bc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662deddc5385803c285c955a1ddd5e525718e26e97079849fba302a3416831ed`

```dockerfile
```

-	Layers:
	-	`sha256:0d4f9639a8725ad7defd4b4824e9b637cbb8b6d68a8f8e06b3e31b562adf658d`  
		Last Modified: Tue, 13 Jan 2026 05:07:51 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00d8dc7be10eaa89858f96552bda58bff01d756e62ab8999a47eb8af56a67d0`  
		Last Modified: Tue, 13 Jan 2026 02:31:44 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:07:57 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ceab790878277f24c39bdb6887b7894b1836783e8bde9c2ef40ab4f7ae6a69`  
		Last Modified: Tue, 13 Jan 2026 05:07:58 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997c347d332a2c61c0fc360ad6eb7c79572de56f76687ff994021f55d5be5509`  
		Last Modified: Tue, 13 Jan 2026 02:10:06 GMT  
		Size: 11.7 MB (11692891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c32144be38bc3cdd35d34b179a53b857bd09030521b64e3b2ade8cfbe04682`  
		Last Modified: Tue, 13 Jan 2026 02:10:11 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b31d31d15813b4a718555d1d4e2460f1942473a1f45559c81acc8d3fa2e639`  
		Last Modified: Tue, 13 Jan 2026 02:10:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941714f5865663330ec0e001ad63079040334233d7b79e405bbcaa371ebdfc91`  
		Last Modified: Tue, 13 Jan 2026 02:10:05 GMT  
		Size: 93.4 KB (93411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83358d0a123b83f0bb86b0baa7411a9619ac366e0c8d8a761413fb6d2c44bb3`  
		Last Modified: Tue, 13 Jan 2026 02:10:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:03 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd72de5be76ee258fd7bc91d339ad00dd77909b399889485157419880d2263b6`  
		Last Modified: Tue, 13 Jan 2026 05:08:39 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:47b754108f2c8ddefe5d13697f941d76f494c994d47b20499fc5fe223716d447
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
$ docker pull neurodebian@sha256:22e37f2603d1ed32821a0cad6512380fa6fabfd53b42aaaa9c5e19c73d718cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9f574a764af442ccf4f0d76ada28a5f05f3e50f49afa75eccb8787883c149`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:32:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:32:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:32:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:32:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc68761723983fb9c260913503a6009ba5a2f08483a876479840bb380f2427da`  
		Last Modified: Tue, 13 Jan 2026 02:32:38 GMT  
		Size: 10.3 MB (10292369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2967f103d4ce45b19792a2ecbff3632e03fea3edc3be61f563e7e43c118f700d`  
		Last Modified: Tue, 13 Jan 2026 02:32:38 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5c85078c373f5db9b4ecc974fafd99fb82e5714a93447ad8b6776458449a4c`  
		Last Modified: Tue, 13 Jan 2026 02:32:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e2e17fc67e8d7c08da7a7f77f3f7db097444f2ffa6707ed5ebc5601fef6a19`  
		Last Modified: Tue, 13 Jan 2026 02:32:43 GMT  
		Size: 90.4 KB (90377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbfc8e24d44e4c71f66017bcedf813c4a42d2b360c8c787a5e10d2f2565e273b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4551d97a664bb0fcd7504cf5e0c293b1e5c69a721fbf18673d1e31805110b45e`

```dockerfile
```

-	Layers:
	-	`sha256:1fbd881cc4c6cabc9c47af353e71736e06885a3d4b903a46fa14e91e66772841`  
		Last Modified: Tue, 13 Jan 2026 05:08:57 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f00b2e3933218e49feba543ae9da5f9a99e694fa143a0b369f3b1dc6d0d0fbd`  
		Last Modified: Tue, 13 Jan 2026 02:32:38 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7684c225310a7186686d90420bff2204e00d1da54ed64629dd5c3e06bedb11`  
		Last Modified: Tue, 13 Jan 2026 02:35:57 GMT  
		Size: 10.1 MB (10073782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6a425fa7aac586d22520ac0e48d6b900e2d7650c99f069fc369de3faad44f9`  
		Last Modified: Tue, 13 Jan 2026 02:35:56 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:03 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f9978ca299f165c197622edd759b69b3cf32899ccbb3854492744e5131a0d`  
		Last Modified: Tue, 13 Jan 2026 02:11:38 GMT  
		Size: 10.5 MB (10466724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdffb0278580783eda7f81d2d70ad20bf0b440ee7b7590e521dc0aa44d3eff2`  
		Last Modified: Tue, 13 Jan 2026 02:11:38 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d29a632dda1a11016736a63fec3296211533322f93651cd5c2f440ed3ea8f04`  
		Last Modified: Tue, 13 Jan 2026 02:11:46 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f369e3c2508700e6055a1900113ae937b42ec7d8683d5ef29fc8b48f14b44a`  
		Last Modified: Tue, 13 Jan 2026 02:11:38 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:09 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:b30144b25b4f9eda8cff7e3527ac291ee12ef4085cc006a28765cb84aa420700
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
$ docker pull neurodebian@sha256:a1f3d681375ae9877cb174d624d1c5cbd04a741b1cada66a9dbce8265700d3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ee6736859c305f7a5a63b3b9e54bdb047bf11407b4ec44ead45a2ee482f2e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:33:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:33:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0719b276ab21986970910cd53aa98e1720cae839dc3245e4539f6466de5586`  
		Last Modified: Tue, 13 Jan 2026 02:33:37 GMT  
		Size: 10.3 MB (10292332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4019c5b48e86642c8626c9b3af0135436b974b87db9eb8192ded3d7ef13afe`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc68ef74c45ffbb305959abee61f51b007da4b83b356f90740ea0a7a315015`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f5af02919eace9dd5db853e2f41d073cd35d27d1c0e8b76f95ff2f940f3dd0`  
		Last Modified: Tue, 13 Jan 2026 02:33:35 GMT  
		Size: 90.4 KB (90370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a513dcbfdcdcca80b9eceb62b78bd4af37a8672d7420381d085405a3dab7a`  
		Last Modified: Tue, 13 Jan 2026 02:33:29 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9817b4cc23261bdf6af3b2b878eac1bec5c62dd85db0d7bd7df14a6039a2817e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0565ca92f711426185538e4fc88ae99140917adec4068a1fd1343dcf23797c4a`

```dockerfile
```

-	Layers:
	-	`sha256:3fdaa0bbf6cb71883d44164a4f5068383c9f11b3230e9905be8b678a54d1ff65`  
		Last Modified: Tue, 13 Jan 2026 05:09:45 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc16a4a69d2920022ac713a906e760a6cf6c371075d6ad1f69e3a8198569a3cb`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ed602a8d82e45752b42458f6c6cf735a34652ba4dde594e695631d834d59b`  
		Last Modified: Tue, 13 Jan 2026 02:36:43 GMT  
		Size: 10.1 MB (10073712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8fc00822d28ca96ab3b0a281c9f30f594ddc2a1097c1d118b5a8d327ade838`  
		Last Modified: Tue, 13 Jan 2026 02:36:42 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:36:42 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:56 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34278bc983bca66a2b8695d2725d6c0031354a486b9d39d322df70ee7d8ffc6`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:242ac2f0e752a3fa7a584047c08e28d832a04c5a40a17e4c69d26bd567402769
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
$ docker pull neurodebian@sha256:9f2cb282ff890f651cc8008a6f1322bc8bf837e45160babfca8ad4352a1306da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60561989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19e777a68b926864e3f4b314232ad008444addba9776e875f2c5970ada1b6cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:33:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:743b991b49b557d24658aa3fd7faa6c90234b4433dabd04078e1e4904b8e483b`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 48.8 MB (48836497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feaa04165ca0cd6010b515b453a1bf9f7a4711e3a08ed8ece5c9543bef1f6ec`  
		Last Modified: Tue, 13 Jan 2026 02:34:17 GMT  
		Size: 11.6 MB (11632219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43963a84add649e811aa4f38c6fb2ec2cdb5904fa655a5eae05ec726ab8e7d4`  
		Last Modified: Tue, 13 Jan 2026 02:34:09 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbe6ea98b303791a0937b0dff6387400d847fcca0018908eed03d6285560f44`  
		Last Modified: Tue, 13 Jan 2026 02:34:09 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08972a25fb6dd26ec80ec4b858db54de047c63f20db5db4ecbc991a6043023f2`  
		Last Modified: Tue, 13 Jan 2026 02:34:16 GMT  
		Size: 90.4 KB (90368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1607ddf77ce1b14227bdfa821a39ac52062ac4e8906c8eaf26e5cfdeaf009d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a5e5fded2b480df07bd87a5b6a8f53190990a926ad6efe1c153ed84f7068a0`

```dockerfile
```

-	Layers:
	-	`sha256:95ccb7119fcc93e995601230e06931d20f6b09ba6d6a8e3fa004d4623604cf6a`  
		Last Modified: Tue, 13 Jan 2026 05:08:34 GMT  
		Size: 3.6 MB (3592480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b0db80dc0ed008545f1dbf219d476c3a90c30aa23037b1eaba5e87ef155ccf2`  
		Last Modified: Tue, 13 Jan 2026 02:34:09 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:37:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:13:13 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f53ad6cf16dbd5f68bc9d9322dbb7cf4cdc0b91cd81817c248463451194c32f`  
		Last Modified: Tue, 13 Jan 2026 02:13:07 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f6d2e23e75837861e27bcb5f7a138da1aafb97f4d81476f5435b4f15a01e0`  
		Last Modified: Tue, 13 Jan 2026 02:13:13 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:46 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:d1a3754b493305398f325ea3a6592d5dda3b5504d2c56e650caedb603b7d0066
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
$ docker pull neurodebian@sha256:3a9843542adba90737d65b1d0cbff2e65ebc3cc6115b888a9f62bca64c61c078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60562386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2a3b5c2fbbe39e2c2b707c7f008b15b58b7e36ba37cecf4be273c9037508dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:34:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:34:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:743b991b49b557d24658aa3fd7faa6c90234b4433dabd04078e1e4904b8e483b`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 48.8 MB (48836497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55492b41b4a9f1fb29f9a699f2bdb4ab3567a04da18e53990fac8ee9a5067fe`  
		Last Modified: Tue, 13 Jan 2026 02:34:37 GMT  
		Size: 11.6 MB (11632195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71003c85ea10f480bbb3572783de51413eda378dc9d0c08c05aec0a84be02f7a`  
		Last Modified: Tue, 13 Jan 2026 02:34:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d42b2d1ed754afaf35635f0d655e1ef533470f8e9407b3bde73984bf77ecb`  
		Last Modified: Tue, 13 Jan 2026 02:34:42 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3302faea5aae0cc4ae334839e449b071eedf8fe2027cc204e87ec6b6875d53a4`  
		Last Modified: Tue, 13 Jan 2026 02:34:42 GMT  
		Size: 90.3 KB (90346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db05db04376f8dcb0185846c487862ff8f945ce3bcb30a123a22c98fb07b7da`  
		Last Modified: Tue, 13 Jan 2026 02:34:42 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8867b289e3c3d47d9a3a1170f86568a18de42083acc96a6f44a2e354088311c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406a671b2eb198d3e70ec2cc3d0d6f82f86b98ed1472463bba0fa84492e0cf55`

```dockerfile
```

-	Layers:
	-	`sha256:481b24813c55a95c43ed835dbc9612dbfe3043d76ed1423bb19f49560baeb7a0`  
		Last Modified: Tue, 13 Jan 2026 02:34:37 GMT  
		Size: 3.6 MB (3592516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e0beae277cf0606ac0bd78a66fda9481dc7a527009e3542e06b59031c7ff6ae`  
		Last Modified: Tue, 13 Jan 2026 02:34:36 GMT  
		Size: 16.0 KB (15957 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:37:27 GMT  
		Size: 11.3 MB (11284159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b04b69ed7b0dc312198ad357b2412c074128f959f7293aed12772b8024660ef`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ff9f4d2e3110d267b69e9306e4a2c646baa86f11542e5890a5a610a3d81b20`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624da5a767e899231c0f32b59b33cb218d6cd91826a2f6983521bf73ce77dca`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:52 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:14:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:08:58 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:32 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:32 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:08:47 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07dbb8c42e97f3cbb99e13a0cce5eaeb2908125d20a39eb7a012208555bb6be0`  
		Last Modified: Fri, 16 Jan 2026 02:08:48 GMT  
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
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a4ea43c440ed4c5c6940006aeb234cf69c04ad0392d10b84fd9766e4a34f8`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 3.6 MB (3602633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae0723c728afe1d94014082337ee6c2c149eac4aa6f8373a264ae6ef9d99e8f`  
		Last Modified: Thu, 15 Jan 2026 22:37:02 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7101abc79e23d3f25054e865a814a95478cc4e41c4b4ccbee0cc361e535cc37d`  
		Last Modified: Thu, 15 Jan 2026 22:36:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c3cd39c7b72b92ef079ad69cd3630b8af83c92b6ffe3230be891653be676b`  
		Last Modified: Thu, 15 Jan 2026 22:37:03 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:08:52 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d01ecd9429deb21559e16c32c9f4e387c8f8033115397f07ceae09f9725024d`  
		Last Modified: Fri, 16 Jan 2026 02:08:53 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:40 GMT  
		Size: 3.6 MB (3624349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903068be00a686117d5126046cccd885353091e8878694caf04fcdb458f28010`  
		Last Modified: Thu, 15 Jan 2026 22:34:39 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:34:39 GMT  
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
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:37:20 GMT  
		Size: 110.5 KB (110485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ade6120433a2a5a27b1949103586f6bea98efdfbdcde54a84ec40fc4703e39`  
		Last Modified: Thu, 15 Jan 2026 22:37:20 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febb96c351dc6c0d19a074b7bf0a980146f228694ed515a5e6e4776348b5d83`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 3.6 MB (3563150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baad77fe67014a99e49ccbb36bfa471550dbfe256c0a7997b77cc92db588b238`  
		Last Modified: Thu, 15 Jan 2026 22:35:05 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:09:14 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d4dd02fcbaa60ee0e870849b37cadc44a2fc95004b2b0c366e2b4f9fd44b22`  
		Last Modified: Fri, 16 Jan 2026 02:09:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:37:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7e1041691204d39dc1e2e6b9a0d184d8a90b0de7386c680d0babf4b584849`  
		Last Modified: Thu, 15 Jan 2026 22:37:48 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a548ca73cf3c853fcef8cc5fc4e37b42dcc57abd2ed979e56815d39fb4d2e1d`  
		Last Modified: Thu, 15 Jan 2026 22:35:28 GMT  
		Size: 3.6 MB (3563186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43697b196e8d2c4b0a8ba22dda06c60a2720d7ecbb327195ef4a733a9a9199a8`  
		Last Modified: Thu, 15 Jan 2026 22:35:27 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf22aeb3829fe498fa19c16c5fdb441e50cdd85738b65a2d38355b2322d1bb`  
		Last Modified: Thu, 15 Jan 2026 22:35:27 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:09:23 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2aea097a4bbb9d5bdaded81482eedf9b99f3c5f026ca55b6e403563c587b66`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 3.6 MB (3560842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76004830fcab5147953ec62120e9188a61c12121f2327a2de3b15e88d02b19d`  
		Last Modified: Thu, 15 Jan 2026 22:38:09 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33a41e6ec1c2b8fe89edb69a4ffd926bd25296f84ed1cd3c94a95975d23a25`  
		Last Modified: Thu, 15 Jan 2026 22:38:09 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f32872c3ae902f9b9f8f6512093ee79fa4f3b288d84103139a75f0a04a60e`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 105.1 KB (105142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d33c20ca018680f26d1c2204d39af5752691853971325601cd21bee5c51074`  
		Last Modified: Thu, 15 Jan 2026 22:38:09 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:09:29 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e09ac7a089e43b83ed3c810459f514467750bce8124e594af9e8ae6471226a`  
		Last Modified: Fri, 16 Jan 2026 02:09:29 GMT  
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
		Last Modified: Tue, 02 Dec 2025 13:58:07 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Tue, 23 Dec 2025 18:33:36 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Fri, 12 Dec 2025 18:34:28 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 25 Dec 2025 08:42:10 GMT  
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
		Last Modified: Tue, 02 Dec 2025 14:40:05 GMT  
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
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
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
		Last Modified: Tue, 02 Dec 2025 13:58:07 GMT  
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
		Last Modified: Tue, 02 Dec 2025 14:40:05 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
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
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febb96c351dc6c0d19a074b7bf0a980146f228694ed515a5e6e4776348b5d83`  
		Last Modified: Thu, 15 Jan 2026 22:34:59 GMT  
		Size: 3.6 MB (3563150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baad77fe67014a99e49ccbb36bfa471550dbfe256c0a7997b77cc92db588b238`  
		Last Modified: Thu, 15 Jan 2026 22:35:05 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:09:14 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d4dd02fcbaa60ee0e870849b37cadc44a2fc95004b2b0c366e2b4f9fd44b22`  
		Last Modified: Fri, 16 Jan 2026 02:09:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:37:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7e1041691204d39dc1e2e6b9a0d184d8a90b0de7386c680d0babf4b584849`  
		Last Modified: Thu, 15 Jan 2026 22:37:48 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a548ca73cf3c853fcef8cc5fc4e37b42dcc57abd2ed979e56815d39fb4d2e1d`  
		Last Modified: Thu, 15 Jan 2026 22:35:28 GMT  
		Size: 3.6 MB (3563186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43697b196e8d2c4b0a8ba22dda06c60a2720d7ecbb327195ef4a733a9a9199a8`  
		Last Modified: Thu, 15 Jan 2026 22:35:27 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf22aeb3829fe498fa19c16c5fdb441e50cdd85738b65a2d38355b2322d1bb`  
		Last Modified: Thu, 15 Jan 2026 22:35:27 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:09:23 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2aea097a4bbb9d5bdaded81482eedf9b99f3c5f026ca55b6e403563c587b66`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 3.6 MB (3560842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76004830fcab5147953ec62120e9188a61c12121f2327a2de3b15e88d02b19d`  
		Last Modified: Thu, 15 Jan 2026 22:38:09 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33a41e6ec1c2b8fe89edb69a4ffd926bd25296f84ed1cd3c94a95975d23a25`  
		Last Modified: Thu, 15 Jan 2026 22:38:09 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f32872c3ae902f9b9f8f6512093ee79fa4f3b288d84103139a75f0a04a60e`  
		Last Modified: Thu, 15 Jan 2026 22:38:02 GMT  
		Size: 105.1 KB (105142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d33c20ca018680f26d1c2204d39af5752691853971325601cd21bee5c51074`  
		Last Modified: Thu, 15 Jan 2026 22:38:09 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:09:29 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e09ac7a089e43b83ed3c810459f514467750bce8124e594af9e8ae6471226a`  
		Last Modified: Fri, 16 Jan 2026 02:09:29 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:b30144b25b4f9eda8cff7e3527ac291ee12ef4085cc006a28765cb84aa420700
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
$ docker pull neurodebian@sha256:a1f3d681375ae9877cb174d624d1c5cbd04a741b1cada66a9dbce8265700d3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ee6736859c305f7a5a63b3b9e54bdb047bf11407b4ec44ead45a2ee482f2e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:33:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:33:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0719b276ab21986970910cd53aa98e1720cae839dc3245e4539f6466de5586`  
		Last Modified: Tue, 13 Jan 2026 02:33:37 GMT  
		Size: 10.3 MB (10292332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4019c5b48e86642c8626c9b3af0135436b974b87db9eb8192ded3d7ef13afe`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc68ef74c45ffbb305959abee61f51b007da4b83b356f90740ea0a7a315015`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f5af02919eace9dd5db853e2f41d073cd35d27d1c0e8b76f95ff2f940f3dd0`  
		Last Modified: Tue, 13 Jan 2026 02:33:35 GMT  
		Size: 90.4 KB (90370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a513dcbfdcdcca80b9eceb62b78bd4af37a8672d7420381d085405a3dab7a`  
		Last Modified: Tue, 13 Jan 2026 02:33:29 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9817b4cc23261bdf6af3b2b878eac1bec5c62dd85db0d7bd7df14a6039a2817e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0565ca92f711426185538e4fc88ae99140917adec4068a1fd1343dcf23797c4a`

```dockerfile
```

-	Layers:
	-	`sha256:3fdaa0bbf6cb71883d44164a4f5068383c9f11b3230e9905be8b678a54d1ff65`  
		Last Modified: Tue, 13 Jan 2026 05:09:45 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc16a4a69d2920022ac713a906e760a6cf6c371075d6ad1f69e3a8198569a3cb`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ed602a8d82e45752b42458f6c6cf735a34652ba4dde594e695631d834d59b`  
		Last Modified: Tue, 13 Jan 2026 02:36:43 GMT  
		Size: 10.1 MB (10073712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8fc00822d28ca96ab3b0a281c9f30f594ddc2a1097c1d118b5a8d327ade838`  
		Last Modified: Tue, 13 Jan 2026 02:36:42 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:36:42 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:56 GMT  
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
		Last Modified: Tue, 02 Dec 2025 13:58:07 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Tue, 23 Dec 2025 18:33:36 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Fri, 12 Dec 2025 18:34:28 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 25 Dec 2025 08:42:10 GMT  
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
		Last Modified: Tue, 02 Dec 2025 14:40:05 GMT  
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
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
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
		Last Modified: Tue, 02 Dec 2025 13:58:07 GMT  
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
		Last Modified: Tue, 02 Dec 2025 14:40:05 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
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
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
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
$ docker pull neurodebian@sha256:64535a2da97c53d7fa7f0f0defaa69da44c5052f8a631c84398d72611d48587b
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
$ docker pull neurodebian@sha256:92487a8aebe98c1c9d388be4905fe1bf1527c1e8c0d4a4cf4030b6fa82f2104b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60567318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc202592d736a492ae1c4a4ba82b22f07e9fea13e8052395c5165dd75760d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:34:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:34:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2184fb6462644b6acf50283df065d3d00ff827c80b1fe7de520944b5c1333b4`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48841950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8a6faf80ecfccce4104b9e268fbed126849120ca36bea68c5394d5c76d9e0b`  
		Last Modified: Tue, 13 Jan 2026 02:35:06 GMT  
		Size: 11.6 MB (11632231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466355a210dbc03ea43136ff8fdd8a5ae5afcf0615e60d30047cfd37efbe4b21`  
		Last Modified: Tue, 13 Jan 2026 02:35:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1779d0fa4495e3d2a0a0b68128d9ef9e82565361d68729bbb5a5885aace097`  
		Last Modified: Tue, 13 Jan 2026 02:35:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f8660c0e79c11d5bbbfff390099d07ced013275c9b7979904bf16339975a7`  
		Last Modified: Tue, 13 Jan 2026 02:35:12 GMT  
		Size: 90.2 KB (90232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:da1774bcfc71603d4d1872cc31f042122eba5b6ba59dc1b50aa749fabb984990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c431dfccbdcb32a1a4cfb4e9d18507058f7eed38cf6ed1103e2e8a03aa0766e6`

```dockerfile
```

-	Layers:
	-	`sha256:b8b556cb0c2448de7f6d828c1c6ee56d88287cefa3f5b4eec41c4c392dd19359`  
		Last Modified: Tue, 13 Jan 2026 05:09:10 GMT  
		Size: 3.6 MB (3593193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74376fbea860e23a42f23513b84b3a49d6803d2a36b913b516096b3fe541aa7`  
		Last Modified: Tue, 13 Jan 2026 02:35:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:38:26 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:15 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:06 GMT  
		Size: 11.8 MB (11777889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b62c15fbf7ad5a88504652ccc590c41168dd750ad796ee00cb146201e51d41a`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572d1ccf01b56f7a38834164db204119048dc7f9118850e151ee844646faa2d7`  
		Last Modified: Tue, 13 Jan 2026 02:15:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:23 GMT  
		Size: 3.6 MB (3591151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8768990e2a7177e584c19848ea859a7128c68a9856c85d9b11594e75f37bada0`  
		Last Modified: Tue, 13 Jan 2026 05:09:23 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:0b630c00c5070bf23631871f269b8293c6027e2f30a895ea73746f2ed9b4b936
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
$ docker pull neurodebian@sha256:883eb0b954b83d7480c8a3678cbc8ae5d0acb09156daa78de63f88d0c7be2215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60567727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f103c35caa70fa2e598bbf9b8e5d389f44a144527d5ae15a2ec8e3bbc2b1be6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:35:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:35:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:35:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b2184fb6462644b6acf50283df065d3d00ff827c80b1fe7de520944b5c1333b4`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48841950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa19ca8127c7609765102d825c06a722be6aa2a704ad10ba538de570a72b6c7e`  
		Last Modified: Tue, 13 Jan 2026 02:35:54 GMT  
		Size: 11.6 MB (11632256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78ad8f8ce96a8a0161687f8d72d7ce31047f9e79c01cc6d465e0f2520459fd7`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2174da5053e56df9335e9b85f225136e8dc9397d0594a3c1fd6850ee2f8bbb7`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220bbb1b36941bb7f746471dbd6af8c3dd4662bade8d99d05f24f13912b51c8f`  
		Last Modified: Tue, 13 Jan 2026 02:35:53 GMT  
		Size: 90.2 KB (90201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181a2da67b8e3991dcb1f417001cfa2694d49106dcc0c91c375c094c1af0bc27`  
		Last Modified: Tue, 13 Jan 2026 02:35:49 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ceb7efd5cc791e93223c656e87687a09bb780e06359f7b203d71b3883af59a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4898b9290d6b9bc8ce40cdde772e085e81442a757a7a24bab3635b2cd8aa9744`

```dockerfile
```

-	Layers:
	-	`sha256:86e4d90f97512714d41888dd2c03de4c8d3dfe00af68c592810d378d4c23225d`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
		Size: 3.6 MB (3593229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25234269e6f4b00858be9f4f0c989c43f66a8e3594d8bc59f42bf51e559e473c`  
		Last Modified: Tue, 13 Jan 2026 02:35:48 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:38:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d8c2ee79391cf1b2076de818d699484239f70dab0332479d0eb6876eb76d24`  
		Last Modified: Tue, 13 Jan 2026 02:38:52 GMT  
		Size: 90.9 KB (90868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7407bf616dbd5929f5d38b6b8161c64ea318bef988d826e2db12e1c7bdfa6b3b`  
		Last Modified: Tue, 13 Jan 2026 02:38:58 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:43 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:15:42 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:40 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:47b754108f2c8ddefe5d13697f941d76f494c994d47b20499fc5fe223716d447
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
$ docker pull neurodebian@sha256:22e37f2603d1ed32821a0cad6512380fa6fabfd53b42aaaa9c5e19c73d718cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9f574a764af442ccf4f0d76ada28a5f05f3e50f49afa75eccb8787883c149`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:32:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:32:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:32:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:32:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc68761723983fb9c260913503a6009ba5a2f08483a876479840bb380f2427da`  
		Last Modified: Tue, 13 Jan 2026 02:32:38 GMT  
		Size: 10.3 MB (10292369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2967f103d4ce45b19792a2ecbff3632e03fea3edc3be61f563e7e43c118f700d`  
		Last Modified: Tue, 13 Jan 2026 02:32:38 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5c85078c373f5db9b4ecc974fafd99fb82e5714a93447ad8b6776458449a4c`  
		Last Modified: Tue, 13 Jan 2026 02:32:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e2e17fc67e8d7c08da7a7f77f3f7db097444f2ffa6707ed5ebc5601fef6a19`  
		Last Modified: Tue, 13 Jan 2026 02:32:43 GMT  
		Size: 90.4 KB (90377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbfc8e24d44e4c71f66017bcedf813c4a42d2b360c8c787a5e10d2f2565e273b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4551d97a664bb0fcd7504cf5e0c293b1e5c69a721fbf18673d1e31805110b45e`

```dockerfile
```

-	Layers:
	-	`sha256:1fbd881cc4c6cabc9c47af353e71736e06885a3d4b903a46fa14e91e66772841`  
		Last Modified: Tue, 13 Jan 2026 05:08:57 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f00b2e3933218e49feba543ae9da5f9a99e694fa143a0b369f3b1dc6d0d0fbd`  
		Last Modified: Tue, 13 Jan 2026 02:32:38 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7684c225310a7186686d90420bff2204e00d1da54ed64629dd5c3e06bedb11`  
		Last Modified: Tue, 13 Jan 2026 02:35:57 GMT  
		Size: 10.1 MB (10073782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6a425fa7aac586d22520ac0e48d6b900e2d7650c99f069fc369de3faad44f9`  
		Last Modified: Tue, 13 Jan 2026 02:35:56 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:03 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f9978ca299f165c197622edd759b69b3cf32899ccbb3854492744e5131a0d`  
		Last Modified: Tue, 13 Jan 2026 02:11:38 GMT  
		Size: 10.5 MB (10466724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdffb0278580783eda7f81d2d70ad20bf0b440ee7b7590e521dc0aa44d3eff2`  
		Last Modified: Tue, 13 Jan 2026 02:11:38 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d29a632dda1a11016736a63fec3296211533322f93651cd5c2f440ed3ea8f04`  
		Last Modified: Tue, 13 Jan 2026 02:11:46 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f369e3c2508700e6055a1900113ae937b42ec7d8683d5ef29fc8b48f14b44a`  
		Last Modified: Tue, 13 Jan 2026 02:11:38 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:09 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:b30144b25b4f9eda8cff7e3527ac291ee12ef4085cc006a28765cb84aa420700
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
$ docker pull neurodebian@sha256:a1f3d681375ae9877cb174d624d1c5cbd04a741b1cada66a9dbce8265700d3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ee6736859c305f7a5a63b3b9e54bdb047bf11407b4ec44ead45a2ee482f2e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:33:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:33:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0719b276ab21986970910cd53aa98e1720cae839dc3245e4539f6466de5586`  
		Last Modified: Tue, 13 Jan 2026 02:33:37 GMT  
		Size: 10.3 MB (10292332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4019c5b48e86642c8626c9b3af0135436b974b87db9eb8192ded3d7ef13afe`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc68ef74c45ffbb305959abee61f51b007da4b83b356f90740ea0a7a315015`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f5af02919eace9dd5db853e2f41d073cd35d27d1c0e8b76f95ff2f940f3dd0`  
		Last Modified: Tue, 13 Jan 2026 02:33:35 GMT  
		Size: 90.4 KB (90370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a513dcbfdcdcca80b9eceb62b78bd4af37a8672d7420381d085405a3dab7a`  
		Last Modified: Tue, 13 Jan 2026 02:33:29 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9817b4cc23261bdf6af3b2b878eac1bec5c62dd85db0d7bd7df14a6039a2817e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0565ca92f711426185538e4fc88ae99140917adec4068a1fd1343dcf23797c4a`

```dockerfile
```

-	Layers:
	-	`sha256:3fdaa0bbf6cb71883d44164a4f5068383c9f11b3230e9905be8b678a54d1ff65`  
		Last Modified: Tue, 13 Jan 2026 05:09:45 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc16a4a69d2920022ac713a906e760a6cf6c371075d6ad1f69e3a8198569a3cb`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ed602a8d82e45752b42458f6c6cf735a34652ba4dde594e695631d834d59b`  
		Last Modified: Tue, 13 Jan 2026 02:36:43 GMT  
		Size: 10.1 MB (10073712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8fc00822d28ca96ab3b0a281c9f30f594ddc2a1097c1d118b5a8d327ade838`  
		Last Modified: Tue, 13 Jan 2026 02:36:42 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:36:42 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:09:56 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34278bc983bca66a2b8695d2725d6c0031354a486b9d39d322df70ee7d8ffc6`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
