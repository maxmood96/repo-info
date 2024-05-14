## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:945b94c9d78ff74efc88bade7ad7941a75bac0007216c82c4bb6d98e597ab988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b3ae4cecce765fb1e419ef28e56adbe542743625480bed78a6f59471004cb855
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66720993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cbced98ae2907bea19c536757d93411ece53976a1629f42df91b5baa50d1f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1e91b07476303f0df1d91a281a88d25601bd2e270c89eada4f0a40f47cd016`  
		Last Modified: Wed, 24 Apr 2024 08:10:01 GMT  
		Size: 11.3 MB (11311794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ed8addc19673e7db759b603705158858544e48a0633620d36ed72c1a0f660e`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd8f59553b16ae226f38ac9ad6b65a6de4ff383235d7dbc12b0bbb5e666e8b1`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d893ba87248b35bffa80dc173f73c1fe372a44783a50068d07f0697be088544`  
		Last Modified: Wed, 24 Apr 2024 08:10:00 GMT  
		Size: 308.0 KB (307954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8269bbc6aa8eea32220fd696f924348d95431a0f432cff2d9c00f3748988b164`  
		Last Modified: Wed, 24 Apr 2024 08:10:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b8ce5dbb664dce1f56363f6b83b4a1976383ad0c34da0d8614af4c3a9d53c575
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65363803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b7159593c55cd9beb5394aa1d4d97239c292a286413e4e239e8bd32a25f81b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca2bcd39cf5a2b8b48bdaac84d8842b5380e0a907ce3f8f79cab17b27a70166`  
		Last Modified: Wed, 24 Apr 2024 04:42:38 GMT  
		Size: 11.3 MB (11313653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445edd25d85483a6153c578a3e8ff8227295525f1f75a1cdf08672f00c757cdf`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23aaa128078e4f96e2f05c9cc17f9aa9e8ee0e3163079a3722a4973a7eadc6d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38430cee7648b905421766aa5de823c46e1959d12f10cd2d1ff78b276509f66d`  
		Last Modified: Wed, 24 Apr 2024 04:42:37 GMT  
		Size: 307.8 KB (307820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9717652fb5e910c228b0dae069d356eb298967cc6440b73745668a420aa2e2a`  
		Last Modified: Wed, 24 Apr 2024 04:42:47 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:28e3f5f42f6bec1bb12a48c70ed8d596b5094fd8c27f441d2d5f5951a2f87793
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68094932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619b6ddada1a5b7f8048024b9fca5df0e5f0f96956c19c5e19be230ef6a2a748`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:22 GMT
ADD file:052f086288480e72435d634b2bf07198eb86bd50d8625c576e50f1c86e39f537 in / 
# Tue, 14 May 2024 00:47:23 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:14:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:14:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 14 May 2024 01:14:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 14 May 2024 01:14:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:14:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:e2ec811b59a6f77ebbb7b1faa7ee83a70e39a8f7628970c01799c727a412a1ca`  
		Last Modified: Tue, 14 May 2024 00:52:20 GMT  
		Size: 56.1 MB (56076057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d58d8f04f6ec3eefdcac30a9a2b8dd157fee1257bee6df4a8a991fdacf09647`  
		Last Modified: Tue, 14 May 2024 01:15:49 GMT  
		Size: 11.7 MB (11708719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873fbc9863e3b959f22b6757e3dceb5da3b76121544a9213abf9e70e7d1a1110`  
		Last Modified: Tue, 14 May 2024 01:15:47 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c6fe230c342d7afcc3acb368763ca675f963d51744171d5e24dcbf3737fe35`  
		Last Modified: Tue, 14 May 2024 01:15:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93bd773a0e7151c80f19f6cfd68cb451d9e7344f66cbd159030dffbac1237d9`  
		Last Modified: Tue, 14 May 2024 01:15:48 GMT  
		Size: 307.8 KB (307786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb701edb2229ac4687cfab354e1a987493951a910ceda750788000d03244509d`  
		Last Modified: Tue, 14 May 2024 01:16:00 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
