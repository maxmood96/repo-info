## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:0541e9e3ec85bdd9009a7631ecac81c9e16df7b8650841f839a807074ba1253f
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
$ docker pull neurodebian@sha256:e0bf514a0d34ecdc8b002e7b22cdd78068a509b97bb1cecc113fc3b4b8066a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33b8d06712b2ab86f0d1b6ee95c1732a91b184078d2afe46f52226a4c5dcee5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
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
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a181a4a3c4cf0bf326ca6d6ce4a6acde2cec0980c6164d6364aac4481ade0b0`  
		Last Modified: Tue, 02 Jul 2024 03:19:32 GMT  
		Size: 11.1 MB (11105038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21225520f7ff518fe183256cab94da710e68586dc6e8b7929b637e7ed0cf96b`  
		Last Modified: Tue, 02 Jul 2024 03:19:31 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2978eb695fe78a3741a7e22bb9251e99406a5d65c6e3d2e4904c9286bac48c8`  
		Last Modified: Tue, 02 Jul 2024 03:19:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e8221f8ce0d5a15c0fc3a0d7208cd3bec1bec51c813bf19b825decdb73bfbf`  
		Last Modified: Tue, 02 Jul 2024 03:19:31 GMT  
		Size: 100.8 KB (100761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2f4c9f413303bbc8b960824fbc95b20b625f2311edc3e98852fbb2bd66abd3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ba2645f04d3eb21b231fdf99e9586136f6ff3b2fe63b13f6dba135c7a861e3`

```dockerfile
```

-	Layers:
	-	`sha256:e44f79f1ace122ac207115246bfcfc9b02de8c6951a412ef5855f851599c1831`  
		Last Modified: Tue, 02 Jul 2024 03:19:32 GMT  
		Size: 4.2 MB (4198737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e12ba6b2875bec7706c65a98634ba58d08c1b93ea121457c42bfa95d58eb44`  
		Last Modified: Tue, 02 Jul 2024 03:19:32 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6375cf81339b4fe8833e60dd040bba97488912c84f70a27969bf2c02cb91eb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64948102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cccd4fdc6edb0a9eb9ba879aed966c878fa3c91107b142797379907bc3544c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ef66b54f3529cd7df198490a60a02b9a4e099ea4456cbc230affa6271d7be`  
		Last Modified: Thu, 13 Jun 2024 19:36:08 GMT  
		Size: 11.1 MB (11105804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf9da50bd694d2938f66745014033d7f272e00c04af58b00384767df0a68779`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d1d085e2488d140f07257a03441112598facbad0671d3f6d3aca4474943da`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6ba47d152985a5fc3c5a383c539496f19f49199c0ba685819566962b387f7`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 100.7 KB (100727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1c099f797210a667e7d6cad5d156c3d71f62da503f81a223646bcdd633e96a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8dc943f053d5cd12505c6b7e69aaee75831d571e6af2c7e94d81ad4f930220`

```dockerfile
```

-	Layers:
	-	`sha256:a87d80d664052af77129cd34468764c3ca1b059b7b914aa236360b86b3b423f3`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 4.2 MB (4198659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e892dffc23567a9acb656fd89cad3615575761a771ef3db6d1c63b06192d2edb`  
		Last Modified: Thu, 13 Jun 2024 19:36:07 GMT  
		Size: 14.1 KB (14078 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:019cf6b18fa8d325c364835a127dd355233f0dd1667463a407b05e7d9f2a5e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67667751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c620322fd7504ee091a4c60dab413cb848763328a7919d1ab43d65fcd6a8fb4f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e6fa59569d6234c463e39f7c2465f2984240a5e8cd613c1ffdc14ab3abb4a7ad in / 
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
```

-	Layers:
	-	`sha256:72a2b38d7f88bb9b0be6097180e8f8261c31815017cb512a158422c2bfba6973`  
		Last Modified: Tue, 02 Jul 2024 00:43:02 GMT  
		Size: 56.1 MB (56064975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313658cba670b69704c21bb3b6cd683cf6bb3d4ee71081c8254b350ce53ae86b`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 11.5 MB (11500171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be962056235be3484050152106eaef9d76a079efc4e0fb9f08c53e92a416b780`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d583c35d672ad69bc748fe666b938bb584c780453ed5b17549c6a4ac885221a`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bea244501331be599fdb702ea10f34d3bd162e65df75233b62c5f9fbe99bf91`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 100.6 KB (100620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ddd6924651e6101933be098f3d127561d6a42c9b386055efc3d0f6bbc0ac0630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7b1d3f3797a1c1f8b72c58e52c089ccbd17adaa20008d6171a072bdddef92a`

```dockerfile
```

-	Layers:
	-	`sha256:2df1b56ccd97b78fb638bf67ea0fefabef37e722fd606934f889c027be4686b1`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 4.2 MB (4195197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e8f5abb370649cfb19b1cc40973f4cd40ae43c2f5348990ae6f582df1c7ac6`  
		Last Modified: Tue, 02 Jul 2024 03:19:25 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json
