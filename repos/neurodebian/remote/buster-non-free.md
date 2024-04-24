## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:8e8485874ecbbc8de1559bf6586ef0192930848c912b5c06464d84a8545e299d
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
$ docker pull neurodebian@sha256:9413a158fa9d3ff82dc865d640f2959d2a22ce946d43db5a6aaf5c32273d7a8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62589880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9eaf0b09a7df95fe5824c2b01d8a917a2f2b3ed9ffae9cd8e359695e11d1af2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:31 GMT
ADD file:5f943bcdbbb65accdf0b3bc452a1d4fafd2c64a9c6f6b3010b2a7ca20bedef36 in / 
# Wed, 24 Apr 2024 03:39:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 16:50:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 16:50:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 16:50:58 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 16:51:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 16:51:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:a3113a911224f7223aa235bbc20dff34c7d1419374b2180cf17ec274239d63d4`  
		Last Modified: Wed, 24 Apr 2024 03:44:44 GMT  
		Size: 51.4 MB (51420054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7e61ffccd36c3a9540801faf4aba761331357d2a9b66806a21f118ae1aba63`  
		Last Modified: Wed, 24 Apr 2024 16:52:45 GMT  
		Size: 10.9 MB (10868230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab4770a86a949c1f963e0818b1a04d677c1cd1029105c09dec9dde6b7293b3`  
		Last Modified: Wed, 24 Apr 2024 16:52:43 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14118cdf032dad8c1130b7501d85ab3d576a6996d00903d01760b3fe959be12`  
		Last Modified: Wed, 24 Apr 2024 16:52:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e85f4fa48637765c7e42f87e562355763d4d92fefd6dad757c34dc46029892`  
		Last Modified: Wed, 24 Apr 2024 16:52:43 GMT  
		Size: 299.2 KB (299222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99c76ce91f0d58aae77290f0bf80b33e07a0e72b2e5cd70ea3338e4bd3f68be`  
		Last Modified: Wed, 24 Apr 2024 16:52:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
