## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:671aebf4b5441b626f248d33d6000831bac3229c6b1da9adf42dbfc20177e97c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:02341e7bf46103f4577ef0e2d745f58d05ae7bb047112c648ec906a889f1ca2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5725464d7419d0cbb29281a4b025c7edc770b315b07e2ab05bfa3cb835841155`
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
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce556cde727d333e73847bbca3d36e434dfca710f1a863ee0439ab136253bf3`  
		Last Modified: Tue, 12 Nov 2024 02:39:28 GMT  
		Size: 6.3 MB (6309051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876190866705e261719a491e7f19b8aab0e39abad8ec417f1480956bd157bcc4`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c713715bdac20ad3f35c0c1187975b28de614033b14c0f83e294aa738eefc15`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e22ee5b8424b9b34d19b1a8282f540e71fe0c07b5d3e25e5263c3d62980313`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 91.4 KB (91428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8dd30245382f3d326108491d8c69fec58237345376554ebbc013cd05fe00c04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f08055e6c70bd7f3696bfdd302af032ff300de65230935ed0088fec46bf3bf`

```dockerfile
```

-	Layers:
	-	`sha256:554a9c326bb4d05222499547a3867292da16c8ae1ba2a279279cb1a564f974d8`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 3.6 MB (3566698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0fc255b6b0f15440f238e312105fdf72dbb54ab3cd63108a000ad188fa088eb`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9a863cbdfe04b91a740c54eeae31e5b9f35ab8716b8bdb46c0bf8b7aefbc62e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60142419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c186ca488265cebb588dfcd888c6005590ebebc506eb3f87ab8d396ffabf753`
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
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3316ef29e88ef66b287f756afc754e9a91d063e4a929cc02b22ab796e4e934`  
		Last Modified: Tue, 12 Nov 2024 13:34:26 GMT  
		Size: 6.3 MB (6288501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3bc0e8335a41c803791dd9651d0311bde3d580b261d8a93b0d2f1416926347`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a48a1f73dd1e3427a91a00259b5902db95632d4bdde9a9c716599a82aaf95`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a65fde09dca43100cea07b77b49479f81cbd872ee34bb95d8182df9b774ef63`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 92.2 KB (92191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd884045b322d450ab4a2830c115c78807eec2535170a42aeb0b1d9106b50c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43849ccb04e72ca000c433e3d0a58825ee093366ed8503f1085948b56a4097d5`

```dockerfile
```

-	Layers:
	-	`sha256:b1b4f3ff58c64efa2ed2dba778ae3ef6087651d32805951af58a4e828aaaa47f`  
		Last Modified: Tue, 12 Nov 2024 13:34:26 GMT  
		Size: 3.6 MB (3572216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7c3c393176545af7583e84316b3211197c14053c26333b28edd1f4a769d141`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 13.8 KB (13752 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:8b53b7402bba2ecb131156dc19c095fa66b390c3e0543ba59bc34a2cf7628808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60921682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855f8cd464ac928372c09088f3336af43660b41eab691ba6369c7efc9a683b0a`
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
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a37078e7ce7126f34e971c8ebed2d9cd9e8ca7917e038a57cbf35f9aab06538`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 6.6 MB (6636005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4828555fa65d9b69815653e52d20d2148dabbc62c748edbecee8d58f2c468da7`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb3886367217864504c880e1e2576ab2ef75119eabeca72c6a29719a2b1af47`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04aafacf598e2fdf002ab8f6b212b056da94e49cc7e813a12c6db9710dfc037`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 91.6 KB (91649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4529d7359a60db5677161dfdac0eaaa2b16f04e52f36f1de8a9c06828760248e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc10daa577d6f41b82fb0a72c8adc673319b83887670bedad3d7f60f049d066`

```dockerfile
```

-	Layers:
	-	`sha256:8452ffb7e51105f9857d885c835b57c39d6ad8ddbf501edb1554680e707ccf1f`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 3.6 MB (3563934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f190e9516f9bca8b481a2ae742f3b3f5ec684d606f53be1fd37fba9ebd0ed36b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 13.6 KB (13599 bytes)  
		MIME: application/vnd.in-toto+json
