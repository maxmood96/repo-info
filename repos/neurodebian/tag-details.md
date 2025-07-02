<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:02e3b5f3334d51d17c907a109e7baa23a3b6f1efece977e6da220de111919d13
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
$ docker pull neurodebian@sha256:6550c17ae669fe37d08f6078e565a0004d60abe45a2e91105aade65b3fce087b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36183da1e19d84de51ea5809e4159ec8f2107f0b70c8aa80d638baf6b273f130`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e2dba99e5ec29a2897821803f9b24d793a027db51662af3afc8e9f66300421`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 11.3 MB (11266786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6474565e4f85706c018a8fe448db75bd10446e9317453d680ca2088c90aea693`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f48f7bf9a7cf900ab4406a612326c755655184ad87bad410ad08c3644c5491`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4256c9ee1313cf8432071147cfcaf1cf34aaef18083c431134d0d76c1021199b`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 93.2 KB (93176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b76cb89bd6c797b23f22af82a03567398b178f8a733f169ee5a6cec048223fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1028bf429c8a434cfa52f7718ced06affeccb0f6f0ec420c0c49d49066ba2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a3239e8e531bb9eb3cbe8ed2e8c93b3bd84ae65295907e1792c4f5348fc26c85`  
		Last Modified: Tue, 01 Jul 2025 04:07:22 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65a7d9bcec73f81f3d1625604e9081d8bacab46d57a5cccdf9bfe6f6da0b253`  
		Last Modified: Tue, 01 Jul 2025 04:07:23 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:684d5cf2924c0259869782c86482e0fad6a5cf03947551803433f7d28e0af651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59666965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e615e57fccd37453ac26b2cf379e4ef9a19c09e78f62dc0a56534e920e6be2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c5ba0efb742f26073ffd659a0388e8baf4bccb00e0d04d7b62e987a7790b2`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 11.2 MB (11232604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41477640941442aae5cee7da6735533b9fe3c5ae829c182a1a4b004a0d710e3`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f06fb7079001d13f92762cd5d30daf1c2f43d5f2d45c1f3f82a2a6396bd423f`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd28da870c451d725c581a4bff03979bc5383a096e98e9df515d7ba8fb18c9`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:98fc1096707aaf619c5bfd33109b22792b8f87cd0bcc58f78e99394d81bf6fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc34afb187651d95ce2ba9a89f16cca65216bf75fa5f2248be8ea5da18f69d4`

```dockerfile
```

-	Layers:
	-	`sha256:89c172bb4e8c24d867bdcf4bfa287c23da7328d77dbc4267ca164801af5342a5`  
		Last Modified: Tue, 01 Jul 2025 10:07:25 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837eb9afd4946b426cc90a905471476d56c51c3b1a5cda9841af37d7fa68cd08`  
		Last Modified: Tue, 01 Jul 2025 10:07:26 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:1eab43ffdf27740a4ff6b9871deef4219fc4477e411d7be25d4b22de0d34a9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61261707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8650137fe780d20c2a45a526a978891d45957513364b3407b3a98fce03e70848`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d91f5c279884c41d79cef474ce847b4a02b3539da5109ddb7c291583cfde223`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 11.7 MB (11688896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a27a41894bbfef54041fa4e2ad7a252456c0ea1aee79ba4868f486ddd4f297`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7938ada2d8cfb84599f71f893924e2223be3bd87eadf4d295c40802ed52d3bd6`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba7d51bfc7e68a98654699faa6f64431b601c24cbfa96d28e9ddcfa34d67711`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 93.2 KB (93218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:63b480a21b477fe6d50a7671f7e045fc812577457017b47afab4ac347120b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b42d2a8c7ccbc53dbf7ae36193dd021faa7764f233843b193f035ea43d73d5b`

```dockerfile
```

-	Layers:
	-	`sha256:286cf155bcb80c002a3636d3de56638554a5e2c1bb711b9a7d3f0b855c66ea2f`  
		Last Modified: Tue, 01 Jul 2025 04:07:33 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7327e91c792401ea5471f2c310b5640c40f44a4db82b5d3772b321fda5c46a`  
		Last Modified: Tue, 01 Jul 2025 04:07:34 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:cf9dca4312541dcdbb0fc6601e7e50430e6ee544f2f6122a2f24556cd4b5a0d7
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
$ docker pull neurodebian@sha256:1ba5cf138a7958ba2373be9f3a012409a50d4f6f69a99b904a23eeaaea1d55bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c59c69d4545682de48af80c95c5998b828426900abeab9761815fc72ae6b8e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff56d4e02de9968c2f7acfe0f70a56dffa1f9e68f2fb07c3a96568b07b7b337`  
		Last Modified: Tue, 01 Jul 2025 02:28:40 GMT  
		Size: 11.3 MB (11266805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f23f67636b82e4340303c4759ba6af0d6c3c122f287fc4aca86952ceeeefb`  
		Last Modified: Tue, 01 Jul 2025 02:28:38 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa6d87e2202e3f134289d48a6e278a08d1307503a49cdffeb0f0aba78d4e845`  
		Last Modified: Tue, 01 Jul 2025 02:28:39 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf5f2dd3e0931e38c25146d41b51a5971c5179c3d275a6470fb1af10a9a8ba0`  
		Last Modified: Tue, 01 Jul 2025 02:28:39 GMT  
		Size: 93.2 KB (93174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c61b91917510b6f66199037aa56cb86698ca55682be722023e3947b2b93e71`  
		Last Modified: Tue, 01 Jul 2025 06:02:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa9525deb20d8a44682ea41f8709711b3b5463a1f1f52fafb72734e7084ef2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcad6a81cb20bbcb750f2326b07a0c6580b3fa3e74783793afd18043c88e63f6`

```dockerfile
```

-	Layers:
	-	`sha256:2a5919c0c461a5cb92cbfc424ab6ac00ab3192939bf304dd87472fe1a966c7be`  
		Last Modified: Tue, 01 Jul 2025 04:07:32 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f5ca90ced41104a890aeb7615ec137b6270f87a8c4709ec7c6510bea1c1a973`  
		Last Modified: Tue, 01 Jul 2025 04:07:33 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c044cb999c18ddbac3e724f4197d6d33cf817d2dcb4d29b5735cc4b391c19794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08bb354e27b07933bf80c2c8991bc18389e2f3dd5114a4695d844ebfd8f3661`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c5ba0efb742f26073ffd659a0388e8baf4bccb00e0d04d7b62e987a7790b2`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 11.2 MB (11232604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41477640941442aae5cee7da6735533b9fe3c5ae829c182a1a4b004a0d710e3`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f06fb7079001d13f92762cd5d30daf1c2f43d5f2d45c1f3f82a2a6396bd423f`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd28da870c451d725c581a4bff03979bc5383a096e98e9df515d7ba8fb18c9`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5989b8596e3bed5b38dcff2149d968db29569057bd0e2ba6900b8158ccd1105e`  
		Last Modified: Tue, 01 Jul 2025 07:25:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a120f1032b969e7a2a8e8efcc1fdb899ea6fe663126e6b4f4a5291419035de11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71586ce4be5773db3e67483c5dbfe915bb3f90e317a494647a5e341a2641d99`

```dockerfile
```

-	Layers:
	-	`sha256:818f202638a8501264794f82f0c03559ff84d5d825a8fee26792e7beefd752ce`  
		Last Modified: Tue, 01 Jul 2025 10:07:29 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfea713e63f375e27832b900ab0f383c0343421ca2b3f9598847848880b0a693`  
		Last Modified: Tue, 01 Jul 2025 10:07:30 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:79e0f033de8cee8abcd6534af7c53e0091dbfb09316a132841d416594cdc5fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0525af502e390e1a5eda9692553346a25c3c21839d2774a07e3778a5d44e41`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6f94804b284437d7ef08613d0829711c88d64ccd070369893a5912c9c05896`  
		Last Modified: Tue, 01 Jul 2025 02:25:24 GMT  
		Size: 11.7 MB (11688973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f54c1638f4bbbbdf67ed7eed767ce99e7a40e7650e32e8d1dc6b58bb53656b`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19552ffd563dcf7d4dc18d2007c211133183546c1158baafbb4e96dc50a9ec51`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ce5aeae3d99912366df51677ffad150f086248c24913ea58482354c707d571`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 93.2 KB (93214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14be2ed04a1ef342abb523a07e79991996f57b732c627bf7ced803dc8faede73`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a84c5938426df0bdda06c3efbf12053b76c0eeb1e979fc464956185b4c4242c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94e7293e4eea8e4ddee297cb3b31e1961f22dc621faed88bca7c01a75783e3a`

```dockerfile
```

-	Layers:
	-	`sha256:6b08eb38b718237949b3eeccf1c246ac5b7f768396574a6db272c487b4a85a54`  
		Last Modified: Tue, 01 Jul 2025 04:07:44 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd4cd176f4c2ebabb39ea41aa1929c6dcef41fa670e7507291455902311ee16c`  
		Last Modified: Tue, 01 Jul 2025 04:07:44 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:324b07146dd268b377780fdb74380b9e9957b46ca3ccc13a16205536632a0bee
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
$ docker pull neurodebian@sha256:b687f95b09bd33f1d6fc6023c50035210c76b090d4452ac589b1e16943d40dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85053dfc60633d33e2da60411b52b36da568192c2d368791a87635521e4477`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def3f2dad6b1f604ad4c07c3db4985365f97269cc58f5920dd7a1500f2d8c8e0`  
		Last Modified: Tue, 01 Jul 2025 02:28:02 GMT  
		Size: 11.1 MB (11105129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ccba64b24515e9839769851aadb7822e51d08f355407c7c41beef62b118b99`  
		Last Modified: Tue, 01 Jul 2025 02:28:01 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776611f363aab3cdb88c94e560b83508c59dc3fee3c8587fc4ed0adaf8dddfde`  
		Last Modified: Tue, 01 Jul 2025 02:28:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcab2dd3be6f48e07a2160f3534a114758725b772bc038dfc4410214b453f7b`  
		Last Modified: Tue, 01 Jul 2025 02:28:01 GMT  
		Size: 101.2 KB (101197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6665a43de60208538f9220729a73928e3a9740302d4281e2a13f013115eda085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9217b8643e922f9471e290337d3f5d00221866205eb1e925f53662a166ffe8ef`

```dockerfile
```

-	Layers:
	-	`sha256:514144ea2bb344684170ef2aa30ae5c85a2ed7a4f8ed8a9635b6b0c163f1de56`  
		Last Modified: Tue, 01 Jul 2025 04:07:39 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540c5f8cc2d3e0620d788d859493e36fb4b167fa8116165969ab865bec5d66a`  
		Last Modified: Tue, 01 Jul 2025 04:07:40 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2c4dc2572b2d080ba1137ceba6fc4183ba6cbd936863b02dbb52a4fee4059d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ce529987960a1f864d4f1e229d4c38137c183bce9d16f105989e7d353c8ef5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256555700ef973ecb73aa3c8bc0f0d7fffe8a2735fa5d91f54019a21aa40f89b`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 11.1 MB (11106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848df86738100d71035e2542674c218a455d241a7441815ae04161bb461b4067`  
		Last Modified: Tue, 01 Jul 2025 07:24:22 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f66cf5fcdebd52fcf9840b91315c7cedd0ef5515157b00fdebe3adc6927e24`  
		Last Modified: Tue, 01 Jul 2025 07:24:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17143762973cab51c96bac474ff8a3892f07cd997104e133db9585aafefe2ec9`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3e30ebe8c2661d7fb6189254862075c00b7af23528a881a91d286694be7cf3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afe3b002bfa2bd8f329e7fbe5bd9226e6b36ec32a6e8204131c314c61402a75`

```dockerfile
```

-	Layers:
	-	`sha256:01e6ca6ebc7ed3e52ee8fa543b9e2d046095251fe7fed28a2471558b67ef15d1`  
		Last Modified: Tue, 01 Jul 2025 10:07:33 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f7e58cc6d5379f9227ea3b0df1025fc7671df63059a7a824d012e1da563e42`  
		Last Modified: Tue, 01 Jul 2025 10:07:34 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:6e909d6c7fa5cf372e8b4abe17f50eeca0e00c630503cec88634de534003f725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60d0d301ed5a1ddd3cf737fc8c7772446f55e1d7d79d437fdbe8d88e08089cb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cf048cdcda148f850e2e923337e3401fbe1b081347cb68f105fe08a801e7e1`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 11.5 MB (11500286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d5835ff83f8c042a185d3cba1bca9295d92658f244e9cd26f2b20ac9c1d1fe`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc86b84a80b36b0face148287be1c965f3409616a10ed9eb7c1b614634fcf52`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b3f1d3e2a2136e743e345a3eb6fb67b18d9dee013e83dcca7096e289dde428`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 101.1 KB (101087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2ccb5caefff2f66c642dbd34b4502767433f033578d678c313a27b4ba11d62b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf33f0ef895cbc93d99d36f202d2ae4942e8025fd3ab6e2c9eec54ce9f5f6cb`

```dockerfile
```

-	Layers:
	-	`sha256:eb2bcb20d589d3cd3dbc77ae5b266f8179020929c01c37afdb660b839c24a802`  
		Last Modified: Tue, 01 Jul 2025 04:07:52 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7136ffec7778c0aa2729a07697c8ecaf5aa45fe1a01ad817adb3d3f20e5e6871`  
		Last Modified: Tue, 01 Jul 2025 04:07:52 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:d17d04f1ac02bad66995998e2ae28c3c82e88e2fcec99f59c0a18d3c776e78f9
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
$ docker pull neurodebian@sha256:b734657b642e08b08866caab9911835193fca7ed33794f7c4367a19454d09b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03085fb17625d1c30ffeb65005700bf706908973c00ef9ac990715dd9e90c25`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dae0b7e934367d2b88f1ac500e6538a222db97b01cf9cd7802c0b1be056884`  
		Last Modified: Tue, 01 Jul 2025 02:28:18 GMT  
		Size: 11.1 MB (11105057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd1d44863bce699262cd8600fe21830eae99bebb3c4423506f7175be56b25fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0f1d88169004dac6c5eb7b29ee577f97f8b081e5497bcae03cad289250deef`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622fb8793f15015673349d020e6b0a437839d9874df364993a396b6648bb6031`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 101.2 KB (101210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b117c85b338d81d39e86682bd380689c8ca814cc3e8bb9666a9a2ea04786e`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5315131dd1e8ea9a82c8c3913d1a9587a8e49fe669b5028cd92c0d9181e77d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be7bd5c287af5b1a13999232ebb8b3e0682549e9d5ff9fe28976cf9ae46bfb`

```dockerfile
```

-	Layers:
	-	`sha256:8a6cf0c7e239504b10520ed25dfd0d1d09f6fb84444cc1e8127ab89f8b28ceb7`  
		Last Modified: Tue, 01 Jul 2025 04:07:47 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d202e357168780849b4b8cac96436c5205ca0df4b7820c95100679a4ed7bd95b`  
		Last Modified: Tue, 01 Jul 2025 04:07:48 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5bff9a16bf98b571670d436bd5d9854bbd08cb1407f3efe7936ddbaa18ec2c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63462044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169ed75b5dab84a414129956ace0159c7a385174e3f72a3cf4b529b69d587201`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256555700ef973ecb73aa3c8bc0f0d7fffe8a2735fa5d91f54019a21aa40f89b`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 11.1 MB (11106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848df86738100d71035e2542674c218a455d241a7441815ae04161bb461b4067`  
		Last Modified: Tue, 01 Jul 2025 07:24:22 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f66cf5fcdebd52fcf9840b91315c7cedd0ef5515157b00fdebe3adc6927e24`  
		Last Modified: Tue, 01 Jul 2025 07:24:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17143762973cab51c96bac474ff8a3892f07cd997104e133db9585aafefe2ec9`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a9b5681836457f57fd5729de52b55557dbe350bd0b8a5583dcd39c3f73610`  
		Last Modified: Tue, 01 Jul 2025 07:24:32 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87e5ba0fcd5512d411875a571e6be060eb598013f084bcc4279e9234bde8e7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9585c29e2d492b76e03c778214e269e64a09e0e5b3033f86fc7e222c387eb7b0`

```dockerfile
```

-	Layers:
	-	`sha256:fdcf64bd1ea6623d9a42c16bfef1676e2bd7fa832839b1a186fdc9a1e014e919`  
		Last Modified: Tue, 01 Jul 2025 10:07:38 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95323069abd8fd7d64d7456366c353250e6e5a9627d8e79eb60a2ed185822a0e`  
		Last Modified: Tue, 01 Jul 2025 10:07:39 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:925b4666368a4ad774e9d181983ba3b3ca654c5abf1519e4d7416b99428a6cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f232b4231124a7fe88e3bc96558cea4458da2f22c3f3164398abd4580befafa6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74345852c65cd02e4e4397d96e28831791f8af681c186316d165d7ada9b85457`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 11.5 MB (11500379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a71a431b08003b189839ebe38675ec712265886ad39cb2bc38f36f37de3ed32`  
		Last Modified: Tue, 01 Jul 2025 02:25:26 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc894d9ac437edcd3a53ff02d8bfbd4d37bd998aa2b3adb659ac2c3d875988`  
		Last Modified: Tue, 01 Jul 2025 02:25:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d2cf47ac839f5eccbb25d4bfcee634c5ecabca37f62b002db96ff745a5f676`  
		Last Modified: Tue, 01 Jul 2025 02:25:29 GMT  
		Size: 101.1 KB (101053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d1bcbbabde5f272e8544c78b363ef94f9221c61429c88fd16a84d0957d01ed`  
		Last Modified: Tue, 01 Jul 2025 02:25:27 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ec739be98441231feb937bc2ae098276e6bc04a105445c89edfd6d558117edd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17289b404e71a37192089b551b24b5db8ce32126f830c878efde71a437aac004`

```dockerfile
```

-	Layers:
	-	`sha256:18a9a8c9a1b8d2ebd12ef4e4c4ed490f485fa5079e20705d93d021243ff15ff0`  
		Last Modified: Tue, 01 Jul 2025 04:07:58 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1013ae2bb3f383bdf4055979fff2420a9f9685bdb331af179c41b9e293bfee64`  
		Last Modified: Tue, 01 Jul 2025 04:07:59 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:92998c4c5d81e049df56f5890828db1584b68d253e49b764d3e59d53e6fc25b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:082741104229bc5d5307ec00e18c8f0e1b92d9ec3c0d18af7b8fd2da303d5fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33272494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e26208fe4fba34f21e765cd213d0f4c4a40dbbb8ffa1e78524916b9b61fe65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2e34da2dc37f3eef61c15e677301ff9791b8f8f70f26fc479ec4d012ed513d`  
		Last Modified: Wed, 02 Jul 2025 05:27:50 GMT  
		Size: 3.6 MB (3624101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865b016ac2b42012c3a60696e045822e8d422cd29395baa864a7750882c4831d`  
		Last Modified: Wed, 02 Jul 2025 05:28:08 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cd7d87cd4cd2188a43546187d892a77babe87c7bcd43debfaf69196d95599c`  
		Last Modified: Wed, 02 Jul 2025 05:28:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cf12ea66c74872173d9ccfa48d1080fc8044a3c8c9bd394e42aef1c7181445`  
		Last Modified: Wed, 02 Jul 2025 05:28:16 GMT  
		Size: 110.5 KB (110529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e0eca4a2f8c5de61848c772c9ef1a28487cc1c88c4504e2d616b6186940ce062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5154015829843e5eadc330b8f1dfb807434bda45074d7881987814d6df084433`

```dockerfile
```

-	Layers:
	-	`sha256:83bfad6ad8349036754358056739fd70f033a0c9071ab4468f016e43222b0f1b`  
		Last Modified: Wed, 02 Jul 2025 07:07:27 GMT  
		Size: 2.2 MB (2198304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588008c9ba816410fe986bb801cb8cc7612f36a539781b2e81047f79dde3e244`  
		Last Modified: Wed, 02 Jul 2025 07:07:28 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a43a9f5cf2b5a6919be93498cf5e14d07d6136bc8978e4fe547f9ae25e0669f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31067642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b929f546c7741727f1b32663b03c90e2455044869615ae7a69cf5d8f770349e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c5693e3ea902ddf9017fc917526111e4b850b883c94049575082a3813eafbc`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 3.6 MB (3595659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6817bd2e46a1e80de24744eceb3b542bdd1e58f2e0a52074aae33b6191465470`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a819b02cab05dbf414b013d4dd4f8a294a9bf8274c20f6be6614d19a5aeb796`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dcc8e65b8099a3653adfe8c17639bdc3cae90813cac88317d52213709883f0`  
		Last Modified: Wed, 02 Jul 2025 05:59:22 GMT  
		Size: 110.5 KB (110530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:90637c4bf53ebcd381bf66f747337a22bf21290b659bee3c1e38bd4ed575e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434a6ddbe1f0ad866bc56aa49fce5ea510ec7f5598a330fecc7c11b1e7d0625d`

```dockerfile
```

-	Layers:
	-	`sha256:cb0f6dc44507091129ad6235df76d8506eecfaffe65b952b1195d241880821cc`  
		Last Modified: Wed, 02 Jul 2025 07:07:32 GMT  
		Size: 2.2 MB (2198564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4706ff6aa3b2ec92170560336d9a608877d30135ca5b534fc9740b80c4fac917`  
		Last Modified: Wed, 02 Jul 2025 07:07:32 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:efdea78c9ceb32fa30b09244de8778357f2127445e395d77b9b8bdae0bd311cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7628012c9ce33421ebe46723882b520d2dd3486af58d6dce9991b9ab4ee47c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33272732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac03db12eb00ddc67da22b7895962536be0140ac04c3e9a4f9717a2127e1b35f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41093334c179adf7ee2c998856026e656b770d3f0d616be80ddbd03bc0731f69`  
		Last Modified: Wed, 02 Jul 2025 05:29:07 GMT  
		Size: 3.6 MB (3624055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd96580cbdabfc7ae730a6c37534d8de4f2d40bb5504173b4708b34cd6ea5ecd`  
		Last Modified: Wed, 02 Jul 2025 05:29:16 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51be9392f49493c01c7da367417b8308180bf4410543718f8c661ba01829243`  
		Last Modified: Wed, 02 Jul 2025 05:29:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67067a6367ccc3c8bb0c66746345fa9bca0a7b36b77a33ab711d0d356bf366`  
		Last Modified: Wed, 02 Jul 2025 05:29:21 GMT  
		Size: 110.5 KB (110533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9032471d089343a57e88445514c5d8984d3bd4c4bdee7e3a9f365f4ac2740`  
		Last Modified: Wed, 02 Jul 2025 05:29:24 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:afdec840f8c89302e8a1c53cc1fa311c7a21bde6644a75925dcc2cb4625db7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a3a57040ecb9c6010cb2005511b811a0de3721e7c3def314ef05ec028967bf`

```dockerfile
```

-	Layers:
	-	`sha256:3ffce0d8c239d874a3c1920ff688b4f673fffc8d45f6cc0278c101a79ca98edd`  
		Last Modified: Wed, 02 Jul 2025 07:07:31 GMT  
		Size: 2.2 MB (2198340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506fd2f6e007e29edb41b564cd18ef46633fdbaa6d13bae3e7f2248b09f26f3e`  
		Last Modified: Wed, 02 Jul 2025 07:07:32 GMT  
		Size: 16.2 KB (16205 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9606aa5b8ca07ec70c713c1595412fc1b5f58e187d466ff359f1625cafd91af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31067929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31630d872868bec77a1bd3273f93c01e05bca9b7134f48af85f1315d53d2aba0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c5693e3ea902ddf9017fc917526111e4b850b883c94049575082a3813eafbc`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 3.6 MB (3595659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6817bd2e46a1e80de24744eceb3b542bdd1e58f2e0a52074aae33b6191465470`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a819b02cab05dbf414b013d4dd4f8a294a9bf8274c20f6be6614d19a5aeb796`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dcc8e65b8099a3653adfe8c17639bdc3cae90813cac88317d52213709883f0`  
		Last Modified: Wed, 02 Jul 2025 05:59:22 GMT  
		Size: 110.5 KB (110530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32962c795559f0f5f00baad5852df2b3dd9c691cc8aef40e9b650305a978f23c`  
		Last Modified: Wed, 02 Jul 2025 05:59:34 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71661675e1b45bce08c679dd642e959257b9a0855429f18a85b83d2414a64249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7eafe1b7d0d14252b5ca09fe258c6114a61b1b8acebca3b07d979c01241393`

```dockerfile
```

-	Layers:
	-	`sha256:ad1bd99d1c183a2e738e4251371bf379198f16bf345cc125d6f300a2bf2e78fd`  
		Last Modified: Wed, 02 Jul 2025 07:07:36 GMT  
		Size: 2.2 MB (2198600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeadbc25eab435a9430ee266732355ccc2ee87783c480e703b43bae8149e7808`  
		Last Modified: Wed, 02 Jul 2025 07:07:37 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:02e3b5f3334d51d17c907a109e7baa23a3b6f1efece977e6da220de111919d13
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
$ docker pull neurodebian@sha256:6550c17ae669fe37d08f6078e565a0004d60abe45a2e91105aade65b3fce087b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36183da1e19d84de51ea5809e4159ec8f2107f0b70c8aa80d638baf6b273f130`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e2dba99e5ec29a2897821803f9b24d793a027db51662af3afc8e9f66300421`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 11.3 MB (11266786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6474565e4f85706c018a8fe448db75bd10446e9317453d680ca2088c90aea693`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f48f7bf9a7cf900ab4406a612326c755655184ad87bad410ad08c3644c5491`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4256c9ee1313cf8432071147cfcaf1cf34aaef18083c431134d0d76c1021199b`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 93.2 KB (93176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b76cb89bd6c797b23f22af82a03567398b178f8a733f169ee5a6cec048223fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1028bf429c8a434cfa52f7718ced06affeccb0f6f0ec420c0c49d49066ba2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a3239e8e531bb9eb3cbe8ed2e8c93b3bd84ae65295907e1792c4f5348fc26c85`  
		Last Modified: Tue, 01 Jul 2025 04:07:22 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65a7d9bcec73f81f3d1625604e9081d8bacab46d57a5cccdf9bfe6f6da0b253`  
		Last Modified: Tue, 01 Jul 2025 04:07:23 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:684d5cf2924c0259869782c86482e0fad6a5cf03947551803433f7d28e0af651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59666965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e615e57fccd37453ac26b2cf379e4ef9a19c09e78f62dc0a56534e920e6be2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c5ba0efb742f26073ffd659a0388e8baf4bccb00e0d04d7b62e987a7790b2`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 11.2 MB (11232604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41477640941442aae5cee7da6735533b9fe3c5ae829c182a1a4b004a0d710e3`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f06fb7079001d13f92762cd5d30daf1c2f43d5f2d45c1f3f82a2a6396bd423f`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd28da870c451d725c581a4bff03979bc5383a096e98e9df515d7ba8fb18c9`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:98fc1096707aaf619c5bfd33109b22792b8f87cd0bcc58f78e99394d81bf6fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc34afb187651d95ce2ba9a89f16cca65216bf75fa5f2248be8ea5da18f69d4`

```dockerfile
```

-	Layers:
	-	`sha256:89c172bb4e8c24d867bdcf4bfa287c23da7328d77dbc4267ca164801af5342a5`  
		Last Modified: Tue, 01 Jul 2025 10:07:25 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837eb9afd4946b426cc90a905471476d56c51c3b1a5cda9841af37d7fa68cd08`  
		Last Modified: Tue, 01 Jul 2025 10:07:26 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:1eab43ffdf27740a4ff6b9871deef4219fc4477e411d7be25d4b22de0d34a9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61261707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8650137fe780d20c2a45a526a978891d45957513364b3407b3a98fce03e70848`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d91f5c279884c41d79cef474ce847b4a02b3539da5109ddb7c291583cfde223`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 11.7 MB (11688896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a27a41894bbfef54041fa4e2ad7a252456c0ea1aee79ba4868f486ddd4f297`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7938ada2d8cfb84599f71f893924e2223be3bd87eadf4d295c40802ed52d3bd6`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba7d51bfc7e68a98654699faa6f64431b601c24cbfa96d28e9ddcfa34d67711`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 93.2 KB (93218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:63b480a21b477fe6d50a7671f7e045fc812577457017b47afab4ac347120b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b42d2a8c7ccbc53dbf7ae36193dd021faa7764f233843b193f035ea43d73d5b`

```dockerfile
```

-	Layers:
	-	`sha256:286cf155bcb80c002a3636d3de56638554a5e2c1bb711b9a7d3f0b855c66ea2f`  
		Last Modified: Tue, 01 Jul 2025 04:07:33 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7327e91c792401ea5471f2c310b5640c40f44a4db82b5d3772b321fda5c46a`  
		Last Modified: Tue, 01 Jul 2025 04:07:34 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:324b07146dd268b377780fdb74380b9e9957b46ca3ccc13a16205536632a0bee
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
$ docker pull neurodebian@sha256:b687f95b09bd33f1d6fc6023c50035210c76b090d4452ac589b1e16943d40dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85053dfc60633d33e2da60411b52b36da568192c2d368791a87635521e4477`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def3f2dad6b1f604ad4c07c3db4985365f97269cc58f5920dd7a1500f2d8c8e0`  
		Last Modified: Tue, 01 Jul 2025 02:28:02 GMT  
		Size: 11.1 MB (11105129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ccba64b24515e9839769851aadb7822e51d08f355407c7c41beef62b118b99`  
		Last Modified: Tue, 01 Jul 2025 02:28:01 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776611f363aab3cdb88c94e560b83508c59dc3fee3c8587fc4ed0adaf8dddfde`  
		Last Modified: Tue, 01 Jul 2025 02:28:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcab2dd3be6f48e07a2160f3534a114758725b772bc038dfc4410214b453f7b`  
		Last Modified: Tue, 01 Jul 2025 02:28:01 GMT  
		Size: 101.2 KB (101197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6665a43de60208538f9220729a73928e3a9740302d4281e2a13f013115eda085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9217b8643e922f9471e290337d3f5d00221866205eb1e925f53662a166ffe8ef`

```dockerfile
```

-	Layers:
	-	`sha256:514144ea2bb344684170ef2aa30ae5c85a2ed7a4f8ed8a9635b6b0c163f1de56`  
		Last Modified: Tue, 01 Jul 2025 04:07:39 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540c5f8cc2d3e0620d788d859493e36fb4b167fa8116165969ab865bec5d66a`  
		Last Modified: Tue, 01 Jul 2025 04:07:40 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2c4dc2572b2d080ba1137ceba6fc4183ba6cbd936863b02dbb52a4fee4059d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ce529987960a1f864d4f1e229d4c38137c183bce9d16f105989e7d353c8ef5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256555700ef973ecb73aa3c8bc0f0d7fffe8a2735fa5d91f54019a21aa40f89b`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 11.1 MB (11106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848df86738100d71035e2542674c218a455d241a7441815ae04161bb461b4067`  
		Last Modified: Tue, 01 Jul 2025 07:24:22 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f66cf5fcdebd52fcf9840b91315c7cedd0ef5515157b00fdebe3adc6927e24`  
		Last Modified: Tue, 01 Jul 2025 07:24:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17143762973cab51c96bac474ff8a3892f07cd997104e133db9585aafefe2ec9`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3e30ebe8c2661d7fb6189254862075c00b7af23528a881a91d286694be7cf3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afe3b002bfa2bd8f329e7fbe5bd9226e6b36ec32a6e8204131c314c61402a75`

```dockerfile
```

-	Layers:
	-	`sha256:01e6ca6ebc7ed3e52ee8fa543b9e2d046095251fe7fed28a2471558b67ef15d1`  
		Last Modified: Tue, 01 Jul 2025 10:07:33 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f7e58cc6d5379f9227ea3b0df1025fc7671df63059a7a824d012e1da563e42`  
		Last Modified: Tue, 01 Jul 2025 10:07:34 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:6e909d6c7fa5cf372e8b4abe17f50eeca0e00c630503cec88634de534003f725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60d0d301ed5a1ddd3cf737fc8c7772446f55e1d7d79d437fdbe8d88e08089cb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cf048cdcda148f850e2e923337e3401fbe1b081347cb68f105fe08a801e7e1`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 11.5 MB (11500286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d5835ff83f8c042a185d3cba1bca9295d92658f244e9cd26f2b20ac9c1d1fe`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc86b84a80b36b0face148287be1c965f3409616a10ed9eb7c1b614634fcf52`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b3f1d3e2a2136e743e345a3eb6fb67b18d9dee013e83dcca7096e289dde428`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 101.1 KB (101087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2ccb5caefff2f66c642dbd34b4502767433f033578d678c313a27b4ba11d62b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf33f0ef895cbc93d99d36f202d2ae4942e8025fd3ab6e2c9eec54ce9f5f6cb`

```dockerfile
```

-	Layers:
	-	`sha256:eb2bcb20d589d3cd3dbc77ae5b266f8179020929c01c37afdb660b839c24a802`  
		Last Modified: Tue, 01 Jul 2025 04:07:52 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7136ffec7778c0aa2729a07697c8ecaf5aa45fe1a01ad817adb3d3f20e5e6871`  
		Last Modified: Tue, 01 Jul 2025 04:07:52 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:d17d04f1ac02bad66995998e2ae28c3c82e88e2fcec99f59c0a18d3c776e78f9
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
$ docker pull neurodebian@sha256:b734657b642e08b08866caab9911835193fca7ed33794f7c4367a19454d09b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03085fb17625d1c30ffeb65005700bf706908973c00ef9ac990715dd9e90c25`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dae0b7e934367d2b88f1ac500e6538a222db97b01cf9cd7802c0b1be056884`  
		Last Modified: Tue, 01 Jul 2025 02:28:18 GMT  
		Size: 11.1 MB (11105057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd1d44863bce699262cd8600fe21830eae99bebb3c4423506f7175be56b25fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0f1d88169004dac6c5eb7b29ee577f97f8b081e5497bcae03cad289250deef`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622fb8793f15015673349d020e6b0a437839d9874df364993a396b6648bb6031`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 101.2 KB (101210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b117c85b338d81d39e86682bd380689c8ca814cc3e8bb9666a9a2ea04786e`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5315131dd1e8ea9a82c8c3913d1a9587a8e49fe669b5028cd92c0d9181e77d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be7bd5c287af5b1a13999232ebb8b3e0682549e9d5ff9fe28976cf9ae46bfb`

```dockerfile
```

-	Layers:
	-	`sha256:8a6cf0c7e239504b10520ed25dfd0d1d09f6fb84444cc1e8127ab89f8b28ceb7`  
		Last Modified: Tue, 01 Jul 2025 04:07:47 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d202e357168780849b4b8cac96436c5205ca0df4b7820c95100679a4ed7bd95b`  
		Last Modified: Tue, 01 Jul 2025 04:07:48 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5bff9a16bf98b571670d436bd5d9854bbd08cb1407f3efe7936ddbaa18ec2c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63462044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169ed75b5dab84a414129956ace0159c7a385174e3f72a3cf4b529b69d587201`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256555700ef973ecb73aa3c8bc0f0d7fffe8a2735fa5d91f54019a21aa40f89b`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 11.1 MB (11106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848df86738100d71035e2542674c218a455d241a7441815ae04161bb461b4067`  
		Last Modified: Tue, 01 Jul 2025 07:24:22 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f66cf5fcdebd52fcf9840b91315c7cedd0ef5515157b00fdebe3adc6927e24`  
		Last Modified: Tue, 01 Jul 2025 07:24:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17143762973cab51c96bac474ff8a3892f07cd997104e133db9585aafefe2ec9`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a9b5681836457f57fd5729de52b55557dbe350bd0b8a5583dcd39c3f73610`  
		Last Modified: Tue, 01 Jul 2025 07:24:32 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87e5ba0fcd5512d411875a571e6be060eb598013f084bcc4279e9234bde8e7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9585c29e2d492b76e03c778214e269e64a09e0e5b3033f86fc7e222c387eb7b0`

```dockerfile
```

-	Layers:
	-	`sha256:fdcf64bd1ea6623d9a42c16bfef1676e2bd7fa832839b1a186fdc9a1e014e919`  
		Last Modified: Tue, 01 Jul 2025 10:07:38 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95323069abd8fd7d64d7456366c353250e6e5a9627d8e79eb60a2ed185822a0e`  
		Last Modified: Tue, 01 Jul 2025 10:07:39 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:925b4666368a4ad774e9d181983ba3b3ca654c5abf1519e4d7416b99428a6cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f232b4231124a7fe88e3bc96558cea4458da2f22c3f3164398abd4580befafa6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74345852c65cd02e4e4397d96e28831791f8af681c186316d165d7ada9b85457`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 11.5 MB (11500379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a71a431b08003b189839ebe38675ec712265886ad39cb2bc38f36f37de3ed32`  
		Last Modified: Tue, 01 Jul 2025 02:25:26 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc894d9ac437edcd3a53ff02d8bfbd4d37bd998aa2b3adb659ac2c3d875988`  
		Last Modified: Tue, 01 Jul 2025 02:25:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d2cf47ac839f5eccbb25d4bfcee634c5ecabca37f62b002db96ff745a5f676`  
		Last Modified: Tue, 01 Jul 2025 02:25:29 GMT  
		Size: 101.1 KB (101053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d1bcbbabde5f272e8544c78b363ef94f9221c61429c88fd16a84d0957d01ed`  
		Last Modified: Tue, 01 Jul 2025 02:25:27 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ec739be98441231feb937bc2ae098276e6bc04a105445c89edfd6d558117edd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17289b404e71a37192089b551b24b5db8ce32126f830c878efde71a437aac004`

```dockerfile
```

-	Layers:
	-	`sha256:18a9a8c9a1b8d2ebd12ef4e4c4ed490f485fa5079e20705d93d021243ff15ff0`  
		Last Modified: Tue, 01 Jul 2025 04:07:58 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1013ae2bb3f383bdf4055979fff2420a9f9685bdb331af179c41b9e293bfee64`  
		Last Modified: Tue, 01 Jul 2025 04:07:59 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:02e3b5f3334d51d17c907a109e7baa23a3b6f1efece977e6da220de111919d13
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
$ docker pull neurodebian@sha256:6550c17ae669fe37d08f6078e565a0004d60abe45a2e91105aade65b3fce087b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36183da1e19d84de51ea5809e4159ec8f2107f0b70c8aa80d638baf6b273f130`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e2dba99e5ec29a2897821803f9b24d793a027db51662af3afc8e9f66300421`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 11.3 MB (11266786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6474565e4f85706c018a8fe448db75bd10446e9317453d680ca2088c90aea693`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f48f7bf9a7cf900ab4406a612326c755655184ad87bad410ad08c3644c5491`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4256c9ee1313cf8432071147cfcaf1cf34aaef18083c431134d0d76c1021199b`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 93.2 KB (93176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b76cb89bd6c797b23f22af82a03567398b178f8a733f169ee5a6cec048223fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1028bf429c8a434cfa52f7718ced06affeccb0f6f0ec420c0c49d49066ba2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a3239e8e531bb9eb3cbe8ed2e8c93b3bd84ae65295907e1792c4f5348fc26c85`  
		Last Modified: Tue, 01 Jul 2025 04:07:22 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65a7d9bcec73f81f3d1625604e9081d8bacab46d57a5cccdf9bfe6f6da0b253`  
		Last Modified: Tue, 01 Jul 2025 04:07:23 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:684d5cf2924c0259869782c86482e0fad6a5cf03947551803433f7d28e0af651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59666965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e615e57fccd37453ac26b2cf379e4ef9a19c09e78f62dc0a56534e920e6be2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c5ba0efb742f26073ffd659a0388e8baf4bccb00e0d04d7b62e987a7790b2`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 11.2 MB (11232604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41477640941442aae5cee7da6735533b9fe3c5ae829c182a1a4b004a0d710e3`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f06fb7079001d13f92762cd5d30daf1c2f43d5f2d45c1f3f82a2a6396bd423f`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd28da870c451d725c581a4bff03979bc5383a096e98e9df515d7ba8fb18c9`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:98fc1096707aaf619c5bfd33109b22792b8f87cd0bcc58f78e99394d81bf6fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc34afb187651d95ce2ba9a89f16cca65216bf75fa5f2248be8ea5da18f69d4`

```dockerfile
```

-	Layers:
	-	`sha256:89c172bb4e8c24d867bdcf4bfa287c23da7328d77dbc4267ca164801af5342a5`  
		Last Modified: Tue, 01 Jul 2025 10:07:25 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837eb9afd4946b426cc90a905471476d56c51c3b1a5cda9841af37d7fa68cd08`  
		Last Modified: Tue, 01 Jul 2025 10:07:26 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:1eab43ffdf27740a4ff6b9871deef4219fc4477e411d7be25d4b22de0d34a9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61261707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8650137fe780d20c2a45a526a978891d45957513364b3407b3a98fce03e70848`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d91f5c279884c41d79cef474ce847b4a02b3539da5109ddb7c291583cfde223`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 11.7 MB (11688896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a27a41894bbfef54041fa4e2ad7a252456c0ea1aee79ba4868f486ddd4f297`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7938ada2d8cfb84599f71f893924e2223be3bd87eadf4d295c40802ed52d3bd6`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba7d51bfc7e68a98654699faa6f64431b601c24cbfa96d28e9ddcfa34d67711`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 93.2 KB (93218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:63b480a21b477fe6d50a7671f7e045fc812577457017b47afab4ac347120b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b42d2a8c7ccbc53dbf7ae36193dd021faa7764f233843b193f035ea43d73d5b`

```dockerfile
```

-	Layers:
	-	`sha256:286cf155bcb80c002a3636d3de56638554a5e2c1bb711b9a7d3f0b855c66ea2f`  
		Last Modified: Tue, 01 Jul 2025 04:07:33 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7327e91c792401ea5471f2c310b5640c40f44a4db82b5d3772b321fda5c46a`  
		Last Modified: Tue, 01 Jul 2025 04:07:34 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:cf9dca4312541dcdbb0fc6601e7e50430e6ee544f2f6122a2f24556cd4b5a0d7
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
$ docker pull neurodebian@sha256:1ba5cf138a7958ba2373be9f3a012409a50d4f6f69a99b904a23eeaaea1d55bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c59c69d4545682de48af80c95c5998b828426900abeab9761815fc72ae6b8e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff56d4e02de9968c2f7acfe0f70a56dffa1f9e68f2fb07c3a96568b07b7b337`  
		Last Modified: Tue, 01 Jul 2025 02:28:40 GMT  
		Size: 11.3 MB (11266805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f23f67636b82e4340303c4759ba6af0d6c3c122f287fc4aca86952ceeeefb`  
		Last Modified: Tue, 01 Jul 2025 02:28:38 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa6d87e2202e3f134289d48a6e278a08d1307503a49cdffeb0f0aba78d4e845`  
		Last Modified: Tue, 01 Jul 2025 02:28:39 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf5f2dd3e0931e38c25146d41b51a5971c5179c3d275a6470fb1af10a9a8ba0`  
		Last Modified: Tue, 01 Jul 2025 02:28:39 GMT  
		Size: 93.2 KB (93174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c61b91917510b6f66199037aa56cb86698ca55682be722023e3947b2b93e71`  
		Last Modified: Tue, 01 Jul 2025 06:02:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa9525deb20d8a44682ea41f8709711b3b5463a1f1f52fafb72734e7084ef2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcad6a81cb20bbcb750f2326b07a0c6580b3fa3e74783793afd18043c88e63f6`

```dockerfile
```

-	Layers:
	-	`sha256:2a5919c0c461a5cb92cbfc424ab6ac00ab3192939bf304dd87472fe1a966c7be`  
		Last Modified: Tue, 01 Jul 2025 04:07:32 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f5ca90ced41104a890aeb7615ec137b6270f87a8c4709ec7c6510bea1c1a973`  
		Last Modified: Tue, 01 Jul 2025 04:07:33 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c044cb999c18ddbac3e724f4197d6d33cf817d2dcb4d29b5735cc4b391c19794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08bb354e27b07933bf80c2c8991bc18389e2f3dd5114a4695d844ebfd8f3661`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c5ba0efb742f26073ffd659a0388e8baf4bccb00e0d04d7b62e987a7790b2`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 11.2 MB (11232604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41477640941442aae5cee7da6735533b9fe3c5ae829c182a1a4b004a0d710e3`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f06fb7079001d13f92762cd5d30daf1c2f43d5f2d45c1f3f82a2a6396bd423f`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd28da870c451d725c581a4bff03979bc5383a096e98e9df515d7ba8fb18c9`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5989b8596e3bed5b38dcff2149d968db29569057bd0e2ba6900b8158ccd1105e`  
		Last Modified: Tue, 01 Jul 2025 07:25:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a120f1032b969e7a2a8e8efcc1fdb899ea6fe663126e6b4f4a5291419035de11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71586ce4be5773db3e67483c5dbfe915bb3f90e317a494647a5e341a2641d99`

```dockerfile
```

-	Layers:
	-	`sha256:818f202638a8501264794f82f0c03559ff84d5d825a8fee26792e7beefd752ce`  
		Last Modified: Tue, 01 Jul 2025 10:07:29 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfea713e63f375e27832b900ab0f383c0343421ca2b3f9598847848880b0a693`  
		Last Modified: Tue, 01 Jul 2025 10:07:30 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:79e0f033de8cee8abcd6534af7c53e0091dbfb09316a132841d416594cdc5fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0525af502e390e1a5eda9692553346a25c3c21839d2774a07e3778a5d44e41`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6f94804b284437d7ef08613d0829711c88d64ccd070369893a5912c9c05896`  
		Last Modified: Tue, 01 Jul 2025 02:25:24 GMT  
		Size: 11.7 MB (11688973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f54c1638f4bbbbdf67ed7eed767ce99e7a40e7650e32e8d1dc6b58bb53656b`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19552ffd563dcf7d4dc18d2007c211133183546c1158baafbb4e96dc50a9ec51`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ce5aeae3d99912366df51677ffad150f086248c24913ea58482354c707d571`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 93.2 KB (93214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14be2ed04a1ef342abb523a07e79991996f57b732c627bf7ced803dc8faede73`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a84c5938426df0bdda06c3efbf12053b76c0eeb1e979fc464956185b4c4242c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94e7293e4eea8e4ddee297cb3b31e1961f22dc621faed88bca7c01a75783e3a`

```dockerfile
```

-	Layers:
	-	`sha256:6b08eb38b718237949b3eeccf1c246ac5b7f768396574a6db272c487b4a85a54`  
		Last Modified: Tue, 01 Jul 2025 04:07:44 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd4cd176f4c2ebabb39ea41aa1929c6dcef41fa670e7507291455902311ee16c`  
		Last Modified: Tue, 01 Jul 2025 04:07:44 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:92998c4c5d81e049df56f5890828db1584b68d253e49b764d3e59d53e6fc25b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:082741104229bc5d5307ec00e18c8f0e1b92d9ec3c0d18af7b8fd2da303d5fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33272494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e26208fe4fba34f21e765cd213d0f4c4a40dbbb8ffa1e78524916b9b61fe65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2e34da2dc37f3eef61c15e677301ff9791b8f8f70f26fc479ec4d012ed513d`  
		Last Modified: Wed, 02 Jul 2025 05:27:50 GMT  
		Size: 3.6 MB (3624101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865b016ac2b42012c3a60696e045822e8d422cd29395baa864a7750882c4831d`  
		Last Modified: Wed, 02 Jul 2025 05:28:08 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cd7d87cd4cd2188a43546187d892a77babe87c7bcd43debfaf69196d95599c`  
		Last Modified: Wed, 02 Jul 2025 05:28:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cf12ea66c74872173d9ccfa48d1080fc8044a3c8c9bd394e42aef1c7181445`  
		Last Modified: Wed, 02 Jul 2025 05:28:16 GMT  
		Size: 110.5 KB (110529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e0eca4a2f8c5de61848c772c9ef1a28487cc1c88c4504e2d616b6186940ce062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5154015829843e5eadc330b8f1dfb807434bda45074d7881987814d6df084433`

```dockerfile
```

-	Layers:
	-	`sha256:83bfad6ad8349036754358056739fd70f033a0c9071ab4468f016e43222b0f1b`  
		Last Modified: Wed, 02 Jul 2025 07:07:27 GMT  
		Size: 2.2 MB (2198304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588008c9ba816410fe986bb801cb8cc7612f36a539781b2e81047f79dde3e244`  
		Last Modified: Wed, 02 Jul 2025 07:07:28 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a43a9f5cf2b5a6919be93498cf5e14d07d6136bc8978e4fe547f9ae25e0669f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31067642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b929f546c7741727f1b32663b03c90e2455044869615ae7a69cf5d8f770349e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c5693e3ea902ddf9017fc917526111e4b850b883c94049575082a3813eafbc`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 3.6 MB (3595659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6817bd2e46a1e80de24744eceb3b542bdd1e58f2e0a52074aae33b6191465470`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a819b02cab05dbf414b013d4dd4f8a294a9bf8274c20f6be6614d19a5aeb796`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dcc8e65b8099a3653adfe8c17639bdc3cae90813cac88317d52213709883f0`  
		Last Modified: Wed, 02 Jul 2025 05:59:22 GMT  
		Size: 110.5 KB (110530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:90637c4bf53ebcd381bf66f747337a22bf21290b659bee3c1e38bd4ed575e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434a6ddbe1f0ad866bc56aa49fce5ea510ec7f5598a330fecc7c11b1e7d0625d`

```dockerfile
```

-	Layers:
	-	`sha256:cb0f6dc44507091129ad6235df76d8506eecfaffe65b952b1195d241880821cc`  
		Last Modified: Wed, 02 Jul 2025 07:07:32 GMT  
		Size: 2.2 MB (2198564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4706ff6aa3b2ec92170560336d9a608877d30135ca5b534fc9740b80c4fac917`  
		Last Modified: Wed, 02 Jul 2025 07:07:32 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:efdea78c9ceb32fa30b09244de8778357f2127445e395d77b9b8bdae0bd311cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7628012c9ce33421ebe46723882b520d2dd3486af58d6dce9991b9ab4ee47c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33272732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac03db12eb00ddc67da22b7895962536be0140ac04c3e9a4f9717a2127e1b35f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41093334c179adf7ee2c998856026e656b770d3f0d616be80ddbd03bc0731f69`  
		Last Modified: Wed, 02 Jul 2025 05:29:07 GMT  
		Size: 3.6 MB (3624055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd96580cbdabfc7ae730a6c37534d8de4f2d40bb5504173b4708b34cd6ea5ecd`  
		Last Modified: Wed, 02 Jul 2025 05:29:16 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51be9392f49493c01c7da367417b8308180bf4410543718f8c661ba01829243`  
		Last Modified: Wed, 02 Jul 2025 05:29:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67067a6367ccc3c8bb0c66746345fa9bca0a7b36b77a33ab711d0d356bf366`  
		Last Modified: Wed, 02 Jul 2025 05:29:21 GMT  
		Size: 110.5 KB (110533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9032471d089343a57e88445514c5d8984d3bd4c4bdee7e3a9f365f4ac2740`  
		Last Modified: Wed, 02 Jul 2025 05:29:24 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:afdec840f8c89302e8a1c53cc1fa311c7a21bde6644a75925dcc2cb4625db7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a3a57040ecb9c6010cb2005511b811a0de3721e7c3def314ef05ec028967bf`

```dockerfile
```

-	Layers:
	-	`sha256:3ffce0d8c239d874a3c1920ff688b4f673fffc8d45f6cc0278c101a79ca98edd`  
		Last Modified: Wed, 02 Jul 2025 07:07:31 GMT  
		Size: 2.2 MB (2198340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506fd2f6e007e29edb41b564cd18ef46633fdbaa6d13bae3e7f2248b09f26f3e`  
		Last Modified: Wed, 02 Jul 2025 07:07:32 GMT  
		Size: 16.2 KB (16205 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9606aa5b8ca07ec70c713c1595412fc1b5f58e187d466ff359f1625cafd91af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31067929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31630d872868bec77a1bd3273f93c01e05bca9b7134f48af85f1315d53d2aba0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c5693e3ea902ddf9017fc917526111e4b850b883c94049575082a3813eafbc`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 3.6 MB (3595659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6817bd2e46a1e80de24744eceb3b542bdd1e58f2e0a52074aae33b6191465470`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a819b02cab05dbf414b013d4dd4f8a294a9bf8274c20f6be6614d19a5aeb796`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dcc8e65b8099a3653adfe8c17639bdc3cae90813cac88317d52213709883f0`  
		Last Modified: Wed, 02 Jul 2025 05:59:22 GMT  
		Size: 110.5 KB (110530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32962c795559f0f5f00baad5852df2b3dd9c691cc8aef40e9b650305a978f23c`  
		Last Modified: Wed, 02 Jul 2025 05:59:34 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71661675e1b45bce08c679dd642e959257b9a0855429f18a85b83d2414a64249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7eafe1b7d0d14252b5ca09fe258c6114a61b1b8acebca3b07d979c01241393`

```dockerfile
```

-	Layers:
	-	`sha256:ad1bd99d1c183a2e738e4251371bf379198f16bf345cc125d6f300a2bf2e78fd`  
		Last Modified: Wed, 02 Jul 2025 07:07:36 GMT  
		Size: 2.2 MB (2198600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeadbc25eab435a9430ee266732355ccc2ee87783c480e703b43bae8149e7808`  
		Last Modified: Wed, 02 Jul 2025 07:07:37 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:cf9dca4312541dcdbb0fc6601e7e50430e6ee544f2f6122a2f24556cd4b5a0d7
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
$ docker pull neurodebian@sha256:1ba5cf138a7958ba2373be9f3a012409a50d4f6f69a99b904a23eeaaea1d55bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c59c69d4545682de48af80c95c5998b828426900abeab9761815fc72ae6b8e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff56d4e02de9968c2f7acfe0f70a56dffa1f9e68f2fb07c3a96568b07b7b337`  
		Last Modified: Tue, 01 Jul 2025 02:28:40 GMT  
		Size: 11.3 MB (11266805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f23f67636b82e4340303c4759ba6af0d6c3c122f287fc4aca86952ceeeefb`  
		Last Modified: Tue, 01 Jul 2025 02:28:38 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa6d87e2202e3f134289d48a6e278a08d1307503a49cdffeb0f0aba78d4e845`  
		Last Modified: Tue, 01 Jul 2025 02:28:39 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf5f2dd3e0931e38c25146d41b51a5971c5179c3d275a6470fb1af10a9a8ba0`  
		Last Modified: Tue, 01 Jul 2025 02:28:39 GMT  
		Size: 93.2 KB (93174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c61b91917510b6f66199037aa56cb86698ca55682be722023e3947b2b93e71`  
		Last Modified: Tue, 01 Jul 2025 06:02:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa9525deb20d8a44682ea41f8709711b3b5463a1f1f52fafb72734e7084ef2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcad6a81cb20bbcb750f2326b07a0c6580b3fa3e74783793afd18043c88e63f6`

```dockerfile
```

-	Layers:
	-	`sha256:2a5919c0c461a5cb92cbfc424ab6ac00ab3192939bf304dd87472fe1a966c7be`  
		Last Modified: Tue, 01 Jul 2025 04:07:32 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f5ca90ced41104a890aeb7615ec137b6270f87a8c4709ec7c6510bea1c1a973`  
		Last Modified: Tue, 01 Jul 2025 04:07:33 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c044cb999c18ddbac3e724f4197d6d33cf817d2dcb4d29b5735cc4b391c19794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08bb354e27b07933bf80c2c8991bc18389e2f3dd5114a4695d844ebfd8f3661`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c5ba0efb742f26073ffd659a0388e8baf4bccb00e0d04d7b62e987a7790b2`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 11.2 MB (11232604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41477640941442aae5cee7da6735533b9fe3c5ae829c182a1a4b004a0d710e3`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f06fb7079001d13f92762cd5d30daf1c2f43d5f2d45c1f3f82a2a6396bd423f`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd28da870c451d725c581a4bff03979bc5383a096e98e9df515d7ba8fb18c9`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5989b8596e3bed5b38dcff2149d968db29569057bd0e2ba6900b8158ccd1105e`  
		Last Modified: Tue, 01 Jul 2025 07:25:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a120f1032b969e7a2a8e8efcc1fdb899ea6fe663126e6b4f4a5291419035de11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71586ce4be5773db3e67483c5dbfe915bb3f90e317a494647a5e341a2641d99`

```dockerfile
```

-	Layers:
	-	`sha256:818f202638a8501264794f82f0c03559ff84d5d825a8fee26792e7beefd752ce`  
		Last Modified: Tue, 01 Jul 2025 10:07:29 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfea713e63f375e27832b900ab0f383c0343421ca2b3f9598847848880b0a693`  
		Last Modified: Tue, 01 Jul 2025 10:07:30 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:79e0f033de8cee8abcd6534af7c53e0091dbfb09316a132841d416594cdc5fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0525af502e390e1a5eda9692553346a25c3c21839d2774a07e3778a5d44e41`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6f94804b284437d7ef08613d0829711c88d64ccd070369893a5912c9c05896`  
		Last Modified: Tue, 01 Jul 2025 02:25:24 GMT  
		Size: 11.7 MB (11688973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f54c1638f4bbbbdf67ed7eed767ce99e7a40e7650e32e8d1dc6b58bb53656b`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19552ffd563dcf7d4dc18d2007c211133183546c1158baafbb4e96dc50a9ec51`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ce5aeae3d99912366df51677ffad150f086248c24913ea58482354c707d571`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 93.2 KB (93214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14be2ed04a1ef342abb523a07e79991996f57b732c627bf7ced803dc8faede73`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a84c5938426df0bdda06c3efbf12053b76c0eeb1e979fc464956185b4c4242c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94e7293e4eea8e4ddee297cb3b31e1961f22dc621faed88bca7c01a75783e3a`

```dockerfile
```

-	Layers:
	-	`sha256:6b08eb38b718237949b3eeccf1c246ac5b7f768396574a6db272c487b4a85a54`  
		Last Modified: Tue, 01 Jul 2025 04:07:44 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd4cd176f4c2ebabb39ea41aa1929c6dcef41fa670e7507291455902311ee16c`  
		Last Modified: Tue, 01 Jul 2025 04:07:44 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
