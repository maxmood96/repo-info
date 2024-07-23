## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:43f5c9c760ec3a6d80953769f7257365dcc98f921d3b3c1337ec0020432b17f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:06213ad735cb9a6dec843dd46a756e6b61a15922bf5c448f0afd3a59c6803ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59137682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959f881ab5a82c005d28359bf56c196d165f5b86c9d6578553f207513293437`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f76dce71e1cdaf2f5fbbd8321fb590faf24afaaf4a1e757a396ba83dc03427`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 6.2 MB (6223956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ef9a74a7171a057b6e8682fe8283d6c99f2e2795d1231f741add8be82d21f2`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a00bf503c4fa80a04227f2ed1c6dffcb56daf70572e1e4743abf42476c4d44`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d563d6355bc3eaf1edef92c45806cb76accd4674904436e2654218c5eb40a5fe`  
		Last Modified: Tue, 23 Jul 2024 07:14:56 GMT  
		Size: 90.1 KB (90111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee3021a05c47fd41365f8421cc847881c408b070780e17c45432ec1ed6f8249`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d761f467d9a341847f66b8b2f1033031bfb02af2db2c217c0f6cc074253e30c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acd0f860e0b9b1c93d7fe9bae5ffb7c454e2d1ac0dce37eca140e0f3bc1c717`

```dockerfile
```

-	Layers:
	-	`sha256:6e58ebed64a728619313a89cac46d38167884ac8c427705b67f3aa3d6a26aa91`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 3.6 MB (3560578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a7b1e282aa3abb11bda3c500a34f80575dd2a0db3198ccd4f136261b220252`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ae227e01cf2cf4676e0dad06a85f444edf7110c3308e37dca9ab2a8a0ef9b53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59339204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66aec19c986d35008e382bc76893b6503d2a27ce5bbfda0ec9285be568b9e2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ddcf50fbfd15049ddbcb10dc63259476763e98b097bffa8a32df909bad91f0`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 6.2 MB (6219715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3483aa0e91299a8856a36b0b796da1e56032f6bf6264a46bc561cc2396e5bb6`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a293bdf5fe3adfbdf9fc137d610631e39fb5217f0ae782744d49b0ecb810a71a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00033a80d29cf074dbb5224456ccd6939491504875f91ecc06de897b8c7e05c2`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 90.8 KB (90756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba27a9cd424832252c3bc77be2ceaf9ec1bfa8b7d89b6d274efafd9c44229fa`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a7a5d1d9aa5d38f7b816188f0bbb15d7b8afdddeb3c696a0cbd7475cb4fa9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8c10ab083598a842ccbc3dcb4c849e36d85315aec9293da11de467620a3c21`

```dockerfile
```

-	Layers:
	-	`sha256:2f0eb7be74e008400584761b42470fbf19c4facfec49d94fab3b40dd02da6921`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 3.6 MB (3561620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad58bd9e9493475fe159f6f233256b3f58f8f9bea08a050d53f7ba19cb479e5a`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b515e0fe0aa2ee64f2f6717bfc7f14e39916427324c828605ac1c54aa47ecbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60328513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687dbf3f13e8f713e239fb916d5bf5b193e2ac5a6901c46bc11ee7c7d8d804a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e24e2f4d3a2116efacc50f90bbb107706948c81dc9a0d5fe2ddcdd54751244`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 6.6 MB (6554835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9da4a0f05951e430e555d94186fdbe3cbe71c5ddee0192d4561e6819b593ae1`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cbcd981bac49fe2c027662d6e6abd44f42fcf467e76250be3030a7b0661073`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94e30e865fcd72a4d1fc4ba4efecba64573c63dc4e4783c2b3595e28d6fafa`  
		Last Modified: Tue, 23 Jul 2024 06:16:25 GMT  
		Size: 90.0 KB (90019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacdc2bb43e1590673d770ada6aa1acc80a042cdf346ba2cdafdedde940d7984`  
		Last Modified: Tue, 23 Jul 2024 06:16:25 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:26fd30457b2ed02bedb0ea1dda2b4dcf2241fdeee25266e834fd89e44207228c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ee93264ade3b9c117f66523d30697b1a90cd364bb14f33f78236dc70a7bfd`

```dockerfile
```

-	Layers:
	-	`sha256:0f2c2bde88471d36a43b3754cebf04d9bcc4b9d8a92de54dfcefa4fe969a1fcd`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 3.6 MB (3557671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050ed7c66b436ec6430ef1671e8ffc4626cddabb29ae26a072df54302fdaaa1b`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json
