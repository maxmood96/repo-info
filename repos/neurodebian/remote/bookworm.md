## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:aacfdbb5899916ce6aff133d995785d867b2697513f51930626919df8816b52c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:dc1103341f4ea2f25e0d9bd456c9a29d1ce3c89fc9fdf03ef9855b40020ce2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60937609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae651fbb06567e9d58779eb005a0d338e9fd6c3e9e2f94f104bc7cf56cf2d8e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f92fba1f2243260f740882b33bd65ce9be7c710ee5ab93f9c7b65c5657cfab`  
		Last Modified: Tue, 12 Nov 2024 02:14:48 GMT  
		Size: 11.3 MB (11266780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0dcde979a959198da9acd3e0363652603c29070808043e0f715abacc4cab3d`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca047e2ff6934fd61ea0fdd2bcfe2eb8c113d771ddf33cd7d69c8e029508bb`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9bc304a1bc3fe8ff0d4ba75eaa7938ce3de3002a43c18a34cbd5f436180128`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 93.1 KB (93143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fd1d034fa70625003727fedc26cc6409115c5ddcef4a034a2b4763cb77ecf1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb574390b66288dc89d92f025f7fbe7bdc29e2f6dfef2aca5cf5b04ed2269f5d`

```dockerfile
```

-	Layers:
	-	`sha256:716b9d855b2d05a308e0a2415f3fc35b67cac1d7d59a739292f73c7c76e4e054`  
		Last Modified: Tue, 12 Nov 2024 02:14:48 GMT  
		Size: 3.9 MB (3938479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b957b5cd62d235b91fff8c8a270d1fb78b3627590548e5fee46f029a6b756fa1`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 14.0 KB (13999 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f36fdde405355c0bf1aa5e1d801e1ac091b9a13b79b5fdc64c67386e08c0e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971276f59476fb7abd2a062acfe28a943c1358d6e56974be08536e68e600e96f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374b4f322cd89941e3a79c9bd26d1a5f1c6bc1cbada76ddcd1dc30f5e5cdba3`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 11.2 MB (11232560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c07a4424e486742d8557f51e2d6ea83c25c81a3fe1083cdc92f2aaabe53972`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76a820ff7756abf0046ae961df3ad5d2f997f1277bdb445d4f9ce1e548f3cc`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89406019c22729ee9e55b00384b15954a2694a0806199b7273eb34553edfd429`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:195fe9b7df249422f67b240aa86b08c2bf8393248857a29dc39df933cd31a46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdf531367dece30285e6b03802b5dee15e61557eb51ef949d9d3d1fcaef099a`

```dockerfile
```

-	Layers:
	-	`sha256:d432ab8fb3e5457fa892a9a9d8693b0ebe28adbc5fa2a5dcd064d8d3244e1ff6`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 3.9 MB (3938732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475ed9a1ab4f5e86469908636c4524eadd55ea92f90cb3e7584a8c8bc22d5e85`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:4c58317ed937fc30fdccbfd6e609c1810573b9052f6937bea93c95eacf668e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436d8bc3e03a379a8d2b25a3b9fbeced8bdfc032e18b7bacf4ea206c9eed744e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cfb12e48f51f3be731070cc296a425d5d61dbb1fd547b84dfa0eadc63c471b`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 11.7 MB (11688927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b6e6861b0b6e94b6ba6dd87d46e8cf625779109eba1a6332bc56147d591897`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a4461e0d5e9d53b5bd20baaf7ce175126b90a0527a6d018f518ff1e8b492f5`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6a54db7525e753cb39845d57cb48831ef1d279a3b3314d566ef7df0cb9afea`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 93.2 KB (93209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3909c5a6bcd7ccb77cffd551f11881687911a606ce66ea956d9182ac8795e15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd98ee86105104e646e2c3de982967161ba4b0854f37f59dfab18b0f08a312`

```dockerfile
```

-	Layers:
	-	`sha256:d9d58fdc2e7d7ce479676d3a6b83a4d215bf5d795015bff631faabc74c8acc24`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 3.9 MB (3936396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b0af7d2d2c98366f72972bf6bdf848dcde29818c43ba6666476d0b655fe602`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
