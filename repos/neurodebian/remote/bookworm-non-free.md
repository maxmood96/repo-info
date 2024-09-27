## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:de074c6477a033b628c052824d0419e3b0a90f13a2fb4073488b3c56fa7cfe59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:efbdeb8b5d814d3b0da4a167795648e3e251258aeec382a14937d4ed99826943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60913673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9576bbaf4ce331301262d1e6d4a9810bd99ef004b198a7126debd55b79b3c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1407873c66503c0a93617924a56b4dd8e307ce2f1c2584c89a9fa1fdb32af2e5`  
		Last Modified: Thu, 05 Sep 2024 12:36:08 GMT  
		Size: 11.2 MB (11232270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71660075504871b9d383826ce5d80aeeafa0f24ef0d028e8c70c2106e2f40295`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920d93d230ac89732db5e1368e9288d33ab00280170ed41ef415abb19e20b71`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80251e079aed2b00cf9612399cb10176c8e0143d29001b61c7468a9dfb9ce708`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367edb1c54966400c609652e755bfdb13b1f44403b415b6f36f5848b816ba7f6`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:900367b3a0829a3505f3df1874436aa29263efaaa70664454f5f91988cd4fb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c011ed8d1fce4e65e055582847acd29b56999057e60cb5495e989ee0817c7a6`

```dockerfile
```

-	Layers:
	-	`sha256:e570ced3443d64a24e17909c417b0370d5ee898bac3f1a6ea39f4a6086ccd8f1`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb42b2ae1c5cd926ed226f5811a5371c33caac652433e2252db8c9c75c3d08b4`  
		Last Modified: Thu, 05 Sep 2024 12:36:27 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1a4afcecebe4bef4caaf6087619df118f6c1c292e033583195fe045694d78fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62359183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dca3b4e9e7222f5e5153b36ebf4f2d7fa9753edac38b779988e74015695147`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
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
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3007322a25966cabf21ac5571de68c821d72acd5af0bab7e29cc49bd24fcf4e2`  
		Last Modified: Thu, 05 Sep 2024 00:09:57 GMT  
		Size: 11.7 MB (11688959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912cbec8e3e3b83e3b0ae68456830d139a8152ca87a74445b5b043d0a407752`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf715249f2d007d220402bfe1d271f2fb1f0a5a7a038325c8da0c0d76071f4c`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c7b649709ff95ab124a63a5e85dd2d68406f923eb64ea2c070ee8e90efff4b`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 93.2 KB (93199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c39ccb9d688897f6f2f421e68d389039bf4d1bd0374f30abbfe71cdff28518`  
		Last Modified: Thu, 05 Sep 2024 00:09:57 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ada24163b1b4d1e3f839b8115b1ed0645c68b9ea55e24ca934727e37e763e815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ab804dbd14fe55a29132e33f7fb879710fe7e02062c17b40e05b75229a1d2`

```dockerfile
```

-	Layers:
	-	`sha256:92daa7227caa0f20eb908642d3589981a329d915032fbb483a7516baf3d45921`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992d1d344f322d643c83815f60fa24f872e11058f6f463a541ec529076a1f76c`  
		Last Modified: Thu, 05 Sep 2024 00:09:56 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
