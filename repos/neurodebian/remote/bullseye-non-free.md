## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:ab8eea31316733657f99c38f6bd74aef51b6c5d16456887b571eb4b95dd611d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7f5088398c7f011e8097a29cd701f675a1080cc500196391c4b6794022b8a9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdfcd7ff9d894bb20277f777c30089d05e6bee15278a392b84be6561a744ef7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781057eafc4c33d419ac01788ae0f4708e6c8b9b42b4c0efa58265084ba5c337`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11105021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9f0b8cb73e5762cef8aad324e1ee6e0a020348d975fcf9a1b709b4c3fe925`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297557466a2385d9af17a8e5e0acc6b5876c310f8717e40aa3661b00dcd1149`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0755dc4a01fa569e141b166f027a20446a1bbb2e769b0548ef4ddb92083bae`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 101.2 KB (101182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a4483fab3e6ba8071f141c5125469123ab6dcbd2c5b2d7d419005489a71053`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2af657dc55a7ddc9f14035295ebd2f147736d2fb0fab02638830682adf4479ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49ad2aa5db65dc48910c228539fe3ce366263eeafc62176ba3c49fa58b7e06`

```dockerfile
```

-	Layers:
	-	`sha256:1c2d01c9aa9c1e38c274b4f75b13960fb53e6223ec48d13adfc84fb8419989a8`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 4.2 MB (4223753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad25678c39510df32b23c842ca8358063f7fc4eb6fc0befe7ae6135f725771ce`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a9b51a2e80948cac7bbee59ea1e13ba5369969893b5d5ceb0521eb696dacb9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64940892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bee63eae38e75bc7be7dffba041e7ca7e73cae2c0e713811bc6551db1d40bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab2fdf0b58451a0c31951dc2a87a932deed77518e2a054bf1aeb38a5a7261e`  
		Last Modified: Thu, 05 Sep 2024 12:35:11 GMT  
		Size: 11.1 MB (11105823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3cce06e7960e8ba47689bbfb2de4f89c0f135a613080c0ecb2e1000bd16804`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23140bbd52963541dd8e0e8cda7d68393aea1804ac6bffb8fcec5940e65548c8`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1608e10ac25cd129bacc060a2fe424b11ed352acf6fbe6cf25636d78d881b`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bd040d3118a6dc2176423c1d31a87a6a1e1e7e868f44fcced1e796200e04d5`  
		Last Modified: Thu, 05 Sep 2024 12:35:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8fe5ebf423951de559c47fa6d007a391c4d6a39842255620507e7a89643d3464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf0a49183496dd812d4c35815772ca7d8afa88030bef74f8c5b130d4ea65bf9`

```dockerfile
```

-	Layers:
	-	`sha256:c742219d6395bd95d2f014a16537d41f6ec98d39481f7a8126835bd2d634a6ed`  
		Last Modified: Thu, 05 Sep 2024 12:35:33 GMT  
		Size: 4.2 MB (4223345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce31a0ef62db38cb1b6a25769b3a8466fed5b6b6aa09a6baac7c73f3cede77a7`  
		Last Modified: Thu, 05 Sep 2024 12:35:32 GMT  
		Size: 15.8 KB (15791 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a847974e93e911586570ee1d7e8f6254ae6933e4ff60a5a4eafc0a59e752e40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67680032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76250fa78ef11613685bfbfcd9362128fbf96968b7ef1346163d86c43dba7967`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef6e128fe253e9e92df878bdf6679d19c4c795a0ad5b4e2763d98dc38d52397`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 11.5 MB (11500106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ec30e15c8071ee1dd2c285d9e9180cbd765125f72712cde12b1e30609cd7d`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3df436804194d27d1205da4b1b5b92b11b5e9dd37789901d1bb7054b49941e`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec155c5566b8bfd54cb4ff20ed3df4ebe932bc0414cdb7a5a1686c9f2943d4c4`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 101.1 KB (101076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f013ea1ffa93929d5f3fc804f87adaa36164ab369bb17de0daf168773747c7e`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0b8a94eaa507d01e918eb51c1691cc17c03ac6f5f39042bdd87316f86c7f4526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f97f8b8941aa00985d47d71e1ca26088ec2cf233814c1fcca8257344690427`

```dockerfile
```

-	Layers:
	-	`sha256:c13ac2c7f8d63495afdaca68139efd3b9e9e5363a3043024ca9ad151326111ac`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 4.2 MB (4220213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44468e83d9ce5d88b4eb7b5dc138e35d4e8586e0dddd16c82cdd5f9c45b443fb`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json
