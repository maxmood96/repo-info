## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:f1700f710fb3a7a7ffd7accf0a37c4009bceb1d2017a8205c6c60109fc57db29
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
$ docker pull neurodebian@sha256:3e1e23c85e5bbd51fe50d63418e35e66134c2ffe2f0645c7a4fb95a55f915f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fab33cac0afcc8955f876e9f2516b2593e2071b93bdd8fcdcfdc67b5bd7eb4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca7f8441975b558ca0ef283f56f08f77825f779c076f6de3575109057618921`  
		Last Modified: Tue, 12 Aug 2025 21:25:50 GMT  
		Size: 11.3 MB (11266802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515da2cae6f4e931c65953b83787a4ed52b06f8970245c8033c02dbe26d32d52`  
		Last Modified: Tue, 12 Aug 2025 21:25:49 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05313306ba9a3a0b254f27c2009f9fcf26e25872e146ec58b68f3f122e9e0c4a`  
		Last Modified: Tue, 12 Aug 2025 21:25:49 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61c2a6c5996ede28c75d6706f475897d1f12b8f2741dc359bf1d5337e64abce`  
		Last Modified: Tue, 12 Aug 2025 21:25:51 GMT  
		Size: 93.2 KB (93166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15131243c0bc8e7238da0779914743d971ccbb6a4c7278acaa41b925dbde7af6`  
		Last Modified: Tue, 12 Aug 2025 21:25:50 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56136ee322b43713bfcef696875cb804c977177bdeeb15ab5ec769eba7ba62af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c4db29c0f03c077b176a86f738264f0994c8af0b9181fa2d8b02f3273fc49a`

```dockerfile
```

-	Layers:
	-	`sha256:90d172a22a1a332971f73b7920c30fab0bb63a4644d128ebb0ae1439329a6a1a`  
		Last Modified: Wed, 13 Aug 2025 01:07:28 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ba733a68ceeec254a0fd4c848d419e069030e5403e7a0277c33ac4f6b24dfc`  
		Last Modified: Wed, 13 Aug 2025 01:07:29 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ba4f5c9d0d8e3e88067449edae8ab672eb4b606fa9dcfc9bbe53120ed06b3fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cc5e8120b309a808b8b17384338da1db82b3ea82dadecfd2ace44069dd3bdb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398157a4590ac7aadba659d655fa1e00f8f05a8ab0784529d0099545f337bc03`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 11.2 MB (11232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e01fcd5942424056ba8f0b9a313ff0dde95202c4e3440076fc637b0813c64d`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405e7c25660e800db97c97594d0a4f9b537b1a9fc32793315de1592d0bcfdb9`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2527f69d856843d89ea49d0ee163b7a03c78ceaa2f858c3cbaddacefb732357`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 93.4 KB (93433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f77e7ba9063abd80126010a77ce29596d5e4ba6c0dee2bafae62978e16d71df`  
		Last Modified: Wed, 13 Aug 2025 08:24:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cced9e2b54e8933202292fb68c6cd3012a6e3b144d28f849eb9f3461833ea802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8929676cc0ef7a9617249ccd15b195901245d06533ca9e718ab60f88e10ddec5`

```dockerfile
```

-	Layers:
	-	`sha256:a2f476cc4360921349bb63f66510650c7ae8c83cb34b75346b64ded471694c9e`  
		Last Modified: Wed, 13 Aug 2025 10:09:32 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc458f66151a39b80f39079ebb5ead336f86564387a23c18609431aff638ef3`  
		Last Modified: Wed, 13 Aug 2025 10:09:33 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:01e8d00045f91fb4738ddefff5ce32ca1be6209de1c09736dbf43c5370751b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16b3729e307a1bf3bd90822470070fee8025ff7fff664dcde64d0fc71908edf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
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
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5394d0fd08e540a301e3b5f99b64f94f1ba947c5bbe47e0d84a2339afa6c994c`  
		Last Modified: Tue, 12 Aug 2025 21:21:53 GMT  
		Size: 11.7 MB (11688885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e663a91a0aa6dacdc64c684bf82d797030d47adcbff357a5cf069460c1197d`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d45030c4feb33187c49f2fd35da69d2b0a7ae3af8dda4972d933421611e48d5`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a397d8483559f951b63a3b5852d5066f8d70d659c67795b7972d016edcf480a`  
		Last Modified: Tue, 12 Aug 2025 21:21:51 GMT  
		Size: 93.2 KB (93211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ff42e5d40a326607d815eb58689a4a20fa2e74ee8668f764f746eadf40a2ad`  
		Last Modified: Tue, 12 Aug 2025 21:21:50 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bdeeddf6ecca857b4fb89f5b698b4675a355670b44cee651810417717e91070f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73276fe5c06baf891d0fa4cebc9ca03db4c8538c244f9f88efe7831ba61ca6fb`

```dockerfile
```

-	Layers:
	-	`sha256:7528113e7f1996421b92ce6c09b20a6971bc66a7884394ec37d5edb8d1c0a25f`  
		Last Modified: Wed, 13 Aug 2025 01:07:38 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f7f08ce14ba39a229be1a13e27219db34478e744420cca8df3c9878a15d1e31`  
		Last Modified: Wed, 13 Aug 2025 01:07:39 GMT  
		Size: 16.3 KB (16311 bytes)  
		MIME: application/vnd.in-toto+json
