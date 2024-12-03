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
$ docker pull neurodebian@sha256:2f2ee431e155b1cbdf9193f76b66b200a715d206243e041e20ddc1e3ce5f4f29
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
$ docker pull neurodebian@sha256:0c7d59a5f8e1550b820a5027a093228b51c5e0d66456669e84947e7afef32a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97157fe06be6c40ed4369da113e6278119516d03dad788264ccf1e31b0c42a01`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950a82ed7125db9e9031ce90322ac9e66a78ed9482daf60f03df07a95a014541`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 11.3 MB (11266835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1b38f8cddfd22a2af98cec683daf6d65d23803957e5dd5dbe69f804a2a3f`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1a0dbd43a3757bda4754fd5c0f02f8548b6030e705dbbd50eb9023dd48b226`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff386c46e5b85cf021e16c77a07eeb3acc1c69637477e33c7f2e55475483934`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 93.1 KB (93138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fbe03585af1476fb2bbd2908efaa2b8ea83b4b68bf5f6bc58ef85f1e70eefc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97ad597ee27c7c3724f6aac33bc5a022ea24f97ad9d4d365a2b6f265f19a26b`

```dockerfile
```

-	Layers:
	-	`sha256:8ad1888ebd680f37d0b7a3511d4c5b1c740b11d503c347ba76058a40d228ad59`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 3.9 MB (3937231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b9c5da835238bc532ec29b931a715c71c311204760c6932ba56679ca5e5184`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 14.0 KB (14000 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5eb8620046a2e02bee05f9dcb5abf9a7ea018cba00b6a5b19d10a4d20b2c25a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da76854b721e08ea18a3c19fb37d170beaeeec6f442c69d981d3a205fd3692bc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d6f082b94e725149735aff5f39abf2a5c1faa04f4f35829c2b04bcf36fdb0`  
		Last Modified: Tue, 03 Dec 2024 06:16:59 GMT  
		Size: 11.2 MB (11232475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7164374defb4bad306066d94c7dac571980f047bf262c550c04b585b492527`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a1000d937bcfa52ee6cff54a54a79274765aab42bb61041dba4d40c8ea00a`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab49634abc6db7b16ad6e4f6d1bd12260c9a0555ba2d16c5abca22782e40f3`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fee13f802494da87f2824243b1ef6ba160c30fc88f4bb898d47172978292f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82beb41f84b93d8e674c7203b9009b5d27ade9c1eda441be5ac865312e51e9aa`

```dockerfile
```

-	Layers:
	-	`sha256:942f1434e7601bc69e26b7cade69d8c6c91abbc09905aa7e29e161a332fa32cc`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 3.9 MB (3937484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a95f2482d505abe9ca79152c5fa27d45a5ecbb3e300f19487154106eb2c2a20`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:7be9f025a968af1334c291d8942067638fecdb9ae6aa2e02ac3a5409c41a37a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd04204578e3c76cda4b47577a26bbace9322f371a285123aa1fc902be6a98a1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590fcc30f6c50f7ad71c3858d2239c46376094eaf1a12e0ef65a4673f5e763d5`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 11.7 MB (11689045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbe2a76c7a0519eb8d714422348d7d6285bfaf0888b3d5341e0bc6ceb17e999`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75487833f3368eab2257a94a630b1880b487a3d9c985df44821377679a8630bf`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7d9d4001de6a0138bedcfe6908f4c986a615e32193ee3c092897d30647ed46`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 93.2 KB (93219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44e8730314266bff6d4bb59854d8785f0f8fe79a8da4a423ce7a6886f9fa63cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb443803c49e4d4189b2e400064620236d7b0aba3972dca81fa2dd4b2e294c5f`

```dockerfile
```

-	Layers:
	-	`sha256:84859747a36c49bfba821a162fe221c7cfe11f09235d8f7a8f66c8c32748ab80`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 3.9 MB (3935148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7067294bc3a8508f9cb372c5d48b39df12f9b701bafa3dbd11218ff8555282`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:81f633276b9be30fa1dd00b0723598ca82c4071e30da9746fc744a70d1d430fd
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
$ docker pull neurodebian@sha256:f0b826db0485d7e82be034c6c5e7edf87df12d265d6677d054029eca4e93eb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7686c9b19aef29cd8dbd901aef411bfa8220e559879f8633d2b8abd2cc429f7f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3cc0f98744a051a1a5f2afd9efb44ebed4fa17eb3c1dddb60d9c9400c80ab2`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 11.3 MB (11266780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ba287ed08d01881207dca39c00528deb3fdc3f2d81914037be7b1cfdbe874d`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150a6037915fb13285e5895a6a1c62c6afc1704844f3fba6208d25301de77e56`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8683715aebd7fa532f695293a9e651f0864ce67665530642a85014fd00d60f96`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 93.2 KB (93152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9738867365afce7f70b32c401344176aad5e654c99fb07a9333af858e584b4e9`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5ea80b90c3a2e9c97601511fd1dc77bf211dee1d51e558aa1fda464ca36368ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33c8834e62878218057544094ea5fe3dd9746688832eccb7832c6c514dd2f1`

```dockerfile
```

-	Layers:
	-	`sha256:7bf28a7d462fb022e11d07e4097edcfda51808238332b04d7be6307f77970fb9`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 3.9 MB (3937271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2408a1585fa162bca505495ed4028662a915c5800c5ec73c3024bf5a965ac6d9`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8727cc1156f0afd9f41a4c982dec32a7669106b1396116e3bf6adae8aa7f4756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52ed086311e71cb3ca17d2f26956adde08dc02a426a23d623a6b6b455dc26b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d6f082b94e725149735aff5f39abf2a5c1faa04f4f35829c2b04bcf36fdb0`  
		Last Modified: Tue, 03 Dec 2024 06:16:59 GMT  
		Size: 11.2 MB (11232475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7164374defb4bad306066d94c7dac571980f047bf262c550c04b585b492527`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a1000d937bcfa52ee6cff54a54a79274765aab42bb61041dba4d40c8ea00a`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab49634abc6db7b16ad6e4f6d1bd12260c9a0555ba2d16c5abca22782e40f3`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfadfcf78518bb3680188a8aa8e9b4e03dd0606fff44a59bb7c8d5499eaf1b4`  
		Last Modified: Tue, 03 Dec 2024 06:17:11 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff00f65b3308cbfe02001d7be3d5101574bcafc13cd2ed12fb2c5ea4a3f904a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88092ab67db4a2a365b3756e65b7129bc9d0f9970f46cee3556212d286bc0541`

```dockerfile
```

-	Layers:
	-	`sha256:5196f61854393e3f4bd1507046c2519f7c7085fc551d84440d34fc98c60437db`  
		Last Modified: Tue, 03 Dec 2024 06:17:11 GMT  
		Size: 3.9 MB (3937524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfdbf730785a3a5e3830386fbec8ccf928bede15706f942762a042e778e73df6`  
		Last Modified: Tue, 03 Dec 2024 06:17:10 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:8dc7482bab5a6e73520137dab2efc0ea2e1cc8fc7b00a55bed98c1f0f08d9b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c795e80457b17a40c2f0ba40bb9b3c56514d9bd56e840230b6cec3cf737c4acb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4351f3571feee02247d67c5362a4118390ace6f8c203163c4f98131c109f39`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 11.7 MB (11688949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47502da2499b6aa6bf2b0b61829d4882722d17064ba80d8bb48ea95f18de4d5d`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807895808115d1d32826306aed408a2b386e021fe7a1a16f92541a7466a2bc9`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ae4b46bcce38d9c1ec20a3d33ac2e841511ae54438cfaafe1d94b487dcc6b0`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 93.2 KB (93220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f86ac460bc7c2375830f2b95cf8a012950443b99acbd0fc9bfc962541710a1`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ddd3208bdcab3b163d0e37e9f5c42ceb55651e14db8e8389f4adaa1ae19865fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a502d814818aeb638b6714649752b3a5f5ef284ca7087a822e7014812d9e26`

```dockerfile
```

-	Layers:
	-	`sha256:1d21298306b6c34fabffe2598c235ed691faa6d0a6279c00194aa06ecb984533`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 3.9 MB (3935188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ebb9243e1a48616e3d08d94ef366bbf4796762ab8c72db1e88b6d07afdce1d`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:fe18aff0849b4e1df68d19c274695dfba5fbb0fdbda98a07358e3385501a4192
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
$ docker pull neurodebian@sha256:98224cdf0cb804f50833ffd343c2cace4d0620cc88d868ceb1cd6c3f0b1be796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a7eacd89d2e958b8a3b6aef1e1fb0af72893321723ca18a1b85f80c3421cf2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a11ff2a1535c8fa479a7c320a495994c3166965074adb19749bcc81e94a236`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 11.1 MB (11105069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bc8189aefd176e625a1f58b86ef8ef61308725ac86d6fd1c717e9b85da58b9`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b867fc96223e2170f08b1bddac268faf03b601fe9d00b5f0ce2da019d85986`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d8f54f537c07c9a80af694512b8f79eb12644da787978689d518b57ffc4c6a`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 101.2 KB (101202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aabe9a95821368dc3e33ae33e0f56d648947a2b242fdc099a2b34d153e0445a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39da91d5bdeb24c36f8303399cf2fc0e0d4932a1f08f7e211d96ff785428d3c`

```dockerfile
```

-	Layers:
	-	`sha256:803d69e4cc55c299148ef4158b0e946e3807a73af9024011dbd4a65f5afcb275`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 4.2 MB (4237043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4709aab7e44720ade9fd334c8d1c2c7cd35b6e7eda4f7d0f5bc30dc8ba85cf`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 13.7 KB (13692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:503b12cc63458348913441053b31b45bf94be1d0e08d898aaab1ee73d447c47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37149593973f1cc0e79d75464579d66456f41879964a0c0f3d2ba14e8d194e51`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fb46d4fbacbba6f0e034e8d65131a0ae5d99a9803eaa1223ca1a1cce020e44`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 11.1 MB (11105958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb47f993ab8f56d97d07ec72b6ec7643575396ff3eb0ac2e06dad8348b99fa6`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe4213d9e47272af07a9e329e0d77dfd006ade0e3035e1d7109e590c58f702`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd00afd1e307fc6212c5179f04ed778efeaa0b8d1c4d2f1cf0ef40961607d39`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d70b2455f8344e8e8324092bf06f83009f2f80bb01fe75818efb32a56e72b6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f454574e54a23090cf00dba92b65577480a93397a5a6de461e23e64b7a4e8db`

```dockerfile
```

-	Layers:
	-	`sha256:8dffb7f08ef77f3d5388260c476513166ccb0f27812ff4240ee86a096ec9498c`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 4.2 MB (4236648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d72e5d7a074b56de4153dcc7da35221212a240b3c5a178af2bf0a8025cebbe79`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:7c5a39a701d8dc66eaf4bf30d54a87c77d1efe5ef0ae96588400f6492cf26489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cf762d4dd883d16a90d46ee45855b8a8179cc4efbe9bcce674e18a1138a672`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef34bc916fc85979e50d28fbf87a379437236619f31787c6253f9be255cf615`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 11.5 MB (11500365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c264fff16245d2054954a0c0d6a4e94402f127fa2f336a10d500b8c9365f237`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3dc84c047211a70772b4b5cc81d0f696576da04dac87d3c77c6b01c0c40856`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987ef48478380284df1d15d0ce83cc3d2b348177e1967cb6995033830ebca434`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 101.1 KB (101064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7ef6b6b3b18b388c4c6a0a2dfe818b51ddf588fa06bc75068201bd43cfe08813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736fb535b3e23528fa401960e8323a637abd1360e60549f9d64c45929306706`

```dockerfile
```

-	Layers:
	-	`sha256:e6431df809d0774340669cb6df2591eb71e2812dafed6c7c91ed5684daf5da56`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 4.2 MB (4233503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d59b514ee3f01c9758a94082d2709cff01cd42599e7c253880f815b86314d4b6`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 13.7 KB (13665 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:978a8625452ab39d13e6a7f02fb3cfd9eb7f71df63e1c1a81c553c61ce2b6514
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
$ docker pull neurodebian@sha256:41bdb44a634f5e4f772e8b59e7a7acd006ddae9b568a2e99b51fb2e2c257ce8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8083ab6daad4423e11c61f0c92526f7aa8c68ed7275722f632c9a567a37d5079`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4769db03e4d35ea9c8cf75cfe915aed6f030961da59a336f4b4368ca4f71fca`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 11.1 MB (11105088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f91ca316c814418b68c407c49bea3fff42122da0c9c1893c000a54305d893e`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942eeb99ec88bc46a9080bd348da8680bbbb1a8b1edbd7f65059f75d8cd0cce0`  
		Last Modified: Tue, 03 Dec 2024 03:20:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80de4a826c59a53034b00bbe50abcf962f0854836822443071456f042f3ac96`  
		Last Modified: Tue, 03 Dec 2024 03:20:21 GMT  
		Size: 101.2 KB (101187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e891a80297e2f74d3274edf0b1c1de023918624816c8875663815aad0019c7`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7238d490a1ca5d396933462607fbbfb142601f035e62da4c4e3ed979bea56eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f78453b1ddeeb1ce16c0702886fa7638f014a6c09422da188ec507efaf3dc9`

```dockerfile
```

-	Layers:
	-	`sha256:e16018084601f4670cdd8bdfbd363f7ea4d46c886a0fbc2dfdbc68534065644b`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 4.2 MB (4237079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:589eabc43436ba0627092ce4ea2ab4f3e528dd1139609ee803094bd027690982`  
		Last Modified: Tue, 03 Dec 2024 03:20:21 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5b57e8e5b7dfb431cb05d5d58451cf4d3ee9a357b94f59f83e5b9ac1145bf342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af5264ab433e8d3e3e5f80bbc2d75ff8af4a6193418868592de413d174fa84c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fb46d4fbacbba6f0e034e8d65131a0ae5d99a9803eaa1223ca1a1cce020e44`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 11.1 MB (11105958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb47f993ab8f56d97d07ec72b6ec7643575396ff3eb0ac2e06dad8348b99fa6`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe4213d9e47272af07a9e329e0d77dfd006ade0e3035e1d7109e590c58f702`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd00afd1e307fc6212c5179f04ed778efeaa0b8d1c4d2f1cf0ef40961607d39`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f9c61c4532d29032e3956422cc71112cfe60ad7e4ac47495587c0586fa15ae`  
		Last Modified: Tue, 03 Dec 2024 06:16:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d72ce6d5735dec09088eba399b7d1a66d7bd4d6dbc1af841657fab98c25eb3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1d6814225bb1f6e768e113c59455e43f0865dfa5c32dff4a8129ce2f3aa20d`

```dockerfile
```

-	Layers:
	-	`sha256:beae995b856fc77a3fe49b4211e6c69ce9120213835d354b41972d306304b5cc`  
		Last Modified: Tue, 03 Dec 2024 06:16:35 GMT  
		Size: 4.2 MB (4236684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a560d37582a8d74f5745c75dd7ced712a4b381c5461cc2870f7b0e246b42bff`  
		Last Modified: Tue, 03 Dec 2024 06:16:35 GMT  
		Size: 15.9 KB (15861 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e9b7abc0bb54d79a9a24ffc0b81d00184d09f10f0016a5f72d2d693308ec24ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66280058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8063c68d8e3e84d7c47d6a92ddba4264f9d204fc2b35bd2a81bcb84a8ca282`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b65f3a96293e2cb168b19c54c2b62093b3728fddf28451b6b6232d90e106527`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 11.5 MB (11500368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c264fff16245d2054954a0c0d6a4e94402f127fa2f336a10d500b8c9365f237`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3dc84c047211a70772b4b5cc81d0f696576da04dac87d3c77c6b01c0c40856`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244a01f2463f793685cc01a57b4ce0420d030c5e38b8ce6a00c2f6813328436`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 101.1 KB (101065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb4dfbab157a0690d795d7386cf3563e5b4515abc4011077ce213843cb5c2d1`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:778a60719cc186db2508f107a4bda760adc002211fe26bac1dd1689b74a61152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4094e65772473b512ae8026ab0810de01b98dde7e8abaa654d59d8542c83d4e`

```dockerfile
```

-	Layers:
	-	`sha256:0a3e5db830790c929c589bf59f3b62306f609956fa0b2dd27ecb900bce3324cb`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 4.2 MB (4233539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e526f0f5199f5f0d41d0d602062811cff0642b5963d4c171bb89d35c5135ea`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 15.7 KB (15691 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:8bcdb02c955c552289fb14468e3d0eccac712d0a170f1fff5601f3f3af9d8a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0c6cb45ac1cfbe06c47f14d684929ff5f5907ef7f083c360195214c3ac6aca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1335fc867ea7b822d1b6882dc96ad365e5cc4643152d61c5fc8a7bc5f85a988`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49fa7316f784f5cf307546c8c97bd1b9f3a1fd2943c27fceb71ec2dd6409f48`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 5.4 MB (5360278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7c65bbf482527df64ccec5d79c08cb11cf2d1f4054f4977e47dad48ff8435`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e678bedd7e50e1ba3e947302d4a3badb36d988b369aab4b47c1fa78259c23552`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9792897da4dcee6732822377f46272804fb1e9b7f31dd60d17894a127edb839`  
		Last Modified: Wed, 16 Oct 2024 16:13:43 GMT  
		Size: 105.3 KB (105327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848d25161f517586e1457fc807e778d3305bad2daae744ec21fc37849f68173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820220dbbd11c6d8f3103b1a3ed83da871c77d7b02f18798badcf3237303dcae`

```dockerfile
```

-	Layers:
	-	`sha256:27970857ec501c025d084e20e5352a5d5ddc17824cc89a85f49e7025cdcb4a02`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849d52e89f42eba3812416ede3dd4d1badb9a69a5a982f874e39c325041eb9a2`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 13.4 KB (13444 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1a3f2e41cb72abdd7dcab281d6513ce2dc547865fa3b4ba0776bd58ea8a5de97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2c98411bfbdccf11946d245a8061c56c6ce058ada6075d911256dd80fadff8`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1f3f34f75e1a4bc32b849a9ffc880a30708443a7fdc0da8a50c2e90180094f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5772b0ce1260ce48effc24ad2f6bdefdb4674ee0d585774b4464dfdaa8df07f`

```dockerfile
```

-	Layers:
	-	`sha256:71ee94546588c20b92a492d129395aac336c0ae8677f9f8048b6890a1e640901`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa10decb4cbaa5f56d95540086539ce9a7bfee79f97ecf26a18eb6160c482bbd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:e1b1eebaa7be7a7ae8986f10c005fbaacce6a33e73c7193cef12dee6f49b40b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ddc9018acf97b1f5814caa6cde3c3d36dc386f558589639e00bd07b61c4ceed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02507bb93b25ace19e3dbcf9e5a746ee64169a6e6641918f946da8db0e4d17b`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4005701787afe01df59207e8d67264732bba189629db1779b4ffa79571550`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 5.4 MB (5360288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6862ce93e83033ea4be1d4f8bd4ea70b498c761c3664782d446af47aa9926b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce53e76a062f11aaecdb2eaab737adaf3dfe235440d4e34cfa7bd8bc8634e70`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f662144d756ef598c43631f18e5a5aa12b2a8e2c719e17635359530cbf9a9b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 105.3 KB (105328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c113f4052eb4bc0e89d69bbfef200be8e9cc348104fc8ae5bc167ebdf6ac683`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fdd9dd95911aad8010d1bd7b668cfc9886a64e712c66aeab16529edd5642e84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419484197e2594f495dc65df02606517cfd33b3e8fb27db49620e293bfb8facc`

```dockerfile
```

-	Layers:
	-	`sha256:96b650f1cbef5c5dbf1b7069ca052e04734ab3f40d4e9ed771e9496d60fd999e`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 2.0 MB (2002687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdacbdc41b77b356c35fb81b7e0fcf121e4d6c1b38d2d913103141df6f522c9a`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b3f6acebf8e01d4ccb64904ddb4e553df094a7fb6223b50f683882a0756a284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9be140461e203793948a95c87503859fadcb667866ac155c79cf9aea88c1edf`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4975400a8d7cbc9b67c0e50618fd95fa63506aa713da18a3da28accdeb57768`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b26186688e44f87210438ddae17d14c31f634b630c497d04013b36ec09d92089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b3564811c260795602aab1de18bc1a0e9abcc4a1a00d4aa08bf2c13102fd50`

```dockerfile
```

-	Layers:
	-	`sha256:5f09b22f2f9e9d8a1f0ccc85ccd622a779576a09f4ec13d286e85c8831be03eb`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 2.0 MB (2002915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc6326745662ee2e02b1d747a2d2ba13494721e28def82decf35cf47a1614ff`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 15.8 KB (15808 bytes)  
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
$ docker pull neurodebian@sha256:2f2ee431e155b1cbdf9193f76b66b200a715d206243e041e20ddc1e3ce5f4f29
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
$ docker pull neurodebian@sha256:0c7d59a5f8e1550b820a5027a093228b51c5e0d66456669e84947e7afef32a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97157fe06be6c40ed4369da113e6278119516d03dad788264ccf1e31b0c42a01`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950a82ed7125db9e9031ce90322ac9e66a78ed9482daf60f03df07a95a014541`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 11.3 MB (11266835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1b38f8cddfd22a2af98cec683daf6d65d23803957e5dd5dbe69f804a2a3f`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1a0dbd43a3757bda4754fd5c0f02f8548b6030e705dbbd50eb9023dd48b226`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff386c46e5b85cf021e16c77a07eeb3acc1c69637477e33c7f2e55475483934`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 93.1 KB (93138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fbe03585af1476fb2bbd2908efaa2b8ea83b4b68bf5f6bc58ef85f1e70eefc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97ad597ee27c7c3724f6aac33bc5a022ea24f97ad9d4d365a2b6f265f19a26b`

```dockerfile
```

-	Layers:
	-	`sha256:8ad1888ebd680f37d0b7a3511d4c5b1c740b11d503c347ba76058a40d228ad59`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 3.9 MB (3937231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b9c5da835238bc532ec29b931a715c71c311204760c6932ba56679ca5e5184`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 14.0 KB (14000 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5eb8620046a2e02bee05f9dcb5abf9a7ea018cba00b6a5b19d10a4d20b2c25a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da76854b721e08ea18a3c19fb37d170beaeeec6f442c69d981d3a205fd3692bc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d6f082b94e725149735aff5f39abf2a5c1faa04f4f35829c2b04bcf36fdb0`  
		Last Modified: Tue, 03 Dec 2024 06:16:59 GMT  
		Size: 11.2 MB (11232475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7164374defb4bad306066d94c7dac571980f047bf262c550c04b585b492527`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a1000d937bcfa52ee6cff54a54a79274765aab42bb61041dba4d40c8ea00a`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab49634abc6db7b16ad6e4f6d1bd12260c9a0555ba2d16c5abca22782e40f3`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fee13f802494da87f2824243b1ef6ba160c30fc88f4bb898d47172978292f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82beb41f84b93d8e674c7203b9009b5d27ade9c1eda441be5ac865312e51e9aa`

```dockerfile
```

-	Layers:
	-	`sha256:942f1434e7601bc69e26b7cade69d8c6c91abbc09905aa7e29e161a332fa32cc`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 3.9 MB (3937484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a95f2482d505abe9ca79152c5fa27d45a5ecbb3e300f19487154106eb2c2a20`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:7be9f025a968af1334c291d8942067638fecdb9ae6aa2e02ac3a5409c41a37a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd04204578e3c76cda4b47577a26bbace9322f371a285123aa1fc902be6a98a1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590fcc30f6c50f7ad71c3858d2239c46376094eaf1a12e0ef65a4673f5e763d5`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 11.7 MB (11689045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbe2a76c7a0519eb8d714422348d7d6285bfaf0888b3d5341e0bc6ceb17e999`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75487833f3368eab2257a94a630b1880b487a3d9c985df44821377679a8630bf`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7d9d4001de6a0138bedcfe6908f4c986a615e32193ee3c092897d30647ed46`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 93.2 KB (93219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44e8730314266bff6d4bb59854d8785f0f8fe79a8da4a423ce7a6886f9fa63cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb443803c49e4d4189b2e400064620236d7b0aba3972dca81fa2dd4b2e294c5f`

```dockerfile
```

-	Layers:
	-	`sha256:84859747a36c49bfba821a162fe221c7cfe11f09235d8f7a8f66c8c32748ab80`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 3.9 MB (3935148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7067294bc3a8508f9cb372c5d48b39df12f9b701bafa3dbd11218ff8555282`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:396c89536fe6db1bc27165b5b3b01c1c141024b20e94ed056ca001ee7d489199
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
$ docker pull neurodebian@sha256:11f1d8a2c1ba5807309a84fe53239c15644decd7e0f952223fcfe8e28b9d40ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d931e73790091e29816ecd8a3b3bd13e50c1b635e8ec66b670304f41e9377f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
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
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e623044ed6d226bb08223597c0f380daf46067df42de48e52515dd8b6015bd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 6.3 MB (6309037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34ef8a3df44564cff9f91477c96045ed1348d5c6bacebb2c30da5ed1d67729`  
		Last Modified: Tue, 03 Dec 2024 02:32:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d9ecdc74a71cc7cfaf2b1635937b88fc90e48932874568379bd4948b83d9c0`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4420bbd6a1e5e4067d6048b9cfc560b9b39df72d87d4ed9e93ebb3c7f8be97e6`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 91.4 KB (91417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:813cab0e7d8d6a6d32eb156bb2a98ba13135a9efdefa45445c299cff634bb3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eddb8c244b0b5047058b014b003d153a1b272ae2e55f50361d6707a657d0ca`

```dockerfile
```

-	Layers:
	-	`sha256:c07968d16a78367e1d48530eb27283dfe91c39751a8b135ec9af329cb9dda337`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 3.6 MB (3559094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddfa355e9e60cc21afc4f6d9b0f6907ad2cd79edba64fdeafb408ff1ebf336c`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f70ccf1c4f8e34348cbd6dbdfdf30069e43ae372c6d6ae4183ee57c6cf6e7f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe90355c453a718b5f375561fdd4ffe5ee6d55f7254cf1b2b706984bfcd91d9a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
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
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:37cfe9a0d72ee56ff9cfbd3d6f54367b57a516bedd5b30b0d1a598123957ab2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3355433a01c656d9187644992eb02f399b926fd6998309ff3152bdd174664e0`

```dockerfile
```

-	Layers:
	-	`sha256:f01a69ba873a649d16109246e36645e9293f212711280454988268bed4add197`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 3.6 MB (3563973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bcd735f99065db42e22a630fcbdde19cc6d75b63789503857eba2885a0de8be`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 13.8 KB (13752 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:a6e34b9b3ef10febb3e68cb59e5d43a9cd4518aaaec42c9fb0eb764661ebac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356823f088987741ec801961eaf46491d407c63f5df550066164acb83a595dcd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
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
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c500b7e81fb48a2ca8dfb944bf05a4434b38906509b44c8230cb468350330652`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 6.6 MB (6636172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cba7baac1bbf19c4eff6cba1e463e4514023f61e5e4f99eabf003c60f53789`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbc8c8ecf4c50fb1afe9f838e8684a9f8283e6edf3aea752fba90ecdfb953c`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38faa38e98066ab42e204ada314c609783c4d1432e9755b2bcb597ed43dd599b`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 91.7 KB (91657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a39472daab1f7ad10eddf0cd67f8453f4675bbd31ed229cb77f9a601729e442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5077173fa2b440d42065a12b5c4ecbf78be9444e400aa418924ffe9cdeb599`

```dockerfile
```

-	Layers:
	-	`sha256:b9520b672b857555a8f6a7d165f2b5323247148278f458a7278373f979f2088f`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 3.6 MB (3556335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a715947ef1aeb942d19d5f3d425c0a032538f9e6b2ee6340f7ab1c249910cdb`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 13.6 KB (13599 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:e7c0d77acdd38391058bb428da4b25ac4b5d5b17dbc921ee7afb854783a1cc48
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
$ docker pull neurodebian@sha256:9cdfe6f90f096c5886af048cddf57f84f7131abc4faa5f65638d66c77660e090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dae39f0e2a61e2773abfc9d19efaff6e24355ae35e8f376529d52c260d4529`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
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
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114eb8c7559544e979c7bc06d71d09eaa2cd00debd8cf4f03a56d8104b7699b3`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 6.3 MB (6308996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80e11993394c1dc9aaa17af36dfa33cca39fa8e0caabe1b3bf52e80a34369c`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4eb1dc4c12753dfe02a45cea97e094916913c37268158aa3b340700e68143f`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12f43e28b0e223dee7e963ea7a4ad3a48f843457e481ee84cfb74772191cd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 91.4 KB (91443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405db61dc15551d8850b73eec4f6ecee2d15504c5d277afd2c8128e17ecf6611`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1bf2d8e93155ae981f2f562f22bf9918fdb877c66cffd35655fec1d9b1f39938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffd90ef4d3ae1ed5361af576f9d3f2c0d2a5754f07e470e32f3a78bc8bd6096`

```dockerfile
```

-	Layers:
	-	`sha256:9702d640d901ef7903e74e7c2b43af913d4f418a939adc866950dcedaf2a783a`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 3.6 MB (3559130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7bb223c6e89608e9722bf8101c7626ae5724ae67e6be3bab333911378929ca4`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c7ac4ef4afbf39509f7a22b31591f646ef72bc02b766b53e5fd512cdd67e0175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed54a230a0fd8bfde46f98be15f4d3b97ce2d877b842da7ab902c830cee5c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
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
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c880850a32196b5042f578dfb72c4fa93d1ee7ebd60d71fa4d5fbe19814c1ac`  
		Last Modified: Tue, 03 Dec 2024 06:18:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:22661e3cbf436b44b80103996ca2bd6577e74d6b1b8bebb5202171aadd46a284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d846bb8b6f1144a2d45721e8f45c30c3f32192c7a1ac72ca6b7268efa446fe48`

```dockerfile
```

-	Layers:
	-	`sha256:96771062d69621936e46943c2483b9fbc12aa2771b6c3722cb1035b36ef91682`  
		Last Modified: Tue, 03 Dec 2024 06:18:32 GMT  
		Size: 3.6 MB (3564009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c24f5aff628042c5046d45e533873a264167660d2769d5c6aa4aad04528fe9`  
		Last Modified: Tue, 03 Dec 2024 06:18:31 GMT  
		Size: 15.8 KB (15793 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a7f28e60fef8ae8c66fd2dba17b3f842cc070ff0f190ebc2bdf9a7a8be76fe7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a1f70a2c0871c021a308aded3c9b948de0de66faaa7121a2d269e4640fc96`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
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
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998bde38fb7afd531148bc5ada8932ba6909774db1014c810250d2fed9705c28`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 6.6 MB (6635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff379f8e9bb8d25d6e0f0189f738f8b022e1073b791de493bf8117cc6d281ae`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c1b51d89e4dd4797ba1c7a7da71a5c460240254b1e7853212c5b2e920c1af`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bc6338d9947bdf727b4f355b78ec884ccc098bacc03deb3d7965d5d04398bb`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 91.6 KB (91629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deb6e8c73557a116710e67686758ffb933b5075a0bed69a3dae3ca0be59627d`  
		Last Modified: Tue, 03 Dec 2024 02:28:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74f05ff960ca0068515281f926b0c25dbcf76375b4f99e58125b16a689b862ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d55b24693960716604398d554cbad7c385b5f86da205d5292975eeb67833ff`

```dockerfile
```

-	Layers:
	-	`sha256:74ca85f2e86db85f7b30f20d46e8e42be283a7b27e1b60976e0ff56e761fd5f2`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 3.6 MB (3556371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d03ff36e1583fd5288b7e43255d4ae49d2af7984f1801d3d5ea02eae17b0cc6`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:fe18aff0849b4e1df68d19c274695dfba5fbb0fdbda98a07358e3385501a4192
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
$ docker pull neurodebian@sha256:98224cdf0cb804f50833ffd343c2cace4d0620cc88d868ceb1cd6c3f0b1be796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a7eacd89d2e958b8a3b6aef1e1fb0af72893321723ca18a1b85f80c3421cf2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a11ff2a1535c8fa479a7c320a495994c3166965074adb19749bcc81e94a236`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 11.1 MB (11105069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bc8189aefd176e625a1f58b86ef8ef61308725ac86d6fd1c717e9b85da58b9`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b867fc96223e2170f08b1bddac268faf03b601fe9d00b5f0ce2da019d85986`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d8f54f537c07c9a80af694512b8f79eb12644da787978689d518b57ffc4c6a`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 101.2 KB (101202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aabe9a95821368dc3e33ae33e0f56d648947a2b242fdc099a2b34d153e0445a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39da91d5bdeb24c36f8303399cf2fc0e0d4932a1f08f7e211d96ff785428d3c`

```dockerfile
```

-	Layers:
	-	`sha256:803d69e4cc55c299148ef4158b0e946e3807a73af9024011dbd4a65f5afcb275`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 4.2 MB (4237043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4709aab7e44720ade9fd334c8d1c2c7cd35b6e7eda4f7d0f5bc30dc8ba85cf`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 13.7 KB (13692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:503b12cc63458348913441053b31b45bf94be1d0e08d898aaab1ee73d447c47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37149593973f1cc0e79d75464579d66456f41879964a0c0f3d2ba14e8d194e51`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fb46d4fbacbba6f0e034e8d65131a0ae5d99a9803eaa1223ca1a1cce020e44`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 11.1 MB (11105958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb47f993ab8f56d97d07ec72b6ec7643575396ff3eb0ac2e06dad8348b99fa6`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe4213d9e47272af07a9e329e0d77dfd006ade0e3035e1d7109e590c58f702`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd00afd1e307fc6212c5179f04ed778efeaa0b8d1c4d2f1cf0ef40961607d39`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d70b2455f8344e8e8324092bf06f83009f2f80bb01fe75818efb32a56e72b6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f454574e54a23090cf00dba92b65577480a93397a5a6de461e23e64b7a4e8db`

```dockerfile
```

-	Layers:
	-	`sha256:8dffb7f08ef77f3d5388260c476513166ccb0f27812ff4240ee86a096ec9498c`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 4.2 MB (4236648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d72e5d7a074b56de4153dcc7da35221212a240b3c5a178af2bf0a8025cebbe79`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:7c5a39a701d8dc66eaf4bf30d54a87c77d1efe5ef0ae96588400f6492cf26489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cf762d4dd883d16a90d46ee45855b8a8179cc4efbe9bcce674e18a1138a672`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef34bc916fc85979e50d28fbf87a379437236619f31787c6253f9be255cf615`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 11.5 MB (11500365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c264fff16245d2054954a0c0d6a4e94402f127fa2f336a10d500b8c9365f237`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3dc84c047211a70772b4b5cc81d0f696576da04dac87d3c77c6b01c0c40856`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987ef48478380284df1d15d0ce83cc3d2b348177e1967cb6995033830ebca434`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 101.1 KB (101064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7ef6b6b3b18b388c4c6a0a2dfe818b51ddf588fa06bc75068201bd43cfe08813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736fb535b3e23528fa401960e8323a637abd1360e60549f9d64c45929306706`

```dockerfile
```

-	Layers:
	-	`sha256:e6431df809d0774340669cb6df2591eb71e2812dafed6c7c91ed5684daf5da56`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 4.2 MB (4233503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d59b514ee3f01c9758a94082d2709cff01cd42599e7c253880f815b86314d4b6`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 13.7 KB (13665 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:978a8625452ab39d13e6a7f02fb3cfd9eb7f71df63e1c1a81c553c61ce2b6514
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
$ docker pull neurodebian@sha256:41bdb44a634f5e4f772e8b59e7a7acd006ddae9b568a2e99b51fb2e2c257ce8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8083ab6daad4423e11c61f0c92526f7aa8c68ed7275722f632c9a567a37d5079`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4769db03e4d35ea9c8cf75cfe915aed6f030961da59a336f4b4368ca4f71fca`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 11.1 MB (11105088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f91ca316c814418b68c407c49bea3fff42122da0c9c1893c000a54305d893e`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942eeb99ec88bc46a9080bd348da8680bbbb1a8b1edbd7f65059f75d8cd0cce0`  
		Last Modified: Tue, 03 Dec 2024 03:20:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80de4a826c59a53034b00bbe50abcf962f0854836822443071456f042f3ac96`  
		Last Modified: Tue, 03 Dec 2024 03:20:21 GMT  
		Size: 101.2 KB (101187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e891a80297e2f74d3274edf0b1c1de023918624816c8875663815aad0019c7`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7238d490a1ca5d396933462607fbbfb142601f035e62da4c4e3ed979bea56eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f78453b1ddeeb1ce16c0702886fa7638f014a6c09422da188ec507efaf3dc9`

```dockerfile
```

-	Layers:
	-	`sha256:e16018084601f4670cdd8bdfbd363f7ea4d46c886a0fbc2dfdbc68534065644b`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 4.2 MB (4237079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:589eabc43436ba0627092ce4ea2ab4f3e528dd1139609ee803094bd027690982`  
		Last Modified: Tue, 03 Dec 2024 03:20:21 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5b57e8e5b7dfb431cb05d5d58451cf4d3ee9a357b94f59f83e5b9ac1145bf342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af5264ab433e8d3e3e5f80bbc2d75ff8af4a6193418868592de413d174fa84c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fb46d4fbacbba6f0e034e8d65131a0ae5d99a9803eaa1223ca1a1cce020e44`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 11.1 MB (11105958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb47f993ab8f56d97d07ec72b6ec7643575396ff3eb0ac2e06dad8348b99fa6`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe4213d9e47272af07a9e329e0d77dfd006ade0e3035e1d7109e590c58f702`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd00afd1e307fc6212c5179f04ed778efeaa0b8d1c4d2f1cf0ef40961607d39`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f9c61c4532d29032e3956422cc71112cfe60ad7e4ac47495587c0586fa15ae`  
		Last Modified: Tue, 03 Dec 2024 06:16:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d72ce6d5735dec09088eba399b7d1a66d7bd4d6dbc1af841657fab98c25eb3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1d6814225bb1f6e768e113c59455e43f0865dfa5c32dff4a8129ce2f3aa20d`

```dockerfile
```

-	Layers:
	-	`sha256:beae995b856fc77a3fe49b4211e6c69ce9120213835d354b41972d306304b5cc`  
		Last Modified: Tue, 03 Dec 2024 06:16:35 GMT  
		Size: 4.2 MB (4236684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a560d37582a8d74f5745c75dd7ced712a4b381c5461cc2870f7b0e246b42bff`  
		Last Modified: Tue, 03 Dec 2024 06:16:35 GMT  
		Size: 15.9 KB (15861 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e9b7abc0bb54d79a9a24ffc0b81d00184d09f10f0016a5f72d2d693308ec24ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66280058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8063c68d8e3e84d7c47d6a92ddba4264f9d204fc2b35bd2a81bcb84a8ca282`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b65f3a96293e2cb168b19c54c2b62093b3728fddf28451b6b6232d90e106527`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 11.5 MB (11500368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c264fff16245d2054954a0c0d6a4e94402f127fa2f336a10d500b8c9365f237`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3dc84c047211a70772b4b5cc81d0f696576da04dac87d3c77c6b01c0c40856`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244a01f2463f793685cc01a57b4ce0420d030c5e38b8ce6a00c2f6813328436`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 101.1 KB (101065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb4dfbab157a0690d795d7386cf3563e5b4515abc4011077ce213843cb5c2d1`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:778a60719cc186db2508f107a4bda760adc002211fe26bac1dd1689b74a61152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4094e65772473b512ae8026ab0810de01b98dde7e8abaa654d59d8542c83d4e`

```dockerfile
```

-	Layers:
	-	`sha256:0a3e5db830790c929c589bf59f3b62306f609956fa0b2dd27ecb900bce3324cb`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 4.2 MB (4233539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e526f0f5199f5f0d41d0d602062811cff0642b5963d4c171bb89d35c5135ea`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 15.7 KB (15691 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:2f2ee431e155b1cbdf9193f76b66b200a715d206243e041e20ddc1e3ce5f4f29
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
$ docker pull neurodebian@sha256:0c7d59a5f8e1550b820a5027a093228b51c5e0d66456669e84947e7afef32a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97157fe06be6c40ed4369da113e6278119516d03dad788264ccf1e31b0c42a01`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950a82ed7125db9e9031ce90322ac9e66a78ed9482daf60f03df07a95a014541`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 11.3 MB (11266835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1b38f8cddfd22a2af98cec683daf6d65d23803957e5dd5dbe69f804a2a3f`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1a0dbd43a3757bda4754fd5c0f02f8548b6030e705dbbd50eb9023dd48b226`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff386c46e5b85cf021e16c77a07eeb3acc1c69637477e33c7f2e55475483934`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 93.1 KB (93138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fbe03585af1476fb2bbd2908efaa2b8ea83b4b68bf5f6bc58ef85f1e70eefc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97ad597ee27c7c3724f6aac33bc5a022ea24f97ad9d4d365a2b6f265f19a26b`

```dockerfile
```

-	Layers:
	-	`sha256:8ad1888ebd680f37d0b7a3511d4c5b1c740b11d503c347ba76058a40d228ad59`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 3.9 MB (3937231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b9c5da835238bc532ec29b931a715c71c311204760c6932ba56679ca5e5184`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 14.0 KB (14000 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5eb8620046a2e02bee05f9dcb5abf9a7ea018cba00b6a5b19d10a4d20b2c25a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da76854b721e08ea18a3c19fb37d170beaeeec6f442c69d981d3a205fd3692bc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d6f082b94e725149735aff5f39abf2a5c1faa04f4f35829c2b04bcf36fdb0`  
		Last Modified: Tue, 03 Dec 2024 06:16:59 GMT  
		Size: 11.2 MB (11232475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7164374defb4bad306066d94c7dac571980f047bf262c550c04b585b492527`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a1000d937bcfa52ee6cff54a54a79274765aab42bb61041dba4d40c8ea00a`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab49634abc6db7b16ad6e4f6d1bd12260c9a0555ba2d16c5abca22782e40f3`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fee13f802494da87f2824243b1ef6ba160c30fc88f4bb898d47172978292f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82beb41f84b93d8e674c7203b9009b5d27ade9c1eda441be5ac865312e51e9aa`

```dockerfile
```

-	Layers:
	-	`sha256:942f1434e7601bc69e26b7cade69d8c6c91abbc09905aa7e29e161a332fa32cc`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 3.9 MB (3937484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a95f2482d505abe9ca79152c5fa27d45a5ecbb3e300f19487154106eb2c2a20`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:7be9f025a968af1334c291d8942067638fecdb9ae6aa2e02ac3a5409c41a37a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd04204578e3c76cda4b47577a26bbace9322f371a285123aa1fc902be6a98a1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590fcc30f6c50f7ad71c3858d2239c46376094eaf1a12e0ef65a4673f5e763d5`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 11.7 MB (11689045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbe2a76c7a0519eb8d714422348d7d6285bfaf0888b3d5341e0bc6ceb17e999`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75487833f3368eab2257a94a630b1880b487a3d9c985df44821377679a8630bf`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7d9d4001de6a0138bedcfe6908f4c986a615e32193ee3c092897d30647ed46`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 93.2 KB (93219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44e8730314266bff6d4bb59854d8785f0f8fe79a8da4a423ce7a6886f9fa63cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb443803c49e4d4189b2e400064620236d7b0aba3972dca81fa2dd4b2e294c5f`

```dockerfile
```

-	Layers:
	-	`sha256:84859747a36c49bfba821a162fe221c7cfe11f09235d8f7a8f66c8c32748ab80`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 3.9 MB (3935148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7067294bc3a8508f9cb372c5d48b39df12f9b701bafa3dbd11218ff8555282`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:81f633276b9be30fa1dd00b0723598ca82c4071e30da9746fc744a70d1d430fd
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
$ docker pull neurodebian@sha256:f0b826db0485d7e82be034c6c5e7edf87df12d265d6677d054029eca4e93eb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7686c9b19aef29cd8dbd901aef411bfa8220e559879f8633d2b8abd2cc429f7f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3cc0f98744a051a1a5f2afd9efb44ebed4fa17eb3c1dddb60d9c9400c80ab2`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 11.3 MB (11266780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ba287ed08d01881207dca39c00528deb3fdc3f2d81914037be7b1cfdbe874d`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150a6037915fb13285e5895a6a1c62c6afc1704844f3fba6208d25301de77e56`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8683715aebd7fa532f695293a9e651f0864ce67665530642a85014fd00d60f96`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 93.2 KB (93152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9738867365afce7f70b32c401344176aad5e654c99fb07a9333af858e584b4e9`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5ea80b90c3a2e9c97601511fd1dc77bf211dee1d51e558aa1fda464ca36368ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33c8834e62878218057544094ea5fe3dd9746688832eccb7832c6c514dd2f1`

```dockerfile
```

-	Layers:
	-	`sha256:7bf28a7d462fb022e11d07e4097edcfda51808238332b04d7be6307f77970fb9`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 3.9 MB (3937271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2408a1585fa162bca505495ed4028662a915c5800c5ec73c3024bf5a965ac6d9`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8727cc1156f0afd9f41a4c982dec32a7669106b1396116e3bf6adae8aa7f4756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52ed086311e71cb3ca17d2f26956adde08dc02a426a23d623a6b6b455dc26b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d6f082b94e725149735aff5f39abf2a5c1faa04f4f35829c2b04bcf36fdb0`  
		Last Modified: Tue, 03 Dec 2024 06:16:59 GMT  
		Size: 11.2 MB (11232475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7164374defb4bad306066d94c7dac571980f047bf262c550c04b585b492527`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a1000d937bcfa52ee6cff54a54a79274765aab42bb61041dba4d40c8ea00a`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab49634abc6db7b16ad6e4f6d1bd12260c9a0555ba2d16c5abca22782e40f3`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfadfcf78518bb3680188a8aa8e9b4e03dd0606fff44a59bb7c8d5499eaf1b4`  
		Last Modified: Tue, 03 Dec 2024 06:17:11 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff00f65b3308cbfe02001d7be3d5101574bcafc13cd2ed12fb2c5ea4a3f904a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88092ab67db4a2a365b3756e65b7129bc9d0f9970f46cee3556212d286bc0541`

```dockerfile
```

-	Layers:
	-	`sha256:5196f61854393e3f4bd1507046c2519f7c7085fc551d84440d34fc98c60437db`  
		Last Modified: Tue, 03 Dec 2024 06:17:11 GMT  
		Size: 3.9 MB (3937524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfdbf730785a3a5e3830386fbec8ccf928bede15706f942762a042e778e73df6`  
		Last Modified: Tue, 03 Dec 2024 06:17:10 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:8dc7482bab5a6e73520137dab2efc0ea2e1cc8fc7b00a55bed98c1f0f08d9b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c795e80457b17a40c2f0ba40bb9b3c56514d9bd56e840230b6cec3cf737c4acb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4351f3571feee02247d67c5362a4118390ace6f8c203163c4f98131c109f39`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 11.7 MB (11688949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47502da2499b6aa6bf2b0b61829d4882722d17064ba80d8bb48ea95f18de4d5d`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807895808115d1d32826306aed408a2b386e021fe7a1a16f92541a7466a2bc9`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ae4b46bcce38d9c1ec20a3d33ac2e841511ae54438cfaafe1d94b487dcc6b0`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 93.2 KB (93220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f86ac460bc7c2375830f2b95cf8a012950443b99acbd0fc9bfc962541710a1`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ddd3208bdcab3b163d0e37e9f5c42ceb55651e14db8e8389f4adaa1ae19865fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a502d814818aeb638b6714649752b3a5f5ef284ca7087a822e7014812d9e26`

```dockerfile
```

-	Layers:
	-	`sha256:1d21298306b6c34fabffe2598c235ed691faa6d0a6279c00194aa06ecb984533`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 3.9 MB (3935188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ebb9243e1a48616e3d08d94ef366bbf4796762ab8c72db1e88b6d07afdce1d`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:bbc3ded260e52ab68dea79f0a8860a9853977c5b81a7cbc61da66dd3e73e464d
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
$ docker pull neurodebian@sha256:22ba4c69dfacb7993f7fcf3708c2ec38e7a15ed1bed206d226c5160e47273847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fd9c4b14dc331719047f53a409b7b3093d384a6ff135c95b14e664c6b43885`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
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
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31fa211153a834040c35ecc855708df74ae143e0f067f5f29d4299bec783171`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 6.3 MB (6309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759be46808786c18908d758383834044fed05ddaf818585877931072aaa3bea3`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9340f215c3f9e9497b17c7dcc21314a53d5553d70c1a45f9ecd9663aa523c`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809dd25b48752fba0eeac0fcf5c38a88f0e12b0db0b022acf82ae7fafd98800f`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 91.4 KB (91435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b22d1f83ebacbb4392e9e1ec31a9e0902f3f7a2cde703ee063fc39bfcd1b648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9d1493dabbbd58df5573fa3c3dc733bfb235815353be42c104a85da39f4758`

```dockerfile
```

-	Layers:
	-	`sha256:8cfad2f41e51e9ca8348d9d7852f9a0f81c5d0a482874503181c168442d46e8d`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 3.6 MB (3564266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291ee8d275476a4f56b64a69bb3c484a527878d207b0f47533dc5df2c24f9458`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1401e84e1f34ba3fec0eccc60bfdb562ec886b1705aeb33459074a37aed25700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58723605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547bcc904f8cc765088dc02b9c5eac15bece1c36242ba056fa8894fa557231aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
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
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4b78788290c99294a51ceca1957d8eb6e9e849177decb1f820324a7d85b171a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c170b6bf1352da87527070a521d5bca904ee0e113091bee7260deb2c47e958`

```dockerfile
```

-	Layers:
	-	`sha256:60730bef667d6b97b826f735f2547ce96c7c51f072bed45993eb690ead280fc9`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 3.6 MB (3569145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a78c16c7a4e8d937b184fa40339df44fa15f714b5d50ea63d627b3763ab773`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 13.8 KB (13791 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:0c302d3d91a06e0de1ae44728e6c238af8f332b079b0dde357761280c7738727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59685891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eda70426935cafff4ae79341debf8d16acdb137a79c79aaf95a4e89287e257`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
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
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07d21ec843fdae56608290e710928213278f433f216169549f4105b0b7adcde`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 6.6 MB (6636002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790ba6a36bbd0ddde077446c337522dff4905079f146ba4f81c5f1b1ba01508e`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f988e696d1fd940f6f8a41f61db71109214ffa05a741e7ad19280fab3317b7a6`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7105d8b802d7cbbf45432b1a9323e287ee890f7b63ac52b16e684f8aa59aa436`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 91.6 KB (91615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:640e8a6c2b29256a11a97f4fab868b83769f471a9a56a787f0520ea21d8560d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0a2cb4139fdbf18dfb086e8db81f463979da7309ce33c42798424276477172`

```dockerfile
```

-	Layers:
	-	`sha256:13a56528e8fb58e39de0f1b02fd41e36f2ce6114df32afe325634c478c2d46c0`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 3.6 MB (3561502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda46b32b1387c0fd07559cd518cb696c94a4a839d171f21cf6124f57cee113a`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:a78a1c95462db7bf414f96ce328616fe968aac57b876af3362c3e4b47cdb81f1
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
$ docker pull neurodebian@sha256:dc2ee078717e5cd6782de72121bcc9936ef63cb0981ca8e921754737a77980e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf94ef9a8ab87a336dec4a29f001d654de0e935525f16a071a00515579aff5be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
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
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507e5811b953238ff193b1168d33f51c6e9d529f200a09d5a7cacc81a3cc8c3`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 6.3 MB (6309097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53110b5d9fe921d17db007a1ddcf5a14b209223be44404d7367639af0432a720`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073121ed00d2745775e339f48a955b95fe1cf8f720671dcb447fc1ed84db92f`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4d13654e7924d6b2b37ec66b136d37c2be5c0336ea4c05ed6c366e2a4fd3f`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 91.4 KB (91421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8461a91abccfb6a0564642a71b515e4966ed0f07a5adb19dea1de7fda249aaf0`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7de7481f3bac1a3622e0eed2ca47e8f02312431429159b58502dfc6e1b23d76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bcddfe5efc17cf322b5dd0859093bb6b3567c32ae516fe9b443b80a0541765`

```dockerfile
```

-	Layers:
	-	`sha256:70ad6f08346ad337d0f9e32f7ec11b22ad0d818d1df8a6aee0a4052c1cd75b1d`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 3.6 MB (3564302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97d1de4b535410fddab63f0e6af15dfaa00cec28ba8c0fde0a15678db848775`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 15.7 KB (15692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:17fe10b8e293faa659d945422ff3aaf4c7e6e1f387d707d314802beb80b71a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d39b737a8ff196e533cfc0ffb9a1412e43594be8673e8c0da6c05751f91ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
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
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da18a25c93d7133b2d4097e549a323142182e4dd20d54315927b6bd6573eb0f1`  
		Last Modified: Tue, 03 Dec 2024 06:17:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c77a0b2714832915027f323e1b1215a7ec8179d2324362662d8283e9cad88fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7509c00ee24dafaacefc91ed80721178d33398b768fb59515c8052afde5a23`

```dockerfile
```

-	Layers:
	-	`sha256:27c4680740117658f3a6d274e90c1bc193f9aed297af2e9c8658296f77a30654`  
		Last Modified: Tue, 03 Dec 2024 06:17:55 GMT  
		Size: 3.6 MB (3569181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37b47d54c077c2ac6d602d5b546c068ab8e54b2c34442bb70ec6ca92ca86216`  
		Last Modified: Tue, 03 Dec 2024 06:17:54 GMT  
		Size: 15.8 KB (15832 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:58259995e2bf23d42df018ba25ba3a67372a2422fdc7914cc5a132eee35433fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59686248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2739463941d7f2c81e9dcf2985fa548a020146336a6608a92ab4a327c6ebdf7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
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
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e886790f9afca68021d7c75698a1217a115b9cc1ad35a2810b2d8b0ad55f3`  
		Last Modified: Tue, 03 Dec 2024 02:28:32 GMT  
		Size: 6.6 MB (6635953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250eb870a6e7d1ba2c1af2ca41ebfa2fb763a5be83d1710296ff798161459c4`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143e50a785fba3cd83cef1e55edff4f0d54e965cede0048ee57f596d5735e0a`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92cccb8507bf0ea24147acd06ddac399895aa65bc91c02c25f650bd8c41174`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 91.6 KB (91598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c62cefd1610f7333f6f871c1794e559b2115e00c5863260f9ddedd99769cf8`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7260c43f0f9e6c3c34410fdfc970a0d4fcc49429c791e26905b3e6bfca89798c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c94c1a91810b80643dc3cac6052e446072381fd31485d5f5196bd3ea6e0cb1`

```dockerfile
```

-	Layers:
	-	`sha256:deab7f2dbd81f35b295f26a1874c4c6ce9cea7f2c767ec20cdf21e9e17c46086`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 3.6 MB (3561538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2606e6a1a87f3ded6407b0d5258d8218f3da05be49ac5201a62941c4296cdb35`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:8bcdb02c955c552289fb14468e3d0eccac712d0a170f1fff5601f3f3af9d8a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0c6cb45ac1cfbe06c47f14d684929ff5f5907ef7f083c360195214c3ac6aca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1335fc867ea7b822d1b6882dc96ad365e5cc4643152d61c5fc8a7bc5f85a988`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49fa7316f784f5cf307546c8c97bd1b9f3a1fd2943c27fceb71ec2dd6409f48`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 5.4 MB (5360278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7c65bbf482527df64ccec5d79c08cb11cf2d1f4054f4977e47dad48ff8435`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e678bedd7e50e1ba3e947302d4a3badb36d988b369aab4b47c1fa78259c23552`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9792897da4dcee6732822377f46272804fb1e9b7f31dd60d17894a127edb839`  
		Last Modified: Wed, 16 Oct 2024 16:13:43 GMT  
		Size: 105.3 KB (105327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848d25161f517586e1457fc807e778d3305bad2daae744ec21fc37849f68173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820220dbbd11c6d8f3103b1a3ed83da871c77d7b02f18798badcf3237303dcae`

```dockerfile
```

-	Layers:
	-	`sha256:27970857ec501c025d084e20e5352a5d5ddc17824cc89a85f49e7025cdcb4a02`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849d52e89f42eba3812416ede3dd4d1badb9a69a5a982f874e39c325041eb9a2`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 13.4 KB (13444 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1a3f2e41cb72abdd7dcab281d6513ce2dc547865fa3b4ba0776bd58ea8a5de97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2c98411bfbdccf11946d245a8061c56c6ce058ada6075d911256dd80fadff8`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1f3f34f75e1a4bc32b849a9ffc880a30708443a7fdc0da8a50c2e90180094f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5772b0ce1260ce48effc24ad2f6bdefdb4674ee0d585774b4464dfdaa8df07f`

```dockerfile
```

-	Layers:
	-	`sha256:71ee94546588c20b92a492d129395aac336c0ae8677f9f8048b6890a1e640901`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa10decb4cbaa5f56d95540086539ce9a7bfee79f97ecf26a18eb6160c482bbd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:e1b1eebaa7be7a7ae8986f10c005fbaacce6a33e73c7193cef12dee6f49b40b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ddc9018acf97b1f5814caa6cde3c3d36dc386f558589639e00bd07b61c4ceed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02507bb93b25ace19e3dbcf9e5a746ee64169a6e6641918f946da8db0e4d17b`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4005701787afe01df59207e8d67264732bba189629db1779b4ffa79571550`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 5.4 MB (5360288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6862ce93e83033ea4be1d4f8bd4ea70b498c761c3664782d446af47aa9926b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce53e76a062f11aaecdb2eaab737adaf3dfe235440d4e34cfa7bd8bc8634e70`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f662144d756ef598c43631f18e5a5aa12b2a8e2c719e17635359530cbf9a9b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 105.3 KB (105328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c113f4052eb4bc0e89d69bbfef200be8e9cc348104fc8ae5bc167ebdf6ac683`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fdd9dd95911aad8010d1bd7b668cfc9886a64e712c66aeab16529edd5642e84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419484197e2594f495dc65df02606517cfd33b3e8fb27db49620e293bfb8facc`

```dockerfile
```

-	Layers:
	-	`sha256:96b650f1cbef5c5dbf1b7069ca052e04734ab3f40d4e9ed771e9496d60fd999e`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 2.0 MB (2002687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdacbdc41b77b356c35fb81b7e0fcf121e4d6c1b38d2d913103141df6f522c9a`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b3f6acebf8e01d4ccb64904ddb4e553df094a7fb6223b50f683882a0756a284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9be140461e203793948a95c87503859fadcb667866ac155c79cf9aea88c1edf`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4975400a8d7cbc9b67c0e50618fd95fa63506aa713da18a3da28accdeb57768`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b26186688e44f87210438ddae17d14c31f634b630c497d04013b36ec09d92089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b3564811c260795602aab1de18bc1a0e9abcc4a1a00d4aa08bf2c13102fd50`

```dockerfile
```

-	Layers:
	-	`sha256:5f09b22f2f9e9d8a1f0ccc85ccd622a779576a09f4ec13d286e85c8831be03eb`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 2.0 MB (2002915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc6326745662ee2e02b1d747a2d2ba13494721e28def82decf35cf47a1614ff`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 15.8 KB (15808 bytes)  
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
$ docker pull neurodebian@sha256:658b81fc7b6abab8f6c7ec216a34eedec275c523b628a5597c9bce280567e964
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:dff773b7560d263c582e2b4a10cb710f42a1c3c52c64ea8a04817cd0308c762a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97e0f663f97c61d8d3b77245c102959f22f0cdb0c658b0f8a911affbc6c77e9`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bb8d306692844672bbfa1d36b12ac9e70dcba3afed1b205da716bd98445dfd`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 3.6 MB (3558848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060c4cfbe42dcf01c60754dde056484b11eb0bf692306f5b6e056073296c5dbd`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10363b67b7c7df5a7f19aeb132cc2e1c148a4850360cbfea065de604e7e84689`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148844dcd0fea449935fdfbce9218162d22b312bdf46e3e6b3944aacbf3d4402`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 101.6 KB (101627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0dd7607b772e7d3e7a9f3c08dcd17fe3fd5d72058d713f657cae66f6cd6c0b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2000857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6499b40b283bd5ef8afc18820da824ee815169303bba4e1cef554e42997c6f27`

```dockerfile
```

-	Layers:
	-	`sha256:912e8b547af7012c23de9e51dad8c0b49a0297f34835163f0a7c0c466ac833f6`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 2.0 MB (1987197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50eac1b2f08d5d06cf4f78d38044ff517d06861bd698f3072184621c47feb780`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d64f68ae17f5144e471f9a21a1cda36c1b06ec1f9b28334d51b36756f721afc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40fc3afe6374d9c363c91f2623c230a34460eefc40c745d48d530be8be422f5`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c806577d234470cc5e1375c6c84e7102c2e92ed2f155ce9a119a4b67e98f9e3`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 3.6 MB (3557863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5dc9f05589119104912fa1a1717ff92659e13dab1440dc6b266b58957e5ee8`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc2614b4bbf71177097aa4d12c46d11d7578598e10aa3592123e9463cdfb0e7`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2df2b4e0bcd2792b731ac676570a2eeed647f45c932ddece55a8243a41bca9`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 102.2 KB (102155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fadec3f89a7e65d06897f8d31756c5c2b70d389671fc741c2ccb854732c6950a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b683ca6c0f1e2df2c80bea9c23df15d7ead46960c997d86d5ecde29072f03e7a`

```dockerfile
```

-	Layers:
	-	`sha256:8f17c09c31cf4b5cd87bde14628854326c2007d643625d168d5ed82a41251647`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 2.0 MB (1988242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc91794bcf6ed620350bcd79c932cb607a78ee37e21fb3a7ac0cc318172128e`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:59016cc49c2abfc881a3b7f98272c830ed6702b068e3793522e63aea1de703ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:67d3460643d6b26642406b01ceb9fc59c13a5d81cebb8e2e236091782d0bc89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e663e38b1ea80eb82dd0de3b799e8cc8de027247ac364f751d674fdff895817f`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29805511ed58135c0cced999bd142320069a543e7cff17820e8850ce00ba67d9`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 3.6 MB (3558831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5beb5ddb9eb8c69b9e51380e1333941f9a3383cb298e38c08ce1da1560b752d`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d288e9927a5384721587c8026d993fd091363f600d2c85c7d71a491a54c19b94`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d58661c2356672d5d22061624f076c4d9973587b3fda3a1fdffc710b3713d`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 101.6 KB (101613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfb151160d7106e163f969786f632abffbcd12e2addd8a1bb2065a701fb8a78`  
		Last Modified: Tue, 03 Dec 2024 02:31:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:388ad092ea4c672ffd86a98ec7837c638279e8131dd255ad16585091b1f17732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24755e2295c3813efe4eb005ced93eb41d9f3d212c725d79b577a930735464f5`

```dockerfile
```

-	Layers:
	-	`sha256:7f9c1aebb86c594c8832946485244dadee636144bbe25e29085eb0cc6d4e0eca`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 2.0 MB (1987233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d438d90a9e8992acc29bcca44911e036312b25385ab8a97f18d2902139fe79`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3115bcb5eab088a991b0972bf07c6ab93b32a8106bae583c3b87c63fb59f5bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c92f5f1dd1ef10ea3757500f3a6a9d0363b5b0670f49b869ec33f67f84c0b03`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c806577d234470cc5e1375c6c84e7102c2e92ed2f155ce9a119a4b67e98f9e3`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 3.6 MB (3557863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5dc9f05589119104912fa1a1717ff92659e13dab1440dc6b266b58957e5ee8`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc2614b4bbf71177097aa4d12c46d11d7578598e10aa3592123e9463cdfb0e7`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2df2b4e0bcd2792b731ac676570a2eeed647f45c932ddece55a8243a41bca9`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 102.2 KB (102155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285d29c45e6ed67911b928eeedda3837b4aa0fb0c4f54c6b1fc3cc5b80539494`  
		Last Modified: Tue, 03 Dec 2024 06:16:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:962a5986a3ecef9ad02e63677ab36ae8aaccb2752411b758ed8b69dba956f914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b395745909e449324cf5858c545fe8d7601ab6cec875cff3c6529d80c36754a5`

```dockerfile
```

-	Layers:
	-	`sha256:266eee23eb9f7320c750bc0576810f902ecbd111643a9682a5f89bcf08049865`  
		Last Modified: Tue, 03 Dec 2024 06:16:00 GMT  
		Size: 2.0 MB (1988278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9676ba9bc0661d12309280a6c4a0b4719091d811cab7dc686ec2953c8cce7ca4`  
		Last Modified: Tue, 03 Dec 2024 06:16:00 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:658b81fc7b6abab8f6c7ec216a34eedec275c523b628a5597c9bce280567e964
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:dff773b7560d263c582e2b4a10cb710f42a1c3c52c64ea8a04817cd0308c762a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97e0f663f97c61d8d3b77245c102959f22f0cdb0c658b0f8a911affbc6c77e9`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bb8d306692844672bbfa1d36b12ac9e70dcba3afed1b205da716bd98445dfd`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 3.6 MB (3558848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060c4cfbe42dcf01c60754dde056484b11eb0bf692306f5b6e056073296c5dbd`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10363b67b7c7df5a7f19aeb132cc2e1c148a4850360cbfea065de604e7e84689`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148844dcd0fea449935fdfbce9218162d22b312bdf46e3e6b3944aacbf3d4402`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 101.6 KB (101627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0dd7607b772e7d3e7a9f3c08dcd17fe3fd5d72058d713f657cae66f6cd6c0b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2000857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6499b40b283bd5ef8afc18820da824ee815169303bba4e1cef554e42997c6f27`

```dockerfile
```

-	Layers:
	-	`sha256:912e8b547af7012c23de9e51dad8c0b49a0297f34835163f0a7c0c466ac833f6`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 2.0 MB (1987197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50eac1b2f08d5d06cf4f78d38044ff517d06861bd698f3072184621c47feb780`  
		Last Modified: Tue, 03 Dec 2024 02:31:15 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d64f68ae17f5144e471f9a21a1cda36c1b06ec1f9b28334d51b36756f721afc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40fc3afe6374d9c363c91f2623c230a34460eefc40c745d48d530be8be422f5`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c806577d234470cc5e1375c6c84e7102c2e92ed2f155ce9a119a4b67e98f9e3`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 3.6 MB (3557863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5dc9f05589119104912fa1a1717ff92659e13dab1440dc6b266b58957e5ee8`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc2614b4bbf71177097aa4d12c46d11d7578598e10aa3592123e9463cdfb0e7`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2df2b4e0bcd2792b731ac676570a2eeed647f45c932ddece55a8243a41bca9`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 102.2 KB (102155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fadec3f89a7e65d06897f8d31756c5c2b70d389671fc741c2ccb854732c6950a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b683ca6c0f1e2df2c80bea9c23df15d7ead46960c997d86d5ecde29072f03e7a`

```dockerfile
```

-	Layers:
	-	`sha256:8f17c09c31cf4b5cd87bde14628854326c2007d643625d168d5ed82a41251647`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 2.0 MB (1988242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc91794bcf6ed620350bcd79c932cb607a78ee37e21fb3a7ac0cc318172128e`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:59016cc49c2abfc881a3b7f98272c830ed6702b068e3793522e63aea1de703ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:67d3460643d6b26642406b01ceb9fc59c13a5d81cebb8e2e236091782d0bc89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e663e38b1ea80eb82dd0de3b799e8cc8de027247ac364f751d674fdff895817f`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29805511ed58135c0cced999bd142320069a543e7cff17820e8850ce00ba67d9`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 3.6 MB (3558831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5beb5ddb9eb8c69b9e51380e1333941f9a3383cb298e38c08ce1da1560b752d`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d288e9927a5384721587c8026d993fd091363f600d2c85c7d71a491a54c19b94`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d58661c2356672d5d22061624f076c4d9973587b3fda3a1fdffc710b3713d`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 101.6 KB (101613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfb151160d7106e163f969786f632abffbcd12e2addd8a1bb2065a701fb8a78`  
		Last Modified: Tue, 03 Dec 2024 02:31:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:388ad092ea4c672ffd86a98ec7837c638279e8131dd255ad16585091b1f17732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24755e2295c3813efe4eb005ced93eb41d9f3d212c725d79b577a930735464f5`

```dockerfile
```

-	Layers:
	-	`sha256:7f9c1aebb86c594c8832946485244dadee636144bbe25e29085eb0cc6d4e0eca`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 2.0 MB (1987233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d438d90a9e8992acc29bcca44911e036312b25385ab8a97f18d2902139fe79`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3115bcb5eab088a991b0972bf07c6ab93b32a8106bae583c3b87c63fb59f5bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c92f5f1dd1ef10ea3757500f3a6a9d0363b5b0670f49b869ec33f67f84c0b03`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c806577d234470cc5e1375c6c84e7102c2e92ed2f155ce9a119a4b67e98f9e3`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 3.6 MB (3557863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5dc9f05589119104912fa1a1717ff92659e13dab1440dc6b266b58957e5ee8`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc2614b4bbf71177097aa4d12c46d11d7578598e10aa3592123e9463cdfb0e7`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2df2b4e0bcd2792b731ac676570a2eeed647f45c932ddece55a8243a41bca9`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 102.2 KB (102155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285d29c45e6ed67911b928eeedda3837b4aa0fb0c4f54c6b1fc3cc5b80539494`  
		Last Modified: Tue, 03 Dec 2024 06:16:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:962a5986a3ecef9ad02e63677ab36ae8aaccb2752411b758ed8b69dba956f914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b395745909e449324cf5858c545fe8d7601ab6cec875cff3c6529d80c36754a5`

```dockerfile
```

-	Layers:
	-	`sha256:266eee23eb9f7320c750bc0576810f902ecbd111643a9682a5f89bcf08049865`  
		Last Modified: Tue, 03 Dec 2024 06:16:00 GMT  
		Size: 2.0 MB (1988278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9676ba9bc0661d12309280a6c4a0b4719091d811cab7dc686ec2953c8cce7ca4`  
		Last Modified: Tue, 03 Dec 2024 06:16:00 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:81f633276b9be30fa1dd00b0723598ca82c4071e30da9746fc744a70d1d430fd
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
$ docker pull neurodebian@sha256:f0b826db0485d7e82be034c6c5e7edf87df12d265d6677d054029eca4e93eb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7686c9b19aef29cd8dbd901aef411bfa8220e559879f8633d2b8abd2cc429f7f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3cc0f98744a051a1a5f2afd9efb44ebed4fa17eb3c1dddb60d9c9400c80ab2`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 11.3 MB (11266780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ba287ed08d01881207dca39c00528deb3fdc3f2d81914037be7b1cfdbe874d`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150a6037915fb13285e5895a6a1c62c6afc1704844f3fba6208d25301de77e56`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8683715aebd7fa532f695293a9e651f0864ce67665530642a85014fd00d60f96`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 93.2 KB (93152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9738867365afce7f70b32c401344176aad5e654c99fb07a9333af858e584b4e9`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5ea80b90c3a2e9c97601511fd1dc77bf211dee1d51e558aa1fda464ca36368ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33c8834e62878218057544094ea5fe3dd9746688832eccb7832c6c514dd2f1`

```dockerfile
```

-	Layers:
	-	`sha256:7bf28a7d462fb022e11d07e4097edcfda51808238332b04d7be6307f77970fb9`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 3.9 MB (3937271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2408a1585fa162bca505495ed4028662a915c5800c5ec73c3024bf5a965ac6d9`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8727cc1156f0afd9f41a4c982dec32a7669106b1396116e3bf6adae8aa7f4756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52ed086311e71cb3ca17d2f26956adde08dc02a426a23d623a6b6b455dc26b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d6f082b94e725149735aff5f39abf2a5c1faa04f4f35829c2b04bcf36fdb0`  
		Last Modified: Tue, 03 Dec 2024 06:16:59 GMT  
		Size: 11.2 MB (11232475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7164374defb4bad306066d94c7dac571980f047bf262c550c04b585b492527`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a1000d937bcfa52ee6cff54a54a79274765aab42bb61041dba4d40c8ea00a`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab49634abc6db7b16ad6e4f6d1bd12260c9a0555ba2d16c5abca22782e40f3`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfadfcf78518bb3680188a8aa8e9b4e03dd0606fff44a59bb7c8d5499eaf1b4`  
		Last Modified: Tue, 03 Dec 2024 06:17:11 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff00f65b3308cbfe02001d7be3d5101574bcafc13cd2ed12fb2c5ea4a3f904a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88092ab67db4a2a365b3756e65b7129bc9d0f9970f46cee3556212d286bc0541`

```dockerfile
```

-	Layers:
	-	`sha256:5196f61854393e3f4bd1507046c2519f7c7085fc551d84440d34fc98c60437db`  
		Last Modified: Tue, 03 Dec 2024 06:17:11 GMT  
		Size: 3.9 MB (3937524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfdbf730785a3a5e3830386fbec8ccf928bede15706f942762a042e778e73df6`  
		Last Modified: Tue, 03 Dec 2024 06:17:10 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:8dc7482bab5a6e73520137dab2efc0ea2e1cc8fc7b00a55bed98c1f0f08d9b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c795e80457b17a40c2f0ba40bb9b3c56514d9bd56e840230b6cec3cf737c4acb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4351f3571feee02247d67c5362a4118390ace6f8c203163c4f98131c109f39`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 11.7 MB (11688949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47502da2499b6aa6bf2b0b61829d4882722d17064ba80d8bb48ea95f18de4d5d`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807895808115d1d32826306aed408a2b386e021fe7a1a16f92541a7466a2bc9`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ae4b46bcce38d9c1ec20a3d33ac2e841511ae54438cfaafe1d94b487dcc6b0`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 93.2 KB (93220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f86ac460bc7c2375830f2b95cf8a012950443b99acbd0fc9bfc962541710a1`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ddd3208bdcab3b163d0e37e9f5c42ceb55651e14db8e8389f4adaa1ae19865fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a502d814818aeb638b6714649752b3a5f5ef284ca7087a822e7014812d9e26`

```dockerfile
```

-	Layers:
	-	`sha256:1d21298306b6c34fabffe2598c235ed691faa6d0a6279c00194aa06ecb984533`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 3.9 MB (3935188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ebb9243e1a48616e3d08d94ef366bbf4796762ab8c72db1e88b6d07afdce1d`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:396c89536fe6db1bc27165b5b3b01c1c141024b20e94ed056ca001ee7d489199
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
$ docker pull neurodebian@sha256:11f1d8a2c1ba5807309a84fe53239c15644decd7e0f952223fcfe8e28b9d40ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d931e73790091e29816ecd8a3b3bd13e50c1b635e8ec66b670304f41e9377f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
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
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e623044ed6d226bb08223597c0f380daf46067df42de48e52515dd8b6015bd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 6.3 MB (6309037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34ef8a3df44564cff9f91477c96045ed1348d5c6bacebb2c30da5ed1d67729`  
		Last Modified: Tue, 03 Dec 2024 02:32:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d9ecdc74a71cc7cfaf2b1635937b88fc90e48932874568379bd4948b83d9c0`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4420bbd6a1e5e4067d6048b9cfc560b9b39df72d87d4ed9e93ebb3c7f8be97e6`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 91.4 KB (91417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:813cab0e7d8d6a6d32eb156bb2a98ba13135a9efdefa45445c299cff634bb3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eddb8c244b0b5047058b014b003d153a1b272ae2e55f50361d6707a657d0ca`

```dockerfile
```

-	Layers:
	-	`sha256:c07968d16a78367e1d48530eb27283dfe91c39751a8b135ec9af329cb9dda337`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 3.6 MB (3559094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddfa355e9e60cc21afc4f6d9b0f6907ad2cd79edba64fdeafb408ff1ebf336c`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f70ccf1c4f8e34348cbd6dbdfdf30069e43ae372c6d6ae4183ee57c6cf6e7f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe90355c453a718b5f375561fdd4ffe5ee6d55f7254cf1b2b706984bfcd91d9a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
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
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:37cfe9a0d72ee56ff9cfbd3d6f54367b57a516bedd5b30b0d1a598123957ab2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3355433a01c656d9187644992eb02f399b926fd6998309ff3152bdd174664e0`

```dockerfile
```

-	Layers:
	-	`sha256:f01a69ba873a649d16109246e36645e9293f212711280454988268bed4add197`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 3.6 MB (3563973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bcd735f99065db42e22a630fcbdde19cc6d75b63789503857eba2885a0de8be`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 13.8 KB (13752 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:a6e34b9b3ef10febb3e68cb59e5d43a9cd4518aaaec42c9fb0eb764661ebac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356823f088987741ec801961eaf46491d407c63f5df550066164acb83a595dcd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
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
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c500b7e81fb48a2ca8dfb944bf05a4434b38906509b44c8230cb468350330652`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 6.6 MB (6636172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cba7baac1bbf19c4eff6cba1e463e4514023f61e5e4f99eabf003c60f53789`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbc8c8ecf4c50fb1afe9f838e8684a9f8283e6edf3aea752fba90ecdfb953c`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38faa38e98066ab42e204ada314c609783c4d1432e9755b2bcb597ed43dd599b`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 91.7 KB (91657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a39472daab1f7ad10eddf0cd67f8453f4675bbd31ed229cb77f9a601729e442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5077173fa2b440d42065a12b5c4ecbf78be9444e400aa418924ffe9cdeb599`

```dockerfile
```

-	Layers:
	-	`sha256:b9520b672b857555a8f6a7d165f2b5323247148278f458a7278373f979f2088f`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 3.6 MB (3556335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a715947ef1aeb942d19d5f3d425c0a032538f9e6b2ee6340f7ab1c249910cdb`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 13.6 KB (13599 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:e7c0d77acdd38391058bb428da4b25ac4b5d5b17dbc921ee7afb854783a1cc48
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
$ docker pull neurodebian@sha256:9cdfe6f90f096c5886af048cddf57f84f7131abc4faa5f65638d66c77660e090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dae39f0e2a61e2773abfc9d19efaff6e24355ae35e8f376529d52c260d4529`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
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
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114eb8c7559544e979c7bc06d71d09eaa2cd00debd8cf4f03a56d8104b7699b3`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 6.3 MB (6308996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80e11993394c1dc9aaa17af36dfa33cca39fa8e0caabe1b3bf52e80a34369c`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4eb1dc4c12753dfe02a45cea97e094916913c37268158aa3b340700e68143f`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12f43e28b0e223dee7e963ea7a4ad3a48f843457e481ee84cfb74772191cd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 91.4 KB (91443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405db61dc15551d8850b73eec4f6ecee2d15504c5d277afd2c8128e17ecf6611`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1bf2d8e93155ae981f2f562f22bf9918fdb877c66cffd35655fec1d9b1f39938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffd90ef4d3ae1ed5361af576f9d3f2c0d2a5754f07e470e32f3a78bc8bd6096`

```dockerfile
```

-	Layers:
	-	`sha256:9702d640d901ef7903e74e7c2b43af913d4f418a939adc866950dcedaf2a783a`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 3.6 MB (3559130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7bb223c6e89608e9722bf8101c7626ae5724ae67e6be3bab333911378929ca4`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c7ac4ef4afbf39509f7a22b31591f646ef72bc02b766b53e5fd512cdd67e0175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed54a230a0fd8bfde46f98be15f4d3b97ce2d877b842da7ab902c830cee5c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
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
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c880850a32196b5042f578dfb72c4fa93d1ee7ebd60d71fa4d5fbe19814c1ac`  
		Last Modified: Tue, 03 Dec 2024 06:18:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:22661e3cbf436b44b80103996ca2bd6577e74d6b1b8bebb5202171aadd46a284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d846bb8b6f1144a2d45721e8f45c30c3f32192c7a1ac72ca6b7268efa446fe48`

```dockerfile
```

-	Layers:
	-	`sha256:96771062d69621936e46943c2483b9fbc12aa2771b6c3722cb1035b36ef91682`  
		Last Modified: Tue, 03 Dec 2024 06:18:32 GMT  
		Size: 3.6 MB (3564009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c24f5aff628042c5046d45e533873a264167660d2769d5c6aa4aad04528fe9`  
		Last Modified: Tue, 03 Dec 2024 06:18:31 GMT  
		Size: 15.8 KB (15793 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a7f28e60fef8ae8c66fd2dba17b3f842cc070ff0f190ebc2bdf9a7a8be76fe7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a1f70a2c0871c021a308aded3c9b948de0de66faaa7121a2d269e4640fc96`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
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
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998bde38fb7afd531148bc5ada8932ba6909774db1014c810250d2fed9705c28`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 6.6 MB (6635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff379f8e9bb8d25d6e0f0189f738f8b022e1073b791de493bf8117cc6d281ae`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c1b51d89e4dd4797ba1c7a7da71a5c460240254b1e7853212c5b2e920c1af`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bc6338d9947bdf727b4f355b78ec884ccc098bacc03deb3d7965d5d04398bb`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 91.6 KB (91629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deb6e8c73557a116710e67686758ffb933b5075a0bed69a3dae3ca0be59627d`  
		Last Modified: Tue, 03 Dec 2024 02:28:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74f05ff960ca0068515281f926b0c25dbcf76375b4f99e58125b16a689b862ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d55b24693960716604398d554cbad7c385b5f86da205d5292975eeb67833ff`

```dockerfile
```

-	Layers:
	-	`sha256:74ca85f2e86db85f7b30f20d46e8e42be283a7b27e1b60976e0ff56e761fd5f2`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 3.6 MB (3556371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d03ff36e1583fd5288b7e43255d4ae49d2af7984f1801d3d5ea02eae17b0cc6`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:bbc3ded260e52ab68dea79f0a8860a9853977c5b81a7cbc61da66dd3e73e464d
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
$ docker pull neurodebian@sha256:22ba4c69dfacb7993f7fcf3708c2ec38e7a15ed1bed206d226c5160e47273847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fd9c4b14dc331719047f53a409b7b3093d384a6ff135c95b14e664c6b43885`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
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
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31fa211153a834040c35ecc855708df74ae143e0f067f5f29d4299bec783171`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 6.3 MB (6309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759be46808786c18908d758383834044fed05ddaf818585877931072aaa3bea3`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9340f215c3f9e9497b17c7dcc21314a53d5553d70c1a45f9ecd9663aa523c`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809dd25b48752fba0eeac0fcf5c38a88f0e12b0db0b022acf82ae7fafd98800f`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 91.4 KB (91435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b22d1f83ebacbb4392e9e1ec31a9e0902f3f7a2cde703ee063fc39bfcd1b648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9d1493dabbbd58df5573fa3c3dc733bfb235815353be42c104a85da39f4758`

```dockerfile
```

-	Layers:
	-	`sha256:8cfad2f41e51e9ca8348d9d7852f9a0f81c5d0a482874503181c168442d46e8d`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 3.6 MB (3564266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291ee8d275476a4f56b64a69bb3c484a527878d207b0f47533dc5df2c24f9458`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1401e84e1f34ba3fec0eccc60bfdb562ec886b1705aeb33459074a37aed25700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58723605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547bcc904f8cc765088dc02b9c5eac15bece1c36242ba056fa8894fa557231aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
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
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4b78788290c99294a51ceca1957d8eb6e9e849177decb1f820324a7d85b171a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c170b6bf1352da87527070a521d5bca904ee0e113091bee7260deb2c47e958`

```dockerfile
```

-	Layers:
	-	`sha256:60730bef667d6b97b826f735f2547ce96c7c51f072bed45993eb690ead280fc9`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 3.6 MB (3569145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a78c16c7a4e8d937b184fa40339df44fa15f714b5d50ea63d627b3763ab773`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 13.8 KB (13791 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:0c302d3d91a06e0de1ae44728e6c238af8f332b079b0dde357761280c7738727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59685891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eda70426935cafff4ae79341debf8d16acdb137a79c79aaf95a4e89287e257`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
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
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07d21ec843fdae56608290e710928213278f433f216169549f4105b0b7adcde`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 6.6 MB (6636002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790ba6a36bbd0ddde077446c337522dff4905079f146ba4f81c5f1b1ba01508e`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f988e696d1fd940f6f8a41f61db71109214ffa05a741e7ad19280fab3317b7a6`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7105d8b802d7cbbf45432b1a9323e287ee890f7b63ac52b16e684f8aa59aa436`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 91.6 KB (91615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:640e8a6c2b29256a11a97f4fab868b83769f471a9a56a787f0520ea21d8560d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0a2cb4139fdbf18dfb086e8db81f463979da7309ce33c42798424276477172`

```dockerfile
```

-	Layers:
	-	`sha256:13a56528e8fb58e39de0f1b02fd41e36f2ce6114df32afe325634c478c2d46c0`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 3.6 MB (3561502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda46b32b1387c0fd07559cd518cb696c94a4a839d171f21cf6124f57cee113a`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:a78a1c95462db7bf414f96ce328616fe968aac57b876af3362c3e4b47cdb81f1
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
$ docker pull neurodebian@sha256:dc2ee078717e5cd6782de72121bcc9936ef63cb0981ca8e921754737a77980e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf94ef9a8ab87a336dec4a29f001d654de0e935525f16a071a00515579aff5be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
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
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507e5811b953238ff193b1168d33f51c6e9d529f200a09d5a7cacc81a3cc8c3`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 6.3 MB (6309097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53110b5d9fe921d17db007a1ddcf5a14b209223be44404d7367639af0432a720`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073121ed00d2745775e339f48a955b95fe1cf8f720671dcb447fc1ed84db92f`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4d13654e7924d6b2b37ec66b136d37c2be5c0336ea4c05ed6c366e2a4fd3f`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 91.4 KB (91421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8461a91abccfb6a0564642a71b515e4966ed0f07a5adb19dea1de7fda249aaf0`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7de7481f3bac1a3622e0eed2ca47e8f02312431429159b58502dfc6e1b23d76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bcddfe5efc17cf322b5dd0859093bb6b3567c32ae516fe9b443b80a0541765`

```dockerfile
```

-	Layers:
	-	`sha256:70ad6f08346ad337d0f9e32f7ec11b22ad0d818d1df8a6aee0a4052c1cd75b1d`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 3.6 MB (3564302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97d1de4b535410fddab63f0e6af15dfaa00cec28ba8c0fde0a15678db848775`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 15.7 KB (15692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:17fe10b8e293faa659d945422ff3aaf4c7e6e1f387d707d314802beb80b71a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d39b737a8ff196e533cfc0ffb9a1412e43594be8673e8c0da6c05751f91ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
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
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da18a25c93d7133b2d4097e549a323142182e4dd20d54315927b6bd6573eb0f1`  
		Last Modified: Tue, 03 Dec 2024 06:17:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c77a0b2714832915027f323e1b1215a7ec8179d2324362662d8283e9cad88fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7509c00ee24dafaacefc91ed80721178d33398b768fb59515c8052afde5a23`

```dockerfile
```

-	Layers:
	-	`sha256:27c4680740117658f3a6d274e90c1bc193f9aed297af2e9c8658296f77a30654`  
		Last Modified: Tue, 03 Dec 2024 06:17:55 GMT  
		Size: 3.6 MB (3569181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37b47d54c077c2ac6d602d5b546c068ab8e54b2c34442bb70ec6ca92ca86216`  
		Last Modified: Tue, 03 Dec 2024 06:17:54 GMT  
		Size: 15.8 KB (15832 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:58259995e2bf23d42df018ba25ba3a67372a2422fdc7914cc5a132eee35433fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59686248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2739463941d7f2c81e9dcf2985fa548a020146336a6608a92ab4a327c6ebdf7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
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
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e886790f9afca68021d7c75698a1217a115b9cc1ad35a2810b2d8b0ad55f3`  
		Last Modified: Tue, 03 Dec 2024 02:28:32 GMT  
		Size: 6.6 MB (6635953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250eb870a6e7d1ba2c1af2ca41ebfa2fb763a5be83d1710296ff798161459c4`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143e50a785fba3cd83cef1e55edff4f0d54e965cede0048ee57f596d5735e0a`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92cccb8507bf0ea24147acd06ddac399895aa65bc91c02c25f650bd8c41174`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 91.6 KB (91598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c62cefd1610f7333f6f871c1794e559b2115e00c5863260f9ddedd99769cf8`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7260c43f0f9e6c3c34410fdfc970a0d4fcc49429c791e26905b3e6bfca89798c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c94c1a91810b80643dc3cac6052e446072381fd31485d5f5196bd3ea6e0cb1`

```dockerfile
```

-	Layers:
	-	`sha256:deab7f2dbd81f35b295f26a1874c4c6ce9cea7f2c767ec20cdf21e9e17c46086`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 3.6 MB (3561538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2606e6a1a87f3ded6407b0d5258d8218f3da05be49ac5201a62941c4296cdb35`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json
