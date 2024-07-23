## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:9934738130c0d0eac989ad9387f991401146190767c418b84da3c5b4473606e5
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
$ docker pull neurodebian@sha256:fabd233511b29371372f9c089fd4b683864f679d1d252216ef8eea4864ca2c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe07a5b4c9c1ea95f2170b1a0087e99a61040d0d41574896c04818aa8b9015e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3ec0f21348ab8b97e349a1a230224eab2abaa91a9bc15ec1756ec679881613`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 11.3 MB (11266567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b6525920c59417749f5f5ed2a2b63bf70e4372d1ad1e43940269f4e46a6a39`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d510146f760f735becbde5f61ec22ff8776568601bab5334c20503e95b76a154`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b114ecc986793dc815210203aae62abfa08219b0f843467dbc1eeec64b622d3`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 92.8 KB (92781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5408265a03e3fc2f5df205622d83f4dccb742f73006527dd9e1a4ffb01eac9c`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:580991d536d1bc4083e536e117f083c498d841a0f9d1f6cd22c6f20ce261626d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9974c18c88586a5a7e0be07f0b836711a742452a233bb0f02ed0035a72456b`

```dockerfile
```

-	Layers:
	-	`sha256:37efcafc97e143a00d67dfcc8a8cce6afb3fd0ee1a47ad53c1283a640f457d55`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29a33d0193d9594976606f3cbea45d1c7997a112205fda7d13587bf33e8faa5`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8ad50c552d2d9ba9971607e3e25fcff5e656fe578bc84e4ebd7fb18738512adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b4c5c48066c6bab18c83db1004c63f2276ce263810a3b47cd0e67ca0e5d0be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c4964b2c74b33113f4f9253f8fdbd6f9effb7070fabfe7998ec7f9f71a68c`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 11.2 MB (11231990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a84d3037e0ebe02d7b2e60abbfa3c50ab185daf05e3e55e3f8ff6cf96a45b2`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784313ea4757f773fd668b9d92e36d3061207f4d5f2fc7c75d857979e14d6f21`  
		Last Modified: Tue, 23 Jul 2024 18:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51ef3b42547d51fc5c3da2f3e174e60effa7629f2f7e46098c454225497cd1`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 93.1 KB (93109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a89e8d1db6d68a3f2363d7ce074b5496e4fa63f099ca409686e3f84f30ebda5`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d20471e880f9bbd6c72aae7179ae7d0d26c0ea16bbfc67999f481fe78ad46d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08416b7a7fa5ef781f905251ee5d1a660baae6bfaf1e10c86a265115cf1660ef`

```dockerfile
```

-	Layers:
	-	`sha256:01968acc1d8a7282a89c4b803ed512cd39f8497d1768e0cf330e008a56dfdad1`  
		Last Modified: Tue, 23 Jul 2024 18:36:06 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13697cc7290159bcf6b045e62a67f922b62336ce65509f7615633065b67364b`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 16.1 KB (16113 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ca14280056db89cfb3698b0f5ed6f7f98c228f7b413c045d84ba87127e8c13e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50812a4495199c3e047fae3ed8ad96942ce0584681f827fed5d49c763caa0d6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c2009cb5fa8b7669e4a2ddc7fe615fd9380d7fa24095ac161b734c176809b`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 11.7 MB (11689019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581009e1a3eab679cc96f1a56f84957915a31999300ee01d3b0eb71c1a4c9bc`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fe1928d3b2e8e4b5cd4c4b503be928244764ffb7b11b74acb72b734dd9f208`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfed7927d4c9944bfa51451f9fd78ccf4f2fec34f40ef194178d40a8c4bae9c`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 92.9 KB (92902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3ea134dabf34c21bb382a7c8d3557c91f40f18a3d35d74d32798fe37081a31`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:585b7f303597ee97acc8e1fd4412bdee58c4ae5d0eb0e80b2a2df82125aa3cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d25650556ecf8f5da6c003c46848f43f3fc156dd14b89a1d52b24f3e9e829db`

```dockerfile
```

-	Layers:
	-	`sha256:788b93f4232871e16b9893be5e8b6cde56c93769029ffa2a5cd71dee99730b96`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f697f0775bb09d617db679f5fa2ad36451d8af809edc427f8cfc7a07c8b1e80c`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
