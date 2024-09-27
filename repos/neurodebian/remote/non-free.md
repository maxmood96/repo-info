## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:4c31540c4a47420fa5e9600cc5da4d3453175aa5a25a37860129f18bb5876da6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b48d6272400457ab71668d983cf66e3677f8df417b405a16646a77398ba08d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f348d52d0a30c0875589c2a9119a552d0157a52592558ed41ab0bfd3e3c77a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9051ff7592ebdf57081bea4813d054f179c10baf88e8edb1b1eb0503dc57a398`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 11.3 MB (11266587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7d938f0d1f711b7744833ba75d25ef22f306b38fed3f791d43c283332c29d`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d8d64e9f86a243cadef1fab89c4bc283c6ab4b4d7acd3c713da0063cfbc7f8`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45240937643905b587fa479f7122727e4da480a63dc938c4d4e680049d4fd520`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca5c0ab742bba3e582138550e8f5870657e878200808229861aaeff5b17eddd`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8be6a251f01d60f7c79d8354d52a880631b39d9b5e7686fa2e26ec2df80aeac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcc537a8cec282d091e002e6f0a1e677c36051a6c61478e3e8eb0454c94a884`

```dockerfile
```

-	Layers:
	-	`sha256:11250ff6b4c7bc963acdf419c612cf7ee613254e2246c5b3d2a533583138de69`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bdef147161d65fa6df17b8f42d4d1bc566bd2ca0efeceae14bea0caf771bed`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1bf2ad888a05ef807d67508a9f6926ad1786f54786c4acea708e393305d3e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f9c69de5373e2c9f69164910ff1d44257dc2596d2f0d7d3cfc67a0c584d68c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18398593d4c19c61fc775e0592d0d8a432ee6462e9a8f7b8810a361333b485d`  
		Last Modified: Fri, 27 Sep 2024 15:28:29 GMT  
		Size: 11.2 MB (11232110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621de790ca72d0c42672a6a2ac731249ca406772328f8c3edd3d594f1f53f616`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b740e3d498ccc528d88bab38ee97183e394cdd50200b197502891dfb79ad4d1`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5924f9901e2c8fcebcabc13a32cffd7e420213b1cf345f0e63ad1b70c157a`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c007be9f3baa091742dc1aebd0ae0a6e3cea7a4b810f0b8e43f15eb877896e70`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a5037ed0757501393c215f764e0ae006eb95c5b18a1b83e29856a21a86f904f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a21e19ca8c5ff905338308a88e40f5a3e1df607f032725531e296e5de2077dd`

```dockerfile
```

-	Layers:
	-	`sha256:b824964735f0d18f63657b8d91305ccedf77807feae3a5161f131d57be3295f5`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 3.9 MB (3924545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c864375c20088fe814094af1263b5d464fc676e095599494c207463caa2967`  
		Last Modified: Fri, 27 Sep 2024 15:28:51 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bee081949cf57ceaecb3135aafb92afa4570a49981637c3417a17b32403c4a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57394c8777f825902239d56e9004bd008fafe81bc34862a6a73b3642af4eb655`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ab7367486539cc2d6c35ad3018714f9ff4f1c097f65527882cda7ba2c4c48b`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 11.7 MB (11689049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47dd5e31a5ba70c7cbc3d81c9ac82a70b05d13aa142f333016a30c7c728d6fa`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a1687c24021dd12f46d38e9eefe255336343473332498d5da65afd4da1a80`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109102859cc8b950870f53e366f28846943d199769ba5a2dd573058136b2dfa4`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 93.2 KB (93204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d3b5d7d64269625fae11e5e669b00c675b3beec6db5b29738bc55b876f48a9`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8125292b6b7515ef1a26096899be0b264288a183078b74c5c9be5b43c677a730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c852d546e62718c86e124fd2031e53b49ffc7e18124bd0ea1aa2c86f1c2c99`

```dockerfile
```

-	Layers:
	-	`sha256:5c1069382d1d1988c0a11261be34df46f7f5c1a229c8c1b93d7cc8711f94f922`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 3.9 MB (3922209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724f78771fbec7e294d02422660c6c79e3db21f706773c18f10c9c77d42bb59b`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
