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
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:936d6b469fbff5c8a402abe66b09f4bf64c61a8c2f7b9f929bf555bccbdd3fa9
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
$ docker pull neurodebian@sha256:bcf81a5101225a7cd909074ee0d0b3b0edee6f32ade3caa814b5ad284f5bf410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e56c3919c86f15faaf5a11a91cbcb6dc32337e086476aa1eefebbaa987adaf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ec4595a3d975d4fe1463c119991d3b97ea186dfdb9beaffbf86d82f87256`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 11.3 MB (11273409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ea247c34b90330172a7683ea0e1d3552d14a478c597b3835fb3f8dcd6fff53`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bba4d323b5bde10a427f41b802e88ae13e2502d12a6f71543f41c638086b13d`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1983b6eced4bb9a5a3435c20a0e80be0f95ec3298d68729b3e3d51442d6e8c2`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 93.4 KB (93386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b30d613e90e133607300246f61900aa635e8fae8b149e443014a815ac31f051b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e08651d25a04d45e850bdb93958025e7a5be0bdaf86f2425a902274a9c636c2`

```dockerfile
```

-	Layers:
	-	`sha256:2db9e2cd120b4ce9ace4b747159ff3a6af43f8835dea224090629d18e284c24f`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce89be306770279efb86a1ccc18a50813f0663a5fab4ec216c7fd2e419529bfa`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 14.0 KB (13963 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c383b1c8bcc59487007ea946c97be72b381f54ee51d5fd892cf0629fdeb1c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628c1e90e3da7350faabb21fc74a0c88da8663666dd19dbdb74ba907e12ef2b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbeab365177c9b941a081ba0b6d957ba147319fe32dff22aa2624a53a06f29b`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 11.3 MB (11252933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fa205d0d4d9ff7d136faa66f376fb23aff6334613faa278f84518f8e5c01ff`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14309867687b534670e51c1d96567476c0f1aaed795f789d0445fab07399b4d`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89033d9b2184954874f8f00b5a17aecc6b429a80a8e0038b84aa6ee81ff3383`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 93.5 KB (93546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ede2b6186f52eb37d412780815c7330d58d6faa9837786a7e5c79b52f572fd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ee394c617722eaa31b6265fd68e7ac215a0a018ff4f39c2985bca8c06e3347`

```dockerfile
```

-	Layers:
	-	`sha256:d4b4657e224bc234c23ab66a4c0a2fe772e905a9fe22fae905f739583d04c417`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29aedf8be25ddf5a7975ddb70961e5bb9c8359ec72bba50cbb2e61f0f256a671`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 14.1 KB (14088 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:4db04057176b65f60447ea0de14d71e589435efc93f5f9e0942650cbc343e201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d0d6bea08068fbb0f25ca7e55202dd93371d5e2f960b095b57d73b56802257`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb9739c6b4f68bc7ceda360ba82976ffea2a2b0f910162f3baaddf10c30baaf`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 11.7 MB (11693065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d4aa3bbcd7f103db531b544aa469fc669490bf0f63070fb63340476b4b2ff6`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f5291b6f5da64f52099bfd741111dd36b90a2fef3af20ec6d5cc367da8d4bb`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea8274562ed42a6906cd9cd33a459780630e229f388af5b5627ab5ae06b749`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 93.4 KB (93437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e167ffe5ba168b8cc58cf782364dda325b14826d22b80241ce109a8f1f87cfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c80c7632358c017feeb7106b43d3f8a70130d34fb57220e3a95f07cf348c3e8`

```dockerfile
```

-	Layers:
	-	`sha256:f6175cf9e3596d080ca37a17bf2e4e4756b45b06df58d192cd2d34c654ec1021`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e857221844e8f6652439e116a12b9371a11d1e340573ecc8b292cf063c8552`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 13.9 KB (13935 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:9301742359389f2d2738c1f6decafb303e83a33da734b5262947586e3fdba70f
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
$ docker pull neurodebian@sha256:99792aa6ba989a7415f0cd2cb8e195c8aa99bb3c897fe33a7bf5c35607c275fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517d328014a4be6f7b02aa9d27f2bb76abc751cbc7e0234bfbde2239a7433a8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157e5aa142e191f389177cafc25663cf3ead7455488e9b3ae8d80faac203470f`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 11.3 MB (11273453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139c6137c970e0c7654c2cbd7329fc30bb23de4da7928a386b807149d6d4257`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eae6607455a450e3b7448918a266a5499f18306d75cae839cf0e46cdac78678`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de341e23682505074c2fde67892b0004b2e62d8351a93b78e388774d57c92afd`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 93.4 KB (93413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2970b98df9f5f093f0122c8c3983b1b6e87287a424fe66b37b04e459da79b8a`  
		Last Modified: Fri, 08 May 2026 19:44:40 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:21531d38e6403bf24665a621472f6c8082e62fa42aa9ae11d4bf72ae1bae6da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4593617393e092d54b447d141bc3d9055d3dd3fb0bc63c086ec490b43db5eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a5ec5d989239fca2a2f74da4290145a9fc4c5111be3458d332ca6523993ba972`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9c958dd7a81bf5555df9c02b20af25ae3d95a6fbc3d76dfe60c15f229dfa70`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ce456a29d55af753754c81bcf6c489b588e4ef8d345a25a1185ac4ed38d7067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83671130319d212529fed9657df2275a72b7a9972a90c7d4eeb3087a8c2e780`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297af71f398d804e9824bb6964f5f84de1d86338b03a2c087345a9e6adeae9e7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 11.3 MB (11252932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbc6e93f45b3f4cf455734139898464377b66e14251b76f3361f3d34ed49b9d`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2bd671e957e80374283f5fb64814dafa746ed40e7cf68d7972fffd7054de17`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c4f363214c80dee9f62e6d8d410c16b88764ef3e641e1d8bc9231b3d9cae7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 93.6 KB (93575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1d2f24bc5c69d6c727ad3568cbc4addea466c9b6cc928ea044b626717466f`  
		Last Modified: Fri, 08 May 2026 19:46:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f29b6635607465a6f03d6780e7c09679fb49ac9bb340deaae75b283f8ed832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3acb1d5d8d6cb02f7c1e8bd1cb80b8eb98d8808fa839c362abc1fbb0ad92f8`

```dockerfile
```

-	Layers:
	-	`sha256:c992b9778cd7c443812a6eca47e360178d13695c8043203be74e9562afd8f30e`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5d86f16916b238e87145c3058d5b9f4308cb209db7450c1e9f13152f33e5b9`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7bc7df072b8d4192da532d04d6fead4b1e24bc92dc244d3039bd8a47c37f53fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3f5e69332c4e42d45a5f556b5626d9a922ed8e3e5702c07d3e8270f7a02cd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fd686c2be4701aa5e99504e0a0a231438cebab31803f9703d4f2817fcfaf3c`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 11.7 MB (11693032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c275dff193370be94cf6b05afcd2f50b992d61b429151ede147e0d16bd143`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed34c26dacdd7f022ad39094d3a0e7234c0e1adaf272d36639f4a548d0bb34a`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed24d41000306ac52cbf2623e08455d064489dded03b85fd01bce6bd72a7c0`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 93.4 KB (93421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c476f9525210c69f52698c6764a1dd93f0e3c72cb3941432ffad0b4dfe7ee5f`  
		Last Modified: Fri, 08 May 2026 19:44:53 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8707a48f987ea14bd078ac3746d28881d4119f0480d7627964a7d15c52545760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7f5ae92125a30eea36bb373c2d4ef882b6f6936fbc0adf910cfc3e2feec4c`

```dockerfile
```

-	Layers:
	-	`sha256:f5e53c43561d0cbbbb39a871b900ba903431c52a26c9b7b5d743b6635d3bfdc9`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6d2384fe0ae77451cec1bc567fb85d31e77c7b721f8bf337871e4e30ebdf90`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:0b737232c9794e792613e2948c2dc646da73742794d05989706bdda85dadfb98
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
$ docker pull neurodebian@sha256:948a806d10e8de99412f13e48921d95a685331e685fcc5407941162c24a64d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c739e12ee1b66df8b53d57247ccb7d3ccde3a9da7ade4e337147027212c8c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb0713476e6838e62fce3e969ddf9e132bfcb3d7e2381b96a3e6590bea17355`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 11.1 MB (11103472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8c97eadffb1f79f36461db289f9d13b34abe3b10d6b2212fb7cb568f87c88c`  
		Last Modified: Fri, 08 May 2026 19:44:17 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb74a3e1d476d5675ca0b0ec9c21c09ed0ceb2776c8b0b4d9f6211687d86722`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19972676d50f6a3f1df56d9a06783980125881e306a22240dffb30771d4c04d9`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 101.4 KB (101405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ec6f6d915f962e6180edb45f9e2b0ed07d34d1a406ca966444a00063bf5c0bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e318efab8b68b3a161ff0ded8b0cbbb53f5f184fd83aa7308634335aff71761a`

```dockerfile
```

-	Layers:
	-	`sha256:2e54cd4f6b03da76b043ede7315e1c5f2c6bee9f880f71566cac57f4127ab4b8`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848dd6c010f74e7c1081c9108123e2b50de591b2f2cc38e0e7e07b7bde117f73`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:62347cb324bd70e5569c022cf36e136aa8e826f40f1c2238889b719f8cc66a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088aaba085173fd83cbf817a16c6e4af04bdc9ae9eedb10afd7c44e3489ddef4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49da93cc2679b1db042cd202e875060e5e3220e87732350bd5904898892e8b8`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 11.1 MB (11109914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825eee855070f51dfefec4cf70685dd607f1dc1402855869b4bbcaf7b576135`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3209c067378d18d75a18203938000ce323b7b747348cca016301c372c516e6a7`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c848bef723aca7f046b18ce448a4097239a1da120f540e52dd1c9a68a4b31`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 101.3 KB (101279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4243308f1b786a75f6a0506780d5c7b33ac30f8511fccca56aec4dea210c21b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e762402feeb4d06253b996167883d80d3641bf9e0680cf01273d11c016d6d5`

```dockerfile
```

-	Layers:
	-	`sha256:b14f0dcc1c2ef0142185e8793a6e22f9422570c4ba9d2b6abb2cb7125ce110f1`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2aa08681f076f24ce71cb639cc4949a46b91a1a127541e91c515a501664465`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:8008767bb706f4c4cb709ab5f06a757d417059201885cf55e86abcb4cb6dcef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2c192eae3260d4134a76b7bfbe15ddfec137154687d3fa42db1128cb0fe0a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e381fa04b31e7bcb9cbbc40e4bf2902f0c275db7edc7b0462ee8936db48315`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 11.5 MB (11502397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ab2eed64c3b37a86ab0b509b8f661cecbf7b66e171eaec9e5c546fa3036762`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a997cd26a4c569d5d64a9da26466d3c5c487619a3e32f1c97969f13fa616a`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3596ad0c31ef351fa9a9305382ce6d40415c6c0b91c7298614f295de6c8582`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 101.3 KB (101301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:42f660d3785330ad3907a27b2a3014a5478c77cb6a2ae7174a586851e2a97d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f329d1467811d726f323694ba1065308a4220276c10e46100ba962ecb9c53f90`

```dockerfile
```

-	Layers:
	-	`sha256:a6c78a26c8ba94bd4d662a5f8aa1daccf0739185d688ddd88ead6c3050508785`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad96a7377786062bdd01bea8d0bb1ed027db71956b280c297a74b774fa1ab0db`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:1b2d3eb7162fae37bb54559c3bac058da9808476b1876f6027f94729f0fea0c2
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
$ docker pull neurodebian@sha256:970c3a6ae528525bb1e8ab1ec34a277265ab7d1abdb574832d47e7b4b8c78959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3cb5553e0927f86dbaffefdba643cac55d235a4910d2d479e673633f35f833`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c21a08615a577f1cfa9ccc4980ad83b9af3be6520d08499173bfbbb61cc28de`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 11.1 MB (11103504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa6222b3a12994a0a3d2d5aa4e59b93806764f67a9b46108db2375b92572559`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3439e15c014b6ca69436cc53714a5a12b8c82d212bba1d8118567a3fbd3d26c4`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1712a4f29c136e1d7c3f29a70419828d6a06c4f8c0bd8aa2555a88172fd1f9`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 101.4 KB (101392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921683cc3659083392b4ff077850901d45c2fac00ad861af8966aae15ec5a7d8`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:80de42a461bdee72a6de0d2d96c33b96fda58b0f709ab38dda5fbda0dee923d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c6e6e38805523120e40167d506fa8e6fbb1c80532580e72d86225e2ef8685a`

```dockerfile
```

-	Layers:
	-	`sha256:ecf8938eaaae846b52eff960911e1aaeaeea774db94fa0d9270c7ccacacba99b`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97ff8956eacb6b69eead663a90a02709ad62af7970c98817fcf8310f3c26185d`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d72cd51fb944fbeefc59dbcfd9207dd62d6b1409175dc0b62c30c20f9723340d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c72a73a81907cd10f4ed9d514fe1d0c96154b13d775360ec1f4e578b4b7c08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4d4853c366ae1d8a6092357fdeceb46f1af7fb6971f30fb5bac64d2816093`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 11.1 MB (11109872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860e8ce6527c5e5eb574f904941f9d5fd1ac72704eec1e19c9667591571cda7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407a0ee518c92a25d491c4909ce3ed0cb4f84524941a201a7cf2bfd943c1ed7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86985c6bd9a382f6fe79e55952fe846b9dac4b331da91606603aeebec797fb71`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 101.3 KB (101294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a645068ae63614955aa0cce30edd178a25de8ca2dd269f25af6a34467cb6d54c`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e79ba75ecd78047e815efee9fa2ef478d94689d9d1ab9f20fb7ba7bf72a022e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aae72f0e29b5b3a88976fb346afe0082117da0014a70001d64ee3963b586eab`

```dockerfile
```

-	Layers:
	-	`sha256:97a48df79af5e64bcca963ffbc0947249e8e2964559cd3a0216d0b5fe3a662f7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ecf2ecbf82b72a416e1ef61bc9ea6fe75d4c000ee213c306b6148414a9521`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ded0c9f44bfebe4345080e2a4390c3b4fed39780d1353b24e811e6661fba9ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a59c5ac3b1631f24b5bc8d5baae5bb53973e1d0f372a2f088c0314105f17e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9627add8f31e74417d79a305014794f3cbdfc718e75672d32ef679cae4d543`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 11.5 MB (11502376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fbbd060166db850453937acb417b1629ded3d89e8f175047d313eb4d4ea249`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bda2e809eea5007777365a49ca07551a25dead0adc7cab0981a605143ef59a`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f25d850d54a1638e683ef541be2effa3bca6c0b42442affc13c0b580347563f`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fad3e9fd8287dfd51f1b9399e6918557a0ab780529cfb43d95f377c5871ffc`  
		Last Modified: Fri, 08 May 2026 19:44:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84d520f83be769fc2d681e70788d29039c5cde27701f289c18e4bab929ce8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24962661fd033444e442b5d8f8a4cce6aa12e5693c6953d7f1bff736b34e166d`

```dockerfile
```

-	Layers:
	-	`sha256:423513329c10f41f709cff6f55c81130aebb09ea250c3f3d837102c1163b7fbc`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4f37060f92539dd9a20f74d6de85a1f15bebe90d992329da9927373d4af4e8`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:ccc940c9d2313a988be650e62fa8fe32896169d7166dada433cb7577c7127b92
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
$ docker pull neurodebian@sha256:823eba2bae9921e5463b6eddfd83ea6ec97be637f27393c7becd15416cdfd2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60076903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6453d6a4685ccd2fe37f542bcf9ffc8d8d1d85e846201edb41d98468372ca394`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:44:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e929ba940bb6645aaebb3cf3e1b30d0ccaa2f7d53cb82e57d451efa023dead7`  
		Last Modified: Fri, 08 May 2026 18:23:00 GMT  
		Size: 48.6 MB (48622043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e894cb91c5db397e5c3ebf6633fc5ebbab445f65fbdd4935dec5f6dc43ccb8`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 11.4 MB (11362509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d43a67b811a859ca589502f851db11afc79e31242d643c4eff5a05f7e633a95`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd467f5800893dee759399c43bc14785cf96cd9adea98dbdfe2350dea8708e06`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9326cf6c59b1d22ee9d0eaa828b37444e375e7416a42afbfc0efaa1ab04b62a2`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 89.4 KB (89447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fae01ebd151036016f748add050d543821c6787fd1c8c202f3700afb9c388c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af742fa40471c540b7db0eda1d05cfacb054817217b3e40387ca666778dfda2`

```dockerfile
```

-	Layers:
	-	`sha256:677cf0ab5038da62decc38492ba5f7524541156fb4ae31f22a283b7e62b46d99`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 3.6 MB (3556244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551e6773ea14d7cf6411fc65fbd7026c699bb5cba718984d5078e0fb08b69de8`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4445a9b88c3aba497a2008d7c26ab7680dc4cc162d8bc18e7fdd2abe797929b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a6e9a7461b3bd032f5da0f32d43b6ef28490fb1b2a094321029284aea38845`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38be54f67917d094862e34ed83d9f5b14050260224cc43c64865734d5907fd67`  
		Last Modified: Fri, 08 May 2026 19:46:46 GMT  
		Size: 11.1 MB (11059291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc2a856e734427e804ed50a73e236f216b87a5f0fe32affedbf2c2fdb7e367`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb5943e9f00792ba990c85877f68cd02fb0f955ac2c056c784d0a7f5efe7b7`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148505e68f723384842e9256ab27a20502fb933a703a02c8a8387a13fde81fa5`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 90.1 KB (90057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ffe6c1be02db912c32558802a1cee4640d3337a3f6da771c03c12a11baeb264d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dfd5864f60dfab734040f18b26d324ec7edae066ea58ce1f03dbf96587f3bb`

```dockerfile
```

-	Layers:
	-	`sha256:750cd9e0c7163f4d2f76ca439df028cb8f7e095be5f57e672cf6e8101639d6c2`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 3.6 MB (3561592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b03532524e5b66cb48a0b22ed5257ca466acb5e304ca5e4b016ba269a51762ec`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:229b368a6b98d7ce660433a55e8b2363a19a2f808ab9c873f24b05b1a8a7be84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61605870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075291128ef3150dc12f76a862c4d327c51305f9d2d92705a276cef92e88d3be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fd7fd52239cf41c1513003560316f753d3b29bffb106c1c8cbf260e58621e`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 11.6 MB (11589003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b51446d80054a5f43c4ce780e4dc27dd69be5690c5515991223b5af7a9fdb9`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39c1cdcded0b2bce400d9caac28b0b5ddc7273cc5e5c057393fdcebbb9055d5`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3edebb8be1094d35833e792183bac8d8b69a4cce9b1de1627b384fde68c22b`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 89.7 KB (89744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7585901b3fcd61be98cc07c0fce812830eeccbd9bbbc4c73075927b5a94c6ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b2de58ad6d4212e7b4a3044a392c77b1cb7b570cafeb9b7a95c08097b9b83`

```dockerfile
```

-	Layers:
	-	`sha256:a5e656a37608c6c496bbc4e3f21f2e6ebdd0ca00774a6b5e42196d97aca1ff25`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 3.6 MB (3554190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac42095d0498fb668d35a1880cc1400381b34697805a03ea4a3cef3243668e26`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:cef5a7249de9c877b5f697fa3e104454149bcdc02e814a22d09bd463bda75f31
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
$ docker pull neurodebian@sha256:5226686b3732483477cad20cd6e322d9998a4bf932871ab9fc2f87848d7dad60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60077340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f04cff1ccfe79e7383ead04f269d7ec790faa2f6c04d69c1c31e94390981c27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0e929ba940bb6645aaebb3cf3e1b30d0ccaa2f7d53cb82e57d451efa023dead7`  
		Last Modified: Fri, 08 May 2026 18:23:00 GMT  
		Size: 48.6 MB (48622043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631bd401a9ea85121899c742741152c2d753c20f5063b4935e5677c9b9bb941`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 11.4 MB (11362517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c5849b7c2876a6e27b5173f8d1e8f02d5fcd243d1dfc50b858e91b67083f22`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a5f0d6856a2cfa52c99b2c2ed11dfd8851eb14b84b636b738a49ade15c18a0`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9758222cb4c90ec2c761ca114b3db8c018b0d6b65d329a9f50422fda80d02d31`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e2980abcfd428f39d3236270246d8a542601ad7016f6a19e3f33ca6c13b26`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:51d3b372a86f0abfb8cf682c3f299797d0fa31e061849f6511133bfa2430f687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067694b030e0ad0f1a824f2d5271aac7d5f509e60a64cb051696a7c62e671b9`

```dockerfile
```

-	Layers:
	-	`sha256:51c0f2b8c73138f5a50f5cfb4cdb5f94ba792bf7099a8cd6c1236b12edd975e8`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 3.6 MB (3556280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af51c446d933ca99eda664c827ad478fc09984eed72ce1e7c5689ab96396f57f`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c5f596c4bf8c0ccc478841c47092c4a4dad71a015d664685dc1c4b96dc058b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9528113b20964df2f7a7b1284f55ba0993cab2d96ad5485be40a46fb10c581f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be64bdc407e7e3b95b79a3ffa508782d23c39791fc66237b6b9ac0079e6f8e5`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 11.1 MB (11059006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a038166bca6013ff60ba5efd623dbb4e5fe1ee3d4446048b568c45cd48f1f4`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc2ed7a3a505ca3103c47fba46d5e291e08d49ee72ba39dedef20b1008f326`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a68e5868a8cbc24ca18677d15c10aa94f4c51fb3e1f19e418a98acd77848b6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0446785ebbf74532dcba92825c6decba78dcf6a16420b18506b2ed57f7928eb`  
		Last Modified: Fri, 08 May 2026 19:46:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b0d5416b6794a636e42304fdb74a53a9ee53950b35de114de8bbb04947b6043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bac42a5873dea8825b57dc7136a3a27ca3ab5b4fcb1501abbb9798be97ed00`

```dockerfile
```

-	Layers:
	-	`sha256:24443809fcc31ff23bd314ca750f0f95a8effe8849bd1131390892d2ec92e5a6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 3.6 MB (3561628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a27081017521680b89fcfa70690d05d07b6f2c8103aaa1557dbe8917649d344`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:03a1a328bfee5ff0a2bcd6a694bf094d95381b9b663a843aa2e3ae99924b758c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61606220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c3c7ade491f697623eaf25c70f50f5a71cfb7bb1d3153121edb8caadc6b964`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a99493d96d6f92ea6d88890fe995d3918a05c9baec0b84c6e9d10b95007a82`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 11.6 MB (11588918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a0c33e147fa59d9124cbf1b02679d5996d94f20e43a0b0dcc7bac0c76d9bae`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a895ebfb8de9b1aba761e3f5032daf08032da3fa41c4770fb7be187e4cf0`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d22eba06c949e34b02517b4968779ffafdb8e6ce52c51cf497c682389b154`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 89.7 KB (89726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2616c3f976bfa74ec623fc4792a7910f4ad8177ed3b117a8e270087f0510a539`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c75c21cbb9fff8f22041a53794d1631c30d371e24e4a25d431e1c649eb7fa77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7075d85a25976a8e3bcacbf0a99c3a51ddb29e013c5b42c7da1a973f852c1ea0`

```dockerfile
```

-	Layers:
	-	`sha256:7ca33354efa5a678e18c52598a002e0f989c7bb096e45147472c2b5788c43e45`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 3.6 MB (3554226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d2a0a43649d8f679119161461ce4dc60d130a0faefe0533fc5173dbdb17353`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:75f904d0c67f4c9858cff6f0103e91027e807518b04fe5f8092efc0c0981aa3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:50424def1a9f9c45659cd9a3c8fd7be20b771d9faf316706d56191817d0a7bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caa9f0454a8506b06908af40b3180c7ab34e543901a0d141383284031761739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e965e0cbfb28916191745c6417d4338beea7aec2cb5fd81e10dec40dd2e8366`  
		Last Modified: Fri, 15 May 2026 21:20:18 GMT  
		Size: 3.6 MB (3624588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b460ff363337b53a251fba6ab38f85ae7dbd0d322131f9f7ef3e3e5ec3993841`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c526a5517cd48bc16f89213299da52f9690296195e5ac59667a2bd643e3c5e41`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf8b1159386b1fd839b78027a3b340ad638ebceb5a5539d309b242933f1831`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 111.2 KB (111232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e412202f26ceb6d4c1bcffdc5575ef0790972dcdd1ad14eaf46f040cac1316cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f887bb03cdd347eeb92f232c6a07d31436a34375b07e390389807dabe87027`

```dockerfile
```

-	Layers:
	-	`sha256:809d99babe923ab2dd062a2f570a5266b242a04c4fafc307c92fed2e3a9b282b`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 2.2 MB (2198324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdea2d028b9d02999d109dc927e7a4f4f2eb569da53527dbaa7364aabe4f58ae`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:97414ed4f59910609b1a9d705b7a3a667c26066208e644efec505f633b47edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31324763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a849cdc79b65cf626b3b9fcf4493328abde886f8144f0e07b67910f9031ef4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5439fbff57039d8111c79e00db08bd4ce15263bd5b99af9187a4bc0f4e8b3a3f`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 3.6 MB (3604765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4e64fc2883d214a40a57eaf9b537698bd2716c653c6222dcbfe6fe31ae80c9`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16947bc03ead29ec0c191d87407de3718f236783939aab991b0796802259874`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6602ba41307da6865e1f72143c4370a3e8314e6549962b23a911c4258a962097`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 111.2 KB (111196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b49ffa2049e4591c8f82f011202a785b743c0a435508fa5289cd41580900181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a7e9d197c9c0dc0a6f3713a812beb76783de250350cd4f1c949813ce36d7b`

```dockerfile
```

-	Layers:
	-	`sha256:6e35d0abb6e3a97793d611df4083460be5d8ca41a0a4a4caad1681ea6c693031`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 2.2 MB (2198584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3059046f1d26c24c93d9cbbebe2a0e41abff976015c5e06bf32a4c00ed72ba5a`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:c15cc5b2609215d38f487ca74d9a0c364fef640456351786ba6ed7ddbdbd9e23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:741e4d235640395bb69af07b20575215e3726c3a51b342d7a6ab63b03f542913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d070a1b4367810c74bf7fd5297d7c2b0bdf28bfb7bf8fb1d2f140a7477eb6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38cc2da34443ee698d2fb5746eeb70d00d8cf9832f5c179c94dd01d32a6c322`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 3.6 MB (3624605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8de9718e2df29fa2d76f88c5bdf5a5d1c67dd9cb2a42ac280a5a11008d6cad`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c6677ad71bba680f8167c8974b73f8286635b51e89d7e59b83165f5c783e4`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815bfcf7ec7f087a70287169d800d287b5168932caff8ea06f75959b47451481`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 111.2 KB (111242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49aaddb4c43128aebecde25753a0bb923ccbf5ea00aa45045cbaf373d236054`  
		Last Modified: Fri, 15 May 2026 21:20:21 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:81dcf4b3a3c8ea4dc21201c4b401da4547964aa00e40f97394136dfdee1287ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5876d21edff0cea93eac4c36709504c4935003c3b39eff6d3fcb78e2c01670`

```dockerfile
```

-	Layers:
	-	`sha256:fea8fd6c0a0c0ec27d42693017eb03dcb6517cec0badbda611767531ced60f5a`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 2.2 MB (2198360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30444ea650f022aaa5e6707a1d474afb7a85e00f07e9dec8bf133305f85eb69`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ebb7a5aaf051c49d265817b4c21a8f3e1f4340caa4351791250395b45a1daeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f7558d4f7ce8272783cff8b620052a1e42f297365702f22fed127d8fa014ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfba9082861e846762690f8c9061bf0b330a06abe65636c2f7b0cdfb25816ca`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 3.6 MB (3604762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eec572cc90753bca88496df6fd51ebb6a228bd52acfd45bb858c247fe34c87`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6e73b3568c2e79fee913e8fb0a2417d91340fb6ff38a5a55fd03819c0aa86c`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254233f274bb3fe0fd62162e9a7bd9946f215e74774b49e235310bbef9e524f`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 111.2 KB (111186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7e707bf8653b57bc80f5de25934e155b312dfce4cc4e3277a8dec5b82a3aa0`  
		Last Modified: Fri, 15 May 2026 21:20:40 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:02916722ca03dcac193f1f622dfc12e91bf090281b8072122d1ce4e2b71f5c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba93e33625286cae36e90a26e761bf14cb9cc9a67492eb5aee053c0159c1beeb`

```dockerfile
```

-	Layers:
	-	`sha256:81747f061bbcb86cfb76d061f8c57a6146ba8174df02ef5a65b960be9d7224d6`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 2.2 MB (2198620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb84873f4648ef88e059c7ec03f22b542751d2dea12d0f148bd6cd60c7d624d`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 16.3 KB (16301 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:7d615974d7618624acaf024c794146f6955178920e4a11205f0b463c1a903434
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
$ docker pull neurodebian@sha256:48409e2266289921f625e696fd82ae75b3dc7d3429568e904bccb3046e022dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982b441ccd68e375ce55850b6f2530e35f89c4a858bb75344fd7a5dded7d5ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603e83f84352e4d604d1ebd2e7b11a116e1d73c815b1f21b71c35cf4d26a6adf`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 10.3 MB (10293033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9841317468747bb9c4d672ac9e22fdbaf7467995b3009c013af9504275765`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97afa150b5dfa5f4868492e1872f0bd5d68742189b24436efcc83edb5b863ad1`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80469e6eba86735ca23d5fc2e8e6e31019a42fe3e7a96b5d2580cffd3a1892ab`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 90.4 KB (90409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93973523588868a89ea7a3048595fc8a05179b43bd1a791ce32770712d00e9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3739871772f9c6753eab2831cf79f90dc38c2a6030448f67185547885e75dffe`

```dockerfile
```

-	Layers:
	-	`sha256:48c1c93d4580490d300f49739cf9b99e4a0678b32abf78a80898f5033fa0cc82`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a980516244bf1755bee0e5c4047d7bd22a6645fb62f256893244939631312c4`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d503ee17e4a04127673e873eadb5e238338d8534e69de76f9a2834dea00068f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d388d64eed3a472d75c0230a0f7e0ec18ea76b7a49cf2f265fc7b87ba9fbbad9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c629af507dca062ea56f93574fa391e844b4d6e1b5cd11cad63be92b46a1d6`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 10.1 MB (10078011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abab8ca898857514fc5bd463e6e97a767bbca2cb8aea60e359cd6acaaa15751`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a787e0f5c6e783915e7fc9afa550e0bcf87b812188a88bfe09536d428841b0`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac226701451e2fd232f7351b186bb36b4f7e1742f26e18192509106d28c45ec3`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 91.0 KB (91035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dc047d2f30ed6ac4ec61cc1afcc3087048f8b38a8af931444118db41c4d4566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb1e88be3ddf79970c3f161eee07195b0acfc24a53e5306704d479fd7126a7`

```dockerfile
```

-	Layers:
	-	`sha256:4d576367898d58cb2af04ebc67ca27c1a684572a74fe8c3a8c3fa9d91bb20031`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349d03efc82e58b0fabaeba13d01e95372d1322c71cdcb42706cd4ee07d99898`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:674b7f113ab98f457c90a5407cf9fce5d326c1ada9d335c3bb736dac15df1d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd893df613b6c8c15a740d7cf4906096d1c477af22aea43f2c1a7965c5c10b95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918b15ce42e2f43331d7ca8a6909c2f318788178997f3be2a6c20d15686eae08`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 10.5 MB (10467078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d8c3e17a2f821d9a1e4a647dd71fd281974066ed12286ff5344c3c70918add`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745c310d83150426f135a032fe18cc82a8e5631e02d97a07354f8c9341131d6`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d13836b8f7a1419799c27ce5e5586655df8273d6004aaa0c492b5a99f6622d`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 90.7 KB (90733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e4dfc7f492836cce5f36a3a8e3941b8d6619c004fb9fb3e8a3df42c8c567950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911b218b44e62288fb317f239ec58d54680252b6ad5b7b84abdeee0eff2adaf`

```dockerfile
```

-	Layers:
	-	`sha256:b35285063f63c97ca1e2f1b58a75539e178f06a4277ff94135e31ab43d844d97`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be65c44927642dbaf0443b5d950bdb2eba7e045ec2186605bd5528701cc1ccdc`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:5462c83858d3feb66eab9b4197a35e7c3f2c97168a1f033fa5ff54bc7b0089db
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
$ docker pull neurodebian@sha256:8a4c8e5c02d9c032eff3aca30a89bb11dd0afdb58ba10ea078d0248b1842a7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60186278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739630cd28c1d946604021f5e65b72c0489c653c44c1558e0271fc06dc041df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:099d3355eff9ccff1f5ee3b288e1ead2e7035e89d68d0fc80f60a9bd7a9815e3`  
		Last Modified: Fri, 08 May 2026 18:23:36 GMT  
		Size: 48.7 MB (48702238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e478533e6ae193c6fcaae041855399f59338878fa7e4644c40a17730309dca`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 11.4 MB (11391655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601904e49e5900acca267146a686c3f2a2a62c1246a1e38d212fea83bffbe0bb`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d949441ff174a57a6fc707bc732ca1634e6558df38f4715cbfcbaebe99f00`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dbdaf7f7809f135ace320cd033d9a6d661f149877bfc78ee99f12ba8f0ae08`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 89.5 KB (89483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:412cbed693a82d055a8f5357999ea9f0053401665d64aeef08fd5f06d2dcec0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66b334229b8a964cc51e6b877024313d7cc9a4d9a13c5c0ac570a1714ad128f`

```dockerfile
```

-	Layers:
	-	`sha256:2798dfba3ee312a5c3c86f73e2dd22eff329c06e0ea7cf6108e8ab3f170b1791`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3556234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c8c7bd53e080388c9a1eb264e0fbea45b097b66db0192338955fa9903db445`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8d042e0c6b2b0bdc7bd6088a54197a0062b4e77fef4e334f0b514b42ce76bf43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca4e48d28afe7d23765196f54fdea60741801af0f6b198d4f1d7aff164ec43b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2a6841249cc037385aca9cb88bc26e07cfa8ed2a3f883ffdea8ae1be354b5a`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 11.1 MB (11092978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938906dfc842f7becc351af1835f05072b61776a354569f75a22d1f1e6ac299`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0668f71f67e7f7a552b9af4850f0941fb6afd56c29cadc4acd358584bd8a7518`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c06c9c91f639614d4952e3ed20b59bf97c833709c3620987f812909d74f82f`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 90.0 KB (90027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1515e7f8ac45bd3a4a536ba87d58574f9beedb409c59fc72752b88164c944056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36672cedf692ab9b354876cbf435214d90917c05080107060f25e608acf9f045`

```dockerfile
```

-	Layers:
	-	`sha256:1aa37ce6e70e12258b02b458c1845581d86ecdd450c40a6a59c724b75463cf93`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 3.6 MB (3560939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da2b316ca48ed77a2b1aa0ced2f3d8e67b58143d8135f7f24e5168d05f49127`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:73ba3061222d6c325c0a346e63bc504de41f9532e07a59209fa44e4519dcdabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5af2eace4327f02703f432d25d547b430da3ef4030f8154d0d4dd1322459e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f0c0878f24a22f4bae1cce2bb33ade2528e750968c7f19e4683f865ecf624f`  
		Last Modified: Fri, 08 May 2026 19:45:28 GMT  
		Size: 11.6 MB (11625846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83aff980bc85ff5b2ce155faf54e6e3fbf0412fad6b9b461726d7a94f49ec8b`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1690741b56c00af9a9e027b2f45da2d3c964439f6016d2a01ae49e540c9a138`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403996057114e2cd0d36ee941960ee517faaab068e8e0cbc9de09e96c9223a56`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 89.7 KB (89717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ab1c10a7c00e20030be43916af676fbd69ea524a13a3d1f1100bc9cad07f30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df6d819178bee19b394bd34bd99b9a33ff2d758ed51a85705d80ba78362451f`

```dockerfile
```

-	Layers:
	-	`sha256:2890089b6f33dd50ea7d84ff7f43fd03e40b52a12e2925bb4cd5456bc7dd9b0a`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 3.6 MB (3554180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27aea920f78950a42d40670e7327c30443ef99b9d23d92570dbbee1e83f95701`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:eabaa9df6e6f28acda269868f36fe6b1ef1678d2762119d6c77c78b5d87b1363
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
$ docker pull neurodebian@sha256:5334a29a1f0fb4835758c1b388e322a2348ec3032da1a4e6572e98134532a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60186655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064c3891de8ce33ff0e4fe108f5171b68727f60ddc6590af502f8e0281df2af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:099d3355eff9ccff1f5ee3b288e1ead2e7035e89d68d0fc80f60a9bd7a9815e3`  
		Last Modified: Fri, 08 May 2026 18:23:36 GMT  
		Size: 48.7 MB (48702238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85957d69d501ec6d0cc38c388d29b67893409a599a0fcd2b22af2a3660ed4cc`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 11.4 MB (11391676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d154e7fe6720de57e32775de2e5bdeba041c1cc8be9924ff6250053bca50a1e`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01de64d5db46c87cdc4f28638e85cb1ed77837b8947122fd2a37dbf6a2f7b87`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfcec0b2aa32503cec752f39c7a9b0c88eef9c3672f941e3e83f08087d90a4d`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 89.4 KB (89417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93eceb2733233ea0ba023ae35ac2b50c8272e02060ead780922c8d64837d456`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:83338b9dab02c5e892d7e4c04216af3417a35050a3c6a89f5679c02580d0fbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d211b3029e995baba17d24b26293538cc7ca7cbb4c686d90d9282b1952bd0328`

```dockerfile
```

-	Layers:
	-	`sha256:489a9f86bff40e3acd067530f627ebc463f581180e26ef866ff20945dbb69aea`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 3.6 MB (3556270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9842aa3c21dd529e05422a063872ac17852062730e02604d63b250e85fae24ab`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bc374f952257e26453ff7836ddfaedb60bcb7b8567066896a59a1dc6235eafc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33147fd5038a8f3c7854dd92f9f80f55966afc35978f38770149742f5fcb876e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364834fc8139dd37c03942d4ae776f1690a19fa2aadbf6286e0c696c77f02654`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 11.1 MB (11093047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce88d73a7e0fe050bda503e936cec378bffa4e11cf99f44f3547a9bb9550e9b`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042248e359b2ca8c613f492ddea03664e1f5545d422f89ca2eb579ec4fe36cf8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05b1b5889373a2ff082dcc562fe9b6c87f4dc954311c07a9235161b5b8348a`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 90.0 KB (90047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb1a6769325f550371ea3eda25df8162e96ffd9d1e724c04e9fd6a53a5b15d3`  
		Last Modified: Fri, 08 May 2026 19:47:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:38f1246a7857ae16f1ee50ce83dd99f709d82307b1ac48db4580cdd4ec7ea6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3237ed235baeb7082f0151c28c4714dc3f510674f4b363afa9a12ad73cdc2a00`

```dockerfile
```

-	Layers:
	-	`sha256:d51df37178d40b9b383e7bec1cacfb104cebafc298e749ac1e0fe3566149be4c`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 3.6 MB (3560975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fef56e4295a87c65f8c4cda5532f9cef3a17c374c89cd048b622e0afe8df15d8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fdfa585524dbca77dc88c79d28594b439056998a1873b0734100d0fbfcc4983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e746d8a97559c27eb06570b8eb5bf7fd0656d5f75194b377aaefd9ce7fea3f94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60950ea8f81eeb40f4ffd4c9eb5344310a3d3b4a3ba10d8636c3e11c143743a`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 11.6 MB (11625857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e999e91d392ae0fef15aeed6175ba39d08817b5593d30f26ef16d1565d28f379`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208859bef58c08283e7c0113598e89b5851cffe3ad75ec5cbe4f8826bba0007`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec1337df25fa89a088252f15b64bba7bf8f37501ac5944f7352dd621c52673`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 89.7 KB (89684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354222966e2e2c36cd8e4d1a765f5ce435c85024a44468f4c76ad662da8dbe34`  
		Last Modified: Fri, 08 May 2026 19:45:42 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:efdcb503bdb440864d0bfd5fcf11ce13a5bcd3ca870806e08019df74f241815d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77f0b27c9a0833de49273eb014ec6b6900a97b4265c8339e9c8422a12a57f18`

```dockerfile
```

-	Layers:
	-	`sha256:d3ca879e53a051396232cc6749a325b48a90a77b314898d6642ff4a75b84707d`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 3.6 MB (3554216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bf0aae2c3093143415998f808232246df063b6a5a9ac0bd9e4a9bd97ff539e`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:0b737232c9794e792613e2948c2dc646da73742794d05989706bdda85dadfb98
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
$ docker pull neurodebian@sha256:948a806d10e8de99412f13e48921d95a685331e685fcc5407941162c24a64d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c739e12ee1b66df8b53d57247ccb7d3ccde3a9da7ade4e337147027212c8c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb0713476e6838e62fce3e969ddf9e132bfcb3d7e2381b96a3e6590bea17355`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 11.1 MB (11103472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8c97eadffb1f79f36461db289f9d13b34abe3b10d6b2212fb7cb568f87c88c`  
		Last Modified: Fri, 08 May 2026 19:44:17 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb74a3e1d476d5675ca0b0ec9c21c09ed0ceb2776c8b0b4d9f6211687d86722`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19972676d50f6a3f1df56d9a06783980125881e306a22240dffb30771d4c04d9`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 101.4 KB (101405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ec6f6d915f962e6180edb45f9e2b0ed07d34d1a406ca966444a00063bf5c0bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e318efab8b68b3a161ff0ded8b0cbbb53f5f184fd83aa7308634335aff71761a`

```dockerfile
```

-	Layers:
	-	`sha256:2e54cd4f6b03da76b043ede7315e1c5f2c6bee9f880f71566cac57f4127ab4b8`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848dd6c010f74e7c1081c9108123e2b50de591b2f2cc38e0e7e07b7bde117f73`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:62347cb324bd70e5569c022cf36e136aa8e826f40f1c2238889b719f8cc66a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088aaba085173fd83cbf817a16c6e4af04bdc9ae9eedb10afd7c44e3489ddef4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49da93cc2679b1db042cd202e875060e5e3220e87732350bd5904898892e8b8`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 11.1 MB (11109914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825eee855070f51dfefec4cf70685dd607f1dc1402855869b4bbcaf7b576135`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3209c067378d18d75a18203938000ce323b7b747348cca016301c372c516e6a7`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c848bef723aca7f046b18ce448a4097239a1da120f540e52dd1c9a68a4b31`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 101.3 KB (101279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4243308f1b786a75f6a0506780d5c7b33ac30f8511fccca56aec4dea210c21b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e762402feeb4d06253b996167883d80d3641bf9e0680cf01273d11c016d6d5`

```dockerfile
```

-	Layers:
	-	`sha256:b14f0dcc1c2ef0142185e8793a6e22f9422570c4ba9d2b6abb2cb7125ce110f1`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2aa08681f076f24ce71cb639cc4949a46b91a1a127541e91c515a501664465`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:8008767bb706f4c4cb709ab5f06a757d417059201885cf55e86abcb4cb6dcef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2c192eae3260d4134a76b7bfbe15ddfec137154687d3fa42db1128cb0fe0a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e381fa04b31e7bcb9cbbc40e4bf2902f0c275db7edc7b0462ee8936db48315`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 11.5 MB (11502397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ab2eed64c3b37a86ab0b509b8f661cecbf7b66e171eaec9e5c546fa3036762`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a997cd26a4c569d5d64a9da26466d3c5c487619a3e32f1c97969f13fa616a`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3596ad0c31ef351fa9a9305382ce6d40415c6c0b91c7298614f295de6c8582`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 101.3 KB (101301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:42f660d3785330ad3907a27b2a3014a5478c77cb6a2ae7174a586851e2a97d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f329d1467811d726f323694ba1065308a4220276c10e46100ba962ecb9c53f90`

```dockerfile
```

-	Layers:
	-	`sha256:a6c78a26c8ba94bd4d662a5f8aa1daccf0739185d688ddd88ead6c3050508785`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad96a7377786062bdd01bea8d0bb1ed027db71956b280c297a74b774fa1ab0db`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:1b2d3eb7162fae37bb54559c3bac058da9808476b1876f6027f94729f0fea0c2
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
$ docker pull neurodebian@sha256:970c3a6ae528525bb1e8ab1ec34a277265ab7d1abdb574832d47e7b4b8c78959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3cb5553e0927f86dbaffefdba643cac55d235a4910d2d479e673633f35f833`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c21a08615a577f1cfa9ccc4980ad83b9af3be6520d08499173bfbbb61cc28de`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 11.1 MB (11103504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa6222b3a12994a0a3d2d5aa4e59b93806764f67a9b46108db2375b92572559`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3439e15c014b6ca69436cc53714a5a12b8c82d212bba1d8118567a3fbd3d26c4`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1712a4f29c136e1d7c3f29a70419828d6a06c4f8c0bd8aa2555a88172fd1f9`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 101.4 KB (101392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921683cc3659083392b4ff077850901d45c2fac00ad861af8966aae15ec5a7d8`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:80de42a461bdee72a6de0d2d96c33b96fda58b0f709ab38dda5fbda0dee923d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c6e6e38805523120e40167d506fa8e6fbb1c80532580e72d86225e2ef8685a`

```dockerfile
```

-	Layers:
	-	`sha256:ecf8938eaaae846b52eff960911e1aaeaeea774db94fa0d9270c7ccacacba99b`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97ff8956eacb6b69eead663a90a02709ad62af7970c98817fcf8310f3c26185d`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d72cd51fb944fbeefc59dbcfd9207dd62d6b1409175dc0b62c30c20f9723340d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c72a73a81907cd10f4ed9d514fe1d0c96154b13d775360ec1f4e578b4b7c08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4d4853c366ae1d8a6092357fdeceb46f1af7fb6971f30fb5bac64d2816093`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 11.1 MB (11109872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860e8ce6527c5e5eb574f904941f9d5fd1ac72704eec1e19c9667591571cda7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407a0ee518c92a25d491c4909ce3ed0cb4f84524941a201a7cf2bfd943c1ed7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86985c6bd9a382f6fe79e55952fe846b9dac4b331da91606603aeebec797fb71`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 101.3 KB (101294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a645068ae63614955aa0cce30edd178a25de8ca2dd269f25af6a34467cb6d54c`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e79ba75ecd78047e815efee9fa2ef478d94689d9d1ab9f20fb7ba7bf72a022e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aae72f0e29b5b3a88976fb346afe0082117da0014a70001d64ee3963b586eab`

```dockerfile
```

-	Layers:
	-	`sha256:97a48df79af5e64bcca963ffbc0947249e8e2964559cd3a0216d0b5fe3a662f7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ecf2ecbf82b72a416e1ef61bc9ea6fe75d4c000ee213c306b6148414a9521`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ded0c9f44bfebe4345080e2a4390c3b4fed39780d1353b24e811e6661fba9ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a59c5ac3b1631f24b5bc8d5baae5bb53973e1d0f372a2f088c0314105f17e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9627add8f31e74417d79a305014794f3cbdfc718e75672d32ef679cae4d543`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 11.5 MB (11502376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fbbd060166db850453937acb417b1629ded3d89e8f175047d313eb4d4ea249`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bda2e809eea5007777365a49ca07551a25dead0adc7cab0981a605143ef59a`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f25d850d54a1638e683ef541be2effa3bca6c0b42442affc13c0b580347563f`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fad3e9fd8287dfd51f1b9399e6918557a0ab780529cfb43d95f377c5871ffc`  
		Last Modified: Fri, 08 May 2026 19:44:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84d520f83be769fc2d681e70788d29039c5cde27701f289c18e4bab929ce8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24962661fd033444e442b5d8f8a4cce6aa12e5693c6953d7f1bff736b34e166d`

```dockerfile
```

-	Layers:
	-	`sha256:423513329c10f41f709cff6f55c81130aebb09ea250c3f3d837102c1163b7fbc`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4f37060f92539dd9a20f74d6de85a1f15bebe90d992329da9927373d4af4e8`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:936d6b469fbff5c8a402abe66b09f4bf64c61a8c2f7b9f929bf555bccbdd3fa9
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
$ docker pull neurodebian@sha256:bcf81a5101225a7cd909074ee0d0b3b0edee6f32ade3caa814b5ad284f5bf410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e56c3919c86f15faaf5a11a91cbcb6dc32337e086476aa1eefebbaa987adaf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ec4595a3d975d4fe1463c119991d3b97ea186dfdb9beaffbf86d82f87256`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 11.3 MB (11273409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ea247c34b90330172a7683ea0e1d3552d14a478c597b3835fb3f8dcd6fff53`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bba4d323b5bde10a427f41b802e88ae13e2502d12a6f71543f41c638086b13d`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1983b6eced4bb9a5a3435c20a0e80be0f95ec3298d68729b3e3d51442d6e8c2`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 93.4 KB (93386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b30d613e90e133607300246f61900aa635e8fae8b149e443014a815ac31f051b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e08651d25a04d45e850bdb93958025e7a5be0bdaf86f2425a902274a9c636c2`

```dockerfile
```

-	Layers:
	-	`sha256:2db9e2cd120b4ce9ace4b747159ff3a6af43f8835dea224090629d18e284c24f`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce89be306770279efb86a1ccc18a50813f0663a5fab4ec216c7fd2e419529bfa`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 14.0 KB (13963 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c383b1c8bcc59487007ea946c97be72b381f54ee51d5fd892cf0629fdeb1c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628c1e90e3da7350faabb21fc74a0c88da8663666dd19dbdb74ba907e12ef2b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbeab365177c9b941a081ba0b6d957ba147319fe32dff22aa2624a53a06f29b`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 11.3 MB (11252933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fa205d0d4d9ff7d136faa66f376fb23aff6334613faa278f84518f8e5c01ff`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14309867687b534670e51c1d96567476c0f1aaed795f789d0445fab07399b4d`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89033d9b2184954874f8f00b5a17aecc6b429a80a8e0038b84aa6ee81ff3383`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 93.5 KB (93546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ede2b6186f52eb37d412780815c7330d58d6faa9837786a7e5c79b52f572fd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ee394c617722eaa31b6265fd68e7ac215a0a018ff4f39c2985bca8c06e3347`

```dockerfile
```

-	Layers:
	-	`sha256:d4b4657e224bc234c23ab66a4c0a2fe772e905a9fe22fae905f739583d04c417`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29aedf8be25ddf5a7975ddb70961e5bb9c8359ec72bba50cbb2e61f0f256a671`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 14.1 KB (14088 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:4db04057176b65f60447ea0de14d71e589435efc93f5f9e0942650cbc343e201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d0d6bea08068fbb0f25ca7e55202dd93371d5e2f960b095b57d73b56802257`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb9739c6b4f68bc7ceda360ba82976ffea2a2b0f910162f3baaddf10c30baaf`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 11.7 MB (11693065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d4aa3bbcd7f103db531b544aa469fc669490bf0f63070fb63340476b4b2ff6`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f5291b6f5da64f52099bfd741111dd36b90a2fef3af20ec6d5cc367da8d4bb`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea8274562ed42a6906cd9cd33a459780630e229f388af5b5627ab5ae06b749`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 93.4 KB (93437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e167ffe5ba168b8cc58cf782364dda325b14826d22b80241ce109a8f1f87cfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c80c7632358c017feeb7106b43d3f8a70130d34fb57220e3a95f07cf348c3e8`

```dockerfile
```

-	Layers:
	-	`sha256:f6175cf9e3596d080ca37a17bf2e4e4756b45b06df58d192cd2d34c654ec1021`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e857221844e8f6652439e116a12b9371a11d1e340573ecc8b292cf063c8552`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 13.9 KB (13935 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:9301742359389f2d2738c1f6decafb303e83a33da734b5262947586e3fdba70f
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
$ docker pull neurodebian@sha256:99792aa6ba989a7415f0cd2cb8e195c8aa99bb3c897fe33a7bf5c35607c275fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517d328014a4be6f7b02aa9d27f2bb76abc751cbc7e0234bfbde2239a7433a8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157e5aa142e191f389177cafc25663cf3ead7455488e9b3ae8d80faac203470f`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 11.3 MB (11273453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139c6137c970e0c7654c2cbd7329fc30bb23de4da7928a386b807149d6d4257`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eae6607455a450e3b7448918a266a5499f18306d75cae839cf0e46cdac78678`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de341e23682505074c2fde67892b0004b2e62d8351a93b78e388774d57c92afd`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 93.4 KB (93413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2970b98df9f5f093f0122c8c3983b1b6e87287a424fe66b37b04e459da79b8a`  
		Last Modified: Fri, 08 May 2026 19:44:40 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:21531d38e6403bf24665a621472f6c8082e62fa42aa9ae11d4bf72ae1bae6da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4593617393e092d54b447d141bc3d9055d3dd3fb0bc63c086ec490b43db5eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a5ec5d989239fca2a2f74da4290145a9fc4c5111be3458d332ca6523993ba972`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9c958dd7a81bf5555df9c02b20af25ae3d95a6fbc3d76dfe60c15f229dfa70`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ce456a29d55af753754c81bcf6c489b588e4ef8d345a25a1185ac4ed38d7067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83671130319d212529fed9657df2275a72b7a9972a90c7d4eeb3087a8c2e780`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297af71f398d804e9824bb6964f5f84de1d86338b03a2c087345a9e6adeae9e7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 11.3 MB (11252932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbc6e93f45b3f4cf455734139898464377b66e14251b76f3361f3d34ed49b9d`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2bd671e957e80374283f5fb64814dafa746ed40e7cf68d7972fffd7054de17`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c4f363214c80dee9f62e6d8d410c16b88764ef3e641e1d8bc9231b3d9cae7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 93.6 KB (93575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1d2f24bc5c69d6c727ad3568cbc4addea466c9b6cc928ea044b626717466f`  
		Last Modified: Fri, 08 May 2026 19:46:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f29b6635607465a6f03d6780e7c09679fb49ac9bb340deaae75b283f8ed832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3acb1d5d8d6cb02f7c1e8bd1cb80b8eb98d8808fa839c362abc1fbb0ad92f8`

```dockerfile
```

-	Layers:
	-	`sha256:c992b9778cd7c443812a6eca47e360178d13695c8043203be74e9562afd8f30e`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5d86f16916b238e87145c3058d5b9f4308cb209db7450c1e9f13152f33e5b9`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7bc7df072b8d4192da532d04d6fead4b1e24bc92dc244d3039bd8a47c37f53fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3f5e69332c4e42d45a5f556b5626d9a922ed8e3e5702c07d3e8270f7a02cd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fd686c2be4701aa5e99504e0a0a231438cebab31803f9703d4f2817fcfaf3c`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 11.7 MB (11693032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c275dff193370be94cf6b05afcd2f50b992d61b429151ede147e0d16bd143`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed34c26dacdd7f022ad39094d3a0e7234c0e1adaf272d36639f4a548d0bb34a`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed24d41000306ac52cbf2623e08455d064489dded03b85fd01bce6bd72a7c0`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 93.4 KB (93421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c476f9525210c69f52698c6764a1dd93f0e3c72cb3941432ffad0b4dfe7ee5f`  
		Last Modified: Fri, 08 May 2026 19:44:53 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8707a48f987ea14bd078ac3746d28881d4119f0480d7627964a7d15c52545760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7f5ae92125a30eea36bb373c2d4ef882b6f6936fbc0adf910cfc3e2feec4c`

```dockerfile
```

-	Layers:
	-	`sha256:f5e53c43561d0cbbbb39a871b900ba903431c52a26c9b7b5d743b6635d3bfdc9`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6d2384fe0ae77451cec1bc567fb85d31e77c7b721f8bf337871e4e30ebdf90`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:7d615974d7618624acaf024c794146f6955178920e4a11205f0b463c1a903434
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
$ docker pull neurodebian@sha256:48409e2266289921f625e696fd82ae75b3dc7d3429568e904bccb3046e022dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982b441ccd68e375ce55850b6f2530e35f89c4a858bb75344fd7a5dded7d5ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603e83f84352e4d604d1ebd2e7b11a116e1d73c815b1f21b71c35cf4d26a6adf`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 10.3 MB (10293033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9841317468747bb9c4d672ac9e22fdbaf7467995b3009c013af9504275765`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97afa150b5dfa5f4868492e1872f0bd5d68742189b24436efcc83edb5b863ad1`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80469e6eba86735ca23d5fc2e8e6e31019a42fe3e7a96b5d2580cffd3a1892ab`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 90.4 KB (90409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93973523588868a89ea7a3048595fc8a05179b43bd1a791ce32770712d00e9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3739871772f9c6753eab2831cf79f90dc38c2a6030448f67185547885e75dffe`

```dockerfile
```

-	Layers:
	-	`sha256:48c1c93d4580490d300f49739cf9b99e4a0678b32abf78a80898f5033fa0cc82`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a980516244bf1755bee0e5c4047d7bd22a6645fb62f256893244939631312c4`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d503ee17e4a04127673e873eadb5e238338d8534e69de76f9a2834dea00068f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d388d64eed3a472d75c0230a0f7e0ec18ea76b7a49cf2f265fc7b87ba9fbbad9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c629af507dca062ea56f93574fa391e844b4d6e1b5cd11cad63be92b46a1d6`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 10.1 MB (10078011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abab8ca898857514fc5bd463e6e97a767bbca2cb8aea60e359cd6acaaa15751`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a787e0f5c6e783915e7fc9afa550e0bcf87b812188a88bfe09536d428841b0`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac226701451e2fd232f7351b186bb36b4f7e1742f26e18192509106d28c45ec3`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 91.0 KB (91035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dc047d2f30ed6ac4ec61cc1afcc3087048f8b38a8af931444118db41c4d4566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb1e88be3ddf79970c3f161eee07195b0acfc24a53e5306704d479fd7126a7`

```dockerfile
```

-	Layers:
	-	`sha256:4d576367898d58cb2af04ebc67ca27c1a684572a74fe8c3a8c3fa9d91bb20031`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349d03efc82e58b0fabaeba13d01e95372d1322c71cdcb42706cd4ee07d99898`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:674b7f113ab98f457c90a5407cf9fce5d326c1ada9d335c3bb736dac15df1d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd893df613b6c8c15a740d7cf4906096d1c477af22aea43f2c1a7965c5c10b95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918b15ce42e2f43331d7ca8a6909c2f318788178997f3be2a6c20d15686eae08`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 10.5 MB (10467078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d8c3e17a2f821d9a1e4a647dd71fd281974066ed12286ff5344c3c70918add`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745c310d83150426f135a032fe18cc82a8e5631e02d97a07354f8c9341131d6`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d13836b8f7a1419799c27ce5e5586655df8273d6004aaa0c492b5a99f6622d`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 90.7 KB (90733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e4dfc7f492836cce5f36a3a8e3941b8d6619c004fb9fb3e8a3df42c8c567950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911b218b44e62288fb317f239ec58d54680252b6ad5b7b84abdeee0eff2adaf`

```dockerfile
```

-	Layers:
	-	`sha256:b35285063f63c97ca1e2f1b58a75539e178f06a4277ff94135e31ab43d844d97`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be65c44927642dbaf0443b5d950bdb2eba7e045ec2186605bd5528701cc1ccdc`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:b44b5529fabf774a6953c7810dfb0a7becd318d5e07cacc59b1d5f70b3e9db13
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
$ docker pull neurodebian@sha256:4ebd736271d09525672664c3c407e4571dc1b3e4b5456c2f9f1cb57cea432da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59689076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94042a90a21d39fa810f29af2dbe6e9e9e6acf8e9d4d4a0548c07e815ad85df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5ae048d466c70689a7edc5eedf4cf1793ffee4a9b646f2c5582a319d9f8feb`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 10.3 MB (10293020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f3d32951cca7431a1cf21e1aafd0f0fe2b9862713fc19ff35fd5aab0770fa9`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0afa5be5588e323635ba7e46523fcc7d695788b8c883106495ce8fe959cbe0`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d615a8943f123da71966af78797d000d0b087502770705ff702fa8e4d72de499`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 90.4 KB (90383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d1b8a4db5664e6ee8564db8b48db1e602ff4076af3e42b0162ac45ced4d869`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:988cde20d5d12bbbb0de2df64351abef2e21260c34d79bbcac811dea876ef166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c96707ae5af4e3a90694b82d76bce82726327aad21d64f646e786b574b03d1`

```dockerfile
```

-	Layers:
	-	`sha256:97516c0a52ed039e6b3094072fbf6966a275e16ead77e38af34979e8a923b720`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:100674fd8708b6042e678d39193d51e761bba8a6a49fed4f4aceb77bb7f8f5f6`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57b13c1e50963a6187b7e20ca9c973fe30970f06aa206a968c81ed3e3aea7ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32a80663dcc17719bc1935a712da2852657de51fc94f60eaaa9ccc05276764`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77348ea04670cc60ed3fd70e8a942379a3a778401a47da14bddddaedbbcd473`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 10.1 MB (10077993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4f986dcc8620c40bddb431aed2820d258c0ba86a933a572cfb5aea1b7c8d1`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484764866e70b0d12ffdf225ed2ef6dc9af0cfbae6d1ffc072bc54f2bbd8710c`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13df355aa2411e3cab96fecc0b4927c1a75301419531a535765c87be27bdcc72`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 91.0 KB (91046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb102d2bb0e4b299a1747924f034d561048a35b0c3ad22fb08df099037f5e1e`  
		Last Modified: Fri, 08 May 2026 19:46:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a7fc429753a5755b5ee64226c7038ce723951b0fe08eabbc3fba8e4a1697e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c66c6f71d2cc072b4de445c3593012348006787233156dcc732fecc292ecf16`

```dockerfile
```

-	Layers:
	-	`sha256:4d3e70240cf4968ed03616db1c20e456abae7c75f133eabd39d8fea05bf2ab22`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac819a829dd4e682388cbb13c01e4c3ee1c2e11f1c959436f84e286ee2fb631`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b75946ef52c181c76c2e00440d05d0622edfe6da94570e49ddae38ea079dd3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b263265c43778c4c1b4e8f75212dc86f2c4bef41fbb14feea9119600cafa0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4a335a9da7e3093e947b7d57025190b5739906b8bd558a221a15ddf6aa9ee1`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 10.5 MB (10467127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b54ccf8ac71030c118f8ef845986b5523b82fed115f87119415e7d8cc6a7e8`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfaab1b9dbef7720bd0084cf9e3eb661688ece913432774491e5c8964364e34`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a31952666a61c2db472bc221ef5ccc404ecc5d08cea8a1059c7cc6d24e1f2e`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 90.7 KB (90749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a9d9d9e1e36df62b6a57b49fb8a76a463da0ead6d8b53ad51fe669976c35f`  
		Last Modified: Fri, 08 May 2026 19:45:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2acad64ea16cc709a06d2a5aee32e9877e05ebb94c5c760a32e21c3e45deac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a59f41855cbbd51dc2e3c593cbaa8adf474717a361518cb3ebb5186e2b4760`

```dockerfile
```

-	Layers:
	-	`sha256:0d1f3edb3bc163776717dfd578079bce618888a806181425e93980efaaffe421`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cb1f47cd785673497359532ec8428f026e1c4021584f5b6423cb001e8a911c`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:ccc940c9d2313a988be650e62fa8fe32896169d7166dada433cb7577c7127b92
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
$ docker pull neurodebian@sha256:823eba2bae9921e5463b6eddfd83ea6ec97be637f27393c7becd15416cdfd2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60076903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6453d6a4685ccd2fe37f542bcf9ffc8d8d1d85e846201edb41d98468372ca394`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:44:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e929ba940bb6645aaebb3cf3e1b30d0ccaa2f7d53cb82e57d451efa023dead7`  
		Last Modified: Fri, 08 May 2026 18:23:00 GMT  
		Size: 48.6 MB (48622043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e894cb91c5db397e5c3ebf6633fc5ebbab445f65fbdd4935dec5f6dc43ccb8`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 11.4 MB (11362509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d43a67b811a859ca589502f851db11afc79e31242d643c4eff5a05f7e633a95`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd467f5800893dee759399c43bc14785cf96cd9adea98dbdfe2350dea8708e06`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9326cf6c59b1d22ee9d0eaa828b37444e375e7416a42afbfc0efaa1ab04b62a2`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 89.4 KB (89447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fae01ebd151036016f748add050d543821c6787fd1c8c202f3700afb9c388c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af742fa40471c540b7db0eda1d05cfacb054817217b3e40387ca666778dfda2`

```dockerfile
```

-	Layers:
	-	`sha256:677cf0ab5038da62decc38492ba5f7524541156fb4ae31f22a283b7e62b46d99`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 3.6 MB (3556244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551e6773ea14d7cf6411fc65fbd7026c699bb5cba718984d5078e0fb08b69de8`  
		Last Modified: Fri, 08 May 2026 19:44:54 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4445a9b88c3aba497a2008d7c26ab7680dc4cc162d8bc18e7fdd2abe797929b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a6e9a7461b3bd032f5da0f32d43b6ef28490fb1b2a094321029284aea38845`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38be54f67917d094862e34ed83d9f5b14050260224cc43c64865734d5907fd67`  
		Last Modified: Fri, 08 May 2026 19:46:46 GMT  
		Size: 11.1 MB (11059291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc2a856e734427e804ed50a73e236f216b87a5f0fe32affedbf2c2fdb7e367`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb5943e9f00792ba990c85877f68cd02fb0f955ac2c056c784d0a7f5efe7b7`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148505e68f723384842e9256ab27a20502fb933a703a02c8a8387a13fde81fa5`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 90.1 KB (90057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ffe6c1be02db912c32558802a1cee4640d3337a3f6da771c03c12a11baeb264d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dfd5864f60dfab734040f18b26d324ec7edae066ea58ce1f03dbf96587f3bb`

```dockerfile
```

-	Layers:
	-	`sha256:750cd9e0c7163f4d2f76ca439df028cb8f7e095be5f57e672cf6e8101639d6c2`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 3.6 MB (3561592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b03532524e5b66cb48a0b22ed5257ca466acb5e304ca5e4b016ba269a51762ec`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:229b368a6b98d7ce660433a55e8b2363a19a2f808ab9c873f24b05b1a8a7be84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61605870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075291128ef3150dc12f76a862c4d327c51305f9d2d92705a276cef92e88d3be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fd7fd52239cf41c1513003560316f753d3b29bffb106c1c8cbf260e58621e`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 11.6 MB (11589003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b51446d80054a5f43c4ce780e4dc27dd69be5690c5515991223b5af7a9fdb9`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39c1cdcded0b2bce400d9caac28b0b5ddc7273cc5e5c057393fdcebbb9055d5`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3edebb8be1094d35833e792183bac8d8b69a4cce9b1de1627b384fde68c22b`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 89.7 KB (89744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7585901b3fcd61be98cc07c0fce812830eeccbd9bbbc4c73075927b5a94c6ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b2de58ad6d4212e7b4a3044a392c77b1cb7b570cafeb9b7a95c08097b9b83`

```dockerfile
```

-	Layers:
	-	`sha256:a5e656a37608c6c496bbc4e3f21f2e6ebdd0ca00774a6b5e42196d97aca1ff25`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 3.6 MB (3554190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac42095d0498fb668d35a1880cc1400381b34697805a03ea4a3cef3243668e26`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:cef5a7249de9c877b5f697fa3e104454149bcdc02e814a22d09bd463bda75f31
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
$ docker pull neurodebian@sha256:5226686b3732483477cad20cd6e322d9998a4bf932871ab9fc2f87848d7dad60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60077340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f04cff1ccfe79e7383ead04f269d7ec790faa2f6c04d69c1c31e94390981c27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0e929ba940bb6645aaebb3cf3e1b30d0ccaa2f7d53cb82e57d451efa023dead7`  
		Last Modified: Fri, 08 May 2026 18:23:00 GMT  
		Size: 48.6 MB (48622043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631bd401a9ea85121899c742741152c2d753c20f5063b4935e5677c9b9bb941`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 11.4 MB (11362517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c5849b7c2876a6e27b5173f8d1e8f02d5fcd243d1dfc50b858e91b67083f22`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a5f0d6856a2cfa52c99b2c2ed11dfd8851eb14b84b636b738a49ade15c18a0`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9758222cb4c90ec2c761ca114b3db8c018b0d6b65d329a9f50422fda80d02d31`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e2980abcfd428f39d3236270246d8a542601ad7016f6a19e3f33ca6c13b26`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:51d3b372a86f0abfb8cf682c3f299797d0fa31e061849f6511133bfa2430f687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067694b030e0ad0f1a824f2d5271aac7d5f509e60a64cb051696a7c62e671b9`

```dockerfile
```

-	Layers:
	-	`sha256:51c0f2b8c73138f5a50f5cfb4cdb5f94ba792bf7099a8cd6c1236b12edd975e8`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 3.6 MB (3556280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af51c446d933ca99eda664c827ad478fc09984eed72ce1e7c5689ab96396f57f`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c5f596c4bf8c0ccc478841c47092c4a4dad71a015d664685dc1c4b96dc058b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9528113b20964df2f7a7b1284f55ba0993cab2d96ad5485be40a46fb10c581f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be64bdc407e7e3b95b79a3ffa508782d23c39791fc66237b6b9ac0079e6f8e5`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 11.1 MB (11059006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a038166bca6013ff60ba5efd623dbb4e5fe1ee3d4446048b568c45cd48f1f4`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc2ed7a3a505ca3103c47fba46d5e291e08d49ee72ba39dedef20b1008f326`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a68e5868a8cbc24ca18677d15c10aa94f4c51fb3e1f19e418a98acd77848b6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0446785ebbf74532dcba92825c6decba78dcf6a16420b18506b2ed57f7928eb`  
		Last Modified: Fri, 08 May 2026 19:46:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b0d5416b6794a636e42304fdb74a53a9ee53950b35de114de8bbb04947b6043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bac42a5873dea8825b57dc7136a3a27ca3ab5b4fcb1501abbb9798be97ed00`

```dockerfile
```

-	Layers:
	-	`sha256:24443809fcc31ff23bd314ca750f0f95a8effe8849bd1131390892d2ec92e5a6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 3.6 MB (3561628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a27081017521680b89fcfa70690d05d07b6f2c8103aaa1557dbe8917649d344`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:03a1a328bfee5ff0a2bcd6a694bf094d95381b9b663a843aa2e3ae99924b758c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61606220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c3c7ade491f697623eaf25c70f50f5a71cfb7bb1d3153121edb8caadc6b964`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a99493d96d6f92ea6d88890fe995d3918a05c9baec0b84c6e9d10b95007a82`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 11.6 MB (11588918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a0c33e147fa59d9124cbf1b02679d5996d94f20e43a0b0dcc7bac0c76d9bae`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a895ebfb8de9b1aba761e3f5032daf08032da3fa41c4770fb7be187e4cf0`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d22eba06c949e34b02517b4968779ffafdb8e6ce52c51cf497c682389b154`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 89.7 KB (89726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2616c3f976bfa74ec623fc4792a7910f4ad8177ed3b117a8e270087f0510a539`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c75c21cbb9fff8f22041a53794d1631c30d371e24e4a25d431e1c649eb7fa77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7075d85a25976a8e3bcacbf0a99c3a51ddb29e013c5b42c7da1a973f852c1ea0`

```dockerfile
```

-	Layers:
	-	`sha256:7ca33354efa5a678e18c52598a002e0f989c7bb096e45147472c2b5788c43e45`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 3.6 MB (3554226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d2a0a43649d8f679119161461ce4dc60d130a0faefe0533fc5173dbdb17353`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:75f904d0c67f4c9858cff6f0103e91027e807518b04fe5f8092efc0c0981aa3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:50424def1a9f9c45659cd9a3c8fd7be20b771d9faf316706d56191817d0a7bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caa9f0454a8506b06908af40b3180c7ab34e543901a0d141383284031761739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e965e0cbfb28916191745c6417d4338beea7aec2cb5fd81e10dec40dd2e8366`  
		Last Modified: Fri, 15 May 2026 21:20:18 GMT  
		Size: 3.6 MB (3624588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b460ff363337b53a251fba6ab38f85ae7dbd0d322131f9f7ef3e3e5ec3993841`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c526a5517cd48bc16f89213299da52f9690296195e5ac59667a2bd643e3c5e41`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf8b1159386b1fd839b78027a3b340ad638ebceb5a5539d309b242933f1831`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 111.2 KB (111232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e412202f26ceb6d4c1bcffdc5575ef0790972dcdd1ad14eaf46f040cac1316cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f887bb03cdd347eeb92f232c6a07d31436a34375b07e390389807dabe87027`

```dockerfile
```

-	Layers:
	-	`sha256:809d99babe923ab2dd062a2f570a5266b242a04c4fafc307c92fed2e3a9b282b`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 2.2 MB (2198324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdea2d028b9d02999d109dc927e7a4f4f2eb569da53527dbaa7364aabe4f58ae`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:97414ed4f59910609b1a9d705b7a3a667c26066208e644efec505f633b47edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31324763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a849cdc79b65cf626b3b9fcf4493328abde886f8144f0e07b67910f9031ef4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5439fbff57039d8111c79e00db08bd4ce15263bd5b99af9187a4bc0f4e8b3a3f`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 3.6 MB (3604765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4e64fc2883d214a40a57eaf9b537698bd2716c653c6222dcbfe6fe31ae80c9`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16947bc03ead29ec0c191d87407de3718f236783939aab991b0796802259874`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6602ba41307da6865e1f72143c4370a3e8314e6549962b23a911c4258a962097`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 111.2 KB (111196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b49ffa2049e4591c8f82f011202a785b743c0a435508fa5289cd41580900181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a7e9d197c9c0dc0a6f3713a812beb76783de250350cd4f1c949813ce36d7b`

```dockerfile
```

-	Layers:
	-	`sha256:6e35d0abb6e3a97793d611df4083460be5d8ca41a0a4a4caad1681ea6c693031`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 2.2 MB (2198584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3059046f1d26c24c93d9cbbebe2a0e41abff976015c5e06bf32a4c00ed72ba5a`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:c15cc5b2609215d38f487ca74d9a0c364fef640456351786ba6ed7ddbdbd9e23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:741e4d235640395bb69af07b20575215e3726c3a51b342d7a6ab63b03f542913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d070a1b4367810c74bf7fd5297d7c2b0bdf28bfb7bf8fb1d2f140a7477eb6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38cc2da34443ee698d2fb5746eeb70d00d8cf9832f5c179c94dd01d32a6c322`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 3.6 MB (3624605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8de9718e2df29fa2d76f88c5bdf5a5d1c67dd9cb2a42ac280a5a11008d6cad`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c6677ad71bba680f8167c8974b73f8286635b51e89d7e59b83165f5c783e4`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815bfcf7ec7f087a70287169d800d287b5168932caff8ea06f75959b47451481`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 111.2 KB (111242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49aaddb4c43128aebecde25753a0bb923ccbf5ea00aa45045cbaf373d236054`  
		Last Modified: Fri, 15 May 2026 21:20:21 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:81dcf4b3a3c8ea4dc21201c4b401da4547964aa00e40f97394136dfdee1287ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5876d21edff0cea93eac4c36709504c4935003c3b39eff6d3fcb78e2c01670`

```dockerfile
```

-	Layers:
	-	`sha256:fea8fd6c0a0c0ec27d42693017eb03dcb6517cec0badbda611767531ced60f5a`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 2.2 MB (2198360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30444ea650f022aaa5e6707a1d474afb7a85e00f07e9dec8bf133305f85eb69`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ebb7a5aaf051c49d265817b4c21a8f3e1f4340caa4351791250395b45a1daeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f7558d4f7ce8272783cff8b620052a1e42f297365702f22fed127d8fa014ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfba9082861e846762690f8c9061bf0b330a06abe65636c2f7b0cdfb25816ca`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 3.6 MB (3604762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eec572cc90753bca88496df6fd51ebb6a228bd52acfd45bb858c247fe34c87`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6e73b3568c2e79fee913e8fb0a2417d91340fb6ff38a5a55fd03819c0aa86c`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254233f274bb3fe0fd62162e9a7bd9946f215e74774b49e235310bbef9e524f`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 111.2 KB (111186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7e707bf8653b57bc80f5de25934e155b312dfce4cc4e3277a8dec5b82a3aa0`  
		Last Modified: Fri, 15 May 2026 21:20:40 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:02916722ca03dcac193f1f622dfc12e91bf090281b8072122d1ce4e2b71f5c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba93e33625286cae36e90a26e761bf14cb9cc9a67492eb5aee053c0159c1beeb`

```dockerfile
```

-	Layers:
	-	`sha256:81747f061bbcb86cfb76d061f8c57a6146ba8174df02ef5a65b960be9d7224d6`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 2.2 MB (2198620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb84873f4648ef88e059c7ec03f22b542751d2dea12d0f148bd6cd60c7d624d`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 16.3 KB (16301 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:c9591f4172a58016cea53f10633f28c9a67eb0c4fbab204e98458063173e7e36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:1518613179d554ee395421eeb519425512ab078a24ce559713b4606e857cba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc43d80b9e552ae205bf50ff50f0113b430ede2c359ed52f3a0d2327df2f493d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91080953c2acbc96d10fe4828cad1bc2ab4c82db5ad02792fb933f2f13d70499`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 3.6 MB (3564544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da89c7f3acd4423e93a16abf1489589f3fbdfcdfab0b54df625457971fef8b`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650122efd7cf995263806f1fe9121463a523a5bbf31f21d00c0ba81d6d9fa7f8`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ce33ae3d4d5119b02d4348559779a6077a6bb3619b38275c043e5ca34fb175`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 104.4 KB (104395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c64c241bf3bcb286d2669479231d7b5953479c2b33e5e0317e711e845b82beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43acc54ca15fdaab04e44258b4027e15d888095aaf22666a598513e7f21a7aad`

```dockerfile
```

-	Layers:
	-	`sha256:aef0071be2d264eb5d2f4b705a5ea4f2c3c964edb559665e113daee604652134`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e55928452738f82644f08e8558fc8b565f25553a9a422a68775fd846c39d6fb`  
		Last Modified: Wed, 15 Apr 2026 20:46:20 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0dbeaa0754ba2cdcb516d4e39a6416bdf4b7da10525f24b49a61a5feff148dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32545705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7e10aaa4b0b64ac0c39126ae227a9bdbec863342e509b369c6be2f8b82be23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f12429cade407731c202b448c703c798c9843ba5b9efa8f1a25a05dc3e8431`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 3.6 MB (3561756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0b0c76a6f242383cf184fe0f4b6508ddb63d2551c1887ac7ea459225396d5e`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6ec1313b41e7c409808c452fe2ec0303a6c067f2aa660e1ae358e5c1a81a75`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9641397dcb223d6c745a891cfd688294dd62dd50c7d4cbe7a43ff6cf2263a9c4`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 105.3 KB (105254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7b321a66d15717b3b34d38d2409b7da87889dddead7ab790a2e96cbc6bb4ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c3f02ab98fb8ba900768139bc6cce9d405d08fd7c739b9500102dee1c52ed6`

```dockerfile
```

-	Layers:
	-	`sha256:1a33387cf012fc9bb15766ae8a05b79ea4d5bfad8dde9f4fa45bf81a7fe88da2`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697097c5075451332b4cba4f90f0e91bdbd2283eaf06a606e58e535bbcacbdba`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:bda267ffb25655b138791cdc439402237cdd57fc240dbd1ba48fa2175c635fa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:753f04dda59b30f6d474a02368db6d4f6a878af353dd81f4e2d07514311453f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33405189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a23d22a82f9e7a0e1b7fca068649af2b195d7bc4a3444159e8f9ee151c4ffc7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614a601681e659d79f5c69f0390c48a36c84a64b92bb8e53e4358eeb0bb3eeb`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 3.6 MB (3564486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa5d8582b88e334628969d6d48b2099e0a7a8bb3d62fc00fdabf16f034233a5`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d2ac74681d70d35cdcf2431d8762c164f671eec996d2a3dafa98689ac83823`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f39a48763b024b1a23e5214e867803863840d93086632a2fb92ac045daaf4dd`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 104.4 KB (104383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa07982c3e5c85c7afbd286cd46af0d532c819440627f7583bbf701ca623087`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72aaef1b785221a079ce03cca78c0bd381d9afb9199b21a165a243f2d21eef9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8d96813bdf0095b63b0700d9b6a14bb56b946b99f400d0dd3d55a92d9cb06`

```dockerfile
```

-	Layers:
	-	`sha256:d47849cd84c0097cb2a3418c558e81a77037bd392916aa7c14f7fe2ca4574547`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 2.1 MB (2120925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:511bee88869cc2d89ef9c1b421317dc586f9dca84881109cfa34b8979f0fb982`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:291bc47a26a7b51a80ea7ed02233b7699565c12c6d20a912a40e8d58045ded22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0877cf08816abcc870642ed5dc27b24bef2d18dbeb76c5ac2c324300f72d89aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20e0ca3ac0fbfe1bdd4cec3f984ada36b78041af894097406a8b6c45a300d6`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 3.6 MB (3561763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75275b141d7d2666df1d5d74b6716f343b5860db710efdef969380b54e00e2dd`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e077fd96e28046b9bc25a82b6c9cdb92cc2748fa320d3329753b6ea1c8322d3`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6172f876e47872566aea14fe5035b707fa576624cc97fec495aee863f822843d`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 105.3 KB (105269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30abc1f01381670ec2eed5998a62313532731d3c41ca4dd6f1b1549c601e9804`  
		Last Modified: Wed, 15 Apr 2026 20:46:53 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ff95d846cfe672fc8b83392edc13971714f0f54564c81d9c64760f31e9bf250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26251360511a41e7a9968f92c92dbf251012bede7d3744b70d46ad83d4e98f7c`

```dockerfile
```

-	Layers:
	-	`sha256:0f315ba6b52f9fc12490c58464febe57a58d57d017ce508d206b02e88fff432a`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 2.1 MB (2121970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b7e6de6c91d5088ba7363653354f5f14eb64acabd62b1ba1eda4cf8c9fae44`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:c9591f4172a58016cea53f10633f28c9a67eb0c4fbab204e98458063173e7e36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:1518613179d554ee395421eeb519425512ab078a24ce559713b4606e857cba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc43d80b9e552ae205bf50ff50f0113b430ede2c359ed52f3a0d2327df2f493d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91080953c2acbc96d10fe4828cad1bc2ab4c82db5ad02792fb933f2f13d70499`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 3.6 MB (3564544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da89c7f3acd4423e93a16abf1489589f3fbdfcdfab0b54df625457971fef8b`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650122efd7cf995263806f1fe9121463a523a5bbf31f21d00c0ba81d6d9fa7f8`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ce33ae3d4d5119b02d4348559779a6077a6bb3619b38275c043e5ca34fb175`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 104.4 KB (104395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c64c241bf3bcb286d2669479231d7b5953479c2b33e5e0317e711e845b82beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43acc54ca15fdaab04e44258b4027e15d888095aaf22666a598513e7f21a7aad`

```dockerfile
```

-	Layers:
	-	`sha256:aef0071be2d264eb5d2f4b705a5ea4f2c3c964edb559665e113daee604652134`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e55928452738f82644f08e8558fc8b565f25553a9a422a68775fd846c39d6fb`  
		Last Modified: Wed, 15 Apr 2026 20:46:20 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0dbeaa0754ba2cdcb516d4e39a6416bdf4b7da10525f24b49a61a5feff148dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32545705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7e10aaa4b0b64ac0c39126ae227a9bdbec863342e509b369c6be2f8b82be23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f12429cade407731c202b448c703c798c9843ba5b9efa8f1a25a05dc3e8431`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 3.6 MB (3561756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0b0c76a6f242383cf184fe0f4b6508ddb63d2551c1887ac7ea459225396d5e`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6ec1313b41e7c409808c452fe2ec0303a6c067f2aa660e1ae358e5c1a81a75`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9641397dcb223d6c745a891cfd688294dd62dd50c7d4cbe7a43ff6cf2263a9c4`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 105.3 KB (105254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7b321a66d15717b3b34d38d2409b7da87889dddead7ab790a2e96cbc6bb4ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c3f02ab98fb8ba900768139bc6cce9d405d08fd7c739b9500102dee1c52ed6`

```dockerfile
```

-	Layers:
	-	`sha256:1a33387cf012fc9bb15766ae8a05b79ea4d5bfad8dde9f4fa45bf81a7fe88da2`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697097c5075451332b4cba4f90f0e91bdbd2283eaf06a606e58e535bbcacbdba`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:bda267ffb25655b138791cdc439402237cdd57fc240dbd1ba48fa2175c635fa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:753f04dda59b30f6d474a02368db6d4f6a878af353dd81f4e2d07514311453f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33405189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a23d22a82f9e7a0e1b7fca068649af2b195d7bc4a3444159e8f9ee151c4ffc7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614a601681e659d79f5c69f0390c48a36c84a64b92bb8e53e4358eeb0bb3eeb`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 3.6 MB (3564486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa5d8582b88e334628969d6d48b2099e0a7a8bb3d62fc00fdabf16f034233a5`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d2ac74681d70d35cdcf2431d8762c164f671eec996d2a3dafa98689ac83823`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f39a48763b024b1a23e5214e867803863840d93086632a2fb92ac045daaf4dd`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 104.4 KB (104383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa07982c3e5c85c7afbd286cd46af0d532c819440627f7583bbf701ca623087`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72aaef1b785221a079ce03cca78c0bd381d9afb9199b21a165a243f2d21eef9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8d96813bdf0095b63b0700d9b6a14bb56b946b99f400d0dd3d55a92d9cb06`

```dockerfile
```

-	Layers:
	-	`sha256:d47849cd84c0097cb2a3418c558e81a77037bd392916aa7c14f7fe2ca4574547`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 2.1 MB (2120925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:511bee88869cc2d89ef9c1b421317dc586f9dca84881109cfa34b8979f0fb982`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:291bc47a26a7b51a80ea7ed02233b7699565c12c6d20a912a40e8d58045ded22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0877cf08816abcc870642ed5dc27b24bef2d18dbeb76c5ac2c324300f72d89aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20e0ca3ac0fbfe1bdd4cec3f984ada36b78041af894097406a8b6c45a300d6`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 3.6 MB (3561763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75275b141d7d2666df1d5d74b6716f343b5860db710efdef969380b54e00e2dd`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e077fd96e28046b9bc25a82b6c9cdb92cc2748fa320d3329753b6ea1c8322d3`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6172f876e47872566aea14fe5035b707fa576624cc97fec495aee863f822843d`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 105.3 KB (105269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30abc1f01381670ec2eed5998a62313532731d3c41ca4dd6f1b1549c601e9804`  
		Last Modified: Wed, 15 Apr 2026 20:46:53 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ff95d846cfe672fc8b83392edc13971714f0f54564c81d9c64760f31e9bf250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26251360511a41e7a9968f92c92dbf251012bede7d3744b70d46ad83d4e98f7c`

```dockerfile
```

-	Layers:
	-	`sha256:0f315ba6b52f9fc12490c58464febe57a58d57d017ce508d206b02e88fff432a`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 2.1 MB (2121970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b7e6de6c91d5088ba7363653354f5f14eb64acabd62b1ba1eda4cf8c9fae44`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:b44b5529fabf774a6953c7810dfb0a7becd318d5e07cacc59b1d5f70b3e9db13
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
$ docker pull neurodebian@sha256:4ebd736271d09525672664c3c407e4571dc1b3e4b5456c2f9f1cb57cea432da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59689076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94042a90a21d39fa810f29af2dbe6e9e9e6acf8e9d4d4a0548c07e815ad85df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5ae048d466c70689a7edc5eedf4cf1793ffee4a9b646f2c5582a319d9f8feb`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 10.3 MB (10293020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f3d32951cca7431a1cf21e1aafd0f0fe2b9862713fc19ff35fd5aab0770fa9`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0afa5be5588e323635ba7e46523fcc7d695788b8c883106495ce8fe959cbe0`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d615a8943f123da71966af78797d000d0b087502770705ff702fa8e4d72de499`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 90.4 KB (90383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d1b8a4db5664e6ee8564db8b48db1e602ff4076af3e42b0162ac45ced4d869`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:988cde20d5d12bbbb0de2df64351abef2e21260c34d79bbcac811dea876ef166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c96707ae5af4e3a90694b82d76bce82726327aad21d64f646e786b574b03d1`

```dockerfile
```

-	Layers:
	-	`sha256:97516c0a52ed039e6b3094072fbf6966a275e16ead77e38af34979e8a923b720`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:100674fd8708b6042e678d39193d51e761bba8a6a49fed4f4aceb77bb7f8f5f6`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57b13c1e50963a6187b7e20ca9c973fe30970f06aa206a968c81ed3e3aea7ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32a80663dcc17719bc1935a712da2852657de51fc94f60eaaa9ccc05276764`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77348ea04670cc60ed3fd70e8a942379a3a778401a47da14bddddaedbbcd473`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 10.1 MB (10077993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4f986dcc8620c40bddb431aed2820d258c0ba86a933a572cfb5aea1b7c8d1`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484764866e70b0d12ffdf225ed2ef6dc9af0cfbae6d1ffc072bc54f2bbd8710c`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13df355aa2411e3cab96fecc0b4927c1a75301419531a535765c87be27bdcc72`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 91.0 KB (91046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb102d2bb0e4b299a1747924f034d561048a35b0c3ad22fb08df099037f5e1e`  
		Last Modified: Fri, 08 May 2026 19:46:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a7fc429753a5755b5ee64226c7038ce723951b0fe08eabbc3fba8e4a1697e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c66c6f71d2cc072b4de445c3593012348006787233156dcc732fecc292ecf16`

```dockerfile
```

-	Layers:
	-	`sha256:4d3e70240cf4968ed03616db1c20e456abae7c75f133eabd39d8fea05bf2ab22`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac819a829dd4e682388cbb13c01e4c3ee1c2e11f1c959436f84e286ee2fb631`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b75946ef52c181c76c2e00440d05d0622edfe6da94570e49ddae38ea079dd3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b263265c43778c4c1b4e8f75212dc86f2c4bef41fbb14feea9119600cafa0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4a335a9da7e3093e947b7d57025190b5739906b8bd558a221a15ddf6aa9ee1`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 10.5 MB (10467127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b54ccf8ac71030c118f8ef845986b5523b82fed115f87119415e7d8cc6a7e8`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfaab1b9dbef7720bd0084cf9e3eb661688ece913432774491e5c8964364e34`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a31952666a61c2db472bc221ef5ccc404ecc5d08cea8a1059c7cc6d24e1f2e`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 90.7 KB (90749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a9d9d9e1e36df62b6a57b49fb8a76a463da0ead6d8b53ad51fe669976c35f`  
		Last Modified: Fri, 08 May 2026 19:45:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2acad64ea16cc709a06d2a5aee32e9877e05ebb94c5c760a32e21c3e45deac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a59f41855cbbd51dc2e3c593cbaa8adf474717a361518cb3ebb5186e2b4760`

```dockerfile
```

-	Layers:
	-	`sha256:0d1f3edb3bc163776717dfd578079bce618888a806181425e93980efaaffe421`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cb1f47cd785673497359532ec8428f026e1c4021584f5b6423cb001e8a911c`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:5462c83858d3feb66eab9b4197a35e7c3f2c97168a1f033fa5ff54bc7b0089db
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
$ docker pull neurodebian@sha256:8a4c8e5c02d9c032eff3aca30a89bb11dd0afdb58ba10ea078d0248b1842a7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60186278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6739630cd28c1d946604021f5e65b72c0489c653c44c1558e0271fc06dc041df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:099d3355eff9ccff1f5ee3b288e1ead2e7035e89d68d0fc80f60a9bd7a9815e3`  
		Last Modified: Fri, 08 May 2026 18:23:36 GMT  
		Size: 48.7 MB (48702238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e478533e6ae193c6fcaae041855399f59338878fa7e4644c40a17730309dca`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 11.4 MB (11391655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601904e49e5900acca267146a686c3f2a2a62c1246a1e38d212fea83bffbe0bb`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d949441ff174a57a6fc707bc732ca1634e6558df38f4715cbfcbaebe99f00`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dbdaf7f7809f135ace320cd033d9a6d661f149877bfc78ee99f12ba8f0ae08`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 89.5 KB (89483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:412cbed693a82d055a8f5357999ea9f0053401665d64aeef08fd5f06d2dcec0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66b334229b8a964cc51e6b877024313d7cc9a4d9a13c5c0ac570a1714ad128f`

```dockerfile
```

-	Layers:
	-	`sha256:2798dfba3ee312a5c3c86f73e2dd22eff329c06e0ea7cf6108e8ab3f170b1791`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3556234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c8c7bd53e080388c9a1eb264e0fbea45b097b66db0192338955fa9903db445`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8d042e0c6b2b0bdc7bd6088a54197a0062b4e77fef4e334f0b514b42ce76bf43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca4e48d28afe7d23765196f54fdea60741801af0f6b198d4f1d7aff164ec43b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2a6841249cc037385aca9cb88bc26e07cfa8ed2a3f883ffdea8ae1be354b5a`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 11.1 MB (11092978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938906dfc842f7becc351af1835f05072b61776a354569f75a22d1f1e6ac299`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0668f71f67e7f7a552b9af4850f0941fb6afd56c29cadc4acd358584bd8a7518`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c06c9c91f639614d4952e3ed20b59bf97c833709c3620987f812909d74f82f`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 90.0 KB (90027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1515e7f8ac45bd3a4a536ba87d58574f9beedb409c59fc72752b88164c944056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36672cedf692ab9b354876cbf435214d90917c05080107060f25e608acf9f045`

```dockerfile
```

-	Layers:
	-	`sha256:1aa37ce6e70e12258b02b458c1845581d86ecdd450c40a6a59c724b75463cf93`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 3.6 MB (3560939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da2b316ca48ed77a2b1aa0ced2f3d8e67b58143d8135f7f24e5168d05f49127`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:73ba3061222d6c325c0a346e63bc504de41f9532e07a59209fa44e4519dcdabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5af2eace4327f02703f432d25d547b430da3ef4030f8154d0d4dd1322459e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f0c0878f24a22f4bae1cce2bb33ade2528e750968c7f19e4683f865ecf624f`  
		Last Modified: Fri, 08 May 2026 19:45:28 GMT  
		Size: 11.6 MB (11625846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83aff980bc85ff5b2ce155faf54e6e3fbf0412fad6b9b461726d7a94f49ec8b`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1690741b56c00af9a9e027b2f45da2d3c964439f6016d2a01ae49e540c9a138`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403996057114e2cd0d36ee941960ee517faaab068e8e0cbc9de09e96c9223a56`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 89.7 KB (89717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ab1c10a7c00e20030be43916af676fbd69ea524a13a3d1f1100bc9cad07f30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df6d819178bee19b394bd34bd99b9a33ff2d758ed51a85705d80ba78362451f`

```dockerfile
```

-	Layers:
	-	`sha256:2890089b6f33dd50ea7d84ff7f43fd03e40b52a12e2925bb4cd5456bc7dd9b0a`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 3.6 MB (3554180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27aea920f78950a42d40670e7327c30443ef99b9d23d92570dbbee1e83f95701`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:eabaa9df6e6f28acda269868f36fe6b1ef1678d2762119d6c77c78b5d87b1363
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
$ docker pull neurodebian@sha256:5334a29a1f0fb4835758c1b388e322a2348ec3032da1a4e6572e98134532a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60186655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064c3891de8ce33ff0e4fe108f5171b68727f60ddc6590af502f8e0281df2af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:099d3355eff9ccff1f5ee3b288e1ead2e7035e89d68d0fc80f60a9bd7a9815e3`  
		Last Modified: Fri, 08 May 2026 18:23:36 GMT  
		Size: 48.7 MB (48702238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85957d69d501ec6d0cc38c388d29b67893409a599a0fcd2b22af2a3660ed4cc`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 11.4 MB (11391676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d154e7fe6720de57e32775de2e5bdeba041c1cc8be9924ff6250053bca50a1e`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01de64d5db46c87cdc4f28638e85cb1ed77837b8947122fd2a37dbf6a2f7b87`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfcec0b2aa32503cec752f39c7a9b0c88eef9c3672f941e3e83f08087d90a4d`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 89.4 KB (89417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93eceb2733233ea0ba023ae35ac2b50c8272e02060ead780922c8d64837d456`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:83338b9dab02c5e892d7e4c04216af3417a35050a3c6a89f5679c02580d0fbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d211b3029e995baba17d24b26293538cc7ca7cbb4c686d90d9282b1952bd0328`

```dockerfile
```

-	Layers:
	-	`sha256:489a9f86bff40e3acd067530f627ebc463f581180e26ef866ff20945dbb69aea`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 3.6 MB (3556270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9842aa3c21dd529e05422a063872ac17852062730e02604d63b250e85fae24ab`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bc374f952257e26453ff7836ddfaedb60bcb7b8567066896a59a1dc6235eafc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33147fd5038a8f3c7854dd92f9f80f55966afc35978f38770149742f5fcb876e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364834fc8139dd37c03942d4ae776f1690a19fa2aadbf6286e0c696c77f02654`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 11.1 MB (11093047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce88d73a7e0fe050bda503e936cec378bffa4e11cf99f44f3547a9bb9550e9b`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042248e359b2ca8c613f492ddea03664e1f5545d422f89ca2eb579ec4fe36cf8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05b1b5889373a2ff082dcc562fe9b6c87f4dc954311c07a9235161b5b8348a`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 90.0 KB (90047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb1a6769325f550371ea3eda25df8162e96ffd9d1e724c04e9fd6a53a5b15d3`  
		Last Modified: Fri, 08 May 2026 19:47:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:38f1246a7857ae16f1ee50ce83dd99f709d82307b1ac48db4580cdd4ec7ea6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3237ed235baeb7082f0151c28c4714dc3f510674f4b363afa9a12ad73cdc2a00`

```dockerfile
```

-	Layers:
	-	`sha256:d51df37178d40b9b383e7bec1cacfb104cebafc298e749ac1e0fe3566149be4c`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 3.6 MB (3560975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fef56e4295a87c65f8c4cda5532f9cef3a17c374c89cd048b622e0afe8df15d8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fdfa585524dbca77dc88c79d28594b439056998a1873b0734100d0fbfcc4983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e746d8a97559c27eb06570b8eb5bf7fd0656d5f75194b377aaefd9ce7fea3f94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60950ea8f81eeb40f4ffd4c9eb5344310a3d3b4a3ba10d8636c3e11c143743a`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 11.6 MB (11625857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e999e91d392ae0fef15aeed6175ba39d08817b5593d30f26ef16d1565d28f379`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208859bef58c08283e7c0113598e89b5851cffe3ad75ec5cbe4f8826bba0007`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec1337df25fa89a088252f15b64bba7bf8f37501ac5944f7352dd621c52673`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 89.7 KB (89684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354222966e2e2c36cd8e4d1a765f5ce435c85024a44468f4c76ad662da8dbe34`  
		Last Modified: Fri, 08 May 2026 19:45:42 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:efdcb503bdb440864d0bfd5fcf11ce13a5bcd3ca870806e08019df74f241815d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77f0b27c9a0833de49273eb014ec6b6900a97b4265c8339e9c8422a12a57f18`

```dockerfile
```

-	Layers:
	-	`sha256:d3ca879e53a051396232cc6749a325b48a90a77b314898d6642ff4a75b84707d`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 3.6 MB (3554216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bf0aae2c3093143415998f808232246df063b6a5a9ac0bd9e4a9bd97ff539e`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:7d615974d7618624acaf024c794146f6955178920e4a11205f0b463c1a903434
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
$ docker pull neurodebian@sha256:48409e2266289921f625e696fd82ae75b3dc7d3429568e904bccb3046e022dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982b441ccd68e375ce55850b6f2530e35f89c4a858bb75344fd7a5dded7d5ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603e83f84352e4d604d1ebd2e7b11a116e1d73c815b1f21b71c35cf4d26a6adf`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 10.3 MB (10293033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9841317468747bb9c4d672ac9e22fdbaf7467995b3009c013af9504275765`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97afa150b5dfa5f4868492e1872f0bd5d68742189b24436efcc83edb5b863ad1`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80469e6eba86735ca23d5fc2e8e6e31019a42fe3e7a96b5d2580cffd3a1892ab`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 90.4 KB (90409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93973523588868a89ea7a3048595fc8a05179b43bd1a791ce32770712d00e9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3739871772f9c6753eab2831cf79f90dc38c2a6030448f67185547885e75dffe`

```dockerfile
```

-	Layers:
	-	`sha256:48c1c93d4580490d300f49739cf9b99e4a0678b32abf78a80898f5033fa0cc82`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a980516244bf1755bee0e5c4047d7bd22a6645fb62f256893244939631312c4`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d503ee17e4a04127673e873eadb5e238338d8534e69de76f9a2834dea00068f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d388d64eed3a472d75c0230a0f7e0ec18ea76b7a49cf2f265fc7b87ba9fbbad9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c629af507dca062ea56f93574fa391e844b4d6e1b5cd11cad63be92b46a1d6`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 10.1 MB (10078011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abab8ca898857514fc5bd463e6e97a767bbca2cb8aea60e359cd6acaaa15751`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a787e0f5c6e783915e7fc9afa550e0bcf87b812188a88bfe09536d428841b0`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac226701451e2fd232f7351b186bb36b4f7e1742f26e18192509106d28c45ec3`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 91.0 KB (91035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dc047d2f30ed6ac4ec61cc1afcc3087048f8b38a8af931444118db41c4d4566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb1e88be3ddf79970c3f161eee07195b0acfc24a53e5306704d479fd7126a7`

```dockerfile
```

-	Layers:
	-	`sha256:4d576367898d58cb2af04ebc67ca27c1a684572a74fe8c3a8c3fa9d91bb20031`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349d03efc82e58b0fabaeba13d01e95372d1322c71cdcb42706cd4ee07d99898`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:674b7f113ab98f457c90a5407cf9fce5d326c1ada9d335c3bb736dac15df1d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd893df613b6c8c15a740d7cf4906096d1c477af22aea43f2c1a7965c5c10b95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918b15ce42e2f43331d7ca8a6909c2f318788178997f3be2a6c20d15686eae08`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 10.5 MB (10467078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d8c3e17a2f821d9a1e4a647dd71fd281974066ed12286ff5344c3c70918add`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745c310d83150426f135a032fe18cc82a8e5631e02d97a07354f8c9341131d6`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d13836b8f7a1419799c27ce5e5586655df8273d6004aaa0c492b5a99f6622d`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 90.7 KB (90733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e4dfc7f492836cce5f36a3a8e3941b8d6619c004fb9fb3e8a3df42c8c567950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911b218b44e62288fb317f239ec58d54680252b6ad5b7b84abdeee0eff2adaf`

```dockerfile
```

-	Layers:
	-	`sha256:b35285063f63c97ca1e2f1b58a75539e178f06a4277ff94135e31ab43d844d97`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be65c44927642dbaf0443b5d950bdb2eba7e045ec2186605bd5528701cc1ccdc`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:b44b5529fabf774a6953c7810dfb0a7becd318d5e07cacc59b1d5f70b3e9db13
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
$ docker pull neurodebian@sha256:4ebd736271d09525672664c3c407e4571dc1b3e4b5456c2f9f1cb57cea432da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59689076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94042a90a21d39fa810f29af2dbe6e9e9e6acf8e9d4d4a0548c07e815ad85df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5ae048d466c70689a7edc5eedf4cf1793ffee4a9b646f2c5582a319d9f8feb`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 10.3 MB (10293020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f3d32951cca7431a1cf21e1aafd0f0fe2b9862713fc19ff35fd5aab0770fa9`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0afa5be5588e323635ba7e46523fcc7d695788b8c883106495ce8fe959cbe0`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d615a8943f123da71966af78797d000d0b087502770705ff702fa8e4d72de499`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 90.4 KB (90383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d1b8a4db5664e6ee8564db8b48db1e602ff4076af3e42b0162ac45ced4d869`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:988cde20d5d12bbbb0de2df64351abef2e21260c34d79bbcac811dea876ef166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c96707ae5af4e3a90694b82d76bce82726327aad21d64f646e786b574b03d1`

```dockerfile
```

-	Layers:
	-	`sha256:97516c0a52ed039e6b3094072fbf6966a275e16ead77e38af34979e8a923b720`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:100674fd8708b6042e678d39193d51e761bba8a6a49fed4f4aceb77bb7f8f5f6`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57b13c1e50963a6187b7e20ca9c973fe30970f06aa206a968c81ed3e3aea7ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32a80663dcc17719bc1935a712da2852657de51fc94f60eaaa9ccc05276764`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77348ea04670cc60ed3fd70e8a942379a3a778401a47da14bddddaedbbcd473`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 10.1 MB (10077993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4f986dcc8620c40bddb431aed2820d258c0ba86a933a572cfb5aea1b7c8d1`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484764866e70b0d12ffdf225ed2ef6dc9af0cfbae6d1ffc072bc54f2bbd8710c`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13df355aa2411e3cab96fecc0b4927c1a75301419531a535765c87be27bdcc72`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 91.0 KB (91046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb102d2bb0e4b299a1747924f034d561048a35b0c3ad22fb08df099037f5e1e`  
		Last Modified: Fri, 08 May 2026 19:46:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a7fc429753a5755b5ee64226c7038ce723951b0fe08eabbc3fba8e4a1697e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c66c6f71d2cc072b4de445c3593012348006787233156dcc732fecc292ecf16`

```dockerfile
```

-	Layers:
	-	`sha256:4d3e70240cf4968ed03616db1c20e456abae7c75f133eabd39d8fea05bf2ab22`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac819a829dd4e682388cbb13c01e4c3ee1c2e11f1c959436f84e286ee2fb631`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b75946ef52c181c76c2e00440d05d0622edfe6da94570e49ddae38ea079dd3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b263265c43778c4c1b4e8f75212dc86f2c4bef41fbb14feea9119600cafa0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4a335a9da7e3093e947b7d57025190b5739906b8bd558a221a15ddf6aa9ee1`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 10.5 MB (10467127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b54ccf8ac71030c118f8ef845986b5523b82fed115f87119415e7d8cc6a7e8`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfaab1b9dbef7720bd0084cf9e3eb661688ece913432774491e5c8964364e34`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a31952666a61c2db472bc221ef5ccc404ecc5d08cea8a1059c7cc6d24e1f2e`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 90.7 KB (90749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a9d9d9e1e36df62b6a57b49fb8a76a463da0ead6d8b53ad51fe669976c35f`  
		Last Modified: Fri, 08 May 2026 19:45:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2acad64ea16cc709a06d2a5aee32e9877e05ebb94c5c760a32e21c3e45deac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a59f41855cbbd51dc2e3c593cbaa8adf474717a361518cb3ebb5186e2b4760`

```dockerfile
```

-	Layers:
	-	`sha256:0d1f3edb3bc163776717dfd578079bce618888a806181425e93980efaaffe421`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cb1f47cd785673497359532ec8428f026e1c4021584f5b6423cb001e8a911c`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
