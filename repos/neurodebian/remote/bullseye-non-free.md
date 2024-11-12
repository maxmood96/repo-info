## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:4635579678b7a1c8370750e02c1e1a0356c4363152f3081dc13f61e462b34f42
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
$ docker pull neurodebian@sha256:02ce659bb167d59ab6ef1ce34e2ead94bdedf4d7d2033b0ff5abc0609d5965b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66317451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b02b0048fe7520afec08f7397d6ef93116f8d8185d2672bd0f86b8080801ee1`
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
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a37c6f541b5475a2edf1197b5c614e880e7198985a1b8ec0dea4b56d54df03`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 11.1 MB (11105106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c59917fd0abe12cd41ae981ceab5136df3b29e5524b77b56926cff5e7f2541`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c80ba689189a2ba5d02ff74c1ad6e9336099fe96cc77aa1f3edcdcde5b80310`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4f0dce01bd7f03f165e2a75abc50ba124834a23c6696acdc4c61062248dd6e`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 101.2 KB (101220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035b33d71c46650a25383fa983d31ee778f4369a986b057470f3f322c4cc4fe`  
		Last Modified: Tue, 12 Nov 2024 02:14:32 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0d7cafa1afbcc1c9daf9c5c396252a234ecebdf09a5aa8e65a391f0864429941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4254675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7eb0681a44503368077354fb1b000d8e000ffd8e2db6d9a37dae5837064b1d`

```dockerfile
```

-	Layers:
	-	`sha256:5029676a85e8ae6250c676c64cc90541923b66cba1bb3f9f266169b008bb4b3f`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 4.2 MB (4238954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6172bf8268b5a35eb36e648113a11d9b8a66cc27cbbacef84cc0e055c70a7b95`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:53e5c26be17fcd310af32bab934f727db59bf5b3131fe78781f3be135109ba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64944206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bac3ee2359939f8df6987de2ed95c70bc7bc1d87ec943680aa265ea423bbfec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa186315adacfb2b622451de8307f55c83bf74e5926cf7a13b2237e95e062145`  
		Last Modified: Thu, 17 Oct 2024 13:29:04 GMT  
		Size: 11.1 MB (11105848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3aef7bb5d567bc9ddb61f3ff5d2dea7cc2918d39c69a5122c9002662c4b91f`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb3afca1c9a390e8851a572c7497b59366792c63250de9dece52aaad7385c8e`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74a69755a92c3826c34c23ebbacc2bafd74218d37c26d56b22f2f565ea404a5`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934ef0ee7079660d2db15b0ffa13238f756f54d444d1dabe4f9db4f30d5d54ba`  
		Last Modified: Thu, 17 Oct 2024 13:29:24 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ab1d82d946c58360e2a6630d5c49be18c5a6981f9a5108baf8fe490452c452a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52106933ff117a899e05fe9719b2e92d354c61337b5a5f6ea69b3541cf7f5d2`

```dockerfile
```

-	Layers:
	-	`sha256:0543bbddbed63383d3185028800ff399d5985db6b29fd7101ded92416736ff7d`  
		Last Modified: Thu, 17 Oct 2024 13:29:24 GMT  
		Size: 4.2 MB (4223484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2932345dfaa0b574d9ec1414274647c8018eb268c34963c5f709c7ab15a939`  
		Last Modified: Thu, 17 Oct 2024 13:29:24 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1d8853f7410229e33e0e1eb7d3c0f1c986d0956ac3667a4a00eee8502222ff88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67697344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506288179711128f76d5ddde51c19b0683b5e131733e5b78349c66e17b7e7eed`
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
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ae5e516fa02820da75a950a2294dc25d67da99c33d679ded811ab6c0d6089`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 11.5 MB (11500245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ff72eea72a6cd65b46ea3111a4a99ddfc564018dc4244298d84496d5c8b8ca`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d85b7909226fa80dcb04b965a3dffa806c46cb25fdf24c12ef6747b428cc641`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3532548a28e972d50b8e915b968250f536debd39f6faa3e4b28fb6d723f7639c`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 101.1 KB (101069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1b1adbd380455d0c77a203b2d2c09f432ef2a8a02241618dd006ccb95ba4e4`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:212079c516e0addb2743f2e8cc567cd40f8ffc7839b61ff48aae727858c94332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb6915bfe6b29bfd22f1abaa95f7e7e993a81dfb7bdabe9c3c8979f76ee9cf8`

```dockerfile
```

-	Layers:
	-	`sha256:a0bf5352d1cc80c064869854eaa71c8fff6141f9aab0ed63b2fd723a22d6c8a6`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 4.2 MB (4235414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f521ec6a86a2bb91bc017f685c79a6ed5e6ec6eae3ac01da89c7a1bc8c0546`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 15.7 KB (15691 bytes)  
		MIME: application/vnd.in-toto+json
