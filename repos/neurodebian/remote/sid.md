## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:5e8568c26e57ea5d8058a61e446abbb293ecd47bd0c2680448f296b352b1d2c8
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
$ docker pull neurodebian@sha256:fceb7880ecff05e3fad1bd34562c0fee903764280c693fc06edbbb6b5093843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59996796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0c1c96bf04b236a96d091b001f637f30fc4267568e19ad379ebe0583a99ec6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
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
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c4d641255ff6bd7b8ce630c8cf947966d1ff05bdf86f951c687f989e2f5e9`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 6.3 MB (6273546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c25f32db1b1126487143c75b9ce0d496e410c5bae14e76068c7767c3979041`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1aa1fca4ed404a2dafbd083628f990869ee0dd7b253df1199afbf67da6e338`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4cc25b7109f5af55ff37456e9f7fe94f979dff175b36667bc066bff22439`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 91.8 KB (91781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f7c49f91f70d5fd7fdfb393e1255d65bf3963462449605a6b498c5dd601a397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c771ab1f610171f7a17f00660c97e22c04d5fa10ecb778aeed2a621ae3e94e5b`

```dockerfile
```

-	Layers:
	-	`sha256:5e03f04196d30611ce1df27f1d3cc5278240cd13a3eab0cd469eb97f145011bd`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 3.5 MB (3530885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9935b092fb7d33339c675b1c15bbf6ecc7bdb04d95950c01ed5fca038b5e8b`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 13.6 KB (13553 bytes)  
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
