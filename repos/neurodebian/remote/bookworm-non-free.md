## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:5f1c4ffb3aaec94eb85ba6d1159dbaa5d6058199f3c0a84887ab78b469a56d94
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
$ docker pull neurodebian@sha256:86d0f1e008c22ef1371791860617d59b2e903a4d642e928b30e47fa6b181da18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde7ea88b09684b422a1ac05b6b2ad01622129128e5db57512bdd2f99aa342b4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28441ab853fef772e1e1de08ec36f3ed7180ff3c2a9b9c9e671357202dcdd42`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 11.3 MB (11266799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505ff7e6422a09a3eb1a239312fcdaa2044a0e3eefd0c31485b820c54e4b7967`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d76303fdb4aa5d6083836c5414c3e64b7b9e08dfa94e4900c30eba602003b37`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179af51425b94c30d8dc80554e3ef4c9003f44a94784a75458c79f151ab32c10`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 93.2 KB (93157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36083d574b636b75357cbc3e722a118cdd90d3d27dd10a838646f855d03bc976`  
		Last Modified: Tue, 25 Feb 2025 02:27:21 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:672e5a788f4e12dd192919f23b3cdcc8c247268af0e4c265c3b187946806ca98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94236d5f014c5f6d7cd9746c73b7ebabab74fd82e06f0c1da40d26af73f6b90`

```dockerfile
```

-	Layers:
	-	`sha256:31b0617d5bc927443e4c297613d85abb99148b4e4f2e104f826075d993c933b7`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 3.9 MB (3932868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7b4463e7f6d4ef42c049f42246d69980142348e3e7e3a4ef61fb6eb3128006`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:abb99c9c2f059106da856b9d569b4d8b7ca84af59582e6a68cef696edd394382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a022a8b30b7ae18ba216b15f04cbe65382f23139ec4b2b210764daa78ad1fbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268effafc2bde885b308f4884da9a5675b21ea9dd10510af4cc390b22435225`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 11.2 MB (11232612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc8fd8ac1e89535a292d7b52efd5bea69c5f5c3851d37b9929659c0c6c042e`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe958a62bf286f5dab55b9feda9c4012922a2405bd34a8e0570b16801e9f1257`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeac118fe924197167da22818e9394a97999867f5e156777e4fcae652229797`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd5763534ceb76e91f0383484f364058ab48c26cef0fb32914ddad1372da0f8`  
		Last Modified: Tue, 25 Feb 2025 06:12:50 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e7c7ed56d0e480fae65c8cde83e1d1adbc75c0a9a9fced612884ab3a96416e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0204f4c376b7e83a2ff9a754d837369ce083d2bccb96e91a0b065a72eaf2d6`

```dockerfile
```

-	Layers:
	-	`sha256:1737f3c716a72e8e417e4d27d5f130b9ad3b8d0a1374350ae0b58459419195a8`  
		Last Modified: Tue, 25 Feb 2025 06:12:51 GMT  
		Size: 3.9 MB (3933122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fad213bc7f30b41f083d0ea35cc189d394c753fdac72d9e11045dadb9bb777a`  
		Last Modified: Tue, 25 Feb 2025 06:12:50 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:14ea109b5493111055a5aaa853884637148ae4dc485ea5c4e267bdb1add74a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61243186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a7ea209e5b0e6d013100f17eff90f4100955ab738acde7026b6c79cabce3e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52022fd04bcf4f92943afd60360f0ecc2322d7d18d6a0abe22a2cdfe8bcecf6`  
		Last Modified: Tue, 25 Feb 2025 02:12:30 GMT  
		Size: 11.7 MB (11689076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900a00b32801477083168732fb13544e2003e9538368e35080da03e1b17fb70f`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d197c332a3b1cc7550c3bff0a9d351b9730cc7493035604b55fd1b1407153255`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3e2f6fb6f036e3845a4a8b6ee926f3c8d48e922eda645aabbe2681ca3fc57`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 93.2 KB (93240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b9cbc42e9997903403815a1064c86c6cb272ea90c7fc977f69733045254639`  
		Last Modified: Tue, 25 Feb 2025 02:12:30 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d24e1d2b84e10d04805b51e11dd0c50d764501f818f8967b77329b63d229d33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021833d77fdeb79557411acea2ed9985e2d023e575a7287135cb2e1166396447`

```dockerfile
```

-	Layers:
	-	`sha256:335ee5030d46d154190ee10eca81ff2e045c93fb885778864658042d9925fc8a`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 3.9 MB (3930785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:578220ae32d85546c71d91eb6f5654e7c4554c058444cf7711da0b069bef4176`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
