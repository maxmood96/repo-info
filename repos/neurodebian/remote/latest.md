## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:7ea37f7caac43b4ef8ec7fe324816a9dc014c3ea7f26f5e516fc35a5fb18fc8b
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
$ docker pull neurodebian@sha256:a5cf34f4f7825d94fc2337e20eb543fdf07edeec9faa728ef68e18c8a80163e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efee154831aa413a0a1a7e37ea8de60c5acabf853e3d32bb30ddd4c7fdff96cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457e7788552337eafc2fb5171b202fe2567d0a63d8740a19d74db3f68ff4df8f`  
		Last Modified: Tue, 04 Mar 2025 00:29:30 GMT  
		Size: 11.3 MB (11266877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d366fc607bf383bf17c6d940fd56417639297c9673d1f7baf91d9f9ae00476e`  
		Last Modified: Tue, 04 Mar 2025 00:29:30 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b4abb037c055b0e61f2cbabbc5a0a2450eb5365df144d708fd7f85646afb8c`  
		Last Modified: Tue, 04 Mar 2025 00:29:30 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aee0acd8d0140c20de07158ac30b9a43961e57b28747876484581ed3d2d170`  
		Last Modified: Tue, 04 Mar 2025 00:29:30 GMT  
		Size: 93.2 KB (93186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f669f232adff0bcd413da0af81b785676542790ba925aea2cc62ad1fcad0abfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b6d506da5766b8cac56b2277c3d33d09c38a6f291e8761dbf51f36ee53733`

```dockerfile
```

-	Layers:
	-	`sha256:71cfd13c94b079eba60c42dfab96e36bb46459283d07744b1da1ff5cf5fcaac9`  
		Last Modified: Tue, 04 Mar 2025 00:29:30 GMT  
		Size: 3.9 MB (3932828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26733a997ce0759260b5aa3b0bd5f4cc3d51cbab9e2f390058ad1fd8c9ad5d62`  
		Last Modified: Tue, 04 Mar 2025 00:29:30 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d341df33dc4a4b564b0c87796350ae270ce86256347b63e316e9e0e2f2193e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fa60e5f8a6f867c62db1e223fc0cad0c482d0a8e5bd16d1712ddcc59d25f65`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f934fdd885043c38d5ca3311bc219b22c6b73a0e7858d6b2f280b43194e664b`  
		Last Modified: Tue, 04 Mar 2025 00:35:24 GMT  
		Size: 11.2 MB (11232534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606a2d4a3a2584c4c7d955389d138d52a3609637cd3eb74998a5ee5c8b20b4d3`  
		Last Modified: Tue, 04 Mar 2025 00:35:23 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc81288c2e2e7c51508531a4ec9e32086ec519cf09e49a0ea58c3219a247321`  
		Last Modified: Tue, 04 Mar 2025 00:35:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc512a0ea219679579dffe3e7d4b1ed1ba1900e5b906eb85085207d86ca620`  
		Last Modified: Tue, 04 Mar 2025 00:35:23 GMT  
		Size: 93.4 KB (93395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:07ee22283455e9c1bce91c123beb7418317e3ee75a8da9b9f8998a3c88cd53c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d20a2abdcb9b2c08cdc94df1c9b148853b7767b5a910814c34c233673b920a2`

```dockerfile
```

-	Layers:
	-	`sha256:0521310e15e47494eee3d6673506a46142a9a64ac5437009c816a43932a7bd25`  
		Last Modified: Tue, 04 Mar 2025 00:35:38 GMT  
		Size: 3.9 MB (3933082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09adba5af8d580a4c464c88c7206025de6ffd3493c431cbb122f63179399238e`  
		Last Modified: Tue, 04 Mar 2025 00:35:37 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:4588d4ba0df90c382061837acbe8a680b1cdd9b13918b81ffb5c1aeaa2ea901b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d52a6806d69c0c604a9f26eed4a8c0c375ac7d01ad8e26009ebfea03f25f44`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c117430c2bab0250d0c45a59b513985508f1b415a0b7eb524f06b086398bf28`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 11.7 MB (11688957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a31ca4090d5b713c0c95692f7644f130dfb79fdd746896b2bd7ff8c7ba936`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80284e308e4ef3ef520aca9382c4f1be14ee161d48fb138b966a6a42e28b3f51`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc790eff23946c9b3948f4a4a2630a588675c55e0589b592ff37b0bce2e39647`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 93.2 KB (93222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d971a0334905d6b52689f3723f560c50b318853cf4be24ee67578b030e28c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc28a774c79046a54c24e207ad8f101bcd9e1cca7c590387c63af55cd04b4fc7`

```dockerfile
```

-	Layers:
	-	`sha256:36bd51cafa3ea645a9c346ec7d21586478bfdf74440abd688c0de2af0f67465b`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 3.9 MB (3930745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:558d76118c11b534d1dc57e0037ef8d00b7667af34bd3d905c34bc98c647bb70`  
		Last Modified: Tue, 04 Mar 2025 00:29:17 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json
