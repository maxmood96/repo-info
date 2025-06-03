## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:b0fd02fb64867772094c3388f3fa12061f0b1641292c3eb9d4514f5c667eac4a
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
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f0b21e9a2b1d87e8e9d1cf617208198e10c617d9f80b1339ff54ce27ee66c91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36204bccfc429d1ecc0ab3e4cb4d125b9a3f7594aa42d97f2f51c173dce13323`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Thu, 22 May 2025 03:20:05 GMT  
		Size: 93.4 KB (93443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89280029104abf21945b59b054a3eedf9f7b23e94999b1aca58011419c300a`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7e6da63402e4b1eef862b0d8a3f101017276aecf02c60186b794120fd687915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107dbd281f4baae96d89cf725ff834951638204a9503b9812136446b2ad9caf4`

```dockerfile
```

-	Layers:
	-	`sha256:b4f000b0ebc61fecbc86e06e322d07a3aca6d8fa3ed3c9d7d781d5c75cbcf560`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 4.0 MB (3955116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73550faaa5db727c23fdf4536980baf5f17f7a89739abf435a3879571e512a4`  
		Last Modified: Thu, 22 May 2025 03:20:18 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

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
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
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

### `neurodebian:bookworm-non-free` - unknown; unknown

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
