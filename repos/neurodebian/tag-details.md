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
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:00011d6abd9dde0c59b3353738af9d33eccf7cc4ea75d56cdb5f4b7c0a7d85d5
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
$ docker pull neurodebian@sha256:472f1329af991e1e685a0c932048c2d14a8c70d98212bfb2b0a0ecfea20d7809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14e6cdc54dd7040883ede4dd9a98f978fecd7a3742cbe25ad36c853b168a055`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c11fcffe851b5e799a87d40b72001861eb28a55703bfd725f426c3ece51c77`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 11.3 MB (11266789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7f51c087fd27487523c3326871684de41b31a149a14770bf8119560643c6e`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d047d0a8b4395623517336d1eb42449947af65fc5199dcce0fdf50054d793057`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e6abf1a25573145adc50f804864b0d1ecb2c0651aba756443d4d373fda34b`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 93.1 KB (93144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1166e3539e20c2be219eb033fe86f2ddb2c84eda1d3c7aa003be92fd5abce80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58db5cdd34fafbe656ac5c3dfa2429a94197fa24e2d80cc4c2bb71ede7c76a3`

```dockerfile
```

-	Layers:
	-	`sha256:915f97f64acf136652ba4172c415e4d7c9cd66666c73cf447f8bf648c2ed9ac8`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 3.9 MB (3934172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2642b8e300eca497d8a4ae0d709392a6f61a9fc9533c478d43a7566f0db19163`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:444cd101a14485d17efe5e34036b59e1e7655915ec5567f414d5c4ed7d71c154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836780c2337cb4e0aa9d0b3a5a49f155c4bd7092a81af09317adfbdef7838f69`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e779c0c5fdbd8639cbb065648917ee4734d2cb9fb9c196dba52c90d4da7432ef`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 11.2 MB (11232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151d4e03d0d99ffb7b30916bb2e40ac5049633d3f098d072e599571fb7187f1d`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797d29db1aaad9bd5c0aebb832287e073ba8dfbf27fba3ce85b417d757130eb`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eaf5a9db5e5b0c8ee5099db68b3227a57c29b9b3bd879c87e60b84a5ded7f1`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74768f33db9b975bfdf336b272ec1c996a074f611773b7c037e26b1c27c55169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efa5d6bf20faa11b566042e290a899de6c2205955a43f9e514ed2898e73e02f`

```dockerfile
```

-	Layers:
	-	`sha256:5f37514115ebad86e05d6e6c9df25bad70e4fa008e3511e2c86d2f46d5ba83f5`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 3.9 MB (3934426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd890deb3dd68dc857b1766594e01192ba12852af876c01b11f0f3c58ebfe668`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:60d143b8d0798ab387a1ba35ab247442d9c6fa2b843bda309178c14872e8d3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff33a1b034af2dc30dc3e9b22bbfff4caf8eaca37fdd763d7e3782238bd6c9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b0ad1c296260622f338606fa8f84c1154fea119b5af30cbf7d53061931020`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 11.7 MB (11689003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfa4f0764baa8548d16c8fa12a59a1e739021678eef8a25ad09b365c098c202`  
		Last Modified: Mon, 28 Apr 2025 21:54:45 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46418c781371c4d88a5c425804320b04a22ddf1058e46636a2ca953fe8730a19`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9675e565699b56bd5cde2c3c03bd8c454537c6ab6beeecb53e9f8a28470b720`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:281c23b38ae433c291d7b75e19bb449ba0e2d2beecacd4be15404fae5c96dd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5c9ce8044eee941f00a14266fbd7a0bfa0e4de3155c392b537bb4814d0a4a7`

```dockerfile
```

-	Layers:
	-	`sha256:2c4b6823608fb15cb6808d5a20c6983dcd88cde64abad7c123787ed1955db7e8`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 3.9 MB (3932089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17e7dd67872341c783255b0ba32f6b5c1fcfcdf7fc6cb292b41f934fdcac0924`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:896a90715f946f951e18c7d14f0a2f4ea736cee5a4eda37f3390565581545692
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
$ docker pull neurodebian@sha256:50ceb91bc809109f14330fe913d7c5a4fd4cac8baa17311891d7815bf127caa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8243cd751996381b2414a5dfc84cd4d02f659bcbe3f50ac9577e74d497589865`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1726cb87390148585fab582d55c50d11fb91d1fdd0bd1b1ca56b3d30d0ef84`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 11.3 MB (11266846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0d9b893b8c73e8692b95563238811eee14de20516dd375669a29d2b9109f15`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa9335b96de158069a27ad40d057e8544955195a4bccf3348b8a7b7a84b34aa`  
		Last Modified: Mon, 28 Apr 2025 21:57:10 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1336facc6fb76372ce29fb4525827d75ec167ad737ae1e880886237ca216d69`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 93.2 KB (93161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea040038db3b8aa770bf72904c12a92c6715546f4806118468c78d26fb619b0`  
		Last Modified: Mon, 28 Apr 2025 21:57:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d005157e723d9670ee7d251f7ed6c16809d7546d81ea26eb76f80b3190a1574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525a2b1f93dfd30f84e0a8bb3f291a733d6ee875a228756db804773ba2cfe52`

```dockerfile
```

-	Layers:
	-	`sha256:17e92b9cad98e0352bf39ec10ff10c12c5b37a9f87a8e3b0f279ff125b75d1b1`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 3.9 MB (3934212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0b26a5e913156ebd2c17fb450ea4d488a12f3fadc0d49b332f985c71da7194`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f031e9118f0d032736b359371d83c0c1aba42e6372fca911615ce627ffd5d020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59656294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8e9780422504003ec47f8bf6e1162dc7fa2e330048c9a7f9b0309816248d5e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e779c0c5fdbd8639cbb065648917ee4734d2cb9fb9c196dba52c90d4da7432ef`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 11.2 MB (11232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151d4e03d0d99ffb7b30916bb2e40ac5049633d3f098d072e599571fb7187f1d`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797d29db1aaad9bd5c0aebb832287e073ba8dfbf27fba3ce85b417d757130eb`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eaf5a9db5e5b0c8ee5099db68b3227a57c29b9b3bd879c87e60b84a5ded7f1`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1bfffdbe782b62c55f4e41a71f8d3d5ae7e0d68f7e8e6f070a56fa0d01a41a`  
		Last Modified: Tue, 29 Apr 2025 20:18:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d1efb809ea6433be59cd6f799cd5d71a31da2507c0317d65e30e217193587991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfb0b5a8543f039e7275c9dc4184761336206087e451fd39a0911ae73da76c7`

```dockerfile
```

-	Layers:
	-	`sha256:6828cbe3108c6036e8a8f26d449b358a01efbf17e2eed1dd6d3b14eca2376e6c`  
		Last Modified: Tue, 29 Apr 2025 20:18:47 GMT  
		Size: 3.9 MB (3934466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8bb9a1f2a7ca2f5dd9277dbe658fa96fc74cf1189b3fefc8bff8f63901875d`  
		Last Modified: Tue, 29 Apr 2025 20:18:46 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e0f9efeaba1cfd35206171ac6296d3b817aec20343c1bdfd197bc63f6bf0dd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61263300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8eda66d1f24e0ec652f1b4f7f096a77cbbb9c1e02d21088c3ca7530d62acba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf55cf3f7b075c849de2b0637905cbcaa155b900786312febc235450a3d9e186`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 11.7 MB (11688920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9841be6b1d29b72c332cf9244a69b73f9c3905a3e4fecab669cbcbedbfbfba6`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46418c781371c4d88a5c425804320b04a22ddf1058e46636a2ca953fe8730a19`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa2435d68921f8ee6d07f3f0321ac0a746a6cc96ad4de7e3796d252381e381b`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e62d3a2118bb599dfd9f8e453a6382752c4754e2800c1966bed52007242c91`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1e7f21d6d907d5a520c0d179a925520318b259293aada676b0ef391d2e64d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755ac7273bb9a8e9b95db677842cb92bd3f08ed9fd9fce77376afb941568f4d`

```dockerfile
```

-	Layers:
	-	`sha256:9e29e1fa7b2b3e13b3232afd949f2bb4e10ef5337bf92feef772fbd4fbb23deb`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 3.9 MB (3932129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e1593684c0bdf2ba5a620818c5ae41611116487fb181c1fb7766f3c694729a`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:92faf713ac5d573c61e929d1bb0885bd8206160ff2bd83ab782999cd95e11826
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
$ docker pull neurodebian@sha256:3614e7929c3729ee492900655cbb593213ff9b668b06a0a5b65af31ad4e250cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64956137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bb962de648b02471760878f9d9c5bceebfb355a0fa6460146e88b36ebf2c6f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3369c96af3a9fc3eb29426e581d97ea32eaab31c47f81ee9892accb3b232967`  
		Last Modified: Mon, 28 Apr 2025 22:08:32 GMT  
		Size: 11.1 MB (11105044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dd822d9757e8e19577e208ca25031ec40df49dfbe8dd27f79473b2eda7f2a2`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6efc71d615d74c4ba039b2798948093b14e30d977f385680cd8c9bfdfe2099`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9f32be21c243ea5db70432799ed926d4f88873b7799935404984d527f84c3b`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 101.2 KB (101195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:051cbd07a47217a799ca9328cecd294167f18ef76f98afdfe7a7d1e58062f95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8d47fcea2aa238b119b230d048286daf2dbc0c4874f79b98bea4b44dec0b7d`

```dockerfile
```

-	Layers:
	-	`sha256:e7515c8ebe3afb7d5465b050016327ae00b50e6620eeffc63b538820def8f034`  
		Last Modified: Mon, 28 Apr 2025 22:08:32 GMT  
		Size: 4.2 MB (4234764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d532788aa376107485ef5e11dfed5d64f23507c398c86d35c0f454acc6f12317`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:54cc18c5f8099aff6ea8ba3c72a11e79b7905973f6217160e4926034ce9350a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0171329c6886636ba22a3b2b035e468fd6d0f8c2bea8dd80523efc98efcf258`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9753e330284da1899fd231bf33fe62c0d83e3f17a233f3f30f504bbb6fda21`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 11.1 MB (11106062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4499b0e25845d2e35fdde74226cf5901ec7e9be9382eed98b9a3eb02064d539`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4039d5ee1ad977691de6bac1fb9373ed9749a1f33ec81bd570216e56c21b379`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ea557c3b7e8fb6dd8d91d49cae4f0e43f2c39dcfedf77ad960408c3552376f`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5043ae029131864ae3a944a2a752566e6db3aa2a287e8abf3e0f646a0231fe27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92230a230aef69834f4829c9064c575d06f45e0dc635672186d1e3b544444f59`

```dockerfile
```

-	Layers:
	-	`sha256:1c760e8eb6dee853f27cb14705ec5ac2b466a26636ecdfc31f9ecc865866d939`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 4.2 MB (4234371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5319aba817327886dc313845a89cbd8ba1eaa6cef5c0c9fca089e56606a8099e`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:ece69efe387772ae71e49334ad14fb71fca34e8398e9eebc4945eb2e5b5896ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66286721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b61cac2b83d8e5742e4d51cc760dc2ab27575c2116e7a38396a5560908485ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baa54ab7aadb65f6ea817faeccad8b1e8490b283148d13620fe04aa91bcc5a2`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 11.5 MB (11500361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617112d89002a29be31993a712480ac76d7c3fbdcb5c6f3cf40b5b4b8fa886fb`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8d4f800552b99deaca99f39e9c946843f3fbc3a4547f43b1583fa99c0ea721`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6fbe1de2e956cf97516f96ef1b5550fc3c0fd3e6ed042f2bfafdc5860b98e1`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 101.1 KB (101099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b4b8e1705c550b0dc744d427ad3d78c1e2c71de91c2c660f37d57a1ed1f3bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7032562fd624591c59b125344aa2165980d603d957844a2ba94775a0137f3066`

```dockerfile
```

-	Layers:
	-	`sha256:d589af26589c547278945a991c581d65bc5e099cf7a2e6f20c7f76b26303ecd7`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 4.2 MB (4231226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76920d86db0de668b94e501ce99edc5079abcced341354afc9d97bc2c02b104`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:a209a003fe2cf739a06a10bad52dc252cb0b03dd16c3e7218481887f240c5bb9
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
$ docker pull neurodebian@sha256:d81a476a0c0a5200917c0c098955ff67c2dc7163b6722f5b9009ac1d6ce8f87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64956557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bb2c6517b71cad4d4531fb28674813bdd45eaba155b3f1383f1f066bf9f978`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3805948ea0a099f128fd1590cd09c7deba13a775bf11ad6652a65dee5e7b3307`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 11.1 MB (11105099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4bb79503e49002e87fadfc3687fcb6efa56f7c94788a32dd04842147ef637e`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e782051a7146746e97fd5dfaa52270bcbd5ce40d6c85269dbbfed17a02a624`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3633c4afe5e0e441d7aae2bffd0f2374b68698367bd08804f4fc636516b18`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e5747c9ed81a4fef65a55f99af17f7db3a478c7d5d65e53369b2aa9e584969`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4454b45f35b9696e23c0d5f895e9c28c8463b5888c82e6a557714df5e7f6932e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57cbf5bc16f0f074a4177db482f4899dabc0752ee21ac58e4fafffffd3839615`

```dockerfile
```

-	Layers:
	-	`sha256:7d6d60dc20dcc8be5f866b6763476be367a685777bcf709a1813368e566f6ac0`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 4.2 MB (4234800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984001af9a5f710a9a82b5c0fa141ddf03a8717e933fcda115e031f021df0ab5`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3cda06f8fb6326d7aff37ccf966a10e15f1e957e7397892ed65ba00cb7324a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e866f9690cb93c903552d461eaee74e9538e29d9e14eddf6d9fa64f8f3d735b8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9753e330284da1899fd231bf33fe62c0d83e3f17a233f3f30f504bbb6fda21`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 11.1 MB (11106062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4499b0e25845d2e35fdde74226cf5901ec7e9be9382eed98b9a3eb02064d539`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4039d5ee1ad977691de6bac1fb9373ed9749a1f33ec81bd570216e56c21b379`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ea557c3b7e8fb6dd8d91d49cae4f0e43f2c39dcfedf77ad960408c3552376f`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb5394c6c7df9c157ef89060c5b3728c4569afb6f29aa90099a6604e7b5a5b2`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3900a4f64cf6c27e536fc131954fd0c5e09bfeaba76a2c956de2b194626b4606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bf7a90d529ff4e3867c6ee1388eb4da4b771cab6312d7727d44a0862d829e4`

```dockerfile
```

-	Layers:
	-	`sha256:d1212b901568e21393d035b08d640b468c1053363d014e1f3307ed7ce8c051e7`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 4.2 MB (4234407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978d1348aeb4ec99ec3692b6fcc8ef4d9de310223650528f78e204440ac3c50b`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7fe93975c6b8bef6ffc276b4ce7083e14497561f5596eaa3c2c3c77e70ecc0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66287038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed0c0c22ad836af99126ccc8f2c1699cc2253963005fb73df0ccf1dde0ec19b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78a375722d52fe5ae5287838cde6a528a6e3614649ea4486c6a6a04472f8b24`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 11.5 MB (11500331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4961efc6aaa6e0e2fef51fabe26b021418deb491dd1ce5250e97ebbdaf940464`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6799be99c522aa1a27ffd172f171bdec808f16037cbd4c44d8b4f32adac7e7cb`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef98689bf88067a5b7bd537640dba1d3e41a94c92bd39a54a5ba69819f82ced`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 101.1 KB (101058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa2462fc78f51b305bd074cf1634f3470150f9b2f1b82f4e1107b93bc57f047`  
		Last Modified: Mon, 28 Apr 2025 21:54:45 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbd5d38b5fedf86b44de1a7e51c7dde5402528d2aa0091a7f87f2ef16d9ff987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3f2ff430ba7fcd8d76f2f2cee0bcc459bac956d411110e7af8a975f6702b5`

```dockerfile
```

-	Layers:
	-	`sha256:99ce1363ab1e2a5dd36fb177e64e2dc8d8ebc1104b228a1f43e0c06d241aeb44`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 4.2 MB (4231262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe1745ae34a3bf2f421654efb60c5db9c2254eabba488faed4ab3d800519c0c`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:e68b01fb0dea971fa4cfd39d8feb687c3fe2aa4bd228ca5e72189d11d8c78908
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:ec026f26f90a1da8ffc3ba59281854c0bb1a0b5f166e58e75d57f34e8424bd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa3d04109e9bf85dbba55e27e2b0055d3c73ba8b1f21907acb2c7bdb223320`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabac9a159eac99d387c3b1a92d15536e78c12f6596c2dbd37f29d0b63d5dffe`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 5.4 MB (5362390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e9f035d7685c2fdb1e905a640424e5ad669ee2970a32cbec7f8d889e3625f1`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb125018a09465c3a7d0200be55fc6435a06fe742fd5a7a7ef39a0fb83cfbf6`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46b9b7320bd76241047fcf77910ba82992b5e91e204eefe5390b265739db65`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 105.4 KB (105439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed731be31bff11d448e1a27d734e900b2e674625af668b3f9b87ba45b1a8f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fb983f465508bd38f2970b20fcfd3052779b73f8d3b436c6ab4ff79915307d`

```dockerfile
```

-	Layers:
	-	`sha256:079d7ce90a22f0bd844b80ccfaee90ce51150b4f1244f3519448f12bf6c83630`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 2.0 MB (2017825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d275b201a8175e6493a6207f8e73ff2b18780007de8ef8e54adc086578431b8d`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:39c9bfd66371de386419abe34cd806357a534145fbce48504409d1f8f396a4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45aed6d0d9e4f56fcf7aaaad06b6a747462168128f4a0d1f3e2084772af72fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2952dad8358145d90322cccd4047ea733f93fc11fed56791f2817ddc6d99d545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0237cdae437eaedee949f6af64e985420e981a9dfa9474fce1bb2e9aa7fbb8fd`

```dockerfile
```

-	Layers:
	-	`sha256:f307ef0a8e38175dd6e3ceb807d756938a14b991426d356ef4e8432d33ab7e37`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 2.0 MB (2018054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8946cab190197295b0fd0de39d4d1f5d0e06793a5eb36d0073e79597d9fd10d1`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:4c1ed82e5488cc7a87a4035c84b91368bf439418f76c388be8923760e27cc034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5b5f12c95fa70eba84ed0d9a8cfd320ff1f928e0f4ecc665553188865bc1fdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77302996458a5ea42a30e362fe60a32b80399042312ed4461165057feaadc3a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09894bd673fc3443fa4aac9c04f3790e80821023e1b647cb36b0dbb3295685a1`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 5.4 MB (5362436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b567f68d429f42a824fdac7d380831ff3ee4e919d2c1f56ac4ba2d5c728dab9`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe211eff3c4623dbc046e34c08495b6c3665295d30178fc8053cd5baff9b469`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93ed51b316d633e53abd6403ccacb66bf2b80b807810d40df2342572077415`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 105.4 KB (105442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca65e65a74419b6f595b799268195de974952d7e1558d9a39092265337398f`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:451612c81608c2bebc8d3e36a6a521b28025afe8d027348134cdac02a7ec34d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e43683e94761e4cae4d1f50b39b3b1ced64f4fb773232eb29f20df0b386bb`

```dockerfile
```

-	Layers:
	-	`sha256:79b4a3ef3b60d9c20c2340237fe4236376a35581ce8f29f76d044ea8920b97d3`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 2.0 MB (2017861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd949e8f808ff83620701f51061d8dc60e04b6e7afc9a968a71e3ed0ef991e1`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b31849bda994a89ea1e43d1ee83490728e5c84d98e21bb02362919c0ee14a139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9884153e1d1e0355067632367672016383e04b73464a2d8661e4d01f7cf3d14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8215c91245c0463263d03909dc6267e663f8bc6ca035c5fa1478e3632affb97f`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e0dd953f78b0d8045d26f7afb42c726a2cc4e07a96a2b3b741316ca99534d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea7d3f1b864509ea868bded897bb9ca30f452582999b77e73c6bfc798dd9443`

```dockerfile
```

-	Layers:
	-	`sha256:1fcbe13a76f25efb5f459970d227c4628a1a8f71064188a5cd94ffb6874dd526`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 2.0 MB (2018090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dac00fd22e65ab791eda65319d76e0834a665f17c3cf1d1784f781fa3bcd68`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:26f539327816198b90ed431924fec2ff158a98aa745b593bdfb2b2ae8c0cdb4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:5ca7d2535708de52e59146391a85e3222685b2101bcf6fbc69c6feaf164fa8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf1b0c7fa661952a44369df7910143a9f46830a62c9ee24693812478330d276`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7502f8f384c9e39101e17b46acf0f303f53f00c3076b70089bf8b5293c14a4e`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 3.6 MB (3623789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305875cc34b35c47d97f34abae20428fc4785a556dfebcb1e04c18a29117c3`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ad9396ff5157816c245d94d7dabb054e837511ea47b307ed3762318e74bfe`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ac9ef6b50c230c07920e2ccb263260c5218521277d00c0b20f9baebd17b8ff`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 110.7 KB (110667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:810ca171bbe3a461ad3f9c0c841ca6a05c8ceb604c62f05408e5d9b9fb683cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992fa750bd033c67b1276168605e2c584b3fbd033a0f2ae6979168542be25358`

```dockerfile
```

-	Layers:
	-	`sha256:364e84565c06cba8f2e91059f991c8688d269b08155b49077e48c4f2494fec78`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 2.1 MB (2055399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e73795a9937a5c5f7a6f43e8dcdc653d5018d6e430e3b67b8783a422fc7c17`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bfdcd9bb99802a608520d891d99b9a896b9e519c3fc710f5da8a3c92e29e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203958ef9579128f347a4bff0aa2c110790666b706dcff91afdf58e7071c151`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff69349668077007180f865cd316b1438d2244cfb6b5877a93d2ef957fae893`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 3.6 MB (3595245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ba73de0fee7dddc1e560209decbfbb8b8bfdcfc88bbab92fa5c475aea44d6`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f3443353aec912c7886b00a30c1cbded982093a0100e7b31360469c9bc243d`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d514962ad10eec887ec71fc1184b491c71747421dc4270402e4b0789bbf9`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 110.5 KB (110487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f47f5e2a24302ecae11fa9f56b627034c206301bfc142a63a03ba0ba63a2761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4792f4614d130d88d6574df8a599739fe6f52d661775cb0d3124c95e3f72c8c0`

```dockerfile
```

-	Layers:
	-	`sha256:aeb0c1d1d0fdd14937cc58efd46f5290c63cc757662509258f20fa18fadf548f`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 2.1 MB (2055659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a2eafa98dff300a61f97ed986282c056145cd6a289464d241a3947fc933ce2`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:e67dd8274275cc1bc4ccc9c495df2cba487d4c057261a5bbe3a675fc905f7b25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ea75232b46889271617dc481821e1909d05ce5e92545bbba1227bab364999f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d461c6f7b13738c6b4f1a89ee7e24ecff7dc5c5a5bbc035480235c5bff84a0`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b515f437b37abbbf80a20851603ea0e660cc33ed3133ce6e83a3a5001b47cfa8`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 3.6 MB (3623809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eac336a51090a23cc0914f157aeca298493cf6392d5a7bf98a11285541c58de`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89e1a0218ea67a334a752b5e3a2de2d7fce6f8229c537fed384ce40a6c73eef`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad56d373af038e98991e376e180b79cefcac28fcd50c4691e4936c45c0b2c83`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 110.6 KB (110648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ed4506459d767c55f263519a1a8867dcc18b98989376d59aa73bb765358090`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8083f260db3c7a548cbc86e95fe014cd17b417e18f266dc7177bb5a53f7d906f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c20ab0ef254c9cc608600b01f7841ed992b3760200c569b0a4dbabffb2f87a`

```dockerfile
```

-	Layers:
	-	`sha256:c5dec75c2040837c9f93ab3fe9b47cf1145215b4e726a25573ebf5efff863796`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 2.1 MB (2055435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d34f17d0e8739af8fb593e06c8d6482c9edbf64bcd81892b92387c37fe99cc`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d7d3fe31084430bceba93d5ef8c36791c06f81aaba37fd3061e605640cc21799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21edc9ced3f14de6089c514ea712e115634ea4f472b6bade77784b66e285b19d`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff69349668077007180f865cd316b1438d2244cfb6b5877a93d2ef957fae893`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 3.6 MB (3595245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ba73de0fee7dddc1e560209decbfbb8b8bfdcfc88bbab92fa5c475aea44d6`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f3443353aec912c7886b00a30c1cbded982093a0100e7b31360469c9bc243d`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d514962ad10eec887ec71fc1184b491c71747421dc4270402e4b0789bbf9`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 110.5 KB (110487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa8c2eec598bd3e1f629937728f657e829a66175aebd83ec75955e0610b7d70`  
		Last Modified: Wed, 09 Apr 2025 08:38:47 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a65e2f92ef29328dde9fa680fb2ba4202004cebd5d59beb8d6dfb27e06937fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88aea1a112a0452f1a588ced51bfba8be8fd61b854ae3a85f7f56b9bc1757a1e`

```dockerfile
```

-	Layers:
	-	`sha256:72ffbab84cded574356793b5cc86203486b55dd41f91eac101c436104bcd477b`  
		Last Modified: Wed, 09 Apr 2025 08:38:47 GMT  
		Size: 2.1 MB (2055695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0936d3750f33d18090c78dc9e1806e9c95d79d56b2cd5a5a2ea94dac2b22ec`  
		Last Modified: Wed, 09 Apr 2025 08:38:46 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:00011d6abd9dde0c59b3353738af9d33eccf7cc4ea75d56cdb5f4b7c0a7d85d5
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
$ docker pull neurodebian@sha256:472f1329af991e1e685a0c932048c2d14a8c70d98212bfb2b0a0ecfea20d7809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14e6cdc54dd7040883ede4dd9a98f978fecd7a3742cbe25ad36c853b168a055`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c11fcffe851b5e799a87d40b72001861eb28a55703bfd725f426c3ece51c77`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 11.3 MB (11266789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7f51c087fd27487523c3326871684de41b31a149a14770bf8119560643c6e`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d047d0a8b4395623517336d1eb42449947af65fc5199dcce0fdf50054d793057`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e6abf1a25573145adc50f804864b0d1ecb2c0651aba756443d4d373fda34b`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 93.1 KB (93144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1166e3539e20c2be219eb033fe86f2ddb2c84eda1d3c7aa003be92fd5abce80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58db5cdd34fafbe656ac5c3dfa2429a94197fa24e2d80cc4c2bb71ede7c76a3`

```dockerfile
```

-	Layers:
	-	`sha256:915f97f64acf136652ba4172c415e4d7c9cd66666c73cf447f8bf648c2ed9ac8`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 3.9 MB (3934172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2642b8e300eca497d8a4ae0d709392a6f61a9fc9533c478d43a7566f0db19163`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:444cd101a14485d17efe5e34036b59e1e7655915ec5567f414d5c4ed7d71c154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836780c2337cb4e0aa9d0b3a5a49f155c4bd7092a81af09317adfbdef7838f69`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e779c0c5fdbd8639cbb065648917ee4734d2cb9fb9c196dba52c90d4da7432ef`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 11.2 MB (11232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151d4e03d0d99ffb7b30916bb2e40ac5049633d3f098d072e599571fb7187f1d`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797d29db1aaad9bd5c0aebb832287e073ba8dfbf27fba3ce85b417d757130eb`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eaf5a9db5e5b0c8ee5099db68b3227a57c29b9b3bd879c87e60b84a5ded7f1`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74768f33db9b975bfdf336b272ec1c996a074f611773b7c037e26b1c27c55169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efa5d6bf20faa11b566042e290a899de6c2205955a43f9e514ed2898e73e02f`

```dockerfile
```

-	Layers:
	-	`sha256:5f37514115ebad86e05d6e6c9df25bad70e4fa008e3511e2c86d2f46d5ba83f5`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 3.9 MB (3934426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd890deb3dd68dc857b1766594e01192ba12852af876c01b11f0f3c58ebfe668`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:60d143b8d0798ab387a1ba35ab247442d9c6fa2b843bda309178c14872e8d3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff33a1b034af2dc30dc3e9b22bbfff4caf8eaca37fdd763d7e3782238bd6c9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b0ad1c296260622f338606fa8f84c1154fea119b5af30cbf7d53061931020`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 11.7 MB (11689003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfa4f0764baa8548d16c8fa12a59a1e739021678eef8a25ad09b365c098c202`  
		Last Modified: Mon, 28 Apr 2025 21:54:45 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46418c781371c4d88a5c425804320b04a22ddf1058e46636a2ca953fe8730a19`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9675e565699b56bd5cde2c3c03bd8c454537c6ab6beeecb53e9f8a28470b720`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:281c23b38ae433c291d7b75e19bb449ba0e2d2beecacd4be15404fae5c96dd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5c9ce8044eee941f00a14266fbd7a0bfa0e4de3155c392b537bb4814d0a4a7`

```dockerfile
```

-	Layers:
	-	`sha256:2c4b6823608fb15cb6808d5a20c6983dcd88cde64abad7c123787ed1955db7e8`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 3.9 MB (3932089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17e7dd67872341c783255b0ba32f6b5c1fcfcdf7fc6cb292b41f934fdcac0924`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:92faf713ac5d573c61e929d1bb0885bd8206160ff2bd83ab782999cd95e11826
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
$ docker pull neurodebian@sha256:3614e7929c3729ee492900655cbb593213ff9b668b06a0a5b65af31ad4e250cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64956137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bb962de648b02471760878f9d9c5bceebfb355a0fa6460146e88b36ebf2c6f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3369c96af3a9fc3eb29426e581d97ea32eaab31c47f81ee9892accb3b232967`  
		Last Modified: Mon, 28 Apr 2025 22:08:32 GMT  
		Size: 11.1 MB (11105044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dd822d9757e8e19577e208ca25031ec40df49dfbe8dd27f79473b2eda7f2a2`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6efc71d615d74c4ba039b2798948093b14e30d977f385680cd8c9bfdfe2099`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9f32be21c243ea5db70432799ed926d4f88873b7799935404984d527f84c3b`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 101.2 KB (101195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:051cbd07a47217a799ca9328cecd294167f18ef76f98afdfe7a7d1e58062f95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8d47fcea2aa238b119b230d048286daf2dbc0c4874f79b98bea4b44dec0b7d`

```dockerfile
```

-	Layers:
	-	`sha256:e7515c8ebe3afb7d5465b050016327ae00b50e6620eeffc63b538820def8f034`  
		Last Modified: Mon, 28 Apr 2025 22:08:32 GMT  
		Size: 4.2 MB (4234764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d532788aa376107485ef5e11dfed5d64f23507c398c86d35c0f454acc6f12317`  
		Last Modified: Mon, 28 Apr 2025 22:08:31 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:54cc18c5f8099aff6ea8ba3c72a11e79b7905973f6217160e4926034ce9350a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0171329c6886636ba22a3b2b035e468fd6d0f8c2bea8dd80523efc98efcf258`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9753e330284da1899fd231bf33fe62c0d83e3f17a233f3f30f504bbb6fda21`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 11.1 MB (11106062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4499b0e25845d2e35fdde74226cf5901ec7e9be9382eed98b9a3eb02064d539`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4039d5ee1ad977691de6bac1fb9373ed9749a1f33ec81bd570216e56c21b379`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ea557c3b7e8fb6dd8d91d49cae4f0e43f2c39dcfedf77ad960408c3552376f`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5043ae029131864ae3a944a2a752566e6db3aa2a287e8abf3e0f646a0231fe27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92230a230aef69834f4829c9064c575d06f45e0dc635672186d1e3b544444f59`

```dockerfile
```

-	Layers:
	-	`sha256:1c760e8eb6dee853f27cb14705ec5ac2b466a26636ecdfc31f9ecc865866d939`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 4.2 MB (4234371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5319aba817327886dc313845a89cbd8ba1eaa6cef5c0c9fca089e56606a8099e`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:ece69efe387772ae71e49334ad14fb71fca34e8398e9eebc4945eb2e5b5896ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66286721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b61cac2b83d8e5742e4d51cc760dc2ab27575c2116e7a38396a5560908485ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baa54ab7aadb65f6ea817faeccad8b1e8490b283148d13620fe04aa91bcc5a2`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 11.5 MB (11500361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617112d89002a29be31993a712480ac76d7c3fbdcb5c6f3cf40b5b4b8fa886fb`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8d4f800552b99deaca99f39e9c946843f3fbc3a4547f43b1583fa99c0ea721`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6fbe1de2e956cf97516f96ef1b5550fc3c0fd3e6ed042f2bfafdc5860b98e1`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 101.1 KB (101099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b4b8e1705c550b0dc744d427ad3d78c1e2c71de91c2c660f37d57a1ed1f3bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7032562fd624591c59b125344aa2165980d603d957844a2ba94775a0137f3066`

```dockerfile
```

-	Layers:
	-	`sha256:d589af26589c547278945a991c581d65bc5e099cf7a2e6f20c7f76b26303ecd7`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 4.2 MB (4231226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76920d86db0de668b94e501ce99edc5079abcced341354afc9d97bc2c02b104`  
		Last Modified: Mon, 28 Apr 2025 21:54:41 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:a209a003fe2cf739a06a10bad52dc252cb0b03dd16c3e7218481887f240c5bb9
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
$ docker pull neurodebian@sha256:d81a476a0c0a5200917c0c098955ff67c2dc7163b6722f5b9009ac1d6ce8f87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64956557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bb2c6517b71cad4d4531fb28674813bdd45eaba155b3f1383f1f066bf9f978`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3805948ea0a099f128fd1590cd09c7deba13a775bf11ad6652a65dee5e7b3307`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 11.1 MB (11105099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4bb79503e49002e87fadfc3687fcb6efa56f7c94788a32dd04842147ef637e`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e782051a7146746e97fd5dfaa52270bcbd5ce40d6c85269dbbfed17a02a624`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3633c4afe5e0e441d7aae2bffd0f2374b68698367bd08804f4fc636516b18`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e5747c9ed81a4fef65a55f99af17f7db3a478c7d5d65e53369b2aa9e584969`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4454b45f35b9696e23c0d5f895e9c28c8463b5888c82e6a557714df5e7f6932e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57cbf5bc16f0f074a4177db482f4899dabc0752ee21ac58e4fafffffd3839615`

```dockerfile
```

-	Layers:
	-	`sha256:7d6d60dc20dcc8be5f866b6763476be367a685777bcf709a1813368e566f6ac0`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 4.2 MB (4234800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984001af9a5f710a9a82b5c0fa141ddf03a8717e933fcda115e031f021df0ab5`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3cda06f8fb6326d7aff37ccf966a10e15f1e957e7397892ed65ba00cb7324a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e866f9690cb93c903552d461eaee74e9538e29d9e14eddf6d9fa64f8f3d735b8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9753e330284da1899fd231bf33fe62c0d83e3f17a233f3f30f504bbb6fda21`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 11.1 MB (11106062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4499b0e25845d2e35fdde74226cf5901ec7e9be9382eed98b9a3eb02064d539`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4039d5ee1ad977691de6bac1fb9373ed9749a1f33ec81bd570216e56c21b379`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ea557c3b7e8fb6dd8d91d49cae4f0e43f2c39dcfedf77ad960408c3552376f`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb5394c6c7df9c157ef89060c5b3728c4569afb6f29aa90099a6604e7b5a5b2`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3900a4f64cf6c27e536fc131954fd0c5e09bfeaba76a2c956de2b194626b4606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bf7a90d529ff4e3867c6ee1388eb4da4b771cab6312d7727d44a0862d829e4`

```dockerfile
```

-	Layers:
	-	`sha256:d1212b901568e21393d035b08d640b468c1053363d014e1f3307ed7ce8c051e7`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 4.2 MB (4234407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978d1348aeb4ec99ec3692b6fcc8ef4d9de310223650528f78e204440ac3c50b`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7fe93975c6b8bef6ffc276b4ce7083e14497561f5596eaa3c2c3c77e70ecc0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66287038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed0c0c22ad836af99126ccc8f2c1699cc2253963005fb73df0ccf1dde0ec19b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78a375722d52fe5ae5287838cde6a528a6e3614649ea4486c6a6a04472f8b24`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 11.5 MB (11500331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4961efc6aaa6e0e2fef51fabe26b021418deb491dd1ce5250e97ebbdaf940464`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6799be99c522aa1a27ffd172f171bdec808f16037cbd4c44d8b4f32adac7e7cb`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef98689bf88067a5b7bd537640dba1d3e41a94c92bd39a54a5ba69819f82ced`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 101.1 KB (101058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa2462fc78f51b305bd074cf1634f3470150f9b2f1b82f4e1107b93bc57f047`  
		Last Modified: Mon, 28 Apr 2025 21:54:45 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbd5d38b5fedf86b44de1a7e51c7dde5402528d2aa0091a7f87f2ef16d9ff987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3f2ff430ba7fcd8d76f2f2cee0bcc459bac956d411110e7af8a975f6702b5`

```dockerfile
```

-	Layers:
	-	`sha256:99ce1363ab1e2a5dd36fb177e64e2dc8d8ebc1104b228a1f43e0c06d241aeb44`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 4.2 MB (4231262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe1745ae34a3bf2f421654efb60c5db9c2254eabba488faed4ab3d800519c0c`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:00011d6abd9dde0c59b3353738af9d33eccf7cc4ea75d56cdb5f4b7c0a7d85d5
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
$ docker pull neurodebian@sha256:472f1329af991e1e685a0c932048c2d14a8c70d98212bfb2b0a0ecfea20d7809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14e6cdc54dd7040883ede4dd9a98f978fecd7a3742cbe25ad36c853b168a055`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c11fcffe851b5e799a87d40b72001861eb28a55703bfd725f426c3ece51c77`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 11.3 MB (11266789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7f51c087fd27487523c3326871684de41b31a149a14770bf8119560643c6e`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d047d0a8b4395623517336d1eb42449947af65fc5199dcce0fdf50054d793057`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e6abf1a25573145adc50f804864b0d1ecb2c0651aba756443d4d373fda34b`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 93.1 KB (93144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1166e3539e20c2be219eb033fe86f2ddb2c84eda1d3c7aa003be92fd5abce80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58db5cdd34fafbe656ac5c3dfa2429a94197fa24e2d80cc4c2bb71ede7c76a3`

```dockerfile
```

-	Layers:
	-	`sha256:915f97f64acf136652ba4172c415e4d7c9cd66666c73cf447f8bf648c2ed9ac8`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 3.9 MB (3934172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2642b8e300eca497d8a4ae0d709392a6f61a9fc9533c478d43a7566f0db19163`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:444cd101a14485d17efe5e34036b59e1e7655915ec5567f414d5c4ed7d71c154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836780c2337cb4e0aa9d0b3a5a49f155c4bd7092a81af09317adfbdef7838f69`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e779c0c5fdbd8639cbb065648917ee4734d2cb9fb9c196dba52c90d4da7432ef`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 11.2 MB (11232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151d4e03d0d99ffb7b30916bb2e40ac5049633d3f098d072e599571fb7187f1d`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797d29db1aaad9bd5c0aebb832287e073ba8dfbf27fba3ce85b417d757130eb`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eaf5a9db5e5b0c8ee5099db68b3227a57c29b9b3bd879c87e60b84a5ded7f1`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74768f33db9b975bfdf336b272ec1c996a074f611773b7c037e26b1c27c55169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efa5d6bf20faa11b566042e290a899de6c2205955a43f9e514ed2898e73e02f`

```dockerfile
```

-	Layers:
	-	`sha256:5f37514115ebad86e05d6e6c9df25bad70e4fa008e3511e2c86d2f46d5ba83f5`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 3.9 MB (3934426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd890deb3dd68dc857b1766594e01192ba12852af876c01b11f0f3c58ebfe668`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:60d143b8d0798ab387a1ba35ab247442d9c6fa2b843bda309178c14872e8d3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff33a1b034af2dc30dc3e9b22bbfff4caf8eaca37fdd763d7e3782238bd6c9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b0ad1c296260622f338606fa8f84c1154fea119b5af30cbf7d53061931020`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 11.7 MB (11689003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfa4f0764baa8548d16c8fa12a59a1e739021678eef8a25ad09b365c098c202`  
		Last Modified: Mon, 28 Apr 2025 21:54:45 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46418c781371c4d88a5c425804320b04a22ddf1058e46636a2ca953fe8730a19`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9675e565699b56bd5cde2c3c03bd8c454537c6ab6beeecb53e9f8a28470b720`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:281c23b38ae433c291d7b75e19bb449ba0e2d2beecacd4be15404fae5c96dd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5c9ce8044eee941f00a14266fbd7a0bfa0e4de3155c392b537bb4814d0a4a7`

```dockerfile
```

-	Layers:
	-	`sha256:2c4b6823608fb15cb6808d5a20c6983dcd88cde64abad7c123787ed1955db7e8`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 3.9 MB (3932089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17e7dd67872341c783255b0ba32f6b5c1fcfcdf7fc6cb292b41f934fdcac0924`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:896a90715f946f951e18c7d14f0a2f4ea736cee5a4eda37f3390565581545692
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
$ docker pull neurodebian@sha256:50ceb91bc809109f14330fe913d7c5a4fd4cac8baa17311891d7815bf127caa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8243cd751996381b2414a5dfc84cd4d02f659bcbe3f50ac9577e74d497589865`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1726cb87390148585fab582d55c50d11fb91d1fdd0bd1b1ca56b3d30d0ef84`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 11.3 MB (11266846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0d9b893b8c73e8692b95563238811eee14de20516dd375669a29d2b9109f15`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa9335b96de158069a27ad40d057e8544955195a4bccf3348b8a7b7a84b34aa`  
		Last Modified: Mon, 28 Apr 2025 21:57:10 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1336facc6fb76372ce29fb4525827d75ec167ad737ae1e880886237ca216d69`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 93.2 KB (93161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea040038db3b8aa770bf72904c12a92c6715546f4806118468c78d26fb619b0`  
		Last Modified: Mon, 28 Apr 2025 21:57:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d005157e723d9670ee7d251f7ed6c16809d7546d81ea26eb76f80b3190a1574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525a2b1f93dfd30f84e0a8bb3f291a733d6ee875a228756db804773ba2cfe52`

```dockerfile
```

-	Layers:
	-	`sha256:17e92b9cad98e0352bf39ec10ff10c12c5b37a9f87a8e3b0f279ff125b75d1b1`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 3.9 MB (3934212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0b26a5e913156ebd2c17fb450ea4d488a12f3fadc0d49b332f985c71da7194`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f031e9118f0d032736b359371d83c0c1aba42e6372fca911615ce627ffd5d020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59656294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8e9780422504003ec47f8bf6e1162dc7fa2e330048c9a7f9b0309816248d5e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e779c0c5fdbd8639cbb065648917ee4734d2cb9fb9c196dba52c90d4da7432ef`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 11.2 MB (11232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151d4e03d0d99ffb7b30916bb2e40ac5049633d3f098d072e599571fb7187f1d`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797d29db1aaad9bd5c0aebb832287e073ba8dfbf27fba3ce85b417d757130eb`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eaf5a9db5e5b0c8ee5099db68b3227a57c29b9b3bd879c87e60b84a5ded7f1`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1bfffdbe782b62c55f4e41a71f8d3d5ae7e0d68f7e8e6f070a56fa0d01a41a`  
		Last Modified: Tue, 29 Apr 2025 20:18:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d1efb809ea6433be59cd6f799cd5d71a31da2507c0317d65e30e217193587991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfb0b5a8543f039e7275c9dc4184761336206087e451fd39a0911ae73da76c7`

```dockerfile
```

-	Layers:
	-	`sha256:6828cbe3108c6036e8a8f26d449b358a01efbf17e2eed1dd6d3b14eca2376e6c`  
		Last Modified: Tue, 29 Apr 2025 20:18:47 GMT  
		Size: 3.9 MB (3934466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8bb9a1f2a7ca2f5dd9277dbe658fa96fc74cf1189b3fefc8bff8f63901875d`  
		Last Modified: Tue, 29 Apr 2025 20:18:46 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e0f9efeaba1cfd35206171ac6296d3b817aec20343c1bdfd197bc63f6bf0dd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61263300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8eda66d1f24e0ec652f1b4f7f096a77cbbb9c1e02d21088c3ca7530d62acba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf55cf3f7b075c849de2b0637905cbcaa155b900786312febc235450a3d9e186`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 11.7 MB (11688920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9841be6b1d29b72c332cf9244a69b73f9c3905a3e4fecab669cbcbedbfbfba6`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46418c781371c4d88a5c425804320b04a22ddf1058e46636a2ca953fe8730a19`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa2435d68921f8ee6d07f3f0321ac0a746a6cc96ad4de7e3796d252381e381b`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e62d3a2118bb599dfd9f8e453a6382752c4754e2800c1966bed52007242c91`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1e7f21d6d907d5a520c0d179a925520318b259293aada676b0ef391d2e64d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755ac7273bb9a8e9b95db677842cb92bd3f08ed9fd9fce77376afb941568f4d`

```dockerfile
```

-	Layers:
	-	`sha256:9e29e1fa7b2b3e13b3232afd949f2bb4e10ef5337bf92feef772fbd4fbb23deb`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 3.9 MB (3932129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e1593684c0bdf2ba5a620818c5ae41611116487fb181c1fb7766f3c694729a`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:e68b01fb0dea971fa4cfd39d8feb687c3fe2aa4bd228ca5e72189d11d8c78908
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:ec026f26f90a1da8ffc3ba59281854c0bb1a0b5f166e58e75d57f34e8424bd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa3d04109e9bf85dbba55e27e2b0055d3c73ba8b1f21907acb2c7bdb223320`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabac9a159eac99d387c3b1a92d15536e78c12f6596c2dbd37f29d0b63d5dffe`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 5.4 MB (5362390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e9f035d7685c2fdb1e905a640424e5ad669ee2970a32cbec7f8d889e3625f1`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb125018a09465c3a7d0200be55fc6435a06fe742fd5a7a7ef39a0fb83cfbf6`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46b9b7320bd76241047fcf77910ba82992b5e91e204eefe5390b265739db65`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 105.4 KB (105439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed731be31bff11d448e1a27d734e900b2e674625af668b3f9b87ba45b1a8f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fb983f465508bd38f2970b20fcfd3052779b73f8d3b436c6ab4ff79915307d`

```dockerfile
```

-	Layers:
	-	`sha256:079d7ce90a22f0bd844b80ccfaee90ce51150b4f1244f3519448f12bf6c83630`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 2.0 MB (2017825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d275b201a8175e6493a6207f8e73ff2b18780007de8ef8e54adc086578431b8d`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:39c9bfd66371de386419abe34cd806357a534145fbce48504409d1f8f396a4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45aed6d0d9e4f56fcf7aaaad06b6a747462168128f4a0d1f3e2084772af72fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2952dad8358145d90322cccd4047ea733f93fc11fed56791f2817ddc6d99d545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0237cdae437eaedee949f6af64e985420e981a9dfa9474fce1bb2e9aa7fbb8fd`

```dockerfile
```

-	Layers:
	-	`sha256:f307ef0a8e38175dd6e3ceb807d756938a14b991426d356ef4e8432d33ab7e37`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 2.0 MB (2018054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8946cab190197295b0fd0de39d4d1f5d0e06793a5eb36d0073e79597d9fd10d1`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:4c1ed82e5488cc7a87a4035c84b91368bf439418f76c388be8923760e27cc034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5b5f12c95fa70eba84ed0d9a8cfd320ff1f928e0f4ecc665553188865bc1fdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77302996458a5ea42a30e362fe60a32b80399042312ed4461165057feaadc3a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09894bd673fc3443fa4aac9c04f3790e80821023e1b647cb36b0dbb3295685a1`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 5.4 MB (5362436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b567f68d429f42a824fdac7d380831ff3ee4e919d2c1f56ac4ba2d5c728dab9`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe211eff3c4623dbc046e34c08495b6c3665295d30178fc8053cd5baff9b469`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93ed51b316d633e53abd6403ccacb66bf2b80b807810d40df2342572077415`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 105.4 KB (105442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca65e65a74419b6f595b799268195de974952d7e1558d9a39092265337398f`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:451612c81608c2bebc8d3e36a6a521b28025afe8d027348134cdac02a7ec34d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e43683e94761e4cae4d1f50b39b3b1ced64f4fb773232eb29f20df0b386bb`

```dockerfile
```

-	Layers:
	-	`sha256:79b4a3ef3b60d9c20c2340237fe4236376a35581ce8f29f76d044ea8920b97d3`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 2.0 MB (2017861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd949e8f808ff83620701f51061d8dc60e04b6e7afc9a968a71e3ed0ef991e1`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b31849bda994a89ea1e43d1ee83490728e5c84d98e21bb02362919c0ee14a139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9884153e1d1e0355067632367672016383e04b73464a2d8661e4d01f7cf3d14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8215c91245c0463263d03909dc6267e663f8bc6ca035c5fa1478e3632affb97f`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e0dd953f78b0d8045d26f7afb42c726a2cc4e07a96a2b3b741316ca99534d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea7d3f1b864509ea868bded897bb9ca30f452582999b77e73c6bfc798dd9443`

```dockerfile
```

-	Layers:
	-	`sha256:1fcbe13a76f25efb5f459970d227c4628a1a8f71064188a5cd94ffb6874dd526`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 2.0 MB (2018090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dac00fd22e65ab791eda65319d76e0834a665f17c3cf1d1784f781fa3bcd68`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:26f539327816198b90ed431924fec2ff158a98aa745b593bdfb2b2ae8c0cdb4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:5ca7d2535708de52e59146391a85e3222685b2101bcf6fbc69c6feaf164fa8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf1b0c7fa661952a44369df7910143a9f46830a62c9ee24693812478330d276`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7502f8f384c9e39101e17b46acf0f303f53f00c3076b70089bf8b5293c14a4e`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 3.6 MB (3623789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305875cc34b35c47d97f34abae20428fc4785a556dfebcb1e04c18a29117c3`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ad9396ff5157816c245d94d7dabb054e837511ea47b307ed3762318e74bfe`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ac9ef6b50c230c07920e2ccb263260c5218521277d00c0b20f9baebd17b8ff`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 110.7 KB (110667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:810ca171bbe3a461ad3f9c0c841ca6a05c8ceb604c62f05408e5d9b9fb683cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992fa750bd033c67b1276168605e2c584b3fbd033a0f2ae6979168542be25358`

```dockerfile
```

-	Layers:
	-	`sha256:364e84565c06cba8f2e91059f991c8688d269b08155b49077e48c4f2494fec78`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 2.1 MB (2055399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e73795a9937a5c5f7a6f43e8dcdc653d5018d6e430e3b67b8783a422fc7c17`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bfdcd9bb99802a608520d891d99b9a896b9e519c3fc710f5da8a3c92e29e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203958ef9579128f347a4bff0aa2c110790666b706dcff91afdf58e7071c151`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff69349668077007180f865cd316b1438d2244cfb6b5877a93d2ef957fae893`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 3.6 MB (3595245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ba73de0fee7dddc1e560209decbfbb8b8bfdcfc88bbab92fa5c475aea44d6`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f3443353aec912c7886b00a30c1cbded982093a0100e7b31360469c9bc243d`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d514962ad10eec887ec71fc1184b491c71747421dc4270402e4b0789bbf9`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 110.5 KB (110487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f47f5e2a24302ecae11fa9f56b627034c206301bfc142a63a03ba0ba63a2761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4792f4614d130d88d6574df8a599739fe6f52d661775cb0d3124c95e3f72c8c0`

```dockerfile
```

-	Layers:
	-	`sha256:aeb0c1d1d0fdd14937cc58efd46f5290c63cc757662509258f20fa18fadf548f`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 2.1 MB (2055659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a2eafa98dff300a61f97ed986282c056145cd6a289464d241a3947fc933ce2`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:e67dd8274275cc1bc4ccc9c495df2cba487d4c057261a5bbe3a675fc905f7b25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ea75232b46889271617dc481821e1909d05ce5e92545bbba1227bab364999f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d461c6f7b13738c6b4f1a89ee7e24ecff7dc5c5a5bbc035480235c5bff84a0`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b515f437b37abbbf80a20851603ea0e660cc33ed3133ce6e83a3a5001b47cfa8`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 3.6 MB (3623809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eac336a51090a23cc0914f157aeca298493cf6392d5a7bf98a11285541c58de`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89e1a0218ea67a334a752b5e3a2de2d7fce6f8229c537fed384ce40a6c73eef`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad56d373af038e98991e376e180b79cefcac28fcd50c4691e4936c45c0b2c83`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 110.6 KB (110648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ed4506459d767c55f263519a1a8867dcc18b98989376d59aa73bb765358090`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8083f260db3c7a548cbc86e95fe014cd17b417e18f266dc7177bb5a53f7d906f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c20ab0ef254c9cc608600b01f7841ed992b3760200c569b0a4dbabffb2f87a`

```dockerfile
```

-	Layers:
	-	`sha256:c5dec75c2040837c9f93ab3fe9b47cf1145215b4e726a25573ebf5efff863796`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 2.1 MB (2055435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d34f17d0e8739af8fb593e06c8d6482c9edbf64bcd81892b92387c37fe99cc`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d7d3fe31084430bceba93d5ef8c36791c06f81aaba37fd3061e605640cc21799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21edc9ced3f14de6089c514ea712e115634ea4f472b6bade77784b66e285b19d`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff69349668077007180f865cd316b1438d2244cfb6b5877a93d2ef957fae893`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 3.6 MB (3595245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ba73de0fee7dddc1e560209decbfbb8b8bfdcfc88bbab92fa5c475aea44d6`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f3443353aec912c7886b00a30c1cbded982093a0100e7b31360469c9bc243d`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d514962ad10eec887ec71fc1184b491c71747421dc4270402e4b0789bbf9`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 110.5 KB (110487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa8c2eec598bd3e1f629937728f657e829a66175aebd83ec75955e0610b7d70`  
		Last Modified: Wed, 09 Apr 2025 08:38:47 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a65e2f92ef29328dde9fa680fb2ba4202004cebd5d59beb8d6dfb27e06937fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88aea1a112a0452f1a588ced51bfba8be8fd61b854ae3a85f7f56b9bc1757a1e`

```dockerfile
```

-	Layers:
	-	`sha256:72ffbab84cded574356793b5cc86203486b55dd41f91eac101c436104bcd477b`  
		Last Modified: Wed, 09 Apr 2025 08:38:47 GMT  
		Size: 2.1 MB (2055695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0936d3750f33d18090c78dc9e1806e9c95d79d56b2cd5a5a2ea94dac2b22ec`  
		Last Modified: Wed, 09 Apr 2025 08:38:46 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:3933533efbcb36dce4797805ffac1fbd558f96a4f39af547cb98b2789c01a6d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:feb563112d19fff419ebaaf53bc5ebbc34dcc9040aa628f096c64581a1456e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34deb8132c5a1686ec9d58286361410699754a2f529baa356730c46175a0c4cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0dec45a929850354a090e228dca34ea64770e73d857734d9a726740b48821f`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 3.6 MB (3561457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f089d3e9c9757e05c4d1311a2d6aba13c856f4a573071a44317b2a6ba0fd4f`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7634be1479388a2b7edb17be8f8a1f9b6aa3c208bf603334d8e09a171c1ce3a`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a839418267feaba920430528a06b30b3cfb66c0f07340f224de25719c9ce7e`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 102.8 KB (102754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf4d8c29a06175b0473d2537cb5752dbd70d4448bf0158b28648dc07c6123f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2cd8ab6147458d6a82473940a41794b24d350ba03b1ac233e56c1158b53577`

```dockerfile
```

-	Layers:
	-	`sha256:bfb767ec62c3e301f953ba7598a86e910a45e3aee0d5e36d0c80f3b4d7f1d956`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 2.0 MB (1988003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81811e8647f0d03d6ec1be3d5d5e90a149eed9376838f9d536643e9fe7e4b8a9`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:14e68a1ef1499774ab0ff0549fb20c7f0834529679bcc7eae47638bcec32576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d970e55ec6b45eb6d0019fca0ed0c912ec1eb0d52993192334d6119b2740ef10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a6fe8ef82163d62cf9479c2af31f1dee76721ce7bdb1467f9784054fb5170`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 3.6 MB (3560005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7393046cfa6f68b53023c0509639d45a59706d5588f4480400d1b5f4d1d51c`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb7bd55d65f923168a612b75ca3362461569117659348df33de167f110e2de`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3b50d982d93658713726dd5112aa3092e61c54100c34a8400e31f062b0cb54`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 103.3 KB (103335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ab743af2d7bb08cc2c69eebc7eb51f7fdd2f5e7af502f6be85cbc87edaa281d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea7034c60b178ec24c97c8ca6c23f5e8bab3222ca1ddf30c46652b3ff1f9d01`

```dockerfile
```

-	Layers:
	-	`sha256:931bad7ad10f121b5bbe0f215058463c976a98a44f9b02f27f056603d1cd0f2e`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 2.0 MB (1989048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f27bf5833a0ccc06e9de9d76d1c100cce0c517576ebad70a34e924f9f8b96f`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:bb1f2ac5fe5f0fe5344c7f6e87115a959354b486f5c522e7b3bbd2c528825f45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdd4ee60546b3456f3198b0a327b0fd78e7c7da13ff05c7aab8954206e6704f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223dbadc92923109c96d9fc8fc28e5c04ff90f64ebff061e9659599ef2a5cee3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d3be5c72d2ebd1930b95e38b510610cdb291c3324059c55a09596571ba4c4`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 3.6 MB (3561362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de97d0aaf79df6e4cbb6915e4d4a0928c52bd14bfe06eb96dbcb17f26769fc2e`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b3caeb47db1287e5ec5631a60249266bbb9fdcc9a9922d551ff47aae973d8`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cef7682edab5bfa56738f780bb24e3f66449d19e8dce0cf54a9a9cd94233456`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 102.7 KB (102726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ecec4fcbc6ac0c3f46667ce1f223ee30d6e450aa0631e5b43427c23477be7d`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b9f65e539e873578da361c2db1d91aaadc2d8500c4025e4c8c60887b496e2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2162866fd4065055a2a1233c4456c060395e802d2823a032dd2c1f773090b6be`

```dockerfile
```

-	Layers:
	-	`sha256:ad9ad816620dd1b17b44cf321ed4c092277da0053c029ec00b44f8fa4dbd15c2`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 2.0 MB (1988039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa6831df1b93fe94bb9fdf856d3714daa7e72a01c7bbe7c77fcb0f869036229`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0b5d43d5d0aeea5fa8470c82bc076f4904af80272d015abc891445aaa063dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad171fc77df47499dbb19577f4ebfa52637116d2d4e09ab016e39f034ec6e09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a6fe8ef82163d62cf9479c2af31f1dee76721ce7bdb1467f9784054fb5170`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 3.6 MB (3560005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7393046cfa6f68b53023c0509639d45a59706d5588f4480400d1b5f4d1d51c`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb7bd55d65f923168a612b75ca3362461569117659348df33de167f110e2de`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3b50d982d93658713726dd5112aa3092e61c54100c34a8400e31f062b0cb54`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 103.3 KB (103335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de88003e696aae6b7a25af242820bdfcb0c3f13c1cbdf716fb4522a068a91914`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f224288087f656c2eecdcd327493c0110109c09f2e48320cc65c0fa9753c9200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d95a2c9aa6c999e08927bc4cfed6d4e0661f00a0f0e4991edde130e1faeb567`

```dockerfile
```

-	Layers:
	-	`sha256:05fac35361e74846c81e121b1c4498c97998ed8c8decd8931379676aa5f76396`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 2.0 MB (1989084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc577001764b48ee81ae794e79b54c0083061dd7294dec97e301105bafa0f08`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:3933533efbcb36dce4797805ffac1fbd558f96a4f39af547cb98b2789c01a6d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:feb563112d19fff419ebaaf53bc5ebbc34dcc9040aa628f096c64581a1456e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34deb8132c5a1686ec9d58286361410699754a2f529baa356730c46175a0c4cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0dec45a929850354a090e228dca34ea64770e73d857734d9a726740b48821f`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 3.6 MB (3561457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f089d3e9c9757e05c4d1311a2d6aba13c856f4a573071a44317b2a6ba0fd4f`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7634be1479388a2b7edb17be8f8a1f9b6aa3c208bf603334d8e09a171c1ce3a`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a839418267feaba920430528a06b30b3cfb66c0f07340f224de25719c9ce7e`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 102.8 KB (102754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf4d8c29a06175b0473d2537cb5752dbd70d4448bf0158b28648dc07c6123f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2cd8ab6147458d6a82473940a41794b24d350ba03b1ac233e56c1158b53577`

```dockerfile
```

-	Layers:
	-	`sha256:bfb767ec62c3e301f953ba7598a86e910a45e3aee0d5e36d0c80f3b4d7f1d956`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 2.0 MB (1988003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81811e8647f0d03d6ec1be3d5d5e90a149eed9376838f9d536643e9fe7e4b8a9`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:14e68a1ef1499774ab0ff0549fb20c7f0834529679bcc7eae47638bcec32576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d970e55ec6b45eb6d0019fca0ed0c912ec1eb0d52993192334d6119b2740ef10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a6fe8ef82163d62cf9479c2af31f1dee76721ce7bdb1467f9784054fb5170`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 3.6 MB (3560005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7393046cfa6f68b53023c0509639d45a59706d5588f4480400d1b5f4d1d51c`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb7bd55d65f923168a612b75ca3362461569117659348df33de167f110e2de`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3b50d982d93658713726dd5112aa3092e61c54100c34a8400e31f062b0cb54`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 103.3 KB (103335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ab743af2d7bb08cc2c69eebc7eb51f7fdd2f5e7af502f6be85cbc87edaa281d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea7034c60b178ec24c97c8ca6c23f5e8bab3222ca1ddf30c46652b3ff1f9d01`

```dockerfile
```

-	Layers:
	-	`sha256:931bad7ad10f121b5bbe0f215058463c976a98a44f9b02f27f056603d1cd0f2e`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 2.0 MB (1989048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f27bf5833a0ccc06e9de9d76d1c100cce0c517576ebad70a34e924f9f8b96f`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:bb1f2ac5fe5f0fe5344c7f6e87115a959354b486f5c522e7b3bbd2c528825f45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdd4ee60546b3456f3198b0a327b0fd78e7c7da13ff05c7aab8954206e6704f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223dbadc92923109c96d9fc8fc28e5c04ff90f64ebff061e9659599ef2a5cee3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d3be5c72d2ebd1930b95e38b510610cdb291c3324059c55a09596571ba4c4`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 3.6 MB (3561362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de97d0aaf79df6e4cbb6915e4d4a0928c52bd14bfe06eb96dbcb17f26769fc2e`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b3caeb47db1287e5ec5631a60249266bbb9fdcc9a9922d551ff47aae973d8`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cef7682edab5bfa56738f780bb24e3f66449d19e8dce0cf54a9a9cd94233456`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 102.7 KB (102726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ecec4fcbc6ac0c3f46667ce1f223ee30d6e450aa0631e5b43427c23477be7d`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b9f65e539e873578da361c2db1d91aaadc2d8500c4025e4c8c60887b496e2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2162866fd4065055a2a1233c4456c060395e802d2823a032dd2c1f773090b6be`

```dockerfile
```

-	Layers:
	-	`sha256:ad9ad816620dd1b17b44cf321ed4c092277da0053c029ec00b44f8fa4dbd15c2`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 2.0 MB (1988039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa6831df1b93fe94bb9fdf856d3714daa7e72a01c7bbe7c77fcb0f869036229`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0b5d43d5d0aeea5fa8470c82bc076f4904af80272d015abc891445aaa063dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad171fc77df47499dbb19577f4ebfa52637116d2d4e09ab016e39f034ec6e09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a6fe8ef82163d62cf9479c2af31f1dee76721ce7bdb1467f9784054fb5170`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 3.6 MB (3560005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7393046cfa6f68b53023c0509639d45a59706d5588f4480400d1b5f4d1d51c`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb7bd55d65f923168a612b75ca3362461569117659348df33de167f110e2de`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3b50d982d93658713726dd5112aa3092e61c54100c34a8400e31f062b0cb54`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 103.3 KB (103335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de88003e696aae6b7a25af242820bdfcb0c3f13c1cbdf716fb4522a068a91914`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f224288087f656c2eecdcd327493c0110109c09f2e48320cc65c0fa9753c9200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d95a2c9aa6c999e08927bc4cfed6d4e0661f00a0f0e4991edde130e1faeb567`

```dockerfile
```

-	Layers:
	-	`sha256:05fac35361e74846c81e121b1c4498c97998ed8c8decd8931379676aa5f76396`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 2.0 MB (1989084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc577001764b48ee81ae794e79b54c0083061dd7294dec97e301105bafa0f08`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:896a90715f946f951e18c7d14f0a2f4ea736cee5a4eda37f3390565581545692
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
$ docker pull neurodebian@sha256:50ceb91bc809109f14330fe913d7c5a4fd4cac8baa17311891d7815bf127caa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8243cd751996381b2414a5dfc84cd4d02f659bcbe3f50ac9577e74d497589865`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1726cb87390148585fab582d55c50d11fb91d1fdd0bd1b1ca56b3d30d0ef84`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 11.3 MB (11266846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0d9b893b8c73e8692b95563238811eee14de20516dd375669a29d2b9109f15`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa9335b96de158069a27ad40d057e8544955195a4bccf3348b8a7b7a84b34aa`  
		Last Modified: Mon, 28 Apr 2025 21:57:10 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1336facc6fb76372ce29fb4525827d75ec167ad737ae1e880886237ca216d69`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 93.2 KB (93161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea040038db3b8aa770bf72904c12a92c6715546f4806118468c78d26fb619b0`  
		Last Modified: Mon, 28 Apr 2025 21:57:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d005157e723d9670ee7d251f7ed6c16809d7546d81ea26eb76f80b3190a1574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525a2b1f93dfd30f84e0a8bb3f291a733d6ee875a228756db804773ba2cfe52`

```dockerfile
```

-	Layers:
	-	`sha256:17e92b9cad98e0352bf39ec10ff10c12c5b37a9f87a8e3b0f279ff125b75d1b1`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 3.9 MB (3934212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0b26a5e913156ebd2c17fb450ea4d488a12f3fadc0d49b332f985c71da7194`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f031e9118f0d032736b359371d83c0c1aba42e6372fca911615ce627ffd5d020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59656294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8e9780422504003ec47f8bf6e1162dc7fa2e330048c9a7f9b0309816248d5e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e779c0c5fdbd8639cbb065648917ee4734d2cb9fb9c196dba52c90d4da7432ef`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 11.2 MB (11232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151d4e03d0d99ffb7b30916bb2e40ac5049633d3f098d072e599571fb7187f1d`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797d29db1aaad9bd5c0aebb832287e073ba8dfbf27fba3ce85b417d757130eb`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eaf5a9db5e5b0c8ee5099db68b3227a57c29b9b3bd879c87e60b84a5ded7f1`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1bfffdbe782b62c55f4e41a71f8d3d5ae7e0d68f7e8e6f070a56fa0d01a41a`  
		Last Modified: Tue, 29 Apr 2025 20:18:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d1efb809ea6433be59cd6f799cd5d71a31da2507c0317d65e30e217193587991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfb0b5a8543f039e7275c9dc4184761336206087e451fd39a0911ae73da76c7`

```dockerfile
```

-	Layers:
	-	`sha256:6828cbe3108c6036e8a8f26d449b358a01efbf17e2eed1dd6d3b14eca2376e6c`  
		Last Modified: Tue, 29 Apr 2025 20:18:47 GMT  
		Size: 3.9 MB (3934466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8bb9a1f2a7ca2f5dd9277dbe658fa96fc74cf1189b3fefc8bff8f63901875d`  
		Last Modified: Tue, 29 Apr 2025 20:18:46 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e0f9efeaba1cfd35206171ac6296d3b817aec20343c1bdfd197bc63f6bf0dd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61263300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8eda66d1f24e0ec652f1b4f7f096a77cbbb9c1e02d21088c3ca7530d62acba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf55cf3f7b075c849de2b0637905cbcaa155b900786312febc235450a3d9e186`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 11.7 MB (11688920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9841be6b1d29b72c332cf9244a69b73f9c3905a3e4fecab669cbcbedbfbfba6`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46418c781371c4d88a5c425804320b04a22ddf1058e46636a2ca953fe8730a19`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa2435d68921f8ee6d07f3f0321ac0a746a6cc96ad4de7e3796d252381e381b`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e62d3a2118bb599dfd9f8e453a6382752c4754e2800c1966bed52007242c91`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1e7f21d6d907d5a520c0d179a925520318b259293aada676b0ef391d2e64d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755ac7273bb9a8e9b95db677842cb92bd3f08ed9fd9fce77376afb941568f4d`

```dockerfile
```

-	Layers:
	-	`sha256:9e29e1fa7b2b3e13b3232afd949f2bb4e10ef5337bf92feef772fbd4fbb23deb`  
		Last Modified: Mon, 28 Apr 2025 21:54:47 GMT  
		Size: 3.9 MB (3932129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e1593684c0bdf2ba5a620818c5ae41611116487fb181c1fb7766f3c694729a`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
