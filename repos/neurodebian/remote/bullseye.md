## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:3f297160a19ea8ec16f983d5ce3171d63da3045d1b991019f8fa553acef21112
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
$ docker pull neurodebian@sha256:74236c937c5b037ad60fc432ebc254c1e580993ab29f478a9b300daa626bb915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3adae40b3c213aa1ae0712e9060a41aaf499df6ccdbd746f19223f35ec6827e4`
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
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb0a6060b8b0998db2e10892443ef142934b0ef2830beee3e3e7cfe4514bd9`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11104992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d5910828d32d02f070dba4e7945868769def79e0f9902c66830608d68aa481`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be85d64ab216d005b467f6308b5615d673e978f19c236082f992bdaf4ad93bc8`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 101.2 KB (101161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bc6eb256921208f76e8b28589cf11cc18adca9cfe24fed607071a4661686462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56e3b7a65d4bc869c344278645e4b1720f997dbd966ddf3e536b74e2805f59`

```dockerfile
```

-	Layers:
	-	`sha256:29d56d4669ef53c2f9a8c6678f2b9a0ae5aca6a32c1944ff8aec60b1b297320a`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 4.2 MB (4223717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2583fb1f95ef1984a58e4586f792e94a80ff50ed736cd3b33c28bfd5be697f3f`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f8213b6341b1bd416e1b73705a77c5227eb076fbda50c1b61fcd15c711751a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64940530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5805688720b5f4b15de238d4d61f07be3d1b0eefd9289054e89a2edea0cf0d`
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

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:55bc3810d671d847ecc66841d51d017ec8540ed69cbe03815513d4d976f05b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad28e0a95f8254034c3f6e0f85bddea0f76763c2a1a9b2ad5aff778d69795b6`

```dockerfile
```

-	Layers:
	-	`sha256:0d583b4965a88051bb19cd82140b6cdf8b6061f04c587e3a03729578e52f4acf`  
		Last Modified: Thu, 05 Sep 2024 12:35:11 GMT  
		Size: 4.2 MB (4223309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa866db050febfc23f2a557d0e06f92e5c9275ed20dee19a24ea3179a6343a3`  
		Last Modified: Thu, 05 Sep 2024 12:35:10 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:96fe4aae67000ad6550f8e6838709416ceab4f74feb9a1a90cff0c1d77d09d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef01da747f6f76c43b94466e8820aed5df2c186c69932d123b5ada9592911e2a`
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
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a943fde0ebcc219ed5be7a65813a44fd9ae078d1b63ebf63c5da678c99be32`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 11.5 MB (11500208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13415e438d502909f21cbd42d54392b1c1305ef218c1e306f811304d6979e7e0`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c19e1db6c281b76dbd156756d08b252509adc87346da5e11d53521a449f86`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebf1edbb66dc5cf0ded190f867405852068a545f2611eeb6af9decaec8470f6`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 101.1 KB (101061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bbd87945b96ceeba117e56bb2f8cfa4a6ec9224ad3b8f7bcf9f3c092882b83f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b42e85f12377a98e9ea3ff307f1a0e95c144db6a4aaa4d2797138ac8df80f`

```dockerfile
```

-	Layers:
	-	`sha256:125cb6ca9c69dceaeaf638763b1dee8b881dbdaaff4d69680342af0d71b50954`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 4.2 MB (4220164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefe7ff2bc097e2bcb6e8df83f2a1f83fed570e02fdb005a542c2e15d0b65ad6`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json
