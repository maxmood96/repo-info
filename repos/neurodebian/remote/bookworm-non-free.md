## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:1e5336de47c0916153b95b268b167627f1dcbbb014b0dfe948f093a782d4337a
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
$ docker pull neurodebian@sha256:8cd5e6b7bec8b2fb545404fa4ef6bd502469cf4951c316d6e6279f2853160096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59634890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4830671f1f42f572e6707b244573102e521ead223e96423ff85026ae06f25297`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0890be792eb8cf2c454fe7c038fba6da83a8ef251447a532fa6d4f3108c2f7`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 11.2 MB (11232504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99eec1b3a608d28ef329abdd58a2e25ee524c0453b1269a4668003e0983d49`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86127ee86de4c4cff8e4bdd5c18c3f9d3021d01a9a46fb1e63a786d3c5abab3`  
		Last Modified: Tue, 04 Feb 2025 10:14:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd76384f78a868cb30bf0b964090aebaad99664c593dc1fcb7897c3ca2af13`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04417613519d31f6f792cca8327cad6db9d5664fb6531c5c94f92801518ff51d`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5ca00e53e65addbf1adf8782ccd07719cda0df67061120dae1afa0773d8cf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e6e0a88411798e9de89e740aec9110aa51198ec12d4d77b9188f3b5d0ab85a`

```dockerfile
```

-	Layers:
	-	`sha256:2c9e1237745fd9d27f596daf590b01f333c1e6ed5054993d33f0533e77edc71e`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 3.9 MB (3933104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3978024698224d9e7ae7a49ba553a6391e10f049df270264dacc9a5d2e8d971`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
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
