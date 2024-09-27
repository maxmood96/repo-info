## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:1d4be1129dc978e893ca7f1f912b58d26e066836afa98da72b6b6c77f9e09952
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

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

### `neurodebian:nd110-non-free` - unknown; unknown

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

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

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

### `neurodebian:nd110-non-free` - unknown; unknown

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

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7616dceee5aefc521c248668cfe4a6ee06908cd2c688bde93d4e1c62fe1d90d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c8fa70d35b466b7488d6a8bbee5796d005eb095ecd6343839a909543ae790`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
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
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b13fceaf30837919c83ba0eaff4811346a54e9111e8609afa66847dddc498f`  
		Last Modified: Thu, 05 Sep 2024 00:07:30 GMT  
		Size: 11.5 MB (11500195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94822419f2eee106212fd1cfb61f612f5cbb4de0cff53b8b4346661dbd7d6dcf`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72cd6ea7780d9eb88dcbf6a60de043343c71c84b38a3fd593f7c4443e9841eb`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d79df17eae45ea840c3dd3047ee6d29f0238a4f93a9e4e5dfa6bb97776be06`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 101.1 KB (101052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfec050c8598da5da9fa965646f462272eb9bdfa7a27114a560c38e4aa697d3`  
		Last Modified: Thu, 05 Sep 2024 00:07:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f459330823492f170624e082686abd94b19b9855ca680cbc804070ed438cdbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a5abdbadfd2154a3bb12d0bfcaa4d4a86ff75310e4b6c11de2c608942a4f94`

```dockerfile
```

-	Layers:
	-	`sha256:9fe7cc4755190f18ca56b92e4c52d4545aa9e9a4a32a2c49d2ddda1dca821a47`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 4.2 MB (4220200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45de231496ead48cb3e03380acd101ff2b3b7fb3eec01e567cbe03aefdda1d3`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json
