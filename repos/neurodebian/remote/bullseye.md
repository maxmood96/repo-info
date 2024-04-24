## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:61ca3436311957f3ae8a1b021f1a75c4bb52e7a2cf6d7b44f8f56172cf316d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:2320f4fdbffba27f42e311af32288d59b2bfa7b132c7aa9b1feb20779a5373d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66720632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78901287c3396aa5f431afc9e8cf59f5737377a719f5ba1f7d5b47bf3a28c6b`
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

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c3aa55f66293a278b78670a2f2f2d792b19de4177447661cb34602064c86f80e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65363442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7434120237e5c825cea47d3e2542d57b598fefb9c6375f9dfe7948806ee4dbb`
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

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:2a2853ca0a3dfe6921cb72f70109ecc2134abde3493249ef342a5dd82f380ed4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68094954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406b780264189ae1f06695d439076b5028d088a07a467d76bd280f5f495bfb45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:08 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
# Wed, 24 Apr 2024 03:39:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 16:51:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 16:51:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 16:51:23 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 16:51:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:531ff4ee4f75fb0b1990fd185259fbec17670ebea9c3011de30a27e2de08c387`  
		Last Modified: Wed, 24 Apr 2024 03:43:58 GMT  
		Size: 56.1 MB (56076550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5cf2cd1da11a694331a5b5396aef4b857870e4f8f879cbdd87776391f6a8f9`  
		Last Modified: Wed, 24 Apr 2024 16:53:03 GMT  
		Size: 11.7 MB (11708691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73612014291a31319ec1e9b05882f9d7e25f77e42c691312eb4fa77d9814d54`  
		Last Modified: Wed, 24 Apr 2024 16:53:01 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b013007687803dfd282c3465cf1bfc6de80d0db2164951763258b51d731966`  
		Last Modified: Wed, 24 Apr 2024 16:53:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032e58c918cb19530f41c6fadc523d507bd1262aaa8c9627a00a7d7776489a58`  
		Last Modified: Wed, 24 Apr 2024 16:53:02 GMT  
		Size: 307.7 KB (307700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
