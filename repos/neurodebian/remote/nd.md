## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:c99a320f5b489b4b9fd685aa70c861a8e77a3129f3bb1c530d0922b327c88221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0ffafd9fe3daf7efd5f712fc3d053b225086b1827a78e47db5a7431e4be36f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61246246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bdf78211984955858995b9d812f932ac9d4b78d162415e9b8f88e9d3cb9507`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:57 GMT
ADD file:742621d60641957542e01d843bc130e616ba577a7135783b21e53d3a5d77ad5b in / 
# Wed, 01 Mar 2023 04:10:57 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:45:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:45:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:45:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:45:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d80cbe2ffd4f13cce276662ea5b4fa412791129d545137a4bea79fc41c446e0b`  
		Last Modified: Wed, 01 Mar 2023 04:15:57 GMT  
		Size: 49.3 MB (49261286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f07b40e7e9f706f89a559924ad512bd3b0c4f082e17184a96aa7d5540686ce`  
		Last Modified: Wed, 01 Mar 2023 16:46:58 GMT  
		Size: 11.7 MB (11701184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b804ea73e1c67b7cfd483b59108eef0df77751aba531e24ec8a07c192cb6ab37`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09103778873997bf9915a011675211eb2bc00c9e387b1d994fbbf3af88764138`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cb9fe54ae4e96671ce48bdda7ffbe70f0eef14b7e934156aab2e1fae345d12`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 281.8 KB (281768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b922cad3fe5d3b4160ae7b3a5e81a57639a85513db1e474d1ec0eef9c6590bd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61240710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d236ae8b1b48090ac45a3c137236d2519bd66c888ac05b2259490ed82bab035a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:21:20 GMT
ADD file:83e31d97e59fa435e4367903bc4de14c4bc67178b21cea27910cd23f23eb3a80 in / 
# Wed, 01 Mar 2023 02:21:20 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:01:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:01:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4362be0bd44228649833bb1416738fd1e9e110c9b44995dc7b36d6f6c712645f`  
		Last Modified: Wed, 01 Mar 2023 02:25:46 GMT  
		Size: 49.3 MB (49295339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b38c660fc12919553d4c7aa5bc89004fe56e8844231dce893e94984fe56dc23`  
		Last Modified: Wed, 01 Mar 2023 05:03:00 GMT  
		Size: 11.7 MB (11661138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc19c97c2997b743d321faeb9616b3a6e870b9fce608c572197aeab2f394c594`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9217cf8b3cf849d5480f0b028fe5a6a95663fa518c91e44ada3d8c7e086baf`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a238e1cc1f54ddef9247ec8bf508b59a49995e1564a673f8947751096ea9f5`  
		Last Modified: Wed, 01 Mar 2023 05:02:59 GMT  
		Size: 282.2 KB (282223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:f528b19cc612f1d1444e5a4e3a3acf883bfca110b57d86b7f6f1e244c844f371
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62722827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5387b36ce2af622c1e0eba8fe0b4347ccf401180723bdcb1bd9eee565933a3a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
