## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:9e085870cb694cf3b669663a1b243a092c0b330bbafd92c3d7c01682ba8ca0d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:d5b072a5141a86dd1d2500e0c66407e895b6a7cd02772fca2ad2953e01036964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59510892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986472010412306b6437bd6a1fb9bdce5785924d8b5f20a8a1208d6c5635ee52`
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
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034bc937277199ec164847356d05777d74634f8f5f05723bd208cb3eb6138b78`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 6.3 MB (6260893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b77db3a43cb43615e3531865bc65936809125b4da8289276926163d9c2d30d4`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f157f39a62fa798f416a12a4fbcc54c4d50bd039d2428ab32c79c125e0c5874`  
		Last Modified: Wed, 04 Sep 2024 23:11:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f02174b8243c9482bc3bd0e6ee8f3ee77adf56b32417414cddb12cce0e13f62`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 91.2 KB (91162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1717a43a3dd14a94d30142710e223970593b56d0f5309f2ee6294f49cda02ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26637a4026d86d363cc068a6499ad746ffd2cbb35b7e93097653df757a8a92b0`

```dockerfile
```

-	Layers:
	-	`sha256:9c5747490dd0983fcbe9f53c25f5f90cfa0b682f70fd6b32283a230b556d8b4a`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 3.5 MB (3532460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8625fdd4ee91d417fb4bb1b9f41a818c610a6e5b6b07f6806186a3aa72e0def`  
		Last Modified: Wed, 04 Sep 2024 23:11:03 GMT  
		Size: 13.4 KB (13397 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c24554d2b03c88038671f7dd363e185920cb2c3d56fe292a23a6b5316ca9e5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59483897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25afc236d3afba5d4a0961256a2b5fbfcd0bc83d16154e306ed3f4ca8f718d7c`
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

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:565ddfc6af473f19ecdd32e26652054091c8686db3a9e305d6c86b6dbfee0622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8188b1f100e1b01a87195c48287ad47b85c7865a2ce5a2a8226ff6f5ddd1f6af`

```dockerfile
```

-	Layers:
	-	`sha256:06f04d1df7ab382a4d8f77d2d144bf4aeba6c4ab3fafe199d4e33a6bd92251ed`  
		Last Modified: Tue, 13 Aug 2024 07:42:26 GMT  
		Size: 3.5 MB (3533440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b4482dded10009090fd2f781e3e4583a565934f8b5e80fcdd3e3a36123f242`  
		Last Modified: Tue, 13 Aug 2024 07:42:25 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:2d7295e78c1f93e93a2fafe3cf5d6578c9bd04ba3e70aeb1ac00e4ab6a423853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98da68791e8c85b2337b5ace3354f2cf5c2661f1890b36c48faa684596d1a893`
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
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0659bfc4fa78a1d35cc72364a5ae98ac8f4d07bd69d5519d26f5a17cb400a074`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 6.6 MB (6566071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8727d0f61d96321e8ca009fce720e24d7cc8b2eef994ca6bc4de03fca1eec706`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a36b20258ae61eb5dcc9eb1db3b6f8b4cc8dd1758e38b36d1ba0854ca92f`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08afb7bac914d3affff0a203687d081a71dfea865fb144968f617538c675d23`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 90.7 KB (90690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a550bba3856e784dc5634debe1d9eaa3713a572c52b7a21ec54d73e0c2cf13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab79690e1cadf319dd8b38d9a493570fc9e9c614dacf0dae87dbb78b2feacbdf`

```dockerfile
```

-	Layers:
	-	`sha256:1a0d28cdbf8efae3239dea7c48eb32f819b4f35eaba78d926a86bda35ae7add8`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 3.5 MB (3530303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c286a639d57592fa8d3072963de485396b9c4aab261687c908e99b643ae588`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json
