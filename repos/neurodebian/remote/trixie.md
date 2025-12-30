## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:e0b772fb6c8cbf95b4bbc89d59fce54bd4612bea788c25876003179d85a81dc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:11704eb3e9e87e0bfc0474ec7993332f1a5446fd8fcfb93d5bfa76ddf865487a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfbefed7e757187bdc0ba33ca6e231ba0ab03e1d8c01c26ec51bffb858b7f8b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:01:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170e174478fb49afad823cff539b37cc66f46900a7285d0980c69545228ad17`  
		Last Modified: Tue, 30 Dec 2025 00:01:57 GMT  
		Size: 10.3 MB (10289740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98cfd6b6685e00247a8830717622cc76428a34a65ea509838b1ef1cf5f05c74`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c93be1b43a47437859927119984568576e4e7035c09a3328ef782132ad5794`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3130c56d9674187b01ccfa85c055fa9f25023403e80cc08d3bd3fedb46556a5e`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 90.2 KB (90240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1fb327732ae3459a5ace9ae68da17e6b718a91b6edec2e4ba30e8a6c1ce4cc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dafd6febb344bc094cee781197ce68c717521a93152c82a6b3faef2618045e4`

```dockerfile
```

-	Layers:
	-	`sha256:a4c38d6616572e011521486de1ca5c77b753c05e8ac2873b363b81ebd8663c8b`  
		Last Modified: Tue, 30 Dec 2025 02:08:59 GMT  
		Size: 3.6 MB (3613029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e815c9c1e880979ed5797e8604eda18f89cdbc2a0f33a15aa08c9c99c1babfe2`  
		Last Modified: Tue, 30 Dec 2025 02:08:59 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f08af078412593f5e90c7ccc438b36a60853c367d5b1c02977191e59b42e2140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc02347a607123200510623e11328eccf357ded43e2b4c688cf6f3cbd87d6cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:02:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:02:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809d9a2a116ddb1b5044a05d97a74f3b666af6ebf3396b8bd1959b09b2c1dd97`  
		Last Modified: Tue, 30 Dec 2025 00:02:25 GMT  
		Size: 10.1 MB (10073354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43bf434a486a4ffeb412351889920cd853dafb22023f8b56041c1f5d9551def`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fc09b5259d60baa90e66794a8eee4353a12a09741ddf610bc593a7d1a33885`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d0d5e7c0fe7290044e8a33d358ea3fb2637f4a077ae7d449ac0eda02e54e27`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 90.9 KB (90861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f741d89d851cb0175bc345ebf91d0267a3fd846824aff01df647a8423163d3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa99d1b3e6f5e16c3a14b8a2671503fc5c6d885230e3d8d99a1e1783b14e6c5a`

```dockerfile
```

-	Layers:
	-	`sha256:3e2489caeeb90f29d36cf18405d9c354b196ce6768875a219a8c2483595e7b82`  
		Last Modified: Tue, 30 Dec 2025 02:09:03 GMT  
		Size: 3.6 MB (3614556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6028461904b5f9e69fd501748e03c048131c821c768f588bfb954e678cb0680`  
		Last Modified: Tue, 30 Dec 2025 02:09:04 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:c8dc1f5965291d82532beb930b4b8dd9d2857dcffb348f41946ce7525f9d1868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4224f54fb533cad2f8b9b30d2e785eb1fd843e4fd63e905343da0c070c075d03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e964d190139b1aba3de28d11b605a95f92489da3beb9d80e9099db336eb72530`  
		Last Modified: Mon, 08 Dec 2025 23:15:43 GMT  
		Size: 10.5 MB (10463020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec584c96f35b189d796255e99284eb2b5a60beac79d3aa5e9e38511057c721`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b780ecf3cdbfe9614a0f6fb11f3ac440968fc9859f8381cdd325606eb10d5`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e72d44ba44c44786256e5c59963306628e9bc4225d957dc3c3f88b69404871`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 90.6 KB (90608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8feb71ee0324566413295afd412d3e8536f97cd4923d4b4e3a66a630eb6b5e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f48fe17c7803c7f0a740da48d64460f0e14b205e6ef00e468dd25f6d417492`

```dockerfile
```

-	Layers:
	-	`sha256:6565d47d0408e99891700b9f73772b468617ffa2decbf66dd47aa2f3825e0c46`  
		Last Modified: Tue, 09 Dec 2025 02:08:59 GMT  
		Size: 3.6 MB (3610978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928694ae3cbda82a9b5864d3bb2e6e8cc4bfd721706dd53996bd42268ab412db`  
		Last Modified: Tue, 09 Dec 2025 02:09:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
