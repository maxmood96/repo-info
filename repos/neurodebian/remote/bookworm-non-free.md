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
