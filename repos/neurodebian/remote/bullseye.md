## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:c6f386a31699b564a5e7e647419d49e8c9a5d8ff8fc6e83bf44b0c39c849c43d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:74fc96b02460550048711777d4aee359b9d01a9910c726876274e6bfd350d661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64956989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97b32b68c755a266a123b80f24780368f8dea2b3a1f6ac6188a3dec4df671d7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d7693a3bd08decf0ee034f8039bc16bc9fd521dd5db19ed701e183d704389`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 11.1 MB (11105084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d069ea1fb1f3ff59787f0ebb7111b602580aa38a86620c44a0cf24b8da6fe2`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0449a295cdbde22577c56e960271a6b9c63d85cf48c5b36b936aea44657e2f5b`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a264dd350eaddb6c5d16f8f69e14b10ecb8c43398066153a4defa90943598202`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 101.2 KB (101216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65521b7fac9e6793348f912e391f08944fff56db0c77d013c8e99aa3a0a87912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3184399104e7be94e5ebee6d2a88fdb28157e96bf1c1c0dbbf9d628b9de0f7`

```dockerfile
```

-	Layers:
	-	`sha256:8de8a61e2205b3e02d472f6563591743ad6b9c7b2966a5bfe2defdbee23493f9`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 4.2 MB (4234710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f47e7282dafc9f31a669196e043aa1e4c6bb8826b64d8144215bf7ee37d736`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:48e1e794979ba43786bb8fb56d8bd6e2bf3394e94a732509133fc62001c650a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4022d8d914d6d1259ca87ca2e7b9e74df756a74c4da42a3bd6efe907b713be`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3882a7dd0a14bea13a77df5b4c510fe24b4731e60a214c2419a057b09f823`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 11.1 MB (11106035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee718847ca2a78d990086602ec053fb4093415d671b15ba9596f39fa04bc679d`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76a051cd4309c8457edf6b80401a713d6d6fc6449b6443891af1c92d43911af`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70248da80d442a8395b2ec921fbe2e7bcff12b435112dcf248d689354adb71cd`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 101.1 KB (101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b96a5e17ebe207ff9ce4d0a48c7b05604100ccf9ca3bbe7639ff51c4e4bf8468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676d85dae5e7c03df0ef81fad818458b86beeb8d0ef43d8145c99e26903d0e35`

```dockerfile
```

-	Layers:
	-	`sha256:b2a9966658fca6a00227443fcefb6a1195cfc0413de2a2b8fd3ea1112a6eb615`  
		Last Modified: Tue, 18 Mar 2025 03:46:59 GMT  
		Size: 4.2 MB (4232403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3acd4e70a152bb8fe23396cb7a7d3bc616a6fea39169e3d61bf07c6697cfe5`  
		Last Modified: Tue, 18 Mar 2025 03:46:58 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:e7d98c86b376667da8554880ac322c30aa9cfa26b35052c10354aa90ac8b17c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e5552518c011902b1720cb8123841b125e7eba4b7da20beda8a2266b1d1463`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b5ae7d85bf65d375a5f6dc6a0b0877fb963ae7bf8f8f4d27cf5b08eceff6f9`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 11.5 MB (11500465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa007e54c239fbfbe5087cb47ca43af4a7d1df694c5e8a8020174726c19a42`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eac2879e0c6b2ac36eace93767cf632bd46666df09233d59b0a518e37b7db9`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd62ce6834bda03604f319f34b2e62bba14e067be7c7ddb22397f7ea2e79fa12`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 101.1 KB (101100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:59c273c7a6c7e3b8553acd2497cdf98e3326e7e781c78906f5307b20777714b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2aebc2a7ceb47599386a1c4acdac11b4bcb10218d9198e6d60bf8fcc08caa2`

```dockerfile
```

-	Layers:
	-	`sha256:0d3e045b8fd612a40cd1c751b642873c3f741adfa5c7e7401fcc6f79f04bd152`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 4.2 MB (4231172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105b1585b3731f8a7f5fe4b7d5575ba9daff42547c16e7c4c8d5b850660363ef`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 14.0 KB (13980 bytes)  
		MIME: application/vnd.in-toto+json
