## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:03cbdb56368499523b423c42dfb04c2610566ef157caea89cb484b797d96f7da
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
$ docker pull neurodebian@sha256:d1a43d2f25278216c1a9659bfb7c6ec44c80ccd5066649eaf2b0433519242cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ed153cb8527c84eaed449a92f0a656eee5b7d536a5a321c3461a15b862b1ec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f0102900c339db81394076194f5cabc70fd1bd5249b9e279c4c3dff279fa9a`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 11.1 MB (11105025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27e37472add233bbd47e458c8da9afa77fa6eb3b050d84b6a2344733ed9194c`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef3beccf4e525ee8ecb4d8fadaa6b201ac1d55f2e74262d65ae213b3e54144`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64a8c95417d848f4815e9a7b48787a5276ccc3ec7ba73faa304a009fb1d875`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 101.2 KB (101189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fe45998b41628fa647072b6cd3f22a62e5b9e2905f597f1b0a6932f4c4ee7c`  
		Last Modified: Thu, 17 Oct 2024 01:14:15 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f2422cad8533344783d8b8e9380271e3e9e2d273ad283d1e9c0e4d3a70559869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8ba2c3e63c2a0c16de87d27e28cc4d76d86339bba0163ab49426816a18fcff`

```dockerfile
```

-	Layers:
	-	`sha256:889e8208d5f5df28cee3850569bed5963b2617fc3fafa41ac08273dede19fdf4`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 4.2 MB (4223879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd2f394dbcd432364bb73783b3681f40544b3f30d1673fed9ffcea8ff18b60a`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 15.6 KB (15550 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

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

### `neurodebian:nd110-non-free` - unknown; unknown

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

### `neurodebian:nd110-non-free` - linux; 386

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

### `neurodebian:nd110-non-free` - unknown; unknown

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
