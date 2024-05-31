## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:2acf35bd650b76a8a9ef703692ad285f74d89661d86749c99027a06356f3f5f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:9d6b76d38812539161f59c893466f5b49a8fd9591f8d2f2a01015142b1b7b216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60049164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e6ae8e755fa691be543e87a19ceaaf5730a42a8b17045af0d7844f85e3ea4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b719a38bf4aed68db29b56d561e793f8400c5edee1406cefdc25ea0c72ae7`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 7.3 MB (7313247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a778cadd45e115aab99728a495443d9a0e22db2b4cac341924a9d85071fb5`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73059de92601721fef9ac2c3019771fb96130f0ef7280cc538253280cdf1ba92`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c97c37c295b1b834c6ff803661093e3f42e5e01f6c8a476778c58cfb56657`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 91.0 KB (91039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:388a04f898471e845839e7d41f20795d49ce13fa7087377c1fcd80379d946168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de95620c07d5b4bd87bc12d9b2921d0d89a03b37227a84549003b96bd538f2c2`

```dockerfile
```

-	Layers:
	-	`sha256:a4daf7efa1f24d0026d214c5a47303591dc8a26d4667e0022b33447e0bcbb444`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 3.6 MB (3592159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca62554e92aa67d490ef6f1f7c63bcff795065618587426f22dc4754279c1ab`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 13.3 KB (13348 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5351af710581785e6f2098e3fda2a47d25fb0c14f95cd79fc7d70712d30c576e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65423858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2266100b38d8fe22c80c1af34961ed0354233c8c558eb4e5c86dc454b139c961`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:41 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Tue, 14 May 2024 00:40:42 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:16:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:16:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 14 May 2024 03:16:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 14 May 2024 03:16:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d28a39104fd5e32ed412e20d214a05f37a1a4ec16fb97a9a449a83e52258347`  
		Last Modified: Tue, 14 May 2024 03:17:55 GMT  
		Size: 12.2 MB (12203403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e345603e50bdc3be68723503e6942f8482e09b422addd688b37650872fd3d672`  
		Last Modified: Tue, 14 May 2024 03:17:54 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d4647eb3dc1619353f3cc8078aae3ebf270c3f47cb280e016725bd6fda0aa`  
		Last Modified: Tue, 14 May 2024 03:17:54 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c81171b646346b09db33a14c3712df0f0f1ed3e82d9c5186dbf349c927fa9d`  
		Last Modified: Tue, 14 May 2024 03:17:54 GMT  
		Size: 288.2 KB (288160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:6031d8e278a2353e1ea2d9a02ba56013189f78249299cab505eaf9feabf462e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61372571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6188e83e369fa79904c438cc4de65d30e027b1888d7eeb3640d5700d3e8e98a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7eb6b079b0eae2716a306dfd153c88de0766961cbb0cbc2499648abc3b7bb7d in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:241b052c0f57772eb9a56c460c88c133545f781291832042a8e20e0fd5b01591`  
		Last Modified: Tue, 14 May 2024 00:54:59 GMT  
		Size: 53.5 MB (53539918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961763936f39c9f3e6fc3712833553304ecbd59129d921d498e0f39df3a28f7e`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 7.7 MB (7739692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a296211e674cb7d41f502c0528b2553ce0e827cee604b2abbf1aab7b236829e`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d437e53f6c88aa2bd8a128238d49ffaebc152071e70ee972cb11c32296bd7ae`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02fc2d74e732bbddb781f2e95969b6de034cba4921adc2e2429faa9b72456b2`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 91.0 KB (90978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ec5fd0d53dd3b1b59710d496cf1feb1885226c6ec0546a47478f163ecc98528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44791e1c1de742df730d910f0ecc265c191681f772403d0a6ac269e015bfefe`

```dockerfile
```

-	Layers:
	-	`sha256:319c69159993f38862571140615edd5aee9496642761180fbc751cf5dfdc3435`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 3.6 MB (3589255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5eed4bfc1f8c66851679ae6e753c89de4fb38ec1e52d63400943e7a131a56a`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 13.3 KB (13323 bytes)  
		MIME: application/vnd.in-toto+json
