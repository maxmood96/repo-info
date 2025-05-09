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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c11fcffe851b5e799a87d40b72001861eb28a55703bfd725f426c3ece51c77`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
		Size: 11.3 MB (11266789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7f51c087fd27487523c3326871684de41b31a149a14770bf8119560643c6e`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d047d0a8b4395623517336d1eb42449947af65fc5199dcce0fdf50054d793057`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e6abf1a25573145adc50f804864b0d1ecb2c0651aba756443d4d373fda34b`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1726cb87390148585fab582d55c50d11fb91d1fdd0bd1b1ca56b3d30d0ef84`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 11.3 MB (11266846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0d9b893b8c73e8692b95563238811eee14de20516dd375669a29d2b9109f15`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa9335b96de158069a27ad40d057e8544955195a4bccf3348b8a7b7a84b34aa`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1336facc6fb76372ce29fb4525827d75ec167ad737ae1e880886237ca216d69`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
		Size: 93.2 KB (93161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea040038db3b8aa770bf72904c12a92c6715546f4806118468c78d26fb619b0`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
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
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
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
		Last Modified: Thu, 08 May 2025 17:55:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
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
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
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
		Last Modified: Thu, 08 May 2025 17:55:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09894bd673fc3443fa4aac9c04f3790e80821023e1b647cb36b0dbb3295685a1`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
		Size: 5.4 MB (5362436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b567f68d429f42a824fdac7d380831ff3ee4e919d2c1f56ac4ba2d5c728dab9`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe211eff3c4623dbc046e34c08495b6c3665295d30178fc8053cd5baff9b469`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93ed51b316d633e53abd6403ccacb66bf2b80b807810d40df2342572077415`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
		Size: 105.4 KB (105442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca65e65a74419b6f595b799268195de974952d7e1558d9a39092265337398f`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
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
$ docker pull neurodebian@sha256:aadc2821c4fb100912b0a0d2c9ba79b614a0122d76baa24f63cfbfd0c062b184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:ff397a72c04635a55579c8025e87c06b6cf211530dde5d332b8249d330403d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e39866c7946bcfc6840c4e0c99798ab2301423e994f67a9b59d18f006051ab0`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e387fe46d51819e286a445a33730411d77cc121bdb8d7ac28c4aadd0707c98`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 3.6 MB (3623974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54b7cc7b061332b4a6b548f407a16b338ee39763686db874cb834f2d4ad034e`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 1.9 KB (1907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520ca9bcfad5d90a0eb1962746c00b9e58f7f6a659e1955b030090931a988f17`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d29396d7a0397fad77c5b789679468a4e54292b1ca963c71a189bc1447add1`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 110.7 KB (110735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4fd0a38a8864f58f17eb71d15c509a9af8523f3cce63c9b1eed228223de4b276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4e035ed95fddeccc12432c50e575f8715ba7dff8ea464941082279652f25c7`

```dockerfile
```

-	Layers:
	-	`sha256:5d065183ca637ea10089b70a42744d342f113104e1de406d1984cb23cccc57e8`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 2.1 MB (2055399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fe24312cffe4674cbc61ea735748398745d60cce6907ad9b7499079489cda8`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:46b114c6a25d43df06b2367455c9208520e94efb8378f95ded9fb8d031489677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3eccf9b41da37d14ed42d0a2aa76b82cf032fab74de0b4cae3db7f8106dee4`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9b9bbe7463741dd05852bef3e20e4918abb3791e642a53459b7d85a0df1441`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 3.6 MB (3595231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c9a28db0b9d01ec102aabc19b0194e5bc43f48ed9950e82f9438f3bda9f35b`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebccfe88dcf3d8d97ae8ae10386013782461c92e29200dbef75ff693b974276`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd85b43d1613815fca29c2e3b2c7ca24988c55da52443184599ad7aa6946614`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 110.5 KB (110473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71f716a084d4d17ddb17637a7f72b7a8e75a6dd0aa10465d31d778990ff99e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ba0ba152a487af6adbfe538db7aa9421d5d5bd70884f71dda994d1b82b5ac1`

```dockerfile
```

-	Layers:
	-	`sha256:bff8e5a61a14d45e82c3c5f84b93a95274e27a52741f7a498c777670e183b4a3`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 2.1 MB (2055659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7103e27570378d3659f9b71c2a8a96c2531f4f5d95c7f33694c437951a1e222b`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:06b142b4d711bcbe195b005e3ded7479e8ac36e7da28e1dcbe3d3e3f0ad9914d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8745b4739d43041fea2d9f3cfca5c5e72fcfcd7f09ba5e70b6d5363b833d37c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cd179c855f547eaaf62baa8b60401a814378d56efb9cfbe7656a01acb5be5c`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b419c3ff37ef2ac5fa82f5b85314a380bf9dccefbcd3caf5c82f12d45db2dd`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 3.6 MB (3623949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ffc54fef5a2d95fbe22699944431dfe32ea22be8fceb724c9a18978e3a546c`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b757fab4386e86d70a5e84a8a4601e713cc6f6daa82716ceb1b547b41edbe9`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caf4a0206137bf9258208e5033f88f354a90cc40585f68548a934a1413d70fc`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 110.7 KB (110734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3443176ce74e235df7f2ec70f48ec7a2854b049c120c10ba5a497ee12cb2ae4e`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:268deae095fe3c5d59a663f99295fd94d9a0b6f4eff5b68fd180dcd72677ec4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd244d65c53f38bc322681b81e82a26034d1932ed27d13d45c8ad73a52211c9f`

```dockerfile
```

-	Layers:
	-	`sha256:d1171e76917a57f087d2c9519be618651d11350d4f57894452eec95304e0dd80`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 2.1 MB (2055435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d1503584e01253addc76624f770c194dde029241bcfe7f365cd29333796a49`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c63a127ef850b3ec3c132de842bd669ee2be494083d6bef49ec96eaa8823da47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c555e8be455732f19d45cd584d48a1533ad6edde311a21c8aa9dc5b6bbb2387`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9b9bbe7463741dd05852bef3e20e4918abb3791e642a53459b7d85a0df1441`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 3.6 MB (3595231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c9a28db0b9d01ec102aabc19b0194e5bc43f48ed9950e82f9438f3bda9f35b`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebccfe88dcf3d8d97ae8ae10386013782461c92e29200dbef75ff693b974276`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd85b43d1613815fca29c2e3b2c7ca24988c55da52443184599ad7aa6946614`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 110.5 KB (110473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564cfd3215f87ca4868d1e044c8559b75a587d7ab8a81be3104288780e46562a`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea84e072fa2cdb2fb3f2883fc76128e015c6df4df208436e4f62689758261b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a87abcbd2d0153452c05655e838d1d47ee61b4d91a78d94161824743b4c62c6`

```dockerfile
```

-	Layers:
	-	`sha256:1c6ad0d29e8ceab0824b00a9285f398a0305f3ea937b8905d8d097127dd9ca7a`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 2.1 MB (2055695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939dda7ef0ca78df8d4c0860a093b314a5dabe7120df3d94b553415a47d19fcb`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 16.3 KB (16345 bytes)  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c11fcffe851b5e799a87d40b72001861eb28a55703bfd725f426c3ece51c77`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
		Size: 11.3 MB (11266789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7f51c087fd27487523c3326871684de41b31a149a14770bf8119560643c6e`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d047d0a8b4395623517336d1eb42449947af65fc5199dcce0fdf50054d793057`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e6abf1a25573145adc50f804864b0d1ecb2c0651aba756443d4d373fda34b`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
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
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
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
		Last Modified: Thu, 08 May 2025 17:55:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
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
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
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
		Last Modified: Thu, 08 May 2025 17:55:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c11fcffe851b5e799a87d40b72001861eb28a55703bfd725f426c3ece51c77`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
		Size: 11.3 MB (11266789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7f51c087fd27487523c3326871684de41b31a149a14770bf8119560643c6e`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d047d0a8b4395623517336d1eb42449947af65fc5199dcce0fdf50054d793057`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e6abf1a25573145adc50f804864b0d1ecb2c0651aba756443d4d373fda34b`  
		Last Modified: Fri, 09 May 2025 00:42:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1726cb87390148585fab582d55c50d11fb91d1fdd0bd1b1ca56b3d30d0ef84`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 11.3 MB (11266846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0d9b893b8c73e8692b95563238811eee14de20516dd375669a29d2b9109f15`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa9335b96de158069a27ad40d057e8544955195a4bccf3348b8a7b7a84b34aa`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1336facc6fb76372ce29fb4525827d75ec167ad737ae1e880886237ca216d69`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
		Size: 93.2 KB (93161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea040038db3b8aa770bf72904c12a92c6715546f4806118468c78d26fb619b0`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09894bd673fc3443fa4aac9c04f3790e80821023e1b647cb36b0dbb3295685a1`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
		Size: 5.4 MB (5362436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b567f68d429f42a824fdac7d380831ff3ee4e919d2c1f56ac4ba2d5c728dab9`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe211eff3c4623dbc046e34c08495b6c3665295d30178fc8053cd5baff9b469`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93ed51b316d633e53abd6403ccacb66bf2b80b807810d40df2342572077415`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
		Size: 105.4 KB (105442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca65e65a74419b6f595b799268195de974952d7e1558d9a39092265337398f`  
		Last Modified: Fri, 09 May 2025 01:53:03 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
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
$ docker pull neurodebian@sha256:aadc2821c4fb100912b0a0d2c9ba79b614a0122d76baa24f63cfbfd0c062b184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:ff397a72c04635a55579c8025e87c06b6cf211530dde5d332b8249d330403d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e39866c7946bcfc6840c4e0c99798ab2301423e994f67a9b59d18f006051ab0`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e387fe46d51819e286a445a33730411d77cc121bdb8d7ac28c4aadd0707c98`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 3.6 MB (3623974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54b7cc7b061332b4a6b548f407a16b338ee39763686db874cb834f2d4ad034e`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 1.9 KB (1907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520ca9bcfad5d90a0eb1962746c00b9e58f7f6a659e1955b030090931a988f17`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d29396d7a0397fad77c5b789679468a4e54292b1ca963c71a189bc1447add1`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 110.7 KB (110735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4fd0a38a8864f58f17eb71d15c509a9af8523f3cce63c9b1eed228223de4b276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4e035ed95fddeccc12432c50e575f8715ba7dff8ea464941082279652f25c7`

```dockerfile
```

-	Layers:
	-	`sha256:5d065183ca637ea10089b70a42744d342f113104e1de406d1984cb23cccc57e8`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 2.1 MB (2055399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fe24312cffe4674cbc61ea735748398745d60cce6907ad9b7499079489cda8`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:46b114c6a25d43df06b2367455c9208520e94efb8378f95ded9fb8d031489677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3eccf9b41da37d14ed42d0a2aa76b82cf032fab74de0b4cae3db7f8106dee4`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9b9bbe7463741dd05852bef3e20e4918abb3791e642a53459b7d85a0df1441`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 3.6 MB (3595231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c9a28db0b9d01ec102aabc19b0194e5bc43f48ed9950e82f9438f3bda9f35b`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebccfe88dcf3d8d97ae8ae10386013782461c92e29200dbef75ff693b974276`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd85b43d1613815fca29c2e3b2c7ca24988c55da52443184599ad7aa6946614`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 110.5 KB (110473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71f716a084d4d17ddb17637a7f72b7a8e75a6dd0aa10465d31d778990ff99e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ba0ba152a487af6adbfe538db7aa9421d5d5bd70884f71dda994d1b82b5ac1`

```dockerfile
```

-	Layers:
	-	`sha256:bff8e5a61a14d45e82c3c5f84b93a95274e27a52741f7a498c777670e183b4a3`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 2.1 MB (2055659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7103e27570378d3659f9b71c2a8a96c2531f4f5d95c7f33694c437951a1e222b`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:06b142b4d711bcbe195b005e3ded7479e8ac36e7da28e1dcbe3d3e3f0ad9914d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8745b4739d43041fea2d9f3cfca5c5e72fcfcd7f09ba5e70b6d5363b833d37c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cd179c855f547eaaf62baa8b60401a814378d56efb9cfbe7656a01acb5be5c`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b419c3ff37ef2ac5fa82f5b85314a380bf9dccefbcd3caf5c82f12d45db2dd`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 3.6 MB (3623949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ffc54fef5a2d95fbe22699944431dfe32ea22be8fceb724c9a18978e3a546c`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b757fab4386e86d70a5e84a8a4601e713cc6f6daa82716ceb1b547b41edbe9`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caf4a0206137bf9258208e5033f88f354a90cc40585f68548a934a1413d70fc`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 110.7 KB (110734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3443176ce74e235df7f2ec70f48ec7a2854b049c120c10ba5a497ee12cb2ae4e`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:268deae095fe3c5d59a663f99295fd94d9a0b6f4eff5b68fd180dcd72677ec4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd244d65c53f38bc322681b81e82a26034d1932ed27d13d45c8ad73a52211c9f`

```dockerfile
```

-	Layers:
	-	`sha256:d1171e76917a57f087d2c9519be618651d11350d4f57894452eec95304e0dd80`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 2.1 MB (2055435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d1503584e01253addc76624f770c194dde029241bcfe7f365cd29333796a49`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c63a127ef850b3ec3c132de842bd669ee2be494083d6bef49ec96eaa8823da47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c555e8be455732f19d45cd584d48a1533ad6edde311a21c8aa9dc5b6bbb2387`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9b9bbe7463741dd05852bef3e20e4918abb3791e642a53459b7d85a0df1441`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 3.6 MB (3595231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c9a28db0b9d01ec102aabc19b0194e5bc43f48ed9950e82f9438f3bda9f35b`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebccfe88dcf3d8d97ae8ae10386013782461c92e29200dbef75ff693b974276`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd85b43d1613815fca29c2e3b2c7ca24988c55da52443184599ad7aa6946614`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 110.5 KB (110473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564cfd3215f87ca4868d1e044c8559b75a587d7ab8a81be3104288780e46562a`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea84e072fa2cdb2fb3f2883fc76128e015c6df4df208436e4f62689758261b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a87abcbd2d0153452c05655e838d1d47ee61b4d91a78d94161824743b4c62c6`

```dockerfile
```

-	Layers:
	-	`sha256:1c6ad0d29e8ceab0824b00a9285f398a0305f3ea937b8905d8d097127dd9ca7a`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 2.1 MB (2055695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939dda7ef0ca78df8d4c0860a093b314a5dabe7120df3d94b553415a47d19fcb`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:f95676da88045789e619860caeb6a3ecad7e5735e7fe3cba9bc0245f6499fa2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:d38770387a1f54d95d0d558099909093e51c2a541d725a169a3ab440228ce641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e059b96cc5ab2387c1bb2485d9de3fe3aa2dab08159f4e56de08657ed279f9`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aae2be978b6887ba33cc355eb60849e9a4b6494da48dbc2025ec215fc048bbd`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 3.6 MB (3561550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214a87e3f5642da384965dace0ef6f6fe356aeebd976cea08d1deb25cc5b17cc`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 1.9 KB (1907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c2ffabb65505adc1a9bd197602a784b5362d2bf73c24ab87ff05d5de31986b`  
		Last Modified: Mon, 05 May 2025 16:36:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418af0f32ee06323cc96c6ebd9014c231ad3deaa60e018b922a41d15df29cd9e`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 102.8 KB (102849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d05f6938da9aeb0879b1fe995f7e53f824b9806df54a2cf758869d5a75b9fd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3bb6b2ab29942ba9926b585f6a9f2762e3332b5b0917f6c506a00cb07af85`

```dockerfile
```

-	Layers:
	-	`sha256:db5db1fcebc99c5ee245340feaabb7749eaa8dd62337d6b75728edd76c2e33a1`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 2.0 MB (1988007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae603c4f8c4fdbb75e2ff13d822ac64719e2cc5269f96c64fbd4e9433d674d53`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ff983cae8fa779ca9d445f0e2e30c9c0c03e867cff63e93ec397123b526af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9506d7bae42cf7450aa75eaeb8571087a3a9d4066fc59a980c2149e19578d`
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
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac21e8e96238695c860d38f337d7bc1fc8004ea7c02420374175bd455adc01`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 3.6 MB (3560024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc1ea305697372c2857b25e00b899c927cb6bc69155e067e49c0a9bba9402a`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b43beb4a469f9bf1d5fbbde21ed17e9307737945bc57d9f78fc561d40e08ea`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861dc62479460407739b1ccc0c1b1ed34a4710f546a7bb95fdfa45af3b8efd3c`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 103.3 KB (103339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:222ce1225e4552dab3c723682de0a2272dd746e75ef288a430f54e46046c4985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de3d7a56bd63248962b3eb96296da8be24233a5f3739114ca94981c5ccecf8a`

```dockerfile
```

-	Layers:
	-	`sha256:691e9a8ce459d8732c2d0bfe0a5462ebd479d481a963330437c6d61ca42d888c`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 2.0 MB (1989052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c66f9e1f8f25f8e1de91b113698830913584ff5a51823d5484ec6d26a10084`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:69ce90ed413297d173afe360aad6f52bb5176e84eca7931478cd30ca79a58961
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:13066bdb3f041d79fea341879cf32fc99e1501130aba61e38b5bb537e26c6d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e766d4c7c665af01ecdf3c7f5ebacdb666da09a8f6a3fc562abc8135cc5e5b1`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5d60262949712c1e9b418187e3cc8bd5f8d0cd29eb97c9e363914cedaa63b`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 3.6 MB (3561531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4ccf25a7e89dd343d5f776bf03085f2ba18bbad5a4100ece345624e0a595c`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53011f9a2cfb2befb053a53ab616fbc8cdc2c34c7c16c3d64268caf75936a28d`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d8f4ff9e91fa0098e89a942d5178c56e58307eeddb25322eb98cb14237292c`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 102.8 KB (102845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f18bdc3a399429a3003a5facfc548c193056b9f8a3c92159a30cdc1478fdfc`  
		Last Modified: Mon, 05 May 2025 16:35:50 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c63cacdcdeb7eb72ae8539221ee0ebcb57c3925d98bbc09a2a6ec531638dff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c783b424c09b07cd1ef4bfbe1afb9b6a360e746ed91c3589067e70bcefa6ac7a`

```dockerfile
```

-	Layers:
	-	`sha256:0e6a2844b7765ed34907f15e7585e8bdebc12f3faadefd03864a0f5d02a826d0`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 2.0 MB (1988043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314f1c1506cd318e08789d785bcc4374c81b8056d15a4514197f223b08c7268a`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a790631dcdafe28f015c5c0479912489674be9f8f6443c5baa269296a9aac686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6ad30b4f18c93b1b8b0d5ab83d85d1a12a4e4200c5a5b3d74087d39e1af734`
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
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac21e8e96238695c860d38f337d7bc1fc8004ea7c02420374175bd455adc01`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 3.6 MB (3560024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc1ea305697372c2857b25e00b899c927cb6bc69155e067e49c0a9bba9402a`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b43beb4a469f9bf1d5fbbde21ed17e9307737945bc57d9f78fc561d40e08ea`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861dc62479460407739b1ccc0c1b1ed34a4710f546a7bb95fdfa45af3b8efd3c`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 103.3 KB (103339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c89c90922ffd5d5f4ad5e74b112d2030c727ce2904398c5ceef67660d3c259`  
		Last Modified: Mon, 05 May 2025 17:47:55 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f372e8ab37fe59a92e06d06cc943b4f987a2b0248f30c3165bfed88b8836e189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc218ebea555829040d03a4a15c0f5df5da7efb29ac615a2891b238c37f82455`

```dockerfile
```

-	Layers:
	-	`sha256:acbad4c4e58f95388548674e8a027f84744a36ba854c40bcfe075c25f9afc1c0`  
		Last Modified: Mon, 05 May 2025 17:47:55 GMT  
		Size: 2.0 MB (1989088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d3aee94659ed4646a4d848ec65ba5ffaaf28e5be2b04557c641715a24f788f`  
		Last Modified: Mon, 05 May 2025 17:47:55 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:f95676da88045789e619860caeb6a3ecad7e5735e7fe3cba9bc0245f6499fa2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:d38770387a1f54d95d0d558099909093e51c2a541d725a169a3ab440228ce641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e059b96cc5ab2387c1bb2485d9de3fe3aa2dab08159f4e56de08657ed279f9`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aae2be978b6887ba33cc355eb60849e9a4b6494da48dbc2025ec215fc048bbd`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 3.6 MB (3561550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214a87e3f5642da384965dace0ef6f6fe356aeebd976cea08d1deb25cc5b17cc`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 1.9 KB (1907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c2ffabb65505adc1a9bd197602a784b5362d2bf73c24ab87ff05d5de31986b`  
		Last Modified: Mon, 05 May 2025 16:36:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418af0f32ee06323cc96c6ebd9014c231ad3deaa60e018b922a41d15df29cd9e`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 102.8 KB (102849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d05f6938da9aeb0879b1fe995f7e53f824b9806df54a2cf758869d5a75b9fd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3bb6b2ab29942ba9926b585f6a9f2762e3332b5b0917f6c506a00cb07af85`

```dockerfile
```

-	Layers:
	-	`sha256:db5db1fcebc99c5ee245340feaabb7749eaa8dd62337d6b75728edd76c2e33a1`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 2.0 MB (1988007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae603c4f8c4fdbb75e2ff13d822ac64719e2cc5269f96c64fbd4e9433d674d53`  
		Last Modified: Mon, 05 May 2025 16:36:03 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ff983cae8fa779ca9d445f0e2e30c9c0c03e867cff63e93ec397123b526af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9506d7bae42cf7450aa75eaeb8571087a3a9d4066fc59a980c2149e19578d`
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
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac21e8e96238695c860d38f337d7bc1fc8004ea7c02420374175bd455adc01`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 3.6 MB (3560024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc1ea305697372c2857b25e00b899c927cb6bc69155e067e49c0a9bba9402a`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b43beb4a469f9bf1d5fbbde21ed17e9307737945bc57d9f78fc561d40e08ea`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861dc62479460407739b1ccc0c1b1ed34a4710f546a7bb95fdfa45af3b8efd3c`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 103.3 KB (103339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:222ce1225e4552dab3c723682de0a2272dd746e75ef288a430f54e46046c4985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de3d7a56bd63248962b3eb96296da8be24233a5f3739114ca94981c5ccecf8a`

```dockerfile
```

-	Layers:
	-	`sha256:691e9a8ce459d8732c2d0bfe0a5462ebd479d481a963330437c6d61ca42d888c`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 2.0 MB (1989052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c66f9e1f8f25f8e1de91b113698830913584ff5a51823d5484ec6d26a10084`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:69ce90ed413297d173afe360aad6f52bb5176e84eca7931478cd30ca79a58961
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:13066bdb3f041d79fea341879cf32fc99e1501130aba61e38b5bb537e26c6d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e766d4c7c665af01ecdf3c7f5ebacdb666da09a8f6a3fc562abc8135cc5e5b1`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5d60262949712c1e9b418187e3cc8bd5f8d0cd29eb97c9e363914cedaa63b`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 3.6 MB (3561531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4ccf25a7e89dd343d5f776bf03085f2ba18bbad5a4100ece345624e0a595c`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53011f9a2cfb2befb053a53ab616fbc8cdc2c34c7c16c3d64268caf75936a28d`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d8f4ff9e91fa0098e89a942d5178c56e58307eeddb25322eb98cb14237292c`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 102.8 KB (102845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f18bdc3a399429a3003a5facfc548c193056b9f8a3c92159a30cdc1478fdfc`  
		Last Modified: Mon, 05 May 2025 16:35:50 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c63cacdcdeb7eb72ae8539221ee0ebcb57c3925d98bbc09a2a6ec531638dff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c783b424c09b07cd1ef4bfbe1afb9b6a360e746ed91c3589067e70bcefa6ac7a`

```dockerfile
```

-	Layers:
	-	`sha256:0e6a2844b7765ed34907f15e7585e8bdebc12f3faadefd03864a0f5d02a826d0`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 2.0 MB (1988043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314f1c1506cd318e08789d785bcc4374c81b8056d15a4514197f223b08c7268a`  
		Last Modified: Mon, 05 May 2025 16:35:49 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a790631dcdafe28f015c5c0479912489674be9f8f6443c5baa269296a9aac686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6ad30b4f18c93b1b8b0d5ab83d85d1a12a4e4200c5a5b3d74087d39e1af734`
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
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac21e8e96238695c860d38f337d7bc1fc8004ea7c02420374175bd455adc01`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 3.6 MB (3560024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc1ea305697372c2857b25e00b899c927cb6bc69155e067e49c0a9bba9402a`  
		Last Modified: Mon, 05 May 2025 17:47:43 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b43beb4a469f9bf1d5fbbde21ed17e9307737945bc57d9f78fc561d40e08ea`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861dc62479460407739b1ccc0c1b1ed34a4710f546a7bb95fdfa45af3b8efd3c`  
		Last Modified: Mon, 05 May 2025 17:47:42 GMT  
		Size: 103.3 KB (103339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c89c90922ffd5d5f4ad5e74b112d2030c727ce2904398c5ceef67660d3c259`  
		Last Modified: Mon, 05 May 2025 17:47:55 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f372e8ab37fe59a92e06d06cc943b4f987a2b0248f30c3165bfed88b8836e189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc218ebea555829040d03a4a15c0f5df5da7efb29ac615a2891b238c37f82455`

```dockerfile
```

-	Layers:
	-	`sha256:acbad4c4e58f95388548674e8a027f84744a36ba854c40bcfe075c25f9afc1c0`  
		Last Modified: Mon, 05 May 2025 17:47:55 GMT  
		Size: 2.0 MB (1989088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d3aee94659ed4646a4d848ec65ba5ffaaf28e5be2b04557c641715a24f788f`  
		Last Modified: Mon, 05 May 2025 17:47:55 GMT  
		Size: 16.3 KB (16345 bytes)  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1726cb87390148585fab582d55c50d11fb91d1fdd0bd1b1ca56b3d30d0ef84`  
		Last Modified: Mon, 28 Apr 2025 21:57:11 GMT  
		Size: 11.3 MB (11266846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0d9b893b8c73e8692b95563238811eee14de20516dd375669a29d2b9109f15`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa9335b96de158069a27ad40d057e8544955195a4bccf3348b8a7b7a84b34aa`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1336facc6fb76372ce29fb4525827d75ec167ad737ae1e880886237ca216d69`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
		Size: 93.2 KB (93161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea040038db3b8aa770bf72904c12a92c6715546f4806118468c78d26fb619b0`  
		Last Modified: Fri, 09 May 2025 01:07:21 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
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
