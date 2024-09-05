## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:1a080784968bc97b96dc31b596682a891236ab597c97ca532ac4388b4291cfd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

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

### `neurodebian:nd` - unknown; unknown

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

### `neurodebian:nd` - linux; arm64 variant v8

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

### `neurodebian:nd` - unknown; unknown

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

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:47e9bd51827b95feb3e89dafb8583ce8284ef80b888788217dd848b70dad7bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60713448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f4a1a27925112fe41435fa83cfd95c4928b7444cd5434e7dd4b8600b10bc5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
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
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be375743549e0e68564be0499e767c21b7af02c63b8ba6f9874033b7f6989ab3`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 6.6 MB (6587194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98205be1f0f5dea8ace51fc072e692d4ab82ba96a4fa4335fdebb86f2626de82`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf2c5a5226cfdbbcc8b7cf7d0fbc26605fb419d066536422b107cfcd038cac2`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bb3a2800a6b50bcbe14a55b7c4fd0b0ee771e18724d9c5161a7cf486e89064`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 91.0 KB (91010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb2ae32120e24d66fd2c6c77a0d0cb956f8efe63f86d9c563091a9e32530db17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aba443d0e9003cab1e91957153eaf624b50f534608f7beb882d2dc05b166e6`

```dockerfile
```

-	Layers:
	-	`sha256:5fc9f96a0b5046f5dc84f7d0af6bd76e7bb2feb421e41b5aa4a540df22a3fecc`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 3.5 MB (3529559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdfcc25e7f8ad25b6b9bc46f6d0ceba849c15760996ea088413aaffda4a06d4a`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json
