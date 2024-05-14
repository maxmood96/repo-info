## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:7bb82e9d0f9bfc9c68d22fc91cc0f11c4f431dfd50e0f676f8fdf865b19a5dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:8af16353c0e9c11925a2d06e84f94ee6622dd1311e0782cb31e5ef0ff06b1715
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61333615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18094a9b7cd4c5c88c1b8b234d5aa269e23a631cfac99a6b4c2f9e1b93082c60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97db8dc93c243437c267d9050d41579b2c1da9361a99099c87d1e73bce54f380`  
		Last Modified: Wed, 24 Apr 2024 08:10:21 GMT  
		Size: 11.5 MB (11465651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0289cdd63d0b79750c9280dcb3e17b718cccae3e27dc5e4bb33b22e348aef4`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53e5a3f047b2db762be2c81e3c782ad0484dd786c84dfc865e483ce7d6feed2`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5894ce1634f7ae09fa800521db0b96625dee18aaf578129cf1c85c4d3d71dd`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 289.7 KB (289668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:328530398d63ae3d3e39ec8963b2e6684137933d17e5ccd2a7a96852632e7ad6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61335273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b26e0fb52826d601a222c22d359229200170ea7d482d1593aa83d6d1d044921`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc25b7b4f0f0785407b52c5ab62c03c68b16d48dbff6f85628b50a8d5a783d0`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 11.4 MB (11429751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3e19eb2c60eedda2f4cf1976f0c806b310292a7d55e3b1ea15f8cf76d6ba2f`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759585282845c3252db14d8ddcc2c4e2bf59648949ad6c9625a6afad359e0120`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd085a612fc52502e17d38291e29478c6f400c15e4685dcc925cd3a9e8894833`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 290.2 KB (290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:6a51afa82ab0c052e69d885db70ac3a8368a28ab3b253281d7d5405c886d6e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62780077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e6e1667c550ef06eca261b79281578d44d66f175d901e1d5009ee8856e41ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:00 GMT
ADD file:35709674a3b845511a896af16ea37a6022e7d48992d3198d0760c0c3208fe4ed in / 
# Tue, 14 May 2024 00:47:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:14:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:14:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 14 May 2024 01:14:28 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 14 May 2024 01:14:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f2f2f6205661e555e772749ae7fd294fb04fc0d06cbc67a50a11fbb4ef44242`  
		Last Modified: Tue, 14 May 2024 00:51:31 GMT  
		Size: 50.6 MB (50602424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e487027e635539ab67aaa98b8147a776d54b38c10396a07556c92545a5179`  
		Last Modified: Tue, 14 May 2024 01:16:13 GMT  
		Size: 11.9 MB (11885733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b840e1c416ff89af4e81db9b3424660e204b7bd8c2d4206c8fcd84578b339115`  
		Last Modified: Tue, 14 May 2024 01:16:11 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d002b5c98cedd34cf1d0c972616acc15ecd00d8c8b822c8dec3251ed2fbb1ca3`  
		Last Modified: Tue, 14 May 2024 01:16:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6612fc8a4cfce25e19e1760b73eb7f0e894e29965af5948de0fc78a692f1a41e`  
		Last Modified: Tue, 14 May 2024 01:16:11 GMT  
		Size: 289.9 KB (289910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
