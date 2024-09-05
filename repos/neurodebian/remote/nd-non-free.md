## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:299a54ccfcf4ed7b643740603c1abf80e811c5ee8215e3065b305e8fb0ec9dcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:26a59f612ed56a4697f366a60a77194f5641af54e9a1664a020ed586da6d71f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59511253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f2ad76884e7f344ab5b0e055a2b96cca37774aef8be383075916292182c8af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2c007c64da352ec00a7c770959f382104c4122028f01d19283f85f7c5196e5`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 6.3 MB (6260869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e19ed26657edb9a90abf530ae502f28e31e1fcceca1c8faa0c42eca3a5984c`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d3b2c132c8026f38909d51e7a45f40fa7d65bfad4af42b8ff1cd3cae31b32`  
		Last Modified: Wed, 04 Sep 2024 23:10:59 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5389944352d641fbf5d89602026b8119d8cf060cbdac213da804dbba99554b2`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 91.2 KB (91154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a05ede3e7172d449e69bd39da700fee287c4bfcf237b04a327d7c64236ff83e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bc86531131eff71b8b0308bd0c49133fb6956878d87c78527fb4d8c92332daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c70794af3101644cfd9922da9e9cf1d6e31f20c36f21ce04b23f581344a9ef`

```dockerfile
```

-	Layers:
	-	`sha256:2dfae5164f018ebc1798d623dbc99edff836f35311794491eaf4a62521db0c5b`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 3.5 MB (3532496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155d36edcf9182b5d9cd047985eadbb745b640d0e8d69fb82d6ffba6986d16e1`  
		Last Modified: Wed, 04 Sep 2024 23:10:59 GMT  
		Size: 15.4 KB (15428 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7f830e4e2c2d4d6fe4727b5f3c67cef86820ab5773bf9fefac3d72d524451a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a40f7d644f46a12c3166e7f144ef587ae0b9d775bf582804a5923c9540f11c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d3aa31e5e33290bb28cfd74e2b2a88ce7e4415dc0d995c3c39d36c332bdbfcf in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:543c0d8816b61b146fc103b18d6ec335253cba7bad9fa7f1cb3e794a6b9e450c`  
		Last Modified: Tue, 13 Aug 2024 00:44:13 GMT  
		Size: 53.2 MB (53155250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02191b116647481476d52030a803e28ba5e68be75a6620aa17907059437da993`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 6.2 MB (6235299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49fc1a3149682d8a81b651e3c53dcdbb45d3ae5b19c1abed966b8e7ff9ec25`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f53b0fdfbf88451067600990b58000941f44e8fb25d7f56a2040f4c02e5f88`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab9ebaf49832bc2e70ff76ed23a0cd70d02d5b8c5853db5f86181077c727f6`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 91.4 KB (91368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c01f4db884a7e9e5e03a2c3a4f148b5eae1fd576626b29c6eb6ec84ab7abcb`  
		Last Modified: Tue, 13 Aug 2024 07:42:44 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f7a4d4e88328b2a38b7d20e94dc0f3436ca1ad4f9d60b0c983d6c2f136e7ed18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97881e2fcfabb0b2c1d5bbdf55f7996e98f77c400d6e133a047a29729f74e0e6`

```dockerfile
```

-	Layers:
	-	`sha256:346da81b252618de9c218de26e73488c09966414f4b1c0e07c5e8b3c58bba1bd`  
		Last Modified: Tue, 13 Aug 2024 07:42:44 GMT  
		Size: 3.5 MB (3533476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e52f58fee8fab48fa3131808e449368a6cda85d7f168728764bbfdedbf9d3ee`  
		Last Modified: Tue, 13 Aug 2024 07:42:43 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3879645d8248e19c7cecc51e81e443dd2244460b4f358cfeb57cb286852c04a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb0d7cc60a97195c40904e7573f816efef7d6f12cc2155af4cfb3e20b788da`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b71d132a4344bb16e2e09fd83117250f48d572c643b3a712f89502bd494932f`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 6.6 MB (6566180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b92d44337ab2e36cf50dbb0e5f5a982aedb8ea031edfd566ea77794b8600db`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83d54a7d8728387f810ef105293ffd3ecdbe46c909d35465dd6ac692a203a66`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c86223c48237f67a081fdc1da5b575bca1e0b24ca39b18348f604b229ec46a`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 90.7 KB (90739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c730d96f05d4551706957182b16dc3e0b695f848bc18e53ac8a87794f7bc71b5`  
		Last Modified: Tue, 13 Aug 2024 01:12:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:afa48e552f3090b92141c3f16761ea91ebd9c37674b87f9131690f18413b23a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc69503183698682084ccc15450c076f8942d02054a333aa86200e39f668a11`

```dockerfile
```

-	Layers:
	-	`sha256:d17136678b054f4bbd69c0d37627fc779e2d83be22dc0d59ec71ef570984beac`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 3.5 MB (3530339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1d4f4372fabf850ce1ffa73ac663ea1660175de7920a8b704f09006156321a`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json
