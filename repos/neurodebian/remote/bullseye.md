## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:d666b7dfd1e2c733118b91bd9d2e28456600cf9fd6f39d432996c331ed871fb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:3a3dacd8dc96c4600157ef1952dd2e5e4fe982d2dad7431358d7c27e4c2757f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66292272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8d90ef9e063476eb296f568d628c75554d9d83100f01bafafdad95e9cf216e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95209e4966d531d5c931399542274b21d850060079423c08a1878a68833aec55`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 11.1 MB (11104986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfcc9d547b28c0197ff7a323d9b22b76f47e15814975d67dbbb97e53ebafc35`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b41d188bccfa3b45960a95c278f8c902024914b7b05ed0d0e79cdb870715e05`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f638952d08e98890b62f809755d2c9ad0a07dc8fe6504baba832485584467aca`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 100.7 KB (100721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46d70ce8dd8d99e9ce02056cb1ad5d54d105614367bd5c1f56262b4a2bd5ea0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5efa4a7f679eeef05b95a9a80a10f17e7415178c98a306cb70a4fbaf47d51d`

```dockerfile
```

-	Layers:
	-	`sha256:cee9eddc17c2655dfb9abaf0cdf71d375aada9bcaf16023262c5a0035da85efe`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 4.2 MB (4223704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4501df5eb6df5c5c2f4feff8ebd1f42e47607ab814df96b3e3c861aa70e2c7b`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cde9c5093d7919668908f2795c05bc199d0c432638f67e9d14b309ab2edb8eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64938431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befb656edf4b25ace9183765b76423f2197e84039d81357e21cf823f3bfde5e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748620df5e1335ff4d2a1ff3d6b29fdcadb199a1da1c0f954ee400b0987da57`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 11.1 MB (11105782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28772ec05400cd0f7075f13813c452cc315f7c87a3370a48753a5530b8c202b2`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74765cc784e39ab51976cb4f82860a87708d3a5f7bba696c461c07136ec85c5`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36deb65a886758fde62b0455cb2efcf0eba23ed9c43693d1ed048665413046`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 100.7 KB (100677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b631b50282e273242ea8ec4651730804f5e39c293de9e9c41e6d2059aa6f5952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e537dc44a9bf7b9bb9cfe463e69b23d635f05116354a8724e9eb267376818e0`

```dockerfile
```

-	Layers:
	-	`sha256:6a24eb35e9e307896a7530df9b7ec113f39630d9ca0832ba730d924cdb69fcdc`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 4.2 MB (4223309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea98358f3ad2b7c9a87381e505c068f04bc1c3c1c5f79192474dcaefe75ce9b0`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:fcd74b1122a78f38941aac24e98412a3c60225d7c351aa383651d3632af8fb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67676913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8053a7cf2f0a6835bd493e840cfa717c0b20a139e03a14b39749a75e8e7c7da6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c77211f128141a673636e216cc4d5f3e6fa8674bc357847ff9eb04f1b427a2`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 11.5 MB (11500120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e587578fa6285bc49b36daeed4fa6c88fc37fb4c9e75f0fc67ceb57495b4f223`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282d3333d81cb4ad90ea1458f97a73a58b780683b18204825ed5e7ed457efa`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5fa6aee575f2dd024b3e4d2792dc08580763adb69fa8f7ff39380585d9dd4f`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 100.6 KB (100635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7547f244373eefa4aa1f16d59e722f06a5d7d6465966dbfee113d03bd019446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e67b4e71e1ea5cb009225bb500ed01fb2710613c394548c4a620d11dd208708`

```dockerfile
```

-	Layers:
	-	`sha256:3da418a9915b7fdac6c23aff7728473a3d24a8dcdf0ae64515ea57c160a5a113`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 4.2 MB (4220164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab295110c910721b348bcfb4aef1dd38b7f2520b28cedfb80c870d2460c72d2`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json
