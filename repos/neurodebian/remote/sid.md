## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:92e10b28c7a95509d22c284e3d8964a4795db576eb34479822aff72abc0e8ce8
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
$ docker pull neurodebian@sha256:1301c742eca91b58603a2667eff6b9eac6327001ed41f8a042f8618eae9c8662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b82c3e9dac515c8134f33569cc8a7c6cdaf0d6223e596d964073c16c9ffc04c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
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
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408855a53c5bbe2210b3acb92872348f336eed207c1fd565aa9a1894ae3360d7`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 6.2 MB (6248358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513957bcba9f74ca0a80d4f0d2a013c85dedaca9c3d7851562387b57f917f6d2`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b06fa225e64f5f4e0e613985a5fad9decc48bec4c0f6976a7c73a3096c5526`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda73a6bab6cbe0f0ae9577ec42d105d5e08ef05319ea5926169e01c3432901`  
		Last Modified: Thu, 05 Sep 2024 12:38:02 GMT  
		Size: 91.8 KB (91770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78765ff8458b22fec7849265d6db5e083ef24bd5997d278ca662573e4c2314fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27035daa77873055b6fe118538dab410d735292df50392b62c95dcce7efe76a`

```dockerfile
```

-	Layers:
	-	`sha256:83f31aa3a32586e88b0dd27a9dec574b3e8408e8b0e10dbc3ed2ed6c3916214c`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 3.5 MB (3533502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e375418842be8be11aa86a2f2bf098785a3774a084a21041582157fdf98117f`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

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

### `neurodebian:sid` - unknown; unknown

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
