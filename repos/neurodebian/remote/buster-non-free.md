## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:bf3cde46f6ffd67697be6a34bbbdd48faed8a5aa27571d27bab2283ec404e1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:4b091c009dc24d7be992ee1c6109c8716479fdfe17d61066dfd4983b77acf165
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61463743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527f37e21fba42ac823635c60be1750c6c653a66270b196d848d525d58751e8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:41 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
# Wed, 24 Apr 2024 03:28:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:08:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:08:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:08:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:08:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:dbd6422b1b97494149e51bbd6c24d444b4a8794d2702d105efce98c44de9ad50`  
		Last Modified: Wed, 24 Apr 2024 03:33:41 GMT  
		Size: 50.7 MB (50657502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f5a97dfd108ff40ee8c22fb1b674c4b0fa71d4728a7c957f5ec3c7bf3f211f`  
		Last Modified: Wed, 24 Apr 2024 08:09:45 GMT  
		Size: 10.5 MB (10504543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc0aa6e5f908abc21bcc432f37a7616080de8f05aed4a053d5e4c2748186e3e`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d835973a558f188c0dea4ef504782eb743c56e14bef9e753f423a4a44bbab7`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355de9ffe679fe4300a0e38c273cd79b40a5912cbd8af4058d63704daff83b13`  
		Last Modified: Wed, 24 Apr 2024 08:09:44 GMT  
		Size: 299.3 KB (299325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d20dc516f901becb966e456841d1a6c9c9ca61dc07e02c333eff55b439fc1f`  
		Last Modified: Wed, 24 Apr 2024 08:09:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:88a242bbefe2114d7a0d414a1a87c65d47dd3778150637c354b8613a07eb24d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60265352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2471a63b1f2c98d58e22ead1ec9ebc131bc0dcf927a4a26d9c4676a3701a15d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:00 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Wed, 24 Apr 2024 04:11:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:40:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:40:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:40:52 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:40:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:38adae2f446d050038d7d914eddb5b4a481b4c3e73ec18c36be90c376b639389`  
		Last Modified: Wed, 24 Apr 2024 04:15:06 GMT  
		Size: 49.5 MB (49453161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecc8a5ac86b486903737291255556b77f7a90a8e214ec345d700fc1c8f18878`  
		Last Modified: Wed, 24 Apr 2024 04:42:21 GMT  
		Size: 10.5 MB (10510475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e0aabb024a919a3d450e2a440658372daba5388e7b50bddfd1365d0115436`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ea48749b49637a0ef75c50e94c555ac928984662b3635dfee7ca5f0b81a922`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e36e1e3c24b698699ab9452390385c45b992d86280ca886ae53e44fa113e7`  
		Last Modified: Wed, 24 Apr 2024 04:42:20 GMT  
		Size: 299.3 KB (299348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b7af1f9b164792dd8923f97b651ff98e17795691dde122adea7406e9c63aa2`  
		Last Modified: Wed, 24 Apr 2024 04:42:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f2f0471b3e94d8f0e05e2840a0963e8cee4c1c0642bd2511bd1e16f6e45749db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62589560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf11e7d4ae4d17dfefd2091a96bb730c51cad7f7db21d15a090be0a1a33a4308`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:45 GMT
ADD file:5e59addfe8663b7c16cce40874c2a3c8601e20e80f5a0897c86b64ba463c10e9 in / 
# Tue, 14 May 2024 00:47:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:13:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:13:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 14 May 2024 01:13:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 14 May 2024 01:13:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:13:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1a892f56e4b10aaecbb51b3219d90bd0d8a1e955acd0624a6ef27ed086ba168c`  
		Last Modified: Tue, 14 May 2024 00:53:06 GMT  
		Size: 51.4 MB (51419713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eeeb7e1f5d2d854116ced683d87ba05a9fcd7bea0379fa1d5bc8d72f37420b6`  
		Last Modified: Tue, 14 May 2024 01:15:30 GMT  
		Size: 10.9 MB (10868244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1b977801edea4f85e89dc6279dbd077c37384bceb7fcc32db74b12e7c65366`  
		Last Modified: Tue, 14 May 2024 01:15:27 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85155933dbc7889b8bdaccedbd3bcb0360219df1d4960651c345f9482d77710`  
		Last Modified: Tue, 14 May 2024 01:15:27 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc74a826708b2d5703930675cf211ba81773ce2c0a8b980cd41831a435ca0e`  
		Last Modified: Tue, 14 May 2024 01:15:27 GMT  
		Size: 299.2 KB (299239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4a9f186e2bef86c9fb221f3aebf899f2022c2ae5fbf22dfef558b932668db2`  
		Last Modified: Tue, 14 May 2024 01:15:38 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
