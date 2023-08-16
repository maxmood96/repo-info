## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:26858837455717ccc343466334900923140e3e516132dd65fbc9e4db5c6ea17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:1abd2e1a3efc31c1d4a28c94d69ee07797e433f7e60a93119ffb9e9140672844
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64168717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aed6491eea8d1c1077623c4d8e1aa506e169aa01fa3bd38502677c90ad14dc6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:01:27 GMT
ADD file:48c88afb2094d5db855a4fe872b2cbb76a9d3c1b143c67463318da89ff28ed91 in / 
# Wed, 16 Aug 2023 01:01:27 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:14:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:14:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c111fea192ed7adbc203c571a96a882a3741644731e862353e7c2f3259608f77`  
		Last Modified: Wed, 16 Aug 2023 01:07:20 GMT  
		Size: 49.6 MB (49617313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a1753a4167c634c5010550a1f4f417b282f2e72009c2a83a24d3d670c294ad`  
		Last Modified: Wed, 16 Aug 2023 10:16:07 GMT  
		Size: 14.3 MB (14264309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed6425f36a7f840361853d24139d567df7ebcdf25533add46ae9b71a1b58899`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffee644b7121bfa1a75452287f0ec6760aca7d2443b5b40ab08d661983c822`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d34f1a1b9fad277ce6fab6fb5714ff0e477efdacb71481b1a19571270f5c72`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 285.1 KB (285086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:246c4c73759d44ead4c3dfd373311b79df3a25a2dbe53f4c1a2213fe3808763c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63890308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578bda0b0f3ca70f20c661d6af97b9d167a5523ff67cf5fe386467ac94f3cc80`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:01 GMT
ADD file:8064072457ccf7b4072e08095fa84f96b0fe3387ec8f302afde022186aa3eab5 in / 
# Tue, 15 Aug 2023 23:41:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:51:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:51:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:51:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:51:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4513653e4d749342b34f60c592adaf0ef4af993e76a913a1c086a4229a0e3afe`  
		Last Modified: Tue, 15 Aug 2023 23:45:54 GMT  
		Size: 49.5 MB (49531730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce812d7af41ad795cf945688ee3fc47de3e52c7d41f9096865b42621b207cd11`  
		Last Modified: Wed, 16 Aug 2023 03:53:14 GMT  
		Size: 14.1 MB (14070959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd452a3a5eb5d5aa0bca4af1ec0aac980e7024c2886cf99489c75ffb8812530`  
		Last Modified: Wed, 16 Aug 2023 03:53:12 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145fd67a5c34a7ec4d6b4fae9664abcb6c8022c8819ede55397b8fd285ed35cf`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c32c90e7cd03d64125341b0f6c1fe0d8b720900a58bda65b7dc130b02ae1c4b`  
		Last Modified: Wed, 16 Aug 2023 03:53:13 GMT  
		Size: 285.6 KB (285607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:8c02d9e2b2428d501c06b75f1b296231a48040fc4ce123472d2fad97d8ad6574
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65590266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f522dc2f4c7a47c6c5d24ec3af0d697e00ef975d898004c45c535ff685ddbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:34 GMT
ADD file:d86f66385d3993c597ac040a976cd8a826b097d014cc4f3b69d8ebfaa5aa6eff in / 
# Tue, 15 Aug 2023 23:40:35 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:42:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:42:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:42:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e41394c7daa90fb4aae0f67d43af5ee9838fb125e249fc0002bfdc3b90bb6c05`  
		Last Modified: Tue, 15 Aug 2023 23:46:33 GMT  
		Size: 50.6 MB (50631355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b86fa75275b3360f0cabc05723d0926928e895a32997b0045ad1a4b87c6d7a`  
		Last Modified: Wed, 16 Aug 2023 03:43:39 GMT  
		Size: 14.7 MB (14671551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31ed6d29a83b27add317575ac2bad9081baaa869afd0edad2f462982c52e652`  
		Last Modified: Wed, 16 Aug 2023 03:43:36 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94acc54b4e308d89fb245806d56517510569b98017639228cbf03c46350a9a2a`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda7bfdd1b15918713a3b6dec980d78af341813470a5ae7d6b3fb016ea4410e`  
		Last Modified: Wed, 16 Aug 2023 03:43:37 GMT  
		Size: 285.4 KB (285352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
