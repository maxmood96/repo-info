## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:f6e680a2730aa165430fb7b2397ec4fc7376cfab7606fce027c4da0819ad5cb3
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
$ docker pull neurodebian@sha256:8d63c53715ca04153f29d307032b15af604a09d09b77f59650cf848a3ff608e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64950026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229aed07a08563adf03dcc3bfcd2e3760f3949366c2d468b1310001d9ae9757b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f6fd7e0223cdb148d5d913c07f6babb1568f0b86b7f9ccfc45369f5e324987`  
		Last Modified: Tue, 25 Feb 2025 02:27:00 GMT  
		Size: 11.1 MB (11105064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c963f1c8f82ad189a5fc4b0f31b35cbde49379ef9b0ea9b811bb4d5a5ca77c6`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8704f813802b2ceaa6dd7637c468ab12a1006422aa69e5e7d489cd115a799ad`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b485ca6b951ab61bb5c0b158a544c43accbda527cad07cc5b9b5220319ceb348`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 101.2 KB (101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd86c041609621d93bac1450edc528f252eb3ebac4b2f75fa5bdcbc6a2cb473`  
		Last Modified: Tue, 25 Feb 2025 02:27:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0df95cb09083c0e0b21182c4b274d27c968294d38a549738fde69702a1fc62d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c614534c484237f1b3623825e24962fd19d58efc9d22f06240977e3d39cfca`

```dockerfile
```

-	Layers:
	-	`sha256:7485d10d0dccf6932268f1ae0c302116cd9544ae22dbce2bf6d2cb6aa4bcdb78`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f847d9340aa4eae840c9d35f745ee6db4ed0710d06fd2381e5fa4521e0b84b6`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:adeffd7d7b4876d93490b45f1bf7db0a31ebe2c91fe557a5ed33e7dcd95afd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e9bc24d7d988dbc1b420003629bdab58a106a6a0f17ca197d784887859b9d3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e95529282fe4b2c53926ffa260e910ca2e7edbe840ec6045501427c2b0fcc2`  
		Last Modified: Tue, 04 Feb 2025 10:14:11 GMT  
		Size: 11.1 MB (11105949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3498b7aa8199bc97f275a3b6d10573f41165c0eb35ce7ff70f2f3ddd65a4f5`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af64b7d26c87753053c75134052452ee120a3493c4d975102854f002f29f65c`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628b5ae84a5cd3de98a4de2b27f64955e4e5e004721258979acdb6b183904370`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 101.1 KB (101102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df83d3c23da0b5df36bdc784ddee25b91909ea0340f81b77341cbd0e75147f18`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b1c2a555a093d89edb798b9c41eec081c742e59307253be2f5bd4a5899147d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9bb42f0dc95e2bf94c144e676c423415a7b1442a83ede8afbd5847ddeea66`

```dockerfile
```

-	Layers:
	-	`sha256:dfae46ead578e6973908c1a2c813a24d46fc554aba3026407ed83cee0b4ddc46`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5c6fe5fa24a9bafc7f0d161f4b11d10f8578478a0e160fe998a3ec5ac64941`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bda7ef7ecd9283b7822b07b53f221a06ba49fe489060c8a9508d82e98f19bb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064cfaa3cf2dab53ecb8c8de999dfc5d23f3c411e2325896a9a89394c8b02c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484422fd4a1d6ec8ee86b88a25b7b6de58842c0a9766192f8aecc828773d4fb4`  
		Last Modified: Tue, 25 Feb 2025 02:25:41 GMT  
		Size: 11.5 MB (11500408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b0d8ab6eda4034ddfc4abf4375bb7c39167373be9c5b8855cf35709d1ab05f`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8a333b07c35d233d46d7299bb98c76c919c06db1f4b65e5162c094a47a5e45`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630be2d9eda0730b7509b08fc22cc48cb4b2eac0b889ca41056dc7b28e6ac464`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d797416760116642baffb3f545f96399dfdd457f6ee83878d72a6226b27a0`  
		Last Modified: Tue, 25 Feb 2025 02:25:41 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a099be5c16e0ef0a587fc39e2b0c0256c7e453cc89738defc3c6fb1b01b4435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a091dddd9c3609266c5ae727ab24372cedd9e442aad30db1105e60ae0cbe3`

```dockerfile
```

-	Layers:
	-	`sha256:cbc827a05c0eb7c5911633103469d0490d1e56755eb0b1b0cf2748ad4eece5b5`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c2802a2c27fb32ac6e543ac9e274c3da613e921c48a1c00719150e87b37c16`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json
