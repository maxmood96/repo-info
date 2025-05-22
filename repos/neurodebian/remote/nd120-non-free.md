## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:e5f9ba802426ea12a41c4d22c84b76f64a7fe5b63ad38ba9aef83f1007fa86fd
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
$ docker pull neurodebian@sha256:851e63864831469546085f6a457288bab67ac55db23fe8184195c000da461f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1140577c4fa48a7d165ccc461ad7e892f8c319ffc1838973c42f4cd47fbe908a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682aa3f8a7a0c6b2c3f7e69082a7641b2f8a398db39cea59e30577ab2cd9545c`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 11.3 MB (11266852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74fe3db0b2d5102c748c1dced6a2d654dcfe6325440f5ad12c7d15b9e2a4ca`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b621e6e6f14028ed190e855d6f2b7332388d7d99f86177c0839d80572400cfb2`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686d88df96b49bdf2c13c3a23f6cb8d645961840a556883c3cc5b79b9185eb01`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 93.2 KB (93186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6586d320bf1e1e1821085a599b7260b177db8d637dffbc69299cb7848af335c`  
		Last Modified: Wed, 21 May 2025 23:33:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa004cfcf0e1cb0d21a28babe2049d496a76da2dc5adddfdf974e2f8efad05d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061fdf2951dbc561a9c508a39236c8c3dd4a204b208530753faaa768e80ac32a`

```dockerfile
```

-	Layers:
	-	`sha256:305ee82f38619bafff21cca2294c2411ee720c40e0020e78825eeb6c523714a2`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
		Size: 4.0 MB (3954862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b44bd6c10531f89f0b05cc959d4ead7f25c043efd5e5810173fa6bf75fb2de70`  
		Last Modified: Wed, 21 May 2025 23:33:47 GMT  
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
$ docker pull neurodebian@sha256:bfa199662e75b2c37492367434358c210d8a355f2bb15868b5b769db9193be49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61256320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b532a8a00c0c0d7b9dd3f7f594b120af5664d70270ca19502f4e7bc233aace4c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
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
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2befdc47cd4cc9a43be4226914197171d517dbe40274f5b26c8088cdbcaa2b9c`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 11.7 MB (11688920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1bfa09a90b3a837330dd2a72b46dca98d510d8427fb5b9162ae3be7a83bba9`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18aa48402f14aa565c4a322fecbcc79be120249f1f6245662825df0b4a4d37a`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c2353a2d9dd0fffbf5018f9fc815a0ccef03054aee9386f0bfbb9f4d63b6d4`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 93.2 KB (93217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db8ce6f79b3373f6fdcacdddb049c597fb580b389a159ada0336d9dc29e05c`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc54ac074ea1a6afab79cac6dfcfab8d9003737aa056274f441cdf463fd1528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3920c7ac1fba6d508e7195907458fc78fa48d79d67c362e3e13a116d968ef667`

```dockerfile
```

-	Layers:
	-	`sha256:afa6979159e91d00fa568b799a399cc939346264429fe4419c17550b77367215`  
		Last Modified: Wed, 21 May 2025 23:20:36 GMT  
		Size: 4.0 MB (3952830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b28f32383b18cc13b5a4e44e0a3ca98b957af3a8d6c2667e4b7ab8c4a5dd80`  
		Last Modified: Wed, 21 May 2025 23:20:35 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
